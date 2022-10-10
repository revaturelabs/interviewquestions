1. What is CSS?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

CSS is a styling language that makes HTML web pages more presentable. It allows you to add color, design, and buttons, among other things, to a website.

</blockquote>
</details>

---

2. What are the three main ways to apply CSS styles to a web page?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Using the inline style attribute on an element

``` CSS
<div>
    <p style="color: maroon;"></p>
</div>
```
- Using a `<style>` block in the `<head>` section of your HTML

```CSS
<head>
    <title>CSS Refresher</title>
    <style>
        body {
            font-family: sans-serif;
            font-size: 1.2em;
        }
    </style>
</head>
```

- Loading an external CSS file using the `<link>` tag

```CSS
<head>
    <title>CSS Refresher</title>
    <link rel="stylesheet" href="/css/styles.css" />
</head>

```

</blockquote>
</details>

---

3. Can you tell me briefly about  CSS “box model” and the layout components that it consists of?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The CSS box model is a rectangular layout paradigm for HTML elements that consists of the following:

**Content** - The content of the box, where text and images appear
**Padding** - A transparent area surrounding the content (i.e., the amount of space between the border and the content)
**Border** - A border surrounding the padding (if any) and content
**Margin** - A transparent area surrounding the border (i.e., the amount of space between the border and any neighboring elements)

</blockquote>
</details>

---

4. What is a CSS rule?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Web browsers apply CSS rules to a document to affect how they are displayed. A CSS rule is formed from:

- A **set of properties**, which have values set to update how the HTML content is displayed,
- A **selector**, which selects the element(s) you want to apply the updated property values to.
- A **set of CSS rules** contained within a stylesheet determines how a webpage should look.

</blockquote>
</details>

---

5. Can u tell me the three elements of CSS3?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

CSS3 has the elements as syntax rules; they are

- Selector.
- Property.
- It's Value.

</blockquote>
</details>

---

6. Which type of CSS holds the highest priority?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Inline CSS has the highest priority, then comes Internal/Embedded followed by External CSS which has the least priority. Multiple style sheets can be defined on one page. If for an HTML tag, styles are defined in multiple style sheets then the below order will be followed.

- As Inline has the highest priority, any styles that are defined in the internal and external style sheets are overridden by Inline styles.

- Internal or Embedded stands second in the priority list and overrides the styles in the external style sheet.

- External style sheets have the least priority. If there are no styles defined either in the inline or internal style sheet then external style sheet rules are applied for the HTML tags.

</blockquote>
</details>

---

7. What is a CSS selector?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

CSS selectors are used to select the content you want to style. Selectors are the part of CSS rule set. CSS selectors select HTML elements according to its id, class, type, attribute etc.

There are several different types of selectors in CSS.

- CSS Element Selector
- CSS Id Selector
- CSS Class Selector
- CSS Universal Selector
- CSS Group Selector

</blockquote>
</details>

---

8. What do you know about the CSS3 element selector?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

CSS3 element selector helps to find out the HTML elements name which we want to apply in a style sheet. It has five categories. They are

`Attribute Selectors`: Find an attribute or attribute value of an HTML element.
`Combinator Selectors`: Find a specific relationship between elements.
`Simple Selectors`: Find a name, id, or class of an element.
`Pseudo Class Selectors`: Find a certain state of an element.
`Pseudo Elements Selectors`: Find the style part and select an element.

Example:

```CSS
P {
text-align: left;
Color: blue
```
In the output element P will be left aligned with the Blue text color.

</blockquote>
</details>

---

9. Have you played around with the new CSS Flexbox or Grid specs?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Yes. Flexbox is mainly meant for 1-dimensional layouts while Grid is meant for 2-dimensional layouts.

- Flexbox solves many common problems in CSS, such as vertical centering of elements within a container, sticky footer, etc. Bootstrap and Bulma are based on Flexbox, and it is probably the recommended way to create layouts these days. Have tried Flexbox before but ran into some browser incompatibility issues (Safari) in using flex-grow, and I had to rewrite my code using inline-blocks and math to calculate the widths in percentages, it wasn't a nice experience.

