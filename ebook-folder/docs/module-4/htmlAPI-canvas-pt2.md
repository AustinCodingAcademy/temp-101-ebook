# The Canvas API, pt.2: Animating the Canvas

## Overview

Before we dive into animating and interacting with our Canvas drawings let restate that this is NOT a skill you MUST have to finish your 101 Portfolio Project or to be a junior developer. This skill is being provided to you to give you more tools, start learning to program, and seeing visuals on the screen with your JavaScript code.

That said, canvas and animations are SUPER cool so I'd suggest you do spend some time building with this and exploring on your own later.

## Animating Drawings on the Canvas

During part 1 of this Canvas lesson you learned how to draw shapes and even to programmatically draw many circles using a `for()` loop. To animate those same circles it's best to think about the over arching goal: create the illusion of movement!

To create the illusion of movement we'll be, in essence, drawing a circle in one origin, refreshing the page, then drawing the same circle a few pixels away, then repeating. To do this, we'll build a function that will call itself, again and again. *(This type of programming is called **recursion**. We'll dig into this concept in your 200 Level course.)* Once we get one direction of the circle going then we'll get the other direction moving. And each time we do that we'll create a new variable that holds the values of direction and velocity. Ready?

### Creating the Recursive Animate Function

As usual, fork and clone this [101-canvas-practice-pt2](https://github.com/AustinCodingAcademy/101-canvas-practice-pt2.git) repo to get going.

- [ ] We have the basics code to draw a circle on our canvas:

  ```javascript
    // JS for Drawing a Circle
    // define the canvas
    let canvas = document.getElementById("my-canvas")
    canvas.width = window.innerWidth;
    canvas.height = window.innerHeight;

    // hold the 2D drawing context in a global variable
    const c = canvas.getContext('2d')

    // draw the circle
    c.beginPath();
    c.strokeStyle = "limegreen";
    c.arc(600, 250, 50, 0, 2 * Math.PI);
    c.stroke();
  ```

- [ ] Now let's build a function that will do that same instructions over and over.

  ```javascript
    // JS for Drawing a Circle with a Function
    const animate = () => {
      c.beginPath();
      c.strokeStyle = "limegreen";
      c.arc(600, 250, 50, 0, 2 * Math.PI);
      c.stroke();
    }
  ```

But that function, even if called, will only run once. So inside that function we'll use a method on the Window *object-thing* that will refresh the page to redraw something new on the canvas called [`requestAnimationFrame()`](https://developer.mozilla.org/en-US/docs/Web/API/window/requestAnimationFrame). This method is special because it gets called **60 times/second** and will automatically stop if the user switches tabs. It's also only focusing on the Canvas so it's pretty efficient. This is what it looks like:

- [ ] `requestAnimationFrame()`

```javascript
  // JS for Drawing a Circle with a Recursive Function
  const animate = () => {
    // use this special Window method to refresh the Window and call `animate` again, and again, and again...
    requestAnimationFrame(animate)
    c.beginPath();
    c.strokeStyle = "limegreen";
    c.arc(600, 250, 50, 0, 2 * Math.PI);
    c.stroke();
  }
```

  > *Notice the argument passed into the `requestAnimationFrame` method? It's `animate`, the parent function! This is recursion. A child function will call it's parent which then calls the child, which then calls the parent, which then calls the child...........you get it.*

  > *Notice, too, that we didn't have to use empty-parenthesis `()` to invoke `animate`. This is because the argument `requestAnimationFrame` is expecting is a **callback function** or a function that is to be called again and again.*

- [ ] So now we'll need to call/invoke the function:

  ```javascript
    // JS for Drawing a Circle with a Recursive Function 
    const animate = () => {
      requestAnimationFrame(animate)
      // Draw Circle Code here....
      // .....

      // add a log statement to see the number and rate of calls.
      console.log("animate function was called...")
    }

    animate()
  ```

### Moving the X-Coordinate

Sweet! Now if we run that code in our browser with Live-Server we'll see the circle getting thicker and thicker but not moving/animating. That's a problem. How do we solve it? With some quick programming, of course!

- [ ] Let's change the **hard-coded** x-coordinate value of `600` to be a variable that we can change:

  ```javascript
    // create a variable to hold this value
    let x = 600;

    const animate = () => {
      requestAnimationFrame(animate)
      c.beginPath();
      c.strokeStyle = "limegreen";
      // replace the x-coordinate with the variable `x`
      c.arc(x, 250, 50, 0, 2 * Math.PI);
      c.stroke();
    }
  ```

If you run that code it doesn't change much, so let's make the x value change each time the animate function is run. We could add `x = Math.random() * (window.innerWidth - 100)` at the top of the `animate` function but that would just draw a new circle at different points along the `250` y-coordinate. 

- [ ] Instead let's increment from the origin of `x = 600`.

```javascript
  // JS for Increasing the X-Coordinate by 1 each time the Animate function is called.
  let x = 600;

  const animate = () => {
    requestAnimationFrame(animate)
    c.beginPath();
    c.strokeStyle = "limegreen";
    c.arc(x, 250, 50, 0, 2 * Math.PI);
    c.stroke();

    // increment the value of x by 1 each time the function is called
    x += 1
  }
```

### Clear the First Drawing

Now our circle is re-created on top of it's self, *1 pixel to the right*. But that's not animation. We want the circle to appear to move. To do that we'll need need to "erase" the previous circle before we draw the next one. We can use a method on the `getContext('2d')` object-thing called `.clearRect()`. To use it we can access the `getContext('2d') `by calling `c` *(Since we saved the `getContext` in a variable called `c` at the top of our file) then use dot-notation to get `c.clearRect()`*.

 - [ ] The `.clearRect()` method takes 4 arguments: ([start-X], [start-Y], [end-X], [end-Y]) where we'd want to say, "Hey, `.clearRect()`, I want you to clear every thing from the last drawing between the top-left of the screen, `(0,0` down to the farthest bottom-right of the screen: `,innerWidth, innerHeight)`." That in code would look like this:

  ```javascript
    // JS for Clearing the Canvas from Top-Left to Bottom-Right
    // more code....
      requestAnimationFrame(animate)
      // add the clear rectangle before we draw a new one
      c.clearRect(0, 0, innerWidth, innerHeight)
      c.beginPath();
      c.strokeStyle = "limegreen";
      c.arc(x, 250, 50, 0, 2 * Math.PI);
      c.stroke();

      x += 1

    // more code here too...
  ```

#### Changing the Speed and Direction

- [ ] Now we can change the speed of the movement of the circle, or velocity! 

To do this we'll go ahead and create a new variable because, *yes*, we could just change `x += 1` to `x += 4` but we'll want to randomize the velocity at a later point so we might as well throw it into another variable now:

  ```javascript
    // JS for Creating a Velocity Variable
    let x = 600;
    // hold the velocity in a new variable
    let xVelocity = 4;

    const animate = () => {
      // more code here...

      // now `x` will increment by whatever `xVelocity` is
      x += xVelocity
  ```

If you haven't already, go ahead and run that code to see the circle speed up.

Our next problem is that the circle is running off the side of the screen. To fix that all we have to do is us a **Conditional Statement** to say:

- [ ] *"If the x-value becomes higher than the entire window's inner width then reverse the change of new x-coordinate to decrement instead."*:

  ```javascript
    // JS for Changing the X-Coordinate if it's Higher than the Width of the Window
    let x = 600;
    let xVelocity = 4;

    const animate = () => {
      requestAnimationFrame(animate)
      c.clearRect(0, 0, innerWidth, innerHeight)
      c.beginPath();
      c.strokeStyle = "limegreen";
      c.arc(x, 250, 50, 0, 2 * Math.PI);
      c.stroke();

      // Conditional, if x is greater than innerWidth
      if(x > innerWidth) {
        // reverse the value to a negative number
        xVelocity = -xVelocity
      }

      // x will still plus-equal xVelocity
      x += xVelocity
    }
  ```

If you run that new code you'll see that the circle now bumps off the right side when the **CENTER** of the circle gets to the edge and it still goes off the screen on the left. 

- [ ] Let's tell the `animate` function to "Reverse the direction when the **EDGE** of the circle meets the edge of the screen by using the `radius` of the circle **AND** to go the opposite direction when it meets the left-side of the screen.

```javascript
  // JS for "Bouncing" at Edge of Circle & Reversing To Positive At Left-Side of Screen
  let x = 600;
  let xVelocity = 4;
  // Move our circle's radius to a variable we can use in other places
  let radius = 50;

  const animate = () => {
    requestAnimationFrame(animate)
    c.clearRect(0, 0, innerWidth, innerHeight)
    c.beginPath();
    c.strokeStyle = "limegreen";
    // replace the radius value with the variable `radius`
    c.arc(x, 250, radius, 0, 2 * Math.PI);
    c.stroke();

    // Add the "Or condition", `||`, that if the circle's left-side meets the left-side of the screen then add a negative to the already negative velocity to make a positive again.
    if(x + radius > innerWidth || x - radius < 0) {
      xVelocity = -xVelocity
    }

    x += xVelocity
  }
```

## Practice It

At this point you know how to move the x-coordinate now it's time for you to show what you know. Repeat these steps for the y-coordinate so you can have a circle that "bounces" of the top, bottom, and sides of the screen.

You'll need to:

- [ ] Create a variables to hold the `y` coordinate, `yVelocity`.
- [ ] Replace the uses of those values wherever they're used.
- [ ] Change the `y` with the `yVelocity`.
- [ ] Create another conditional statement to change those values.

## Additional Resources

- [ ] [YT, Chris Courses - Animating the Canvas, Ep. 3](https://youtu.be/yq2au9EfeRQ)

## Know Your Docs

- [ ] [MDN Docs - requestAnimationFrame()](https://developer.mozilla.org/en-US/docs/Web/API/window/requestAnimationFrame)
- [ ] [MDN Docs - .clearRect](https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/clearRect)
