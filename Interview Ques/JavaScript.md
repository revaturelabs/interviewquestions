## Technical

1. What type of language is JavaScript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

 JavaScript is a scripting language that may be used to generate websites and applications,to construct online and mobile apps, web servers, games etc. Which is widely used for client-side validation.

 </blockquote>

</details>


---

2. What is used to translate the JavaScript code for the web browser?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

JavaScript is not a compiled language, but it is a translated language. The JavaScript Translator (embedded in the browser) is responsible for translating the JavaScript code for the web browser.

 </blockquote>

</details>


---

3. Mention the different data types present in javascript.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

There are two types of data types to hold different types of values in JavaScript. 

- Primitive types- String, Number, Boolean, Undefined, Null
- Non-primitive (reference) data type - Object, Array, RegExp

 </blockquote>

</details>


---

4. Do we need to specify type of the variable in JavaScript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

JavaScript is a <b> dynamic type language </b>, so no need to specify type of the variable because it is dynamically used by JavaScript engine

 </blockquote>

</details>


---

5. Explain about the scopes of a variable in JavaScript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>


The scope of a variable represents where the variable has been declared or defined in a JavaScript program. There are two scopes of a variable:

`Global Scope` -Global variables, having global scope are available everywhere in a JavaScript code.

`Local Scope` -Local variables are accessible only within a function in which they are defined.

 </blockquote>

</details>


---

6. Differentiate between the terms undefined and not defined.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

``` java
var x;
console.log(x);
```

Here in the example we will get a message x is `undefined` which means the variable x is declared and memory is created but the value is not assigned to it.

<code> console.log(y) </code>

In this case, you will get a message like `not defined` because the variable y is not created, and memory is not allocated for it and we try to reference the variable.

 </blockquote>

</details>


---

7. What is the use of `typeof` operator?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

The `typeof` is a unary operator which takes a single operand in a statement, it is used to check the data type of its operand in the form of a string for example if we check the variable which is undefined then the `typeof` will return values as `undefined`.

``` java
var x=15;
console.log(typeof (x))
```

It will print the number 15 in the console

<code>
var x = 15;
console.log(typeof (y) == 'number')
</code>

From the above code if the `typeof` y is a number, so from the expression it will print true in the console.


 </blockquote>

</details>


---

8. Explain Hoisting in javascript.

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Which is the default behaviour of javascript where all the variable and function declarations are moved on top, irrespective of where the variables and functions are declared, they are moved on top of the scope. The scope can be both local and global.

 </blockquote>

</details>


---

9. When does for loop should be used in JavaScript?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

It iterates the elements for the fixed number of times. It should be used if the number of iteration is known. 

 </blockquote>

</details>


---

10. What loop should be used if number of iteration is not known?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

The JavaScript while loop iterates the elements for the infinite number of times, which should be used if number of iteration is not known

 </blockquote>

</details>


---

11. What is the use of `this` keyword in JavaScript?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>


Which refers to the currently calling object. It is commonly used in constructors to assign values to object properties.

 </blockquote>

</details>


---

12. Explain about Callback functions in JavaScript?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>


- In JavaScript, functions are objects and therefore, functions can take other functions as arguments and can also be returned by other functions.
- Callback is a JavaScript function that is passed to another function as an argument or a parameter. This function is to be executed whenever the function that it is passed to gets executed. 


 </blockquote>

</details>


---

13. What do you understand about cookies?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>


It is generally a small data that is sent from a website and stored on the user’s machine by a web browser that was used to access the website. Cookies are used to remember information for later use and also to record the browsing activity on a website.

 </blockquote>

</details>


---

14. How would you create a cookie?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

We can create a cookie as below:

``` java
document.cookie = "key1 = value1; key2 = value2; expires = date";
```
 </blockquote>

</details>


---

15. What method is used to break the cookie value in JavaScript?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

`split()` method to break the cookie value into keys and values.

 </blockquote>

</details>


---

16. Differentiate between let and var?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>


Both let and var are used for variable and method declarations in JavaScript. var keyword is `scoped by function`, the let keyword is `scoped by a block`.

 </blockquote>

</details>


---

17. What do you know about arrow functions in JavaScript? 

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Arrow functions are used to write functions with a short and concise syntax, which does not require a function keyword for declaration. An arrow function can be omitted with curly braces { } when we have one line of code.

```java

const Message= () => {

  console.log("Welcome!");

};
```

 </blockquote>

</details>


---

18. How should we cache the return value of a function?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Memoization is used to cache the return value of a function concerning its parameters, used to speed up the application especially in case of complex, time consuming functions. 

 </blockquote>

</details>


---

19. what is the use of  `constructor function()`?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

It is a function that creates an instance of a class. We can create several objects of the same type by using an object constructor function.

 </blockquote>

</details>


---

20. Explain about the use of promise in JavaScript.


 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