- Grid is by far the most intuitive approach for creating grid-based layouts (it better be!) but browser support is not wide at the moment.

</blockquote>

</details>

---

10. What is DOM (Document Object Model) and how is it linked to CSS?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The Document Object Model (DOM) is a cross-platform and language-independent application programming interface that treats an HTML, XHTML, or XML document as a tree structure wherein each node is an object representing a part of the document.

With the Document Object Model, programmers can create and build documents, navigate their structure, and add, modify, or delete elements and content. The DOM specifies interfaces which may be used to manage XML or HTML documents.

When a browser displays a document, it must combine the document's content with its style information. The browser converts HTML and CSS into the DOM (Document Object Model). The DOM represents the document in the computer's memory. It combines the document's content with its style.

</blockquote>
</details>

---

11. What does the cascading portion of CSS mean?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- The cascading in CSS refers to the fact that styling rules "cascade" down from several sources. This means that CSS has an inherent hierarchy and styles of a higher precedence will overwrite rules of a lower precedence.

- Even the simplest HTML document may have three or more style sheets associated with it including:

  - The browser's style sheet
  - The user's style sheet
  - The author's style sheet

</blockquote>
</details>

---

12. What is contextual selector?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Contextual selector addresses specific occurrence of an element. It is a string of individual selectors separated by white space (search pattern), where only the last element in the pattern is addressed providing it matches the specified contex.

- It also check the context of the class in the html tree, assigning the style to the element through a specific route, taking into account the order of depth in the tree.

**Example**:

```CSS
table p { property: value; } 
```
</blockquote>
</details>

---

13. Describe floats and how they work

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Float is a CSS positioning property. Floated elements remain a part of the flow of the web page. This is distinctly different than page elements that use absolute positioning. Absolutely positioned page elements are removed from the flow of the webpage.

```CSS
#sidebar {
float: right; // left right none inherit
}
```
The CSS clear property can be used to be positioned below left/right/both floated elements.

</blockquote>
</details>

---

14. What is the difference between classes and IDs in CSS?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

**IDs** — Meant to be unique within the document. Can be used to identify an element when linking using a fragment identifier. Elements can only have one id attribute.

**Classes** — Can be reused on multiple elements within the document. Mainly for styling and targeting elements.

</blockquote>
</details>

---

15. What is the use of CSS Opacity?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The CSS opacity property is used to specify the transparency of an element. In simple word, you can say that it specifies the clarity of the image. In technical terms, Opacity is defined as the degree to which light is allowed to travel through an object.

For example:

```CSS
<style>    
img.trans {    
    opacity: 0.4;    
    filter: alpha(opacity=40); /* For IE8 and earlier */    
}    
</style>   
```

</blockquote>
</details>

---

16. What is the difference between CSS border and outline?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

`CSS border properties` allow us to set the style, color, and width of the border.
`CSS outline property` allows us to draw a line around the element, outside the border.

</blockquote>
</details>

---

17. How can the background color of an element be changed?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The background color of an image can be changed using the background-color property.

```CSS
body
{
background-color: coral;
}
```
</blockquote>
</details>

---

18. Why do we use pseudo-class?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- A pseudo-class is used to define a special state of an element.
- For example, it can be used to:
  - Style an element when a user mouses over it.
  - Style visited and unvisited links differently.
  - Style an element when it gets focus.
  - Pseudo-class names are not case-sensitive.
  - Pseudo-classes can be combined with HTML classes.

- When you hover over the link in the example, it will change color:

```CSS
    selector:pseudo-class {
    property: value;
    }
    Like 
    /* mouse over link */
    a:hover {
    color: #FF00FF;
    }
    
    /* selected link */
    a:active ;
    color: #0000FF;
    }
```
</blockquote>
</details>

---

19. What is the difference between flex and grids?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

**Grid and flexbox**. The basic difference between CSS Grid Layout and CSS Flexbox Layout is that flexbox was designed for layout in one dimension - either a row or a column. Grid was designed for two-dimensional layout - rows, and columns at the same time.

