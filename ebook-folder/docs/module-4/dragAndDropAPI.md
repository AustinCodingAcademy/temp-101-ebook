# Drag and Drop, an HTML5 API

*The will to win, the desire to succeed, the urge to reach your full potential... these are the keys that will unlock the door to personal excellence. —Confucius*

## Overview

When we say that HTML 5 has a Drag-n-Drop API what we mean is that the elements built into the language: `div`, `article`, `img`, `h1`, etc, etc, all have properties that when set to do *something*, will trigger that *something*. Let's consider the way we've used the `onclick` attribute on a `<button />` element.

The `onclick` attribute is a property that can be set to an **Event Handler Function**, maybe we set it to `"handleFormSubmit()"`. Now when the button is clicked by the user it will fire the code inside the `handleFormSubmit` function in our JavaScript! This is exactly how the Drag-n-Drop API works except that it has different attributes and more of them; but, nevertheless, they all trigger what ever function we provide to them! Let's see it in action!

## The Needed Attributes/Properties

Remember that attributes like: `class=""`, `id=""`, `onclick=""`, etc. are like short-cuts to setting the values of properties & methods on an HTML element. They can look like clutter in your HTML files sometimes but they do well to get the job done and they're a more direct way of communicating with the DOM then writing `addEventListener()` in your JS files, so you'll just have to get used to them. The main attributes we use to interact with the DnD API are:

* `draggable=""`
* `ondragover=""`
* `ondragstart=""`
* `ondrag="`
* `ondrop=""`

With the exception of the `draggable` attribute, each of the other attributes capture an event that can be used to fire any function you build; just like the `onclick` attributes capture a click event to fire any function you'd like it to trigger.

