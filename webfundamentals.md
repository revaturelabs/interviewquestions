1. What are some features of JavaScript?

<details> <summary>Show Answer</summary>
 
<blockquote>

JavaScript is a popular programming language used for both front-end and back-end development. Here are some of its key features:

**1. Object-oriented:** JavaScript is an object-oriented programming language, which means it uses objects to represent and manipulate data.

**2. Dynamic:** JavaScript is a dynamic language, which means that variables can be declared and assigned without specifying a data type.

**3. Interpreted:** JavaScript is an interpreted language, which means that code is executed directly by the browser or runtime environment without the need for compilation.

**4. Event-driven:** JavaScript is an event-driven language, which means that it responds to user actions such as clicks and scrolls by executing specific code.

**5. Versatile:** JavaScript can be used for both front-end and back-end development, allowing developers to build full-stack applications.

**6. Cross-platform:** JavaScript can run on a variety of platforms, including web browsers, servers, and mobile devices.

**7. Large ecosystem:** JavaScript has a large ecosystem of libraries and frameworks, including React, Angular, and Node.js, that make it easier to build complex applications.

In summary, JavaScript is an object-oriented, dynamic, interpreted, event-driven, versatile, cross-platform language that is easy to learn and has a large ecosystem of libraries and frameworks.


  
</blockquote>

</details>

2. What is async/await in javascript?

<details> <summary>Show Answer</summary>
 
<blockquote>

- Async/await is a feature in JavaScript that allows asynchronous code to be written in a synchronous style, making it easier to read and write
- In traditional asynchronous JavaScript programming, callbacks and promises are used to handle asynchronous code. However, this can lead to callback hell or deeply nested promise chains, which can make code difficult to read and maintain.
- Async/await provides a way to write asynchronous code that looks and behaves like synchronous code. It allows the use of the async keyword to define a function that returns a promise, and the await keyword to pause the execution of the function until the promise is resolved or rejected.
  
</blockquote>

</details>

3. Diff between == and === in JS?

<details> <summary>Show Answer</summary>
 
<blockquote>

In JavaScript, "==" and "===" are both comparison operators, but they have different behavior.

- The "==" operator is known as the equality operator and compares the values on either side for equality, after performing type coercion if necessary. This means that if the values are of different types, JavaScript will try to convert one of them to match the other before performing the comparison. 

For example:

```js
1 == '1' // true
```

In this example, the string '1' is converted to a number before the comparison is made.

- The "===" operator is known as the strict equality operator and compares the values on either side for equality without performing type coercion. This means that the values must be of the same type to be considered equal. For example:

```js
1 === '1' // false
```
In this example, the values are of different types, so they are not considered equal.

- In general, it is recommended to use the "===" operator whenever possible, as it avoids unexpected behavior that can result from type coercion. However, there may be cases where the "==" operator is more appropriate, such as when comparing values of different types that can be safely coerced, or when comparing values that may be null or undefined.
</blockquote>

</details>

4. What's a mediaQuery?

<details> <summary>Show Answer</summary>
 
<blockquote>

- A media query is a feature in CSS that allows styles to be applied based on the characteristics of the device or screen on which a web page is being viewed. With media queries, web developers can create responsive designs that adapt to different screen sizes and devices.

- A media query consists of a media type, such as "screen" or "print", and one or more expressions that define the characteristics of the device, such as its width or resolution.
  
</blockquote>

</details>

5. How do you use CSS class in HTML?

<details> <summary>Show Answer</summary>
 
<blockquote>

To use a CSS class in HTML, you need to define the class in a CSS stylesheet and then apply it to the HTML element using the class attribute. 

example:

1. Define the CSS class in a stylesheet:
```css
.my-class {
  font-size: 16px;
  color: #333;
}
```
2. Apply the class to an HTML element using the class attribute:

```html
<p class="my-class">This text will be styled using the "my-class" CSS class.</p>
```
In this example, the CSS class "my-class" is defined in a stylesheet with the font-size and color properties. Then, the class is applied to a paragraph element using the class attribute, which styles the text inside the element according to the properties defined in the CSS class.

  
</blockquote>

</details>

6. What is responsive UI?

<details> <summary>Show Answer</summary>
 
<blockquote>
  
  Responsive UI (User Interface) is an approach to designing and developing user interfaces that provide an optimal viewing and interaction experience across a wide range of devices and screen sizes. The goal is to ensure that the user interface adapts to the device on which it is being viewed.

</blockquote>

</details>

