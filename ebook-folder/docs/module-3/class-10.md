# Class 10: TicTacToe

<!-- ! HIDE FROM STUDENT; INSTRUCTOR ONLY CONTENT -->
<!-- ## Instructor Only Content - HIDE FROM STUDENTS -->

<!-- ! END INSTRUCTOR ONLY CONTENT -->

*“There is no royal road to anything. One thing at a time, all things in succession. That which grows fast, withers as rapidly. That which grows slowly, endures.” –Josiah Gilbert Holland*

## Greet, Outline, and Objectify

<!-- SMART: Specific, Measurable, Attainable, Relevant, and Timely. -->
<!-- https://examples.yourdictionary.com/well-written-examples-of-learning-objectives.html -->

Today we're going to:
  
*OBJECTIVE: After this class students will have a firm understanding of:*

* *Multi-Dimensional Arrays*
* *Representational Data*
* *Conditional Programming*

*****

- [ ] Questions for Student Led Discussion
- [ ] Interview Challenge
- [ ] Student Presentations
- [ ] Creation Time
    * [ ] TTT Fun Time - 60 mins
- [ ] Interview Questions: Blog to Show You Know
- [ ] Exit Recap, Attendance, and Reminders

### Questions for Student Led Discussion, 15 mins
<!-- This section should be structured with the 5E model: https://lesley.edu/article/empowering-students-the-5e-model-explained -->

[Questions to prompt discussion](./../additionalResources/questionsForDiscussion/qfd-class-10.md)

### Interview Challenge, 15 mins
<!-- The last two E happen here: elaborate and evaluate  -->
<!-- this sections should have a challenge that can be solved with the skills they've learned since their last class. -->
<!-- ! HIDDEN CONTENT: INSTRUCTOR ONLY -->
[See Your Challenge Here](./../additionalResources/interviewChallenges.md)
<!-- ! END HIDDEN CONTENT: INSTRUCTOR ONLY -->

### Student Presentations, 15 mins

[See Student Presentations List](./../additionalResources/studentPresentations.md)

## Creation Time, 60-90 mins

### TicTacToe

