1. In JavaScript, what is the difference between 'var' and 'let'?
<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Both the `let` and `var` keywords are used to declare variables in JavaScript. The main difference between them is that `var` is function-scoped, while `let` is block-scoped. This means that when you declare a variable with `var` inside a function, it is accessible throughout the entire function, whereas `let` is only accessible within the block it is declared in. `Hoisting` is supported by `var` but not by `let`. Also, we can redeclare a variable in the same scope using `var`, but we can only declare a variable once in the same scope using `let`. 

</blockquote>

</details>

---

2. How do you splice an object?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The `splice()` method in JavaScript is used to add or remove elements from an array. But it can not be used directly on an objcet. So, to perform a similar operation like splice on an object. We can combine the functionalities of `add()` and `delete()` methods.   

</blockquote>

</details>

---

3. What is JSX?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

JSX stands for JavaScript XML, it is a syntax extension in JavaScript that allows you to write HTML in your JavaScript files. It is commonly used with React to define the structure and appearance of components. With JSX, you can use familiar HTML tags to define the structure of your components and JavaScript expressions to add dynamic content. The JSX code is compiled into regular JavaScript using a transpiler like Babel.

</blockquote>

</details>

---

4. What are Arrays in javascript?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

An array is a data structure that holds an ordered list of elements. we can hold elements of any data type, including numbers, strings, objects, and even other arrays in a single array. we can create an array using a square bracket to enclose a list of elements and each element can be accessed and modified using their index numbers. Arrays have built-in methods like `join()`, `pop()`, `push()`, `shift()` and `unshift()` for elements.

</blockquote>

</details>

---

5. How to traverse an array in javascript?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

In JavaScript, you can traverse an `array` using a loop, such as a `for` loop or a `forEach()` method.

For example,

```js
const myArray = [1, 2, 3, 4, 5];

// Using for loop
for(let i = 0; i < myArray.length; i++) {
  console.log(myArray[i]);
}


//Using forEach() method
myArray.forEach(function(element) {
  console.log(element);
});

```
In the first approach, the `for` loop iterates over each element of the array, using the `length` property to determine the number of iterations needed. The loop access each element of an array using the index variable 'i' and logs it to the console. In the second approach, the `forEach()` method iterates over each element of the array and passes it to the callback function, which logs it to the console.

</blockquote>

</details>

---

6. what is an object.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

An object is a collection of related data and/or functionality. It is a non-primitive data type that stores data in key-value pairs, where each key serves as a unique identifier for a value or function. Objects can contain primitive data types, other objects, arrays, and functions. They can be created using object literals, constructors, or classes. Object properties can be added, removed, or modified at runtime making them dynamic in nature. 

</blockquote>

</details>

---

7. how does javaScript handle objects? 

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

In JavaScript, when we create an object, it is stored in memory and a reference to that memory location is assigned to a variable. When we pass or assign an object to a new variable or function, we are actually passing a reference to the same object in memory. This means that if we make any modifications to that object in one place, those changes will be reflected everywhere the object is used.  To create and manipulate objects in JavaScript, we can use various techniques, including `object literals`, `constructors`, `classes`, and built-in object methods. 

</blockquote>

</details>

---

8. How do we write json object? 

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

A JSON object is written using curly braces `{}` to enclose key-value pairs separated by commas. The key and value are separated by a colon `:`. The keys are written in double quotes `"`, and values can be of any JSON-compatible data type.

for example, 
```js
{
  "name": "Sam Doe",
  "age": 24,
  "hobbies": ["reading", "traveling"],
  "address": {
    "street": "Main St",
    "city": "London",,
    "zip": "12345"
  }
}

```


</blockquote>

</details>

---

9. Do we use WSDL with SOAP?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Yes we use WSDL(Web Services Description Language) is with SOAP to describe web services. By using WSDL with SOAP, clients can easily understand the functionality of a web service and generate client code, which simplifies the process of interacting with the service.

</blockquote>

</details>

---

10. What is a client script?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

A client script is a code that runs on the client-side. It enhance the user experience of a web page. Scripting languages like JavaScript are used as client scripts and can perform tasks like validating user input, updating page content dynamically, handling user events, and implementing client-side data storage. 

</blockquote>

</details>

---

11. Difference between observable and subscriber?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

