# Type Array

*“It is time for us all to stand and cheer for the doer, the achiever – the one who recognizes the challenges and does something about it.” –Vince Lombardi*

## Overview

Up to this point you've seen a couple types of data including **String** and **Number**. Just like we have different element types to work with in the DOM, in JavaScript we have different types of data to work with. Each comes with its own properties and methods available to adjust and call.

  > FYI: Last lesson we learned about the syntax of a **Function** but we didn't even mention that itself is a type of data(data type)!

Now we have three types of data: Number, String, and Function. In this lesson we'll add one more type of data, **Array**!

## What's An Array?

The words array and list are interchangeable. In fact, in other languages like C#, they are called lists instead of arrays. If this is true, we can think of the data type, **Array** as a way to group many items together in the form of a list. Let's say we're creating a todo list. We wouldn't want to create a new variable to hold each todo as String types:

```javascript
  // Inefficient way to hold a list of ToDos

  let todo1 = "wash the dog."
  let todo2 = "wash the car."
  let todo3 = "meditate."
  let todo4 = "learn to prepare a new healthy meal."
  let todo5 = "journal my thoughts."
```

Instead, we could hold a list of items like this in an array/list. Like so...

```javascript
  // A better way to hold a list of similar or related items

  let myTodos = ["wash the dog.", "wash the car.", "meditate.", "learn to prepare a new healthy meal.", "journal my thoughts."]
```

From the examples above you can deduce:

1. Arrays are created in a similar way as the Number, String, or Function types are created. We start by simply using the keyword const, then naming the array something like myTodos then assigning it a value with the = symbol.
1. Beyond that, we can see that an array's **syntax** includes a pair of square-brackets, [] and we separate our items with a comma, ,.

  > But what if we want to hold a list of numbers?

```javascript
  let aListOfNumbers = [8, 45, 71, 23, 75, 99, 103, 5, 61, 2]
```

  > What if we wanted to hold a list of Numbers and Strings?

```javascript
  let mixedList = [855, "Growth", 2630, 7, "Strength", "Positive Change", 1013, "Laughter"]
```

  > Great! We can put anything we like in an array as long as we use the proper syntax, but what can we do with an array that we can't do with a String or Number?

I'm glad you asked!

## What Does Indexed Mean?

You see, an Array is **indexed** which means every item in the array has a hidden number attached to it. These *hidden numbers* mark the place in the array the items sits. This means, that every place in the array is marked with a number that ascends from 0 up to the total number of items in the array.

From left to right, we can count the items in the array as 0, 1, 2, 3, 4, 5, 6, etc, until we reach the end of the array. This is useful because we can access those items just the same way we can access the properties on our HTML Elements! Check out the two code snippets below and see if you can figure out the connection.

```html
  <!-- HTML  -->
  <p id="parrot">Blue feathers.</p>

  <script>
    // JavaScript
    let ourElement = document.getElementById("parrot")
    let text = ourElement.innerHTML

    console.log(text) // => "Blue Feathers."
  </script>
```

In the example above we see some JavaScript inside the `<script>` element that holds the value of the `<p>` element in the variable named `ourElement`. Then we access its `innerHTML` property and hold it in the `text` variable. If we log `text` to the console we should see `"Blue Feathers."`.

