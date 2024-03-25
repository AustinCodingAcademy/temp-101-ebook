# Flex Item Properties

Now that you have a basic understanding of using the value `flex` with the property `display` for a "Container" element/Parent element and the associated properties to position the Child elements its time now to see some of the specific properties for the child elements.

As we move deeper in to these properties you'll notice a pattern emerge: properties of HTML Elements set by CSS come in groups because they are associated with each other. For instance, we've covered the Box Model Properties which include `height`, `width`, `padding`, `border`, and `margin` along with all of the sub-properties associated with each of them: `margin-top`, `margin-bottom`, `padding-top`, `border-top`, so forth and so forth. Soon you learn about the `position` property and the `top` and `left` together because they are associated with each other. Now we're in the Display Flex property/value with `justify-content` and `flex-wrap` and all the others.

This pattern is important because it will help you learn faster and deeper! By now, you already have a good understanding HTML element just being objects with properties, methods, and events. You know that JS functions can be triggered by an event on an element like `onclick` and that methods are just built in functions that we don't have to write ourselves. As you move forward trust that you have a good basis to build from and that you CAN learn these seemingly complicated technologies. You got this!!

## The Properties

Items inside a "Container"/Parent Element with its `display` property set to `flex` are said to be **flex items**. When these items are rendered inside a flex display they get unique properties not available outside of the flex container.

As you saw in the [CSS Tricks Flex Guide](https://css-tricks.com/snippets/css/a-guide-to-flexbox/){:target="_blank"} they include:

* [order](https://www.w3schools.com/cssref/css3_pr_order.asp){:target="_blank"} - specifies the order of the flex items. You can tell the 3rd item to be the 1st item to be displayed.
* [flex-grow](https://www.w3schools.com/cssref/css3_pr_flex-grow.asp){:target="_blank"} - specifies how much a flex item will grow relative to the rest of the flex items. Items can be bigger than others.
* [flex-shrink](https://www.w3schools.com/cssref/css3_pr_flex-shrink.asp){:target="_blank"} - how much a flex item will shrink relative to the rest of the flex items. They can also be smaller!
* [flex-basis](https://www.w3schools.com/cssref/css3_pr_flex-basis.asp){:target="_blank"} - specifies the initial length of a flex item. Add as much as you like.
* [align-self](https://www.w3schools.com/cssref/css3_pr_align-self.asp){:target="_blank"} - specifies the alignment for the selected item inside the flexible container and overrides the align-items of the parent container.

  > NOTE: Again, if you like shorthand (and don't mind less code readability), the `flex` property combines flex-grow, flex-shrink, and flex-basis into one.

## Practice It - Giphy Gallery

1. Fork the [Giphy Gallery - https://codepen.io/austincoding/pen/pozQRyQ](https://codepen.io/austincoding/pen/pozQRyQ){:target="_blank"}

2. Take a look at the HTML file. Can you find the `<section class="row portrait-gallery">` code on line 2? Inside this section you'll see three `<img>` elements. The `<img>` element has an attribute/property called `src=`, which stands for source, which is where the image comes from. In this case the images are coming from [giphy.com](https://giphy.com){:target="_blank"} .

3. After that we see another attribute/property called `alt=`, which stands for alternate text. This is for people with blindness that can't see the image we put on the screen. It's important for you to create a descriptive alternate text for them to hear read to them.

4. After that we see `height=` and `width=` which, of course, determine how big the images are.

5. Go ahead and copy/paste this line: `<img src="" alt="what the image is" height="360" width="240">` and add it into the `<section> `tag with the class name `row gallery-two` on line 7, so it looks like this:

    ```html
      <section class="row gallery-two">
          <!--  Copy/Paste the line below for as many images as you'd like   -->
          <img src="" alt="what the image is" height="360" width="240">
          <img src="https://media.giphy.com/media/CBnvmgOvK1d9C/giphy.gif" alt="what the image is" height="360" width="240">
      </section>
    ```

6. Use the suggested links below to copy/paste in between the " " of src="" attribute:

    * [https://media.giphy.com/media/l1KVcrdl7rJpFnY2s/giphy.gif](https://media.giphy.com/media/l1KVcrdl7rJpFnY2s/giphy.gif){:target="_blank"}
    * [https://media.giphy.com/media/l4FGoQFXF7xdU6O7m/giphy.gif](https://media.giphy.com/media/l4FGoQFXF7xdU6O7m/giphy.gif){:target="_blank"}
    * [https://media.giphy.com/media/cJSjCgihYx9GqHXzDN/giphy.gif](https://media.giphy.com/media/cJSjCgihYx9GqHXzDN/giphy.gif){:target="_blank"}
    * [https://media.giphy.com/media/1rK68yfkG1Q8Aw87Lv/giphy.gif](https://media.giphy.com/media/1rK68yfkG1Q8Aw87Lv/giphy.gif){:target="_blank"}
    * [https://media.giphy.com/media/1xlqOpx8T0dlV3ZoHV/giphy.gif](https://media.giphy.com/media/1xlqOpx8T0dlV3ZoHV/giphy.gif){:target="_blank"}
    * [https://media.giphy.com/media/3ohjV5W5NYvGnjJLTa/giphy.gif](https://media.giphy.com/media/3ohjV5W5NYvGnjJLTa/giphy.gif){:target="_blank"}

7. Remember to change the `alt=""` value to describe the gif so that we meet 503 compliance.

8. Repeat this a few times.

    > NOTE: You can also go to giphy.com and find a gif you'd like to use. You'll need the "Gif Link" NOT the "Short Link", "HTML5 Video" or "Embed" link to copy/paste in between the " " of the src="" attribute.

9. Now create a CSS rule for `gallery-two` on line 25 in the CSS file to make it flexible.

    ```css
      .gallery-two {
        display: flex;
      }
    ```

10. Do that again for the third row: `gallery-three`.

11. Once you have at least 9 total images, look at the ones you've added and compare them to the three you started with in the first row: `row portrait-gallery`. What's different? Why?

12. Can you make them match?

13. Change the `order` of your gifs.

14. Can you `-grow` or `-shrink` your gifs?

## Practice It - Flex Box Froggy

Now it's time to have some silly fun with serious results. Go and play, [Flex Box Froggy](https://flexboxfroggy.com/)!

* [How To Froggy](https://player.vimeo.com/video/365836717){:target="_blank"}

## Know Your Docs

Again, I cannot over-emphasize this, read your docs! This is a crucial tool you will use throughout your career and learning to work through them now is **vital** to your success in the future.

* [W3S - Flex](https://www.w3schools.com/css/css3_flexbox.asp){:target="_blank"}
* [MDN - Flex](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Flexbox){:target="_blank"}