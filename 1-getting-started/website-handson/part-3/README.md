# Part 3: Adding CSS & implementing responsive web design

1. Create a file called `styles.css` in the same directory as `index.html`
2. Add the following line **before** the enclosing `</head>` tag in `index.html`

```html
<link rel="stylesheet" href="styles.css" />
```

**Element Selector**

If we add this into `styles.css`, all of the text inside the enclosing `p` elements will be italicized

```css
p {
  font-style: italic;
}
```

- `p` is the selector - this is the element we want to stylize
- each of the lines within the curly brackets `{ }` is a particular style that will be applied to the element selected (`p` in this case)

<p align="center">
   <img width="400" alt="Example of intro italicized" src="../.screenshots/part-3/1-intro-italicized.png">
   </p>

While adding a CSS selector will select all HTML elements with a selected attribute, this may not be what we want. We will instead give the `p` element a specific identity that we can style. We will do this by adding a `class` attribute.

**Class Selector**

Classes define particular styles for all elements that share the same class name.

```css
.cool-class {
  font-weight: bold;
  color: green;
}
```

Corresponding HTML code if we wanted to use this class in HTML

```css
<h1 class="cool-class">Hemlo frens</h1>
```

<p align="center">
   <img width="400" alt="Example of intro text" src="../.screenshots/part-3/2-intro-green-font.png">
   </p>

**ID Selector**

Similar to class selectors, we can set an ID to an HTML element using the id attribute. How this is declared in CSS:

```css
#cool-id {
  color: blue;
}
```

Using this id in an HTML element

```css
<p id="cool-id">much amaze</p>
```

😎 **_Pro tip_**

You might think that ID and class do the exact same thing - you're not wrong! They just have different usages

- ID: for unique instances of an element (e.g. one unique button style that is different from the others)
- class: for repetitive cases (e.g. items listed in bullet points under the same list)

**CSS Grid**

CSS grid is used to structure your webpage into columns and rows

- first we define how the rows and columns are structured in terms of percentages
- for each element we then decide on which cell to put it in

This is important, because we need to make sure that our content is responsive across different screen sizese

Example of 2 x 3 table

| 1 	| 2 	| 3 	|   	
|:---:|:---:|:---:|
| **4** 	| **5** 	| **6** 	|  

To make this table, we do the following

```css
.grid-table {
  display: grid;
  grid-template-rows: auto auto;
  grid-template-columns: auto auto auto;
}
```

- `display: grid` tells the browser that this is a grid container
- `grid-template-rows` and `grid-template-columns` set the dimensions for rows and columns respectively
- `auto` width/column means our grid is flexible - this grid could end up looking very asymmetric depending on the content

HTML

```css
<div class="grid-table">
<div>1</div>
<div>2</div>
<div>3</div>
<div>4</div>
<div>5</div>
<div>6</div>
</div>
```

😎 **_Pro tip_**

You can use percentages/pixels instead of auto, e.g.:

- 50% 50%
- 300px 300px
- 4rem 4rem

**Mobile Responsiveness**

A three-column display on a normal desktop screen may not necessarily look good in a mobile display. When building your site, it's important to design for cases where the user is not viewing your site from a desktop browser, but from their mobile device instead.

**Media Queries**

A media query is a block of CSS code that only runs if a given condition `@media (<condition>)` is met

Example

```css
.grid {
  display: grid;
  grid-template-columns: 100%;
}

@media (min-width: 600px) {
  // breakpoint 1: run this code if the minimum width of screen is 600px
  .grid {
    grid-template-columns: 50% 50%;
  }
}

@media (min-width: 900px) {
  // breakpoint 2: run this code if the screen is at least 900px wide
  .grid {
    grid-template-columns: 1fr 1fr 1fr;
  }
}
```

- `grid-template-column` sets either one column of `100%`, two columns of `50% 50%`, or three columns of `1fr 1fr 1fr` (three equal-sized columns)
- `display: grid` and `grid-template-columns: 100%` applies to both media queries, so we don't need to add them again

### Positioning our portfolio

1. We want to add some margins around the content of our portfolio to give it more space to "breathe". We'll create a `container` class

```html
<body>
  <div class="container">
    <!-- all of our existing content goes here -->
  </div>
</body>
```

```css
.container {
  max-width: 840px;
  margin: 0 auto;
}
```

<p align="center">
   <img width="640" alt="Example of intro text" src="../.screenshots/part-3/3-intro-devtools.png">
   </p>

- `margin: 0 auto;` means no margin for top-bottom, and auto margins for left-right

2. Now we'd like to center-align our intro headline

- Let's make a new class called `intro`

