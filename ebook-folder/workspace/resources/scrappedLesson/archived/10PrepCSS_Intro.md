{% include "../includes/header.md" %}

# CSS

## Purpose

<!-- Here is where we will tell the students the "WHY" behind what they're about to read and learn about. Then we'll give them an overview of the material, sort of a "Big Picture" of the new concept so they can go in with a context of the very NEW material.  -->
A few steps ago, you learned about HTML Elements and how to structure a web page using HTML. But as you may have realized (*and read*), styling your HTML requires a different language (*rather, a set of rules*). These **rules** are applied using another language: CSS. In other words, HTML is the bare-bones structure of the document *(your webpage)* and CSS is the set of rules that the browser has to follow to display the content it finds.

<!-- ### Overview - CSS -->
<!-- @TODO @CLAYTON Add CSS Overview Video -->

## Cascading Style Sheets (CSS)

<!-- This is how each subject should be introduced. Give the students structure so they know they can start trusting the process sooner!  -->
It may feel like we didn't spend much time on HTML before we moved on to CSS, but that's okay. Trust me. As you progress as a developer you'll learn small things from new languages at a time without fully understanding everything about that language. They all build upon one another and you too will build up your understanding of each as they influence one another in your mind.

You could say it's a lot like driving a car. You don't need to know how it works to drive it, you just charge it up and go. And don't worry, in the first class we're going to put these two languages together! Later on you'll learn how the car actually works. For now, let's just get in and let the wind rush through our hair as we cruise down the highway.

### Read It - CSS

CSS stands for [Cascading Style Sheets](https://www.w3schools.com/whatis/whatis_css.asp). **CSS rules** describe how HTML elements are to be displayed/styled on the screen by the browser.

>There's a now-infamous post buried in the archives of the WWW mailing list. It was written by Marc Andreessen in 1994, who would go on to co-create both the Mosaic and Netscape browsers. In the post, Andreessen remarked that because there was no way to style a website with HTML, the only thing he could tell web developers when asked about visual design was, [“sorry you're screwed.”](http://ksi.cpsc.ucalgary.ca/archives/WWW-TALK/www-talk-1994q1.messages/678.html). Ten years later, CSS was on its way to full adoption by a newly enthused web community. **What happened along the way?** - From [CSS Tricks](https://css-tricks.com/look-back-history-css/)

But where does that leave us now?

1. So far you know that you need an `index.html` file to start any website.
1. But that plain HTML only gives us plain text on a screen.
1. You also know that the elements in the HTML file are more than just texts, the store Objects on an Object Tree that have Attributes that we can active.

Remember that example of **Inline-Styles**:

```html
<h1 style="background-color: blue">Stop Fossil Fuels.</h1>
```

The `style=""` attribute is on every element by default but is laying dormant until we activate it, *a lot like very clean and safe oil buried deep in the ground until we tap it, extract it, and use 1 ton moving vehicles to convert it into dangerous gas.* But that's another story for another time.

What I'm saying here is that that **Style Attribute** is always present and all we have to do is write it's name out to use it. The above example is a *possible* way to do it but not the best or an industry standard way of doing it. The better way is to write it in two different files like this:

```html
<!-- in our index.html file -->
<head>
<link rel="stylesheet" type="text/css" href="styles.css">
</head>
<h1>Stop Fossil Fuels.</h1>
```

```css
/* in our styles.css file */
h1 {
  background-color: blue;
}
```

In this way we developers can keep the interactions separate but the browsers can bundle the **Attribute** we just activated with the **Element** we created in the HTML file!!

In the CSS example above:

* You see `h1`. This is called a **Selector**. This selector selects ALL `<h1>` elements in the HTML file.
* The `background-color` is called a **Property**.
* And the `blue` is called a **value**.
* All the things between the `{}`, properties and values are called a **Declaration Block**.
* The whole thing together is called a **CSS Rule**.

Here's a list of ALL [CSS Properties and their possible Values](https://www.w3schools.com/cssref/default.asp). With that and the syntax you see above you can now create any web page!!

### See It - How do we use CSS?

<!-- @TODO @CLAYTON Add How TO Video for CSS Linking -->

<!-- Should include a short video clip of a grad asking a question about the topic. This will bring them context to the what their doing and why its important. Again, always instilling confidence!! -->

### Practice It - CSS

<!-- Section for Code Pen -->

* Go to the [CodePen](https://codepen.io/austincoding/pen/ZyQVWd/)
* First change the line 2 `color: green` to `color: blue`
* Notice the change
* Next uncomment line 5 by removing the `/*` before the `h1`
* What changed? Why are the words "This has paragraphs!" still green?

******

### Suggested Viewing

* [CSS Basics pt. 1](https://www.youtube.com/embed/s7ONvIgOWdM)

## Terms To Know

* Declaration Block
* CSS Selector
* CSS Rule
* Property
* Value
* Attribute

## Questions for Student Discussion

1. Can you explain the relationship of HTML and CSS in your own words?
1. How to do you link a stylesheets to your HTML files? What's the syntax?
1. How do you select all button elements on an HTML file?
1. Why would we not want to use Inline-Styles? Why is multiple files better?

<!-- ## Go to [Step 10 Build First Webpage>](11PrepFirstWebPage.md) -->

{% include "../includes/footer.md" %}