Back in [Class 5](./../module-2/class-5.md) you built a simple [TicTacToe Game](https://github.com/AustinCodingAcademy/TicTacToe-101). If you remember, it didn't have logic that told who or when someone won. Today, let's have some fun playing with JavaScript and let's see if we can all learn how to think a little more programmatically!!

Before we begin, let's create a new branch on our TicTacToe-101 repo.

- [ ] Go find its directory.
- [ ] Make sure you're on the `master`/`main` branch.
- [ ] Use the proper command to create a new branch named `TTT-Logic` and switch to it.
- [ ] Once you've done that let's move ahead!

    > When you finish your TTT board you were able to add "X"s and "O"s as well as clear the board. But now we'll need to compare the data inside those boxes to a set of "rules" to know if there is a win. To do this we have two problems to overcome:

    1. We have to access the data.
    2. We have to know the rules.

    > Let's start with the rules. The "set of rules" might look something like this:

- [ ] Horizontal Win, a.k.a, If row 0 equals all "X"s or "O"s:

    ```javascript
        if((board[0][0] == "X" && board[0][1] == "X" && board[0][2] == "X") 
            || (board[0][0] == "O" && board[0][1] == "O" && board[0][2] == "O")
        )
    ```

    > This could be repeated for rows 1 and 2.

- [ ] Vertical Wins, a.k.a, if column 0 equals all "X"s or "O"s: 

    ```javascript
        if((board[0][0] == "X" && board[1][0] == "X" && board[2][0] == "X") 
            || (board[0][0] == "O" && board[1][0] == "O" && board[2][0] == "O")
        )
    ```

    > This could be repeated for the next two columns.

- [ ] Diagonal Wins, a.k.a, If there is a line created diagonally across the board with "X"s or with "O"s:

    ```javascript
        if((board[0][0] == "X" && board[1][1] == "X" && board[2][2] == "X") 
            || (board[0][0] == "O" && board[1][1] == "O" && board[2][2] == "O")
        )
    ```

    > This would be reversed for the opposite direction.

    > NOTE: You just saw new characters: `==`, `||` and `&&`. If you look at the docs on W3S about [Comparison Operators](https://www.w3schools.com/js/js_comparisons.asp) you'll see that `==` means "is-equal-to", `||` means "or" while `&&` means "and".

    > Now back to the first problem: Accessing the Data. We could use the `getElementById` method to access each box on the screen by it's `value` or `innerHTML` but this would be very expensive for computing power. So instead let's create a multi-dimensional array that can hold a **representational data structure** for our TTT board.

- [ ] Go to the top your `scripts.js` file and create an array called board with three arrays inside of it. Each of these inner arrays should have three places held with empty quotes: `""`, separated by commas, `,`.

    > If you look back up at those `if` statements you might be able to interpret that each one is checking to see what is inside each of the indexes of the arrays.

    > How do you create the representation of the data? In your `addMarker` function in `scripts.js` can you use the following code to set the value of each index in the board array to match what's on the screen? So in the end your `addMarker` function will insert an "X" or "O" in the DOM for the user to see as well as in the multi-dimensional array, board for your JavaScript to easily access.

- [ ] Inside `addMarker` add this line: `board[row][column] = currentMarker`

    > But how do you get the `row` and `column`?

- [ ] If you change the `ids` of each of the `<td>`s in the TTT board from `top-left` to say `0-0` & `middle-middle` to maybe `1-1`, etc... You could create `id`s that match their bracket-notation location in the board array. Then you could use the `parseInt` method to create numbers that you could use to access the arrays and indexes of board:

These variables hold the first and third letters in the element's id.

* `const row = parseInt(element.id.charAt(0))`
* `const column = parseInt(element.id.charAt(2))`

    > What's `charAt()` doing?

- [ ] But now you might have another problem, you're `onclick` might not work with your `addMarker` function because you've changed class names. If it's not, stop here and make sure you do get it working before moving on. Why isn't it working?

    > Now for the `checkForWin`. This bit will seem a little complicated at first but stay cool and breath.

- [ ] Copy/Paste the following code snippet into the bottom of your `scripts.js` file:


```javascript
   const checkForWin = () => {
     if(horizontalWin() || verticalWin() || diagonalWin()) {
       window.alert(`Player ${currentMarker} won!`)
     } else {
       changeMarker()
     }
   }

   const horizontalWin = () => {
     // Your code here to check for horizontal wins
   }

   const verticalWin = () => {
     // Your code here to check for vertical wins
   }

   const diagonalWin = () => {
     // Your code here to check for diagonal wins
   }
```

- [ ] Currently, at the end of your `addMarker` function you tell the computer to change the `currentMarker` from `"X"` to `"O"` or `"O"` to `"X"`. But you wouldn't want to do that if the game was won. So before telling the computer to change the `currentMarker` you would want it to first `checkForWin`.

    > The code snippet you copy/pasted has a function called `checkForWin` which you'll notice calls `changeMarker` if none of the winning rules(see above), are met.

- [ ] So inside `addMarker` you can replace the `changeMarker` call out for `checkForWin` because `changeMarker` will still be called if the other functions don't return `true`.

    > Now for the last part...

- [ ] Look back at the *rules* laid out above in those long `if` statements. Can you figure out how to write the if statements that will go inside `horizontalWin`, `verticalWin`, and `diagonalWin` using the **exact** code given to you in the rules and the code snippet? You'll have to expand upon these *rules* to make multiple `if/if else/else` statements for each to work.

**HAVE FUN and DON'T STRESS if you don't figure it out yet.**

<!-- ! Video Content:  (width="655" height="368", ratio 1.77) -->

### Follow Up

- [ ] Can a group show their code off to the class?
- [ ] Can one of the groups walk us through how this app works?

## Student Feedback

<iframe src="https://docs.google.com/forms/d/e/1FAIpQLScjuL10i2xFGMWRwkjtgAL8F1Y5ipMPPjtTCDzkO1ZBcxUYZA/viewform?embedded=true" width="640" height="500" frameborder="0" marginheight="0" marginwidth="0">Loading…</iframe>

## Blogs to Show You Know

[Blog Prompts](./../additionalResources/blogPrompts.md)

## Exit Recap, Attendance, and Reminders, 5 mins

- [ ] Create TTT-Logic Assignment
- [ ] Create Class 10 Blog Assignment
- [ ] Prepare for next class by completing all of your pre-class lessons
- [ ] Complete the feedback survey(if applicable)
- [ ] You've been working on your Barbershop Capstone Projects for a week now but if you have a little bit of time you should jump back on it! It's due this Sunday!

Next week we'll take our JavaScript skills to a whole new level when we start fetching data and rendering it on our web pages!!!

<!-- <iframe id="openedx-zollege" src="https://openedx.zollege.com/feedback" style="width: 100%; height: 500px; border: 0">Browser not compatible.</iframe>
<script src="https://openedx.zollege.com/assets/index.js" type="application/javascript"></script> -->

<!-- TODO Create 3 question exit questions -->

<!-- TODO INSERT Student Feedback From -->

<!-- TODO INSERT *HIDDEN* Instructor Feedback Form -->
