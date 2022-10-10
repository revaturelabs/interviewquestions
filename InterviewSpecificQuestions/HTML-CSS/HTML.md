1. What is a `<meta>` tag in HTML5?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- The `<meta>` tag offers metadata about the HTML5 document. This metadata is machine-parsable. Typically, meta elements are used for specifying:
   - Author name
   - Keywords
   - Page description

- The metadata supplied by the `<meta>` tag is used by:
   - Web browsers to know how to display content or reload a web page
   - Search engines to know about keywords on a web page
   - Other web services

</blockquote>
</details>

---

2. Is it possible for a web page to have multiple `<header>` and `<footer>` elements?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Yes, a webpage can have many `<header>` and `<footer>` elements. Both tags are specifically designed to serve their respective purposes with respect to their parent section.

Hence, not only the page `<body>` must have the `<header>` and `<footer>` tags, but also does every `<article>` and `<section>` elements. Although a `<footer>` element might not be always necessary for every `<article>` and `<section>` tags, a `<header>` element must always be there.

</blockquote>
</details>

---

3. What is an iframe and how it works?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

An iframe is an HTML document which can be embedded inside another HTML page 
**Example:**

```HTML
<iframe src="https://github.com" height="300px" width="300px"></iframe>
```

</blockquote>
</details>

---

4. How do you set language in HTML?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

There are multiple ways to set language in HTML
  - By setting content-language in headers for language of the page.
  - By setting accept-language in headers for list of language that a page accept.
  - Setting lang attribute in html tag.

**Example:**

```HTML

<!DOCTYPE html>
<html lang="en">
<head>
  <title>Document Title</title>
</head>
<body>

</body>
</html>

```

</blockquote>
</details>

---

5. What does a `<DOCTYPE html>` do?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

A **DOCTYPE** is always associated to a DTD ( Document Type Definition ). A DTD defines how documents of a certain type should be structured (i.e. a button can contain a span but not a div), whereas a **DOCTYPE** declares what DTD a document supposedly respects (i.e. this document respects the HTML DTD). For webpages, the **DOCTYPE** declaration is required. It is used to tell user agents what version of the HTML specifications your document respects.

Once a user agent has recognized a correct **DOCTYPE**, it will trigger the no-quirks mode matching this **DOCTYPE** forreading the document. If a user agent doesn't recognize a correct **DOCTYPE**, it will trigger the quirks mode.

</blockquote>
</details>

---

6. What is difference between span **tag** and **div** tag?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The primary difference between div and span tag is their default behavior. By default, a `<div>` is a block-level-element and a `<span>` is an inline element.

`<div>` is a block level element which means it will render it on it's own line with a width of a 100% of the parent element.
`<span>` is an inline element which means it will render on the same line as the previous element, if it is also an inline element, and it's width will be determined by it's content.

```HTML
<div>Demo Text, with <span>some other</span> text.</div>
```

</blockquote>
</details>

---

7. What is the purpose of `<main>` element?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The HTML `<main>` element represents the dominant content of the `<body>` of a document. The main content area consists of content that is directly related to or expands upon the central topic of a document, or the central functionality of an application.

```HTML
<main role="main">
    <p>Geckos are a group of usually small, usually nocturnal lizards. 
       They are found on every continent except Australia.</p>
    <p>Many species of gecko have adhesive toe pads which enable them to climb walls and even windows.</p>
</main>
```

**Note:** A document mustn't have more than one `<main>` element that doesn't have the hidden attribute specified.

</blockquote>
</details>

---

8. When should you use section, div or article?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

If the content within the element is not semantically related, then use a `<div>`. If the semantically related content is also able to be self-contained, then use an `<article>`. Otherwise, use a `<section>`.


</blockquote>
</details>

---

9. Can a web page contain multiple `<header>` elements? What about `<footer>` elements?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Yes both of these elements can be added multiple times in a webpages. And both of these tags are designed to serve a crucial purpose in relation to their parent section. In **HTML5** not only Page body but section and article elements also contains header and footer elements, although the use of multiple footers is always not required.

</blockquote>
</details>

---

10. What is Character Encoding?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Character encoding is a method of converting bytes into characters. To validate or display an HTML document properly, a program must choose a proper character encoding. This is specified in the tag:

```HTML
<meta charset="utf-8"/>
```

**UTF-8:** A Unicode Translation Format that comes in 8-bit units that is, it comes in bytes. A character in UTF8 can be from 1 to 4 bytes long, making UTF8 variable width.

</blockquote>
</details>

---

11. What is local storage in Html5?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The local storage is a type of HTML5 offline storage ( local storage ) that allows user's data to be saved in their browser. The data is kept in a name and value pairs and not available between different browsers on the same device. Local storage can be used as an alternative to cookies.

</blockquote>
</details>

---

12. What is sessionStorage Object ?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The sessionStorage object is equal to the localStorage object, except that it stores the data for only one session. The data is deleted when the user closes the browser tab.

</blockquote>
</details>

---

13. What is difference between Select and Datalist?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

For the select element, the user is required to select one of the options you've given. For the datalist element, it is suggested that the user select one of the options you've given, but he can actually enter anything he wants in the input.

1. Select:

