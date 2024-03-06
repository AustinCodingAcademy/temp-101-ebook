# CSS is for Looks

CSS works by **selecting & effecting** the HTML content, from basic things like text color to more advanced techniques for placing content on the page you will always **select** an element and then write rules to **effect** the element.

You can target and select HTML in a number of ways but today you're going to use the **tag name** and the **ID** name methods.

## Selecting + Effecting

Let's start by selecting the ID `box`. If you look in your HTML you'll see that the `box` ID is applied to the `main` element holding all our content. To select an ID in CSS always start with a `#` in front of the ID name. 

```css
#box
```

Then, you create a **declaration block** by hitting the space bar and adding the `{}` syntax. 

```css
#box {}
```

You'll write the **rules** you want the HTML to follow inside of these curly-braces `{}`. 

```css
#box {
  border-color: blue;
  border-width: 15px;
  border-style: solid;
}
```

These **rules** are made up of two parts: a **property** and a **value** which are separated by a colon `:`. The **property** is a part of the element that can be changed and all HTML elements have *mostly* the same properties. The **value**, on the other hand, is something you decide to give it as long as it's a **valid value**, i.e. a measurement must be in `px;`, `%;`, or `em;` while a color must be in text (`purple;`) or hexadecimal form (`#e942f5;`) and so forth.