It is an object that may produce value in the future(either a resolved value, or a reason that it's not resolved). It is always in one of the possible states: fulfilled, rejected, or pending. Promises provide an alternative approach for callbacks by reducing the callback and writing the cleaner code.

 </blockquote>

</details>


---

21. How to find the browser which is running the web page?


 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

The window object navigator is used to find the browser which is currently running the web application.

``` java

var browsername = navigator.appName;
console.log(browsername); 
```

 </blockquote>

</details>


---

22. How to redirect the user to a new page?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

 We can use the window object location to redirect the user to the new page by providing the HREF URL link to be redirected.

<code> window.location.href="https://www.dotnettricks.com/" </code>


 </blockquote>

</details>


---

23. What is DOM(Document Object Model)?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

When HTML documents are loaded in the browser(which creates DOM), it will become a document object which is the root element that represents the HTML document. Each DOM element has various properties and methods through which we can add dynamic content to our web page according to the required behavior.

 </blockquote>

</details>


---

24. What do ypu mean by Event and Event handling?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

The change in the state of an object is known as an `Event`. In html, there are various events which represents that some activity is performed by the user or by the browser. When javascript code is included in HTML, js react over these events and allow the execution. This process of reacting over the events is called `Event Handling`. 

 </blockquote>

</details>


---

25. How does HTML events are handled in JavaScript?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

JavaScript handles the HTML events through Event Handlers.

 </blockquote>

</details>


---

26. List the types of events used in JavaScript.

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

27. How to attach an event handler in JavaScript?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

The `addEventListener()` method is an inbuilt function of JavaScript to add multiple event handlers to a particular element without overwriting the existing event handlers.

Syntax:

<code> element.addEventListener(event, function, useCapture);  </code>

 </blockquote>

</details>


---

28. What is the use of JavaScript Strict Mode?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>


- Being a scripting language, sometimes the JavaScript code displays the correct result even it has some errors. To overcome this problem we can use the JavaScript strict mode.

- The JavaScript provides "use strict"; expression to enable the strict mode. If there is any silent error or mistake in the code, it throws an error.

 </blockquote>

</details>


---

29. What method can be used instead of this `document.form1.name.value method`?


 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

we can use the method `document.getElementById()` to get value of the input text. 

 </blockquote>

</details>


---

30. What is the use of `getElementsByClassName()` method?


 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

It is used for selecting or getting the elements through their class name value.

When the method is applied on any particular element, it will search the whole document and will return only those elements which match the specified or given class name.


 </blockquote>

</details>


---

31. List out different types of errors in JavaScript?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

- Run time errors- errors occurred due to misrepresentation of HTML commands.
- Load time errors- errors that occurred at the time of web page loading and may occur due to improper 
  syntaxes
- Logical errors- errors may occur due to improper logical performance of the function.

 </blockquote>

</details>


---

32. How to get an element by class in JavaScript?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

By using  method `Document.getElementsByclass name()`, we can get elements in class name.


 </blockquote>

</details>


---

33.  In how many ways a JavaScript code can be used in an HTML file?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

There are 3 different ways in which a JavaScript code can be involved in an HTML file:

- Inline
- Internal
- External

 </blockquote>

</details>


---

34. Explain about Event Bubbling.

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Whenever an event happens on an element, the event handlers will first run on it and then on its parent and finally all the way up to its other ancestors.

 </blockquote>

</details>


---

35.  Explain about Event Capturing .

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

It is the reverse of the event bubbling and here the event starts from the parent element and then to its child element.

 </blockquote>

</details>


---

36. What do you mean by Promises?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

It is used to handle asynchronous operations in JavaScript, which can handle multiple asynchronous operations easily and provide better error handling than callbacks and events. (handling multiple callbacks at the same time).

 </blockquote>

</details>


---

37. List the states of promises in JavaScript.

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

- fulfilled: Action related to the promise succeeded
- rejected: Action related to the promise failed
- pending: Promise is still pending i.e. not fulfilled or rejected yet
- settled: Promise has fulfilled or rejected


 </blockquote>

</details>


---

38. Explain about Async/Await Function in JavaScript.

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

- Async allows us to write promises based code as if it was synchronous and it checks that we are not 
  breaking the execution thread, which will always return a value.
- Await function is used to wait for the promise. It could be used within the async block only. It makes 
  the code wait until the promise returns a result.


 </blockquote>

</details>


---

39. What is the DOM?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>


Document Object Model(DOM) is a tree-like structure that represents the HTML document. It is used by JavaScript to access and manipulate the document.


 </blockquote>

</details>


---

40. How can we change styles of a particular element using JavaScript?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>


Which can be done by accessing the element’s style property. To change a specific style, set the appropriate property of the style object to the new value.

eg: element.style.color = “new color”;

 </blockquote>

</details>


---

41. Explain about namespace objects in JavaScript?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

It is used to group together related objects, properties, and methods. In JavaScript, the default namespace is the global object. However, you can create your own namespace objects to keep your code organized. 

 </blockquote>

</details>


---

42. Does JavaScript support automatic type conversion?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Yes, it support automatic type conversion. It is the common way of type conversion used by JavaScript developer.

 </blockquote>

</details>


---

43.  What do you mean by variable typing?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Which assigns a number to a variable and then assigns a string to the same variable. For example is a is the varaiable typing here,

a= 6;
a= "JavaScript";

 </blockquote>

</details>


---

44. Differentiate between Local storage & Session storage?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Local Storage – The data is not sent back to the server for every HTTP request , which will reduce the amount of traffic between client and server. 

Session Storage – The data stored in local storage has no expiration time, data stored in session storage gets cleared when the page session ends. Which will leave when the browser is closed.

 </blockquote>

</details>


---

45. How can you convert the string of any base to integer in JavaScript?


 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

The `parseInt()` function is used to convert numbers between different bases. It takes the string to be converted as its first parameter, and the second parameter is the base of the given string.


 </blockquote>

</details>


---

