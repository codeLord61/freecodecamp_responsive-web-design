# Designing a to do list lab

## Structure
A container that wrapped the main contents
Container has one heading and one unorderded list element with 'todo-list' class
Inside main unordered list we have 4 todo item lists (class=todo-item)
Each item list has checkbox input, label for accessibility & another sub-item unordered list
Sub item list has list with anchor tags pointing to link in blank tab

## CSS stylings

Set it's max width to 30% of parent container (the full screen here) so that the appearance looks like a thin list and not stretched in wide screen.

Centered it vertically by adding margin top
Centered horizontally by margin left & right to auto

Added padding for space around internal content

Added border radius for the boxes

Centered headings, and added top bottom margin to give vertical spacing and horizontal center using left, right to auto

Removed todo-list class's default bullet icon by `list-style-type: none`
Default ul adds an indention (padding left = 40px), so removed that by `padding-left: 0;`

Added custom list marker by using pseudo element(::) : 
```li::marker{
    content: "➜";
}```

Made the anchor elements inline element to give space between it and custom list marker. Added space using margin left

Changed the list states color by pseudo classes (:)