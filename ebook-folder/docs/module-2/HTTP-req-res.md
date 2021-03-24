# Pre-Class Lesson 2: HTTP Req/Res + HTML Elements as our Building Blocks/Objects

A few days ago we learned about Objects, Object Modeling and Code as Communication let's now look at how computers communicate through HTTP(s) and why & how that informs the way our web pages are built the way they are. For this lesson, let's back away from the code and take a slower and higher approach to understanding how our web pages are built and delivered.

## Request and Response Objects: The High Overview

Again everything to a computer is an *object*. And we can visualize those objects with Object Modeling. With this in mind, let's now envision your web browser (Chrome, Safari, etc...) navigating to a URL. This act of *navigation* is actually a **request** for information or resources that are sitting at unique addresses in the internet, just like a street address for a house or building. All devices and files on the internet have a unique address we call a [URL, Unique Resource Locator](https://en.wikipedia.org/wiki/URL). So when you "Live Serve" your web pages you use a program to create a mini-internet on your computer and serve that web page at a URL called `localhost:5500` as in, your computer is the `localhost` and the exact address/port it's using is `5500`. This is the exact same process when you navigate to a website on the the real internet. Large computers are holding files at specific addresses(URLs) in the internet and giving them to browsers when they request those files/resources. And this is where we'll begin to explore **requests** and **response** objects as they relate to the way our web pages are built.

<!-- ! END OF VIDEO 101.1.2.1 - The High Overview of Req/Res -->

<!-- ? Video Numbering and Title system: CourseNumber.ModuleNumber.LessonNumber.VideoNumber -->
<!-- * VIDEO 101.2.4.3 - "CSS Selectors" === 101 Course, Module 2, Lesson 4, Video 3 - "CSS Selectors" -->

### The Head and Body

While we won't get into the deep details of these two object in this course we will need to understand the basic gist of these objects to make better sense of our files and why they're arranged the way they are. You'll need paper and pen to continue this section.

**Here's the gist: When a computer makes a request or a response it sends them both in the exact same shape: an object with a head and a body.**

> Title this drawing: "Req/Res"
> Go ahead and draw a computer on the middle-left-side of your page (that's your computer)
> Now draw another computer on the middle-right-side of your page (that's a server/the "Cloud")
> Now draw an arrow from your computer to the server labeled "request"
 > Below that arrow draw a box, then draw a line cutting that box in half horizontally.
 > Label the top half of the box "Head"
 > And the bottom half of the box is "Body"
> You can now draw an arrow from the server computer to your computer and label that "response"
 > Draw another box, cut it in half, label them "Head" and "Body"

The drawing you should have is the premise of how the internet works and the basis for everything we will learn in the next few months. All data exchanges are just requests and response objects with two other objects inside of them called **Head** and **Body**. In the **Head** object there is what we call **metadata**. Or just simply, bits of information that tell the receiving computer something about the contents of the **Body** of the request or response object. And the **Body** object is the actual content of the **request** or the **response**.

When you navigate to a page your browser sends a request object that has a property called `method` and its value is `get` as in, get whatever resources are at this address while the body is empty because there's nothing for your browser to send. When the computer in the "Cloud" receives your request it will put together a response object. In this response object, there will be some metadata in the Head like `title`, `charset`, and `styles`. This is information the browser needs to properly render the content in the Body. Take a look at the page you built a few days ago. Notice any similarities?

```html
<!-- index.html -->
 
<!DOCTYPE html>
 <html lang="en">
   <head>
     <meta charset="UTF-8">
     <meta name="viewport" content="width=device-width, initial-scale=1.0">
     <meta http-equiv="X-UA-Compatible" content="ie=edge">
     <link rel="stylesheet" href="./style.css">
     <title>My Portfolio</title>
   </head>
   <body>
    
   </body>
 </html>
```

In the code above we see a `head` object and a `body` object. These two objects/elements represent in the HTML language/code the same **Head** and **Body** objects of our Response object and they serve the same purpose, the Head describes needed information about the content in the Body. But for now, we're going to have to set aside our short exploration of Request and Response objects in HTTP(S) protocol because we don't need to know their details to build web pages and websites. All we really need to know is that this code represents the response object. Plus, we'll be learning and using the finer details of requests and responses in our 311 course: Servers and Databases.

What we'll do with this information now, though is to assume when we navigate to a URL the **Response** object we get back is the code you see above, from `<!DOCTYPE html>` to `</html>`. In this course, 101: Intro to the Web, we're be building the contents of the **Body Object** of the Response Object so that when other people's browsers navigate to our URL they will get the web page we built. Look back at your Req/Res drawing to know where you are and let's get into some code.

* [W3S Docs - HTTP, Request/Response](https://www.w3schools.com/whatis/whatis_http.asp)

<!-- ! END OF VIDEO 101.1.2.2 - The Head and Body -->

## Know Your Docs

* [W3S Docs - HTTP, Request/Response](https://www.w3schools.com/whatis/whatis_http.asp)
