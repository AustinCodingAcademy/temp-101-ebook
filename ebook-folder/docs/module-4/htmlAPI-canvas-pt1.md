# Canvas, an HTML API, Part One

*“A question that sometimes drives me hazy: am I or are the others crazy?” ―Albert Einstein*

## Overview

Continuing on with these "Quick Tip" types of lessons, let's learn how to build moving backgrounds with the the `canvas` HTML element!

Again, these section of the course is not only intended to give you new tools to work with but also to provide you with context on finding new tools and learning new techniques using your own curiosity. With that said, this lesson is going to follow along with [Chris Courses](https://www.youtube.com/channel/UC9Yp2yz6-pwhQuPlIDV_mjA) a YouTuber that puts together some insanely clear videos. Let's go!

## Creating and Resizing a Canvas

To start let's either create a new repo or clone the [101-canvas-practice repo](https://github.com/AustinCodingAcademy/101-canvas-practice).

Then let's create three files: `index.html`, `canvas-style.css`, and `canvas.js`.

Then build our HTML file and link the other two files to it.

Next create an empty canvas element inside the body with an `id: "my-canvas"`: `<canvas id="my-canvas"></canvas>`

Go to your JS file and save the canvas element in a variable called canvas:

```javascript
  // canvas.js
  let canvas = document.getElementById("my-canvas")

  // console to make sure we captured the element in the variable
  console.log(canvas)
```

Now, we can resize the canvas with JS to equal the height of the whole screen:

```javascript
  canvas.width = window.innerWidth;
  canvas.height = window.innerHeight;
```

Let's now remove the margin around the `body` element so it truly takes up the whole screen:

```css
  /* canvas-style.css */
  body {
    margin: 0;
  }

  canvas {
    background: grey;
  }
```

- [ ] Test it. Open it up in your browser to make sure you have a fully grey screen.

- [ ] Before we can draw we have to capture the drawing context within the canvas element. `.getContext()` is a method built on every canvas element, and yes, we can call it every time we want to use it but that would be a lot of typing on our part and an inefficient use of memory for the computer. So instead let's capture what this method returns in a variable we'll call `c`!

  > NOTE: Paste these code snippets into your repo and run the code in the browser.

```javascript
  // canvas.js
  const c = canvas.getContext('2d')
```

Now let's draw. The object-thing the `.getContext()` method returns has multiple properties like: `.ellipse()`, `.lineTo()`, `.createPattern()`, etc. The first method we'll use is .fillRect() a method that draws and fills in a rectangle shape on the canvas. It requires 4 arguments to know where to begin the top-left corner and how wide and tall the shape should be: `.fillRect(x, y, width, height)`.

```javascript
  // canvas.js
  c.fillRect(75, 75, 100, 100)
```

  > NOTE: You can find [all of the methods on the 2D Canvas Drawing Context at MDN](https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/fillRect).

- [ ] To see ALL of the properties and methods on the object returned by `.getContext('2d')` just `console.log(c)` and check it out in your console!

- [ ] Notice how the rectangle is black? That's because the property: `fillStyle` is defaulted to `#000000` or black. Let's change that by adding these two lines below:

```javascript
  // canvas.js
  c.fillStyle = 'red';
  c.fillRect(125, 125, 200, 40)
```

Your turn. Move the red rectangle to the right so it isn't over lapping with the black one.

- [ ] Change colors again and draw a new rectangle of any size just to the right of your red rectangle.
- [ ] Change the color and draw another just below the black rectangle.

More can be found at [HTML5 Canvas Tutorial - Ep.1](https://www.youtube.com/watch?v=EO6OkltgudE)

## Drawing on the Canvas

Now that we can draw and change the color or rectangles let see some of the other methods that can be drawn including: Lines, Arcs & Circles, Bezier Curves, Images, and Text.

Let's start with Lines:

The first thing we have to do is invoke a method called: `.beginPath()`. This simply tells the canvas element to get ready for a line to be drawn:

```javascript
  // canvas.js
  c.beginPath();
```

Now we have to tell the canvas where to begin and end the line. The start the line we use the method: `.moveTo()` as in, "Canvas, move your pencil to the place I tell you. .`moveTo()` takes to arguments: `.moveTo(x, y)`

```javascript
  // canvas.js
  c.beginPath();
  c.moveTo(20, 100)
```

After we've told the canvas where to begin we have to tell it where to go using the method `.lineTo()` as in, "Draw a line to `x` and `y` coordinates."

```javascript
  // canvas.js
  c.beginPath();
  c.moveTo(20, 100)
  c.lineTo(1000, 500)
```

But still nothing shows up! That's because canvas gives you control as to not only what will be draw but when. This "when" portion comes with the method: `.stroke()` as if to say, "Ok, draw it!"

```javascript
  // canvas.js
  c.beginPath();
  c.moveTo(20, 100)
  c.lineTo(1000, 500)
  c.stroke()
```

You can continue drawing the line from there by giving another instruction before the `.stroke()` method **OR** adding another `.stroke()` method after it:

```javascript
  // canvas.js
  // . . . continued on
  c.lineTo(1500, 200)
  c.stroke()
```

- [ ] You can also change the color of the line the same way you did with the rectangle but with: `c.strokeStyle= "pink"`.

  > NOTE: *For the rest of this section it might be good for you to follow along with with video below starting at 7:10*.

- [ ] To draw arc and circle we use the same techniques but, obviously, a different method: `.arc()`. This method takes multiple arguments with two that will be a little mathy but I think you can figure it out. They go in this order:

`.arc(x, y, radius, startAngle, endAngle [, anticlockwise] )`

- [ ] You know what `x` and `y` are for and can guess what rad`ius is for but let's look quickly at those last three:

  * `startAngle` - angle at which the arc starts in radians, measured from the positive x-axis.
  * `endAngle` - angle at which the arc ends in radians, measured from the positive x-axis.
  * `anticlockwise` - This is an optional argument that will either be `true` draw anti-clockwise or `false`(draw clockwise).

- [ ] To use this try starting with the following code:

```javascript
  // canvas.js
  c.beginPath();
  c.strokeStyle = "hotpink";
  c.arc(600, 250, 50, 0, 2 * Math.PI);
  c.stroke();
```

  > NOTE: If you're curious how to draw arcs checkout [the Arc docs at MDN](https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/arc).

Let's go ahead and program the canvas to draw 50 different circles in different places with a few different colors. We'll start with a for loop, which you've learned about already!!


```javascript
  // canvas.js
  for(let i=0; i < 50; i++ ) {

  }
```

Inside the for loop let's create two random coordinate each time the loop runs:

```javascript
  // canvas.js
  for(let i=0; i < 50; i++ ) {
    const x = Math.random() * (window.innerWidth - 100)
    const y = Math.random() * (window.innerHeight - 100)
  }
```

Then we can use those random coordinates to start a new circle:

```javascript
  // canvas.js
  for(let i=0; i < 50; i++ ) {
    const x = Math.random() * (window.innerWidth - 100)
    const y = Math.random() * (window.innerHeight - 100)

    // Draw Circle
    c.beginPath();
    c.strokeStyle = "black";
    c.arc(x, y, 50, 0, 2 * Math.PI);
    c.stroke();
  }
```

Next we can create a list of colors to randomly selected from:

```javascript
  // canvas.jss
  for(let i=0; i < 50; i++ ) {
    const x = Math.random() * (window.innerWidth - 100)
    const y = Math.random() * (window.innerHeight - 100)
    // the first value will be null to accommodate for no 0 number being drawn
    const colors = [null, "#8C0C3C", "#1B2968", "#4B9C2B", "#A4C89C", "#F8605F", "#F8B493", "#32B9B2", "#F85532", "#C2C8E4", "#357153", "#A061D4", "#404462"]

    // Draw Circle
    c.beginPath();
    c.strokeStyle = "black";
    c.arc(x, y, 50, 0, 2 * Math.PI);
    c.stroke();
   }
```

Now we need to generate a random number to use to select a color from the list and replace "black" with this random number:

```javascript
  // canvas.js
  for(let i=0; i < 50; i++ ) {
    const x = Math.random() * (window.innerWidth - 100)
    const y = Math.random() * (window.innerHeight - 100)
    // the first value will be null to accommodate for no 0 number being drawn
    const colors = [null, "#8C0C3C", "#1B2968", "#4B9C2B", "#A4C89C", "#F8605F", "#F8B493", "#32B9B2", "#F85532", "#C2C8E4", "#357153", "#A061D4", "#404462"]
    const randomIndex = Math.floor(Math.random() * (13 - 1)) + 1;

    // Draw Circle
    c.beginPath();
    // replace "black" with the random color selected from the list
    c.strokeStyle = colors[randomIndex];
    c.arc(x, y, 50, 0, 2 * Math.PI);
    c.stroke();
  }
```

- [ ] Go ahead and run it. Refresh. Refresh. Refresh. Refresh. Like it?

- [ ] Try it yourself. Create a variable that can [randomly generate](https://www.w3schools.com/js/js_random.asp) a new size for the circle!

- [ ] Now try using the `window.onclick` event to run this for loop each time the user clicks on the screen!

More can be found at [HTML5 Canvas Tutorial - Ep.2](https://www.youtube.com/watch?v=83L6B13ixQ0).

## Additional Resources

- [ ] [YT, Chris Course - HTML5 Canvas Tutorial - Ep.1](https://www.youtube.com/watch?v=EO6OkltgudE)
- [ ] [YT, Chris Course - HTML5 Canvas Tutorial - Ep.2](https://www.youtube.com/watch?v=83L6B13ixQ0)

## Know Your Docs

- [ ] [MDN Docs - Canvas API](https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/canvas)
- [ ] [W3S Docs - Canvas API](https://www.w3schools.com/html/html5_canvas.asp)
- [ ] [CodePen - Canvas Demo](https://codepen.io/austincoding/pen/ZyeXJq/)
