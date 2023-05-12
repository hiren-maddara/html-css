# Layouts:

- The way sections, images, navigations, content are arranged on the page
- html content designed into a certain visual arrangement

## types

1.  Page layout

    - arangement of components into larger elements, and elements in a page

2.  Component layout
    - arrangemt of text, icons, headings, in a component

## Building layouts

1.  Float layouts

    - old way, and hardly used today

2.  Flex box

    - 1-dimensional layout of elements.
    - perfect for component layout.

3.  Grid layout
    - fully fledged 2-dimensional grid
    - perfect for page layouts and complex components

## Flex box

1. 1-D layout
2. Automatically align items to one another inside a parent container
3. Eases centering, creatng equal height columns

**Flex box axes**

- #### The main axis: the axis where the elements are flowing

  _Determined by flex-directon property_
  _It is horizontal in row-direction and vertical in column-direction_

- The cross axis: the perpendcular to main axis

```css
    display: flex;
    align-items: //vertical align
    justify-content: //horizontal : center | space-between | space-around |
    gap:;
    flex-direction: column | row | column-reverse | row-reverse;
```

### Flex container

- gap: <len>
- flex-direction:
- flex-wrap:
- align-content:
  Only works in multi-line flex layouts

- justify-content:
  algn items along main axis(default=hor)

- align-items:
  algn items along cross axis(default=vert)

### Flex items

- align-slef
  To overwrite for individual flex items

- flex-grow: <int>
  all an element to grow | 0 = no | 1+ = yes

- flex-shrink: <int>
  allow an element to shrink

- flex-basis: <len>
  to define an item's width _instead of width property_

- flex: <int> <int> <len>
  shorthand for flex-grow, -shrink, -basis

- order: <int>
  control order of individual items. -1 = first | 1+ = last

**Note**

> Most times it is important to create a new container (i.e div) to layout certain elements together when using flex box
> Even if the divs aren't necesarry

_On sizing_

> If widths ain't working,
> set flex-shrink property
> Flexbox maybe automatically shrinking the elements (flex-shrink: auto;)
> Normalize using flex: 1; to enable items grow to fill all available space (instaed of manually controllng it)

_A tip_

> Note that by defualt block-level children (div, section, aside, header, footer, nav) of the body element flow vertically
> it is unnecessary to control this behaviour using flex box or grid
> It is a simple answer to a confusing question: Don't use flex box or grid when a horizontal is not to be manipulated
> Flex box can be used even if you just want to put a gap btn elements

## CSS Grid

- for 2-dimensional layouts
- i.e divide a container into rows and columns
- allows for less-nested HTML
- Not meant to replace flex-box and they work together perfectly

```css
display: grid;
grid-template-columns:
grid-template-rows:
```

> default values of the grid-template-rows & -columsn is auto
> new rows or columns are automatically created
> depending on the grid-auto-flow property

### Grid axes

- Column axis = vertiical
- Row axis = horizontal

### Grid lines

Lines that separate grid-tracks
Named with numbers (No of cols/rows + 1)
They enclose a _grid cell_

**Grid tracks**

- a row or column

**Gutters**
The spacing btn grid tracks

> Specified by row-gap & column-gap properties

### On grid container

- grid-template-rows: <track size>
- grid-template-columns: <track size>
  Establsh the grid row and column track. One length unit for each track

- row-gap: <len>
- column-gap: <len>
- gap: <len> | row-gap = column-gap = <len>

- justify-items: <keyword>
  \*To align items inside rows / horizontally (top-to-bottom)
- align-items: <keyword>
  \*To align items inside columns / vertically (r-to-l)

- justify-content: & align-content
  To align the grid nside grid container. Works f the container is larger than the grid

**Note**

> - Most of the magic of grid is the `fr` unit
> - Allows for flexible tracks
> - You can set the tracksize to `auto` so that the track only fills the space it requres to occupy
> - Note of allocating items to specific grid-cell (template, named grid lines, spanning, as written later)

> **Make use of block level elements flowing verticallay. No need to assign grid or flex layouts in this case**
> Example are in the [Design] folder projects

_The above discussed guidleines are implementedin the html files (**only grid actually**)_
