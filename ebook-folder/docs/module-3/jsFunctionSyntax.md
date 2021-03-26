# JS Function Syntax

*“Often we women are risk averse. I needed the push. Now, more than ever, young women need more seasoned women to provide that encouragement, to take a risk, to go for it. Once a glass ceiling is broken, it stays broken.” –Jennifer Grahnolm*

<!-- Overview of JS Functions
What is the syntax
What can we learn
Alternative syntax
Invoke a JS Function
Moving Forward
Know Your Docs
Terms to Know
Questions for Student Discussion -->

## Overview

Functions may seem scary at first but if you think of them in the same way CSS rules are built, they're actually the same thing! See when you select an element and give it rules those rules are like a function waiting to be called. Usually they're called when the web page loads. Or, if you use a pseudo selector, the rule is called when the user does the thing you were looking for like a `:hover`. In this same way, JavaScript functions are just recipes or sets of instructions waiting to be called and used when they're needed!

Obviously you've already worked with some JavaScript in a few of your projects but starting today we're going to slow down a little to focus on JavaScript. It can be a little harder to grasp than CSS but I think if you work to ask questions, answer your own questions, and ask more questions then you'll get this very quickly!

<!-- ! Video Contents:  (width="655" height="368", ratio 1.77) -->

## What is Syntax?

**Syntax** is a funny word and not often used outside of programming. But, in fact, this word was used before programming was created.

