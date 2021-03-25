# Document Methods

With all this talk of the Window, Buttons, and Input Elements it feels as if we kicked the Document object to the curb. "It has feelings too, guys!"

Check it, the document has access to all elements because it is the **root** element. It is the Mother of All Elements, it creates elements, removes elements, and changes their contents. The Document is THE OBJECT. It's why we call there is a **Document Object Model**, because all objects are born, live, and die with the Document object.

To begin learning the powers of this omnipotent goddess let's create yet another button we can call a function with. Go ahead and do this by yourself. You got this, just create a new button with "Create New Object" as its innerText. Then give the `onclick=` attribute the value of `createNewObject()`.

In JavaScript create a new function called `createNewObject` and write a `console.log("TESTING")` to make sure it's working before we move on.

<!-- NEXT PAGE -->

Now that you got that in order let's build out that function's declaration block. Let's first create a variable to hold a reference to an object:

```html
<!-- 101-onlineClothingStore/index.html -->
<!-- more code up here... -->
 <script>
   // and more JS code here...
 
   function createObject() {
     let newObject = document.createElement("h3")
 
   }
 </script>
```

The variable is called `newObject` and its value is a new H3 object the Document created with its `createElement()` method. That's right! We're now using properties, events, and methods!!!

Now let's create another variable that will hold a reference to a Text Object/Node. We'll give it some basic text for now.

```html
<!-- 101-onlineClothingStore/index.html -->
<!-- more code up here... -->
 <script>
   // and more JS code here...
 
   function createObject() {
     let newObject = document.createElement("h3")
     let text = document.createTextNode("THIS IS A TEST.")
 
   }
 </script>
```
 
Now we need to append that Text Node/Object to our `newObject`.
 
```html
<!-- 101-onlineClothingStore/index.html -->
<!-- more code up here... -->
 <script>
   // and more JS code here...
 
   function createObject() {
     let newObject = document.createElement("h3")
     let text = document.createTextNode("THIS IS A TEST.")
 
     newObject.appendChild(text)
 
   }
 </script>
```

Notice that the `newObject` has this `.appendChild()` method on it as if by magic! It's not magic it **inheritance**. Even though it's a brand-spankin’ new H3 object, it's inheriting all of the Global Methods that are available to all HTML elements. The last step is to append our `newObject` to our Body object.

```html
<!-- 101-onlineClothingStore/index.html -->
<!-- more code up here... -->
   <script>
     // and more JS code here...
 
     function createObject() {
       let newObject = document.createElement("h3")
       let text = document.createTextNode("THIS IS A TEST.")
 
       newObject.appendChild(text)
       document.body.appendChild(newObject)
 
     }
   </script>
 </body>
```

Wow!! That was a lot, let's slow this train down and look at it more closely. Inside our functions declaration block, we declared 4 steps for the computer to do.
 
1. Create a new variable and use the Document's `createElement` method to place a new H3 element at its value
2. Then create another variable and use the Document's `createTextNode` method to place a Text Node/Object with `"THIS IS A TEST"` as dummy data.
3. Use the Global method, `appendChild()` to stick the Text Node/Object into the new H3 Object.
4. Use the same method to stick the new H3 Object into the Body of the Document object.
 
That wasn't so bad, was it?
 
##### Use the Data in the Variable
 
Instead of using that dummy data, `"THIS IS A TEST"` let's instead use the data our user would put in. Replace that **argument** with `usersInput`. Now that line of code will read: `let text = document.createTextNode(usersInput)`. Test it out. How's it working?
 
Annoying that you have to manually delete your input? This is why we use Input Elements and Button Elements inside Form Elements. But we'll have to get to that in a later lesson.
 
For now, you have a challenge!
 
<!-- ! END OF VIDEO 101.1.3.7 - Document Methods + Creating New Elements -->
 
<!-- TODO @CLAYTON section on ids and getElementById -->
 
## Summary & Challenge Yourself
 
We've covered a lot of information in this lesson from Button Elements and their methods like `onclick` to JavaScript keywords like `let` that communicates to our computer when we want to hold data in a variable or the keyword `function` that tells the computer to create a function and remember the instructions inside its declaration block and how to invoke a function with the trailing `()`. We began working with methods of the Window, Console, and Document Object to create new windows, logs, and elements.
 
I know this is a lot, but I hope this quick but deeper dive into the building blocks of web pages and the properties, methods, and events that compose them helps you start seeing this stuff as less "computer-sciency" and more practical. Sure, you have JavaScript and HTML syntax to learn, but that WILL come with practice. Just keep reading, studying, and saving your docs and do your Challenges!!
 
### Challenge One: A Very Important List
 
Your challenge is in this repo: [https://github.com/AustinCodingAcademy/101-important-to-do-list](https://github.com/AustinCodingAcademy/101-important-to-do-list). Start with the README.md file, read the entire instructions, then clone it and begin completing it.
 
 > NOTE: There's curveball: there's a new method introduced in this code, `getElementById()`. Just read the comments and look up the documentation if you don't understand it.
 
We'll use this assignment in our next class. If you want to get a leg up checkout the docs below:
 
* [Wikipedia - D.R.Y Principle](https://en.wikipedia.org/wiki/Don%27t_repeat_yourself)
* [W3S Docs - if Statement](https://www.w3schools.com/js/js_if_else.asp)
* [Medium - AirBNB Code Style](https://medium.com/dailyjs/dot-notation-vs-bracket-notation-eedea5fa8572)
* [W3S Docs - Name Attribute](https://www.w3schools.com/tags/att_name.asp)
* [W3S Docs - getElementById()](https://www.w3schools.com/jsref/met_document_getelementbyid.asp)
 
<!-- ! END OF VIDEO 101.1.3.1 - TITLE-->
<!-- ? Video Numbering and Title system: CourseNumber.ModuleNumber.LessonNumber.VideoNumber -->
<!-- * (VIDEO 101.2.4.3 - "CSS Selectors") === 101 Course, Module 2, Lesson 4, Video 3 - "CSS Selectors" -->

