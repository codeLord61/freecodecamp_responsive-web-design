# Parent Teacher Conference Form

This mini project focuses on building a **semantic HTML form** and applying **custom CSS styling**, with special attention to **custom radio buttons**, transitions, and smart selector usage like `:not()`.

---

## 📐 Semantic HTML Structure

The form is built using semantic and accessible HTML elements:

* **`<main class="container">`**
  Acts as the primary wrapper for the page content.

* **Headings and descriptions**

  * `<h1>` for the main title
  * `<p>` for a short explanation
    Both are centered using a reusable `.center` class.

* **`<form>` with multiple `<fieldset>` sections**
  The form is organized logically using `fieldset` and `legend`:

  * Student Information
  * Parent/Guardian Information
  * Preferred Contact Method
  * Additional Notes

  Using `fieldset` first makes the form:

  * Easier to read
  * More accessible
  * Visually grouped in a meaningful way

* **Proper label–input pairing**

  * Every input is associated with a `<label>` using the `for` and `id` attributes.
  * This improves accessibility and click behavior.

---

## 🎨 CSS Layout & Styling Approach

### Overall Styling

* Dark theme using:

  * `background-color: midnightblue`
  * `color: whitesmoke`

* Semi-transparent container background using **8-digit hex color**:

  ```css
  #ffffff1a
  ```

  This adds opacity using the alpha channel.

* Centered container with:

  * `max-width`
  * `margin: auto`
  * `box-shadow` for depth

---

## 📦 Fieldset-First Styling

All form sections are styled consistently:

```css
fieldset {
  border: 1px solid gray;
  border-radius: 5px;
  margin: 20px 0;
  padding: 20px;
}
```

Legends are emphasized using larger font size and heavier weight, making each section clearly identifiable.

---

## 🧠 Smart Selector Usage: `:not()`

Instead of styling everything individually, the `:not()` pseudo-class is used to **exclude specific elements**.

### Example 1: Stack most labels vertically

```css
label:not(.contact-method) {
  display: block;
  margin: 10px 0;
}
```

This keeps normal labels stacked while allowing radio button labels to stay inline.

### Example 2: Exclude radio buttons from general input styles

```css
input:not(.contact-method-radio-btn), textarea {
  width: 95%;
  padding: 10px;
}
```

This prevents radio buttons from inheriting styles meant for text inputs.

---

## 🔘 Custom Radio Button Styling 

Default radio buttons are replaced with a fully custom design.

### 1️⃣ Remove native appearance

```css
.contact-method-radio-btn {
  appearance: none;
}
```

This gives full control over styling.

---

### 2️⃣ Create the outer circle

```css
width: 20px;
height: 20px;
border-radius: 50%;
border: 2px solid gray;
```

---

### 3️⃣ Add the inner circle using `::before`

```css
.contact-method-radio-btn::before {
  content: " ";
  width: 10px;
  height: 10px;
  border-radius: 50%;
}
```

The inner circle exists even when unchecked—but is hidden using scale.

---

### 4️⃣ Smooth transition animation

```css
transform: translate(3px, 3px) scale(0);
transition: all 0.3s ease-in;
```

* `scale(0)` hides the inner circle
* Transition creates a smooth animation when checked

---

### 5️⃣ Checked state styling

```css
.contact-method-radio-btn:checked::before {
  transform: translate(3px, 3px) scale(1);
  background-color: lightgreen;
}
```

When selected:

* The inner circle scales up
* Color appears
* Animation feels responsive and modern

---

## ✨ Button Styling & Feedback

The submit button is styled for clarity and interaction:

* Rounded corners
* Centered layout
* Pointer cursor
* Hover effect for feedback

```css
.submit-btn:hover {
  background-color: midnightblue;
}
```