A [Google Search](https://www.google.com/search?q=syntax&oq=syntax) provides the following:

  > "the arrangement of words and phrases to create well-formed sentences in a language. From the Greek, Suntaxis, - To arrange together."

What this means for us is that certain **keywords** and **characters** must go in specific order for the computer to interpret what we're trying to tell it. Just the same with CSS we have a **Selector**, **Property**, **Value** and **Declaration Block** and with HTML we have an **Opening Tag**, `<h3>` and a **Closing Tag**, `</h3>`, we have specific syntax for JavaScript functions, as well. Take a look:

```javascript
  // Function Declaration
  const separateWord = (word) => {

    // Function Body (between the { } )
    const splitUpWord = word.split("")

    // Function Return Statement
    return splitUpWord
  }
```

The code snippet above:

1. creates a **function** called `separateWord`
2. which takes in a **parameter** named `word`
3. and creates a new **variable** inside its **Function Body** called `splitUpWord`
4. then assigns this new variable's value to what the **method** `.split() `returns when 5. it is called on the `word` that is given to the function.
6. After this the function returns the value of `splitUpWord`.

If we **called** this function with the word: "Balloon" like so, `separateWord("Balloon")` we would expect it to return the following: `["B", "a", "l", "l", "o", "o", "n", ]`

```javascript
  separateWord("Balloon")
```

### What Can We Learn From This?

In this small example you can deduce that JavaScript, like CSS and HTML reads from top to bottom and left to right. We call this **Synchronous**, or that each action happens after the last action is finished, one at a time.

We can also see that a **function** is created the same way a **variable** is created, using the const **keyword** and then **naming** it what we'd like to name it.

Next we see that, besides having to use the JavaScript Language Specific **Keywords** like `const`, `.split()` and return we as the developer get to decided on the names of our functions and variable. In the snippet above we get to decide the name of `separateWord`, `word` and `splitUpWord`. We could have just as easily named these `crumble`, `cookie`, or `chip` and the program would have still done the exact same thing!

Now we can focus in on the characters or **tokens** used in sequential order. After the name of the function, separateWord we see the following characters: `= () => {}` these character go in order every time you create a function and you can read them aloud to yourself like this: "Create a variable called `separateWord` that equals a function and returns the following..." Where:

```markdown
* `const` - "Create a variable..."
* `separateWord` - "...called separateWord..."
* `=` - "...that equals..."
* `()` - "...a function..."
* `=> {}` - "...and returns the following..."
```

So you see then that a pair of parenthesis, `()` signifies a function in JavaScript. This is where we declare **parameters** when we declare a functions and where to pass in **arguments** when we call/invoke a function.

A **Fat Arrow**, `=>` shows that it returns whatever follows, and a pair of curly-braces, `{}`, (just like CSS), is a block of code to be run when the function is called.

### Alternative Syntax

We've just covered the *preferred* way to create a JavaScript function, now we'll show you the older way to create a function. This way is still used and you might even use it later on in your coursework and career but for now just know that it exists but that we'll use the preferred signature, (detailed above), throughout this course.

```javascript
  function separateWord(word) {
    const splitUpWord = word.split("")

    return splitUpWord
  }
```

This method uses the **reserved word** `function` to declare the same function as we saw above. It has it's [purposes](https://mrkiffie.com/2017/anatomy-of-a-javascript-function/) but for now let's just let it reside in our awareness.

## Invoke a JavaScript Function

Declaring a function is the hard part. It's where you write out the steps you want your computer to do when that function is **called** but when the computer reads the **function declaration** it doesn't *run* the code. Instead it just stores it in memory as a set of instructions to do before it's time to run them.

Therefore, **invoking** or **calling** a function is when the function is actually run. The syntax of this is really simple, it looks like this: `myFunction()`.

That's it! Seriously, when ever we want your computer to run a function you've built you give it a simple line: `thFunctionsName()` where the name of the function is followed by a pair of parenthesis, `()`.

## Parameters vs Arguments

Not all functions have **parameters**. Parameter are bits of data that functions hold on to and use to make calculations or perform specific tasks on like our separateWord example above. That function example had a parameter we called word. Which means, we the function is called it needs a piece of data like a word, or **string**, given to it so it can perform the tasks it's supposed to perform. When we give, or **pass**, data to a function we call it an **argument**. Below is an example of two functions. One requires a parameter and the other does not. Then you'll see them both invoked, one with an **argument** passed to it and the other without.

```javascript
  // requires an argument to be passed to it because it has a parameter defined as "username"
  const sayHi = (username) => {
    greetingString = "Hi, " + username + "!"

    return greetingString
  }

  // doesn't require an argument because it has no parameters defined
  const sayHello = () => {
    return "Hello!"
  }




  // This line will return: "Hi, Greta!" because we passed it an argument: "Greta"
  sayHi("Greta")

  // This next line will return: "Hello!"
  sayHello()
```

## As We Move Forward

As we add more to our JavaScript knowledge base you'll see methods like `.split()` used again and again. So let's take a minute to cover three aspects that will give us a solid foundation of what they are and how they're being used.

**Aspect 1**. Just like the methods you're used to on the `document` or on each of the HTML Elements, methods in JavaScript are **built-in** to the language and are specific to the **Data Types** just like certain methods are specific to certain HTML Elements. In the case of `.split()`, this method is specific to the **String** data type, or words/characters inside a pair of quotes, `" "`. You can't call this method on a Number data type because it doesn't exist on **Number** types of data! So you can start thinking of the **Data Types** a lot like the Elements we create on the DOM Tree. They are plain object-things we can't see but have many little properties we can access on the back side of them.

**Aspect 2**. The syntax of `.split()` looks just like the syntax of **Invoking** a JavaScript function we built ourselves. That's because it is. These **methods** were built by the developers of the JavaScript language and reside under-the-hood. We don't have to build them, all we have to do is [read the docs](https://www.w3schools.com/js/js_string_methods.asp) on them and know how to use them.

**Aspect 3**. The `.split()` method returns a funny looking thing called an **Array**. (*Remember, `["B", "a", "l", "l", "o", "o", "n", ]` from above?*) This is another **type of data** in JavaScript which we're going to dig into in the next lesson. It's important to understand simply that each *type of data* or **data type** has utility for specific scenarios. The Array data type has the most built-in methods so it's often advantageous to convert data like a string to an array. You'll see in the next lesson!!

## Practice It

Go to [W3Schools JavaScript Exercises](https://www.w3schools.com/js/exercise_js.asp?filename=exercise_js_datatypes1) and complete the first 15 challenges in JS Variables, **JS Operators**, **JS Data Types**, and **JS Functions**.

  > HINT: in **JS Data Types** you'll be asked about a data type we haven't covered in length yet. It's an Object.

## Know Your Docs

- [ ] [MDN Docs - Old-School Function Syntaxt](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Functions)
