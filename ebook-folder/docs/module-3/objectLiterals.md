# Type Object-Literal

*“He who refuses to embrace a unique opportunity loses the prize as surely as if he had failed.“ – William James*

## Overview

<!-- ! Video Contents: 101 - Object-Literals (width="655" height="368", ratio 1.77) -->
<iframe src="https://player.vimeo.com/video/409877283" width="655" height="368" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen></iframe>

The reason we've held off teach JavaScript **Objects** until now is because in JavaScript, everything is a object: Strings, Numbers, Arrays, Functions, Arrays, and yes, Objects. This is also why we refer to everything as object-things, because they're all just chunks of data held within the program we're building.

So a pure JavaScript Object is a way to group multiple bits of data that are all related to one another. For instance, if we were cataloging types of trees for people to contribute to the [1 Trillion Tree Need](http://1t.org/) you might want to offer them things like:

* grow Zone
* Mature Height in feet
* Special Care
* Soil Type
* as well as name and catalogID

To offer an easier way to structure the data we'd need to display on the web page for them we wouldn't want an array because those are for lists, not necessarily related items.

```javascript
  const arrayOfTree = [{
    catalogID: 38,
    name: "American Beech",
    growZone: "4-9",
    matureHeightFT: 40,
    specialCare: "Full Sun",
    soilType: ["Acidic", "Clay", "Loamy", "Moist", "Sandy", "Well-drained"]
  },
    {
    catalogID: 81,
    name: "River Birch",
    growZone: "4-9",
    matureHeightFT: 70,
    specialCare: "Partial Shade"
    soilType: ["Acidic", "Clay", "Drought-Tolerant", "Loamy", "Moist", "Sandy", "Well-drained", "Wet"]
  },
    {
    catalogID: 90,
    name: "Northern Catalpa",
    growZone: 4-8,
    matureHeightFT: 60,
    specialCare: "Partial Shade",
    soilType: ["Acidic", "Alkaline", "Clay", "Drought-Tolerant", "Loamy", "Moist", "Rich", "Sandy", "Well-drained", "Wet"]
  }]
```

Above we see an array of three objects that each contain information on three different trees. We can loop over the object themselves but we cannot loop over the keys inside them. However, we can still access the values with dot-notation.

```javascript
  console.log(arrayOfTree[2].name) // => Northern Catalpa
  console.log(arrayOfTree[1].matureHeightFT) // => 70
```

If you're confused, think of them just like CSS, on the left-side of the `:` is the **key**/property and on the right-side is **value**.

<!-- ## Practice It -->

<!-- [Try it yourself](https://replit.com)! -->
<!-- [Try it yourself](https://codepen.io)! -->

## Additional Resources

TheNetNinja goes a little further than you need to know at this point in your career but at least you can see how an objects is created in the first 10 minutes.

- [ ] [YT, The Net Ninja - JS Tutorial 5: Objects](https://youtu.be/X0ipw1k7ygU)

## Know Your Docs

- [ ] [MDN Docs - Object Initializer](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Object_initializer)


<!-- ! END OF VIDEO 101.1.3.1 - TITLE-->
<!-- ? Video Numbering and Title system: CourseNumber.ModuleNumber.LessonNumber.VideoNumber -->
<!-- * (VIDEO 101.2.4.3 - "CSS Selectors") === 101 Course, Module 2, Lesson 4, Video 3 - "CSS Selectors" -->

<!-- 

```javascript

```

| Method      | Description                          |
| ----------- | ------------------------------------ |
| `GET`       | Fetch resource                       |
| `PUT`       | Update resource |
| `DELETE`    | Delete resource |


    `line numbers`
:do you like 'em?


++slash++
https://facelessuser.github.io/pymdown-extensions/extensions/keys/

=== "Javascript"

    ```javascript
    ```

=== "Python"

  ```python
  ```

=== "Example"
    ```console
      .
    ```

=== "Instructions"
    ```markdown
      .
    ```

=== "Result"
    ![PIC](./../images/pic.png)
-->