1. Angular data binding.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Angular supports one way data binding and two way data binding. 

</blockquote>

</details>

---
There are four types of data binding in Angular:

Interpolation: Interpolation is a one-way data binding that allows you to display component data in the view. It is denoted by double curly braces {{ }} and can be used to display variables, expressions, and even method calls.

Property binding: Property binding is another one-way data binding technique that allows you to bind a component property to an HTML element property. It is denoted by square brackets [ ] and allows you to set the value of a property based on the component's data.

Event binding: Event binding is a one-way data binding technique that allows you to respond to user events such as button clicks, mouse clicks, or keyboard events. It is denoted by parentheses ( ) and allows you to call a method in the component when an event occurs.

Two-way binding: Two-way data binding is a two-way data binding technique that allows you to bind a component property to an HTML element property and update both the component and the view when either one changes. It is denoted by square brackets and parentheses [( )] and allows you to keep both the view and the component data in sync.

In summary, data binding is a powerful feature in Angular that makes it easy to create dynamic and interactive web applications. Understanding the different types of data binding is key to building successful applications with Angular.


2. what is ngModel

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

ngModel is an Angular directive that provides two-way data binding between a form control element and a component's property. It allows you to bind an input, select, or textarea element to a component property, and automatically updates the component property when the user interacts with the form control, and vice versa.

</blockquote>

</details>

---


3. observables vs. promises

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Promises:

Promises are an ES6 feature that allows you to handle asynchronous code in a more synchronous way.
Promises represent a single value or an error that will be available in the future.
Promises can be in one of three states: pending, fulfilled, or rejected.
Promises can only be resolved or rejected once.
You can chain multiple promises using .then() and .catch() methods.
Promises are not cancellable once they are initiated.
Observables:

Observables are a feature of RxJS library that allows you to handle asynchronous code in a more flexible way.
Observables can represent a stream of multiple values that will be available in the future.
Observables can emit values multiple times.
Observables can be subscribed to and can emit values asynchronously over time.
Observables can be transformed and combined using operators.
Observables are cancellable using the unsubscribe() method.
In summary, Promises are useful for handling a single asynchronous operation that will complete in the future, while Observables are useful for handling streams of asynchronous data that may emit values over time. Observables provide more flexibility and can be cancelled, transformed, and combined using operators.


</blockquote>

</details>

---


4. what is Node and why it's used.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Node.js, commonly referred to as Node, is an open-source, cross-platform JavaScript runtime environment built on the V8 JavaScript engine of Google Chrome. It allows developers to run JavaScript on the server-side to build fast, scalable, and high-performance network applications.

Node.js uses an event-driven, non-blocking I/O model, which makes it ideal for building applications that require real-time data processing, such as chat applications, gaming, and streaming services. It also makes it possible to handle a large number of connections with less overhead than traditional server-side technologies, such as PHP or Java.

Node.js provides a rich set of built-in modules that simplify the development of web applications, including HTTP, File System, Stream, and OS. In addition to the built-in modules, Node.js has a vast ecosystem of third-party modules available through the npm (Node Package Manager) registry. These modules enable developers to quickly and easily add functionality to their applications.

Node.js is used in a wide range of applications, including web applications, mobile applications, desktop applications, IoT (Internet of Things), and cloud applications. It is also popular for building microservices, APIs, and serverless applications. Many large companies, such as Netflix, LinkedIn, Walmart, and PayPal, use Node.js to power their applications and services.

</blockquote>

</details>

---


5. what are promises

<details><summary><b> Show Answer</b></summary>
  
<blockquote>
Promises are a feature of JavaScript that allow you to handle asynchronous code in a more synchronous way. They were introduced in ES6 (ECMAScript 2015) and are now a core part of the JavaScript language.

A Promise is an object that represents a value that may not be available yet, but will be at some point in the future. It is a placeholder for a future value, or for a future error. Promises can have one of three states: pending, fulfilled, or rejected.

When a Promise is pending, it means that the operation it represents is still in progress and the result is not yet available. When a Promise is fulfilled, it means that the operation has completed successfully, and the result is available. When a Promise is rejected, it means that the operation has failed, and an error is available.

