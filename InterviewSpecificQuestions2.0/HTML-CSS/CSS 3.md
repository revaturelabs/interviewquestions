1. What are the three elements of CSS3?

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

2. What is CSS3 element selector?

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

```css
P {
text-align: left;
Color: blue
}
```
In the output element P will be left aligned with the blue text color.

</blockquote>
</details>

---

3. What are the media we can add in CSS3?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Mostly we customize the design by using media. We need media control to make the external style sheet. Through the network, we can also retrieve and load in CSS3. List of media:

`braille`: Suitable for braille tactile feedback devices.
`embossed`: Suitable for barrel printers.
`all`: Can be used for all devices.
`handheld`: Suitable for small screens with limited bandwidth.
`print`: Suitable for show print preview before printing.
`screen`: Suitable for a projector.
`tty`: Can be used for teletypes or portable display devices.
`speech`: It helps to identify the synthesizer.
`tv`: Provides connection with television devices with color, sound, low resolution, and small scroll area.
`screen`: it helps to color computer display screen like PC screen or Laptop screen.

</blockquote>
</details>

---

4. Differentiate Physical tags and Logical tags.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Physical tags can be used to mark up presentations or appearances. Logical tags can not be used for markup, presentation, or appearances. 

The latest tag version is a physical tag type. The logical tag type is an older version of the tag.

Physical tag is concentrated on all media. Logical tags concentrated on HTML content only.

</blockquote>
</details>

---

5. Is style sheet different from HTML?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Yes, they are different. Because style sheets provide more styling, HTML provides less. If we use style sheets then we can get better formatting options and maximum browser compatibility.

</blockquote>
</details>

---

6. What is the ruleset in CSS3?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

One selector can be added to another selector by using the ruleset. It has two steps:

- Selector R 
- Declaration {text-indent: 12pt}.

</blockquote>
</details>

---

7. Is CSS3 case sensitive?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

CSS3 is not case sensitive, even also not dependent on font styles, or images on a website. But, if we do use XML then DOCTYPE will be XHTML, in that case, CSS3 will be case sensitive.

</blockquote>
</details>

---

8. Explain the declaration block in CSS3.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The declaration block is actually a bundle of consisting property, colon, and value within braces. Like [property 2: value 5]

</blockquote>
</details>

---

9. What are the various font attributes available in CSS3?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The various font attributes are

Caption.
Font Family.
Font Style.
Font Weight.
Icon.
Font size and height.
Font variant.

</blockquote>
</details>

---

10. Is it possible to insert a file by importing it in CSS3?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Yes, we can insert the file. Actually importing activates the combining sheets to be attached to other sheets. Here we can use different files and sheets for a few functions. So we can use this given syntax:

@import notation, used with <Style> tag.

</blockquote>
</details>

---

11. What are the different scenarios where you can use the class selector?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

In CSS3, the class selector is a commonly used selector that allows you to target elements based on their class attribute. You can use the class selector in various scenarios, including:

1. Styling Multiple Elements: By assigning the same class to multiple elements in your HTML document, you can use the class selector in CSS to apply the same styles to all those elements. This is useful when you want to maintain consistent styling across different elements.

Example:
HTML: `<p class="highlight">This is a highlighted paragraph.</p>`
CSS: `.highlight { color: red; }`

2. Differentiating Styles: If you have multiple elements of the same type but want to apply different styles to each, you can assign different classes to those elements and use the class selector to target them individually.

Example:
HTML:
```html
<p class="important">This is an important paragraph.</p>
<p class="warning">This is a warning paragraph.</p>
```
CSS:
```css
.important { font-weight: bold; }
.warning { color: red; }
```

3. Combining with Other Selectors: You can also combine the class selector with other selectors to target specific elements within a class. For example, you can use the class selector along with the descendant selector or the child selector to target elements within a specific class.

Example:
HTML:

```html
<div class="container">
  <h1>Title</h1>
  <p>Some text.</p>
</div>
```
CSS:
```css
.container h1 { color: blue; }
.container p { font-size: 14px; }
```

</blockquote>
</details>

---

12. Explain the Pseudo element.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

See in CSS3 Pseudo-elements are used by some selectors to add some special effects like styles in HTML normal markup level. But in some special cases, we can not add any document. In those cases, we can also use Pseudo-elements. Because it helps to mark up the document without distributing it.

</blockquote>
</details>

---

13. Can we overrule underlining hyperlinks?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Yes, we can overrule underlining hyperlinks.
```css
B {
Text-decoration:none:
}
<b href="career.html" style="text-decoration: none">link text </B>
```

</blockquote>
</details>

---

14. Can we use 100 % of the width over the page?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Yes, we can use it. When we declare the float then 1 pixel will be added every time. It can be added more to the border of the form with more floats.

</blockquote>
</details>

---

15. How to restore property values in CSS3?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

In CSS3, you can restore property values to their default or initial state using the `initial` keyword or by resetting the value to `inherit`. Here are two methods to restore property values in CSS3:

1. Using the `initial` keyword:
The `initial` keyword allows you to reset a property to its initial value, which is the value defined by the CSS specification. This effectively restores the property to its default state.

Example:
```css
p {
  color: initial; /* Restore the color property to its initial value */
  font-size: initial; /* Restore the font-size property to its initial value */
}
```

