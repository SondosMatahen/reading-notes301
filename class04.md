# Read 4
<hr>
<br>

## A Complete Guide to Grid

CSS Grid Layout is the most powerful layout system available in CSS. It is a 2-dimensional system, meaning it can handle both columns and rows, unlike flexbox which is largely a 1-dimensional system. You work with Grid Layout by applying CSS rules both to a parent element (which becomes the Grid Container) and to that element’s children (which become Grid Items).

<br>

## Properties for the Parent (Grid Container):
<br><br>

* display:Defines the element as a grid container and establishes a new grid formatting context for its contents. 
Values:
grid – generates a block-level grid
inline-grid – generates an inline-level grid

* grid-template-columns or grid-template-rows:
Defines the columns and rows of the grid with a space-separated list of values. The values represent the track size, and the space between them represents the grid line.
* grid-template-areas: Defines a grid template by referencing the names of the grid areas which are specified with the grid-area property. Repeating the name of a grid area causes the content to span those cells. A period signifies an empty cell. The syntax itself provides a visualization of the structure of the grid.
* gap grid-gap: A shorthand for row-gap and column-gap
* justify-items
* align-items 
* place-items
* justify-content
* align-content 
* place-content
<br><br>
<br><br>

## Properties for the Children (Grid Items):
* float, display: inline-block, display: table-cell, vertical-align and column-* properties have no effect on a grid item.
* grid-column-start ,grid-column-end ,grid-row-start ,grid-row-end
* grid-column
* grid-row
* grid-column
* grid-area
