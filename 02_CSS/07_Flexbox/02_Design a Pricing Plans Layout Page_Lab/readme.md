# Pricing Plans Layout Page

## 1. Project Structure

### HTML Overview

```plaintext
<body>
  <h1>Pricing Plans</h1>
  <div class="pricing-container">
    <div class="pricing-card pro-plan">...</div>
    <div class="pricing-card basic-plan">...</div>
    <div class="pricing-card premium-plan">...</div>
  </div>
</body>
```

* **`h1`**: Page title, displayed above the pricing cards.

* **`.pricing-container`**: Flex container holding all pricing cards.

* **`.pricing-card`**: Individual pricing cards containing:

  * Plan name (`h2`)
  * Price (`.price`)
  * Features list (`.features`)
  * Call-to-action button (`<a>`)

* Each card has specific classes (`.basic-plan`, `.pro-plan`, `.premium-plan`) for **ordering and styling differences**.

---

## 2. CSS Styling

### Body & Layout

```css
body {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  min-height: 100vh;
}
```

* Centers the entire content vertically and horizontally.
* Sets a column layout for stacking page title and container.

### Pricing Container

```css
.pricing-container {
  display: flex;
  flex-wrap: wrap;
  align-content: center;
  border: 2px solid #000;
  gap: 20px;
  width: 80%;
  max-width: 900px;
  height: 70vh;
  padding: 0 20px;
}
```

* **Flexbox container**:

  * `flex-wrap: wrap` allows cards to wrap onto multiple lines if space is limited.
  * `gap: 20px` provides consistent spacing between cards.
* Responsive width:

  * `width: 80%` of viewport with `max-width: 900px`.
* Height set to `70vh` for initial large-screen layout.

### Pricing Cards

```css
.pricing-card {
  flex: 0 0 200px;
  padding: 20px;
  border: 2px solid black;
  text-align: center;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  transition: transform 0.3s ease;
}
```

* **Flex properties explained**:

  * `flex: 0 0 200px`:

    * `flex-grow: 0` → card won’t grow by default.
    * `flex-shrink: 0` → card won’t shrink below `flex-basis`.
    * `flex-basis: 200px` → starting width of each card.
* Internal flex column for content distribution:

  * `flex-direction: column`
  * `justify-content: space-between` ensures price, features, and button are evenly spaced vertically.

### Plan-specific Styling

```css
.basic-plan { order: 0; }
.pro-plan { order: 1; flex-grow: 2; background: #f0f8ff; }
.premium-plan { order: 2; flex-grow: 3; }
```

* **Order** controls the visual sequence of cards.
* `flex-grow` allows some cards to expand more than others when extra horizontal space exists:

  * Pro grows 2x, Premium grows 3x relative to a base unit.

---

## 3. Responsiveness (Media Queries)

### Medium Screens (`max-width: 1000px`)

```css
.pricing-card { flex: 0 0 175px; }
```

* Cards shrink slightly to fit smaller widths.
* Container height becomes `auto` to adjust dynamically.

### Small Screens (`max-width: 650px`)

```css
.pricing-container { flex-direction: column; height: auto; }
.pricing-card { flex: 1 1 auto; width: 100%; }
```

* Cards stack vertically (`flex-direction: column`) for mobile-friendly layout.
* `flex: 1 1 auto`:

  * `flex-grow: 1` → each card can expand along the main axis (height in column layout) to fill available space.
  * `flex-shrink: 1` → cards can shrink if needed.
  * `flex-basis: auto` → height is determined by content.
* `width: 100%` ensures cards take full container width.

---

## 4. Features & Styling Highlights

* **Hover effect**: `transform: scale(1.05)` adds interactivity.
* **Price section**: Bold, larger font with a subtle bottom border.
* **Feature list**: Green check (`✓`) for included features, red cross (`✗`) for unavailable features.
* **CTA button**: Styled with background, border, and hover transitions for user engagement.

---

## 5. Flexbox Behavior Summary

* On large screens:

  * Cards are **side-by-side**, wrapped if container is too small.
  * Extra horizontal space is distributed according to `flex-grow` values.
* On medium screens:

  * Cards shrink slightly in width to maintain layout.
* On small screens:

  * Cards stack vertically, `width: 100%`.
  * Flex-grow affects **height**, so cards can expand equally if container height is set.
* `gap` ensures consistent spacing regardless of wrapping or stacking.
