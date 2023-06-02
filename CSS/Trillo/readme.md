# Flexbox

- Is a new CSS3 module that makes it easy to align elements to one another, in dfft directions and orders
- Givves the container the ability to expand and shrink element to bst use all the available space
- Replaces float layout, using LESS
- more readable and logical ode

## Main concepts

> To define a flex container

```css
display: flex;
//or
display: inline-flex; //container beaves as inline-element
```

Flex items = direct children of flex container
Main axis = The direction in which flex items are laid out
Cross axis = Perpendicular to the main

> The direction of main axis can be changed

### Properties

**Container**

1. Flex-direction: `row` | row-reverse | column | column-reverse
2. Flex-wrap: `nowrap` | wrap | wrap-reverse

   - How flex items bahave in multiline flexbox layout, n when there's more space

3. justify-content: `flex-start` | flex-end | center | space-between | space-around | space-evenly

   - alignment along main axis

4. align-items: `flex-start` | flex-end | center | space-between | space-around | space-evenly

   - alignment along cross axis

5. align-content: `stretch` | flex-start | flex-end | center | space-between | space-around | space-evenly
   - onl if there's more than one row/col
   - algignment along cross axis

**Flex item**

1. align-self: `auto`

   - applies to one specific item,
   - overwrites align-items

2. order: `0` | int
3. flex-grow: `0` | \<int\>
4. flex-shrink: `1` | \<int\>
5. flex-basis: `auto` | \<int\>
6. flex-grow: \<grow\> \<shrink\> \<basis\>

# The Trillo project

1. Defn

- Custom properties set to include colors and shadows
- Only `main.scss`, `_base.scss`, `_components.scss` files present

2. Overall Layout

- huge overall container tat contains overall app
- In the container;
- 1. Header: logo, search, user nav
- 2. Sidebar: sidebar
- 3. Main block: content

### 3. Header

- Using SVG icons
- Finding, generating and using SVG sprites
- Changing color of SVG in css
- Advanced flex-box alignment: `justify-content`, `align-items`, `align-self`, `flex`
- Res: [icomoon](icomoon.io)
- **sprite.svg** is a sinlge file that contains all the svg icons. It loaded once from the server

```html
<svg class="search__icon">
  <use xlink:href="img/sprite.svg#icon-id"></use>
</svg>
```

> `input` elements donot automatically inherit font-related styles
> Set font styles to `inherit`

_refer to the scss files to see how the layout is coded up_
_this only serves as a reference to easily fidn the features you'll later look for in the projects_

### 4. Navigation/Sidebar

- Creative hover effect using multiple transition properties with dfft settings
- The `currentColor` CSS variable

### 5. Hotel overview

- creating infinite animation
- Using `margin: auto` with flex box and why it is so powerful

### 6. Hotel description part

- Using `flex-wrap` to build a multicolumn list
- Using CSS masks with `mask-image` and `mask-size`
- There are nice cards and list elements used in this section
- Building multple avatars with `border`

### 7. User reviews

- Block quote icon
- Expanding button effect
- Using `figure` elements

> `figure` elements are not just for images. They can be used for cards etc. E.g;

```html
<figure class="review">
  <blockquote class="review__text">
    Quae labore minus minima amet est at eaqueet corrupti excepturi inventore
    aliquiipsa, magnam quam expedita repudiandae. Lcum!
  </blockquote>
  <figcaption class="review__user">
    <img src="img/user-1.jpg" class="review__photo" />
    <div class="review__user-box">
      <p class="review__user-name">Nick Smith</p>
      <p class="review__user-date">Feb 23rd,p></p>
    </div>

    <div class="review__rating">7.8</div>
  </figcaption>
</figure>
```

### 8. CTA section

- Cool hover effect button

### 9. Writing media queries

- Flexbox makes it very easy to optimize the design for dfft screen sizes

> Use [CanIUSe](caniuse.com) to check the browser compatibility/support of dfft browsers
> Note there are also feature queries to check if the browser supports certain features. e.g. The `mask-image` feature
