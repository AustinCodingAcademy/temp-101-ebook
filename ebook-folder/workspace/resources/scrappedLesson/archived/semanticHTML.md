{% include "../includes/header.md" %}

# Semantic Elements

<!-- Overview Video of Semantic Elements -->
<iframe src="https://player.vimeo.com/video/389069194" width="640" height="360" frameborder="0" allow="autoplay; fullscreen" allowfullscreen></iframe>

## Semantic Elements Overview

From the last lesson you learned that **HTML Tags** create and represent **Elements** on the **DOM**. In other words, they are dedicated words we recognize as humans that are also built into the browser's understanding. For example, an `<article> text goes here </article>` tag would probably mean there is text of an article inside. Just like the browser knows these keywords, Google's web crawler also knows these keywords and uses them to analyze, categorize, and rank millions of pages and return them as search results. The Elements you learned last lesson are simple Elements, they provide content to the inside of the document. But if we step back a little we can see that a web page is broken into many pieces even before we get to `<h1>`s or `<p>`s. Let's take look at those.

A **Semantic Element** is one that clearly describes its meaning to both the browser **and** to the developer - that is, the original developer (you), and any developers who work on the project in the future (your coworkers).

One of the benefits of writing HTML semantically is that it's easy-to-use as your project evolves and grows.

> You might have come across the `<div>` tag. This tag is problematic because so many developers use it but it isn't **Semantic**, gets placed as low priority by Google and doesn't help those with disabilities! Please avoid using this element when you can. *Moving on*...

The use of semantic HTML elements provides a developer the combined advantage of writing fewer attributes while avoiding **Inline-Styling**. *More on this later.*

All of this makes your code look and feel more structured. Whenever future developers read or edit your code, they will have an easier time comprehending it. Plus, your code will be simpler and more condensed.

### See It - Semantic Elements

<!-- Semantic Elements -->
<iframe src="https://player.vimeo.com/video/292802698" width="640" height="360" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>

******

### Read It - Semantic Elements

Here is a list of the most common semantic elements.

The [`<header>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/header) element represents a group of introductory or navigational aids. It may contain some heading elements, and also other elements like a logo, wrapped section's header, a search form, and so on.

A [`<nav>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/nav) element (HTML Navigation Element) represents a section of a page that links to other pages or to parts within the page: a section with navigation links.

The [`<main>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/main) element represents the main content of the `<body>` of a document or application. The main content area consists of content that is directly related to, or expands upon the central topic of a document or the central functionality of an application.

A [`<section>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/section) element represents a generic section of a document, i.e., a thematic grouping of content, typically with a heading. Each `<section>` should be identified, typically by including a heading (`<h1>`-`<h6>` element) as a child of the `<section>` element.

The [`<article>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/article) element represents a self-contained composition in a document, page, application, or site, which is intended to be independently distributable or reusable.

The [`<aside>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/aside) element represents a section of the page with content connected tangentially to the rest, which could be considered separate from that content. These sections are often represented as sidebars or inserts.

The [`<footer>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/footer) element represents a footer for its nearest sectioning content or sectioning root element. A footer typically contains information about the author of the section, copyright data or links to related documents.

### Practice It - HTML Structure

Look at the picture below to see if you can translate it into what you might write in HTML:

![SemanticElementsImage](../images/semantic-elements.gif)

*****

```html
<html>
  <body>
    <header></header>
    <nav></nav>
    <main>
      <section></section>
      <article></article>
    </main>
    <aside></aside>
    <footer></footer>
  </body>
</html>  
```

You see, a web page, despite all of its pretty pictures and curved shapes is just a bunch rectangles or **containers** that we organize content inside of. Remember too, every time we add an HTML element in the file, we also create a new **Node** of the **Document Tree** for us to access via CSS or JavaScript!!

******
******

## Terms to Know

*You're probably wondering why we don't give the definition to all of the words. It's because I want you to get comfortable with not knowing, questioning, and finding out for yourself. This will train you into a VERY valuable employee and entrepreneur! Now go find out what these mean.*

* Inline-Styling
* Container in the DOM
* Node on the Document Tree

## Question for Student Discussion

*If you copy/paste the code from the **Practice It - HTML Structure** example into a new CodePen, you might notice the styling will look different from the  picture shown in the example. Why do you think that is?? The html code is exactly what you'd use to build those elements...but.....*

<!-- <body>
  <header><h1>My Awesome Blog!</h1></header>
  <nav>Home<br>About<br>Events<br>Contact</nav>
  <main>
    <section>
      <h2>Posts</h2>
      <article>My First Post!</article>
      <article>My Second Post!</article>
      <article>My Third Post!</article>
    </section>
    <section>
      <h2>Calendar</h2>
      <table>...</table>
    </section>
  </main>
  <aside>You Win!!!</aside>
  <footer>© 2016 Austin Coding Academy</footer>
</body> -->