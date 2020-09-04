# 💼 What will we be building?

- building out a personal portfolio

## We have split the project into four parts

1. Creating `index.html`
2. Designing & building a wireframe
3. Adding CSS & implementing responsive web design
4. Adding advanced styling

#### Want to learn more? We recommend you check out Mozilla Developer Network (MDN) [web docs](https://developer.mozilla.org/en-US/docs/Learn)

<hr>

# Part 1: Creating `index.html`

1. Create a directory called `<GH Username>.github.io`
2. Create a new file called `index.html` under the new directory
3. Type the following snippet into `index.html`

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8" />
    <title>My Portfolio</title>
  </head>
  <body>
    <h1>Hello! My name is [name] ✌️</h1>
  </body>
</html>
```

4. Now, we are going to see how our code looks on the browser. In your terminal, navigate to your `<GH Username>.github.io` directory, and type in `open index.html` - this will allow you to see your changes by automatically opening a tab on your browser for your html file.
1. Alternatively: open Chrome, and press `Ctrl + O` on Windows/Linux or `Cmd + O` on Mac to open the file explorer dialog box. Then, navigate to your `<GH Username>.github.io` directory and open the `index.html` file
1. You will see something like this on your browser

<img width="961" alt="Screen_Shot_2020-07-19_at_12 43 55_PM" src="https://user-images.githubusercontent.com/38872354/91757507-463f0600-eb83-11ea-978b-97ace4f375cc.png">

6. When you make any changes to `index.html`, you can refresh the newly-opened tab to see your changes. Add the following into the `h1` tag:

```html
<h1>Hello! My name is [name] ✌️, welcome to my portfolio :)</h1>
```

7. When you refresh the page, you should see

<img width="957" alt="Screen_Shot_2020-07-19_at_12 43 31_PM" src="https://user-images.githubusercontent.com/38872354/91757505-450dd900-eb83-11ea-9bf8-9ebfd41808de.png">

<hr>

# Part 2: Designing & building a wireframe

![portfolio](https://user-images.githubusercontent.com/38872354/91757580-6b337900-eb83-11ea-857b-2c35b0dca80c.jpg)

Let's start with a mockup of how we are going to compartmentalize our page into sections. We roughly have these sections:

- Intro
  - Profile picture
  - Name
  - Title burb
- About
  - Who I am
  - My interests
- Projects
- Contact
  - Links
  - Contact form

**Intro**

The intro contains an image (profile picture), heading (name), and subheading (title blurb)

We can start with the following code snippet (going in between `<body> </body>`) containing these nested elements:

```html
<div>
  <img src="https://via.placeholder.com/150" />
  <h1>Hello! My name is Jenny</h1>
  <h3>I'm a 4th year BUCS student at UBC</h3>
</div>
```

<img width="991" alt="Screen_Shot_2020-07-19_at_2 32 45_PM" src="https://user-images.githubusercontent.com/38872354/91757583-6c64a600-eb83-11ea-89f2-2a0bf56886b5.png">

**About**

The About section has a text snippet and a subheading followed by a list. Write the following under the ending `</div>` for the Intro section (replacing content inside the square brackets with whatever applies to you)

```html
<div>
  <div>
    <p>[short snippet about my background and aspirations]</p>
  </div>
  <div>
    <p>[interest heading]</p>
    <ul>
      <li>[do thing 1]</li>
      <li>[do thing 2]</li>
      <li>[do thing 3]</li>
    </ul>
  </div>
</div>
```

For instance, for me, I would put:

```html
<div>
  <div>
    <p>I love nwPlus. Very amaze.</p>
  </div>
  <div>
    <p>Some of my interests include:</p>
    <ul>
      <li>Doggos</li>
      <li>Dogspotting</li>
      <li>Smol puppers</li>
    </ul>
  </div>
