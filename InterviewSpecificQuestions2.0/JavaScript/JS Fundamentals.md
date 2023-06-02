## Technical

1. What is JavaScript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

JavaScript is a scripting language which is not only used for client-side validation in web application but also evolved and helps to build end to end web applications. It has significant contribution in building diversified platform mobile applications today. 

</blockquote>
</details>

---

2. Mention the different data types present in JavaScript.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

There are two types of data types to hold different types of values in JavaScript. 

- Primitive types- String, Number, Boolean, Undefined, Null
- Non-primitive (reference) data type - Object, Array, RegExp

</blockquote>
</details>

---

3. Do we need to specify the type of the variable in JavaScript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

JavaScript is a <b> dynamic type language </b>, so no need to specify type of the variable because it is dynamically used by JavaScript engine

</blockquote>
</details>

---

4. What are the scopes of a variable in JavaScript and explain them.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>


The scope of a variable represents where the variable has been declared or defined in a JavaScript program. There are two scopes of a variable:

`Global Scope` -Global variables, having global scope are available everywhere in a JavaScript code.

`Local Scope` -The Local Scope has divided into the Function scope, the Block scope, and the Lexical scope.
  - `Function Scope` -The variable declared in a function is only visible inside that function.
  - `Block Scope` -Block scope is the scope of the variables declared inside the {} (curly brackets).
  - `Lexical Scope` -Lexical scope is that a variable defined outside a function can access the inside another function defined after the variable declaration. The inner functions are lexically bound to the execution context of their outer functions.

 </blockquote>

</details>


---

5. Differentiate `undefined` and `not defined`.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

``` java
var x;
console.log(x);
```

Here in the example, we will get a message x is `undefined` which means the variable x is declared and memory is created but the value is not assigned to it.

<code> console.log(y) </code>

In this case, you will get a message like `not defined` because the variable y is not created, and memory is not allocated for it and we try to reference the variable.

</blockquote>

</details>


---

6. What is the use of `typeof` operator?

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

7. Explain Hoisting in JavaScript.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Hoisting is the default behavior of JavaScript where all the variable and function declarations are moved on top, irrespective of where the variables and functions are declared, they are moved on top of the scope. The scope can be both local and global.

</blockquote>
</details>

---

8. When `for loop` should be used in JavaScript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

It iterates the elements for the fixed number of times. It should be used if the number of iterations is known. 

</blockquote>
</details>

---

9. What loop should be used if number of iterations is not known?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

The JavaScript while loop iterates the elements for the infinite number of times, which should be used if number of iteration is not known

</blockquote>
</details>

---

10. What is the use of `this` keyword in JavaScript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Which refers to the currently calling object. It is commonly used in constructors to assign values to object properties.

</blockquote>
</details>

---

11. Differentiate `let` and `var`.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Both let and var are used for variable and method declarations in JavaScript. var keyword is `scoped by function`, the let keyword is `scoped by a block`.

</blockquote>
</details>

---

12. What is difference between `==` vs `===` in JavaScript?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

- `==` is used for comparison between two variables irrespective of the data type of variable. 
- `===` is used for comparison between two variables but this will check strict type, which means it will check datatype and compare two values.
- Example:
 - 5 == '5' // Returns true
 - 5 === '5' // Returns False
</blockquote>
</details>

---

13. What is the use of  `constructor function()`?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

- It is a function that creates an instance of a class. We can create several objects of the same type by using an object constructor function.
- Example
```javascript
//Constructor
function User (name, age) {
    this.name = name;
    this.age = age;
}
var user1 = new User('Bob', 25);
var user2 = new User('Alice', 27);
```
 </blockquote>

</details>

---

14. List out different types of errors in JavaScript?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

- **Run time errors**- errors occurred due to misrepresentation of HTML commands.
- **Load time errors**- errors that occurred at the time of web page loading and may occur due to improper syntaxes
- **Logical errors**- errors may occur due to improper logical performance of the function.

</blockquote>

</details>

---

15. What are the ways a JavaScript code can be used in an HTML file?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

There are two ways:

- `Internal JavaScript:` Writing the code in your HTML file by writing the code inside the `<script> tag`.
- `External JavaScript:` Through an external file having a .js extension and then link the file inside the `<head>` or `<body>` tag of the HTML file.

</blockquote>
</details>

---

16. Does JavaScript support automatic type conversion?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Yes, it support automatic type conversion. It is the common way of type conversion used by JavaScript developer.

</blockquote>
</details>

---

17. Why JavaScript is termed as loosely typed?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

JavaScript is a loosely typed language, so a variable can store any type of value.
```javascript
a= 6;
a= "JavaScript";
```
</blockquote>
</details>