In this same way, we can access the **items**/*properties* of an array by using its **indexes**: 0, 1, 2, 3 ... ∞. Below we see an example of JS code that creates an array and logs out a few of its items/properties.

```javascript
  let courage = [999, "wonderful", 100, 10, "challenge"]

  console.log(courage[0]) // => 999
  console.log(courage[1]) // => "wonderful"
  console.log(courage[4]) // => "challenge"
```

In the code snippet above you see a different syntax than what we've used before, [0]. This is called **bracket-notation**. It works the same as dot-notation except that it can accept numbers where dot-notation can only take letters/words that refer to a property name like `.innerHTML`.

  > To access the *hidden numbers*, **indexes**, we use bracket-notation. To access properties with names we know we use dot-notation. We'll use these indexes later when we write loops, as well!

### Practice It - Array Indexes

- [ ] In Chrome, open the inspector tool, then open the Console tab.( ++cmd+shift+c++ / ++ctrl+shift+c++ )
    * [ ] Inside that open space, you can type JavaScript. Go ahead and create an array called `phones` with 4 phone numbers as 4 different items. Type them as strings like this: `"512-888-0000"`.
    * [ ] Hit ++enter++.
    * [ ] Now `console.log` each of the phone number using bracket-notation: `phones[2]`, `phones[3]`,` phones[0]`, etc.

## First Two Array Methods

Again, just like each HTML Element has methods, or built-in functions, so do each of our JavaScript Data Types. Arrays have many many methods which makes them very useful and versatile. Today we'll cover two very essential methods: `.pop()` and `.push()`.

These two methods remove or add an item to the end of the array. So `phones.pop()` will remove the last phone number in the array you created in the **Practice It** section above.

On the contrary, `.push()` will add an item to the end of an array. If you wanted to add a number to your phones array you could write: `phones.push("214-991-0050")`. This would add `"214-991-0050"` to the end of the array.

**Try it yourself!**

- [ ] Go back to your Console tab (if you reloaded your window you'll need to create a new array called `phones`. See the **Practice It** section above for instructions)
- [ ] Write `phones.push("214-991-0050")` + ++enter++ .
- [ ] Now `console.log(phones)` + ++enter++. What do you see?
- [ ] Now `write phones.pop()` + ++enter++.
- [ ] Then `console.log(phones)` + ++enter++ again. What do you see?

These two methods are very useful! Let's say you're building a todo app *(like we'll be doing in a few days)* and you'd like to add an item to the list. You can use and `onclick` method to pass the `input`'s value to a function that `.push()`es to the todo list! When you've finished the todo, you could do the same technique but instead use `.pop()` to remove the last todo!

We'll stop for now on the methods of Arrays but we'll come back to the them soon because they are very useful **types of data**! In the next lesson we'll cover how to **loop** over an array while we cover Loops!!

## Practice It

Create a new repo or [CodePen](https://codepen.io) and paste the following code into the `index.html` file.

```html
  <!DOCTYPE html>
  <html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
  </head>
  <body>
    <article id="text-box"></article>
    <button onclick="addNewElement()">Click Me</button>

    <script>
      // Create an array called listOfWords
      const listOfWords = ["Beautiful", "Grand", "Brave", "Powerful"]
      // Create a variable to count the number of clicks
      let clicks = 0

      const addNewElement = () => {

        // Use the document method: .createElement() to create a <p> element
        const newParagraph = document.createElement("p")

        // Use the .createTextNode() method to create a text node with each of the words of the array
        // ON LINE 25 - Replace the "me" to Practice Bracket-Notation and make this function access each element one-at-a-time using the "clicks" as a value for the indexes of the array.
        const newText = document.createTextNode(me[me])

        // Then attach the text node to the new <p> element
        newParagraph.appendChild(newText)

        // Next, hold the value of the <article> element
        const myElement = document.getElementById("text-box")

        // Then add the new <p> element with the new text node inside it to the <article> element
        myElement.appendChild(newParagraph)

        // Each time this function runs add 1 to the value of clicks so we can iterate over the array
        clicks++

        return console.log(clicks)
      }
    </script>
  </body>
  </html>
```

- [ ] Read the comment lines to figure out what the code is supposed to be doing.

- [ ] Find the two bugs and fix them to make this web page work.
- [ ] **BONUS 1**: Create a new button, an input field, and a new function that will add words to the list of words.
- [ ] **BONUS 2**: Take this practice problem to you for loop practice and get the program to display the new words you add to the list.

## Know Your Docs

- [ ] [MDN Docs - Type Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)


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