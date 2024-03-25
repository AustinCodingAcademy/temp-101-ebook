## Box Model: Margin

Continuing on with our Box Model properties, we arrive now at `margin`.

Beyond the edge of the `border` lies the `margin`. If you add margin to any side of an element, it will push against other elements near it and create an invisible barrier between the elements. If you were looking at an image gallery, the margins would create the **gutter** between each column and row of images.

Just like `padding` and `border` we can set the values of all four margins like the following:

```css
p {
  margin-top: 10%;
  margin-right: 15%;
  margin-bottom: 1%;
  margin-left: 15%
}
```

## The Margin Short-Hand

Again, like `padding` and `border` there are short-hands versions that are harder to read. However, if you have uniform margin on all for side it maybe be easier to just write something like this:

```css
/* In this example, 15pt of margin will be applied to all four sides of the element */
.margin-on-all-sides {
  margin: 15pt;
}
```

And if you have equal margins on the left and right and equal margins on the top & bottom you could right it like this:

```css
/* In this example, 15pt will be applied to the TOP and BOTTOM margins, 30pt to the LEFT and RIGHT margins*/
.TopBottom-LeftRight {
  margin: 15pt 30pt;
}
```

This is a very common form of the short-hand to center an element:

```css
.topBottom-leftRight-centered {
  margin: 15pt auto;
}
```

## The Worst Short-Hand

The last two short-hands are so confusing they're not really worth mentioning but just so you have them as a reference here they are:

```css
/* the TOP margin will be 15pt, the RIGHT 30pt, the BOTTOM 25pt, the LEFT 20pt (clockwise)*/
.T-R-B-L {
  margin: 15pt 30pt 25pt 20pt;
}

/* :yuck: */

/* In this example, 15pt on the TOP margin, 30pt on LEFT and RIGHT margins, 45pt on BOTTOM margin*/
.Top-LeftRight-Bottom {
  margin: 15pt 30pt 45pt;

  /* :barf: */
}
```

You can do the same thing but with a little more typing that results in **far more readable code**!

```css
.T-R-B-L {
  margin-top: 15pt;
  margin-right: 30pt;
  margin-bottom: 25pt;
  margin-left: 20pt;
}

/* YAY, MUCH MORE READABLE CODE WE'LL GET HIRED FOR!!!!! */
```  

<!-- ! END OF VIDEO 101.1.23.1 - Box Model: Margin -->

## Additional Resources

* [W3S Docs - Margin](https://www.w3schools.com/css/css_margin.asp){:target="_blank"}
* [CodePen - Box Model Visualizer](http://codepen.io/carolineartz/pen/ogVXZj/){:target="_blank"}
* [W3S Docs - Default CSS Values Reference](https://www.w3schools.com/cssref/css_default_values.asp){:target="_blank"}