`Observable` is a source of data that emits values over time, while `Subscriber` is an object that receives the data emitted by an `Observable`. The `Observable`can be subscribed by one or more `Subscriber`. `Observable` is lazy and can emit multiple values. The `Subscriber` can request a certain number of values and also can unsubscribe from the Observable to stop receiving the values.

</blockquote>

</details>

---

12. What is the package JSON?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The `package.json` file is a configuration file which is used to define dependencies and metadata like name, version, license in a Node.js application. The mentioned dependencies in the `package.json` file can be installed automatically by running the `npm install` command. Additionally, the package.json file can include other configuration settings like scripts, allowing developers to easily share and distribute their packages..

</blockquote>

</details>

---

13. What is the render method?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The `render()` method is used in React and Vue.js to define the view of a component. It generates a virtual representation of HTML elements and their properties to be displayed on the web page. The method updates the component's view whenever there is a change in the data or state of the component.

</blockquote>

</details>

---

14. 

<details><summary><b> Show Answer</b></summary>
  
<blockquote>



</blockquote>

</details>

---

15. Hoisting in JavaScript

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Hoisting is a JavaScript behavior where variable and function declarations are moved to the top of their respective scopes during the compilation phase, before the code is executed. This means that it is possible to use a variable or function before it has been declared in the code. However, only the declarations are hoisted, not the assignments or initializations.

For example,

```js
console.log(a); // Output: undefined
var a = 10;

foo(); // Output: "Hello!"
function foo() {
  console.log("Hello!");
}
```

</blockquote>

</details>

---

16. Datatypes in Javascript?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

In JS, we have primitive datatypes like `Number`, `String`, `Boolean`, `Undefined`, `Null`, `Symbol`, and non-primitive datatypes like `Object`.

</blockquote>

</details>

---

17. What is the difference between a var, let, and const in JavaScript? 

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The `let`, `var` and `const` keywords are all used for variable declaration, but they have some differences:
- `var` has function scope or global scope and can be re-declared and reassigned. It also supports hoisting.
- `let` and `const` have block scope and cannot be re-declared within the same block. Both `let` and `var` do not support hoisting.
- `let` can be reassigned, while `const` cannot be reassigned, but the properties or elements of an object or array assigned to it can be modified.
It is advised to use `let` and `const` over `var`.

</blockquote>

</details>

---

18. What is the difference between a map and reduce? 

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The map and reduce are higher-order functions that are used to perform operations on an array. The `map()` method is used to perform operation on each element of an array like if we want to add one in each element of the array we can use the `map()` method. The `map()` method returns a new array with the modified values. The syntax of `map()` method is given below,

```js
demoArray.map(function(currentValue, index, arr), thisValue)

```

The `reduce()` function is used to perform an operation on each element of an array, resulting in a single output value. we can use the `reduce()` method in tasks like calculating the sum of all the elements present in an array.

```js
demoArray.reduce((accumulator, currentValue) => {}, initialValue);
```

</blockquote>

</details>

---

19. What is an async-function?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

An async function is used to write a function that will handle asynchronous calls. The async functions are declared using `async` keyword. In simple terms, the async function will wait for an operation to get completed, without blocking the execution of the rest of the code. The async function returns a promise. We use the `await` keyword to wait for a promise to resolve or reject before continuing the execution of the code.

For example, 

```js

function waitFor1Second() {
  return new Promise(resolve => {
    setTimeout(() => {
      resolve('resolved');
    }, 1000);
  });
}

async function asyncCallDemo() {
  console.log('asyncCallDemo');
  const result = await waitFor1Second();
  console.log(result);
  // Expected output: "resolved"
}

asyncCallDemo();

```

</blockquote>

</details>

---

20. What is a callback function?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

A function which is passed as an argument to another function is called a callback function. The callback function will get executed once a particular task in completed. It is mainly used to handle asynchronous operations.

</blockquote>

</details>

---

21. What is a closure?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>



</blockquote>

</details>

---

22. Tell me about JavaScript?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>



</blockquote>

</details>

---

23. What is state?  

<details><summary><b> Show Answer</b></summary>
  
<blockquote>



</blockquote>

</details>

---

24. How do you get the current state? 

<details><summary><b> Show Answer</b></summary>
  
<blockquote>



</blockquote>

</details>

---

25.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>



</blockquote>

</details>

---
