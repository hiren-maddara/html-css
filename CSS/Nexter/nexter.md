# CSS Grid

- Two-dimensional grid system to css
- Works perfectly with flexbox

### Concepts

Set `display: grid` to turn a div into a grid container

- All direct children are grid item
- Axes (Main and cross) diectiions can not be changed like in flex box

Grid lines:

- Vert. & Horr. that divide up the grid and set up the cols and rows
- Automatically numbered from 1

Grid track: a space between two grid lines i.e rows and columns
Gutter: space between rows and cols
Grid area
Grid cell

### Properties

1. Container

   1. grid-template-rows
   2. grid-template-columns
   3. grid-template-areas

      > grid-template

   4. grid-row-gap
   5. grid-column-gap

      > grid-gap

   6. justify-items
   7. align-items
   8. justify-content
   9. align-content

   10. grid-auto-rows
   11. grid-auto-columns
   12. grid-auto-flow

2. Item
   _grid-row_

   1. grid-row-start
   2. grid-row-end

   _grid-column_ 3. grid-row-start 4. grid-row-end
   _**grid-area**_

   5. justify-self
   6. align-self

   7. order

Grid

1. The `fr` unit: plus others like auto
2. Positioning grid items: using grid track numbers and `span`
3. Naming grid lines
4. Implicit and explicit grids

# The Nexter Project

- Usage of CSS grids

1. Overall layout

```css
 {
  display: grid;
  grid-template-rows: 80vh min-content;
}
```

Defining the template rows

- SHould be based on the dfft sections and their content
  `min-content` = get enough size to just contain the content
  `auto` = adapts to the content
  `vh` = relative to the viewport(browser window) height
  `vw` = relative to the viewport(browser window) width

- Using `min-content` is advisable to avod using any statis values
- `minmax(`min-content`, `1fr`)`

Defing the columns

- Use many equal sized columns to cover the whole viewport
- `grd-template-columns: repeat(8, 1fr)`

- Use grid-line-names. It will be easer when placing items and writing media queries

```css
grid-template-columns:
  [sidebar-start] 8rem [sidebar-end full-start] 1fr [center-start] repeat(
    8,
    [col-start] minmax(min-content, 14rem)
  )
  [center-end] 1fr [full-end];
```

// i.e. A name, before the track size, in square brackets;

- Usage of grid-line names

```css
.selector {
  grid-column: sidebar-start / sidebar-end;
}
```

2. Features section

- Creating grids inside grids
- CReating a responsive design without media queries
- Build even small components using CSS grid

Note

> `grid-template-columns`: `repeat(auto-fit, minmax(15rem, 1fr))`

> This trick creates auto tracks.
> `auto-fit` = Creates as many tracks as can fit based on the defined width. `minmax()` function is used to control limits of the track sizes

3. Stories section

- Deal with overlapping grid items, i.e grd cells over other grid-cells
- Why images are special and bhave dfftly than other grid grid items
- How to tell if flexbox is a better tool in certain situations: When it is a 1-D layout in teh component

4. Homes section

- Build a complex grid component using flexbox and overlapping

5. Gallery section

- complex grid-looking gallery
- Using `object-fit`

Images overflow the containers since they dont have the same aspect ratio. This will create a messy gallery

- Add a parent container to hold the image
- Set `object-fit: cover` on the image itself to make the image cover full and only the size of the container
- It will work only if the height and width are manually set
- Advisable to set images to `display: block`
