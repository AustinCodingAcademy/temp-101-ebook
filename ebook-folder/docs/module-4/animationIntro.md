# Intro to Animations

*“If one dream should fall and break into a thousand pieces, never be afraid to pick one of those pieces up and begin again. “ —Flavia*

## Overview

Animations, while not a definitive skill you must master, do create needed flare on websites and can set you apart from other candidates.

The first thing you should learn is to not build your own, but instead "steal" ideas from others at [CodePen.io](https://codepen.io/) -just search for "animation." This is a great place to get ideas, and learn how to do different things. Don't be afraid to fork someone else's code, and break it, trying to figure out how they did it. It really is the best way to learn! After enough stealing you'll become a pro but for now, let's look into the basics of animations using CSS so you can steal well.

## How to use CSS Animations

When making animations in CSS, we are actually just setting the style of an element to make it look a certain way at one point in time, then specifying a new look for a different point in time, and then setting how long it will take for the change to happen. We do this using `@keyframes`, along with `animation-name`, `animation-duration`.

When you define CSS styles inside the `@keyframes` rule, the animation will plot a gradual change from one to the next that takes a specified percentage of the total time given to complete.

To get started let's build a simple `<div>`:

```html
  <div class="animated-div"></div>
```

Then we have to give the element an animated name so the `@keyframe` function knows what to target. In the code snippet below, we'll add some style, an `animation-name`, and some `animation-duration` time.

```css
  .animated-div {
      width: 100px;
      height: 100px;
      background-color: red;
      animation-name: example;
      animation-duration: 4s;
  }
```

With the code above we can see that the element will start at 100px by 100px, be red and the change will happen over 4 seconds.

Now we can call the `@keyframes` function and pass it the `animation-name` we want to execute on which is `example` in this example.

Now you see that code if fairly straightforward: it will change from red background to yellow background.

  > NOTE 1: You can see the full code and [try it out yourself at W3S](https://www.w3schools.com/css/tryit.asp?filename=trycss3_animation1).

  > Note 2: The `animation-duration` property defines how long in seconds an animation should take to complete. If the `animation-duration` property is not specified, no animation will occur, because the default value is `0s` (0 seconds).

In the example above, we have specified when the style will change by using the keywords "from" and "to," which represent 0% (start) and 100% (complete), respectively.

It is also possible to use percentages **explicitly**, and by doing so you can add as many style changes as you like to happen throughout the duration of the animation!

```css
  @keyframes example {
      0%   {background-color: red;}
      25%  {background-color: yellow;}
      50%  {background-color: blue;}
      100% {background-color: green;}
  }
```

[Try it for yourself](https://www.w3schools.com/css/tryit.asp?filename=trycss3_animation2)!

<!-- ! Video Contents: YT, DarkCode - Simple Text Animation  (width="655" height="368", ratio 1.77) -->
<iframe width="655" height="368" src="https://www.youtube.com/embed/Syg_9iB1vco" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Practice It

- [ ] Open and Fork the [CodePen](https://codepen.io/hipperger/pen/GwEqpY/).
- [ ] Change the color of each square in the CSS file.
- [ ] Change the animation duration from 1.5 seconds to 3 seconds, and run it.
- [ ] See if you can get the squares to go the opposite direction.
- [ ] Don't be afraid to get so immersed you spend hours playing around. That's how you get good at coding! *Nerd out!*

## Additional Resources

- [ ] [YT, tuber - title]()

## Know Your Docs

- [ ] [MDN Docs - Animation](https://developer.mozilla.org/en-US/docs/Web/CSS/animation)
- [ ] [W3S Docs - Animation](https://www.w3schools.com/css/css3_animations.asp)


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