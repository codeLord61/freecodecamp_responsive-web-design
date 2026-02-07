## Overall Structure & Semantics
- Created a **single card container** using a `div.blog-post-card` to wrap the entire component.
- Used **semantic hierarchy inside the card**:
  - `img` for the visual header
  - `h2` for the post title
  - `p` for the excerpt
  - `a` for the call-to-action
- Properly linked the external stylesheet via `<link rel="stylesheet" href="styles.css">`.

## Image Handling (`.post-img`)
- Set `width: 100%` so the image **fully spans the card width**.
- Added a **bottom border** to visually separate the image from the content.
- Used `border-top-left-radius` and `border-top-right-radius` with `inherit` so:
  - The image **respects the card’s rounded corners**
  - No sharp edges overflow the card
- Provided a **valid `alt` attribute** for accessibility.

## Card Layout (`.blog-post-card`)
- Applied a **white background** to make the card stand out from the page.
- Used `border-radius: 15px` to create smooth, modern rounded corners.
- Added a **drop shadow** using layered `box-shadow` values:
  - One larger, softer shadow
  - One smaller, tighter shadow
  - This gives a realistic elevation effect
- Controlled sizing with:
  - `max-width: 25%` for large screens
  - `min-width: 350px` to prevent the card from becoming too narrow
- Centered the card horizontally using:
  - `margin-left: auto`
  - `margin-right: auto`
- Added `margin-top: 150px` to vertically separate the card from the top of the page.
- Set `text-align: center` for a clean, card-style layout.

## Content Spacing (`.post-content`)
- Added `padding: 15px` so text and buttons:
  - Don’t touch the card edges
  - Feel breathable and readable

## Typography & Text Styling
**Post Title (`.post-title`)**
- Used a **non-default color** (`hsl(220, 91%, 56%)`) for visual hierarchy.
- Applied margins on all sides to separate it from surrounding elements.

**Post Excerpt (`.post-excerpt`)**
- Used a muted gray color to:
  - Reduce visual weight compared to the title
  - Improve readability
- Added margins for spacing consistency.
- Slightly reduced horizontal margins to tighten text alignment visually.

## Call-to-Action Button (`.read-more`)
- Styled the anchor to **look like a button**:
  - `display: inline-block` so padding and margins work properly
  - Removed underline using `text-decoration: none`
- Applied:
  - Custom text color (`white`)
  - Background color (same blue as the title for visual consistency)
  - Padding to increase click area
  - Margin to separate it from text
  - Rounded corners for a modern UI feel
- Added a **hover effect**:
  - Darkened the background using HSL lightness
  - Creates clear visual feedback on interaction

## Page-Level Styling
- Set a **non-white background color** on the `body` to:
  - Make the white card stand out
  - Add contrast and depth
- Chose a neutral, warm background (`hsl(40, 13%, 95%)`) that doesn’t compete with the card.
- Defined a clean, readable font stack using system sans-serif fonts.