</div>
```

How this code looks like when you reload your tab on Chrome displaying `index.html`

<img width="642" alt="Screen_Shot_2020-08-06_at_4 39 35_PM" src="https://user-images.githubusercontent.com/38872354/91757586-6c64a600-eb83-11ea-9247-102c29a79533.png">

**Projects**

The projects section will contain four projects. You'll notice in our wireframe that we're planning on arranging then in a 2x2 grid. We'll be able to do that with CSS later on, but for now, let's add the following snippet

```html
<div>
  <h3>Projects</h3>
  <img src="https://via.placeholder.com/300" />
  <img src="https://via.placeholder.com/300" />
  <img src="https://via.placeholder.com/300" />
  <img src="https://via.placeholder.com/300" />
</div>
```

How this looks like when you reload your `index.html` tab

<img width="1275" alt="Screen_Shot_2020-07-19_at_2 34 17_PM" src="https://user-images.githubusercontent.com/38872354/91757585-6c64a600-eb83-11ea-90ed-4f05c08e78a4.png">

**Contact**

The contact section contains links of where people can learn more about you or contact you (for example, GitHub, LinkedIn, email, or anything else you feel is relevant).

Place this section after the enclosing `</div>` tag of the Projects section. Note that you should replace the text enclosed by the square brackets inside the `href` attribute with your own information.

```html
<div>
  <h3>Links</h3>
  <ul>
    <li>
      <a href="https://github.com/[user]">Github</a>
    </li>
    <li>
      <a href="https://linkedin.com/in/[user]">Linkedin</a>
    </li>
    <li>
      <a href="mailto:[email@example.com]">Email</a>
    </li>
  </ul>
</div>
```

For instance, I would put:

```html
<div>
  <h3>Contacc</h3>
  <p>My Links</p>
  <ul>
    <li>
      <a href="https://github.com/panjenny0">GitHub</a>
    </li>
    <li>
      <a href="https://linkedin.com/in/pan-jenny">LinkedIn</a>
    </li>
    <li>
      <a href="mailto:panjenny0@gmail.com">Email</a>
    </li>
  </ul>
</div>
```

We will also add a contact form with input fields.

- for a real website, this will allow people to send you a message
- for the purpose of this workshop, we will only create the front-end, since we do not have a back-end that will handle sending the message for us.

Add this code snippet underneath the `</ul>` element from above

```html
<div>
  <form action="#">
    <label for="email">
      Email: <input type="email" id="email" placeholder="Enter your email" />
    </label>
    <label for="message">
      Message: <textarea id="message">Your Message</textarea>
    </label>
    <input type="submit" valid="Send Message" />
  </form>
