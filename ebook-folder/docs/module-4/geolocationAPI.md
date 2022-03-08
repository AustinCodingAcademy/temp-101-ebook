# Geolocation, An HTML5 API

*Good, better, best. Never let it rest. 'Til your good is better and your better is best. —St. Jerome*

## Overview
<!-- ! Video Contents:  (width="655" height="368", ratio 1.77) -->

Now that you have a handle on what HTML5 APIs are available for you to use, let's figure out how to use one and cover it some detail. The Geolocation API is a really useful API for adding functionality that lets the user and the app interact with their physical world. Let's get started!

## The Geolocation API

The HTML5 Geolocation API lets you communicate with a user's device to obtain their relative location using the [Global Positioning System, launched in 1960 for Dept. of Defense](https://www.geotab.com/blog/what-is-gps/) use only until it was released for civilian use in 1983. With this incredible technology, you can share data specific to the location of the device viewing the websites and apps you've built. *Ever wondered how Pokemon Go or Uber works*?

By writing just a little bit of JavaScript, you can capture [latitudinal and longitudinal coordinates](https://www.latlong.net/). After you have this coordinates data you can do simple tasks like offer the user the local weather or greet them with a city specific phrase: "Good Morning Dallas, TX!" AND later on, when you learn to build servers & databases, you could send this Lat/Long coordinates to a back-end web server to perform location-aware tasks, such as finding & suggesting local businesses or sharing the user's location with friends, etc.

## Practice It

For a better understanding of how this works you'll have to do more investigation on your own:

- [ ] Fork and clone this [101-Geolocation-Demo](https://github.com/AustinCodingAcademy/101-Geolocation-Demo) repo.
- [ ] Run it and figure out how it's working. Check your `console.log` statements.
- [ ] Read the `README.md` file and see if you can solve the two challenges by reading the MDN - [ ] Docs and watching the two videos below.

  > NOTE: Here's a [CodePen for Geolocation](https://codepen.io/hipperger/pen/gQXMbx/) as well.

## Know Your Docs

- [ ] [MDN Docs - Geolocation API](https://developer.mozilla.org/en-US/docs/Web/API/Geolocation_API)

## Additional Resources

As always, there is no substitute for the [documentation](https://developer.mozilla.org/en-US/docs/Web/API/Geolocation_API); however,[here is an easy read](http://www.standardista.com/html5/introduction-to-geolocation/), which will give you a good feel for the structure and use of the Geolocation API within HTML5. Basically, you could copy/paste the code from that article into your js file, and get the coordinates of your location, or the location of a user who's using your page! Pretty cool, right?

  > NOTE ON VIDEO 1: This next video uses a special kind of programming that we haven't gotten to yet, called functional programming. The guy passes a function `showPosition` into a method called `navigator.geolocation.getCurrentPosition()`. Essentially, this passes whatever is returned from `.getCurrentPosition()` into `showPosition` and that data is held in the parameter named: `position`. Open up the repo above and try it yourself.

- [ ] [YT, Programming Wizard - HTML5 Geolocation API Tutorial](https://youtu.be/PnTiwcHM828)
  
  > NOTE ON VIDEO 2: This second video is a bit more advanced, and provides a lot more detail. Just follow along, and type exactly what you see for now. You will understand it better as you build more stuff.

- [ ] [YT, DoingITeasyChannel - JS Lesson 18: Geolocation API](https://youtu.be/pPAvL21kZQ0)