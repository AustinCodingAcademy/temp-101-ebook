## The Two Perspectives + Object Modeling

* Perspective One: Objects are how the computer keeps up with memory and interacts with the world and people around it?
* Perspective Two: We use code to organize our thoughts about how to access that memory and give instructions on what to do with that memory to both the computer and other human-beings(fellow developers).

In the next session we'll explore the following questions:

  * How do we accomplish the invisible task of seeing the memory of computers?
  * How does code represent our programming intentions to the computer?

To do this we'll break them down in three parts: **Objects**, **Object Modeling**, **Code as Communication**.

<!-- ! END OF VIDEO 101.1.1.5 - Two Perspectives Overview -->

### Part One: Objects

Computers don't have eyes or ears...yet. They can't see a dog and hear a bark; therefore, they can't perceive the animal before them is a canine and not a feline. Instead they rely on objects, and categories of objects to interact with the world. So that dog would become an object with properties like: `wagsTail=true, barks=true, licks=true, species="canine"`. With this object and its properties the computer could categorize the animal as a dog type object but when it is given another animal with properties: `wagsTail=false, barks=false, licks=true, species="feline", isSelfCentered=true` then it can categorize that animal as a cat type object.

Everything is an object to the computer. It's how it relates to the world around it. People are objects, foods are objects, vehicles are objects. With so many objects, it would stand to reason that there would be types of objects/categories to put similarly related types of objects in. So cars, trucks, motorcycles, buses, scooters they could all be Vehicle type objects, objects that are of Vehicle type.
<!-- * relate this to block and inline elements later -->
This is the same with the components you see on your screen when you open a page. Your browser creates an object called `window`. And the website you navigate to sends information back to your browser to create another object called `document` which gets **mounted** inside of `window`. Inside this `document` object there are many other objects. Typical objects inside the `document` object include `header`, `body`, and `footer`, among many more. These are by no means all of the possible objects but they are the general first objects to build a web page.

  > Try it out:

  * Go to any website and right-click your mouse, 
  * Then click "Inspect" to open your Developer Tools. 
  * Next click on Console and type `window` + ENTER where the cursor is flashing. 
  * You should get something like this returned on the next line: 
    * `Window {window: Window, self: Window, document: document, name: "", location: Location, …}` 
  * What you did was ask the `console` object to access the `window` object and give you information about it.
  * What you're seeing is the **object literal** (literally the object written in JS) with its properties: `window`, `self`, `document`, `location`, etc...

We'll be using the console much more in the future and diving much deeper into all the objects mentioned above but before we do we have to get a mental "model" of all of these objects in our minds! The *third thing to keep in mind*!

<!-- ! END OF VIDEO 101.1.1.6 - Objects -->

### Part Two: Object Modeling

Object Modeling is the process of seeing the objects of the computer and how they relate to one another in our minds so we can effectively communicate with ourselves and one another about what is happening inside and between computers. To model these objects, we can imagine them in our minds, draw them on whiteboards, and even have graphic representations for them on our screen. This type of thinking is the intermediary between what the computer understands and what we humans understand. It is imperative that we practice Object Modeling every time we approach the building of a site or page because it will act as our map and compass for solving problems we've never seen.

