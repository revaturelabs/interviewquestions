1. Can you explain the Rest parameters in Typescript?

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

2. What are Generics in TypeScript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Generics in Typescript is no different from generics in other programming languages like Java.
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

3. How to declare a variable so that it can hold multiple values?

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
let employee: [number, string] = [1, "Priya"]; //Create a  tuple 
console.log(employee[0]); // Output: 1
console.log(employee[1]); // Output: Priya

```

</blockquote>
</details>

----

