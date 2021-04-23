{% include "../includes/header.md" %}

# Portfolio Landing Page

*A journey of a thousand miles begins with a single step. – Lao Tzu* 

## Overview

<!-- @TODO @CLAYTON ADD OVERVIEW video to first portfolio piece, why an how. more pages than just index -->
Today you are going to build your first website! I think you'll get the hang of it quickly, you're already an HTML and CSS pro. But if you don't feel it, don't worry. If all you do is get a page up on in your browser that says, "Hello World" then you've got a great start. Whatever page you build today and get up with live-server through VS Code, we'll get hosted for the world to see on your first day of class!

## Today's Checklist

<!-- This is for their personal navigation through the project. They can go through and make sure they get each thing and can comb over it later.  -->

**HOW CLASSES WORK**

*Each class throughout the program will come with the following "checklist". The checklist will give you an idea of the general flow of class as well as key points and topics so that you know what to expect before diving in.*

1. Create directory/folder called: `myPortfolio` in either your documents folder or your desktop folder.
2. Create your `index.html` file
3. Build your first webpage using HTML
4. Link a CSS file
5. Copy/Paste CSS code into that css file
6. Experiment with CSS on your own
7. Build a "hero" style landing page by the end of class
<!-- 8. Write & publish your first blog post -->

******

## The Hero Landing Page Objective

