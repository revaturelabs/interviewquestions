## Technical

1. What is window object in JavaScript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

- It represents the browser's window. 
- All global JavaScript objects, functions, and variables automatically become members of the window object. 
- Global variables are properties of the window object. 
- Global functions are methods of the window object.

</blockquote>
</details>

---

2. How to redirect the user to a new page?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

We can use the window object location to redirect the user to the new page by providing the HREF URL link to be redirected.

`window.location.href="https://www.domain.com/"`

</blockquote>
</details>

---

3. What is DOM(Document Object Model)?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

When HTML documents are loaded in the browser(which creates DOM), it will become a document object which is the root element that represents the HTML document. Each DOM element has various properties and methods through which we can add dynamic content to our web page according to the required behavior.

</blockquote>
</details>

---

4. What is an Event and explain Event Handling.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

The change in the state of an object is known as an `Event`. In html, there are various events which represents that some activity is performed by the user or by the browser. When JavaScript code is included in HTML, JS react over these events and allow the execution. This process of reacting over the events is called `Event Handling`. 

</blockquote>
</details>

---

5. How do you change the text content of an HTML element using JavaScript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

You can change the text content of an HTML element using the `textContent` property. For example: `element.textContent = 'New text';`

</blockquote>
</details>

---

6. List the types of events used in JavaScript.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

- Mouse events
- Keyboard events
- Form events
- Window/Document events

</blockquote>
</details>


---

7. How do you handle events in JavaScript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

You can handle events in JavaScript by using the `addEventListener` method to attach an event listener to an HTML element. The listener is a function that gets executed when the event occurs. For example:
```javascript
element.addEventListener('click', function() {
  // Event handling code
});
```

</blockquote>
</details>

---

8. What method can be used instead of this `document.form1.name.value method`?