> NOTE: **Valid values** can be found in the documentation of the [CSS Properties at W3Schools](https://www.w3schools.com/cssref/index.php).

The rules you write inside the declaration block will be applied to the HTML element that was selected in-front of the declaration block.

=== "the CSS"

    ```css
    #box {
      border-color: blue;
      border-width: 15px;
      border-style: solid;
      border-radius: 25px;
    }
    ```

=== "the Result"

    ![surfCity-io-example-blue-border](./../images/surfCity-io-example-blue-border.png)

## Align & Margin

The next thing we want to do is align some of the content. To this, we'll add another property to our `#box` rule declaration block. This one is `text-align: center;`.
  
  > We always want to remember to add the `:` and the `;` when adding properties. The part on the left of the `:` tells the browser what to change, the part on the right tells it how to change it, and the `;` tells the browser when the rule is completed.

Next, let's center our container by adding, `margin: auto;`. This tells the browser to put an equal amount of space on either side of the container.

While we are centering things, let's center that image container we added in HTML. The Img container has an ID of `social` on it. In order to center it, we need to set its width to be less than its parent's width, the `main` container, and add another `margin: auto;`:

=== "the CSS"

    ```css
    #box {
      border-color: blue;
      border-width: 15px;
      border-style: solid;
      border-radius: 25px;
      text-align: center;
      margin: auto;
    }


    #social {
      width: 500px;
      margin: auto;
    } 
    ```

=== "the Result"

    ![surfCity-io-example-margin](./../images/surfCity-io-example-margin.png)

## Font

The next thing we want to do is set a specific `height` and `width` on the `#box` container. Let's set it to `width: 500px;` and `height: 200px;`

After that, let's change the font. If you don't specify which font to use, the browser will just use a [default font](https://www.granneman.com/webdev/coding/css/fonts-and-formatting/web-browser-font-defaults). Telling the browser what font to use is a little tricky because not all machines have the same fonts installed. We could tell the browser to download a font, but instead we are just going to assign a category and let the browser pick its default one of that category. We do that with the following key/value pair: `font-family: cursive;`

=== "the CSS"

    ```css
    #box {
      border-color: blue;
      border-width: 15px;
      border-style: solid;
      border-radius: 25px;
      text-align: center;
      margin: auto;
      width: 500px;
      height: 200px;
      font-family: cursive;
    }
    ```

=== "the Result"

    ![surfCity-io-example-width](./../images/surfCity-io-example-width.png)

## Background

Let's add a little more color by setting the `background` of the `body` to `red`. The whole visible area in the browser is inside the body. To change its background color, we add `background: red;`

Next we want to clean up some of the spacing and formatting in the `#box` container. We'll do this by changing some font sizes and margin spacing. We're adding a new type of measurement here, the `em`. The `em` is similar to the pixel(`px`), but it's a relative measurement and helps the browser resize the text on different screen sizes.

=== "the CSS"

    ```css
    body {
      background-color: red;
    }

    h1 {
      font-size: 2.2em;
      margin-top: 10px;
      margin-bottom: 0;
    }

    span {
      font-size: 1.5em;
    }
    ```

=== "the Result"

    ![surfCity-io-example-background](./../images/surfCity-io-example-background.png)

The black text on the red background is a little harsh. We could change the font color, but instead, we are going to change the background of the `#box` container. We just saw how we can change the background to a specific color, but we can also change it to a pattern. Creating these pattens can be complicated, but fortunately, someone has created a bunch of them and shared the code with us. You can find them by going to this website [CSS3 Patterns Gallery](http://lea.verou.me/css3patterns/).

Scroll down until you see a pattern called "Wave" and click it. This will bring up the code, and you can copy the code/paste it into the `#box` rule as shown below.

=== "the CSS"

    ```css
    #box {
      border-color: blue;
      border-width: 15px;
      border-style: solid;
      border-radius: 25px;
      text-align: center;
      margin: auto;
      width: 500px;
      height: 200px;
      font-family: cursive;
      background: linear-gradient(#ffffff 50%, rgba(255,255,255,0) 0) 0 0,
    radial-gradient(circle closest-side, #FFFFFF 53%, rgba(255,255,255,0) 0) 0 0,
    radial-gradient(circle closest-side, #FFFFFF 50%, rgba(255,255,255,0) 0) 55px 0 #48B;
      background-size: 110px 200px;
      background-repeat: repeat-x;
    }
    ```

=== "the Result"

    ![surfCity-io-example-wave-patterns](./../images/surfCity-io-example-wave-patterns.png)

## JS is for Interactivity

The last thing we need to do is make the countdown clock work. Writing JavaScript is a little more complicated than CSS or HTML, but you did a quick Google search and [found that someone else had written the code already](https://stackoverflow.com/questions/20618355/how-to-write-a-countdown-timer-in-javascript) and like the CSS background patterns, they have shared the code for other developers to use and learn from.

Copy the code from below and paste it into the JS window in your CodePen. And with that working, we are ready to show it to our friend (the customer/client)

=== "the JS"

    ```js
    // this is a "comment". Any characters after the "//" symbols are ignored by the computer.
    // The following line of code will create an object that will hold a date in the future
    const targetDate = new Date();

    // logs out the value of targetDate to the console which is the current date.
    console.log("targetDate is: " + targetDate) 

    // Adds 30 days to that date
    targetDate.setDate(targetDate.getDate() + 30) 

    console.log("the new targetDate is: " + targetDate)

    // create units of time for the computer to calculate with & save them in variables
    const second = 1000;
    const minute = second * 60;
    const hour = minute * 60;
    const day = hour * 24;

    // set up a loop to update the countdown clock every second
    const calculateTimeAndUpdateCountdownDisplay = setInterval(function() {

    // get & store the current time
    const now = new Date().getTime();

    // get & store the remaining time
    const distance = targetDate - now;

    // update each <span> tag with the corresponding countdown values
    document.querySelector('#days').innerHTML = Math.floor(distance / (day))+" days, ";
    
    document.querySelector('#hours').innerHTML = Math.floor((distance % (day)) / (hour))+" hours, ";
    
    document.querySelector('#minutes').innerHTML = Math.floor((distance % (hour)) / (minute))+" minutes, ";
    
    document.querySelector('#seconds').innerHTML = Math.floor((distance % (minute)) / second)+" seconds ";
    }, second)
    ```

=== "result"

    <iframe src="https://giphy.com/embed/9orov3qualQiJAPHRb" width="300" frameBorder="0" class="giphy-embed" allowFullScreen></iframe>


> HINT: click the console button at the bottom left of your CodePen screen to see the logs of this script.

Now **delete line 9** and **change line 3** to use your birthday as the future date, i.e. `const targetDate = new Date("October 20, 2025);`

## Additional Resources

- [ ] [Reference, granneman.com - Web Browser Font Defaults](https://www.granneman.com/webdev/coding/css/fonts-and-formatting/web-browser-font-defaults)
- [ ] [Reference, lea.verou.me - CSS3 Patterns Gallery](http://lea.verou.me/css3patterns/)