Objects are just slots of memory that represent real-world things. So what does an object look like? What model can we use to describe them? Try first to write it down, draw it, and then imagine it. This will take some time. 

  > But try!

  * Draw a large box nearly the size of a sheet of notebook paper. At the top label it `window`. Inside draw another box nearly 3/4 the size of the first box. Label this one `document`.
    * Inside the `window` box create two lists titled: "Properties" & "Methods"
    * Under the "Properties" list write down the first five properties you find at this website: [W3S Window Object](https://www.w3schools.com/jsref/obj_window.asp) *NOTICE: The 2nd property is "Console" and the 4th is "Document"* These are two objects you've already come across; the "Console" is the one you opened in your Inspect > Developer Tools earlier and typed "window". And the "Document" is the other box on your page!!
    * In the "Methods" list write the first 5 methods you see on that same website: [W3S Window Object](https://www.w3schools.com/jsref/obj_window.asp)
    * Repeat these steps for the smaller box, the "Document" object, but with this page instead: [W3S Document Object](https://www.w3schools.com/jsref/dom_obj_document.asp)
    
      > *NOTE: the ones with parenthesis, `()` following them are methods and the ones without are properties.*
  
  * What you see on your paper is a simple model of two objects, Window and Document, and shorts lists of each of their properties and methods. This is Object Modeling. And this is how we will talk about EVERYTHING we learn. Everything is an object with properties, methods, and events.

To continue on this Object Modeling exploration we'll need to cover some new terms: **Properties**, **Methods**, and **Events**. These three new terms are called the **members** of an object.

<!-- ! END OF VIDEO 101.1.1.7 - Object Modeling Overview -->

#### Properties

All objects have **properties**. Properties are descriptions of the object. If you were an object you would have properties that might include: `name:`, `gender:`, `height:`, `weight:`, `age:`, `DOB:`, `job:`. The same goes for our web page objects. All visible objects have `color:`, `height:`, `width:`, `z-index:`, `font-size:`, etc... Properties are things that describe what something is, what it contains, and what it looks like when rendered. You'll also see properties referred to as **attributes** and **keys** while the value that is assigned to each of them (the part after the colon and before comma) is called a **value** leading to the common expression: **key/value pairs**, i.e. `name: "Rebecca",`, `age: 33,` or `width: 500px,`

#### Methods

Most objects have **methods**. Methods are like special properties in that they don't describe the object but instead they describe actions the object can do! You might have methods like `eat()`, `sleep()`, `run()`, and `beStill()`. However, as you saw in your exercise, objects on our web pages might have methods like: `confirm()`, `clearInterval()`, `createElement()`, `execCommand()` and `open()` because they are computer object-things and not human-being things with needs like food, water, and shelter.

Methods are also called **built-in functions** because they work like functions. They're small sets of instructions that can be executed just like other functions. Now, we haven't fully covered functions yet but suffice it to say that if you just learned how to mix cocktails you would now have two new functions written into your system that are maybe called: `mixIngredients()` and `shakeVigoursly()`. So every time you need to make a cocktail for your party you would first call `mixIngredients()` then `shakeVigoursly()`. Not everyone needs or wants to learn how to make cocktails but everyone needs to eat, sleep, and drink. So the good Lord gave us all built-in functions/**methods** called: `sleep()`, `eat()`, and `drink()`. In web development, the reason we have methods is because some functions need to be called regularly, by all developers for most apps and don't need to be special or customized. So the engineers of HTML created "built-in functions" that are readily available to be used by us. The "built-in" functions are **methods**.

#### Events

Most objects also have a third category of **members** called **Events**. You can think of events as interactions. Interactions that happen between objects and other objects or objects and humans. See, we can move our mouse, place our cursor on an element on our screen, and click on that element. In that single move there are three distinct events/interactions that happen: 1) `onmousemove`, `onmouseenter`, and `onmousedown`. The events are built into objects so that they can be interacted with. We people have events like: `lookedAt`, `smiledAt`, `handShaked`, `poked`, `hugged`, `shoved`, `greeted`. All of these are ways in which our bodies are interacted with in the world around them.

In web development terms, these Events are used to "capture" an interaction and then trigger an action because of it. For the most part all of these built-in events are attached to a "blank"; in that, they fire every time the event happens but nothing is triggered. It's up to us, the developer to create the reactions and then attach them to the events. So we might say something like: `onmouseenter="openGreetingWindow()"`. This could be equivalent to our bodies being programmed with: `smiledAt="smileBack()"`.

At this point you may be a bit confused on the difference between **methods** and **events** so for now separate them by this distinctions:
  
  * **Events** capture interactions with the object from the outside world, in order for us to attach instructions to be carried out when the event happens.
  * **Methods** are actions(built-in functions) the object can use to outwardly interact with its world.
  * And **properties** are bits of information that describe the object. Often called **attributes**, as well.

While object modeling is a great way to understand how a computer interacts with the world it is not how we communicate to the computer our programming intentions. The computer, frankly doesn't know anything about this Object Modeling stuff. It just knows about objects because what we interpret as a "model" is the complete and total reality of a computer. It knows nothing else. Because of this, we have to use a language that communicates to the computer our intentions with its objects and their subsequent properties, methods, and events. This language is what we generally call **code**. The great thing about you learning code now is that you've already built things with three different coding languages and you've been reading code in all of these textual examples.

<!-- ! END OF VIDEO 101.1.1.8 - Objects, Properties, Methods, and Events -->

### Part Three: Code as Communication

In order for us to communicate our programming needs and intentions we need a language that can be interpreted by the computer and understood by humans. This is what we call **code**. Code comes in many different names and flavors that we call languages, or **programming languages**.

We use programming languages to communicate to both humans and computers what our programming needs and intentions are. Notice earlier, we used the word "interpret" for computers and "understand" for humans. This is because, as long as your fellow developers know the syntax and semantics of the language you chose to write, they will understand what you meant. But the computer must "interpret" what you wrote because the computer doesn't actually know JavaScript from Closure or Haskell. Our computers use interpreters that convert your programming language of choice to binary before it executes the program you built.

Programming languages are similar to our human languages in that they were all created to represent and communicate our needs and intentions. It doesn't matter what language you are speaking...as long as you are speaking to someone who understands the language they will know what you're saying. This goes for computers as well. When we're building websites and web app we're talking to web browsers who know three languages: HTML, JS, and CSS. If we are building iOS apps we're talking to an operating system that understands Swift and if we're build apps for Android we're talking to a system that understands Java. All languages are built in similar ways because they all have to accomplish the same goals: store data, move data, and render data. In this way, you can feel confident that once you now how to program in JavaScript, learning to program with Python, Swift, Java, Go, or C# will come much easier!

This layer of "abstraction" is not so important for us to learn, so much, as it is helpful for us to understand that programming languages like JavaScript are just languages with nouns, verbs, sentence structure, actions, and objects that all represent to the computer our programming needs and intention of how to we would like to move, manipulate, and display the objects our computers know about.

<!-- ! END OF VIDEO 101.1.1.9 - Code as Communication -->

## In Summary: Our Three Jobs, Object Modeling & Code as Communication

Now that we've learned our three jobs as web developers are to store, move, and render data inside an invisible world with 10 levels of abstractions on a computer that sees only objects with properties, methods, & events and interprets only code it recognizes we have our work cut out for us. How do we do it?

We first have to remember that our three jobs as web developers is to store data, move data, and render data. The next is to always draw out our objects on paper, whiteboard and in our mind so we don't forget that everything is an object. Third, we have to practice gratitude for the languages we get to learn and be happy that we get to create stories and books with these programming languages instead of new words for every thought. After that, we must always reference our docs. [Docs are how to learn and remember object, properties, methods, and events](https://www.w3schools.com/jsref/obj_window.asp). And lastly, we have to keep learning and trusting that **you can do this**!

<!-- ! END OF VIDEO 101.1.1.10 - In Summary: Our Three Jobs, Object Modeling & Code as Communication -->
<!-- SEND THEM OFF @CLAYTON -->