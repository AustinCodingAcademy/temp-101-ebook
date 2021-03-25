# The Window Object

A few lesson earlier you used the `alert()` method on the Window object but the Window object has far more abilities than just signaling an alert! In fact, it has 31 properties, 26 methods, and 80 events in total. You can learn to use each of them by [reading the documentation](https://www.w3schools.com/jsref/obj_window.asp) on them. For now, let's look at two of them `.open()` and `.close()` just to get familiar with the process of using them.

## Window.open & Window.close Methods

These methods, respectively, open and close a new window. Use that code you've been playing with to follow along:

```html
<!-- 101-onlineClothingStore/index.html -->
 <body>
   <button onclick="sayHello();">Click Me</button>
   <button onclick="sayHi();">Click Me Too</button>
   <button onclick="openANewWindow();">Open</button>
  
   <script>
     let secondWindow;
 
     function sayHello(){ alert('Hello, Window.alert Method!') };
     function sayHi(){ console.log('Hi, Console.log Method!') };
     function openANewWindow() {
       secondWindow = window.open("", "myWindow", "width=400, height=300");
     }
    
   </script>
 </body>
```

There are a few more bits of **syntax** to take in. We created a new function called `openANewWindow` and call it with a new button to `onclick` event. But there's something new going on at the top of the Script element and inside the `openANewWindow` function declaration. The `let` **keyword** you see up there signifies a place to hold a bit of data. We call this a **variable** because the bit of data that's held in these things usually change and we don't always know what value will be there, we just know we'll need to reference it later.

 > Think of how you might build a calculator. When the user types the first input you only know the number could be between -∞ and ∞; the same goes for the second input. Because of this programming challenge we have to create a place for the values the user inputs to be held until we know if we're going to add, subtract, multiply, or divide the numbers. This "place to hold values" is called a **variable** and we use the keyword `let` to communicate that in JavaScript.

After the **keyword** `let` we see `secondWindow`. This is the name of the variable and it’s used just the same way we name our functions, so we can reference them later in our program. It's important to know you can name your variables anything you want as long as they don't begin with a number(0-9) and are not one of [JavaScript's keywords](https://www.programiz.com/javascript/keywords-identifiers). The second guideline about naming variables is that they usually have descriptive names and are **camelCased**; `secondWindow` is a descriptive name for this variable it starts with a lower-case letter and has a capitalized letter at the beginning of its next word.

This particular variable would be described as **declared** but not **defined**. Try it.

 > Go to your DevTools, open the console tab and type `secondWindow` + ++enter++. What do you get?

You should get "undefined" as a return value. This is because the variable, the space for data, is declared but it has no value. Click the "Open" Button and re-type `secondWindow` in the console. What do you get? You should get something like: `Window {window: Window, self: Window, document: document, name: "myWindow", location: Location, …}`- This is another Window object opened by the browser and the properties and values you see listed are the key/value pairs of that new Window Object. The reason you're able to see these properties is because you saved a reference to this new Window object in the variable `secondWindow` and are now listing that data out in the Console.

### Window.Close

As you would expect there is an opposite method to the Open method, `close()`. Go ahead and create a function that calls `window.close()` and run it

```html
<!-- 101-onlineClothingStore/index.html -->
 <button onclick="closeTheNewWindow();">Close</button>
 
 <script>
   function closeTheNewWindow() {
     window.close();
   }
 </script>
```

What happened? Yeah, I tricked you. This code tells our current window to execute its own `close()` method. But we want instead for this Window to close the other window.

 > Hold ++cmd+shift+t++ (Macs) or ++ctrl+shift+t++ (Windows) to reopen that tab or simply relaunch Live Server.

The way we close this second window from our current window is to use that same variable we referenced in the Console to list out its properties. If we can get to its properties, we can get to its methods! Replace `window.` with `secondWindow.` and see what happens.

 > NOTE: You'll have to open the second smaller window before you can close it again.

<!-- ! END OF VIDEO 101.1.3.5 - Window.open + .close -->

## Know your Docs

- [ ] [W3S Docs - HTML Events](https://www.w3schools.com/tags/ref_eventattributes.asp)
- [ ] [W3S Docs - Window Object](https://www.w3schools.com/jsref/obj_window.asp)