```HTML

<select name="browser">
  <option value="firefox">Firefox</option>
  <option value="ie">IE</option>
  <option value="chrome">Chrome</option>
  <option value="opera">Opera</option>
  <option value="safari">Safari</option>
</select>
```

2. Datalist:

```HTML
<input type="text" list="browsers">
<datalist id="browsers">
  <option value="Firefox">
  <option value="IE">
  <option value="Chrome">
  <option value="Opera">
  <option value="Safari">
</datalist>
```

</blockquote>
</details>

---

14. What are data- attributes good for?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The HTML5 data attribute lets us assign custom data to an element. When we want to store more information/data about the element when no suitable HTML5 element or attribute exists.

</blockquote>
</details>

---

15. List out the page structure elements of HTML5.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

`<header>:` Represents the header section and stores the starting information about the web page.
`<footer>:` Represents the footer section (last portion) of the page.
`<nav>:` Represents the navigation elements of the HTML page.
`<article>:` It is a set of information.
`<section>:` It is a set of instructions that is used inside the article block to define the basic structure of a page.
`<aside>:` Sidebar content of the page.

</blockquote>
</details>

---

16.  What is Microdata in HTML5?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Microdata is a new simple semantic syntax, that is used to add the nested groups of name and value pair of data to documents, that are commonly based on the page content. Microdata is used for new global attributes.

</blockquote>
</details>

---

17. Explain the `<figure>` tag in HTML5.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The `<figure>` tag is used for specifying self-contained content, such as diagrams and photos, in an HTML5 web page. Although the content of the figure element is related to the main flow of the document, its position is independent of the same, i.e., if removed, it will not affect the main flow of the document.

</blockquote>
</details>

---

18. Please explain whether an `<article>` element can have `<section>` elements and vice-versa.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Yes, an `<article>` element can have `<section>` element(s) and a `<section>` element can also have `<article>` elements. For example, a user panel for a website can have multiple `<section>` elements, intended for blog, analytics, payment options, news, etc.

Now, the `<section>` element for the blog can have multiple `<article>` elements to accommodate various articles. Further, each of these `<article>` elements can have two `<section>` elements, one for the comments section and the other for sharing section.

</blockquote>
</details>

---

19. Can u tell us about image maps in HTML5?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Image maps allow users to click on images for opening new web pages. As such, these are a combination of images and URLs. Image maps are of two types:

**Client-side Image Map** - Created using `<area>` and `<map>` elements. The map element holds the map information, and the area element takes the attributes for defining each section of the map.
**Server-side Image Map** - Created using the `<usemap>` attribute, which is the name of the map.

</blockquote>
</details>

---

20.  What are the various common lists for designing a web page in HTML5.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

`<dl>` - Definition list
`<dir>`- Directory list
`<menu>` - Menu list
`<ol>` - Ordered list
`<ul>` - Unordered list.

</blockquote>
</details>

---

21. Explain the difference between block elements and inline elements. 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Elements can be block-level elements or inline elements. The difference between block and inline elements is that the block elements take up the full width available while the inline elements take the required width to display the contents of the elements.

</blockquote>
</details>

---

22.  What are semantic and non-semantic elements?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

**Semantic elements:** clearly describes its meaning to both the browser and the developer. For example: `<form>, <table>, <article>, <aside>, <details>, <figcaption>, <figure>, <footer>, <header>, <main>, <mark>, <nav>, <section>, <summary>, <time>` clearly defines its content.

**Non-semantic elements:** `<div>` and `<span>` tells nothing about its content. 

</blockquote>
</details>

---

23. What are the elements in HTML?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- An HTML element is an individual component of an HTML document. It represents semantics, or meaning. For example, the title element represents the title of the document.

- Most HTML elements are written with a start tag (or opening tag) and an end tag (or closing tag), with content in between. Elements can also contain attributes that defines its additional properties.


</blockquote>
</details>

---

24. What ere void elements in HTML?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

All elements don't require the end tag or closing tag to be present. These are referred as empty elements, self-closing elements or void elements.

</blockquote>
</details>

---

25. What is the newest version of HTML and its new features?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The latest version is HTML5.

HTML5 is based on styles, a style attribute is used to format each tag. People say it will replace the flash player used to watch online videos, as HTML5 directly support the videos of HTML5 format, so we will never have to install flash player

</blockquote>
</details>

---

26. Explain Drag and Drop in HTML5?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

HTML5 drag-and-drop uses the DOM event model and drag events inherited from mouse events. A typical drag operation begins when a user selects a draggable element, drags the element to a droppable element, and then releases the dragged element.

**Example**
```HTML
<!DOCTYPE HTML>
<html>
   <head>
   <script>
        function allowDrop(ev) {
            ev.preventDefault();
        }

        function drag(ev) {
            ev.dataTransfer.setData("text", ev.target.id);
        }

        function drop(ev) {
            ev.preventDefault();
            var data = ev.dataTransfer.getData("text");
            ev.target.appendChild(document.getElementById(data));
        }
    </script>
</head>
<body>
  <div id="div1" ondrop="drop(event)" ondragover="allowDrop(event)"></div>
  <img id="drag1" src="img_logo.gif" draggable="true" ondragstart="drag(event)" width="336" height="69">
</body>
</html>
```

</blockquote>
</details>

--- 
