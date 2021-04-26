# Let's Write Some Code

## HTML is for Content

We use HTML to insert our content into the page. Text, images, video, forms, PDFs, etc... are all created by the HTML tags we use.

Some tags like **Header**, **Main**, and **Footer** are used to group together multiple pieces of content.

Let's create a Main tag to hold all of the content. Be sure to follow along in CodePen. It looks like this:

```html
  <main id="box">

  </main>
```

Our `<main>` opening tag looks a little different because we added an `id=` **property** to it.

**ID**s are like labels we put on our HTML tags. We can use these labels in CSS and JavaScript to 'select and affect' the contents in the HTML later.

Inside the **Main** tag, let's create an **H1** tag and give the page a title with it:

```html
<main id="box">
  <h1>SurfCity.io - Coming Soon</h1>
</main>
```

The title looks good, so now we need to create the structure for our countdown clock. We are going to do that by creating a series of four **Span** tags. The Span tag is usually used to wrap around bits of text that we want to change using CSS or JavaScript. In this case we are going to use JavaScript to make the countdown timer, and we need to update the contents of these span tags once every second.

  > Notice the new **ID**s we are adding. It's important to note that IDs like these have to be typed exactly as we show them here. Typos, or making the first letter upper-case *instead of lower-case* will confuse the browser and it will not work.

=== "the HTML"

    ```html
    <main id="box">
      <h1>SurfCity.io - Coming Soon</h1>

      <span id="days">0 days</span>
      <span id="hours">0 hours</span>
      <span id="minutes">0 minutes</span>
      <span id="seconds">0 seconds</span>
    </main>
    ```

=== "the Result"

    ![surfIO-countdown-page-title](./../images/surfIO-countdown-page-title.png)

Now we're going to add two more tags. A **br** tag which adds a **line-break** to force the following content onto the next line, and a **p** tag. The `p` stands for paragraph and is designed to hold multiple lines of text.

We will use this space to ask if our users would like to join the mailing list.

=== "the HTML"

    ```html
    <main id="box">
      <h1>SurfCity.io - Coming Soon</h1>

      <span id="days">0 days</span>
      <span id="hours">0 hours</span>
      <span id="minutes">0 minutes</span>
      <span id="seconds">0 seconds</span>

      <br>
      <p>
        Would you like to be notified when we go live?
      </p>
    </main>
    ```

<!-- === "the Result"

  ![surfIO-countdown-page-](./../images/surfIO-countdown-page-.png) -->

Now we come to the **Form** tag. Every time you've given your email address, logged in to an account, bought something with a credit card, or filled out a survey online, you've done it in a **Form** tag.

**Form** tags are how we accept information from our users and they are critically important to most web sites. The form is just a content container though, and inside the container we can design it to look any way we like, but in order to accept data from the user, we need to add at least one **Input** tag.

=== "the HTML"

    ```html
    <main id="box">
      <h1>SurfCity.io - Coming Soon</h1>

      <span id="days">0 days</span>
      <span id="hours">0 hours</span>
      <span id="minutes">0 minutes</span>
      <span id="seconds">0 seconds</span>

      <br>
      <p>
        Would you like to be notified when we go live?
      </p>

      <form>
        Email:

      </form>
    </main>
    ```

=== "the Result"

    ![surfIO-countdown-page-form](./../images/surfIO-countdown-page-form.png)

There are a variety of different types of data that a form can accept, and the tag we use to do it is called an **Input** tag. Inside the **Input** tag is a property called `type=`. Changing the type property changes what kind of data the input accepts, and we need the user to give us an email, so we will use `type="text"`.

The second input is a little different. It has its `type` property/attribute set to `submit`. This will create a button input element that will be used to trigger a submission function on the Form Element it's inside.

  > Notice: we also give Input elements a `name=` property. This gives us a way to access the value stored in that input via thing called a **key**. This input's **key** will be `email` and its **value** will be whatever the user inputs. You'll here the term **key:value pairs**; this describes the relationship of these pieces of data.

=== "the HTML"

    ```html
    <main id="box">
      <h1>SurfCity.io - Coming Soon</h1>

      <span id="days">0 days</span>
      <span id="hours">0 hours</span>
      <span id="minutes">0 minutes</span>
      <span id="seconds">0 seconds</span>

      <br>
      <p>
        Would you like to be notified when we go live?
      </p>

      <form>
        Email:
        <input type="text" name="email">
        <input type="submit" name="submit" value="Submit">

      </form>
    </main>
    ```

=== "the Result"

    ![surfIO-countdown-page-formWithEmailInput](./../images/surfIO-countdown-page-formWithEmailInput.png)

Ok, we're almost done with the HTML, but our friend, the client, just called to say we need to include links to their social media... He doesn't have the links yet because some of the accounts are still being created, but that's OK. We can include an image for now and add the link later when it's available.

The Img tag just needs the `src=` property filled in with a URL so that it knows where find the image.

That's it! We're done with the HTML. It still looks a little plain...let's learn how to use CSS to transform the look of it!!

=== "the HTML"

    ```html
    <main id="box">
      <h1>SurfCity.io - Coming Soon</h1>

      <span id="days">0 days</span>
      <span id="hours">0 hours</span>
      <span id="minutes">0 minutes</span>
      <span id="seconds">0 seconds</span>

      <br>
      <p>
        Would you like to be notified when we go live?
      </p>

      <form>
        Email:
        <input type="text" name="email">
        <input type="submit" name="submit" value="Submit">

      </form>
    </main>

    <div id="social">

      <img src="https://assets.codepen.io/1240556/social.png" />

    </div>
    ```

=== "the Result"

    ![surfIO-countdown-page-social-media-icons](./../images/surfIO-countdown-page-social-media-icons.png)

