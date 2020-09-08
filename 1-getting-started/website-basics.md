# 🛠 What do you need to build a website?

Before we start building a website it's important to know the tools you will be using to get your website up and running! The tools we will be adding to our toolbox today include **HTML (Hypertext Markup Language), CSS (Cascading Style Sheets) and JS (JavaScript)**.

Before we actually get into building the website, we want to familiarize ourselves with the tools that we will be using, to make the idea easier to grasp we will use the analogy of building a house:

## 🏗 HTML:

This is the foundations of your website - in terms of our house analogy, HTML is represented by the basic barebones frames that are setting up the foundations of your house. Every single website uses HTML and is composed of the following three layers: a window, a DOM (Document Object Model), and elements. In writing an HTML document, we are mainly concerned with elements.

**What is an element?**

An element is how we break up content within an HTML document, it can be a paragraph, a button, a heading, and dozens more. To create an element we use a tag, for example:  
`<p> I am a paragraph <\p>`

For every element there are numerous additional attributes you can specify to customize your element to your liking! Some of the attributes are global (applicable to any element), whilst others can be specific to specific elements. An example of an image with additional attributes:  
`<img src='doggo.jpg' width='500' height='400'>`

All in all, a webpage is just an collection of different elements with an initial html tag opening and closing the page:

```
<html>
    <head></head>
    <body></body>
</html>
```

The head tag is a place to put resources required for the body (e.g. links) and the body is where to put all the visible content.

## 🎨 CSS:

The basic structure of our house is layed out, but we have yet to make it pretty such that anyone would want to live in it! This is where CSS comes in, it lets you paint your walls and gives you the power to specify all the little details in your house. In terms of our webpage, CSS can be used for anything from determining the colours of the background to specifying how an element should look on hover.

Best practices for CSS is to create an external CSS file that is imported into the relevant HTML file for use. To help our style sheet identify which element should receive what styling, CSS leverages the HTML attributes of ID and class:  
`#element-id{}`  
`.element-class{}`  
Within every CSS styling block, we want to define a selector (which is the class name or ID) and property value pairs, which define how we want our item styled, example:

```
p {
    color: purple;
    font-size: 14px;
    font-family: Arial, Helvetica, sans-serif;
}
```

## 🏡 JavaScript:

Last, but not least, we want the house to add additional high tech features to the house, it could be automated porch lights that turn on whenever it detects motion, or regulating the thermostat to turn-off during working house. Similarly JavaScript gives us the power to define logic to be execute upon different iteractions on our webpage.

JavaScript is a dynamically typed programming language that has been historically used for websites, but is now being used everywhere. Within webpages, it can be used to handle clicks of buttons, or prompt pop-ups on certain events, or help in redirecting users to different pages.

Some more advanced JavaScript topics include the following with links where you can read more:

- [Type Coercion](https://medium.com/developers-arena/type-coercion-in-javascript-c973b369b272)
- [JSON](https://www.copterlabs.com/json-what-it-is-how-it-works-how-to-use-it/)
- [Promises](https://web.dev/promises/)
