# HTML Project

## Questions for Discussion

BEFORE WE GET STARTED ARE THERE ANY QUESTIONS ABOUT THE HOMEWORK AND CLASS MATERIAL FROM DAY 1?

*Purpose: To introduce you to the concepts of web development with a fundamental understanding of what HTML is.*

*Objective: By the end of this lesson, you will be able to identify HTML as a language, as well as elements and tags with the language.*

Exercise: Quizlet Game, HTML Burger

## WHAT IS HYPER-TEXT MARKUP LANGUAGE (HTML)?

**HTML** is the standard mark-up language for creating web pages. The following are the main points about HTML:

* HTML stands for HyperText Markup Language
* HTML describes the structure of a web page
* An HTML document consists of a series of elements
* HTML elements tell the browser how to display the content
* HTML elements are represented by tags
* HTML tags label pieces of content such as “header”, “paragraph”, “list”, and so on
* Browsers do not display the HTML tags, but use them to render the content of the page

An **HTML Element** is defined by an **Opening tag**, some content, and a **Closing tag**:

```html
  <tagname>Content goes here...</tagname>
```

The HTML element is everything from the start tag to the end tag:

```html
<h1>My First Heading</h1>
<p>My first paragraph.</p>
```

| Start tag	Element content	End tag | Close Tag |
| - | - | - |
| `<h1>`	| My First Heading	 | `</h1>` |
| `<p>	`| My first paragraph	| `<p>` |
| `<br>`	| none | none |

> NOTE: Some HTML elements have no content (like the `<br>` element). These elements are called empty elements or **void elements** because they are *void* of content. Empty elements do not have an end tag!

### Nesting

HTML elements can be nested (this means that elements can contain other elements).

All HTML documents consist of nested HTML elements.

The following example contains four HTML elements (`<html>`, `<body>`, `<h1>` and `<p>`):

=== "HTML Nested Elements Example"

```html
<!DOCTYPE html>
<html>
<body>

  <h1>My First Heading</h1>
  <p>My first paragraph.</p>

</body>
</html>
```

> The `<html>` element is the root element and it defines the whole HTML document.
> It has a start tag `<html>` and an end tag `</html>`.
> Then, inside the `<html>` element there is a `<body>` element:

```html
<body>

  <h1>My First Heading</h1>
  <p>My first paragraph.</p>

</body>
```

The `<body>` element defines the document's body.

It has a start tag `<body>` and an end tag `</body>`.

Then, inside the `<body>` element there are two other elements: `<h1>` and `<p>`. These could be called **Child Elements** of the Body. Which means the Body element could be called a **Parent Element**

```html
  <h1>My First Heading</h1>
  <p>My first paragraph.</p>
```

The `<h1>` element defines a heading.

It has a start tag `<h1> `and an end tag `</h1>`:

```html
<h1>My First Heading</h1>
```

The `<p>` element defines a paragraph.

It has a start tag `<p>` and an end tag </p>:

```html
<p>My first paragraph.</p>
```

Some HTML elements will display correctly, even if you forget the end tag. This is because the language and browsers were built to handle a little developer-error...

```html
 EDIT
 Set Access Duplicate Move Delete 
<html>
<body>

  <p>This is a paragraph
  <p>This is a paragraph

</body>
</html>
```

> However, **never rely on this!** Unexpected results and errors may occur if you forget the end tag!

### EMPTY HTML ELEMENTS

HTML elements with no content are called empty elements.

The `<br>` tag defines a line break, and is an empty element without a closing tag.

```html
<p>This is a <br> paragraph with a line break.</p>
```

### Not Case Sensitive

HTML tags are not case sensitive: `<P>` means the same as `<p>`.

The HTML standard does not require lowercase tags, but W3C recommends lowercase in HTML, and demands lowercase for stricter document types like XHTML.

| Tag	| Description |
| - | - |
| `<html>` | Defines the root of an HTML document |
| `<body>` | Defines the document's body |
| `<h1>` through `<h6>`  Defines HTML headings |