2. Using the `inherit` keyword:
The `inherit` keyword allows a property to inherit the value from its parent element. By setting a property to `inherit`, you restore it to the value inherited from its parent, effectively reverting any customizations applied to that property.

Example:
```css
p {
  color: inherit; /* Restore the color property by inheriting from the parent element */
  font-size: inherit; /* Restore the font-size property by inheriting from the parent element */
}
```

By using either the `initial` or `inherit` keyword, you can restore specific property values to their default or inherited states. It's important to note that not all properties have an initial or inherited value defined, so restoring properties in this way may not work for every property.

</blockquote>
</details>

---

16. Explain the CSS3 box model.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Actually, this box model contains the design and the element layout of CSS3. It has a few elements. Like:

Margin: Overall structure shoes in this topmost layer within this margin.
Border: Around the structure, the whole padding with contents is shown with color effects on the border.
Padding: It shows the spaces in content within the border.
Content: It shows the whole content.

</blockquote>
</details>

---

17. Differentiate Hexadecimal color codes and RGB values.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Hexadecimal color code uses a set of 6 characters and numbers. Whereas RGB uses 3 sets of 3 numbers with a range of 0-255. 

</blockquote>
</details>

---

18. Explain Grouping in CSS3.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

We can group the selector with the same values of property and the development code will be reduced. Now if they are having the same property then we can use commas to avoid rewriting.

</blockquote>
</details>

---

19. How to use Nesting CSS3?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Suppose, we want to specify a selector inside of a selector, then we have to use nesting in CSS3.

Example:
```css
p
{
color: black;
text-align: right;
}
.marked
{
background-color: white;
}
.marked p
{
color: orange;
}
```

</blockquote>
</details>

---

20. Differentiate the class selector and id-selector with an example.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The overall block is called a class selector, but a single element that is different from others elements is called an id selector.

Example of class selector:
```html
<style>
.center {
text-align: center;
color:red;
}
</style>
```

Example of id selector:
```html
<style>
#para1
{
text-align: centre;
color:red;
}
</style>
```

</blockquote>
</details>

---

21. What is the basic difference between visibility: hidden and display: none?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

They are different in properties in the case of the former, the element is deleted, the element is hidden or no space is consumed.

</blockquote>
</details>

---

22. Explain the Float property of CSS3.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

We can wrap the text and position it on the left or right without changing the element's property. If we need to move the images on web pages then we have to use the float property. We can move the right of the image to the left or left to right along with the attached text.

</blockquote>
</details>

---

23. What is the CSS3 counter?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Actually, this CSS3 counter is a variable. We can increase this variable value by using CSS3 inspect, even if we can find the number of times we have used the variable.

</blockquote>
</details>

---

24. What is the purpose of background-position property?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

When we want to declare the initial position of a particular background image, we have to do it through the background-position property. By default, the position is top left of the page. We can set the position as per our requirement, like right or corner or center, etc.

</blockquote>
</details>

---

25. What is Image repetition backup?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The background repetition property controls this backup process. If we are not repeating the image then we have to use no-repeat.

Example:
```html
<html>
<head>
<style>
body {
background-image: url("/css/images/css.jpg");
background-repeat: no-repeat;
}
</style>
</head>
<body>
<p> Text </p>
</body>
```
</blockquote>
</details>

---

26. Explain CSS3 Opacity.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Opacity means a certain degree that is applicable to light that passes through the objects in the pages. Actually, in CSS3 we control the transparency of any HTML elements by using opacity. It makes the images clear and visible. We can control opacity in two ways. 

First: We can declare it by @media or @import at-rules of specific target medium:
```css
@import url("fancyfonts.css") screen;
@media print {
 /*style sheet for print goes here*/
}
```

Second: Within the HTML4 document, we can declare the media attribute.
```html
<html>
 <head>
  <TITLE>Link to a target medium</TITLE>
  <LINK REL="stylesheet" TYPE="text/css"
        MEDIA="print,handheld" HREF="foo.css">
  </head>
 <body>
   <p>The body...
 </body>
</html>
```

</blockquote>
</details>

---

27. How will you define element dimension in CSS3? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

We can define the element dimension by the given properties:

Width.
Min Width.
Max Width.
Height.
Min Height.
Max Height.

</blockquote>
</details>

---

28. Explain Z-index in CSS3. 

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

If we are overlapping the elements vertically then we must use a z-index. It provides the vertical stack order of the elements. The default value we need to take is 0 in positive or negative. Also, we can the given values for z-index:

Inherit.
Initial.
Auto.
Number.

</blockquote>
</details>

---

29. What do you know about CSS3 Flexbox?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

It's a flexible box in CSS, also available in CSS3. It provides proper orientation of elements in web pages, easy layout handling, and space distribution within elements in a responsive website. We can also handle the dimensions of elements by using the flexbox property. It has a few properties. They are

Flex wrap: Identify whether the items should be wrapped or not.
Flex Direction: Identify the direction of the container to be stacked.
Flex Flow: Identify the flow direction and wrapping in one action.
Justify Content: Control the content alignment.
Align Items: Used to align flex items.
Align Content: Used to align flex lines.

</blockquote>
</details>

---