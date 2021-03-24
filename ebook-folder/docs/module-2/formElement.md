# The Form Element

*Be a self-starter. Do it now! When you don't know how to do something, start. Beware of the paralysis of analysis. Be a person of action. —Mamie McCullough*

The Form Element is used to create, you guessed it, forms! Or as defined by [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/form):

 > "The HTML `<form>` element represents a document section containing interactive controls for submitting information."

The Form element is an object in HTML that presents to the human-user a place to input information/data but also gives us a place to store that data until they complete the form and click the submit button which triggers a fetch request to send that data to a server then to a database.

To use Form elements properly we have to learn their attributes(properties and methods).

<!-- TODO INSERT Drawing of Form => Function => Internet => Server => Database -->

<!-- ! END OF VIDEO 101.1.10.1 - Form Element Overview -->

## Attributes of the Form

Like all other HTML Elements, the Form Element has all the [Global Attributes](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes) (events and methods) along with a few special ones of its own. Let's break them into two categories: Required and Optional

### Required Attributes/Properties: action, enctype, method, novalidate, target

These properties are required to be defined for your forms to work properly so let's look at them and how they're used. We'll be using the following code as a reference point.

```html
 <form action="https://www.singlesingerssite.com/signin.htm" method="post" autocomplete="off">
   <div>
     <label for="email">Email</label>
     <input type="text" name="email" id="email" required>
   </div>
   <div>
     <label for="password">Password</label>
     <input type="password" name="password" id="password" required>
   </div>
   <div>
     <input type="submit" value="Subscribe!">
   </div>
 </form>
 
 <!-- Notes on the unfamiliar part of the code above: -->
 <!-- The Div element is used to divide out the page -->
 <!-- Label Elements are used to label an Input Element -->
 <!-- Input Elements are versatile and can be used for any type of form input -->
```

* `action=` - The value of this must be a URL like the one you see above. This tells the form where to send the data when it's submitted by the human-user. However, the preference for this technique has been replaced with creating a function that uses `fetch` to handle the HTTP request and calling it `onclick=` of a `submit` button, i.e. `<input type="submit" onclick="handleSubmit()">,`

* `method=` - If you choose to use the `action=` attribute to define the URL that will process your forms data, then you have to define the method as a POST. Later in this lesson, you'll learn about the multiple values you can use here to send different types of Requests over HTTP(S). For now, the two values you can use here are `"post"` and `"get"`. If you use the preferred `fetch` alternative then you will need to declare the Request as a POST in the `fetch` because the default value of the Form Element's `method=` is `get`, see below:

```js
 fetch('https://fakestoreapi.com/products', {
   method:"POST",
   body: {}
 })
```

#### Properties that are Required but have Implied Default Values

* `enctype=` - This defines the type of encoding the data should go through before it's sent over HTTP. The values you can use are:
 * `"application/x-www-form-urlencoded"`: The default value and used for most forms. You don't see it defined and declared in the code above because it's the default value if you don't type out one of the following instead.
 * `"multipart/form-data"`: If your form accepts files as a possible input then you need to declare it using this value.
 * `"text/plain"` - Introduced by HTML5 for debugging purposes.

* `target=` - this property specifies where the Response object should load; that is, after the form is submitted and there's a response from the other page, site, or server where should the response go? The option you have are:

 * `_self`: Load the response into the same browsing context(window/tab) as the current one. This is the default if the attribute is not specified.
 * `_blank`: Load the response into a new unnamed browsing context — usually a new tab or window, depending on the user’s browser settings.
 * `_parent`: Load the response into the parent browsing context of the current one. If there is no parent, this option behaves the same way as `_self`.
 * `_top`: Load the response into the top-level browsing context (that is, the browsing context that is an ancestor of the current one, and has no parent). If there is no parent, this option behaves the same way as `_self`.

 >NOTE: later on we'll override this behavior with a `.preventDefault()` but more on that later.

* `novalidate` - The default attribute is `validate` which translate to `validate=true`. The reason this is defaulted to `validate` is because form validation is the first step in preventing hackers’ attacks. It's not the end-all-be-all but it is the first layer of security in building apps. **Form Validation** is part of a larger practice called **Client-side Validation** and HTML comes with built-in measures that we'll get into when we learn about the Input Element. For now, in the code example notice `required` and `type=email` and `type=password`. These are form validation measures built into HTML because they require the human-user to fill them out and the Email Type Inputs require a `@` and `.com` while the Password Type Inputs mask the password with `••••••`. Try it. Throw the code into a new HTML file and serve it up. Do you see the `•s`? Try submitting an email with the `@`.

Most of the time you do want to `validate` so you won't type `novalidate` and don't need to specify `validate` because its default value is implied.

### Optional Form Attributes/Properties

