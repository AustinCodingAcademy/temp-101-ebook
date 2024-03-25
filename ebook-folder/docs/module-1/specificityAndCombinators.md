# Specificity and Combinators

Specificity is the means by which browsers decide which CSS property values are the most relevant to an element and, therefore, will be applied.

Remember this order - it is critical for understanding how to properly apply (and debug) CSS.

| Least Specific |           More Specific              | Most Specific  
| -------------- | ------------------------------------ | ------- |
| Type selectors and pseudo-elements | Class selectors, attribute selectors and pseudo-classes | ID selectors |
| `h1`, `:before`, etc... | `.example`, `[type="radio"]`, `:hover`, etc	| `#example` |

Universal selector (`*`), combinators (`+`, `>`, `~`, `' '` (space)) and negation pseudo-class (`:not()`) have no effect on specificity. (The selectors declared inside :`not()` do, however.)

Inline styles added to an element (e.g., `style="font-weight:bold"`) always overwrite any styles in external stylesheets - in a sense they can be considered to have the highest specificity.

Take a look at the following code and determine what color the paragraph is going to be. Then *uncomment* the CSS and see if you are correct!

## CSS Combinators

If you haven't picked up on this yet, you can stack multiple selectors on top of one another separated by a comma like so:

```css
  body, h1, p, section, div {
    border: 1px solid black;
  }
```

to give the same properties & values to multiple elements without typing them over and over again. The snippet above would make all `body`, `h1`, `p`, `section`, `div` elements have a 1-pixel-wide-solid-black-border around them.

If you don't put a comma between the selectors you'll create **Descendent Selectors** which select an element that is a descendant/child element/grandchild element of another specified element. These rules will apply to all descendants within that specified parent element. In short, descendant selectors are separated by a space with the parent selector on the left and the descendant on the right which is the one that is actually getting targeted.

```css
  /* "body" is the parent and "h1" is the targeted descendant element */
  body h1 {
    font-size: 1.75em;
  }

  /* "section" is the grandparent and ".warning" is the parent and "p" targeted descendant element */
  section .warning p {
    color: red;
    font-weight: bold;
  }
```

Perhaps the most useful are **Child selectors** which match an element that is a direct child of another. It will not include grandchildren and down. It is more restrictive than a descendant selector. It uses a `>`.

```css
  body > main {
    font-size: 1.75em;
  }

  section > article > h2.title {
    color: red;
    font-weight: bold;
  }
```

### Practice It - Specificity

**MUST DO: [CSS Diner](https://flukeout.github.io/){:target="_blank"} !!**

## Additional Resources

* [YT, Clayton@ACA - CSS](https://youtu.be/XnwlIF6pSWU){:target="_blank"}
* [YT, DevTips - CSS Basics pt. 3](https://youtu.be/emMO3iCpvrc){:target="_blank"}

## Know Your Docs

* [Article, Carl Camera - CSS Poker](https://carl.camera/default.aspx?id=95){:target="_blank"}
* [W3S Docs - Pseudo Classes](https://www.w3schools.com/css/css_pseudo_classes.asp){:target="_blank"}
* [Article, SmashingMagazine - CSS Inheritance and Cascade](https://www.smashingmagazine.com/2016/11/css-inheritance-cascade-global-scope-new-old-worst-best-friends/){:target="_blank"}