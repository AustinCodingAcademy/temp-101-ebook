# More CSS Selectors

*“Listen to the mustn'ts, child. Listen to the don'ts. Listen to the shouldn'ts, the impossibles, the won'ts. Listen to the never haves, then listen close to me... Anything can happen, child. Anything can be.” ―Shel Silverstein*

## Overview

Today we're going to spend some solid time on [how to select the right element](https://css-tricks.com/the-difference-between-id-and-class/) in your HTML file so you can style and manipulate to your pleasure.

  > NOTE: This can be a little trickier than you may first realize. *Remember the "Cascade"? In this lesson, we're going to talk a little more about that and learn how to get to exactly the element on the document we want!*

Today you'll learn to:
  1. Reference elements by selectors and why you'd use different selectors.
  1. Select and style an element based on pseudo-elements and pseudo-classes.
  1. Implement [inheritance](https://css-tricks.com/latest-ways-deal-cascade-inheritance-specificity/) and learn to work with it using the Rules of Specificity.

<iframe src="https://player.vimeo.com/video/393464823" width="655" height="368" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen></iframe>

## The Selectors

The reason for all the many **selectors** is because of the way the [DOM](https://en.wikipedia.org/wiki/Document_Object_Model) is built under-the-hood. As the browser loads your HTML it reserves space for each of the elements in the file, then assigns them properties and values based on what it finds in your CSS and JS files. As it does this it will rewrite those values when it finds a new value assignment, but... if no property & value is found for each child elements during the build, they will *Inherit* the properties & values of their Parent Elements. This process of **Inheriting** and reassigning values as the page is built is the **Cascade** of **C**ascading **S**tyle **S**heets. But the Cascade can be overwritten using the *Rules of Specificity*, hence why we need so many selectors.

**The 5 Main of Selectors**

*****

1. `ids` - This is added inside the element's opening tag and denoted with a "#". html `<article id="element_ID">` text goes here `</article>`
1. `classes` - This is denoted by the keyword: class="someClassNameHere" html `<article class="element_class">` text goes here `</article>`
1. `attributes` - `<input disabled >` For a full list of [HTML attributes](https://www.w3schools.com/html/html_attributes.asp).
1. `pseudo-classes` are selectors used on an element when something is done to them like when you hover over an element with your cursor: `:hover { }`

### Type Selector

=== "index.html"
    ```html
      <a href="https://google.com">Google</a>
    ```

=== "index-style.css"
    ```css
      a {
        /* removes the underline */
        text-decoration: none;
      }
    ```

This selector is useful at saving you typing time by setting generic rules for all of your `<p>` tags, or all of your `<section>` tags so that they all have the same general style, but then you can give them a `class` name or `id` when you want each one to look/do something different than the other `<p>` and `<section> `tag.

### id Selector

The `id` selector is used for a unique element, which means that an `id` should only be used one time, on one element, per page. Simply add an id `attribute` and a value.

=== "index.html"
    ```html
      <div id="mario"></div>
      <div id="wario"></div>
    ```

=== "index-style.css"
    ```css
      #mario {
        color: red;
      }

      #wario {
        color: yellow;
      }
    ```

  > You should only use an `id` once but you can use multiple ids on a page.

### Class Selector

The `class` selector is very similar to the id selector, but `class` can be shared with more elements. You can apply classes multiple times on a page to any element you want.

=== "index.html"
    ```html
      <div class="luigi"></div>
      <div></div>
      <div class="luigi"></div>
    ```

=== "index-style.css"
    ```css
      .luigi {
        color: green;
      }
    ```

### Attribute Selector

You are not restricted to the two attributes, class and id. You can specify other element-specific attributes by using `[square brackets]`. Inside the brackets you put the attribute name, optionally followed by a matching operator and a value.

=== "index.html"
    ```html
      <a disabled>I'm a disabled link!</a>
      <input type="button">
    ```

=== "index-style.css"
    ```css
      [disabled] {
        color: gray;
      }

      [type="button"] {
        font-size: 16px;
      }
    ```

### Psuedo-class Selectors

A CSS pseudo-class is a keyword added to one of the selectors covered above that specifies a special *characteristic* or **state** of the element you're selecting. For example `:hover` will apply a style when the user's cursor hovers over the element specified by the selector. You won't see these special state attributes explicitly written in HTML, but they are present nonetheless, as **Element Properties** ready to be manipulated using CSS.

```css
  /* The Syntax looks like this: */
  selector:pseudo-class {
    property: value;
  }
```
=== "index.html"
    ```html
      <section></section>
    ```

=== "index-style.css"
    ```css
      section {
        display: block;
        background-color: blue;
      }

      section:focus {
        background-color: yellow;
      }
    ```

### Practice It - Common CSS Selectors

1. Fork the [CSS Selector CodePen](https://codepen.io/austincoding/pen/pempxa/)
    - [ ] Give every other `<li>` element the class name "other"
    - [ ] Make the font color of "other" `brown`.
    - [ ] Make the [font style](https://www.cssfontstack.com/Verdana) of "other `verdana`.
    - [ ] Give different `id` attributes to each of the `<p>` elements.
    - [ ] Use the `id`s to give them different background colors.
    - [ ] Select the `body` element an get the text to be centered in the middle of the page.

2. Fork the [Pseudo Selector CodePen](http://codepen.io/mistakevin/pen/grVaJL/)

    - [ ] Make an `<h1></h1>` tag in the html
    - [ ] In the CSS, pseudo-select the h1 with a :hover and make it change to the font color of your choice when you hover on it.
    - [ ] copy/paste the tr:nth-child(odd) rule and see if you can add a hover selector on top of it to make the light blue backgrounds change to yellow when hovered on.
    - [ ] Do the same to the even numbered trs but give them a different background color.

3. Fork the [CSS Selector Practice Exercise CodePen](https://codepen.io/austincoding/pen/YQWNjK/)

    - [ ] Follow the directions in the comment section of the CSS to learn more about selectors.
    - [ ] **--or--** follow these instructions
    - [ ] Give the `<body>` element a background: #bdc3c7;
    - [ ] Make the `<h1>` element color: #9b59b6;
    - [ ] Make all `<h2>` elements color: orange;
    - [ ] Make all `<li>` elements blue(Use this [tool](https://chrome.google.com/webstore/detail/eye-dropper/hmdcmlfkchdmnmnmheododdhjedfccka?hl=en) to pick your own hexadecimal blue)
    - [ ] Change the background on every paragraph to be background: `yellow`;
    - [ ] Make all inputs have a `border: solid red 3px`;
    - [ ] Give everything with the class '`hello`' a `white` background
    - [ ] Give the element with id 'special' a 2px solid blue border(pick your own rgb blue) #special {`border: #ff0000`}
    - [ ] Make all the `<p>`'s that are nested inside of divs 25px font(font-size: 25px)
    - [ ] Make only inputs with type 'text' have a gray background
    - [ ] Give both `<p>`'s inside the 3rd `<div>` a pink background
    - [ ] Give the 2nd `<p>` inside the 3rd `<div>` a 5px white border
    - [ ] Make the `<em>` in the 3rd `<div>` element white and 20px font(font-size:20px)
    - [ ] **BONUS CHALLENGES**
        * [ ] You may need to research some other selectors and properties
        * [ ] Make all "checked" checkboxes have a left margin of 50px(margin-left: 50px)
        * [ ] Make the `<label>` elements all UPPERCASE without changing the HTML(definitely look this one up
        * [ ] Make the first letter of the element with id 'special' green and 100px font size(font-size: 100)
        * [ ] Make the `<h1>` element's color change to blue when hovered over
        * [ ] Make the `<a>` element's that have been visited gray

## Additional Resources

- [ ] [Article, CSS Tricks - Difference btw `id` and `class`](https://css-tricks.com/the-difference-between-id-and-class/)
- [ ] [Article, CSS Tricks - Inheritance](https://css-tricks.com/latest-ways-deal-cascade-inheritance-specificity/)
- [ ] [Reference, CSSFontStack - Verdana](https://www.cssfontstack.com/Verdana)

<!-- [Try it yourself](https://replit.com)! -->

## Know Your Docs

* [W3S Docs - HTML attributes](https://www.w3schools.com/html/html_attributes.asp)

<!-- 
```javascript

```

| Method      | Description                          |
| ----------- | ------------------------------------ |
| `GET`       | Fetch resource                       |
| `PUT`       | Update resource |
| `DELETE`    | Delete resource |


- [ ] [MDN Docs - ...]()

    `line numbers`
:do you like 'em?


++slash++
https://facelessuser.github.io/pymdown-extensions/extensions/keys/

cp workspace/resources/templateFile.md docs/module-

! height/width = 1.777 ---- width="655" height="368"

=== "Javascript"

    ```javascript
    ```

=== "Python"

  ```python
  ```

=== "Example"
    ```console
      .
    ```

=== "Instructions"
    ```markdown
      .
    ```

=== "Result"
    ![PIC](./../images/pic.png)
-->