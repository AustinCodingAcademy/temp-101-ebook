# The DOM + JS Intro Part Two

## The Document

The **document** or `document` is the *Mother of All Objects*. It is where your `body`, `header`, `footer`, `title`, `meta`, and all other HTML elements are created. This *"Mother of All Objects"* has a whole list of properties and methods we can use, some of which you'll see in the video below.

  > In this video , we'll cover a few things in a slow and careful way. Take your time through it and make sure you re-create the task on your own either in a new repo or a codePen.

<iframe src="https://player.vimeo.com/video/393569778" width="655" height="368" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen></iframe>

  > The following will make more sense if you watch the video above first.

<iframe src="https://player.vimeo.com/video/395213797" width="655" height="368" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen></iframe>

To begin, a Method is a special type of Property; in that, a property just holds a value like: `font-size: 12pt`. While a method looks the same as a property it is actually a **Function** stored in the value of the property name, i.e. `write: function(){// code that writes to the document}`. This subtle difference helps us understand what we're talking about in the future.

* **Property** - holds a value that represents a particular attribute.
* **Method** - a functionality of the object stored in an accessible location.
* **Event Listener** - a special function that "listens" for certain events, or interactions, in order to trigger a specified action when the "event" happens.

In either case, when we access a property or a method we use **Dot-Notation**, aka the **Member Operator**. It looks like this: `.`. Seriously, to get the property `write()` on the Document Object, we type `document.write()`. Remember, the Document Object Model is a way we, as humans, can visualize the way these HTML Elements are written under-the-hood.

  > NOTE: The following code snippet is **not** real code, just a representation that can help you visualize what methods look like on the Document Object:

```json
document = {
  addEventListener: // a function that attaches an event handler to the document
  adoptNode: // a function that adopts a node from another document
  close: // a function  that closes the output stream previously opened with document.open()
  createAttribute: // a function that creates an attribute node
  // createComment:  a function that creates a Comment node with the specified text
  createDocumentFragment: // a function that creates an empty DocumentFragment node
  createElement: // a function that creates an Element node
  createEvent: // a function that creates a new event
}
```

STOP! It's important you don't get overwhelmed with all of these **methods**. You don't need to know all of them or even most of them. You'll only use a few of them for the majority of your career. In the video above we only use `document.getElementById()`.

For a full list of the available `document` methods [visit and bookmark the docs page](https://www.w3schools.com/jsref/dom_obj_document.asp).

### document.getElementById()

Just like we use Selectors in CSS to access a specific element and change its properties, in JavaScript, we have access to a few methods that help us get elements by their specific attributes or type. The `getElementById()` method is a very common method that accesses an element by an id. In the video above we use it to "grab" an element then change its `style.display` property.

There are many other methods to get an element by its `class` name or `data` or type. For now, all you need to know is that they exist and when you need to use them there are [docs you can reference](https://www.w3schools.com/jsref/dom_obj_document.asp).

### `onclick=` & Event Listeners

It's a little confusing at first but I think you'll get the hang of it. While the Document Object has methods like the one we just discussed, each and every HTML element also has methods available to them. The methods are usually associated with the action of a user interacting with it so we call them **Event Listeners**. They listen for **Events**, or interactions, between the user and objects in the Document Object Model(**DOM**).

One of the most common Event Listeners to use is `onclick`. It, of course, listens for a click from the user's mouse. When the user clicks on that element an event **bubbles** up and we we can point that action to trigger something to happen, like a function to load more pictures or login. In the video above, we use the user's click to trigger a function that sets the element's `display` property to `none` so it disappears from the page.

=== "HTML"
    ```html
      <button onclick="sayHello()">Click To See a Greeting</button>
    ```

=== "JS"
    ```js
    function sayHello() {
      window.alert("Hello")
    }
    ```

There are many Event Listeners so just breathe for now and be happy that you know this one. But if you're looking for more there are always [more docs to study](https://www.w3schools.com/jsref/dom_obj_event.asp).

## JS Keywords

### Use `let` to Declare Variables

Just the same way CSS and HTML have specific words that mean something to the browser, so does JavaScript. In HTML we have words like `<section>` and `class=""` and in CSS we have `color:` and `solid`. JavaScript has a whole set of keywords we'll learn to use in time but the first one we need is: `let`, as in *let* me store something here.

When we program we usually need a place to store data. This data could be a number, a word, an HTML Element, or a function. Whatever it is, we need to store it for later use. In the above video we used two variables to hold two numbers: `70` & `5`. Then we add them together by referencing their variable name and not the numbers themselves.

We also used the keyword `const` but you'll regularly see `let` and `var`. I will now break these three words down once and for all while I continue to reinforce how/when to use them as we learn more about programming.

* `var` is the **old way** to declare a variable. We don't use it anymore but you will still see it in old code bases.
* `let` is used when we expect for the value of the variable to change.
* we use `const` when we expect for the value to stay the same.

We'll get into the nitty gritty of this later on but for now just know that's why there are two different words to do the "same" thing. For now, *let*'s just use the keyword `let` to **declare** and **define** all of our variables.

```javascript
let aVariable = 7
let anotherVariable = "hello"
```

### Function Signatures

In the video you two different ways to declare functions:

```javascript
  function myFunction() {
    // this is the old way of declaring a function in JS
  }

  const myFunction2 = () => {
    // this is the new and preferred way of declaring a function in JS
  }
```

  > Again, there is an old way and a new way to write functions in JS. You'll still see the old way so we must teach you it but you'll learn to write functions in the new format.

You also so something like this written in the HTML:

```javascript
  myFunction() // this is how we invoke a function in JS
  myFunction2() // no matter how the function is declared in JS
```

The difference between these two examples is subtle but vastly different! 

The first, `const myFunction2 = () => {}` & `function myFunction() {}`, is a **Function Signature** or **Function Declaration**. This is where we write the instructions to be used later.

The second, `myFunction()` & `myFunction2()`, is a *Function Invocation* which means we're calling the function or saying, "Hey, do your thing now!" This is when we use the instructions previously written.

  > If none of that made sense, here's Joe, who might be able to explain it better.

<iframe src="https://player.vimeo.com/video/373457883" width="655" height="368" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen></iframe>

## Know Your Docs

- [ ] [W3S Docs - Document Object](https://www.w3schools.com/jsref/dom_obj_document.asp)
- [ ] [W3S Docs - DOM Event Listeners](https://www.w3schools.com/jsref/dom_obj_event.asp)