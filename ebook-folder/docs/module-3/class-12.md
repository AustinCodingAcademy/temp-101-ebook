# Class 12: Filtering ToDo List

<!-- ! HIDE FROM STUDENT; INSTRUCTOR ONLY CONTENT -->
<!-- ## Instructor Only Content - HIDE FROM STUDENTS -->

<!-- ! END INSTRUCTOR ONLY CONTENT -->

*“When written in Chinese the word “crisis” is composed of two characters – one represents danger and the other represents opportunity. “ –John F. Kennedy*

## Greet, Outline, and Objectify

<!-- SMART: Specific, Measurable, Attainable, Relevant, and Timely. -->
<!-- https://examples.yourdictionary.com/well-written-examples-of-learning-objectives.html -->

Today we're going to:
  
*OBJECTIVE: After this class students will have a firm understanding of:*

* *Using callback functions*
* *Filtering Data*
* *Project Planning*

*****

- [ ] Final 101 Project Planning Discussion
- [ ] Questions for Student Led Discussion
- [ ] Interview Challenge
- [ ] Student Presentations
- [ ] Creation Time
    * [ ] Filter Dummy API ToDos
- [ ] Push Yourself Further
- [ ] Interview Questions: Blog to Show You Know
- [ ] Exit Recap, Attendance, and Reminders

### Final 101 Project Planning Discussion

As you saw in your homework, next week you'll begin work on your new Portfolio Website, before we get to that let's gave a quick talk about what this is:

- [ ] Why: you will need to have a very sharp portfolio to represent you out there in the job market and you're first site is likely not to be your best work.
- [ ] What? A responsive portfolio website that includes,
    * [ ] A Landing page
    * [ ] An About page
    * [ ] A Resume page
    * [ ] A Contact Me page
    * [ ] An image gallery, so to speak, that will serve as your Portfolio Page. It will have thumbnails of all the websites you've built and hosted up to this point, that when clicked they will take you to those websites.
    *  [ ] design for phone, tablet, and laptop
- [ ] How: Team work and planning. So let's partner up:
    * [ ] First based on similar work schedules
    * [ ] Secondly, based on similar ideas of their website....so
- [ ] Let's have students that are willing to show their ideas off.
- [ ] Spend a few minutes chatting to find a partner.
- [ ] RocketChat/Chat your instructor you and your partner's name (one per group is fine.)
- [ ] With that, let's move to Trello and continue our discussion on planning.

### Questions for Student Led Discussion, 15 mins
<!-- This section should be structured with the 5E model: https://lesley.edu/article/empowering-students-the-5e-model-explained -->

[Questions to prompt discussion](./../additionalResources/questionsForDiscussion/qfd-class-12.md)

### Interview Challenge, 15 mins
<!-- The last two E happen here: elaborate and evaluate  -->
<!-- this sections should have a challenge that can be solved with the skills they've learned since their last class. -->
<!-- ! HIDDEN CONTENT: INSTRUCTOR ONLY -->
[See Your Challenge Here](./../additionalResources/interviewChallenges.md)
<!-- ! END HIDDEN CONTENT: INSTRUCTOR ONLY -->

### Student Presentations, 15 mins

[See Student Presentations List](./../additionalResources/studentPresentations.md)

## Creation Time, 60-90 mins

We'll still be using the same JSON Placeholder API and the same `/todos` endpoint but this time you're going to only show/*filter* todos created by one user, i.e. in the 200 todos you fetch you'll see there are 10 different `userIds`. With the input of a number and the click of a button your todo list should only show the todos of a selected ``userId``.

### The Specifications/Specs

- [ ] Using the assignment from yesterday, create a branch called: " Todo-Filtering ".
- [ ] Fetch the same data.
- [ ] Store the data in a variable.
- [ ] Add an input for the `userID`. This input should only take in a number from `1 - 10`.
- [ ] Add a button that when clicked will:
    * [ ] clear the previous todos from the view
    * [ ] and populate it with only todos with the userID that matches the number inputted.
    * [ ] then stores the currently filtered todos in a variable so that ...
- [ ] You can create two more buttons that when clicked:
    * [ ] removes those todos from the view
    * [ ] and shows only todos that are either:
        - completed
        - not completed

    > HINT-1: When you're removing and repopulating, remember that you're removing them from the DOM and not the array. 

    > HINT-2: Take these tasks one at a time.

<!-- ! Video Content:  (width="655" height="368", ratio 1.77) -->

### Push Yourself Further

- [ ] Build another column for Complete todos.
- [ ] Sort the todos on just one click,
    * [ ] Show only the selected userID's todos
    * [ ] displays the Completed todos in one column
    * [ ] and the incomplete todos in another.

## Student Feedback

<iframe src="https://docs.google.com/forms/d/e/1FAIpQLScjuL10i2xFGMWRwkjtgAL8F1Y5ipMPPjtTCDzkO1ZBcxUYZA/viewform?embedded=true" width="640" height="500" frameborder="0" marginheight="0" marginwidth="0">Loading…</iframe>

## Blogs to Show You Know

[Blog Prompts](./../additionalResources/blogPrompts.md)

## Exit Recap, Attendance, and Reminders, 5 mins

- [ ] Create Filter Todos Assignment
- [ ] Create Class 12 Blog Assignment
- [ ] Prepare for next class by completing all of your pre-class lessons
- [ ] Complete the feedback survey(if applicable)

In the next two week, you'll have class time to work on your Portfolio Website Rebuild but it won't be enough time to complete it because we'll be learning new tricks that will spiff up your pages. Talk with your partner over the next few days so you have a good idea of what you'd like to start on first thing next week!

<!-- <iframe id="openedx-zollege" src="https://openedx.zollege.com/feedback" style="width: 100%; height: 500px; border: 0">Browser not compatible.</iframe>
<script src="https://openedx.zollege.com/assets/index.js" type="application/javascript"></script> -->

<!-- TODO Create 3 question exit questions -->

<!-- TODO INSERT Student Feedback From -->

<!-- TODO INSERT *HIDDEN* Instructor Feedback Form -->