```CSS
<div class="wrapper">
  <div>One</div>
  <div>Two</div>
  <div>Three</div>
  <div>Four</div>
  <div>Five</div>
</div>

​​.wrapper {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
}
```
Flex Example :

```CSS
.wrapper {
  width: 500px;
  display: flex;
  flex-wrap: wrap;
}
.wrapper > div {
  flex: 1 1 150px;
}
```

</blockquote>
</details>

---

20. Give an example where we have to use grids and where you have to use flexbox?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

If we are using flexbox and find yourself disabling some of the flexibility, we probably need to use CSS Grid Layout. An example would be if we are setting a percentage width on a flex item to make it line up with other items in a row above. In that case, a grid is likely to be a better choice.

Use a grid when we already have the layout structure in mind, and flex when we just want everything to fit.

</blockquote>
</details>

---

21. Which one of these units would you prefer: `px, em, % or pt` and why?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

It depends on what we are trying to do.

**px** gives fine grained control and maintains alignment because 1 px or multiple of 1 px is guaranteed to look sharp. px is not cascade, this means if parent font-size is 20px and child 16px. child would be 16px.

**em** maintains relative size. we can have responsive fonts. em is the width of the letter 'm' in the selected typeface. However, this concept is tricky. 1em is equal to the current font-size of the element or the browser default. if we sent font-size to 16px then 1em = 16px. The common practice is to set default body font-size to 62.5% (equal to 10px). em is cascade

**%** sets font-size relative to the font size of the body. Hence, we have to set font-size of the body to a reasonable size. this is easy to use and does cascade. for example, if parent font-size is 20px and child font-size is 50%. child would be 10px.

**pt(points)** are traditionally used in print. 1pt = 1/72 inch and it is fixed-size unit.

</blockquote>
</details>

---

22. How do absolute, relative, fixed and static position differ?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

**absolute**, place an element exactly where we want to place it. absolute position is actually set relative to the element's parent. if no parent available then relatively place to the page itself.

