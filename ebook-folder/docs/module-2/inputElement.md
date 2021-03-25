# The Input & Creating Objects

With this new knowledge, you are able to build some pretty awesome stuff already, even if you don't recognize that yet. Yet, before you take on the world let's learn just two more skills: Input elements and how to create new Elements.

## Using the Input Element

The first is actually very easy and will boost your skillset tremendously! The `input` element is by far the most used element on the web simply because it can be for so many things: checkboxes, radio buttons, email, password, paragraph, sliders, file uploaders, color pickers, and more!! The full list can be found at [W3S Docs - Input Element](https://www.w3schools.com/tags/tag_input.asp).

Its default mode is a short input box: `<input />`. But using the `type=` attribute we can change it to be any of the types of input listed above including a button! Try it.

 > In the same file create an `<input type="submit"></button` element.

The reason we have this option is that Input Elements normally go inside the Form Element and we need to distinguish them as submit buttons & reset buttons versus input type inputs. We'll get into the Form Element soon but for right now let's figure out how we can use the Input Element to take input from a human to later do something with it!

The Input element, just like the Button element has many Events we can use to capture interactions and pass along data. The event we'll use for this example is the `onkeydown` event which gets fired when a human-user presses any key down while inside the input field. Other events get fired including `onkeyup` & `onkeypress`, you can study the full list of [Global Events here, aka Event Listeners](https://www.w3schools.com/tags/ref_eventattributes.asp).

In the same fashion, we made our Buttons call a function when they were clicked let's make our input element call a function when a human-user's key is lifted.

```html
<!-- 101-onlineClothingStore/index.html -->
 <body>
     <!-- ...more code here.. -->
   <input value="" onkeyup="setValue(this.value)"/>
 
   <script>
     // and more JS code is here...
 
     function setValue(input) {
       console.log({input})
     }
   </script>
 </body>
```

  > NOTE: To view your [Browser's Console](https://developer.chrome.com/docs/devtools/shortcuts/) object you'll need to open your DevTools (Mac) ++cmd+opt+j++ ; (Windows) ++ctrl+shift+j++ ; or just right-click >> Inspect >> Console

Everything works well? Can you see your input in the Console? The only new bits of syntax you see here are `this.`, `value="`, and `{input}`.

* `this` is actually pretty easy, it refers to the exact object that is calling the function. If we created a new input and it called the same function the computer wouldn't know what to do because it wouldn't know how to call it. So we use the keyword `this` to communicate that the context were calling the function from is *this object* and not *that object* or any other object besides `this` object.

* `value=` is also easy because it's an attribute just like the other attributes we've been writing and refers to the property `value` on that object. Its current value is an **empty string**, `""` but as we type, the value will change under-the-hood. To see this change we need to pass that value along to a function to do something with it.

* The last bit is super easy. You can see the input appear in the console without the `{}` but with the **curly-braces** we just see the data in a cleaner format: an object with a key called `input` that has a value of whatever the `input` is. If this is confusing, just remove the `{}` around `{input}`.

## Using Variables To Hold Values

We already know how to create variables with the `let` keyword and we know that we need to use variables to hold on to pieces of data. Let's create a variable that can hold onto our user's input so we can do other things besides logging it in the Console object...

```html
<!-- 101-onlineClothingStore/index.html -->
 <body>
     <!-- more code is here.. -->
   <input value="" onkeyup="setValue(this.value)"/>
 
   <script>
     let usersInput;
     // and more JS code is here...
 
     function setValue(input) {
       usersInput = input
       console.log({usersInput})
     }
   </script>
 </body>
```

  > Note the changes in the code: We're now saving our data to a variable and logging the value of the variable, `usersInput` instead of directly logging what comes into the function's **parameter**, `input`.

<!-- ! END OF VIDEO 101.1.3.6 - Input Element + `let` Variable -->

## Additional Resources

- [ ] [Article, Geeks4Geeks - Button vs Input](https://www.geeksforgeeks.org/button-tag-vs-input-typebutton-attribute/)
