1. What is TypeScript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- TypeScript is an open-source object-oriented programming language developed and maintained by Microsoft. It is a superset of JavaScript.
- TypeScript is designed for the development of large applications and transpiles to JavaScript.

</blockquote>
</details>

---

2. Why do we need TypeScript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- TypeScript is an attempt to fix JavaScript problems.
- Since we all know that JavaScript is the only language used in client-side scripting browsers can only understand JavaScript.
- Since TypeScript simplifies JavaScript code, making it easier to read and debug. It saves developers time and increases productivity.

</blockquote>
</details>

---

3. What are the advantages of using TypeScript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Advantages of using TypeScript:

- Integrates well with React, Vue, and Angular.
- Is a statically typed language and this makes the code easier to refactor. 
- Is easier to read and access. Helps in code maintainability.
- Has a powerful type system, including generics.
- Statically typed programming languages are those in which the type of a variable is known at compile-time instead of at run-time.

</blockquote>
</details>

---

4. Explain the TypeScript program execution?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

TypeScript follows the OOPS (Object-Oriented Programming System) concept and with the help of TSC (TypeScript Compiler), we can convert Typescript code (.ts file) to JavaScript (.js file).

</blockquote>
</details>

---

5. What OOPs does TypeScript support?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Typescript supports the four object-oriented programming concepts – Abstraction, Polymorphism, Inheritance, and Encapsulation.

</blockquote>
</details>

---

 6. Explain data types in TypeScript?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Typescript supports Any, Built-in, and User-defined data types.
- Any is the superset for all the data types available. It means that the variable could be of any type. It will override the type checking.
- The Built-in types include string, number, boolean, undefined, null, and void.
- The User-defined types include array, enum, interface, class, union, and tuple.

</blockquote>
</details>

---

7. What are modules in TypeScript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- A module is a way to construct a local scope in a file. So that all the classes and variables declared in a module are not accessible outside the module.
- We can create a module using the export keyword.
- A module in typescript can be used in another module using the import keyword.

</blockquote>
</details>

---

8. What is a namespace in TypeScript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Using a namespace we can group logically related code. A namespace can include classes, interfaces, functions, and variables.
- We can create a namespace in typescript using the namespace keyword followed by any valid name.
- For Example:

```ts

namespace MyNamespace {

}
```

</blockquote>
</details>

---

9. What are typed functions in TypeScript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

In Typescript, a function can be created as a named function or an anonymous function. We can further add types to each of the parameters of the function as well.

```ts

// Named function
function add(a: number, b: number) : number {
    return a + b;
}

// Anonymous function
let funcAdd = function(a: number, b: number): number { return a + b; };
```

If we want to write the full type of the function:

```ts

let funcAdd: (a: number, b: number) => number = 
     function (a: number, b: number) : number  { return a + b; };
```
</blockquote>
</details>

---

10. What is **as** syntax in TypeScript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

This is an additional Type of assertion syntax. The reason for including the **as** syntax in typescript was that `<type>` conflicted with JSX.

```ts

let strength: number= (someString as string).length;
```

</blockquote>
</details>

---

11. Difference between reading-only and const?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

const is used on a variable whereas read-only is used on properties of an object.

</blockquote>
</details>

---

12. What are static properties?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Static properties are those that are shared by all the instances of a class and they can be accessed via the class name and dot operator.

```ts

class Singleton {
    static counter = 0;
    constructor() {
        Singleton.counter++;
    }
  }
  
  var singleton = new Singleton();
  console.log(Singleton.counter); //1
```  

</blockquote>
</details>

---

13. Explain access modifiers in Typescript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

There are 3 types of access modifiers in TypeScript: public, private, and protected.

**Public**:
By default, all the members of a class are public in TypeScript.

**Private**:
When any of the class members are declared private, it is only accessible within the class scope.

**Protected**:
The protected members are similar to private access modifiers, except that they are accessible in the derived class.

</blockquote>
</details>

---
 
14.  Define the Lambda function.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- For defining function expressions, TypeScript provides a shortcut syntax. A lambda function is an unnamed anonymous function. 
- **Example**:
```ts
let sum=(a: num, b: num): num=>{ return a+b;}

console.log(sum(5,10)); //returns 15
```
Here, `?=>?` is a lambda operator.

</blockquote>
</details>

---

---

15. Can we use JSX in TypeScript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Yes, JSX is an embeddable XML-like syntax.
- To use JSX, we must name our file with a .tsx extension and should enable the jsx option.

</blockquote>
</details>

---

16. What are Decorators in TypeScript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Decorators are functions that modify a class, property, method, or method parameter. The syntax to define decorators is “@”.
- In other words, Decorators are functions that take their target as the argument.

</blockquote>
</details>

---
 
17. Explain the Declare keyword in Typescript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- The **declare** keyword is used for ambient declarations and methods where we want to define a variable that may exist elsewhere.
- If we want to use any library in our TypeScript code, we can use the following code:

```ts

declare var myAlexaLibrary;

```

</blockquote>
</details>

---

18. Explain the need for a TypeScript Definition Manager?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- TypeScript Definition Manager (TSD) is a package manager used to search and install typescript definition files directly from the community-driven DefinitelyTyped repository.
- Now, if we want to use some jQuery code in your .ts file:

```ts

$(document).ready(function() { //Your jQuery code });

```
- Here, when we try to compile it by using tsc, it will give a compile-time error: Cannot find the name “$”.
- So, we need to inform the TypeScript compiler that “$”belongs to jQuery.
- To do this, TSD comes into play. We can download the jQuery Type Definition file and include it in our .ts file.

</blockquote>
</details>

---
 
19.  How to call the base class constructor from the child class in TypeScript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

We can call the base class constructor using `super()`.

</blockquote>
</details>

---

20. What is Interface in TypeScript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- An `interface` is a virtual structure that only exists within the context of TypeScript. The TypeScript compiler uses interfaces only for type-checking purposes.
- When we define your interface we’re saying that any object (not an instance of a class) given this contract must be an object containing interface properties.

</blockquote>
</details>

---

21. When to use interfaces and when to use classes in TypeScript? 

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- If we need/wish to create an instance of perhaps a custom object, whilst getting the benefits of type-checking things such as arguments, return types, or generics - a class makes sense. 
- If we’re not creating instances - we have interfaces at our disposal, and their benefit comes from not generating any source code, yet allowing us to somewhat “virtually” type-check our code.

</blockquote>
</details>

---

22. What are getters and setters in TypeScript?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- TypeScript supports getters/setters as a way of intercepting accesses to a member of an object. This gives a way of having finer-grained control over how a member is accessed on each object.
```typescript
class Employee {
   
    private _name: string;

    get Name() {
        return this._name;
    }
    set Name(val) {
        this._name = val;
    }
}
```

</blockquote>
</details>

---

23.  When to use the interface in TypeScript?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Interfaces help to achieve Polymorphism.
- An interface is a contract to implement a shape of the data. 
- Use the interface to make it clear that it is intended to be implemented and used as a contract about how the object will be used.
```typescript
interface Bird {
    size: number
    fly(): void
    sleep(): void
}
class Hummingbird implements Bird { ... }
class Bellbird implements Bird { ... }
;
```
---
 
