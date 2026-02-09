## CSS Flexbox Photo Gallery

This project demonstrates how to build a responsive photo gallery using modern CSS techniques, with a strong focus on **Flexbox layout**, **box sizing**, and **image handling**.

### Global Styling & Box Model
- Applied `box-sizing: border-box` globally to ensure padding and borders are included in element width and height calculations.
- This prevents layout overflow issues and makes sizing more predictable across the gallery.
- Reset default body margin and applied a neutral background color for better visual contrast.

### Header Styling
- Centered the header text and transformed it to uppercase for emphasis.
- Used padding to create breathing space and added a contrasting background color.
- Added a bottom border to visually separate the header from the gallery content.

### Flexbox Gallery Layout
- Turned the gallery container into a flex container using `display: flex`.
- Set `flex-direction: row` and enabled wrapping with `flex-wrap: wrap` so images move to new rows on smaller screens.
- Used `justify-content: center` to horizontally center rows and `align-items: center` to align items vertically.
- Applied `gap` to create consistent spacing between images without relying on margins.
- Limited the gallery width with `max-width` and centered it using `margin: 0 auto`.

### Image Sizing & Consistency
- Gave images a fixed height and a maximum width to maintain uniform sizing.
- Used `object-fit: cover` to preserve image aspect ratios while filling their containers, allowing controlled cropping instead of distortion.
- Rounded image corners with `border-radius` for a softer, modern look.

### Layout Edge Case Handling
- Used the `.gallery::after` pseudo-element to insert an invisible placeholder.
- This ensures the last image aligns to the left in incomplete rows, counteracting the centering effect of `justify-content: center`.

### Accessibility Considerations
- Added descriptive `alt` text to all images to improve accessibility and provide meaningful fallbacks when images fail to load.