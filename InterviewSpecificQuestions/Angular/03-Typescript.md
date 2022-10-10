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
- Since we all know that JavaScript is the only language used in client-side scripting as browsers can only understand JavaScript.
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

4. How to install TypeScript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

There are two ways to install typescript:

Using npm (Node Package Manager)
Install the TypeScript plugin in your IDE
```ts
`npm install -g typescript`
```

We can also install a typescript plugin available for our IDE.We can use IDE of our choices such as VS Code, Visual Studio, Atom, or Sublime Text.

</blockquote>
</details>

---

5. Explain the TypeScript program execution?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

TypeScript totally follows the OOPS (Object-Oriented Programming System) concept and with the help of TSC (TypeScript Compiler), we can convert Typescript code (.ts file) to JavaScript (.js file).

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

- A module is a way to construct a local scope in a file. So that all the classes, variables declared in a module are not accessible outside the module.
- We can create a module using the export keyword.
- A module in typescript can be used in another module using the import keyword.

</blockquote>
</details>

---

9. What is a namespace in TypeScript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Using namespace we can group logically related code. A namespace can include classes, interfaces, functions, and variables.
- We can create a namespace in typescript using namespace keyword followed by any valid name.
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

In Typescript, a function can be created as a named function or anonymous function. We can further add types to each of the parameters and to the function as well.

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

This is an additional Type assertion syntax. The reason for including the **as** syntax in typescript was that `<type>` conflicted with JSX.

```ts

let strLength: number= (someString as string).length;
```

</blockquote>
</details>

---

12. Difference between readonly and const?

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

15. Can you explain Rest parameters in Typescript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Sometimes, we want to work with multiple parameters as a group, or we may not know how many parameters a function will ultimately take. In JavaScript, we have something known as arguments. Similarly, we have Rest parameters in typescript.

- Rest parameters are treated as a boundless number of optional parameters. The compiler will build an array of the arguments passed in with the name given after the ellipsis (…)

```ts

function getPlayersList(name:string, ...players: string[]) {
    return name + " " + players.join(" ");
}

let players = getPlayersList("Virat", "MS", "Warner", "Kane", "Ben")
```

</blockquote>
</details>

---

16. What are Generics in TypeScript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Generics in Typescript is no different than generics in other programming languages like Java.
- We can create a class, an interface, or a function that works with different types, without specifying the type upfront.

```ts

function greet(a : T) {
  console.log(`Hi ${a}!`)
}

greet('DS'); //function call

```
- The symbol T identifies a generic type.

</blockquote>
</details>

---

17. What is Modules in TypeScript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- A module is a way to construct a local scope in a file. So that all the classes, variables declared in a module are not accessible outside the module.
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
- In order to use JSX, we must name our file with a .tsx extension and should enable jsx option.

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

20. What is Triple-Slash Directive?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Triple-slash directives are single-line comments containing a single XML tag. The contents of the comments are used as compiler directives.

```ts

 /// <reference path = "filename.ts" />
 ```
- Triple-slash directives are only valid at the top of their containing file.

</blockquote>
</details>

---

21. What is the ts.config file in Typescript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The typescript project will have a ts.config file which provides an infinite number of ways to customize the behavior of the compiler.

</blockquote>
</details>

---

22. Is it possible to compile a typescript file automatically?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Yes, it is possible using --watch option while compiling the typescript file for the first time.

```ts

tsc --watch filename.ts

```

</blockquote>
</details>

---

23. Explain the Declare keyword in Typescript?

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

24. Explain the need for a TypeScript Definition Manager?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- TypeScript Definition Manager (TSD) is a package manager used to search and install typescript definition files directly from the community-driven DefinitelyTyped repository.
- Now, if we want to use some jQuery code in your .ts file:

```ts

$(document).ready(function() { //Your jQuery code });

```
- Here, when we try to compile it by using tsc, it will give a compile-time error: Cannot find the name “$”.
- So, we need to inform the TypeScript compiler that “$” is belongs to jQuery.
- To do this, TSD comes into play. We can download the jQuery Type Definition file and include it in our .ts file.

</blockquote>
</details>

---

25. How to debug a TypeScript file?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- To debug any TypeScript file, we need a .js source map file. So, we have to compile the .ts file with the --sourcemap flag to generate a source map file.
```ts

$ tsc -sourcemap filename.ts

```
- This will create a filename.js and filename.js.map. And the last line of filename.js would be a reference to the source map file.

```ts

//# sourceMappingURL=filename.js.map
```

</blockquote>
</details>

---

26.  How to call base class constructor from child class in TypeScript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

We can call base class constructor using `super()`.

</blockquote>
</details>

---

27. What is Interface in TypeScript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- An `interface` is a virtual structure that only exists within the context of TypeScript. The TypeScript compiler uses interfaces only for type-checking purposes.
- When we define your interface we’re saying that any object (not an instance of a class) given this contract must be an object containing interfaces properties.

</blockquote>
</details>

---

28. When to use interfaces and when to use classes in TypeScript? 

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- If we need/wish to create an instance of perhaps a custom object, whilst getting the benefits of type-checking things such as arguments, return types or generics - a class makes sense. 
- If we’re not creating instances - we have interfaces at our disposal, and their benefit comes from not generating any source code, yet allowing us to somewhat “virtually” type-check our code.

</blockquote>
</details>

---

29. How to declare variable so that it can hold multiple values?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

**Tuples**:
It represents a heterogeneous collection of values. In other words, tuples enable storing multiple fields of different types. Tuples can also be passed as parameters to functions.

**Syntax**
```typescript
let tuple_name = [value1, value2, value3,… value n]
```
Example:
```typescript
let employee: [number, string] = [1, "Priya"]; //create a  tuple 
console.log(employee[0]); // Output: 1
console.log(employee[1]); // Output: Priya

```

</blockquote>
</details>

---

30. What is getters and setters in TypeScript?

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

31.  When to use interface in TypeScript?

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

32. Can u explain a bit about Enum in TypeScript?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Enums or enumerations are a TypeScipt data type that allow us to define a set of named constants. Using enums can make it easier to document intent, or create a set of distinct cases. It is a collection of related values that can be numeric or string values.

**Example**
```typescript
enum Gender {  
  Male,  
  Female  
  Other  
}  
console.log(Gender.Female); // Output: 1  
//We can also access an enum value by it's number value.  
console.log(Gender[1]); // Output: Female  
```

</blockquote>
</details>

---

33. Define Lambda function.

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

34. What does Typescript do when you try to open it in a browser?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- TypeScript cannot be run or understood in any browser. 
- TypeScript need to be compiled (transplied) to JavaScript which any browser can understand. 

</blockquote>
</details>

---