<!-- In this section we tell the students what they will achieve by the end of the class. For us its a way to set up a goal and reverse engineer it.  -->
The [Hero Landing Page](https://www.justinmind.com/blog/10-inspiring-hero-image-websites/) is a trend in aesthetic web design. The goal of the hero landing page (or hero image) is to instantly capture the user's attention and shape their opinion of the website before they even begin to look at the content on the site. This is extremely important on the web. It takes [approximately 50 milliseconds](https://cxl.com/blog/first-impressions-matter-the-importance-of-great-visual-design/) for users to form an opinion about a website that determines whether they’ll stay or leave – so your hero image better be good!

In this section you're going to be building your first web page in the "Hero" style! This page will be a jumping off point for you to build a "portfolio website" where you can hook-in, store, and show-off all of the cool apps, games, and widgets you build in this course, the next courses, and beyond!

As a future web developer you **must, must, must** have a portfolio site when you are looking for work! It is absolutely required! Your portfolio page is an opportunity to show off your skills to potential employers, present your projects, and communicate your personality. And so, in this first project you will not only be learning the ropes by building your first site, but you'll also start creating version 1 of the portfolio site that you'll one day show to the world! Remember, you're going to be looking to be hired by tech companies who have considerable experience in the interwebs and have no qualms about google searching your name or clicking on your profile page. Therefore, your web presence must be on *fleek*!

### Project Instructions

<!-- There should be clear step by step instruction so the material can be asynchronously consumed. This will significantly help our students learn, review and improve your teaching experience.  -->

#### Create Your Folder and File Structure

1. Inside your documents or desktop folder create a folder called `myPortfolio`.
1. Open VS Code (Your text editor).
1. In the top-left, click "file" and then "open" to find the new folder that you just created.
1. Using VS Code, create a new file inside of your folder called `index.html`.
1. Open that `index.html` file up and paste in the code you see on this [htmlExample](../codeSnippets/htmlExample.md) page.

> *NOTE: Don't worry too much about what each of these lines of code mean for right now. There's plenty of time to figure that out later. For now, we'll just build a web page.*

1. Save. *(CMD + s)*

#### Build The Index File

A **wireframe** is, "an image, or set of images, which displays the functional elements of a website or page, typically used for planning a site's structure and functionality". In other words, a wireframe is the blueprint of a website. You'll be using the wireframe throughout this course and your career. It's the plan for your codebase!!

1. Take a look at the "wireframe" below.

      ![landingPage-Wireframe](../images/webPage2.png)

    <!-- 1. **As we move forward, notice there are abbreviations throughout these instructions that look like this: `<nav/>` or `<button/>`**
        * **These are simply short-hand/pseudo code to represent the opening & closing tags of an element:**
          * **`<nav />`** = `<nav></nav>`
          * **`<button />`** = `<button></button>`
        * **Make sure that you are typing the correct tags when building your page and see these "self-closing" tags only as abbreviations.** -->

2. Build two elements inside the **body** tag called **header** and **main**. Go ahead and copy/paste the code below to get started.

    *NOTE: Remember to reference you previous lessons and bookmarked docs while doing this. And be sure you only have ONE **body** tag.*

    ```html
    <!-- Don't include this <body> tag, it's for reference only -->
    <!-- <body>  -->
      <header>
      <!-- REPLACE THIS LINE WITH THE PROVIDED IMG TAG -->
      <!-- REPLACE THIS LINE WITH A NAV ELEMENT, STEP 5-->
      </header>
      <main>
        <!-- REPLACE THIS LINE WITH YOUR HEAD SHOT IMG TAG, STEP 6-->

        <!-- REPLACE THIS LINE WITH THE PORTFOLIO BUTTON, STEP 9  -->
        <a class="small-text" href="https://austincodingacademy.com/">© Austin Coding Academy</a>
      </main>
    <!-- </body> -->
    <!-- Don't include this </body> tag, it's for reference only -->
    ```

3. Inside the **header** element paste in this line of code:

    ```html
    <img src="https://cdn.evbuc.com/eventlogos/188084824/acastandardcirclefullname.png" class="logo" alt="austin coding academy logo">
    ```

    *You don't have to know, but can you imagine what this line does? What does it do?*

4. **NEXT**, below that code but still inside the **header** tag, build a **nav** element.
5. Inside this **nav** element create 4 **anchor** tags for each of the following: "Resume", "About Me", "My Blog", "Contact Me"
    * The anchor tag for "Contact Me" should look like this: `<a class="has-border">Contact Me</a>`
6. In between the **main** tags paste in this line of code: `<img src="./myProfilePic.jpg" id="profile-pic" alt="Head shot of Me">`
7. Then go to your finder/file explorer on your computer and open two separate windows in your computer.
    * In one of the the windows find a good, clear, professional picture of yourself.
    * In the other window, navigate the the `myPortfolio` folder this project is in.
    * Then drag the image of yourself from one window into the "myPortfolio" directory in the other window.
    * Then rename the image `myProfilePic.jpg` *Note: if your image is a .png, .jpeg or other simply change the suffix in the line of code from **Instruction 6**.*
8. Still inside the **main** element but below this new **img** tag create an **h1** element with your full name in it. And below it, create an **h2** element with your current title: *Student of Web Development*.
9. Below that create a **button** element: `<button id="portfolio">Portfolio</button>`.
10. If you haven't already, in VS Code, click the squares on the left-side and install live-server. [Live-Server Instructions](https://www.youtube.com/watch?v=8pOv1V4w3N8).
11. Save your code, restart VS Code, and fire up your *live-server* using the "Go Live" button at the bottom right of VS Code.
    
    *NOTE: If the button doesn't show up right away, try quitting VS Code and restarting it. Or uninstall Live-Server and reinstall then restart VS Code again.*
    
    >*NOTE 2: Another reason (rarely) you may see is that you're not in a "Workspace", simply open your `myPortfolio` in a new workspace.*

12. Go check out your website in Chrome, localhost:4000.
13. Not matching your wireframe?? Yeah that's okay. You see, *[normal document flow](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Normal_Flow)* says that each element will be read top-to-bottom and left-to-right in the file and rendered on the screen top-to-bottom and left-to-right.

#### Adding Style

1. To fix this we're going to attach a set of rules listed in a **css** file to make everything look pretty.
2. Look in the **head** tag at the top of your **index.html** file. Do you see the `<link rel="stylesheet" href="./style.css">`? That line of code is going to allow you to link styles to the otherwise very boring website. The line is actually telling the browser to go find a file called: `style.css` but we haven't created the file for it to find yet...
3. On the left side of VS Code click on your directory: `myPortfolio`, then click the icon that creates a new file and name it: "style.css"
4. Inside that new file copy/paste the following code:

    ```css
    body {
      font-family: Arial, Helvetica, sans-serif;
      background-image: url(https://png.pngtree.com/thumb_back/fh260/back_pic/00/15/30/4656e81f6dc57c5.jpg);
      background-repeat: no-repeat;
      background-size: 1600px 1000px;
      width: 100vw;
      height: 100vh;
    }
    /* What kind of selector is this? */
    .logo {
      width: 150px;
      height: 100px;
      margin: 3% 10%;
    }

    header {
      display: grid;
      grid-template-columns: 40% 60%;
      width: 100%;
    }

    main {
      height: auto;
      width: 100%;
      display: grid;
      grid-template-columns: 30% 40% 30%;
    }

    /* This is an element within and element selector */ 
    nav > a {
      margin: 2% 1% 3%;
      height: 10%;
      width: 15%;
      color: white;
      font-family: Arial, Helvetica, sans-serif;
      font-size: 20px;
      border-radius: 25px;
      background: transparent;
      padding: 20px;
      text-align: center;
      border: 2px solid white;
    }

    .has-border {
      border-radius: 25px;
      border: 2px solid #0795C3;
      background: none;
      padding: 20px;
    }

    nav {
      display: flex;
      justify-content: flex-end;
      width: 100%;
      padding-right: 2%;
    }
    /* This is an ID selector */
    #profile-pic {
      width: 300px;
      height: 300px;
      border-radius: 50%;
      margin: 15% auto;
      grid-column: 2/3;
    }

    h1 {
      color:white;
      grid-column: 2/3;
      margin: 3% auto;
      border-bottom: 2px solid #1940A9;;
    }

    h2 {
      grid-column: 2/3;
      margin: 3% auto;
      font-style: italic;
    }

    .small-text {
      grid-column: 2/3;
      color: white;
      font-size: 10px;
      margin: 3% auto;
    }

    button {
      grid-column: 2/3;
      margin: 3% auto;
      width: 70%;
      height: 15%;
      font-family: Arial, Helvetica, sans-serif;
      font-size: 20px;
      border-radius: 25px;
      background: transparent;
      padding: 20px;
      padding-bottom: 5%;
      text-align: center;
      color: white;
      letter-spacing: 16px;
      font-style: italic;
    }
    ```

    *Now it's playtime*

5. Save your file and then go back to your browser to see what happened.
6. What happened? Is it all working?
7. If so, read through and see if you can figure out how to change the background `img` to something you like better.
8. Can you figure out how to change the color of the links at the top?
9. What about the logo at the top-left?
10. **Finally:** Fix any bugs you have and get excited about playing with stuff.

This is how you will be learning from here on out! Playing, breaking, fixing, playing, breaking and fixing again! Don't be afraid to change colors, text sizes, font families – whatever! You can always *undo*.

> *NOTE: As you learn you will be pushing into unfamiliar territory. This will be your job! To push the boundary, experiment, and come up with solutions to problems. Embrace this learning, love the bugs, find joy in squashing them and you will do well!*

### Follow-up Video

<!-- VIDEO FOR FIRST WEBSITE -->
<iframe src="https://player.vimeo.com/video/389053330" width="640" height="360" frameborder="0" allow="autoplay; fullscreen" allowfullscreen></iframe>
******

## Review and Further Practice

<!-- Link to a challenge to use the same skill but in a different project that doesn't have step-by-step instructions. This is for the more advanced students and for students to continue practicing btw, during and after sessions.  -->

*Every lesson in this book will end with a **Review and Further Practice** Section. These sections are here to help you push yourself further once you've completed the in-class assignment. You should never stop coding or think you can't do or learn more. So to help guide you forward, these sections are given as highly-recommended suggestions on what you should code next. Take advantage of them and don't be afraid to Google your way through the challenges*

1. Play with the properties and other values in the css file to see what they are changing on the page. Don't be afraid to break things. Just click undo! If you feel like you've made a mess, remember that you have all of the original code here within this assignment.
1. Google each of the properties in the CSS file like `margin`, `font-family`, `text-align`, `color` and so forth.
1. Learn new values for each of those properties.
1. **Don't be afraid to break things.** You can always come back and fix them. Just come back to these instructions!
1. See what else you can change and really get this page customized to your tastes. We'll learn more about CSS later on, but you should start experimenting and playing with it now.
1. [Learn more](https://www.youtube.com/watch?v=6dzpt1_y0CA) about your editor. *Side-Note: Hitesh is an awesome youTuber for coding.*
1. Use these pages for inspiration:

![bio-1](../images/bio-1.png)
![bio-2](../images/bio-2.png)

******
******

<!-- ## Go to [Day 1 Pre-Homework - What is Git >](../01Week/01DayPrep.md) -->

{% include "../includes/footer.md" %}
