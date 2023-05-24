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

<code> window.location.href="https://www.revature.com/" </code>

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

4. What do you mean by Event and Event handling?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

The change in the state of an object is known as an `Event`. In html, there are various events which represents that some activity is performed by the user or by the browser. When JavaScript code is included in HTML, JS react over these events and allow the execution. This process of reacting over the events is called `Event Handling`. 

 </blockquote>

</details>


---

5. How does HTML events are handled in JavaScript?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

JavaScript handles the HTML events through Event Handlers.

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

7. How to attach an event handler in JavaScript?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

The `addEventListener()` method is an inbuilt function of JavaScript to add multiple event handlers to a particular element without overwriting the existing event handlers.

Syntax:

<code> element.addEventListener(event, function, useCapture);  </code>

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
10. Explain about Event Bubbling.

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Whenever an event happens on an element, the event handlers will first run on it and then on its parent element and finally all the way up to its other ancestor elements.

 </blockquote>

</details>


---

11.  Explain about Event Capturing .

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

It is the reverse of the event bubbling and here the event starts from the parent element and then to its nested child elements.

 </blockquote>

</details>


---