Promises are created using the Promise constructor, which takes a function as an argument. The function takes two parameters: resolve and reject. resolve is a function that is called when the operation is successful, and reject is a function that is called when the operation fails.

Promises have two main methods for handling their results: then() and catch(). The then() method is used to handle the successful completion of a Promise, and the catch() method is used to handle any errors that occur.


</blockquote>

</details>

---

6. what are callback functions.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>



</blockquote>

</details>

---

7. What is the declarations in app module?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>



</blockquote>

</details>

---

8. Passing and binding data in Angular?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>



</blockquote>

</details>

---

9. what is the decorator of a module in angular

<details><summary><b> Show Answer</b></summary>
  
<blockquote>



</blockquote>

</details>

---

10. What are some features you used in Angular?;

<details><summary><b> Show Answer</b></summary>
  
<blockquote>



</blockquote>

</details>

---

11. Create a class component which has an element in it with onClick attribute and a function that is called when that element is clicked

<details><summary><b> Show Answer</b></summary>
  
<blockquote>



</blockquote>

</details>

---

12. What is Angular? What is an SPA?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>



</blockquote>

</details>

---

13. What are components in angular?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>



</blockquote>

</details>

---

14. How do you get data in Angular to your application using another application’s API?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>



</blockquote>

</details>

---

15. What is an observable in Angular?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>



</blockquote>

</details>

---


16. What are some commands in Angular?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>



</blockquote>

</details>

---


17. How do you do two-way data binding?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>



</blockquote>

</details>

---


18. What are pipe transform interfaces and have you ever used them? 

<details><summary><b> Show Answer</b></summary>
  
<blockquote>



</blockquote>

</details>

---


19. How do you use ngfor in Angular? 

<details><summary><b> Show Answer</b></summary>
  
<blockquote>



</blockquote>

</details>

---


20. they asked a question on angular hooks but i told them we did not do hooks.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>



</blockquote>

</details>

---


21. What directives did you use in Angular and what do they do?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>



</blockquote>

</details>

---


22. what is a promise.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>



</blockquote>

</details>

---


23. What is a component?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>



</blockquote>

</details>

---

24. The exact syntax for filling in a form and submitting the form in HTML, then how to set up a call from the TS file in the front end to the backend, then how do you call the backend with that. 

<details><summary><b> Show Answer</b></summary>
  
<blockquote>



</blockquote>

</details>

---

25. How do you start a server in angular?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>



</blockquote>

</details>

---

26. What is dependency injection?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>



</blockquote>

</details>

---

27. Do you know states and props in Angular?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>



</blockquote>

</details>

---

28. Do you know lazy loading (Angular)?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>



</blockquote>

</details>

---

29. I was asked all kinds of questions about Angular, its components & templates, npm, directives, route guards, libraries, etc. I was asked about "parallel queries" in SQL, which I had not heard before, but figured it might be another term for multiple query, as with unions and views. 

<details><summary><b> Show Answer</b></summary>
  
<blockquote>



</blockquote>

</details>

---

30. List some decorators in Angular

<details><summary><b> Show Answer</b></summary>
  
<blockquote>



</blockquote>

</details>

---

31. Difference between AngularJS and Angular

<details><summary><b> Show Answer</b></summary>
  
<blockquote>



</blockquote>

</details>

---

32. How does routing work in the UI layer?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>



</blockquote>

</details>

---

33. How do you handle an exception in the UI layer? (like, how would you handle an exception in angular?)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>



</blockquote>

</details>

---

34. What is TypeScript?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>



</blockquote>

</details>

---

35. What is the apply() method?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>



</blockquote>

</details>

---

36. What is bind()?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>



</blockquote>

</details>

---

37. How would you create a component in Angular?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>



</blockquote>

</details>

---

38. How would you create a module?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>



</blockquote>

</details>

---

39. What file do you edit for dependencies?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>



</blockquote>

</details>

---


40. What is the angular life cycle?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>



</blockquote>

</details>

---