</div>
```

After the above is added, this is what our Contact section will look like

<img width="804" alt="Screen_Shot_2020-08-06_at_4 40 52_PM" src="https://user-images.githubusercontent.com/38872354/91757587-6cfd3c80-eb83-11ea-828a-3e06a98ad170.png">

<hr>

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

<img width="735" alt="Screen_Shot_2020-08-06_at_4 41 28_PM" src="https://user-images.githubusercontent.com/38872354/91757845-dda45900-eb83-11ea-9b74-ddf3db460fbb.png">

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

<img width="420" alt="Screen_Shot_2020-08-06_at_4 42 30_PM" src="https://user-images.githubusercontent.com/38872354/91757850-de3cef80-eb83-11ea-9122-10013450f356.png">

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

| 1 | 2 | 3 | 
| -- | -- | -- |
| 4 | 5 | 6 |   


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

<img width="1278" alt="Screen_Shot_2020-08-06_at_4 45 57_PM" src="https://user-images.githubusercontent.com/38872354/91757853-ded58600-eb83-11ea-9b9e-4f951d069902.png">

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

<img width="1278" alt="Screen_Shot_2020-08-06_at_5 02 06_PM" src="https://user-images.githubusercontent.com/38872354/91757856-df6e1c80-eb83-11ea-90d6-ea06d639c2b5.png">

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

<img width="1272" alt="Screen_Shot_2020-08-06_at_5 19 18_PM" src="https://user-images.githubusercontent.com/38872354/91757857-df6e1c80-eb83-11ea-8db2-b1f189f8dcdb.png">
<img width="1280" alt="Screen_Shot_2020-08-06_at_5 20 33_PM" src="https://user-images.githubusercontent.com/38872354/91757858-e006b300-eb83-11ea-9603-b5be3cb6d866.png">

4. To simulate a mobile screen, we can do cmd+(or ctrl)shift+m. Notice how the content looks very disproportional, like a zoomed-out version of the desktop site

<img width="458" alt="Screen_Shot_2020-08-06_at_5 21 43_PM" src="https://user-images.githubusercontent.com/38872354/91757859-e006b300-eb83-11ea-90c8-ca9f2a68f7ac.png">
<img width="446" alt="Screen_Shot_2020-08-06_at_5 24 53_PM" src="https://user-images.githubusercontent.com/38872354/91757862-e09f4980-eb83-11ea-9fb7-f4836dc2ae75.png">

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

<img width="455" alt="Screen_Shot_2020-08-06_at_5 35 41_PM" src="https://user-images.githubusercontent.com/38872354/91757863-e137e000-eb83-11ea-8cce-9ffd46e54a2f.png">

5. Another thing we'd like to do is have the about sections one below another on mobile devices. Let's write a media query for that, defining the breakpoint as `480px`

```css
@media (max-width: 480px) {
  .about-grid {
    grid-template-columns: 100%;
  }
}
```

<img width="353" alt="Screen_Shot_2020-08-06_at_5 39 27_PM" src="https://user-images.githubusercontent.com/38872354/91757864-e137e000-eb83-11ea-9e58-c2107c1ea234.png">
<img width="685" alt="Screen_Shot_2020-08-06_at_5 40 09_PM" src="https://user-images.githubusercontent.com/38872354/91757866-e1d07680-eb83-11ea-8957-76e425b34d52.png">

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

<img width="1270" alt="Screen_Shot_2020-08-06_at_5 47 29_PM" src="https://user-images.githubusercontent.com/38872354/91757867-e1d07680-eb83-11ea-860f-0bc4b9f6b03d.png">
<img width="336" alt="Screen_Shot_2020-08-06_at_5 47 49_PM" src="https://user-images.githubusercontent.com/38872354/91757869-e2690d00-eb83-11ea-91f0-162f72af5888.png">

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

<img width="750" alt="Screen_Shot_2020-08-06_at_6 15 16_PM" src="https://user-images.githubusercontent.com/38872354/91758139-5b686480-eb84-11ea-9a36-ddd89bb93bd2.png">

<hr>

# Part 4: Applying advanced styling

**Applying placeholders with your own images**

1. To better organize our images, let's make a file called `images` in the root level of our application
2. Download the images: <link to zip>
3. Replace the profile picture `<img src="https://via.placeholder.com/150" />` with

   ```html
   <img src="images/profile-picture.jpg" />
   ```

4. Add some styling to the image

   ```css
   .profile-picture {
     border-radius: 50%;
     width: 150px;
     height: 150px;
     /* offset-x | offset-y | blur-radius | spread-radius | color */
     box-shadow: 0 4px 6px 0 rgba(34, 60, 80, 0.16);
     transition: all ease-in-out 0.2s;
   }

   .profile-picture:hover {
     /* offset-x | offset-y | blur-radius | spread-radius | color */
     box-shadow: 0 8px 12px 0 rgba(34, 60, 80, 0.16);
   }
   ```

   - `border-radius` sets the border radius of the image
   - `box-shadow` adds shadows to the image. Check [Mozilla web docs](https://developer.mozilla.org/en-US/docs/Web/CSS/box-shadow) for more details on the syntax
   - `transition`
     - `all` means we want to animate all aspects of the image
     - `ease-in-out` is a timing function that describes the speed of the animation. In this case we want the animation to run for `.2` seconds
   - `hover` sets properties for when we hover over the image, giving users a more visual feedback

       <img width="1277" alt="Screen_Shot_2020-08-06_at_6 57 13_PM" src="https://user-images.githubusercontent.com/38872354/91758181-6b804400-eb84-11ea-8111-f0931fba92f7.png">

5. Replace the project placeholders with the given images (or your own)

   ```html
   <h3 class="heading">Projects</h3>
   <div class="projects-grid">
     <img class="project-image" src="images/project-1.jpg" />
     <img class="project-image" src="images/project-2.jpg" />
     <img class="project-image" src="images/project-3.jpg" />
     <img class="project-image" src="images/project-4.jpg" />
   </div>
   ```

   <img width="1279" alt="Screen_Shot_2020-08-06_at_6 58 04_PM" src="https://user-images.githubusercontent.com/38872354/91758184-6cb17100-eb84-11ea-86fc-4e194d80fc96.png">

**Setting custom fonts**

1. We will be using Roboto Mono for headings and Noto Sans for body text, free for download at [https://fonts.google.com/](https://fonts.google.com/)
2. To use the fonts, add this snippet into the `head` section

   ```html
   <link
     href="https://fonts.googleapis.com/css?family=Noto+Sans|Roboto+Mono&display=swap"
     rel="stylesheet"
   />
   ```

3. Then we want to add these to the `styles.css` for the default body and heading fonts

   ```css
   body {
     font-family: 'Noto Sans', sans-serif;
   }

   h1,
   h2,
   h3,
   h4 {
     font-family: 'Roboto Mono', monospace;
   }
   ```

   Now let's refresh the page! Wow ✨

   <img width="1279" alt="Screen_Shot_2020-08-06_at_7 08 06_PM" src="https://user-images.githubusercontent.com/38872354/91758194-71762500-eb84-11ea-9499-633a204bc309.png">

4. Let's add some footer fixes

   ```html
   <div>
     <h3 class="heading">Contacc</h3>
     <div class="contact">
       <div class="links">
         <h4 **class="form-heading" **>Links</h4>
         <ul class="links-list">
           <!-- List content -->
         </ul>
       </div>

       <div>
         <form action="#">
           <label for="email">
             <h4 class="form-heading">Email</h4>
             <input type="email" id="email" placeholder="Enter your email" />
           </label>
           <label for="message">
             <h4 class="form-heading">Messages</h4>
             <textarea id="message">Your Message</textarea>
           </label>
           <div class="submit-button-wrapper">
             <input type="submit" valid="Send Message" />
           </div>
         </form>
       </div>
     </div>
   </div>
   ```

   ```css
   form input,
   textarea {
     padding: 5px;
     border-radius: 5px;
     width: 240px;
   }

   form {
     width: 250px;
     margin: 0 auto;
   }

   form input[type='submit'] {
     width: 250px;
   }

   .submit-button-wrapper {
     margin: 8px 0;
   }

   .form-heading {
     margin-bottom: 8px !important;
   }
   ```

   <img width="1271" alt="Screen_Shot_2020-08-06_at_7 33 09_PM" src="https://user-images.githubusercontent.com/38872354/91758195-720ebb80-eb84-11ea-9ffc-131dfef40b71.png">

**Change Background Colour**

Let's add a background color and some separation of content

```css
body {
  background-color: #e2f8ec;
}

.container > div {
  margin: 20px auto;
}

hr {
  border: 0;
  height: 1px;
  background-color: #f2fff8;
}
```

Then add this before and after the `about-grid`

```html
<hr />
<div class="about-grid">
  <!-- About content -->
</div>
<hr />
```

<img width="1277" alt="Screen_Shot_2020-08-06_at_7 35 03_PM" src="https://user-images.githubusercontent.com/38872354/91758198-72a75200-eb84-11ea-8f53-4decf2c4d7d4.png">

**Change text color**

```css
body {
  color: #333333;
}
```

`#333333` is a slightly lighter and more gentle shade of black that is easier on the eyes. You won't see a drastic change when you refresh the screen, but from a UX point-of-view, this does make the text easier to read.

‼️ **Challenge** ‼️

- Add effects for project thumbnails when the user hovers onto the pictures
- Suggestions & ideas to get started: [https://www.w3schools.com/howto/howto_css_image_overlay.asp](https://www.w3schools.com/howto/howto_css_image_overlay.asp), [https://codepen.io/nxworld/pen/ZYNOBZ](https://codepen.io/nxworld/pen/ZYNOBZ)
