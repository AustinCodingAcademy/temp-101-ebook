# Nested Arrays

*“Do one thing every day that scares you.”―Eleanor Roosevelt*

## Overview

Nested Arrays or **Multi-Dimensional** Arrays at first sound scary and crazy. But, rest assured, they are simple and very easy to use.

Remember how we learned that Array data types are really lists of other objects like Numbers, Strings, Functions, and yes, even other Arrays? When we have an array nested inside of another array we call them **Nested** or **Multi-Dimensional** Arrays.

```javascript
  const myArr = [
    [1, 2, 4, 88, 54, 91, 3],
    ["let", "live", "love", "leadership", "last", "lofty", "leader"],
    [personObj, personTalkFunc, addPersonFunc, removePersonFunc],
    [[3, 5, 6, 99], [100, 6, 4, 2], [77, 81, 9]]
  ]
```

The array, `myArr`, from the snippet above has 4 objects inside of it; the fact that each of those objects is an array makes it an array of 4 arrays. Do you see them? Each is separated by a comma, `,`.

If we logged each of these arrays to the console we'd see the following:

  * `myArr[0]` => `[1, 2, 4, 88, 54, 91, 3]`
  * `myArr[1]` => `["let", "live", "love", "leadership", "last", "lofty", "leader"]`
  * `myArr[2]` => `[personObj, personTalkFunc, addPersonFunc, removePersonFunc]`
  * `myArr[3]` => `[[3, 5, 6, 99], [100, 6, 4, 2], [77, 81, 9]]`

  > Do you see it?

The beauty of Multi-Dimensional Arrays is that we can continue stacking, or **chaining** bracket-notation on top of other brackets!! For example, if we wanted to access the first number in the first object of myArr we'd write: `myArr[0][0]` which would be `1`.

But if we wanted to access the first number of the first array of the last object in `myArr` we'd write `myArr[3][0][0]` which would be `3`; but if we just wrote `myArr[3][0]` would equal `[3, 5, 6, 99]`. See that?

To get to the word `"lofty"` in the second object of `myArr`: `myArr[1][5]`.

  > Are you catching on?

Below you'll see an example that relates directly to your Tic Tac Toe game in class but it's important to remember that these **Data Structures** are similar to the [data structures you'll see when you retrieve data from a database](http://dummy.restapiexample.com/api/v1/employees). Knowing how to access the data inside nested arrays is crucial to your future job!

<!-- ! Video Contents:  (width="655" height="368", ratio 1.77) -->

## Practice It

To complete the logic of your Tic Tac Toe game you'll need to know how to access Nested Arrays because the Data Structure we would use to represent a Tic Tac Toe board would be a Nested Array like:

```javascript
  let board = [
    ["", "", ""], // <-- Row 1, index 0
    ["", "", ""], // <-- Row 2, index 1
    ["", "", ""] // <-- Row 3, index 2
  ]
```

Where each index in the `board` array represents a *row* on the Tic Tac Toe board and each `""`, or index of the inner arrays, represents *column* on the Tic Tac Toe board.

[Try it yourself](https://replit.com). Go to the console in your browser and:

- [ ] Copy/paste the board example into it. Hit ++enter++.
    * [ ] Then run `board[0][0] = "X"`
    * [ ] Then run `board`. What do you see? It should be something like: "(3) [Array(3), Array(3),Array(3)]"
    * [ ] Click on the drop-down arrow to open the array. What changed?
    * [ ] Try it again but this time, change the position you want to change: `board[1][2]`, `board[2][1]`, etc.
    * [ ] Play and see what you can figure out.
    * [ ] Try `.push()`, `.pop()`, `shift` and `unshift`
- [ ] Go to [W3Schools to practice on these three Array Exercises](https://www.w3schools.com/js/exercise_js.asp?filename=exercise_js_arrays1)

<!-- [Try it yourself](https://replit.com)! -->
<!-- [Try it yourself](https://codepen.io)! -->