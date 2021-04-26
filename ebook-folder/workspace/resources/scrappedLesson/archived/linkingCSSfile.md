{% include "../includes/header.md" %}

## Linking HTML & CSS + the Cascade...
<!-- This is how each subject should be introduced. Give the students structure so they know they can start trusting the process sooner!  -->

## Overview - Linking Stylesheets and the DOM

<!-- overview of bundling elements with their rules and functions in the DOM, show how to create a link to a CSS file, and how Paths work -->
<!-- 101 - Link CSS and JS Files -  -->
<iframe src="https://player.vimeo.com/video/389338861" width="640" height="360" frameborder="0" allow="autoplay; fullscreen" allowfullscreen></iframe>

### Read It - 3 Ways to combine your CSS rules to your HTML elements
<!-- Give them our writing of the subject then link to a few articles: Medium, Wikipedia, CSS-Tricks, W3S, MozillaDev, etc... that help give more perspective on the subject  -->

There are three ways to link a CSS file to your index.html file. We'll talk about each, but in class, we'll do it the right way!

1. An **External Style Sheet** means that is a separate file than your HTML files. This is the **most maintainable** method and the method we'll be using here and forever. By keeping our CSS rule in their own files and *referencing* them in our HTML files we can debug and make adjustments more easily. This method is considered *best practice* - we'll be using it throughout this course. It looks like this:

  ```html
  <head>
    <title>Awesome website</title>
    <link rel="stylesheet" href="path/to/your/css-file.css">
  </head>
  ```

*Notice line 3 above. This is how you link an external CSS file*.

1. **In-Line** styling.  This is the **least maintainable** method, and should be used for testing ONLY so that it later moves to an external file.

```html
<section style="width: 500px; height: 256px; background:#ccc;"></section>
```

1. With a `<style></style>` element definition at the beginning of the document. Use this method **solely** for styles that are used *only* within a particular page. It is rare to see this method but is certainly a possible method.

  ```html
  <head>
    <title>Adding CSS using style element</title>
    <style>
    h1 {
      text-decoration: underline;
      font-family: 'Arial', sans-serif;
    }
    </style>
  </head>
  ```

## The Cascade

Under the hood, CSS relies on a specific **order of Inheritance**. This order determines how your element is rendered by **prioritizing some methods over others**. This complex interaction makes CSS powerful, but it can also make it confusing and difficult to debug.

There are three main sources of style information that form the [Cascade](https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Getting_Started/Cascading_and_inheritance). In order of **loading order** (that is, which styling loads first), they are:

1. The browser's default styles for the markup language. (*ex. Chrome or Firefox built-in defaults*)
1. Styles specified by a user who is reading the document. (*ex. Maybe a user set some custom settings somewhere like someone with a color-blindness or hearing impairment.*)
1. The styles linked to the document by its creator. (*This is what we can control*)
  
Below this last level of the cascade comes even more levels, like the Inception!

  * The most specific rules apply last but have the most importance. 
  * The most generic rules apply first but have the least importance.

This is a little harder to understand because we haven't gotten to **Specific Selectors** yet but maybe you can imagine that there are ways to target just one `<p>` tag on a page while leaving the other `<p>` tags alone. This would be done with a more [Specific Selector](https://www.w3schools.com/cssref/css_selectors.asp).

### See It - The Cascade

<!-- 101 - Inheritance and Cascade - a video that helps students understand the cascade and how to follow its rules -->
 <iframe src="https://player.vimeo.com/video/389057261" width="640" height="360" frameborder="0" allow="autoplay; fullscreen" allowfullscreen></iframe>

### Suggested Viewing

* [The Cascade](https://www.youtube.com/watch?v=tZhmjgLQgXU)

<!-- @TODO NEED to add a practice problem to deepen their understanding of the cascade and specificity. -->
******
******

## Terms to Know

* Loading Order
* The Cascade
* In-line Styles
* External CSS File

## Questions for Student Discussion

**At the end of each Pre-Homework, we will ask you important questions to ask yourself and make sure you are able to answer them in class.**

* How would you describe the "Cascade"?
* Explain the 3 ways to use CSS to style an html file. What is the best way? How do you do it?
* How would you explain the way CSS works out loud to someone?
* Where do you find the Properties of CSS?

{% include "../includes/footer.md" %}