# Initial setup

1. Normalize CSS - Set default propertes

```css
* {
  margin: 0;
  padding: 0;
  border-box: 0;
}
```

> Set them to universal slector i.e all elements
> Set inherited properties to the `body` (like `font`, everything rlated to font)

```css
body {
  font-family: "Lato", sans-serif;
  font-weight: 400;
  font-size: 16px;
  line-height: 1.7;
  color: #777;
}
```

> We can set multiple backgrounds using `background-image` / `background` using commas

```css
background-image: linear-gradient(),
  url() // reduce opacity of colors(using rgba) to see other bgs;;
```

> Setting bg shapes using clip path

```css
clip-path: polygon(<x><y>, <x><y>, <x><y>, ...);
```

> starting from the top left corner
> cordinate for every corner
> Think about how many corners the polygon has and how far from the top left each corner should be
> Resource: [clip-path maker](bennettfeely.com/clippy/)

_The image is an inline element, so it's better to put it into a contaner as its parent or as bg-url_

> It is important to put a title of your site in an `h1` element for good SEO,
> Put subtilte ina span el

Note

> Some times to layout elements, one under another (`img`, `h1`, `span` i.e nline elements), use `display: block`

Centering els
**I know a number of ways**

1. Absolute positioning plus transform
   ```css
   position: absolute;
   top: 50%;
   left: 50%;
   transform: translate(-50%, -50%);
   ```
2. Flex box: `align-items`, `justify-content`
3. Grid: `place-items`

**Note**
I won't at all focus on the layout patterns used in this natours section
Because, I'd rather focus on flex and grid, instead of cols, floats, etc

- So it will be about css features like typography, animations

Animations

```css
 @keyframes animationName {
    from {
        //styles
    },

    to {
        //styles
    }
 }

 @keyframes animName {
    0% {},
    50% {},
    100% {}
 }

 selector {
    animation: <animName> <animDuration> <...other props: iteration-count, animation-timing-function>:
 }
```

> `cubic-bezier` function allows us to write custom animation-timing-functon

> For better performace, it's recommended to animation only `opacity` & `transform`

> To removes small glitches from animations try `backface-visibility: hidden;`

> For smooth animations use: `transition: all .3s;`

Advanced animations

- provide default styles for links

```css
a:link,
a:visited,
a:active {
  text-decoration: none;
}
```

Using pseudo elements
`::after` & `::before`
Adds an element besides the `selector` that is not in the html file
e.g.

```css
selector::after {
  content: "";
  display: inline-block;
  //any styles
}

//To animate

selector:hover::after {
  //styles
  //Add animatons as usual
}
```

> animation-fill-mode: backwards;
> automatically applies animatons of 0% be for ethe anmation starts

A complete `final.html` site is included with all the folllowing features

- BEM archtecture (block element modifier)
- CSS overlay navigation menu
- Button and content animations
- background-clip
- clip-path
- Turntable css cards
- background vdeo
- Cutom radio buttons
- linear-gradient techniques
- perspective
- box-decoraton-break
- Shape outside

2. About section
   - css utility classes
   - `background-clip` property
   - `transform` multiple properties simultaneously
   - `outline-offset` property
   - `:not()` pseudoclass selector
3. Features section

   - icon fonts
   - skewed section design

4. Tours section

   - rotating crad effect
   - `perspective` in css
   - `backface-visibility` property
   - background blend modes
   - `box-decoration-break`

5. Stories section

   - `shape-outside`
   - `filter images`
   - background video
   - `<video>` html tag
   - `object-fit` property

6. Booking section

   - solid-color gradients\*
   - `::input-placeholder`
   - `:focus`, `:invalid`, `placeholder-shown`, `checked` pseudoclasses
   - build custom radio buttons

7. Navigation

   - checkbox hack to make css overlays
   - custom animation timing f(x) using cubic-bezier cuves
   - animate "solid-color gradients"
   - `transform-origin`
   - Creative hover effect

8. Popup window
   - popup with only css
   - `:target`
   - `display: table-cell`
   - CSS text columns
   - automatically 'hyphenate' words using hyphens

Media queries

- Mobile first n Desktop first
- while using max-width and min-width
- Use max-width for desktop-frst and min-width for mobile first approaches

> Media queries don't add any importance or specificity to selectors, so order matters
> Include media queries at the end of the code
> The best breakpoint strategy is to set breakpoints wherever the design breaks

Common breakpoints
2000px > 1800 > 1600 > 1200 > 1000 > 800 > 600 > 400 > 200 > 0

> Order of medi queries

- Base & Typography
- Layout
- Individual sections
