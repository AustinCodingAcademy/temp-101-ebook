# Animate.css

*“We need never be hopeless because we can never be irreparably broken.” ―John Green, **Looking for Alaska***

## Overview

The introduction of [Animate.css](https://github.com/daneden/animate.css) is more of an introduction to a concept you'll be using throughout your advanced courses and in your career, **open-source code**. Open-source means that is is open to public use and contribution. Within the JavaScript ecosystem, there have been over 350,000 code bases built for the use of anyone that wants to use them. If you clicked on the link above you saw that the URL has `github.io` in it. This shows that the developer of Animate.css is using gitHub to host his portfolio of work which includes Animate.css. Sound familiar?

So what does it mean to use other people's code bases? It means that you get do really cool things in your apps without having to do the very heavy lifting of building the code for all of those cool things. This may not seem important at the moment but I promise you it is. You see, if each of us had to hand-build a sort function, a drop-down menu, a light-box, a Geolocation API, etc.... we'd never get out of the 2000s. We'd never be able to evolve because we'd all be rebuilding the same things! Because we don't have to rebuild these things ourselves, we can work more creatively to find ways to rearrange and synthesize these components in new and fun ways!!

We've talked about some high-level concepts so I'm sure you're wondering how Animate.css comes into play with this **open-source** ecosystem. Turns out that animations, or movements on the page, are commonly used. Instead of re-building/(*recreating the wheel*) these animations, we can use the code built by Dan Eden!

<!-- ! Video Content: Reading Documentation & Animate.CSS (width="655" height="368", ratio 1.77) -->
<iframe src="https://player.vimeo.com/video/396496673" width="655" height="368" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen></iframe>

  > NOTE: This video uses Animate.css version 3.7 and is therefore out-of-date with version 4.1. Nevertheless, it may prove useful to understand how Animate.css is built for your convenience. Play it on 2x speed ;)

## Animate.css

