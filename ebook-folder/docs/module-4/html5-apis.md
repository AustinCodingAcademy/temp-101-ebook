# The HTML5 APIs

*Look up at the stars and not down at your feet. Try to make sense of what you see, and wonder about what makes the universe exist. Be curious. —Stephen Hawking*

## Overview

Again, there are SO many options for you to learn and the great thing about learning web development is there is SO much to learn!! Seriously, everyday you could be deepening and/or broadening your knowledge base just by going to work. Wouldn't that be cool!?!

Today we're going to learn about the built-in APIs of HTML5. Already you've been working with some of them like Fetch and Canvas. But before we can learn how to use any more of theme we should first learn a bit of the history of HTML and how we got to this moment you're in now, able to use these built-in APIs!!

To do this we'll start with an extraordinary [NebraskaJS conference](https://nejsconf.com/) talk where [Zeno Rocha](https://zenorocha.com/zip-code-and-happiness/) breaks down the history of HTML, the changes with HTML5, why/what/how to use some of the best HTML APIs as well as how to step out of your comfort zone to experiment and make magic happen!

<!-- ! Video Contents: Coding Tech - JSConf: Zeno Rocha, Web APIs You Probably Didn't Know Existed -  (width="655" height="368", ratio 1.77) -->
<iframe width="655" height="368" src="https://www.youtube.com/embed/EZpdEljk5dY" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## What Makes up the HTML5 APIs?

