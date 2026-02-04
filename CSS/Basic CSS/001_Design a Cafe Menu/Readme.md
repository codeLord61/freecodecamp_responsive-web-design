# Design a Cafe menu Workshop

## What I Built
A simple cafe menu page using semantic HTML and CSS

## Concepts Practiced / Learned

### HTML
- Used semantic structure with `main`, `section`, `article`, and `footer`
- Separated coffee and dessert menus into distinct sections
- Used `address` element in footer for contact info and link

### CSS
- Reset default italic style of `address` using `font-style: normal`
- Styled different link states using pseudo-classes:
  - `:visited`
  - `:hover`
  - `:active`
- Used `hr` to visually separate header, menu, and footer
- Aligned menu item names and prices using `text-align`
- Centered block elements with `margin-left: auto; margin-right: auto`
- Converted image to `display: block` to center it
- Applied `max-width` to prevent layout from stretching on large screens

## Notes / Gotchas
- Block elements can be centered horizontally without flexbox using margin left and right to auto
- Standard (got from gpt): 
  - div{
    - width: N px
    - margin: 0 auto}
    - top, bottom margin = 0; left, right, margin = auto for centering. 
- Images need `display: block` for margin auto centering since it's an inline element by default
- Default browser styles (like italic `address`) need explicit overrides