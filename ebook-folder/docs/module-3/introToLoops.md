# Intro To Loops

*“Press on – nothing can take the place of persistence. Talent will not; nothing is more common than unsuccessful men with talent. Genius will not; unrewarded genius is almost a proverb. Education will not; the world is full of educated derelicts. Perseverance and determination alone are omnipotent.” –Calvin Coolidge*

## Overview

By now you've probably understood that we write/build functions as sets of instructions that sit in storage until the computer needs to use/execute them. These sets of instructions are very useful because we can ** our web pages to do specific actions when a user interact with it. And so far, we've built simple actions, however, if we want to build more complex sets of instructions we'll need to learn why and how to use **.

Loo**ps are just like what they sound like. Under certain conditions, the tasks detailed inside the set of instruction should loop until the conditions have changed.

### What's a Condition?

A condition is a certain **state**; as in the current *state* or *status* of something.

If you arrive at an intersection and the light is red then the condition is `light = "red"`. But if you arrive at the intersection and the light is green then the condition is `light = "green"`. Based on these two different *states* we could tell the program to do certain things. Let's pretend we're programming an driverless car! We might be able to write a conditional statement that looks like this:

```javascript
  const checkLight = () => {
    if (light = "green") {
      accelerate()
    } else if (light = "red") {
      stop()
    } else {
      slowDown()
    }
  }

  checkLight()
```

In the code snippet above, we see a simple JS function that does one of three things based on a certain condition, the color of the `light`! We are getting a little ahead of ourselves right now because today we're going to cover two different loops: `while()` and `for()`. These do loops are commonly used in programming. But to use either of these loops you'll need to have a basic understanding of **conditional statements**. Now that you do, let's get to it.

### While Loop

Remembering what you just learned about conditions, look at the code snippet below and see if you can figure out how this built-in functions works.

```javascript
  let light = "red"

  while (light === "red") {
    holdBrake()
  }
```

A while loop is function built-in to the JavaScript language that will execute its **Action Statement** as long as its **Conditional Statement** evaluates to true. In the code above, as long as the light is red the car should *holdBrake()*. If the light should change the car will cease *holdBrake()*.

Explore the example below.

```javascript
  const countOneToHundred = () => {
    let counter = 1
    while (counter <= 100) {
      console.log(counter)
      counter++
    }
  }

  countOneToHundred()
```

Stop an ask yourself:

- [ ] What does the condition statement say?
- [ ] What is the line `counter++` doing?
- [ ] Throw this into your Console Tab and try it out yourself!
- [ ] You'll use this loop in the next class. Make sure to spend sometime learning this for yourself.


### For Loop

Last lesson we learned about Arrays and why they're really useful. To add to their utility, let's now learn how to use their **indexes** to **Loop/iterate** over arrays. To **loop** or **iterate** means that we ask the computer to traverse each item in the array so we can do something with each item.

<!-- ! Video Contents: 211 - Arrays and Loop (width="655" height="368", ratio 1.77) -->
<iframe src="https://player.vimeo.com/video/385377379" width="655" height="368" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen></iframe>

Like the **while** loop, a **for loop** repeats an actions over and over until a specified condition evaluates to false; the difference is that it's meant specifically for an array. What that means is that we tell the for loop how long an array is and what actions to do until we've looped over each item in the array/its traversed the length of the array.

First things first:

1. A `for()` loop is a built-in function that takes in arguments like any other function.
2. The arguments of the `for()` loop function are always in 3 and always go in this order:

    ```javascript
      for ([initialExpression]; [condition]; [incrementExpression]) {
        action statement
      }
    ```

    `Initial Expression`
: declares an iterator variable that will hold a number.

    `Condition`
: when the iterator meets this specific value the loop will stop.

    `Increment Expression`
: Tells how much the iterator number should increase or decrease.

    `Action Statement`
:is where we detail a set of instructions to do on every loop.

Look at the syntax below:

```javascript
  const arrOfNums = [2, 33, 4, 54, 13, 8, 79]

  for (let i = 0; i < arrOfNums.length; i++) {
    console.log(arrOfNums[i])
  }
```

From the code above we can see that an array is created that hold a handful of numbers. Then, a for loop is given three argument:

  * `let i = 0;` creates a variable called `i` and sets it to `0`
  * `i < arrOfNums.length - 1;` creates a condition for the loop to stop when its met.
  * `i++` continually adds 1 to the value of `i`

  > BUT WAIT!! We just saw some code we've never seen: `.length`! True, this a property on arrays and string data types. We can access this value and use as we like... in this case, to evaluate when our loop should stop. Just like HTML elements have properties like `color`, `border`, and `padding`, so too do Arrays, Strings, and Numbers!!

  > Everything is an object and every object has properties and methods!

Check out the code below. [Run it yourself](https://replit.com):

```javascript
  let alphabet = [ 'a','b','c','d','e','f','g','h','i','j','k','l','m','n','o','p','q','r','s','t','u','v','w','x','y','z' ]
  let digits = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

  const logCharacters = (arr) => {
    for (i = 0;  i < arr.length; i++){
      console.log("current character is " + arr[i]);
    }
  }

  logCharacters(alphabet)
  logCharacters(digits)
```

In the code snippet above, the `for` loops states:

1. Read the `for()` line. What is it saying?
1. Where is `arr` coming from?
1. How does `arr` allow us to call the function with two different arrays passed to it?

## Practice It

<!-- [Try it yourself](https://replit.com)! -->
<!-- [Try it yourself](https://codepen.io)! -->

For each of these you can write them in a new `.js` file and run them with live-server or use [Repl.it](https://replit.com); as long as you use `console.log()` to see the results in the Console Tab.

- [ ] Create a while loop to print out numbers from 1 - 10.
- [ ] Create an array and a for loop that will iterate over it backwards.
- [ ] Create a while loop to prints out every multiple of 3 up to 100.

## Additional Resources

- [ ] [YT, whatsdev - While Loops](https://www.youtube.com/embed/eQS9C_ZxKt0?start=12)
<!-- - [ ] [YT, tuber - title]() -->

## Know Your Docs

- [ ] [MDN Docs - While Loop](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/while)
- [ ] [MDN Docs - For Loop](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for)
- [ ] [MDN Docs - Conditional Statement](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/if...else)


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