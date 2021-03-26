# The Video Element

*“In a time of destruction, create something.” ―Maxine Hong Kingston*

## Overview

Continuing on with our *Special HTML Element Week*, we're going to cover two important elements today: `<video>` & `<iframe>`. These elements are similar to the `<img/>` element but have some funny but useful attributes to play with.

<!-- ! Video Contents: The Video Element  (width="655" height="368", ratio 1.77) -->
<iframe src="https://player.vimeo.com/video/396008957" width="655" height="368" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen></iframe>

### The Video Element & Its Attributes

The `<video>` tag creates an HTML Video Element that will embed a media player into a page. This allows the user to interact with video playback inside the `document`. Just as you learned with the `<img />` element, the video element will get its content via the path to the media file specified inside a `src=""` attribute. Videos also come with the `width` & `height` attribute just like the <img/> element. But a few more attributes you haven't seen before include:

* `autoplay` - sets the element's `autoplay` property to true which tells the browser to play the video as soon as the page loads.
* `controls` - sets the element's `controls` property to true which provides built-in play/pause buttons and a tracking slider.
* `poster` - means thumbnail, which is the initial image you see before a video plays. If this attribute isn't specified the browser will use the first frame in the video. This attribute takes a pathname or URL.
* `muted` - sets the element's `muted` property to true which means the video will begin with no volume.
* `loop` - sets the element's `loop` property to true which means the video will play again when it finishes.

```html
  <video 
    src="./videos/myMovie.mp4" 
    width="320" height="240" 
    poster="./images/myMovieThumbnail.png" 
    autoplay controls
  >
  <video>
```

### Video Sources

The `<video>` element is pretty versatile. In fact, you can use it to provide multiple types of video files for multiple browsers. Say if you used [`.webm`](https://www.webmproject.org/about/) as a video format for Chrome but a user came to your site using Safari which only supports `.mp4` format you could deliver to them the "same video" through different formats by creating two `<source> `elements as child elements inside the parent `<video>` element. Check it out.

```html
  <!-- HTML for Multiple Possible Sources Video Elements -->
  <video width="320" height="240" poster="./images/myMovieThumbnail.png" autoplay controls muted >

      <!-- If using Chrome, this video will be shown -->
      <source src="./videos/myMovie.webm"
              type="video/webm" />

      <!-- If using Safari or other browsers that don't support .webm then use this video -->
      <source src="./videos/myMovie.mp4"
              type="video/mp4" />

      <!-- And if neither are supported, give them this text as a default. -->
      <p>Your browser doesn't support the HTML5 Video Element. Here is a
          <a href="https://www.youtube.com/myhandle/myVideo">link to the video instead.
          </a>
      </p>
  </video>
```

  > NOTE: the `<source />` tag, like `<img />`, is self-closing, having no closing tag paired with it. In the new HTML5 specifications, it is optional to include the slash (conventionally written with a space preceding it) before the final angle bracket (*i.e., `<source>` works just as well as `<source />`*). HTML5 simply ignores the slash, but some technologies that intersect with HTML (*such as XML, and the JSX language used with React*) do require the slash; so it doesn't hurt to develop the habit of using it in elements that don't have closing tags, which are called **void elements**.

  > NOTE 2: Do you see where we placed a `<p>` tag in our `<video>` element? This serves as something like an `alt=""` text? In case the video doesn't load for the user, we explain the reason for this in the `<p>` tag, and provide a URL link to the youTube version of the same video in the `<a>` tag.

## The IFrame Element

So the `<video>` element is pretty straight-forward but remember, it is only used when you own the content, as in, it resides on your server. So what do you do if you don't own the content? Say for a youTube video? Well, that's where we use an [Inline Frame element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/iframe).

The `<iframe>` represents a nested browsing window, which effectively embeds another HTML page within the current page. You can include any number of `<iframe>` elements inside the `<body>` of a document, each of them displaying a separate page in the area covered by the `<iframe>`. While it can be used to display video, the `<iframe>` can **also** be used for things like games, code snippets for CodePen or Repl.it, and advertising. When it comes to video, `<iframe>` is used primarily when we are linking to the video on YouTube or Vimeo rather than storing the file on our server.

### IFrame Caution

You should know there are some security risks involved with the `<iframe>` element. The risk revolve around the fact that you are "effectively embed[ding] another HTML page within the current page". We won't go into the technicalities of this because it is beyond the scope of this course but you should be aware as you move forward. Read this short article, [3 Reasons You Might Not Want To Use Iframes](https://www.ostraining.com/blog/webdesign/against-using-iframes/) by Alex Smirnov to get an idea of the problems surrounding this special element.

## Additional Resources

- [ ] [YT, Kody Simpson - How to Use Video Tag](https://youtu.be/Ynuz1UGPoTg)
- [ ] [YT, tipswithpunch - Embed YouTube Video](https://youtu.be/9YffrCViTVk)
- [ ] [YT, Dani Krossing - HTML5 Video Embed](https://youtu.be/OOy764mDtiA)

  > NOTE: In the last video you'll learn about the CSS property `position` which is **very useful hack** to making element do what we want!

## Know Your Docs

- [ ] [MDN Docs - iFrame Element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/iframe)
- [ ] [MDN Docs - Video Element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/video)

<!-- ! END OF VIDEO 101.1.3.1 - TITLE-->
<!-- ? Video Numbering and Title system: CourseNumber.ModuleNumber.LessonNumber.VideoNumber -->
<!-- * (VIDEO 101.2.4.3 - "CSS Selectors") === 101 Course, Module 2, Lesson 4, Video 3 - "CSS Selectors" -->

<!-- 

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