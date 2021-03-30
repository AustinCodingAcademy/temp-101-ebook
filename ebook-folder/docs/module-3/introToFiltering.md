# Intro To Sorting

*”Fall seven times, stand up eight.” –Japanese Proverb*

## Overview

Let's start with a code snippet:

```javascript
const words = ['ray', 'limitless', 'elite', 'exuberant', 'devotion', 'presence', 'great'];

const result = words.filter((word) => word.length > 6);
```

Above we see an array is created called words, that has multiple strings in it. Then we see a variable called `results` that is pointing to the value of `words` with the .`filter()` method called on it.

`.filter` is another method on array *object-things* and it takes a special argument: a **callback function**

  > WAIT! Before you get hung up on trying to figure out what that means, do you remember when we saw an **anonymous function** passed into a `.then()` method while learning `fetch()`? Well...that too was a **callback function**. In both cases, the code snippet above and the `.then()` use an anonymous **callback function**.

  * An **Anonymous Function** is a function that doesn't have a name and can be passed into another function, or method.
  * A **callback Function** is a function placed into another function, or method, that will be called multiple times. It can only be used in methods or functions that use a callback functions like `.filter()`

So, reading the code again,

```javascript
  const result = words.filter((word) => word.length > 6);
```

We can expect whatever is returned from `.filter()` will be saved into the value of `result`. From the [docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter), we can also know that `.filter()` returns an array so results will be an array of something.

What will this *something* be?

For that we can look at what is passed into this anonymous function that will be called back, which is:

```javascript
  word => word.length > 6

  // or in long-hand
  (word) => { word.length > 6 }
```

The word `word` is not unique. We could have just as easily named it `greta`, so long as the next part was `greta.length > 6`. `word` is just holding the value of each value in the array: `words`.

Now we know that `.filter()` loops over an array and applies what is inside of its callback function. Which in this case is `word.length > 6`. This means that all words that have more than six letters will be added to the new array, `results`.

From all of this we find that `.filter()` creates a filter for large sets of data in an array!

```javascript
  const words = ['ray', 'limitless', 'elite', 'exuberant', 'devotion', 'presence', 'great'];

  const result = words.filter(word => word.length > 6);

  console.log(result);
  // Try it yourself, paste this into your browser's console, repl.it, or in a new repo and let it fly
```

Now that you know how JavaScript's `.filter()` works you can apply it to your todo application!!

<!-- ! Video Contents:  (width="655" height="368", ratio 1.77) -->

<!-- ## Practice It -->

<!-- [Try it yourself](https://replit.com)! -->
<!-- [Try it yourself](https://codepen.io)! -->

## Additional Resources

- [ ] [YT, Programming with Mosh - JavaScript Array Filter](https://youtu.be/4_iT6EGkQfk)

## Know Your Docs

There's more to filter including two other argument that filter's callback takes so make sure you checkout the docs.

- [ ] [MDN Docs - Array.filter()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter)


<!-- ! END OF VIDEO 101.1.3.1 - TITLE-->
<!-- ? Video Numbering and Title system: CourseNumber.ModuleNumber.LessonNumber.VideoNumber -->
<!-- * (VIDEO 101.2.4.3 - "CSS Selectors") === 101 Course, Module 2, Lesson 4, Video 3 - "CSS Selectors" -->

<!-- 

cp workspace/resources/templateFile.md docs/module- 


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