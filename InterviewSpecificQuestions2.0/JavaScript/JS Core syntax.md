## Technical
1. What type of language is JavaScript?

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

3. Do we need to specify type of the variable in JavaScript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

JavaScript is a <b> dynamic type language </b>, so no need to specify type of the variable because it is dynamically used by JavaScript engine

 </blockquote>

</details>


---

4. Explain about the scopes of a variable in JavaScript?

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

5. Differentiate between the terms undefined and not defined.

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

8. When ‘for loop’ should be used in JavaScript?

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
11. Differentiate between `let` and `var`?

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

13. what is the use of  `constructor function()`?

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
15.  In how many ways a JavaScript code can be used in an HTML file?

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

17.  What do you understand by loosely typed in JavaScript?

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
