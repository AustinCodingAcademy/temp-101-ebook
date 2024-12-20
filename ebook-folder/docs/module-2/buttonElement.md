# The Button Element

*“Hold fast to dreams,*<br/>
*For if dreams die*<br/>
*Life is a broken-winged bird,*<br/>
*That cannot fly.”*<br/>
*―Langston Hughes*<br/>

## Overview

As you learned in the Form Elements lesson earlier, `input` elements can be changed to accept all sorts of data including *buttons* by changing the value of their `type=` attribute. Here we'll cover the actual `<button>` element because the real reason to use it over a `<input type="button">` element is for styling.

If you're wanting to but content or images inside of a button then you'll have to use the `<button></button>` element. Plain and simple, that's it!

However, if you want to use a `<button>` element on a form you have to set its `type= `attribute to "submit": `type="submit"` and *poof*, you have a submission button.

But learning about this new element brings us closer to a topic we've only briefly covered so far, Event Listeners.

<iframe src="https://player.vimeo.com/video/395038529" width="655" height="368" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen></iframe>

## Follow Along

We're about to learn how to use Event Listeners in the next lesson. To get familiar with what they are and how to use them, we'll use the familiar Button Element as a leaping off point. Go ahead and open the `101-onlineClothingStore` folder you started earlier and add this bit of code to the `index.html` file.

```html
<!-- 101-onlineClothingStore/index.html -->
 <body>
   <button></button>
 </body>
```

Turn on your [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) and see what's on the screen. Is there a tiny grey button at the top-left of your white screen? Good, that's how it should look. Your browser comes with "[Default Visual Styles](https://gist.github.com/ambidexterich/34828a904dd97dd2a345)" of content created in HTML. So all elements will come with some sort of, albeit, ugly styling. Button styling is defaulted to grey and is as wide and tall as the content inside them, the **innerText**.

  > **innerText** is a property on ALL HTML elements. It holds the value of the text inside. When we learn how to build with `<p>`, `<a>`, and all the `<h*>` elements, we'll see they all have a property on them called innerText. Write that down and draw it for yourself. This is part of your Object Modeling in your own mind.

<!-- TODO INSERT IMAGE of Button Element table with 3 rows: properties, methods, events that includes innerText as a property -->

Let's now add some "innerText" to this button. Between the opening tag and the closing tag type "Click Me".

```html
<!-- 101-onlineClothingStore/index.html -->
 <body>
   <button>Click Me</button>
 </body>
```

When we learn a little more JavaScript we'll be able to change this `innerText` property dynamically by writing some JS code like `button.innerText = "Oh, Click Me Again!"` For now, we'll **statically** set it in HTML by putting the text between the opening and closing tags.

Now that we have the first **property** of ALL HTML elements including the `button` element let's play with one of its events! Again, all elements have Properties, Methods, and [Events](https://www.w3schools.com/tags/ref_eventattributes.asp) we get to use to build with. By reading the documentation of these **members** we learn more about them and how to use them.

