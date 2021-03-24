# Common Event Listeners

Since our web pages are built for a human user to interact with it would make sense that we have some built in tools to capture their actions and do something with it. For this purpose, think of a user interaction with the web page as an **Event** and we'll be **Listening** for them. Remember, with programming we just need one action to trigger another action to trigger another action. So as we learn more about programming in JavaScript all you have to remember is that if you want a user trigger a script you built, just go back and find the event listener that will capture that event. Here's a list of a few of the **common** event listeners:

### Common Mouse Events

* `dblclick`: when the mouse button is rapidly clicked on an element
* `mousedown`: when the mouse button is pressed on an element
* `mouseup`: when the mouse button is released on an element
* `onclick`: when the mouse button is pressed & released on an element

### Common Keyboard Events

* `keydown`: when a key is pressed,
* `keyup`: when a key is released

### Common Form Events

As if you didn't have enough to remember about Forms, there are event specific to them!

* `onfocus`: when a user bring into focus a form element either by clicking on it or tabbing to it.
* `onblur`: this is the opposite, as soon as they move away from the element.
* `onchange`: when a value of an input is changed
* `onsubmit`: when a form is submitted.

  > NOTE: onsubmit triggers a page reload. As you use this event listeners you'll also have to use `event.preventDefault()` to [prevent the default page reload](https://www.w3schools.com/jsref/event_preventdefault.asp).

### Common Window Events

* `window.resize`: when the window is resized
* `window.onhashchange`: when an anchor tag has changed
* `window.onload`: when the page has finished loading
* `window.unload`: when the page has been closed

We've just thrown a lot of event listeners at you. It important to breathe and just know you only have to be aware of them so you can use them when you need. You don't have to memorize them right now. Just take notes and remember that these methods are built in and ready for you to use at anytime.

## Know Your Docs

- [ ] [W3S Docs - Event Listener Attributes](https://www.w3schools.com/tags/ref_eventattributes.asp)