# Coding vs Programming

## Overview

<!-- content-data="101-blogging" brand="circle" -->
<iframe src="https://player.vimeo.com/video/387535106" width="640" height="480" frameborder="0" allow="autoplay; fullscreen" allowfullscreen content-data="101-code-program" brand="circle"></iframe>

<!-- This is how each subject should be introduced. Give the students structure so they know they can start trusting the process sooner!  -->
While the words **"programming"** and **"coding"** may be used interchangeably by some, it is worth thinking about how they differ. Throughout this course we want you to consider both of these words. Think about how they are similar, how they are different, and above all how to be both an effective programmer and an effective coder.

### Read It

<!-- Give them our writing of the subject then link to a few articles: Medium, Wikipedia, CSS-Tricks, W3S, MozillaDev, etc... that help give more perspective on the subject  -->

For the sake of this class, I want you to think of **programming** as a method of figuring out the steps of a process (program)/problem-solving while **coding** is the process of communicating with your machine in a detailed, non-ambiguous way how to execute each step of the solution.

In this way, **programming** is a high-level, problem-solving process that involves using your logic, vision, hearing, past experience, visualization, and even touch to figure out solutions to problems. And **coding** is the implementation of the found solution.

As you'll see in the example below, we'll use programmatic thinking to identify the problem and list out each step a program will need to accomplish a task. **Coding**, on the other hand, is utilizing a specific language that a computer is capable of understanding to make it return an expected result.

With these two definitions in mind, does it begin to make sense how both a programming and coding approach come together to help us create solutions?

**Take the problem below for example:**

*Problem: "Build a program that when given a list of singular words makes them plural."*

Taking a programmatic approach, we would identify these steps:

1. Create a list of singular words
1. Go to each word
1. Add an 's' to the end
1. Collect each new plural word
1. Return the new list of the plural words

Alternatively, the *coding* steps, using JavaScript, would look like this:

```javascript
const singularWords = ['dog', 'god', 'tree', 'paper', 'problem']

const makePlural = (list) => {
  let newWordList = []

  for(word of list){
    const pluralWord = word.concat('s')
    newWordList.push(pluralWord)
  }

  return newWordList
}

makePlural(singularWords)
```

Obviously this is a simple example but it describes what you'll be doing in this intro course, throughout the rest of this program, and in your future career. First, you should look to identify the problem(s), think critically about the best way to solve the problem(s), *then* use code to teach the computer how to achieve your desired solution.

In this way it should be stated very strongly: **DO NOT RUSH INTO CODING!!**

Good Developers – even only decent developers – take the time to whiteboard, wireframe, code plan, and task **BEFORE** they ever start coding.

If there is one piece of advice you take from this section, it should be this: plan first.

## Additional Resources

* [YT, Ohto Rainio - What is Programming?](https://www.youtube.com/embed/3tWMQ3ZMjbg)
* [YT, TeXpliaNIt - What is Coding?](https://www.youtube.com/embed/N7ZmPYaXoic)
