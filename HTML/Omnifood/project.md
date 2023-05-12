# OMNIFOOD

## Step 1. Define

1. Who is the site for?

- For a client

2. What is the site for?

- Business goal: Selling mnthl food subscription
- User goal: Eating effortlessly, without spending a lot of time & money

3. Target audience

- From content: Busy people who like technology, are interested in a healthy diet, n have a well payin gjob

## Step 2: Plan the project

1. Gather content

- Provided by client(omnifood)

2. Plan out the sitemap:

   - A one-page landing marketing website, no sitemap

3. Define website personality
   - We'll use a startup/upbeat personality.
   - We'll add some elements of calm/peaceful
4. Plan the sections
   - Navigation
   - Hero
   - Featured in
   - Features
   - How it works
   - Meals (and list of diets)
   - Testimonials + gallery
   - Pricing
   - CTA
   - Footer

> First ideas and sketch
> Make a sket based on content and a bunch of insprtaions

> Resources
>
> > Get avatar faces from [UIFaces](uifaces.co)

## Responsive design

= Design technique to make a webpage adjust layout and visual styles to any possible screen size (window and viewport size)

> It's simply a set of practices, not a separate technology. It is all CSS

Responsive design ingredients:

1. Fluid layouts

   - Allow the oage adapt ot current viewport width
   - Use `% | vh | vw` instaed of `px`
   - Use `max-width` instead of `width`

2. Responsive units

   - Use `rem` unit instead of `px` for most lengths
   - Trick: set 1rem to 10px for easy calc (i.e. `font-size: 62.5%`)

3. Flexible images

   - Images don't scale automatically by default
   - Always use `%` for images dimensions, together with `max-width` property

4. Media queries

> **Desktop-first dev**
> Starting with CSS for the desktop, then scaling it down to mobile

> **Mobile-first dev**
> Starting with CSS for the mobile, then scaling it up to desktop
> Note: Since mobile devices are most commonly used, this is the modern approach
