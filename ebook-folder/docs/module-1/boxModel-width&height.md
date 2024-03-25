# Content Width & Height + New Length Units

Since you already know these two values let's take some time to cover them quickly but **also** introduce to you some other useful values/**length units** you can use for margin, padding, and border as well as height and width.

## New Length Units

By default, the dimension of an element is the size of the content contained within the element. This means that when you create an `<article>` element it won't have a height that you can see on the screen because there is nothing inside of it. But as soon as you add content you'll be able to see it grow to fit the amount of content. We can, of course, make the element larger than the content by changing its width and height properties.

The width and height properties take the traditional `px`(pixel) unit like the other properties you've read about so far, but now we'll throw a curve ball at you: All of the properties you've read about take far more length units than just the traditional `px`, including: `in`, `cm`, `mm`, `em`, `rem`, `vh`, `vw`, `%`, `pt` and many more.

"Why so many?" That's a good question that doesn't really need to be answered right now. Suffice it to say that there have been many additions to the CSS language trying to accommodate for designers working on computers. The ones I'd like you to focus your attention on right now are `%` and `pt`.

### Percentage is Dynamic

`%`, or **percentage**, tells the child element to be displayed at a specified percentage, or proportion, of its parent element. Check out the example below:

```html
<!-- index.html file -->
<article>
  <p>The red fox jumped over the green turtle.</p>
</article>

<style>
  /* style.css file */
  article {
    width: 500px;
    height: 600px;
  }

  article > p {
    width: 90%;
    height: 50%;
  }
</style>
```

In the example above, the `<article>` element, or parent element, will be `500px` by `600px` while the `<p>` element, or child element, will be rendered at 450px(`90%`) by 300px(`50%`) because it is set to be a percentage of its parent element.

This is really useful when parent elements are set to be sized in proportion to their parent element like maybe . . . `<body>`. See the example below:

```html
<!-- index.html file -->
<article>
  <p>The red fox jumped over the green turtle.</p>
</article>

<style>
    /* style.css file */

  /* The <body> element will be automatically set to the height and width of the viewport, or display of the computer, tablet, or phone's window */
  body {
    width: auto;
    height: auto;
  }

  /* Then the <article> element will be set to 50% as wide as the whole <body> and 100% as tall as the <body> */
  article {
    width: 50%;
    height: 100%;
  }

  /* Can I assume you can guess what the paragraph element will do? */
  article > p {
    width: 90%;
    height: 50%;
  }
</style>
```

Using percentages is advantageous because you will never know all the sizes of screens that will view your web pages; this way you can tell elements to be a specific percentage of the available area instead of **hard coded** pixels!

#### Follow It Up with Min- & Max-

When using percentages as values it's important to include the `min-width`/`max-width` and `min-height`/`max-height` properties so as to avoid your elements being rendered in sizes that are unmanageable for the user. See below:

```css
body {
  width: auto;
  height: auto;
  min-width: 100pt; /* <--- Notice the use of the pt unit */
  max-width: 1000pt;
  min-height: 150pt;
  max-height: 1500pt;
}
```

Above you saw the use of `pt` or **points**. These are a little more reliable than `px` which are relative to the number of pixels in a user's display and [other factors](http://inamidst.com/stuff/notes/csspx){:target="_blank"} . The `pt` value is equal to 1/72nd of an inch so you can calculate a little more easily the size of your elements.

### View-height & View-Width

The last units you should know about are `vh` and `vw` which stand for **view-height** and **view-width**, respectively. These are very useful units except for the fact that they are not supported on all previous versions of mobile browsers.

## Additional Resources

* [W3S Docs - Height & Width](https://www.w3schools.com/css/css_dimension.asp){:target="_blank"}
* [CodePen - Box Model Visualizer](http://codepen.io/carolineartz/pen/ogVXZj/){:target="_blank"}
* [W3S Docs - Default CSS Values Reference](https://www.w3schools.com/cssref/css_default_values.asp){:target="_blank"}

<!-- ! END OF VIDEO 101.1.20.1 - Height & Width + Length Values -->

********************************************
<!-- NOTES -->
<!-- ! END OF VIDEO 101.1.3.1 - EXAMPLE TITLE -->
<!-- ? Video Numbering and Title system: CourseNumber.ModuleNumber.LessonNumber.VideoNumber -->
<!-- * (VIDEO 101.2.4.3 - "CSS Selectors") === 101 Course, Module 2, Lesson 4, Video 3 - "CSS Selectors" -->

<!-- TODO - INSERT IMAGE EXAMPLE -->
********************************************