The code for [Animate.css](https://animate.style/) is held in a repo on GitHub, just like all of your projects. Notice that the name has a .css file extension in it. This is because, it's all CSS! Isn't that easy? Yeah, it is. You use it just like you use your own .css files, with a `<link rel="stylesheet" href="">` tag, but instead of style.css value in the href="" attribute you'll do this instead:

    ```html
      <head>
        <link
          rel="stylesheet"
          href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css"
        />
      </head>
      <body>
        <h1 class="animate__animated animate__jello">An animated element</h1>
      </body>
    ```

  > This method requires an internet connection to work, even locally.

In a previous lesson, you came across the word [Content Delivery Network](https://en.wikipedia.org/wiki/Content_delivery_network). This is a really good example. Instead of keeping up with the code for Animate.css in our website's folder, we will pull the code in from CloudFlare, which Dan Eden is using to disperse this code. That's what the URL: "https://cdnjs.cloudflare.com/ajax/libs/animate.css/3.7.2/animate.min.css" is doing; just the same as Google Fonts.

The *alternative method* is that you can [download a minified copy](https://github.com/daneden/animate.css) of it to your local directory, and reference this way:

```html
  <head>
    <link rel="stylesheet" href="./styles/animate.min.css">
  </head>
  <body>
    <h1 class="animate__animated animate__jello">An animated element</h1>
  </body>
```

  > This method assumes you downloaded the code and have it in the website's folder as animate.min.css

### Basic Usage of Animate.css

After you've downloaded the condensed **minified** code or linked the CDN, 

- [ ] all you have to do now is give ANY element you want to be animated the class name `animate__animated`.  
- [ ] then give it the specific class name, like `animate__heartBeat`. You can easily copy/paste them by hovering over the animation style you want and then clicking the "Copy to Clipboard" icon. (See image below)

    ![animate-css-classname-copy-to-clipboard](./../images/animate-css-classname-copy-to-clipboard.png)

Next step is to change delay, speed, and duration. There are **three** different ways to do this...*all of this is clearly in the documentation*.

#### Individual Element

The first and maybe most obvious way to change an elements animation delay, duration, and speed is by calling the element specifically. Let's say we used the same element above but added another class name to it. These code snippets come directly from the [documentation(using `@keyframes`)](https://animate.style/).

  > NOTE: We can assign multiple class names to an element by separating them by spaces.

=== "the HTML"
    ```html
      <head>
        <link
          rel="stylesheet"
          href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css"
        />
      </head>
      <body>
        <h1 class="animate__animated animate__jello my-element">An animated element</h1>
      </body>
    ```

=== "the CSS"
    ```
      .my-element {
        display: inline-block;
        margin: 0 0.5rem;

        animation: bounce; /* referring directly to the animation's @keyframe declaration */
        animation-duration: 2s; /* don't forget to set a duration! */
      }
    ```

#### By Specific Class Name with Custom Properties

The second way is to use **Custom Properties**/**CSS Variables**. What you see below is essentially adding a new property `--animate-duration` to the `.animate__bounce` class elements that also have the `.animate__animated` class name. See that? It's a bit like dot-notation...

```css
  /* style.css file*/
  /* This only changes this particular animation duration */
  .animate__animated.animate__bounce {
    --animate-duration: 2s;
  }
```

You can also use **CSS Variables** in what's known as a **Globally Scoped** variable, that is to say its available to the whole file/namespace rather than just a specific class name like we see directly above.

In this example we see the syntax `:root` which means these properties and values will be applied to all animated elements from the very beginning. This can be overridden with the **Locally Scope** technique we just covered, if needed.

```css
  /* style.css file*/
  /* This changes all the animations globally */
  :root {
    --animate-duration: 800ms;
    --animate-delay: 0.9s;
  }
```

#### All Animations



> NOTE: The newer version of Animate.css (4.1) is focus on web development in Node which is where we're headed but haven't gotten there quite yet. For this reason, using the README will come with challenges so I recommend use the [animate.style](https://animate.style/) page for documentation. Use the CDN method **not** the `npm install animate.css --save` method.

## Practice It

<!-- [Try it yourself](https://codepen.io)! -->

This website gives you a very clear representation of which classes do what. Simply select a class name, and then click "Animate it."

If you've linked the CDN in your <head> (or downloaded and linked the minified CSS file), all you have to do then is give an element that class name you like and tada... you'll get the very same effect on your own HTML element. Simple, no?

Then you can reference the documentation to see the variations of duration, speed, and delay time.

- [ ] Go try it yourself! [Create a new CodePen](https://codepen.io) or repo, whichever you prefer,
- [ ] In your `index.html` file, copy/paste the following code snippet:

    ```html
      <head>
        <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.0.0/animate.min.css">
      </head>

      <!-- This h1 will bounce infinitely-->
      <h1 class="animate__animated animate__infinite animate__bounce">This is a Bouncing Example</h1>
    ```

- [ ] Practice what you just learned about but then go deeper into the documentation starting with "Utility Classes" so you can grow in your ability to read and use documentation while learning how to customize speed, delay and duration in Animate.css.

[Prefers-Reduced-Motion](https://blog.logrocket.com/new-in-chrome-74-prefers-reduced-motion-media-query-50cd89d3e769/)

## Additional Resources

- [ ] [YT, tuber - title]()

## Know Your Docs

- [ ] [MDN Docs - title]()

All Open-Source code will have documentation; [Animate.css](https://animate.style/) is no different. All you have to do is read.
<!-- 

```javascript

```

! height/width = 1.777 ---- width="655" height="368"

| Method      | Description                          |
| ----------- | ------------------------------------ |
| `GET`       | Fetch resource                       |
| `PUT`       | Update resource |
| `DELETE`    | Delete resource |


    `line numbers`
:do you like 'em?


++slash++
https://facelessuser.github.io/pymdown-extensions/extensions/keys/

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

## Animations and Open-Source
What is Minified Code? Why do we need it? What is its purpose?
What does Open-Source mean? How is it used? Where do you see it in the wild?
Why is documentation so important? How do you use documentation?
What are your strategies for approaching documentation?
Why is open-source important to the development of human-centered technology?
How do you think open-source played a role in the fast and vast expansion of the web?
How do you think you can use Open-source code to facilitate the building of your Capstone Project?
Where do you find open-source code?
Does anyone have some interesting open-code they'd like to share with the class?



-->
