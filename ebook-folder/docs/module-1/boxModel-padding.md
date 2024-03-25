## Box Model: Padding

After we've decided how big an element's content should be using `height:` and `width:` we should starting thinking about the space between the content and the border, the **padding**.

Padding is the space between the element's border and the content itself. If you had a bird's-eye-view of a pool table, you can think of the padding as the cushions or banks between the wooden outside border and the content inside, the billiard balls and green felt.

As you saw before there are for properties that address the padding of an element:

* `padding-top` - holds the value of the padding at the top of the element
* `padding-right` - holds the value of the padding on the right side of the element
* `padding-bottom` - holds the value of the padding at the bottom of the element
* `padding-left` - holds the value of the padding on the left side of the element

Each of these properties gives you control of the four different sides of the element. However, if you intend to have equal padding on either side and a different amount of padding for the top & bottom you might try the short-hand property: `padding` and write them with only two values:

```css
  /* The element(s) with the class name: my-other-element will have 20 points of padding on the top & bottom and 10 points of padding on the right & left */
  .my-element {
    padding: 20pt 10pt;
  }
```

And if you wanted to have an equal amount of padding all the way around you could write it like this:

```css
  /* The element(s) with the class name: my-other-element will have an absolute padding of 20 points on all four sides*/
  .my-other-element {
    padding: 20pt;
  }
```

While you *can* use four values to specify the four sides in this short-hand it gets **hard to read and remember the order**: TOP, RIGHT, BOTTOM, LEFT (clockwise)

```css
  /* The element(s) with the class name: my-last-element will have 20 points of padding on the top, 5 points on the right, 10 points on the bottom and 1 point of padding on the left*/
  .my-last-element {
    padding: 20pt 5pt 10pt 1pt;
  }
```

For **code readability**, you should use the long-hand form of the padding properties to specify 4 different values:

```css
  .my-readable-code {
    padding-top: 20pt;
    padding-right: 5pt;
    padding-bottom: 10pt;
    padding-left: 1pt;
  }
```

## Additional Resources

* [W3S Docs - Padding](https://www.w3schools.com/css/css_padding.asp){:target="_blank"}
* [CodePen - Box Model Visualizer](http://codepen.io/carolineartz/pen/ogVXZj/){:target="_blank"}
* [W3S Docs - Default CSS Values Reference](https://www.w3schools.com/cssref/css_default_values.asp){:target="_blank"}

<!-- ! END OF VIDEO 101.1.21.1 - Box Model: Padding -->