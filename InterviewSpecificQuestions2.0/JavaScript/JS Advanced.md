## Technical
1. Explain about Callback functions in JavaScript?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>


- In JavaScript, functions are objects and therefore, functions can take other functions as arguments and can also be returned by other functions.
- Callback is a JavaScript function that is passed to another function as an argument or a parameter. This function is to be executed whenever the function that it is passed to gets executed. 


 </blockquote>

</details>


---
2. What do you know about arrow functions in JavaScript? 

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
3. Explain the use of `Promise` in JavaScript.


 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

It is an object that may produce value in the future(either a resolved value, or a reason that it's not resolved). It is always in one of the possible states: fulfilled, rejected, or pending. Promises provide an alternative approach for callbacks by reducing the callback and writing the cleaner code.

 </blockquote>

</details>


---
4. What is the use of JavaScript Strict Mode?

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
5. What is meaning of BOM in JavaScript?

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
6. List the states of `Promise` in JavaScript.

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

7. Explain about Async/Await Function in JavaScript.

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

