# CSS Reset

*“Applause is the spur of noble minds, the end and aim of weak ones.“ –Edmund Burke*

## Overview

The first coding lesson this week is pretty darn simple, it's called CSS reset. All you have to do is create a new CSS file, throw in the code shown below, link it to your HTML files ABOVE your other CSS files, and boom, you're done! But why?

<!-- ! Video Contents:  (width="655" height="368", ratio 1.77) -->

### Why

Browsers come with various default styling which means they display HTML elements slightly different from one another. Chrome has its own, Firefox another, and Safari a different default. This can cause small deviations in the appearance of your web pages.

To avoid your layout looking different in the various browsers people use to see the internet, you use what's called a "CSS Reset". Think of it as a clean slate to start painting on. A CSS reset reduces browser default styling like `border`, `padding`, `margins` and `font-size`. When you are use a CSS reset you can count on a starting point of defining rules for elements without having surprises later on!

### How

To create a CSS Reset just create a new CSS file and name it something like reset.css. Then, paste the following code in there.

```css
  html, body, div, span, applet, object, iframe,
  h1, h2, h3, h4, h5, h6, p, blockquote, pre,
  a, abbr, acronym, address, big, cite, code,
  del, dfn, em, img, ins, kbd, q, s, samp,
  small, strike, strong, sub, sup, tt, var,
  b, u, i, center,
  dl, dt, dd, ol, ul, li,
  fieldset, form, label, legend,
  table, caption, tbody, tfoot, thead, tr, th, td,
  article, aside, canvas, details, embed,
  figure, figcaption, footer, header, hgroup,
  menu, nav, output, ruby, section, summary,
  time, mark, audio, video {
    margin: 0;
    padding: 0;
    border: 0;
    font-size: 100%;
    font: inherit;
    vertical-align: baseline;
  }
```

All this code is doing is selecting all HTML elements and applies the same rules to them. Obviously you can overwrite the rules with new CSS rules as long as they are listed in a file **below** the `reset.css` file.

## The Cascade

To use your new `reset.css` in a project, remember that HTML is read from **top-down**, **left-to-right** - if it finds two CSS definitions for the same element in both files, it will apply the most recently parsed definition, *the one on the bottom*. Therefore, you write `<link href="reset.css"/>` before you link in any other CSS files, like your `style.css` or Google Fonts.

=== "Just like this."
    ```html
      <link rel="stylesheet" href="./css/reset.css"/>
      <link rel="stylesheet" href="./css/style.css"/>
    ```

=== "If using a **third-party**"
    ```html
      <link rel="stylesheet" href="./css/reset.css"/>
      <link rel="stylesheet" href="./css/bootstrap.css"/>
      <link rel="stylesheet" href="./css/style.css"/>
    ```

If your `reset` is read after your `style`, and both contain conflicting style definitions for the same element, the reset's style definition will be applied. This can be quite perplexing - to prevent unnecessary confusion, remember:

  > **add the reset before any of your own styles.**
  > **Your custom styles should always come last**, after any outside styles.

=== "Not like this"
    ```html
          <!-- BAD! DON'T DO -->
      <link rel="stylesheet" href="./css/style.css"/>
      <link rel="stylesheet" href="./css/reset.css"/>
    ```

## Additional Resources

- [ ] [YT, Kevin Powell - The Problem with Browser Default Values](https://www.youtube.com/watch?v=L4wPV-K1lNI)
- [ ] [Medium, Kevin Powell - Understanding "Initial", "Inherit", and "Unset](https://elad.medium.com/understanding-the-initial-inherit-and-unset-css-keywords-2d70b7121695)

## Know Your Docs

- [ ] [W3S Docs - Default CSS Values](https://www.w3schools.com/cssref/css_default_values.asp)