---

18. What are callback functions in JavaScript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

A callback function is a function that is passed as an argument to another function and is invoked or called inside that function. It allows for asynchronous operations and can be used to handle events or execute code after a certain operation completes.

</blockquote>
</details>

---

18. What are arrow functions in JavaScript? 

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Arrow functions are used to write functions with a short and concise syntax, which does not require a function keyword for declaration. An arrow function can be omitted with curly braces { } when we have one line of code.

```javascript

const Message= () => {
  console.log("Welcome!");
};
```

</blockquote>
</details>

---

19. Explain the use of `Promise` in JavaScript.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

It is an object that may produce value in the future(either a resolved value, or a reason that it's not resolved). It is always in one of the possible states: fulfilled, rejected, or pending. Promises provide an alternative approach for callbacks by reducing the callback and writing the cleaner code.

</blockquote>
</details>

---

20. What is the use of JavaScript Strict Mode?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>


- JavaScript is a loosely typed scripting language. 
- JavaScript allows strictness of code by using "use strict"; statement at the top of JavaScript code or in a function.
- For example, when we expect the compiler to give an error if we have used a variable before defining it, then we apply "strict mode" to the JavaScript code.
- The strict mode in JavaScript does not allow us to use undefined variables, reserved keywords as variable or function name, duplicate properties of an object, duplicate parameters of the function, assign values to read-only properties, modifying arguments object, and Deleting an undeletable property.
- Strict mode can be applied to function level in order to implement strictness only in that particular function.

</blockquote>
</details>

---

21. What is BOM in JavaScript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

- BOM means `Browser Object Model`. 
- These are objects that you can use to manipulate the browser. 
- They are `navigator`, `screen`, `location`, `history`, `document`.
- All above mentioned objects are children of the `window` Object.

</blockquote>
</details>

---

22. List the states of `Promise` in JavaScript.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

- fulfilled: Action related to the promise succeeded
- rejected: Action related to the promise failed
- pending: Promise is still pending i.e., not fulfilled or rejected yet
- settled: Promise has fulfilled or rejected

</blockquote>
</details>


---

23. What does async and await keywords do in JavaScript.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

- Async allows us to write promises based code as if it was synchronous and it checks that we are not 
  breaking the execution thread, which will always return a value.
- Await keyword is used to wait for the promise. It could be used within the async block only. It makes 
  the code wait until the promise returns a result.

</blockquote>
</details>

---

24. How do you concatenate strings in JavaScript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

You can concatenate strings in JavaScript using the `+` operator. For example, `var fullName = firstName + ' ' + lastName;` combines the values of `firstName` and `lastName` into `fullName`.

</blockquote>
</details>

---

25. What is the difference between null and undefined in JavaScript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

`null` is an assignment value that represents the intentional absence of an object value, while `undefined` is a variable value that indicates the absence of a value. `null` is assigned by developers, whereas `undefined` is automatically assigned to variables that have been declared but not assigned a value.

</blockquote>
</details>

---

26. How do you loop through an array in JavaScript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

You can loop through an array using various methods, such as `for` loops, `forEach()`, `for...of`, or `for...in`. For example, using a `for` loop: 
```javascript
var array = [1, 2, 3];
for (var i = 0; i < array.length; i++) {
  console.log(array[i]);
}
```
</blockquote>
</details>

---

27. How do you create an object in JavaScript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

You can create an object using object literal notation or by using the `new` keyword. For example:
```javascript
var myObject = {
  key1: value1,
  key2: value2,
};
```
or
```javascript
var myObject = new Object();
myObject.key1 = value1;
myObject.key2 = value2;
```
</blockquote>
</details>

---

28. How do you convert a string to a number in JavaScript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

You can convert a string to a number using the `parseInt()` or `parseFloat()` functions. For example: `var number = parseInt('42');`

</blockquote>
</details>

---

29. What is the relation between ECMAScript and JavaScript?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

- JavaScript is a general-purpose scripting language that conforms to the ECMAScript specification. 
- ECMAScript is a JavaScript standard intended to ensure the interoperability of web pages across different browsers.
- It is standardized by ECMA International in the document ECMA-262.
- The ECMAScript specification is a blueprint for creating a scripting language. 
- JavaScript is an implementation of that blueprint. 
- JavaScript implements the ECMAScript specification as described in ECMA-262.

</blockquote>
</details>

---

30. Explain about namespace objects in JavaScript?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

It is used to group together related objects, properties, and methods. In JavaScript, the default namespace is the global object. However, you can create your own namespace objects to keep your code organized. 

</blockquote>
</details>

---