**relative**, is position an element relative to itself (from where the element would be placed, if we don't apply relative positioning). for example, if we set position relative to an element and set top: 10px, it will move 10px down from where it would be normally.

**fixed**, element is positioned relative to viewport or the browser window itself. viewport doesn't changed if we scroll and hence fixed element will stay right in the same position.

**static**, element will be positioned based on the normal flow of the document. usually, we will use position static to remove other position might be applied to an element.

</blockquote>
</details>

---

23. What are the differences between visibility hidden and display none?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

`display`: none removes the element from the normal layout flow and allow other elements to fill in. `visibility`: hidden tag is rendered, it takes space in the normal flow but doesn't show it.

</blockquote>
</details>

---

24. What are the differences between inline, block and inline-block?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

`inline`, elements do not break the flow. think of span it fits in the line. Important points about inline elements, margin/ padding will push other elements horizontally not vertically. Moreover, inline elements ignores height and width.

`block`, breaks the flow and dont sits inline. they are usually container like div, section, ul and also text p, h1, etc.

`inline-block`, will be similar to inline and will go with the flow of the page. Only differences is this this will take height and width.

</blockquote>
</details>

---

25. What are the properties related to box model?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Technically, height, width, padding and border are part of box model and margin is related to it.
- Everything in a web page is a box where we can control size, position, background, etc. Each box/ content area is optionally surrounded by padding, border and margin. When we set height and width of an element, we set content height and width.

</blockquote>
</details>

26. Does overflow: hidden create a new block formatting context?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

yes, overflow property deals with the content if content size exceeds the allocated size for the content. We can make extra content visible, hidden, scroll or auto (viewport default behavior).

</blockquote>
</details>

---

27. What are the some pseudo classes you have used?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- pseudo class tells us specific state of an element. allow to style element dynamically. The most popular one is `:hover`. Besides i have used `:visited`, `:focus`, `:nth-child`,` nth-of-type`, `:link`, etc.

- pseudo classes is better if we don't want to mess up with javaScript however, pseudo-classes is slow to process and apply rules.

</blockquote>
</details>

---

28. How do you align a p center-center inside a div?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

`text-align: center` will do the horizontal alignment but `vertical-align: middle` will not work here. there are couple of different ways to solve this problem and one of them are positioning. We make the parent as relative position and child as absolute positioning. And then define all position parameter as zero and width 50% and height 30%.

**Example**

```CSS
<style>
   .divContainer{
      height: 100px;
      border: 2px solid gray;
      text-align: center;
      position: relative;
   }
   p{        
      position: absolute;
      top: 0;
      bottom: 0;
      left: 0;
      right: 0;
      width: 50%;
      height: 30%;
      margin: auto;
    }
</style>
<div class = "divContainer">
  <p>content example</p>
</div>
```
</blockquote>
</details>

---

29. How do you optimize css selectors?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

This is very open and depend on what we are trying to achieve. If we order selectors in terms of render speed it would be like id, class, tag, siblings, child, descendant, universal, attribute, pseudo. Speed of ID and class is very close. However your code should be readable, maintainable and DRY along with highly performant.

</blockquote>
</details>

---

30. How can you load css resources conditionally?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

`@import` allows us to load/ import stylesheet by using a path (uri) representing the location of the file. We can define one or more media by comma separation for which we want to load the stylesheet. If browser dont support the media stylesheet will not be loaded.



</blockquote>
</details>

---

31. What are the different css filter you can use?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

css filter allows us to render DOM element, image, or video. We can choose from: grayscale, blur, opacity, brightness, contrast.

</blockquote>
</details>

---

32. What do you know about transition?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Transition allows to add an effect while changing from one style to another. we can set the which property we want to transition, duration, how we want to transit (linear, ease, ease-in, ease-out, cubic-bezier) and delay when transition will start. We can transition more than one property by comma separation.

</blockquote>
</details>

---

33. What are the reasons to use preprocessor?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

We write css in high level with some special syntax (declaring variable, nested syntax, mathematical operations, etc.) and that is compiled to css. Preprocessor helps us to speed up develop, maintain, ensure best practices and also confirms concatenation, compression, etc.

</blockquote>
</details>

---

34. Explain the usage of "table-layout" property

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The table-layout property defines the algorithm used to layout table cells, rows, and columns.

`table-layout`: auto|fixed|initial|inherit;
`auto` - Browsers use an automatic table layout algorithm. The column width is set by the widest unbreakable content in the cells. The content will dictate the layout.
`fixed` - The layout is fixed based on the first row. Set the width of those, and the rest of the table follows. If no widths are present on the first row, the column widths are divided equally across the table, regardless of content inside the cells.
`initial` - Sets this property to its default value.
`inherit` - Inherits this property from its parent element.

</blockquote>
</details>

---

35. How is responsive design different from adaptive design?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Both responsive and adaptive design attempt to optimize the user experience across different devices, adjusting for different viewport sizes, resolutions, usage contexts, control mechanisms, and so on.

Responsive design works on the principle of flexibility — a single fluid website that can look good on any device. Responsive websites use media queries, flexible grids, and responsive images to create a user experience that flexes and changes based on a multitude of factors. Like a single ball growing or shrinking to fit through several different hoops.

Adaptive design is more like the modern definition of progressive enhancement. Instead of one flexible design, adaptive design detects the device and other features, and then provides the appropriate feature and layout based on a predefined set of viewport sizes and other characteristics. The site detects the type of device used, and delivers the pre-set layout for that device. Instead of a single ball going through several different-sized hoops, we’d have several different balls to use depending on the hoop size.

</blockquote>
</details>

---

36.  What does Accessibility (a11y) mean?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Accessibility (a11y) is a measure of a computer system's accessibility is to all people, including those with disabilities or impairments. It concerns both software and hardware and how they are configured in order to enable a disabled or impaired person to use that computer system successfully.

Accessibility is also known as assistive technology.

</blockquote>
</details>

---

37.  What’s the difference between “resetting” and “normalizing” CSS? Which would you choose, and why?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

**Resetting** — is meant to strip all default browser styling on elements. For e.g. margins, paddings, font-sizes of all elements are reset to be the same. You will have to redeclare styling for common typographic elements.
**Normalizing**— preserves useful default styles rather than “unstyling” everything. It also corrects bugs for common browser dependencies.
It's a good idea to choose resetting when we have very a customized or unconventional site design such that we need to do a lot of our own styling do not need any default styling to be preserved.

</blockquote>
</details>

---

38. Describe pseudo-elements and discuss what they are used for.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

A CSS pseudo-element is a keyword added to a selector that lets you style a specific part of the selected element(s). They can be used for decoration (`:first-line, :first-letter`) or adding elements to the markup (combined with content: ...) without having to modify the markup (`:before, :after`).

Example of usage:

- `:first-line and :first-letter` can be used to decorate text.
- Used in the `.clearfix` hack to add a zero-space element with clear: both.
- Triangular arrows in tooltips use `:before and :after`. Encourages separation of concerns because the triangle is considered part of styling and not really the DOM, but not really possible to draw a triangle with just CSS styles.

</blockquote>
</details>

---

39. What is the difference between RGBa, HEX and HSLa?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- RGB (Red/Green/Blue) is a color model.
```CSS
p {
  color: rgba(37, 84, 127, 1);
}
```

- HEX (Hexadecimal color values)
```CSS
p {
  color: #25547f;
}
```

- HSLa (Hue Saturation Lightness alpha)
```CSS
p {
  color: hsla(209, 55%, 32%, 1);
}
```

</blockquote>
</details>

---

40. Explain the purpose of clearing floats in CSS?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The **clear** property is directly related to the float property. It specifies if an element should be next to the floated elements or if it should move below them. This property applies to both floated and non-floated elements.

**CSS Syntax:**

```css
clear: none|left|right|both|inherit|inline-start|inline-end;
```

**Property Values:**

|Value       |Description	                                       |
|------------|---------------------------------------------------|
|none	       |The element is not moved down to clear past floats.|
|left	       |The element is moved down to clear past left floats.|
|right	     |The element is moved down to clear past right floats.|
|Both 	     |The element is moved down to clear past both left and right floats.|

**Example:**

```Html
<!DOCTYPE html>
<html>
<head>
  <title>CSS clear Property</title>
  <style>
    .div1 {
      float: left;
      width: 100px;
      height: 50px;
      margin: 10px;
      border: 3px solid #73AD21;
    }

    .div2 {
      border: 1px solid red;
      height: 100px;
    }

    .div3 {
      float: left;
      width: 100px;
      height: 50px;
      margin: 10px;
      border: 3px solid #73AD21;
    }

    .div4 {
      border: 1px solid red;
      height: 100px;
      clear: left;
    }
  </style>
</head>
<body>
    <h2>Without clear</h2>
    <div class="div1">div1</div>
    <div class="div2">div2 - Notice that the div2 element is after div1, in the HTML code. 
      However, since div1 is floated to the left, this happens: the text in div2 is floated 
      around div1, and div2 surrounds the whole thing.
    </div><br/>

    <h2>Using clear</h2>
    <div class="div3">div3</div>
    <div class="div4">div4 - Using clear moves div4 down below the floated div3. The value 
      "left" clears elements floated to the left. You can also clear "right" and "both".</div>
</body>
</html>
```

</blockquote>
</details>

---

41. How a browser determines what elements match a CSS selector?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Browsers match selectors from rightmost (key selector) to left. Browsers filter out elements in the DOM according to the key selector and traverse up its parent elements to determine matches. The shorter the length of the selector chain, the faster the browser can determine if that element matches the selector.

For example with this selector p span, browsers firstly find all the `<span>` elements and traverse up its parent all the way up to the root to find the `<p>` element. For a particular `<span>`, as soon as it finds a `<p>`, it knows that the `<span>` matches and can stop its matching.

</blockquote>
</details>

---

42. What is At-Rule?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

At-rules are `CSS statements` that instructs CSS how to behave. They begin with an at sign, `@` followed by an identifier and includes everything up to the next semicolon, `;` or the next CSS block, whichever comes first.

```css
/* General structure */
@IDENTIFIER (RULE);

/* Example: tells browser to use UTF-8 character set */
@charset "utf-8";
```

|Sl.No| at-rules  | Description |
|-----|-----------|-------------|
| 01. |@charset   |Defines the character set used by the style sheet.|
| 02. |@import    |Tells the CSS engine to include an external style sheet.|
| 03. |@namespace |Tells the CSS engine that all its content must be considered prefixed with an XML namespace.|
| 04. |@media     |A conditional group rule that will apply its content if the device meets the criteria of the condition defined using a media query.|
| 05. |@supports  |A conditional group rule that will apply its content if the browser meets the criteria of the given condition.|
| 06. |@page      |Describes the aspect of layout changes that will be applied when printing the document.|
| 07. |@font-face |Describes the aspect of an external font to be downloaded.|
| 08. |@keyframes |Describes the aspect of intermediate steps in a CSS animation sequence.|

</blockquote>
</details>

---

43. How do i restore the default value of a property?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The keyword `initial` can be used to resets it to its default value, which is defined in the CSS specification of the given property.

</blockquote>
</details>

---

44.  What is the difference between padding and margin?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

**1) Margin** is applied to the outside of you element hence effecting how far your element is away from other elements.  
**2) Padding** is applied to the inside of your element hence effecting how far your element\'s content is away from the border.

