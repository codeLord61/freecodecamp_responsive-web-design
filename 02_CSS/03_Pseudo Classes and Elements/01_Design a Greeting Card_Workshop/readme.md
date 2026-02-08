# 🎉 Greeting Card Project Workshop

## Overview

This mini project is a simple **interactive greeting card** built using **HTML and CSS**.
The goal was to practice **pseudo-classes, pseudo-elements, transitions, transforms, and the `:target` selector** while keeping the layout clean and beginner-friendly.

The card reacts to user interactions like hover, click, focus, and visited states, and conditionally displays content without JavaScript.

---

## Features Implemented

### 1. Basic Layout & Structure

* Linked an external `styles.css` file.
* Created a main card container using:

  ```html
  <div id="greeting-card" class="card">
  ```
* Added:

  * A heading (`h1`)
  * A message paragraph
  * Action links (`Send Card`, `Share on Social Media`)
* Used semantic `<section>` elements for send/share content.

---

### 2. Global Styling

* Applied global styles on the `body`:

  * `font-family: Arial, sans-serif`
  * Centered text
  * Padding for spacing
  * Brown background color

---

### 3. Card Styling

* Styled `.card` with:

  * Max width and centered layout
  * Padding and rounded corners
  * Box shadow for depth
* Added smooth transitions for:

  * `transform`
  * `background-color`

#### Hover Effect

* On hover:

  * Background changes to **khaki**
  * Card scales up using `transform: scale(1.1)`

---

### 4. Pseudo-elements (`::before` & `::after`)

* Added emojis before and after the title using:

  ```css
  h1::before
  h1::after
  ```
* This enhances visuals without changing HTML.

---

### 5. Message Styling

* Increased readability using:

  * Larger font size
  * Bottom margin for spacing

---

### 6. Flexbox Preview

* Used Flexbox for link alignment:

  ```css
  display: flex;
  justify-content: space-around;
  ```
* This evenly spaces action links inside the card.

---

### 7. Link Styling & Pseudo-classes

Styled links inside `.card-links` with:

* `:hover` → background turns **orangered**
* `:active` → resets to **midnightblue**
* `:focus` → yellow outline (keyboard accessibility)
* `:visited` → text turns **crimson**

Added smooth transitions for background color changes.

---

### 8. Section Styling & Interaction

* Sections are hidden by default:

  ```css
  display: none;
  ```
* When a link is clicked, the matching section appears using:

  ```css
  section:target {
    display: block;
  }
  ```
* Added hover skew effect:

  ```css
  transform: skewX(10deg);
  ```

✅ This allows content toggling **without JavaScript**.

---

## Concepts Practiced

* Pseudo-classes (`:hover`, `:active`, `:focus`, `:visited`, `:target`)
* Pseudo-elements (`::before`, `::after`)
* CSS transitions & transforms
* Flexbox basics
* Semantic HTML
* Interactive UI using only CSS
