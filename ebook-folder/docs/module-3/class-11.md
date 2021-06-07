# Class 11: ToDo List

<!-- ! HIDE FROM STUDENT; INSTRUCTOR ONLY CONTENT -->
<!-- ## Instructor Only Content - HIDE FROM STUDENTS -->

<!-- ! END INSTRUCTOR ONLY CONTENT -->

*“He who has a why to live can bear almost any how.“ –Friedrich Nietzsche*

## Greet, Outline, and Objectify

<!-- SMART: Specific, Measurable, Attainable, Relevant, and Timely. -->
<!-- https://examples.yourdictionary.com/well-written-examples-of-learning-objectives.html -->

Today we're going to:
  
*OBJECTIVE: After this class students will have a firm understanding of:*

* *Using Fetch API to interact with APIs outside of the browser*
* *Read documentation and use APIs*
* *Loop over JavaScript arrays and create multiple items*

*****

- [ ] Questions for Student Led Discussion
- [ ] Interview Challenge
- [ ] Student Presentations
- [ ] Creation Time
    * [ ] Todo List - 80 mins
- [ ] Push Yourself Further
<!-- - [ ] Interview Questions: Blog to Show You Know -->
- [ ] Exit Recap, Attendance, and Reminders

### Questions for Student Led Discussion, 15 mins
<!-- This section should be structured with the 5E model: https://lesley.edu/article/empowering-students-the-5e-model-explained -->

[Questions to prompt discussion](./../additionalResources/questionsForDiscussion/qfd-class-11.md)

### Interview Challenge, 15 mins
<!-- The last two E happen here: elaborate and evaluate  -->
<!-- this sections should have a challenge that can be solved with the skills they've learned since their last class. -->
<!-- ! HIDDEN CONTENT: INSTRUCTOR ONLY -->
[See Your Challenge Here](./../additionalResources/interviewChallenges.md)
<!-- ! END HIDDEN CONTENT: INSTRUCTOR ONLY -->

### Student Presentations, 15 mins

[See Student Presentations List](./../additionalResources/studentPresentations.md)

## Creation Time, 60-90 mins

Today you're going to use the Fetch API on the browser to fetch data from the [JSON Placeholder API](https://jsonplaceholder.typicode.com/) which will provide you with **dummy data** to create a todo list which will get you ready for next class, where you'll be filtering those todos!!

- [ ] Create and clone a new repo with a `README` called: " `Dummy-Data-Todo-List` ".
- [ ] Go ahead and turn in your homework now *(if you're instructor creates the place for it. ;)*
- [ ] Create files for HTML and JavaScript. (You can add CSS later.)
- [ ] You'll start with some code like this:

=== "The JavaScript"
    ```javascript
        // We'll pre-populate this array with a couple objects just so it's not undefined if your internet connection isn't working properly.

    let arrayOfTodos = [
        {
        "userId": 14,
        "id": 1,
        "title": "delectus aut autem",
        "completed": false
    },
    {
        "userId": 20,
        "id": 2,
        "title": "delectus aut autem",
        "completed": false
    }]

    const fetchTodos = () => {
        fetch('https://jsonplaceholder.typicode.com/todos')
        .then( (response) => response.json())
        .then( (json) => arrayOfTodos = json)
    }

    const logTodos = () => {
        console.log(arrayOfTodos)
    }

    const populateTodos = () => {

    }
    ```

=== "The HTML"

    ```html
        <button onclick="fetchTodos()">Fetch Todos</button>
        <button onclick="logTodos()">Log Todos</button>
        <button onclick="populateTodos()">Populate Todos</button>
        <ol id="todo-list">
        <!-- LIs will go here -->
        </ol>
    ```

- [ ] Notice the `<ol></ol>` element. This is an [Ordered List](https://www.w3schools.com/html/html_lists.asp) that takes only `<li></li>` elements, or [List Items](https://www.w3schools.com/tags/tag_li.asp).

- [ ] Use the Ol element to insert new Li element for each todo in the `arrayOfTodos`.

- [ ] Notice to that each object comes inside **curly-braces**, `{ }`. This is called a JavaScript Object. You can access an object's **properties** with **dot-notation**. See the example below:

    ```javascript
        const arrayOfTodos1 = [
            {
            "userId": 14,
            "id": 1,
            "title": "delectus aut autem",
            "completed": false
        },
        {
            "userId": 20,
            "id": 2,
            "title": "delectus aut autem",
            "completed": false
        }
        ]

        console.log(arrayOfTodos[0].userId) // => 14
        console.log(arrayOfTodos[1].userId) // => 20
    ```

- [ ] After you've been able to access and console the properties on any object in the array your next step is to insert that data into an `li` element and insert the `li` into the `ol`.
- [ ] Start with getting just the **first** item and its `title` property.
    * [ ] Then capture the `ol` item into a variable (getElementById)
    * [ ] `createElement` to make a new LI
    * [ ] `createTextNode` inside the `li` using the `title` property.
    * [ ] Now append the text to the new element
    * [ ] Then append the element to the `ol` element.
    * [ ] Put all of that inside your `populateTodos` function.

- [ ] `git status`, `add`, `commit`, `push`
- [ ] Now that you have one element created and showing up on the screen, put the same code inside a `for` loop and iterate over the `length` of the array. But now just change out `[0]` for `[i]`! (Refer back to your for loop lesson if needed)
- [ ] Remember to `commit` often.

## Student Feedback

<iframe src="https://docs.google.com/forms/d/e/1FAIpQLScjuL10i2xFGMWRwkjtgAL8F1Y5ipMPPjtTCDzkO1ZBcxUYZA/viewform?embedded=true" width="640" height="500" frameborder="0" marginheight="0" marginwidth="0">Loading…</iframe>

## Exit Recap, Attendance, and Reminders, 5 mins

- [ ] Create JS-ToDo List Assignment
- [ ] Prepare for next class by completing all of your pre-class lessons
- [ ] Complete the feedback survey(if applicable)

<!-- <iframe id="openedx-zollege" src="https://openedx.zollege.com/feedback" style="width: 100%; height: 500px; border: 0">Browser not compatible.</iframe>
<script src="https://openedx.zollege.com/assets/index.js" type="application/javascript"></script> -->

<!-- TODO Create 3 question exit questions -->

<!-- TODO INSERT Student Feedback From -->

<!-- TODO INSERT *HIDDEN* Instructor Feedback Form -->
