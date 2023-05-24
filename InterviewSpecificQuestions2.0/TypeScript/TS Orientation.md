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

5. Explain the TypeScript program execution?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

TypeScript follows the OOPS (Object-Oriented Programming System) concept and with the help of TSC (TypeScript Compiler), we can convert Typescript code (.ts file) to JavaScript (.js file).

</blockquote>
</details>

---

6. What OOPs does TypeScript support?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Typescript supports the four object-oriented programming concepts – Abstraction, Polymorphism, Inheritance, and Encapsulation.

</blockquote>
</details>

---

 07. Explain data types in TypeScript?

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

8. What are the modules in TypeScript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- A module is a way to construct a local scope in a file. So that all the classes and variables declared in a module are not accessible outside the module.
- We can create a module using the export keyword.
- A module in typescript can be used in another module using the import keyword.

</blockquote>
</details>

---

9. What is a namespace in TypeScript?

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

10. What are typed functions in TypeScript?

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

11. What is **as** syntax in TypeScript?

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

12. Difference between reading-only and const?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

const is used on a variable whereas read-only is used on properties of an object.

</blockquote>
</details>

---

13. What are static properties?

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

14. Explain access modifiers in Typescript?

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
 
 17. What are Modules in TypeScript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- A module is a way to construct a local scope in a file. So that all the classes and variables declared in a module are not accessible outside the module.
- We can create a module using the export keyword.
- A module in typescript can be used in another module using the import keyword.

```ts

export class Student {
    readonly Id: number;
    Name: string;
    
    constructor(id: number, name: string) {
        this.Id = id;
        this.Name = name;
    }
}

let Subject: string = "Computer Science";
```

</blockquote>
</details>

---

18. Can we use JSX in TypeScript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Yes, JSX is an embeddable XML-like syntax.
- To use JSX, we must name our file with a .tsx extension and should enable the jsx option.

</blockquote>
</details>

---

19. What are Decorators in TypeScript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Decorators are functions that modify a class, property, method, or method parameter. The syntax to define decorators is “@”.
- In other words, Decorators are functions that take their target as the argument.

</blockquote>
</details>

---
