# More Grid Properties

Just like with flex, when we use grid we have a load more properties that we get to use to get our web pages to look exactly the way our designers laid them out to be. We'll cover many of them here but be sure to checkout the **Know Your Docs** section to see more, get your short-hand code (if you like), and reference all the properties available with `grid`.

## Grid Gaps

Between each of the Grid Items are gutters or gaps. You can adjust the size of these Gaps with the following properties: `grid-column-gap` and `grid-row-gap`

```css
.grid-container-element {
  display: grid;
  grid-column-gap: 8pt;
  grid-row-gap: 2pt;
}
```

## Justify-Content & Align

Justify-Content & Align
Since you're already familiar with the additional properties with `flex` you'll be happy to know that you can do the same thing with `grid`:

```css
.grid-container-element {
  display: grid;
  /* position on the x-axis */
  justify-content: space-evenly;
  /* position on the y-axis */
  align: center;
}

/* You can also use: space-between, space-around, start, end, and center */
```

## The Unit: fr

So far we've given our rows and columns percentages of the display. But as you work with other people's code you'll likely come across `fr`, a unit of fractions. It stands for a fraction of the total available space.

In the snippet below we have 4 equally sized columns. They are laid out the same way as we saw earlier by giving 4 values to the `grid-template-column` property. But instead of `%` we'll use `fr`.

```css
.our-parent-container {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr 1fr;
}
```

In the next snippet we'll see 4 columns again but now the two on the left will be half the width and the one on the right will be twice the width:

```css
.our-parent-container {
  display: grid;
  grid-template-columns: .5fr .5fr 1fr 2fr;
}
```

When using frs it's important to make sure the numbers add up to the **whole number equal to the number of columns** just the same way we make sure that our percentages total 100. So if we have 5 columns, our `frs` need to add up to 5, i.e. `1fr 2fr 1fr .5fr .5fr`, `1fr 1fr 1fr 1fr 1fr` or `.5fr 1fr 1fr 2fr .5fr`, etc.

## The Short-Hands

We won't cover these in detail because you don't necessarily need them right away but just incase you want to advance your skills let's make you aware of them:

`grid-area` property can be used as a shorthand property for the `grid-row-start`, `grid-column-start`, `grid-row-end` and the `grid-column-end` properties.
`grid-template-areas` [take values of elements with the Parent Container and arrange them depending on their order](https://www.w3schools.com/cssref/pr_grid-template-areas.asp).

## Practice It - CSS Grid

### Part One: FR & Gap

[fr & CSS Gap CodePen](https://codepen.io/austincoding/pen/OzZQoY/)
    - [ ] Fork the CodePen,
    - [ ] In the CSS file, change the values on line 4 but be sure to maintain the total value of the number of columns,
    - [ ] On line 11, change the width of the gaps.
    - [ ] MUST DO! the CSS Grid Garden

### Part Two - Grid Garden!!

- [ ] **MUST DO**: Play [CSS Grid Garden](http://cssgridgarden.com/).

  > If you get stuck, there are two hints for 26 and 28 below in the scrambled text.

=== "Warning!"
    ```markdown
    In the next tab there are answers to #26 and #28.
    But first, push yourself to see if you can work through these two problems on your own.
    ```

=== "Hidden Answers"
    ```markdown
      **WARNING ANSWERS BELOW**

    > //////////////////////////////////////////////

    > 88 : 00 = 5% 6^ 7& 8* 9() 1! 2@ 3# 4$ 5% 6^ 7&
    > 88 : 00 = 5% 6^ 7& 8* 9() 1! 2@ 3# 4$ 5% 6^ 7&
    > *26: grid-template-rows: 50px 0 0 0;* 1! 2@ 3#
    > 88 : 00 = 5% 6^ 7& 8* 9() 1! 2@ 3# 4$ 5% 6^ 7&
    > *28: 1fr 50px/ 20% 80%;*  1! 2@ 3# 4$ 5% 6^ 7&
    > 88 : 00 = 5% 6^ 7& 8* 9() 1! 2@ 3# 4$ 5% 6^ 7&

    > //////////////////////////////////////////////
    ```

## Additional Resources

- [ ] [YT, LayoutLand - Easy Layout with CSS Grid](https://www.youtube.com/embed/tFKrK4eAiUQ)
- [ ] [Article, CSS Tricks - Intro to FR Units](https://css-tricks.com/introduction-fr-css-unit/)
- [ ] [Article, Alligator IO - Grid Areas](https://alligator.io/css/css-grid-layout-grid-areas/)
- [ ] [Article, SmashingMagazine, Best Practices with Grid](https://www.smashingmagazine.com/2018/04/best-practices-grid-layout/)

## Know Your Docs

* [W3S Docs - Grid](https://www.w3schools.com/css/css_grid.asp)
* [W3S Docs - Grid Container](https://www.w3schools.com/css/css_grid_container.asp)
* [W3S Docs - Grid Item](https://www.w3schools.com/css/css_grid_item.asp)
* [CSS Tricks - Grid Trick](https://css-tricks.com/snippets/css/complete-guide-grid/)