```html
<div class="intro">
  <!-- content goes here -->
</div>
```

```css
.intro {
  text-align: center;
}
```

<p align="center">
   <img width="560" alt="Example of intro text" src="../.screenshots/part-3/4-intro-centered.png">
   </p>

3. Let's arrange the about portion to have two columns with the first half on the left and second half on the right

```html
<div class="about-grid">
  <div class="about-section">
    <p>I love nwPlus. Very amaze.</p>
  </div>
  <div class="about-section">
    <p>Some of my interests include:</p>
    <ul class="about-list">
      <li>Doggos</li>
      <li>Dogspotting</li>
      <li>Smol puppers</li>
    </ul>
  </div>
</div>
```

```css
.about-grid {
  display: grid;
  grid-template-columns: 50% 50%;
}

.about-section {
  text-align: center;
  text-decoration: none;
}

.about-list {
  list-style: none;
  padding: 0;
}
```

<p align="center">
   <img width="640" alt="Example of intro text" src="../.screenshots/part-3/5-intro-about.png">
   </p>
<p align="center">
   <img width="640" alt="Example of intro text" src="../.screenshots/part-3/6-intro-about-devtools.png">
   </p>

4. To simulate a mobile screen, we can do cmd+(or ctrl)shift+m. Notice how the content looks very disproportional, like a zoomed-out version of the desktop site
      <p align="center">
         <img width="480" alt="Example of intro text" src="../.screenshots/part-3/7-intro-about-projects-devtools.png">
         </p>
   <p align="center">
      <img width="480" alt="Example of intro text" src="../.screenshots/part-3/8-intro-responsive.png">
      </p>

- we can make our site more responsive by instructing our browser to show the webpage in mobile size
- Let's add this `meta` tag before the closing `head` tag

```html
<head>
  <meta charset="utf-8" />
  <!-- existing content in the <head> element -->
  <meta name="viewport" content="width=device-width, initial-scale=1" />
</head>
```

- `meta` allows you to control the dimensions and scaling of a page
- `width=device-width` sets the width of page to follow the screen-width of the device
- `initial-scale=1.0` sets the initial zoom level when the page is first loaded

<p align="center">
   <img width="320" alt="Example of intro text" src="../.screenshots/part-3/9-intro-responsive-small.png">
   </p>

5. Another thing we'd like to do is have the about sections one below another on mobile devices. Let's write a media query for that, defining the breakpoint as `480px`

```css
@media (max-width: 480px) {
  .about-grid {
    grid-template-columns: 100%;
  }
}
```

<p align="center">
   <img width="320" alt="Example of intro text" src="../.screenshots/part-3/10-intro-responsive-smaller.png">
   </p>
   <p align="center">
   <img width="400" alt="Example of intro text" src="../.screenshots/part-3/11-intro-responsive-med.png">
   </p>

6. Let's make similar changes to the projects section - 2x2 on desktop, 4x1 on mobile

```html
<h2 class="heading">Pawjects</h2>
<div class="projects-grid">
  <img class="project-image" src="https://via.placeholder.com/300" />
  <img class="project-image" src="https://via.placeholder.com/300" />
  <img class="project-image" src="https://via.placeholder.com/300" />
  <img class="project-image" src="https://via.placeholder.com/300" />
</div>
```

```css
.heading {
  text-align: center;
}

.projects-grid {
  display: grid;
  grid-template-columns: 50% 50%;
}

.project-image {
  justify-self: center;
  padding: 4%;
}
@media (max-width: 650px) {
  .projects-grid {
    grid-template-columns: 100%;
  }
}
```

<p align="center">
   <img width="560" alt="Example of intro text" src="../.screenshots/part-3/12-projects.png">
   </p>
   <p align="center">
   <img width="400" alt="Example of intro text" src="../.screenshots/part-3/13-projects-responsive-small.png">
   </p>

7. Let's split the contact section as well, by 30-70

```html
<div>
  <h3 class="heading">Contacc</h3>
  <div class="contact">
    <div class="links">
      <h4>Links</h4>
      <ul class="links-list">
        <!-- List items -->
      </ul>
    </div>
    <div>
      <!-- Contact form -->
    </div>
  </div>
</div>
```

```css
.contact {
  display: grid;
  grid-template-columns: 30% 70%;
}

.links {
  justify-self: center;
}

.links-list {
  list-style: none;
  padding: 0;
}

@media (max-width: 650px) {
  .links-and-contact {
    grid-template-columns: 100%;
  }
}
```

<p align="center">
   <img width="560" alt="Example of intro text" src="../.screenshots/part-3/14-contact.png">
   </p>