* **[autocomplete=](https://developer.mozilla.org/en-US/docs/Web/Security/Securing_your_site/Turning_off_form_autocompletion#the_autocomplete_attribute_and_login_fields)** - allows the human-user's browser to auto-fill the form if they have their information stored in their browser. You can toggle this with the values: `"on"` and `"off"` however many browsers are opting to not read `"off"` for login fields.

 > NOTE: If you are building a page that allows the human-user to update their password you can use the third value: `autocomplete="new-password"` to prevent the browser from auto-filling the inputs on that form.

* **accept-charset=** - sets the language/[Character Set](https://developer.mozilla.org/en-US/docs/Web/Guide/Localizations_and_character_encodings) the form can take like German, Cyrillic, Japanese, so forth. For most languages, including English this is "utf-8" as in: `<form accept-charset="utf-8">`. However, you don't have to set this property/attribute because it defaults to the character set/[Content Encoding](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Encoding) you have in the Head Element to set the character set of your page: `<meta charset="utf-8">`

* **rel=** - this gives you a place to give an annotation or explanation of the form is something is unclear. Most of the time you won't use this property.

<!-- ! END OF VIDEO 101.1.10.2 - Form Element Attributes -->

## Inputs

The Form element has many elements that go inside of it but, by far, the most common elements are the Label and Input Element:

```html
 <label for="password">Password</label>
 <input type="password" name="password" id="password" required>
```

This is because the Input element is a versatile element that can be used for all sorts of inputs from text and numbers to files and colors.

> NOTE: The HTML snippet above has a Label element with a `for` attribute set to `"password"`. In this way it is now tied to the Input element `id="password"` and NOT the `name` or `type` attributes. You see that? The label is `for` the `id` of the input.

The list below tells you most of the values you can give to the `type` attribute of an Input element.

`<input type="text">`: defines a one-line text input field. If you need a bigger area for lots of text you'll use a TextArea element.
`<input type="password">`: defines a password field.
`<input type="submit">`: defines a button for submitting form data.
`<input type="radio">`: defines a radio button.
`<input type="checkbox"`>: defines a checkbox.
`<input type="button">`: defines a button.
`<input type="date">`: creates a date selector
`<input type="color">`: provides a color picker wheel
`<input type="submit" value="Submit">`: creates a button that is registered automatically with its parent form element as a "submit" button AND it doesn't need a partner Label element.
`<input type="reset" value="Reset">` - creates a button that defaults to call the Form's `.reset()` method to clear all of it's fields.

<!-- ! END OF VIDEO 101.1.10.3 - The Input and Label Elements -->

### Other Attributes of the Input Element

**Form validation means we're verifying the data a user puts in, such as the type, length, validity, and shape we want so we can properly save it to a database.

> NOTE: Later in this full-stack program you'll see that data must be in the same format, or shape, as the other bits of data being saved with it else the computer can't read it. It is costly both in time and money to send the data from the user to our databases only for it to be in the wrong format. A shorter, safer, and cheaper first filter we can use is HTML's built-in form validation, and you've actually already seen one of the tools, `type`, which specifies the type of data that can go into an input.

We'll not cover them all in extreme detail because you'll have docs to reference later. But because you need a good introduction of **form validation** and some tools to do it, let's look at a few of the other attributes we can leverage on Input elements.

* `maxlength=`: limits the maximum number of characters that can go into the input
* `minlength=`: limits the minimum number of characters that can go into the input
* `max=` and `min=`: creates upper and lower limits on a data input
* `required`: forces the user to fill out the input
* `type="email"`: verifies that the input has a @ and .com
* `type="phone"`: verifies that it is a legit phone number
* `autocomplete="on"`: let's the browser offer autocompletion of the form
* `type="password"`: blots out the characters in this field automatically
* `placeholder=`: isn't a validation attribute but it does give the user a hint about what goes in the field

```html
 <label for="price">Price ($)</label>
 <input type="number" name="price" id="price" placeholder="$10.00" onkeyup="updateNewProduct(this)" min="1" max="100000" required>
```

* [MDN Docs - Input Element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input)

<!-- ! END OF VIDEO 101.1.10.4 - The Attributes of the Input Element -->

### Other Elements That Belong to the Form Element

Besides Input, there are a few other form elements you should know about but don't concern yourself with them *too much*. Remember, there are a lot of tools built into HTML that were developed over years of trial and error and there is no way for us to learn every detail to perfection right now. Take this as a very superficial survey of these other elements:

* `<fieldset>` & `<legend>`: The fieldset groups related data together and the legend acts the same way as the Label does for the Input. In this way, `<fieldset>` and `<legend>` always go together.
* `<textarea>`: As mentioned before, it is for large sections of text like this page you're reading now!!! ;)
* `<datalist>`: gives you a "pre-fill" menu for your inputs
* `<output>`: of course, shows you the output of some script you've built. You might try using this in your calculator app.
* `<select>`: offers a dropdown menu to your user.

The last thing we'll say about the HTML Form elements is that they can all be styled just like your other HTML elements. Have fun, let your creativity run wild, and enjoy building!!

* [MDN Docs - All Form Elements](https://developer.mozilla.org/en-US/docs/Web/API/HTMLFormElement/elements)

<!-- ! END OF VIDEO 101.1.10.5 - More Elements of the Form Element -->

<!-- TODO tell them the better way to handle submission is through the onclick -->

## Practice It - Forms

1. You have two projects to do in class. Go ahead and start on one of them now.
2. If you want something more to work with try fiddling with this [Example Form CodePen](https://codepen.io/austincoding/pen/awBGPx/).

Next class you'll be building a Contact Me Page & a Calculator. Look ahead to see the specifications for it and wireframe it tonight.

## Know Your Docs

* [MDN Docs - All Form Elements](https://developer.mozilla.org/en-US/docs/Web/API/HTMLFormElement/elements)
* [MDN Docs - Input Element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input)

## Additional Resources

* [YT, Richard Barkinskiy - Styling Form Elements](https://www.youtube.com/watch?v=2ACrHs5o9LM)]
* [YT, Web Dev Simplified - Learn HTML Form Elements](https://youtu.be/fNcJuPIZ2WE)
* [YT, InfoQ - Styling Form Validation Messages](https://youtu.be/bb4NqVycr-4)
* [CodePen, Code Snippet - Example Form Starter](https://codepen.io/austincoding/pen/awBGPx/)