But how does it work? Remember how the DOM is an upside-down tree structure? It has branches that consist of nodes, which are just *object-things* (collections of key-value pairs which just branch out into — other nodes/*object-things* , containing other nodes, and so on and so on?

### The Document Object-Thing

The `document` object is the top-level node in this structure, so that, starting with `document`, we could use dot-notation to call any one of the method or properties it has, such as `.getElementById()`. We could also refer to one of the properties belonging to `document` in the same way, such as `document.domain`, which would give us the domain name of the server that loaded the page. And the same is true of the lower(child) nodes...they have their own properties and methods. For instance:

```html
<p id="our-element">
Hello World!!
</p>
```

```javascript
const x = document.getElementById("our-element")

console.log(x.innerHTML); // = Hello World!!
```

If we logged out `x.innerHTML` when `x` is set to capture the `<p id="our-element">` element on our document we'd get what's on the inside of it: `"Hello World!!"`.

### The Window Object-Thing

When we're talking about HTML APIs, we need to conceptualize the `document` node as the top, or root object of the DOM tree; but there is actually yet another object above it in the tree structure, which is not part of the DOM, but contains the entire DOM as one of its own properties. This great-grandmother of objects is the `window` object. It's known as the **Global Object** of a web page. It represents the browser's window that is displaying the `document`. And, in addition to `document` (and the rest of the DOM), `window` has its own properties and methods, one of these properties is the `navigator` object as in: `window.navigator`.

#### The Navigator Object

You can think of the `navigator` object-thing as a sister element to `document` and, unsurprisingly, it also contains its own properties and methods that provide information about the user's browser. To access a property within `navigator`, you would, again, use dot-notation, thus: `window.navigator.`*someProperty*.

And, actually, in the case of the properties and methods of the window object, we don't even have to use window explicitly when referring to them. Since `window` is the **global object**, sitting at the top of the whole tree structure, the browser knows that when we write `navigator.`*someProperty* in our JavaScript, we implicitly mean `window.navigator.`*someProperty*.

##### A Few Properties Available on The `navigator` Object

* `.appCodeName` returns the code name of the browser.
* `.appName` returns the name of the browser.
* `.appVersion` returns the version information of the browser.
* `.cookieEnabled` determines whether cookies are enabled in the browser.
* `.geolocation` returns a Geolocation object that can be used to locate the user's position.
* `.language` returns the language of the browser.
* `.onLine` determines whether the browser is online.
* `.platform` returns for which platform the browser is compiled.
* `.product` returns the engine name of the browser.
* `.userAgent` returns the user-agent header sent by the browser to the server. 

*Here's a [complete list](https://www.w3schools.com/jsref/obj_navigator.asp).*

It's all of these properties and methods on the `window`, `navigator`, and [other related objects](https://developer.mozilla.org/en-US/docs/Web/API/Window) that create all of the HTML5 APIs like `geoLocation`, `canvas`, and `fetch`.

#### Practice It - Navigator Object

Open your browser's dev tools and go to the Console Tab.

- [ ] Type in `navigator.online` + ++enter++
- [ ] Type in `navigator.language` + ++enter++
- [ ] Type in `navigator.userAgent` + ++enter++
- [ ] Type in `navigator.geolocation` + ++enter++
- [ ] What did you see each time?
- [ ] How many other properties and methods do you see on the navigator object?

## More HTML5 APIs

* **Ambient Light API**: provides information about the ambient light levels, as detected by a device’s light sensor.
* **Battery Status API**: provides information about the battery status of the device.
* **Canvas 2D Context**: allows drawing and manipulation of graphics in a browser.
* **Clipboard API**: provides access to the operating system’s copy, cut and paste functionality.
* **Contacts**: allows access to a user’s contacts repository in the web browser.
* **Drag and Drop**: supports dragging and dropping items within and between browser windows.
* **File API**: provides programs secure access to the device’s file system.
* **Forms**: gives programs access to the new data types defined in HTML5.
* **Fullscreen API**: enables full-screen display of elements within web pages, and temporarily suppresses display of the browser's own user interface.
* **Gamepad API**: supports input from USB game-pad controllers.
* **Geolocation**: provides web applications access to geographical location data about the user’s device.
* **MediaDevices.getUserMedia()**: provides access to external device data (such as webcam video).
* **History API**: allows programs to manipulate the browser history.
* **HTML Microdata**: provides a way to annotate content with computer-readable labels.
* **Indexed database**: creates a simple client-side database system in the web browser.
* **Internationalization API**: provides access to locale-sensitive formatting and string comparison.
* **Offline apps**: allows programmers to make web apps available in offline mode.
* **Proximity API**: provides information about the distance between the device and another object.
* **Screen Orientation**: reads the screen orientation state (portrait or landscape), and gives programmers the ability to know when it changes, and to lock it in place.
* **Selection**: supports selecting elements in JavaScript using CSS-style selectors.
* **Server-sent events**: allows the server to push data to the browser without the browser needing to request it.
* **User Timing API**: gives programmers access to high-precision timestamps to measure the performance of applications.
* **Vibration API**: allows access to the vibration functionality of the device.
* **Web Audio API**: is an API for processing and synthesizing audio.
* **Web Messaging**: allows browser windows to communicate with each other across different origins.
* **Web Speech API**: provides speech input and text-to-speech output features.
* **Web Storage**: allows the storage of key-value pairs in the browser.
* **Web Sockets**: opens an interactive communication session between the browser and server.
* **Web Workers**: allows JavaScript to execute scripts in the background.
* **XMLHttpRequest2**: improves XMLHttpRequest, eliminating the need to work around same-origin policy errors, and making it work with new features of HTML5.

Here's a reference for more information about these and other [web APIs](https://developer.mozilla.org/en-US/docs/Web/API).

## Additional Resources

- [ ] [Article, CreativeBloq - Guide to HTML5 APIs](https://www.creativebloq.com/html5/developer-s-guide-html5-apis-1122923)
- [ ] [YT, Steve Griffith - Web APIs Playlist](https://www.youtube.com/playlist?list=PLyuRouwmQCjlBGMxI_0Ly_Dw-vrniOYNh)

## Know Your Docs

- [ ] [MDN Docs - The Web APIs](https://developer.mozilla.org/en-US/docs/Web/API)
- [ ] [MDN Docs - Window Object](https://developer.mozilla.org/en-US/docs/Web/API/Window)
- [ ] [MDN Docs - Navigator Object](https://www.w3schools.com/jsref/obj_navigator.asp)
