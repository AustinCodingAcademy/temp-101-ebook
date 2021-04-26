# HTML Attributes

When we say **attributes** in HTML we're talking about the bits of code inside the **opening tag** of the element like `id="box"`, `input="submit"`, `href="https://website.com"`, etc. These bits of code store useful **values** inside what we call **properties** on the Element object. These **values** communicate crucial information to the browser about what it's supposed to do with the HTML, CSS, and JS code it receives.

 > While we will interchangeably call this bits of information **attributes** and **properties** -know that we're talking about the same thing.

## Class

The HTML `class=` attribute is used to specify a `class` for an HTML element. Unlike the `id` attribute, multiple HTML elements can share the same `class` name.

### USING THE CLASS ATTRIBUTE

The class attribute is often used on multiple HTML elements to point styling rules to all of them. In JavaScript class names can be used to access and manipulate only elements with the specific class name.

In the following example we have three `<div>` elements with a class attribute with the value of `"city"`. All of the three `<div>` elements will be styled equally according to the `.city` style definition in the CSS:

=== "the HTML"

    ```html
    <!DOCTYPE html>
    <html>
      <body>

        <div class="city">
          <h2>London</h2>
          <p>London is the capital of England.</p>
        </div>

        <div class="city">
          <h2>Paris</h2>
          <p>Paris is the capital of France.</p>
        </div>

        <div class="city">
          <h2>Tokyo</h2>
          <p>Tokyo is the capital of Japan.</p>
        </div>

      </body>
    </html>
    ```

=== "the CSS"

    ```css
    .city {
      background-color: tomato;
      color: white;
      border: 2px solid black;
      margin: 20px;
      padding: 20px;
    }
    ```

## HTML Burger

Here is an exercise for you to interact with and to continue to help with your learning.

Make the burger your own, you can click the open Sandbox button and interact with it in the editor and make your own unique burger.

<iframe src="https://codesandbox.io/embed/html-burger-o9qwj?fontsize=14&hidenavigation=1&theme=dark"
     style="width:100%; height:500px; border:0; border-radius: 4px; overflow:hidden;"
     title="HTML Burger"
     allow="accelerometer; ambient-light-sensor; camera; encrypted-media; geolocation; gyroscope; hid; microphone; midi; payment; usb; vr; xr-spatial-tracking"
     sandbox="allow-forms allow-modals allow-popups allow-presentation allow-same-origin allow-scripts"
   ></iframe>