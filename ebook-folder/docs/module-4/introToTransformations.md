# Intro to Transformations

*“I have found the paradox, that if you love until it hurts, there can be no more hurt, only more love.“ —Mother Teresa*

## Overview

CSS transformations are a lot like CSS Animations but instead of use the `@keyframe` function to execute on specific animation-names you can use specific functions within the declaration block of an element's CSS rules to change is properties from within on a specific DOM event or timing. These specific transform functions include: `translate()`, `rotate()`, `scale()`, and `skew()`.

With these transformation functions you can change an element's shape, size, position and even duplicate itself!!!

## Parent & Nested Selectors

Before you can use CSS Transformations we'll need to learn a new way to use CSS selectors: **Parent** & **Nested**. It looks like this:

```css
.square {
  background: Khaki;
  border-radius: 5px;
  height: 150px;
  margin: 100px
    ;
  transition: transform 1s;
  width: 150px;

  &:hover {
    transform: skew(-20deg);
  }
}
```

In the code snippet above you see that we select the class name "square", the **Parent Selector** then inside it has an additional rule at the bottom: `&:hover` which is the **Nested Selector**. It's like saying, "This element will have all of these rules but also has these...when this event happens."

In the `&:` declaration block we can apply our transformations functions!! So let's get to them!

## To transform an element, simply give it the transform property, and assign one of the following functions as its value:

1. `translate()` - takes 1 or 2 arguments of any **length** or **percentage** value like `px`, `pt`, `%`, or `em`. If given 1 argument it will only apply that to the x-axis. To use the y-axis you must give it 2 arguments.
  Long-hand alternatives:
    * `translateX()`
    * `translateY()`
2. `rotate()` / `rotateZ()` - Both functions take 1 argument of positive or negative `deg`(degrees).
3. `skew()` - Takes either 1 or 2 arguments of `deg`(degrees). If given 1 it will apply the value of degrees to both the x-axis and the y-axis. Can take positive & negative degrees.
  Long-hand alternatives:
    * `skewX()`
    * `skewY()`
4. `scale()` - Takes 1 or 2 number arguments to apply the size the element will grow or shrink along the x-axis and y-axis.

```css
  /* make a, h1 element duplicate and slide down and to the right on a hover event */
  h1:hover {
    /*                 x-axis  y-axis     */
    transform: translate(20px, 20px);
  }


  /* flip an image upside-down on a hover event */
  img:hover {
    transform: rotate(180deg);
  }

  /* make a header change shape by skewing it's left and right side downward and upward on a hover event */

  header:hover {
    transform: skewY(-20deg);
  }

  /* make a button grow twice its size on a hover event */
  button:hover {
    transform: scale(2);
  }
```

### Z-Index + 3D Transformations

Even though the web screen looks two-dimensional we can create the illusion that it's three-dimensional with the `z-index` property. With this property we can push images or other element backward: `z-index: -1;`, `z-index: -2;`, etc. All elements by default set to `z-index: 0` so any element you want to bring forward you just add a `1` and any you want to push back you subtract a `-1`.

Below you you'll find all of the 3D functions you'll need to turn your 2D world 3D!!

* [`translateZ()`](https://developer.mozilla.org/en-US/docs/Web/CSS/transform-function/translateZ)
* [`rotateX()`](https://developer.mozilla.org/en-US/docs/Web/CSS/transform-function/rotateX)
* [`rotateY()`](https://developer.mozilla.org/en-US/docs/Web/CSS/transform-function/rotateY)
* [`rotate3d()`](https://developer.mozilla.org/en-US/docs/Web/CSS/transform-function/rotate3d)
* [`scale3d()`](https://developer.mozilla.org/en-US/docs/Web/CSS/transform-function/scale3d)

## Additional Resources

- [ ] [Resource, HTMLDOG - Transformations](https://htmldog.com/guides/css/advanced/transformations/)
- [ ] [MUST READ, ThoughtBot - Transitions and Transforms](https://thoughtbot.com/blog/transitions-and-transforms)

  > Side Note: [Webflow](https://webflow.com/) may be a neat tool for you to learn later on, if you're interested in front-end work or web design!

- [ ] [Article, CSS Tricks - Text Rotate](https://css-tricks.com/snippets/css/text-rotation/)
- [ ] [YT, Webflow - 2D & 3D Transforms](https://youtu.be/bPF156ZvgAM)

<!-- ! Video Contents:  (width="655" height="368", ratio 1.77) -->

## Practice It

1. Fork this [CodePen](https://codepen.io/austincoding/pen/xxGNjRo)

  - [ ] create three new squares with different class names and colors.
  - [ ] use the other three 2D Transformation functions to make each new square rotate, or grow, or translate on a hover event.

2. Change the color of the underlines in this [CodePen](https://codepen.io/austincoding/pen/pweWJp/).

<!-- [Try it yourself](https://replit.com)! -->
<!-- [Try it yourself](https://codepen.io)! -->
## Know Your Docs

- [ ] [MDN Docs - translate()](https://developer.mozilla.org/en-US/docs/Web/CSS/transform-function/translate)
- [ ] [MDN Docs - translateX()](https://developer.mozilla.org/en-US/docs/Web/CSS/transform-function/translateX)
- [ ] [MDN Docs - translateY()](https://developer.mozilla.org/en-US/docs/Web/CSS/transform-function/translateY)
- [ ] [MDN Docs - rotate()](https://developer.mozilla.org/en-US/docs/Web/CSS/transform-function/rotate)
- [ ] [MDN Docs - skew()](https://developer.mozilla.org/en-US/docs/Web/CSS/transform-function/skew())
- [ ] [MDN Docs - skewX()](https://www.w3schools.com/css/tryit.asp?filename=trycss3_transform_skewx)
- [ ] [MDN Docs - skewY()](https://www.w3schools.com/css/tryit.asp?filename=trycss3_transform_skewy)
- [ ] [MDN Docs - scale()](https://developer.mozilla.org/en-US/docs/Web/CSS/transform-function/scale)


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