# The Image Element

*“Hope can be a powerful force. Maybe there's no actual magic in it, but when you know what you hope for most and hold it like a light within you, you can make things happen, almost like magic.” ―Laini Taylor,* **Daughter of Smoke & Bone**

HTML is the only language that web content is encoded in. No matter what programming language you work in, if you're serving your software through the web you'll be encoding that software's content to the user in HTML. Because HTML is the only language for the web, it has to be super flexible to handle all of the crazy cool stuff we see on the web. Just stop and think for a moment about [some of the coolest websites](https://www.awwwards.com/) you've seen. All of that was built in HTML!!

So when you're wondering when you'll know everything there is to know about HTML, well maybe never...but the upside is that there is always something to learn! In this lesson, we'll spend time on the Image Element, `<img />` because during class and your upcoming career you'll need to display the images.

We won't cover all of the "special HTML elements" a.k.a **[Replaced Elements](https://developer.mozilla.org/en-US/docs/Web/CSS/Replaced_element)**: in this lesson like: `<video>`, `<embed>` and `<iframe>` but just know if you're wanting to build videos into a web page you can read the docs on these two elements and all the other HTML elements!!

<!-- Video Subject: Special HTML Elements -->
<iframe src="https://player.vimeo.com/video/395992193" width="655" height="368" frameborder="0" allow="autoplay; fullscreen" allowfullscreen></iframe>

## Using the Image Element

You've probably already recognized the Image Element, `<img />`, from a Learn-to-Code event or from your Portfolio Landing page. This takes the fear out of learning yet another *Object-Thing*!

To begin, the `<img />` known as a **self-closing** or **void** element because it doesn't keep its content between the opening- and closing-tags like most other HTML elements do, instead it uses two properties/**attributes** to *source* its content:

* `src=""` - the source of the actual image in the form of a URL or pathname
* `alt=""` - A description used to replace the image if a person who is blind is using your web page.

Take a look at the following code snippet:

```html
  <img 
    src="https://images.unsplash.com/photo-1590004987778-bece5c9adab6?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1502&q=80"
    alt="Grapefruit wedges spaced evenly apart on orange background."
  />
```

![grapefruitWedges](./../images/grapefruitWedges.png)

Similar to `src=` attribute on the Script Element, `<script src="">`, the Image element sources its image with the same attribute, `src=""`. While the `alt=""` attribute stands for "alternative text" and is used in place of the image when it is not being displayed or when someone with a visual impairment visits your page. This "alt" text is required for screen readers—accessibility devices used primarily by the visually impaired—to be able to communicate image content to their users. For this reason, you should put lengthy and descriptive alternative text so that screen readers can actually communicate what is in the image.

  > NOTE: It's important to know that a pathname and a URL are essentially the same thing but differ in a small but large ways: a pathname refers to a path from one file on your computer to another file on your computer, but a URL refers to a path from a file on your computer to a file on another computer that is connected to your computer through the internet. Both do the same thing because the storing structure of your computer, my computer, and everyone else's computers are the same. However, with a URL we use HyperText Transfer Protocol or HTTP(S).

* [W3S Docs - Image Element](https://www.w3schools.com/tags/tag_img.asp)

### Styling Images

Styling Images can be tricky because they are a "special element" known as a **Replaced Element**. This means they don't quite follow the same CSS rules as most other elements. So the best way style an image is to put it inside a Div element and style the Div:

=== "The HTML"

    ```html
      <div id="image-container">
        <img 
          src="https://cdn.pixabay.com/photo/2016/03/27/19/31/fashion-1283863_960_720.jpg"
          alt="folded blue and white knit sweater on white background">
      </div>
    ```

=== "The CSS"

    ```css  
        #image-container {
          margin: 1% auto;
          text-align: center;
          padding: 5% auto;
        }
    ```

In addition to styling an Image with a **"wrapper" Div**, Image elements have two special properties on them that control the content(the actual image) held within the Image Element object. They're called:

* [object-fit](https://developer.mozilla.org/en-US/docs/Web/CSS/object-fit) - determines the size of the content(image) inside the Image object/element.
* [object-position](https://developer.mozilla.org/en-US/docs/Web/CSS/object-position) - determines the position of the content(image) inside or outside the Image object/element.

The following code snippet would be paired with the code snippets you just saw above:

 ```css
   /* styles.css file */
 
   #image-container > img {
     object-fit: contain;
     object-position: 50% 50%;
     width: 250px; /* <-- image height is proportionally controlled with the width property */
   }
 ```

Try it. Go to the MDN Docs on [object-position](https://developer.mozilla.org/en-US/docs/Web/CSS/object-position) & [object-fit](https://developer.mozilla.org/en-US/docs/Web/CSS/object-fit) and play!

### Image as Background Technique

An alternative to styling an Image Element is setting the background of a Div Element to the image you want displayed:

=== "The HTML"

    ```html
      <!-- HTML -->
      <div id='elephant-pic'></div>
    ```

=== "The CSS"

    ```css
    /* the CSS */
    .elephant-pic {
      width: 300pt;
      height: 200pt;
      background-image: url(./images/Elephant-At-Sunrise.png);
      background-size: cover;
      background-repeat: no-repeat;
    }
    ```

=== "The Result"
    ![Elephant-At-Sunrise](./../images/Elephant-At-Sunrise.png)

This last technique is convenient but comes with the drawback of not being **Semantic**. For now, that's shouldn't be of high concern to you though.

The videos below demonstrate how you would use both techniques.

## Additional Resources on Styling Images

- [ ] [YT, Dani Krossing - Inserting Images](https://youtu.be/_w6N_nplmAw)
- [ ] [YT, Chris Walker - IMG for Images](https://youtu.be/PDfWeUP09TA)

## Know Your Docs

- [ ] [MDN Docs - Replaced Elements](https://developer.mozilla.org/en-US/docs/Web/CSS/Replaced_element)
- [ ] [W3S Docs - Image Element](https://www.w3schools.com/tags/tag_img.asp)
- [ ] [MDN Docs - object-position](https://developer.mozilla.org/en-US/docs/Web/CSS/object-position)
- [ ] [MDN Docs - object-fit](https://developer.mozilla.org/en-US/docs/Web/CSS/object-fit)
 
<!-- ! END VIDEO - 101.1.15.1 - The Image Element -->