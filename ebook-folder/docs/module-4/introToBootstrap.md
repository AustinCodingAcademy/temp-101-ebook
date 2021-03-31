# Intro to Bootstrap

*“If you have made mistakes, there is always another chance for you.You may have a fresh start any moment you choose,for this thing we call ‘failure’ is not the falling down, but the staying down.“ –Mary Pickford*

## Overview

As you grow into understanding and accepting that you are a web developer you'll find there are many short-cuts to creating web sites. Many of these short-cuts are needed because of the lack of time in which this society we built demands us to build things within. One of the common terms you'll hear among start-ups is "bootstrapping". This just means that whatever the team built is built on top of other technologies already available. "Bootstrapping" is widely used and has it's own pros and cons we can discuss at a later time; for now, let's learn about a specific library called [Bootstrap](https://getbootstrap.com/docs).

We use Bootstrap by simple linking the CDN at the top of our web page then adding the class name we want. With this technique you can create entire websites with all of the common features you're used to surf-seeing. Just wait...you're going to like this!

Follow along by creating a new repo or [clone this one](https://github.com/AustinCodingAcademy/101-Bootstrap-Boilerplate). Open the `index.html` file and let's go!

## Get Ready To Bootstrap

The steps we take in this section will mirror the [Getting Started Docs @getbootstrap.com](https://getbootstrap.com/docs/4.4/getting-started/introduction/).

First, link the CDN to your web page:

```html
  <!-- index.html -->
  <head>
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.4.1/css/bootstrap.min.css" integrity="sha384-Vkoo8x4CGsO3+Hhxv8T/Q5PaXtkKtu6ug5TOeNV6gBiFeWPGFN9MuhOf23Q9Ifjh" crossorigin="anonymous">
    <!-- <link rel="stylesheet" href="Your-CSS-File-Path-Here" /> -->
  </head>
```

Now we have to bring in the JavaScript and another JS library called jQuery that runs alongside the components we're going to build. Put these links at the bottom of your body element:

```html
  <!-- index.html ...continued -->
  <head>
    <!-- ...more code here...see above ^ -->
  </head>
  <body>
    <!-- ...your other code will go here... -->

    <!-- ...and above here... -->
    <script src="https://code.jquery.com/jquery-3.4.1.slim.min.js" integrity="sha384-J6qa4849blE2+poT4WnyKhv5vZF5SrPo0iEjwBvKU7imGFAV0wwj1yYfoRSJoZ+n" crossorigin="anonymous"></script>
    <script src="https://cdn.jsdelivr.net/npm/popper.js@1.16.0/dist/umd/popper.min.js" integrity="sha384-Q6E9RHvbIyZFJoft+2mJbHaEWldlvI9IOYy5n3zV9zzTtmI3UksdQRVvoxMfooAo" crossorigin="anonymous"></script>
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/4.4.1/js/bootstrap.min.js" integrity="sha384-wfSDF2E50Y2D1uUdj0O3uMBJnjuUD4Ih7YwaYd1iqfktj0Uod8GCExl3Og8ifwB6" crossorigin="anonymous"></script>
  </body>
```

Now you're ready to begin building!!!

### Reboot

Remember when we added a CSS reset to our bank of knowledge? The reason for that was to create a blank slate for our other styles to be added. Turns out, Bootstrap has its own form of CSS reset called Reboot. You don't have to do anything special to get it to work. Once you've linked the CSS CDN at the top of your page it works.

Try it! Create an `h1`. See the different font? There's plenty more but we have a lot to get to so if you're curious come back later to the [Reboot page](https://getbootstrap.com/docs/4.4/content/reboot/) to learn more.

### Add a Nav Menu

Go to the [Navs](https://getbootstrap.com/docs/4.4/components/navs/) page.

Here you can see there are pre-built navigation menus you can use. All of them are 100% customizable but the benefit you have here is that you didn't have to build it all from scratch. So scroll down until you see: "Horizontal alignment".

![bootstrap-docs-nav-horizontal-alignment](./../images/bootstrap-docs-nav-horizontal-alignment.png)

 Notice the example and the code snippet below it? You can just click the copy button and paste it into the body of your HTML file then see what happens in live-server!!

Try it!!

Now replace `justify-content-center` with j`ustify-content-end`. Do you see that? We can change the entire layout with a simple change of class names!!

### Grid Layout

Speaking of layout...since you know display flex this should be very easy for you. To layout out a page or a section all you'll need to do is create a `div` container element with the class name `container-fluid`.

```html
  <div class="container-fluid">
  <!-- to create a row for items create another container element with the class name: "row" -->
    <div class="row">
    <!-- inside any row you have 12 columns for items to be arranged on. -->
    <!-- These three elements will each take up 4 columns to fill up the screen -->
      <div class="col-sm">
        first column
      </div>
      <div class="col-sm">
        second column
      </div>
      <div class="col-sm">
        third column
      </div>
    </div>
  </div>
```

Try it! Paste it underneath your nav menu and see what happens!

When you do this, the [row elements will have 12 columns](https://getbootstrap.com/docs/4.4/layout/grid/) added to them automatically. (They use display: flex to do this.) So if you put three items inside, each element will take up 4 columns. Only 2 items? Each will take up 6 columns. But you can change that by giving it the number of column they should take up with...you guessed it...a class name!!

```html
  <div class="col"></div>
  <div class="col-8"></div>
  <div class="col"></div>
```

In the example above the first and last `div` will only have 4 columns to divide themselves into because the second `div` is set to take up the middle 8 columns.

### Buttons!

Buttons are incredibly useful to have on hand and Bootstrap does a wonderful job at creating many of them!! Go to the [Buttons page](https://getbootstrap.com/docs/4.4/components/buttons/) and read up. You can change nearly anything you want by just changing class names so throw a few buttons in a new "row" and see what you can create!!

Have fun! Play! This is the way you truly deepen your understanding.

## Summary

Bootstrap is an incredibly useful tool to jump start your app or website. You can use this technology for your 101 final project but you don't have to feel obligated! We really just want for you to have all the options available to you, give you a solid road map, and fundamental understanding so you can navigate, discover, and become your own developer!!

Have fun and keep coding!

## Additional Resources
s

- [ ] [YT, Academind - Bootstrap 4 Concepts](https://youtu.be/7g8Gg2QVdeU)
  
  > NOTE: the video from BlondieBytes below is on an older version of Bootstrap but the basics are still the same.

- [ ] [YT, BlondieBytes - Learn Bootstrap in 5 mins](https://youtu.be/yalxT0PEx8c)

## Know Your Docs

- [ ] [Obviously Bootstrap](https://getbootstrap.com/docs/4.4/getting-started/introduction/).
