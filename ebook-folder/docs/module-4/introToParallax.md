# Parallax

*“Somehow I can’t believe that there are any heights that can’t be scaled by a man who knows the secrets of making dreams come true. This special secret, it seems to me, can be summarized in four C s. They are curiosity, confidence, courage, and constancy, and the greatest of all is confidence. When you believe in a thing, believe in it all the way, implicitly and unquestionable.” —Walt Disney*

## Overview
<!-- ! Video Contents:  (width="655" height="368", ratio 1.77) -->

While this section is titled "Parallax" we'll be using this time to learn something a little more important: Teaching yourself new tricks(aka, learning how to learn)!

This lesson will be using [W3Schools How To lesson on Parallax](https://www.w3schools.com/howto/default.asp) because we want for you to not only know how to create [parallax effects](https://www.impactbnd.com/blog/what-is-parallax-scrolling) for your websites but ALSO to teach yourself to read other people's code, learn from their techniques, and implement them in your projects.

That said, as we work through this short lesson we'll be referencing the [How To: Parallax at W3Schools](https://www.w3schools.com/howto/howto_css_parallax.asp).

Go ahead and create a new CodePen or repo to follow along as we build this cool and useful effect.

### What is a Parallax Effect?

The long answer it that it relates to the perspective of two different observers viewing a single object. It's used to calculate distance to an object in space. But the word has been adopted into web development to mean the viewing of a background from different points that makes it appear to scrolls at a different speed than the rest of the site's content. You, undoubtedly, have [seen this before] so let's get to how to actually make it happen!

## Additional Resources

- [ ] [YT, pizzabagles - What is Parallax](https://youtu.be/53rqXj5CLFs)
- [ ] [YT, Lucky Gunner Ammo - Rifle Scope Parallax](https://youtu.be/1VPGcq9IVxc)
- [ ] [YT, iEatWebsites - Hot to Create a Cool Parallax Effect](https://youtu.be/d34GsFz-HkY)

## Creating a "Fixed" Background

To have an image "slide" behind our other content at a different scrolling speed we'll need to do two things:

1. Create an image container.
2. Use the `background-attachment` property with the value fixed.

  > To reiterate, we will be following along with the [How To: Parallax at W3Schools](https://www.w3schools.com/howto/howto_css_parallax.asp)!

To create an image container we can use the non-semantic element `div` and give it a class name to select it with. Then, nn our CSS we can give this div element a background and height/width properties:

=== "the HTML"
    ```html
      <div class="parallax"></div>
    ```

=== "the CSS"
    ```css
      /*
      To use percentage(%) values to size the div element we'll have to:
      - also give the html element 100% to size to the full height of the viewport
      - and the same to the body element so it is 100% the height of the HTMl element
      */
      body, html {
        height: 100%;
      }

      .parallax {
        height: 100%;
        background-image: url("img_parallax.jpg");
        background-position: center;
        background-repeat: no-repeat;
        background-size: cover;
      }
    ```

Now that we have an image on the screen that isn't repeating, fit the full-screen and is centered let's add the last piece to make it scroll slower!

```css
  body, html {
    height: 100%;
  }

  .parallax {
    height: 100%;
    background-image: url("img_parallax.jpg");
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    /* Give the value "fixed" to the background-attachment property to create the parallax scrolling effect */
    background-attachment: fixed;
  }

  /* Some mobile devices have a problem with background-attachment: fixed. So, you can use media queries to turn off the parallax effect for mobile devices: */
  @media only screen and (max-device-width: 1366px) {
    .parallax {
      background-attachment: scroll;
    }
  }
```

To see this better you'll need to add some other sections into your HTML that will scroll normally. Try copy/pasting from the example's source code.

- [ ] Open your inspector tool.
- [ ] Select the "Source" tab.
- [ ] Click the `tryhow_css_parallax_demo.htm` file
- [ ] Then copy/paste lines 77-110 and find the CSS you'll need to style them.
- [ ] GO AHEAD! TRY IT!