![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

we can use the method `document.getElementById()` to get value of the input text. 

</blockquote>
</details>

---

9. What is the use of `getElementsByClassName()` method?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

It is used for selecting or getting the elements through their class name value.

When the method is applied on any particular element, it will search the whole document and will return only those elements which match the specified or given class name.


</blockquote>
</details>

---

10. Explain Event Bubbling.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Whenever an event happens on an element, the event handlers will first run on it and then on its parent element and finally all the way up to its other ancestor elements.

</blockquote>
</details>

---

11.  Explain Event Capturing .

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

It is the reverse of the event bubbling and here the event starts from the parent element and then to its nested child elements.

</blockquote>
</details>

---

12. How do you access an HTML element using JavaScript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

You can access an HTML element using JavaScript by using methods like `getElementById`, `getElementsByClassName`, `getElementsByTagName`, or `querySelector`. For example: `var element = document.getElementById('myElement');`

</blockquote>
</details>

---

13. How do you change the content of an HTML element using JavaScript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

You can change the content of an HTML element using the `innerHTML` property or the `textContent` property. For example: `element.innerHTML = 'New content';`

</blockquote>
</details>

---

14. How do you change the style of an HTML element using JavaScript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

You can change the style of an HTML element using the `style` property and assigning new CSS values to its individual properties. For example: `element.style.color = 'red';`

</blockquote>
</details>

---

15. How do you create a new HTML element using JavaScript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

You can create a new HTML element using the `createElement` method, specifying the element type, and then appending it to the DOM using methods like `appendChild` or `insertBefore`. For example:
```javascript
var newElement = document.createElement('div');
parentElement.appendChild(newElement);
```

</blockquote>
</details>

---

16. How do you remove an HTML element using JavaScript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

You can remove an HTML element from the DOM using the `remove` method or by targeting its parent element and using the `removeChild` method. For example:
```javascript
var element = document.getElementById('myElement');
element.remove();
```
</blockquote>
</details>

---

17. How do you add a CSS class to an HTML element using JavaScript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

You can add a CSS class to an HTML element using the `classList.add` method. For example: `element.classList.add('myClass');`

</blockquote>
</details>

---

18. How do you get the value of an input element using JavaScript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

You can get the value of an input element using the `value` property. For example: `var inputValue = inputElement.value;`

</blockquote>
</details>

---

19. How do you manipulate the attributes of an HTML element using JavaScript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

You can manipulate the attributes of an HTML element using the `getAttribute`, `setAttribute`, or `removeAttribute` methods. For example: `element.setAttribute('src', 'image.jpg');`

</blockquote>
</details>

---

20. How do you remove a CSS class from an HTML element using JavaScript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

You can remove a CSS class from an HTML element using the `classList.remove()` method. For example: `element.classList.remove('oldClass');`

</blockquote>
</details>

---

21. How do you toggle a CSS class on an HTML element using JavaScript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

You can toggle a CSS class on an HTML element using the `classList.toggle()` method. For example: `element.classList.toggle('active');`

</blockquote>
</details>

---

22. How do you check if an HTML element has a specific CSS class using JavaScript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

You can check if an HTML element has a specific CSS class using the `classList.contains()` method. It returns `true` if the element has the class, and `false` otherwise. For example: `element.classList.contains('myClass');`

</blockquote>
</details>

---

23. How do you change the source (URL) of an image using JavaScript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

You can change the source of an image element using the `src` property. For example: `imageElement.src = 'newImage.jpg';`

</blockquote>
</details>

---

24. How do you hide an HTML element using JavaScript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

You can hide an HTML element by modifying its CSS `display` property. For example: `element.style.display = 'none';`

</blockquote>
</details>

---

25. How do you show a hidden HTML element using JavaScript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

You can show a hidden HTML element by modifying its CSS `display` property. For example: `element.style.display = 'block';`

</blockquote>
</details>

---

26. How do you get the parent element of an HTML element using JavaScript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

You can get the parent element of an HTML element using the `parentNode` property. For example: `var parentElement = element.parentNode;`

</blockquote>
</details>

---

27. How do you prevent the default behavior of an HTML element using JavaScript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

You can prevent the default behavior of an HTML element using the `event.preventDefault()` method. For example:
```javascript
element.addEventListener('click', function(event) {
  event.preventDefault();
});
```
</blockquote>
</details>

---

28. What is event delegation in JavaScript?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Event delegation is a technique where you attach a single event listener to a parent element to handle events on its child elements. This is useful when dynamically adding or removing elements from the DOM.

</blockquote>
</details>

---

29. How do you create and dispatch a custom event in JavaScript?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

To create and dispatch a custom event, you can use the `CustomEvent` constructor. For example:
```javascript
var customEvent = new CustomEvent('myEvent', { detail: { data: 'Hello' } });
element.dispatchEvent(customEvent);
```
</blockquote>
</details>

---

30. How do you clone an HTML element using JavaScript?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

You can clone an HTML element and its contents using the `cloneNode()` method. For example: `var clone = element.cloneNode(true);`

</blockquote>
</details>

---

31. How do you dynamically load external JavaScript files?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

You can dynamically load external JavaScript files by creating a `<script>` element and appending it to the document's `<head>` or `<body>` using the `appendChild()` method. For example:
```javascript
var script = document.createElement('script');
script.src = 'external.js';
document.head.appendChild(script);
```
</blockquote>
</details>

---

32. How do you check if an element has a specific attribute using JavaScript?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

You can check if an element has a specific attribute using the `hasAttribute()` method. For example: `element.hasAttribute('class');`

</blockquote>
</details>

---

33. How do you scroll to a specific element on a page using JavaScript?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

You can scroll to a specific element on a page using the `scrollIntoView()` method. For example: `element.scrollIntoView();`

34. How do you create a live collection of elements in JavaScript?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

You can create a live collection of elements using methods like `querySelectorAll()`. The returned collection is live, meaning it is updated automatically when the DOM changes.

</blockquote>
</details>

---

35. How do you create a custom data attribute in HTML and access it using JavaScript?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

You can create a custom data attribute in HTML by prefixing the attribute name with `data-`. For example: `<div data-info="myData"></div>`. You can access it using the `dataset` property in JavaScript. For example: `var data = element.dataset.info;`

</blockquote>
</details>

---

36. How do you disable or enable an HTML form element using JavaScript?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

You can disable or enable an HTML form element by setting the `disabled` property to `true` or `false`, respectively. For example: `element.disabled = true;`

</blockquote>
</details>

---

37. How do you dynamically create a CSS rule using JavaScript?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

You can dynamically create a CSS rule using the `insertRule()` method of a stylesheet. For example:
```javascript
var sheet = document.styleSheets[0];
sheet.insertRule('.myClass { color: red; }', 0);
```
</blockquote>
</details>

---