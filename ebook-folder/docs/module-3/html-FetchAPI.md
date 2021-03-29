# HTML Fetch API

*“I decided, very early on, just to accept life unconditionally; I never expected it to do anything special for me, yet I seemed to accomplish far more than I had ever hoped. Most of the time it just happened to me without my ever seeking it.” –Audrey Hepburn*

## What is the HTML Fetch API?

<!-- ! Video Contents: 101 - HTML Fetch API (width="655" height="368", ratio 1.77) -->
<iframe src="https://player.vimeo.com/video/409867819" width="655" height="368" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen></iframe>

=== "The JavaScript"

    ```javascript
      const getRemoteData = () => {
        fetch('https://jsonplaceholder.typicode.com/todos/1')
          .then(response => response.json())
          .then(json => console.log(json))
      }
    ```

=== "The HTML"

    ```html
      <button onclick="getRemoteData()">Get Data</button>
    ```

- Take the code snippet you see above and throw it into one of your projects.
- Create a button and attach a function to it that when clicked will call this fetch code.
- Check out the [JSON Placeholder Documentation](https://jsonplaceholder.typicode.com/).

  > HINT: Start with changing the end of the URL in the request from 1 to 2...or something else...

## Additional Resources

- [ ] [YT, Paul Halliday - How to Use Fetch](https://youtu.be/tVQgfKqbX3M)
- [ ] [YT, Web Dev Simplified - Fetch API in 6 mins](https://youtu.be/cuEtnrL9-H0)

## Know Your Docs

You've become used to W3Schools as your main documentation provider. But as you move into JavaScript, I suggest you start learning with Mozilla Developer Network(MDN) documentation. They have more robust explanations and cover deeper topics in web development.

- [ ] [MDN Docs - Fetch API](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API)
- [ ] [W3S Docs - JSON](https://www.w3schools.com/js/js_json_intro.asp)
- [ ] [MDN Docs - Response](https://developer.mozilla.org/en-US/docs/Web/API/Response)
- [ ] [JSON Placeholder Documentation](https://jsonplaceholder.typicode.com/)


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