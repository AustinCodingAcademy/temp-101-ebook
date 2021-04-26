{% include "../includes/header.md" %}

## Syntax of CSS Rules

Just like HTML or any other language, CSS has syntax that must be followed for it to be "valid" and readable by the web browser.

## Overview - CSS Syntax and the DOM

<!-- video in context with the DOM + the syntax -->
<iframe src="https://player.vimeo.com/video/389280163" width="640" height="480" frameborder="0" allow="autoplay; fullscreen" allowfullscreen></iframe>

### Read It - The Structure of CSS Rules

![CSS AnVS Codey](../images/03/css-rule-anatomy.jpg)

The syntax of CSS is pretty straightforward:

* State the element you are selecting from the document - THE **SELECTOR**
* And give it some rules - THE **DECLARATION BLOCK** using a **Property** with a **Value**

**If this is our index.html file:**

```html
  <head>
      <link rel="stylesheet" href="./styles/stylesheet1.css">
  </head>
  <body>
      <div> Content is inside here </div>
  </body>
```

**And this is our styles/stylesheet1.css file:**

```css
  body {
    font-family: 'Verdana', sans-serif;
    margin: 50px auto;
    width: 760px;
  }
```

* Then the `<body></body>` element on the webpage will be presented with all of its text in Verdana font. This is called **Inheritance**. Child element will inherit style rules from their parents.
* The `<body>` will also have 50px of invisible space, `margin` on the top and bottom and have  auto-centered invisible space on the right and left.
* The content of the `<body>` will be 760px wide on the screen.

> *NOTE: To get an idea of what a pixel is: if you're on a **macOS** hold **command** + **shift** + **4** to get a cross-hair for your cursor. Click and drag to see the size of your rectangular screen capture marked in pixels at the cursor. For **Windows** access your "Snipping" tool.*

```css
  body {
    font-family: 'Verdana', sans-serif;
    margin: 50px auto;
    width: 760px;
  }
```

In the CSS snippet above:

* `body` is the **selector**. *It tells the browser what element to attach these rules to*.
* `width` is a **Property**
* `760px` is a **Value**

You can add as many Properties and Values as you like/need.

## Know Your Docs

* [W3Schools - CSS Properties](https://www.w3schools.com/cssref/default.asp)
* [MDN - CSS Basics](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/CSS_basics) on CSS.

### Practice It - CSS Rules

* Fork the [CodePen](https://codepen.io/hipperger/pen/bmYmQG/), then click the top-left corner to open in a new window.
* Study the html and cross-reference the CSS to see why it is styled the way it is. 
* How do the two relate to one another?
* Try changing main content to green or pink.
* What happens when you remove the ```/* */``` from line 59 and 63 in the CSS file?
* Why do you think that happened?
* What happens when you change the values in width or or margin?

### Suggested Viewing

* [CSS with BlondieBytes](https://www.youtube.com/embed/3T4BsrBISnI)

## Terms to Know

* CSS Inheritance
* CSS Selector
* CSS Declaration Block
* CSS Rule
* CSS Property
* CSS Value

## Question for Student Discussion

1. Why would we say you can build any web page you'd like with the information you have?
1. What do you think an entrepreneur thinks about?
1. How do you think Michael Dell created a computer and software company?
1. What do the developers of Instagram think about?

{% include "../includes/footer.md" %}