Additional attributes that give you more options and control over your DnD experience can be found at [MDN: HTML DnD API](https://developer.mozilla.org/en-US/docs/Web/API/HTML_Drag_and_Drop_API) and include the following:

* `ondragend=""` - when a drag operation ends
* `ondragenter=""` - when a dragged item enters a valid drop zone.
* `ondragexit=""` - when an element is no longer the drag operation's immediate drop zone/target.
* `ondragleave=""` - when a dragged item leaves a valid drop zone/target.

### How to Use The DnD Attributes

Go ahead and fork & clone this [101-DnD-Demo repo](https://github.com/AustinCodingAcademy/101-DnD-Demo).

To begin dragging an element we have to tell the browser that the element can be dragged by giving the element the attribute: `draggable="true"`

```html
  <img draggable="true" src="../image/flower.png" alt="picture of a flower" />
```

Many elements already have this property/attribute set to true by default but it's good practice to go ahead and make it true for whatever elements you want to work with as draggable elements.

Now we'll need a place to drag the element, the **drop zone/target**. Essentially be telling the browser that when our dragged element is taken to a specific location on the screen, let's not *prevent* it from being dropped. To do this we use a method on the **event** called `.preventDefault()`.

What is the **event**? Again, just like an `onclick` it's the thing that happens between a user and the app, the event, and it's actually data we can access too! So in our DnD example we might be using the attribute `ondrag` but the *event* is "Drag" and `ondrop` attribute is really watching for a "Drop" event. But we don't normally call them by their name instead we use parameter names like `event`, `ev`, or simply `e`. It doesn't matter what we call it because it's always passed into the **Event Handler Function**, the function we built that we want to be fired when the event happens.

I know that was a lot but I promise it's much simpler than it sounds. Let's see it in action for two places we'd like for the "Draggable" element to be dropped:

```html
<!-- below the previous div element -->
<div ondragover="allowDrop(event)">

</div>
<div ondragover="allowDrop(event)">

</div>
```

Now create a function called `allowDrop`

```js
const allowDrop = (e) => {
  e.preventDefault();
}
```

  > NOTE: Notice in the HTML that we pass in `event` but in the JS we use the parameter name `e`. This is okay. We can call them whatever we want as long as we know what's going on in the program.

The `.preventDefault()` method is a special function used to tell the browser to do something different than it is normally supposed to do. [MDN has a nice example of preventing the click of a checkbox(its default setting)](https://developer.mozilla.org/en-US/docs/Web/API/Event/preventDefault)

Now that we've called the `.preventDefault()` method the browser will allow an element to be dropped on the element you'd like for it to be dropped on. If you'd like, we can add a visual element to this so we the human can see it happening by adding & removing a class name from the "dropzone" elements:

=== "the HTML"

    ```html
      <!-- HTML for Adding Visual of Valid Dropzone -->
      <div id="div2" ondrop="drop(event)" ondragover="allowDrop(event)"></div>
    ```

=== "the CSS"

    ```css
      /* CSS for Adding Visual Cue of Valid Drop Zone 
      by Creating a Rule for an Element with this Class Name
      */
      .hovering {
        background: rgba(0, 151, 19, 0.3);
      }
    ```

=== "the JS"

    ```js
      // JS for Adding a Visual of a Valid Drop Zone by Adding a Class Name
      const allowDrop = (e) => {
        e.preventDefault();
        // add "hovering" to the classList of the targeted drop zone element
        document.getElementById(e.target.id).classList.add("hovering")
      }
    ```

But this isn't everything! We still have to capture the data, set it, get it, then append it to the targeted drop zone!

### Tranferring the Data on Drop

Now that we have "Draggable" elements and "Drop Zone" elements let's see how we grab the data of the thing we're actually going to drag!

Right when we grab an element to be dragged we get access to yet another DOM event: **dragstart**. To use it we simply type the attribute: `ondragstart=""` then give it an event handler function we've built in JS:

HTML for Capturing and Passing the Event over to an Event Handler Function

```html
  <!-- HTML for Capturing and Passing the Event over to an Event Handler Function -->
  <img draggable="true" ondragstart="drag(event)" src="../image/flower.png" alt="picture of a flower" />
```

```js
  /* 
    - JS for Creating an Event Handler Function 
   that Will Take the Event and Set the Data for the Transfer
   - We have to use ES5 not ES6 syntax for this event handler due to the context needed to capture the data. */

  function drag(e) {
    e.dataTransfer.setData("text", e.target.id);
  }
```

Just like the `.preventDefault()` method, the event also has a property called `.dataTransfer` which has a method called `.setData()` which, as you guessed, *sets the data* to be transferred.

Imagine the element that's being dragged is being put into a "pseudo state" between the place it's pickup and put down. In this in-between state the browser will have to know the data to store so it can safely put it down where we choose. To set the data to be transferred we use the `.setData()` method which takes two arguments, `format` and `data`.

In the example above you see the format will be `"text"`, and the data will be the dragged element's `id`, as you see in `e.target.id`

### Dropping the Data

Finally we need to drop the data into the location we choose. To do that we use the same techniques we've been doing except we use a different attribute: `ondrop=""` and then use the opposite method from `.setData()`, -`.getData()`.

`.getData()` is still on the `.dataTransfer` *object-thing* so we just add it to an event handler function that will be fired when an element is dropped on a drop zone element:

```html
<!-- Looking at the attribute: ondrop="drop(event)" -->

<div id="div2" ondrop="drop(event)" ondragover="allowDrop(event)" ondragleave="stopDrop(event)">

</div>
```

```javascript
// Event Handler Function
const drop = (e) => {
  // standard preventDefault
  e.preventDefault();
  // extract & hold the data we set in the dataTransfer property
  const data = e.dataTransfer.getData("text");
  // use the "data" we set as a reference to what dragged element we want to drop.
  // then append it to the element we are doing the drop event on
  e.target.appendChild(document.getElementById(data));
}
```

## Practice It

Go to the [101-DnD-Demo repo](https://github.com/AustinCodingAcademy/101-DnD-Demo) you cloned earlier and solve the problems laid out in the comments.

## Know Your Docs

- [ ] [MDN Docs - Drag & Drop API]((https://developer.mozilla.org/en-US/docs/Web/`API/HTML_Drag_and_Drop_API))
- [ ] [MDN Docs - preventDefault()](https://developer.mozilla.org/en-US/docs/Web/API/Event/preventDefault)
- [ ] [Reference, Alligator.io - Modify Class Names in JS](https://alligator.io/js/classlist/)
- [ ] [Reference, FontAwesome - How to Use Icons](https://fontawesome.com/how-to-use/on-the-web/referencing-icons/basic-use)

## Additional Resources

- [ ] [CodePen, Coding_Journey - Advanced DnD](https://codepen.io/Coding_Journey/pen/YzKpLvE)
- [ ] [YT, Coding Journey - HTML Drag and Drop API](https://youtu.be/7HUCAYMylCQ)
