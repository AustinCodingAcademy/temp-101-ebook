## Box Model: Border

The border of an element sits just outside the padding and before the margin, usually invisible. In fact, all HTML Elements have a border but have a default value of `null`, meaning you won't see them (See, [Default CSS Values Reference](https://www.w3schools.com/cssref/css_default_values.asp)).

To make a border visible you need to set three values: `border-style`, `border-width`, and `border-color`. [Try it](https://codepen.io/)!

```html
  <p>Hello World</p>
```

```css
  p {
    border-style: groove;
    border-width: 12pt;
    border-color: #FF9633;
  }
```

Just like padding (and margin) there is a short-hand, `border`:

```css
  p {
    border: groove 12pt #AA9933;
  }
```

  > NOTE: Again, this short-hand comes with a warning: it is less readable than the long-hand form.

## More Long-Hand

To complicate things a little more there are properties that allow us to style each side of the border differently. This isn't all that common but it becomes VERY useful when you're creating strange and interesting shapes on the screen. [Try it](https://codepen.io/)!

```css
  p {
    border-style: groove;
    border-top-color: blue;
    border-top-width: 75pt;
    border-right-color: green;
    border-right-width: 40pt;
    border-right-style: dotted;
    border-bottom-color: purple;
    border-bottom-width: 100pt;
    border-left-color: red;
    border-left-width: 60pt;
    border-left-style: dotted;
  }
```

Above you can see there are properties for each side so you are able to control `-style`, `-color`, and `-width` of each side as you please!!

## Border Counts for Total Width

There's a small "gotcha" with borders. Because borders are often invisible they don't have a value on the screen which means that count in the total amount of "available space". But, when you start add value to the `border-width`, it will start to push outward affecting the element's neighbor(s). The docs will say: "Although an element's border is bound to the element itself, border settings will affect neighboring elements."
  
  > NOTE: Check out the docs ahead to see all the values these properties can take.

<!-- ! END OF VIDEO 101.1.23.1 - Box Model: Border -->

## Additional Resources

* [W3S Docs - Border](https://www.w3schools.com/css/css_border.asp)s
* [CodePen - Box Model Visualizer](http://codepen.io/carolineartz/pen/ogVXZj/)
* [W3S Docs  - Default CSS Values Reference](https://www.w3schools.com/cssref/css_default_values.asp)