Also, using margin will not affect your element\'s dimensions whereas padding will make your elements dimensions (set height + padding) so for example if you have a 100x100px div with a 5 px padding, your div will actually be 105x105px

```CSS
<p align="center">
  <img src="assets/images/padding-margin.png" alt="Padding vs Margin" width="600px" />
</p>
```
*Note:* **Top/Bottom margins are collapsible:** if you have a 20px margin at the bottom of an element and a 30px margin at the top of the next element, the margin between the two elements will be 30px rather than 50px. This does not apply to left/right margin or padding.

</blockquote>
</details>

---

45. How is the concept of inheritance applied in CSS?


![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Inheritance is a concept in which the child class will inherit the properties of its parent class. It is used in CSS to define the hierarchy from the top level to the bottom level. Inherited properties can be overridden by the children class if the child uses the same name.

**Example:**

```CSS
span {
  color: blue;
  border: 1px solid black;
}
.extra span {
  color: inherit;
}
```

</blockquote>
</details>

---

46. How does Calc() work?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The `calc()` function can be used to perform addition, subtraction, multiplication, and division calculations with numeric property values. Specifically, it can be used with `<length>`, `<frequency>`, `<angle>`, `<time>`, `<number>`, or `<integer>` data types.

**Example:**

```css
/* Example - 1 */
.main-content {
  width: calc(100vh - 10px); /* Subtract 10px from 100vh */
}

/* Example - 2 */
.container {
  padding: calc(1vw + 1em);
  width: calc(var(--variable-width) + 200px);
  transform: rotate( calc(1turn + 28deg) );
  background: hsl(100, calc(3 * 20%), 40%);
  font-size: calc(50vw / 3);
  border-radius: 15px calc(15px / 3) 4px 2px;
}
```
</blockquote>
</details>

---

47. Can you add 3D transformations to our project using CSS?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Yes, 3D transformations can be used to change elements. The elements in 3D transformation are rotated along the X, Y, and Z axes.

There are three main transformation types that are mentioned below:

   -  rotateX()
   - rotateY()
   - rotateZ()

</blockquote>
</details>

---

48. What is responsive web design?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Responsive Design is a method of creating web pages that makes use of adaptable images, versatile layouts, and CSS media queries. This design approach aims to create web pages that identify the orientation and screen size of visitors and adjust the layout accordingly.

</blockquote>
</details>

---

49. How does the Z index function?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Sometimes, while positioning the elements of HTML using CSS, overlapping may occur. Z index helps in identifying and specifying the element that is overlapping. Z index’s default value is zero, but it can be a positive or a negative number.

</blockquote>
</details>

---

50. Define Image sprites with context to CSS?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Image Sprites is the process of collaborating several images into one. It reduces the time taken in loading images and gives information more quickly.

</blockquote>
</details>

---

51. State the difference between Style Sheet and HTML?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

HTML lacks styling even though HTML has an easy structure method. Styling Sheets not only offer styling but also have better formatting options and browsing capabilities.

</blockquote>
</details>

---

