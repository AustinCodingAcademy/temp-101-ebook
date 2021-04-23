{% include "../includes/header.md" %}

# Hyper-Text Markup Language(HTML) + the DOM
<!-- This is how each subject should be introduced. Give the students structure so they know they can start trusting the process sooner!  -->

## HTML Elements in the DOM Structure

<!-- Video on HTML Elements in the DOM Structure -->
<iframe src="https://player.vimeo.com/video/389038638" width="640" height="360" frameborder="0" allow="autoplay; fullscreen" allowfullscreen></iframe>

[HyperText Markup Language (HTML)](https://en.wikipedia.org/wiki/HTML) is the standard markup language for creating web pages and web applications. HTML describes the structure of a web page [semantically](https://www.merriam-webster.com/dictionary/semantic) and includes cues for the appearance of the document, i.e. **hyper-links** appear blue and **visited links** appear as purple. However, if we want those elements to be styled in a certain way or do specific actions when a user interacts with them, we need to know how those Elements have built-in tools we can call and use. *With this collection of built-in tools you'll soon see that we can use CSS to tell the browser how our web page should appear, maybe we wanted visited links to be red and not purple!!* For now, we'll start with HTML Elements the structure of our web pages.

> Note: HTML, **Cascading Style Sheets** (CSS), and **JavaScript** (JS), form the triad languages of the World Wide Web. They are are the three languages EVERY website uses. The way it works is that web browsers, like Chrome, receive HTML documents from a **web-server** or **local server** (*the way you'll be working in this course*) and render them into dynamic web pages that use CSS and JavaScript to make them powerful interactive tools for the user.

### Read It - HTML Structure - Elements

<!-- Give them our writing of the subject then link to a few articles: Medium, Wikipedia, CSS-Tricks, W3S, MozillaDev, etc... that help give more perspective on the subject  -->

HTML, quite simply put, is a markup language, which means it details the shape of a document. It's also a universal language because its read by all browsers! But don't underestimate the power of clear shape and universality.

When a browser reaches out to a server for a website, it uses a URL as the address to get there but then it will need an entry point into the folder that holds the entire website. This entry point is the `index.html` file. The `index.html` file is always the first file requested by the browser which makes it the first file sent by the server. Because it is the point of entry for all **web apps** and **web sites**, we will start from here.

Going back to our Programming and Web Development lessons, we know that computers keep memory in specific shapes, usually know as **Objects**. Because of the shape of these objects we can access them with other languages like CSS and JavaScript. Therefore, all HTML is written to build *things* called **Elements**. The elements can be thought of as those *objects* that the computer stores its information.

Let's say we want the Heading of our **web page** to be " Stop Fossil Fuels. Build 100% Renewables. " as in the current title of [350.org](https://350.org/). *See image below*

![350.org Landing Page](../images/00/350-org-landing-page.png)

To write that in HTML we would do this:

```html
<h1>Stop Fossil Fuels.</h1>
<h1>Build 100%</h1>
<h1>Renewables</h1>
```

> *NOTE: `<h1></h1>` are the **tags** that represent an HTML Element*

But this would only result in the following because HTML gives us structure and content not colors or interaction like the picture below.

![Plain Example 350.org Landing Page](../images/PlainHTMLText.png)

BUT! Because we have this structure, given to us by the `<h1></h1>` element we now have access to things called: **attributes**. These attributes are set as **null** by default. This means, they aren't used/don't really matter. But if we want them to matter and be used we can activate them with CSS or JavaScript. Maybe think of HTML elements as a lego piece with many bumps and holes to interlock with other pieces. Its just sitting there waiting to be give actions and things to do with its attributes.

One of these attributes is `background-color`. We can activate it by adding a bit of CSS:

```html
<h1 style="background-color: blue">Stop Fossil Fuels.</h1>
<h1>Build 100%</h1>
<h1>Renewables</h1>
```

This would produce:

![Blue-350.org Text](../images/Blue-350-Text.png)

We're not going to go into the details of CSS or JavaScript right now, what is important for you to learn right now it the structure of these *objects* we get to work with because there are many *objects*/**Elements** in HTML:

### Know Your Docs

This website will become your study companion. You will learn not only HTML, CSS, and JS from it but also you will learn how to learn and build up your own confidence as you do. Bookmark and refer back to it often: [All HTML5 Tags](https://www.w3schools.com/tags/).

*****

## The DOM

Now that we see there are these Elements shaped like a very generic computer *object* let's talk about the *thing* that holds all of those Elements, the **Document**.

The **Document** is the large, all-encompassing, great-great-grandparent to all of the other Elements you ever add to a web page. Through the document you can access any object you add to add style(CSS) or functionality(JS). No, we won't get into the details, it would be way too overwhelming right now, we will instead get familiar with the structure of the **Documents** so we have a map to use as we learn new features and have the ability for you to explore on your own!!

The structure of the Document is know as the DOM, or **Document Object Model**, it is a large *thing* that the computer stores all of those other elements within and give us developers the ability to navigate around and do things to those many elements.

The way we write the basic `index.html` file, *remember the web page all websites begin with*:
  
```html
<!DOCTYPE html>
<html>
  <head>
    <title>Title of Web Page</title>
  </head>  
  <body>
    <!-- This is comment-line to communicate to humans and not to computers, like a secret language! ssshhh.... -->
    <p>Inside the body element is where most of your other elements will go</p>
  </body>
</html>
```

What this produces is a **Document Tree**, or **DOM**

![Document-Tree](../images/Document-Tree.png)

So far we've covered this structure in very basic terms but its important that you see how the **tags** in the code above relate to the **elements** created in the DOM picture below it.

### Practice It - HTML Elements

Create a new [CodePen](http://codepen.io/) to practice building a silly and simple page with the following tags:

#### Elements to Use

* Copy/Paste the sample code above to get started.
* `<h1>, <h2>, <h3>, <h4>, <h5>, <h6>`
* `<p>, <button>`
* also:

    ```html
      <ul>
        <li>item 1</li>
        <li>item 2</li>
        <li>item 3</li>
      </ul>
    ```

* **BONUS 1**: See if you can figure out how to change this special element to be named and navigate you to your favorite shopping website: `<a href="google.com">My Link</a>`
* **BONUS 2**: Look up font-color, background-color, and font-size to see if you can add CSS rules change the H1-6 tags to be something more inlined with your tastes.

You have only four rules:

1. `<!DOCTYPE html>` must go at the top of ALL of your web pages
1. Open all of your tags with `<>` and close them with `</>` as in, `<p></p>` or `<h2><h6>`
1. Put all of your tags between your `<body> </body>` tags
1. Don't be afraid to play!!

*****
*****

## Terms To Know

* Hyper Links
* Visited Links
* Cascading Style Sheets
* JavaScript
* DOM
* Document Tree
* The Document
* HTML
* Elements
* HTML Tags
* Web Page
* Web Site
* Web App
* Locally Served

<!-- ## Questions for Student Discussion -->

<!-- ## Go to [Pre-Work Step 7 >](07PrepSPLAT.md) -->

{% include "../includes/footer.md" %}
