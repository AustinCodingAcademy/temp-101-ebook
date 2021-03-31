# Bootstrap Modals

*“Worry does not empty tomorrow of its sorrow, it empties today of its strength. —Corrie Boom*

## Overview
<!-- ! Video Contents:  (width="655" height="368", ratio 1.77) -->

Continuing on with learning useful features of Bootstrap let's play with Modals! To start, we'll need to know what a modal is.

Wikipedia describes a [Modal Window](https://en.wikipedia.org/wiki/Modal_window) as:

  > ".... a graphical control element subordinate to an application's main window. It creates a mode that disables the main window but keeps it visible, with the modal window as a child window in front of it. Users must interact with the modal window before they can return to the parent application."

In short, it's a window/**** that pops up over another window. You've definitely seen a modal pop up when you're repop-upading a Medium article or a reputable newspaper article usually asking you to subscribe. These are annoying for sure and this is why we'll plan to use them sparingly and think about what they are actually accomplishing in our user's story.

For our coding purposes a modal is simply an element in the file whose `display`: property is set to `hidden`; but when an event happens such as a page load or a button is clicked the value is set to block; so it appears. It's then reverted back to `hidden`; after the "x" is clicked, -or the user clicks outside the modal.

Use the following repos to teach yourself how modals work.

## Two Basic Modals from Scratch

For the rest of this class you'll be given code to read and learn from. To do this you'll need to clone the repos give to you and work your way through how they work. *You must approach these with curiosity to learn from them.*

Go ahead now, fork & clone this [101-Modal-Practice repo](https://github.com/AustinCodingAcademy/101-Modal-Practice).

Then open it up with Live-Server and count to 4.
What happens?
How? Go find the code that makes this pop-up happen.
What lines of code create the dismiss functionality?
Can you track down the event that happen to open each of the two modals?
Can you track down how each are changed and dismissed again?

  > NOTE: Although much of this code has been edited to implement the Timed Modal, a majority of the code was taken from this [How To: Modal on W3Schools](https://www.w3schools.com/howto/howto_css_modals.asp).

## Modals with Bootstrap

As you learned in the last section, [Bootstrap](https://getbootstrap.com/docs/4.4/components/modal/) is an incredibly powerful tool to help you quickly build websites and app. It also comes with a Modal component that is 100% customizable and ready to go "**out-of-the-box**"!

Again, a modal is simply an HTML element that's built and sitting in the HTML file but its `display:` property is set to `hidden;` until a particular event triggers the property to be set to `block;`. Bootstrap modals are no different but they do have a few additional features that are useful but take a little more attention to use.

Fork & clone this [101-BS-Modal](https://github.com/AustinCodingAcademy/101-BS-Modal) repo and follow along.

In the `index.html` file you'll see that Bootstrap's CSS and JS CDNs have already been linked and there is code there to create a modal.

- [ ] Open this up with Live-Server to see what's going on.
- [ ] Now read the comments to see how the open button knows which modal to open.
- [ ] Copy/paste the code at the bottom of the file into the body and see what happens.
- [ ] Notice the `data-target` value of the button and the `id` value of the modal. These are how you'll create multiple modals on the same page. **BUT there's another way!!**
- [ ] Scroll to the top of the Bootstrap modal docs and read the "gotchas" before preceding.
- [ ] Go to the [Varying Modal Content section](https://getbootstrap.com/docs/4.4/components/modal/#varying-modal-content) of the Bootstrap Modal docs and implement three different modals with different content but use the same modal.
- [ ] Make sure you create your own silly content.
- [ ] After that implement the [Tooltip Popovers](https://getbootstrap.com/docs/4.4/components/modal/#tooltips-and-popovers)
- [ ] Now structure your content with the [Grid](https://getbootstrap.com/docs/4.4/components/modal/#using-the-grid).
- [ ] And lastly, [change the size of the modals](https://getbootstrap.com/docs/4.4/components/modal/#optional-sizes).

If you completed all of these steps you are well on your way to proving you can work in the tech world!!! Let's keep going so you can can build some killer websites!

## Practice It

<!-- [Try it yourself](https://replit.com)! -->
<!-- [Try it yourself](https://codepen.io)! -->

## Additional Resources

- [ ] [YT, tuber - title]()

## Know Your Docs

- [ ] [W3S How To - Modal](https://www.w3schools.com/howto/howto_css_modals.asp)
- [ ] [Bootstrap.Components.Modal](https://getbootstrap.com/docs/4.4/components/modal/)


<!-- ! END OF VIDEO 101.1.3.1 - TITLE-->
<!-- ? Video Numbering and Title system: CourseNumber.ModuleNumber.LessonNumber.VideoNumber -->
<!-- * (VIDEO 101.2.4.3 - "CSS Selectors") === 101 Course, Module 2, Lesson 4, Video 3 - "CSS Selectors" -->

<!-- 

cp workspace/resources/templateFile.md docs/module- 

```javascript

```

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
-->