[W3S Docs - Button Element](https://www.w3schools.com/tags/tag_button.asp)

<!-- ! END OF VIDEO 101.1.3.1 - The Button Element -->
<!-- ? Video Numbering and Title system: CourseNumber.ModuleNumber.LessonNumber.VideoNumber -->
<!-- * VIDEO 101.2.4.3 - "CSS Selectors" === 101 Course, Module 2, Lesson 4, Video 3 - "CSS Selectors" -->

### The "onclick" Event + Inline JavaScript

Most HTML elements have the `onclick` event as one of their **members** but Button depends on this **event** because what else do you do with a button besides click it?

As mentioned before, **Events** are like triggers that fire each time the interactions happens. But until we add a function to that trigger the Event is firing a blank. Even though we don't see code that represents it, our `button` object currently has an **undefined** function attached to its `onclick` event. We don't typically write undefined events, but if we did write it in code it would look like this:

```html
<!-- 101-onlineClothingStore/index.html -->
 <body>
   <button onclick="">Click Me</button>
 </body>
```

  > Notice the **empty quotes**? Inside those quotes, after the `=` sign is the value of this event. This is a **key/value** pair. the key is `onclick` and the value is `""`.
  
Let's write a value for this button's `onclick` key. Type this in and run it to see what happens in the browser.

```html
<!-- 101-onlineClothingStore/index.html -->
 <body>
   <button onclick="function sayHello(){ alert('Hello!') }; sayHello();">Click Me</button>
 </body>
```

The line of code we just added between the `""` marks is actually JavaScript but it's written **inline** with the HTML code. This isn't a common practice anymore but it's the way developers wrote it *back in the day* and a good way for us to begin to learn what's going on. Take a close look at this new code and spend time trying to understand it. The best place to start is dividing it in half at the `;`.

  > NOTE: Traditionally, lines of JavaScript are ended with `;`(semi-colons) although the latest versions of the language don't require it. Nevertheless, we'll use them in our first lessons as we get acquainted with the language.

Before the first semi-colon we see `function sayHello(){ alert('Hello!') }`. With the **keyword**, **function** we are declaring a function named "sayHello()" and defining what it's supposed to do when called, which is: `{ alert('Hello')}`. This segment of code is called a **Declaration Block**, it's where we declare to the computer the instructions we want for it to run when the function is run/executed/called/invoked. We can put any set of instructions we want between the `{ }` but this one's pretty simple, it calls another function named `alert`.

  > NOTE: These words: run, execute, call, invoke all mean the same thing: "To perform the instructions of a particular function." You can interchange them as much as you like but this digital book will try to use the words "called" and "invoke".

`alert()` is a function that opens a drop-down window that "alerts" you of something. It's typically used to forewarn the user they are about to submit a form or override a security measure, etc. *Actually*, the alert is a [Method of the Window object](https://www.w3schools.com/jsref/met_win_alert.asp) which means we could have written the code like, `{ window.alert('Hello')}` as well. We don't have to do this because "alert" isn't a method on the Button object, the Body object, or the Document object, only on the Window object so when we call it, the browser will keep going up the levels of objects until it finds the first "alert" method it comes to. We'll learn more about these [Window Object Methods](https://www.w3schools.com/jsref/obj_window.asp), known also as **Global Methods**, as we build more and more.

The last two parts of this code are: `'Hello!'` and `sayHello();`. The first of these is easy. It's an **argument**. **Arguments** are values we, as developers, get to decide to pass into functions and the functions return different things based on what we pass into them. Try it.

Change the `'Hello!'` argument to something like: `'Hello, Clayton!'`. Did you see the change?

What about that last part? `sayHello();`. This is what's called a **Function Invocation**. It invokes/runs the function. The way it works is by naming the function we want to invoke/call. In this case, it's `sayHello` then we add those trailing parenthesis afterward `()` to communicate to the computer we want it to run the instructions inside the **Declaration Block** of the function we just named. See how this is written the same as `alert()`? ...`sayHello()`...`alert()`...? Name the function and then invoke the function/

<!-- ! END OF VIDEO 101.1.3.2 - onclick + Function Breakdown -->

#### New Word Clarification

We just covered a lot of new terms so let's take a moment to revisit some of those tricksters.

* **Function Declaration** - This is where a function is declared and defined. Until it's called/invoked, it isn't doing anything except taking up memory like a recipe in your cookbook.

```js
 function myFunctionExample(a, b) {
   let sum = a + b
   return sum
 }
```

* The **Declaration Block** is the part between the `{}` where the step-by-step instruction goes.

* **Function Invocation** - This the code that calls/invokes the Function Declaration. It tells the computer to execute the instructions in the Declaration Block.

```js
 myFunctionExample(2, 3)
```

* **Function Arguments** - These are values you can pass into functions. In the example above `2` and `3` are two arguments passed into the `myFunctionExample` function. Based on the instructions in the Function Declaration and the arguments passed into it, the result would be 5.

* **Attribute/Property/Method** - If you visited the [Button Element Docs page](https://www.w3schools.com/tags/tag_button.asp) your probably saw the use the word **Attributes** instead of **Property**, **Event** or **Method**. This is because HTML was created to represent visual Elements on a screen so all of the properties and their values were originally written together, in line with the elements like the line of JavaScript we just broke down. The word **Attribute** means the same thing as **Property**, **Event** or **Method** but specifically refers to something written in HTML rather than in CSS or JavaScript. Anything you see written inside the opening tag of an element is an **Attribute** but it refers to the **Properties**, **Events**, and **Methods** of that object. Example:

```html
 <h3 id="fish-fry" >Example Title</h3>
```

The H3 Element above has an `id` attribute. This attribute assigns the value of  `"fish-fry"` the the `id` property of that object.

 > NOTE: If this all doesn't gel right now, don't worry. With practice and in time it'll all come together.

<!-- ! END OF VIDEO 101.1.3.3 - New Word Clarification -->

### A Better Way to Write JavaScript

The line of JavaScript we just broke down was a little hard to read because it was all on one line. Thankfully there's a better way to write it, with the `<script>` Element!

The Document Object has a `scripts` property to hold scripts. When we create a Script Element we are giving the `scripts` property a value. And just like with our Human object, if we want them to be able to do new things we need to give them new functions like: `rideBicycle()` or `cutWatermelon()`. With the `<script>` element we can give our Document Object new values inside of its `scripts` property.

Let's move our current **inline JavaScript** into our `<script>` element.

```html
<!-- 101-onlineClothingStore/index.html -->
 <body>
   <button onclick="sayHello();">Click Me</button>
 
   <script>
     function sayHello(){ alert('Hello!') };
    
   </script>
 </body>
```

Make these changes and run your page again. It should be working just as before. Now let's create another button and have it also call `sayHello` when its `onclick` event is ...clicked.

```html
<!-- 101-onlineClothingStore/index.html -->
 <body>
   <button onclick="sayHello();">Click Me</button>
   <button onclick="sayHello();">Click Me Too</button>
 
   <script>
     function sayHello(){ alert('Hello!') };
    
   </script>
 </body>
```

Now build another function called `sayHi` but this time call the Console object's method named `log()` and pass into it a different **string**.

```html
<!-- 101-onlineClothingStore/index.html -->
 <body>
   <button onclick="sayHello();">Click Me</button>
   <button onclick="sayHi();">Click Me Too</button>
 
   <script>
     function sayHello(){ alert('Hello, Window.alert Method!') };
     function sayHi(){ console.log('Hi, Console.log Method!') };
    
   </script>
 </body>
```

> NOTE: In order to see this you'll have to open your DevTools and go to the Console Tab. Click on both buttons and see what happens.

<!-- ! END OF VIDEO 101.1.3.4 - Inline JavaScript + Script Element -->

## Summary

In the next lesson we'll learn how to tie Input Elements and Button Elements together but at this point you know know how Event Listeners work, even if you've only used one: `onclick=`. Essentially, you figure out what action you'd like the user to do then attach it to a **invocation** to call a function you wanted executed when that action is done!

Let's look at the Input Element and then move to see a more Event Listeners.