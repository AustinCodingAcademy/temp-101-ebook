# Intro to Transitions

*“When life knocks you down, try to land on your back. Because if you can look up, you can get up.” –Les Brown*

## Overview

Animations & Transformations are nice, but to really control the movements of our elements we'll need to dive a bit deeper into what makes them work, what functions the properties are expecting, and what values those functions accept. Let's do it!

## Transitions with CSS

CSS transitions specify how Animations, Transforms, and pseudo selections will happen. So instead of saying *what* will happen in the change, the `transition` property details *how* something will change as in: how long the change will take place or at what rate the change will take place.

  > NOTE: *This does not replace Animation or Transform but instead is used together to enhance the change.*

To use a transition in your animations or transformation you give the first CSS declaration block the property `transition`:
<!-- ! Video Contents:  (width="655" height="368", ratio 1.77) -->

```css
  /* This code tells img elements to be 300px wide and when they change width to follow the rules to do it in 2 seconds, start fast and end slowly(ease-out), and delay by 250ms */

  img {
    width: 300px;
    transition: width 2s ease-out 250ms;
  }

  /* Then on a hover event to change the width to 400px */
  img:hover {
    width: 400px;
  }
```

The transition property takes the following values in this order: "property", "duration", "timing-function", "delay" where:

* [property](https://css-tricks.com/almanac/properties/t/transition-property/) - details the properties that will change during the animations or transform like width, height, or color, etc. You can also use `all` to select all the properties on the element.
* [duration](https://css-tricks.com/almanac/properties/t/transition-duration/) - given in values of `s`/seconds or `ms`/milliseconds, i.e `3s`/ 3 seconds or `30ms`/ 30 milliseconds.
* [timing-function](https://css-tricks.com/almanac/properties/t/transition-timing-function/) is a special value that determine the rate to change within the duration of the change and it takes one of these values:

  * `ease`
  * `linear`
  * `ease-in`
  * `ease-out`
  * `ease-in-out`
  * `step-start`
  * `step-end`

  > NOTE: Click the timing function link to find out about each of these values.

* [delay](https://css-tricks.com/almanac/properties/t/transition-delay/) - obviously refers to the time between the event happening on the DOM like an on-hover to the beginning of the movement. It too takes values of `s` or `ms`.

```css
  /* transition: [property] [duration] [timing-function] [delay]; */
  transition: all 0.5s ease-in-out 1s;
```

### Transitions Continued

Think of the pseudo selectors we've been using like :hover. We know the elements change when we hover over them but this currently happens quickly and harshly. What if we wanted the transition to be smoother? That's where the CSS property `transition-...` comes in.

  > NOTE: *Transitions work with psuedo-selectors, animation keyframes, & transformations*

When you use a the transition property you're simply telling the element, "Get ready, I'm giving you instructions on how you'll be changing and how long it will take for you to get there. Ready?"

Now, when the element is hovered on it will change according to how long you told it to do so.

Let's create another red square and give it the `transition` property.

=== "the HTML"

    ```html
      <div class="transition-example"></div>
    ```

=== "the CSS"

    ```css
      .transition-example {
          width: 100px;
          height: 100px;
          background: red;
          transition: width 2s ease-out 500ms;
      }
    ```

Now let's tell it what will look like when someone hovers over it:

```css
  .transition-example:hover {
    width: 300px;
  }
```

### Behind the Transition Property

`transition` is actually short-hand for four properties:

`transition-property`,
`transition-duration`,
`transition-timing-function`, and
`transition-delay`.

If you remember, it works a lot like `grid-area` that's short-hand for:

`grid-row-start`,
`grid-column-start`,
`grid-row-end`, and
`grid-column-end` properties.

**You don't** have to use the short-hand transition. In fact, you should use the long-hand for code readability. Here's an example of what you just saw above, only now in long-hand form:

```css
  .transition-example {
      width: 100px;
      height: 100px;
      background: red;
      /* transition: width 2s ease-out 500ms;*/
      /* the following will do the same thing as the line above would do */
      transition-property: width;
      transition-duration: 2s;
      transition-timing-function: ease-out;
      transition-delay: 500ms;
  }
```

Make sure you study each property in the docs, so you know what you're actually doing when you use `transition`.

  > Note 1: *If the duration is not specified, the transition will happen instantaneously, because the default value is `0`.*

#### Vender Prefixes

In the above code example, we see a use of `transition` that will work in most browsers, but it *won't* work in Safari, Firefox, Opera if you don't use the [vendor prefixes](http://prefixr.com/what-are-vendor-prefixes.php). To meet the requirements for these browser, you'll also have to include the following rule **before** the traditional rule:

```css
    -webkit-transition: width 2s ease-in-out 500ms; /* Safari Browser*/
    -moz-transition: width 2s ease-in-out 500ms; /* Firefox */
    -o-transition: width 2s ease-in-out 500ms; /* Opera */
    transition: width 2s ease-in-out 500ms
```

## Additional Resources

- [ ] [Article, Zinoui - CSS Transitions](https://zinoui.com/blog/css-transitions)
- [ ] [YT, The Net Ninja - Transitions](https://youtu.be/oYlJR4Le228)

## Practice It

- [ ] Fork the [CodePen](https://codepen.io/austincoding/pen/dRvVMb/)
- [ ] Change the color of the main text to a color of your choice.
- [ ] Change the text to your name
- [ ] Change the duration of the transitions from `1s` to `5s`.
- [ ] Change the easing function of the transition. Use the values you learned above.
- [ ] Comment out the Vendor Prefixes on lines 13-16 & 38-41.
- [ ] Change the `rotate() `and `scale()` functions out for other transformation functions.
- [ ] Can you make it 3D?

## Know Your Docs

- [ ] [MDN Docs - CSS Transitions](https://developer.mozilla.org/en-US/docs/Web/CSS/transition)


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