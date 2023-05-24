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

We can also install a typescript plugin available for our IDE. We can use the  IDE of our choice such as VS Code, Visual Studio, Atom, or Sublime Text.

</blockquote>
</details>

---

21. What is the ts. config file in Typescript?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The typescript project will have a ts. config file which provides an infinite number of ways to customize the behavior of the compiler.

</blockquote>
</details>

---

22. Is it possible to compile a typescript file automatically?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Yes, it is possible to use -the watch option while compiling the typescript file for the first time.

```ts

tsc --watch filename.ts

```

</blockquote>
</details>

---

25. How to debug a TypeScript file?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- To debug any TypeScript file, we need a .js source map file. So, we have to compile the .ts file with the –source map flag to generate a source map file.
```ts

$ tsc -source map filename.ts

```
- This will create a filename.js and filename.js.map. And the last line of filename.js would be a reference to the source map file.

```ts

//# sourceMappingURL=filename.js.map
```

</blockquote>
</details>

---

34. What does Typescript do when you try to open it in a browser?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- TypeScript cannot be run or understood in any browser. 
- TypeScript needs to be compiled (translated) to JavaScript which any browser can understand. 

</blockquote>
</details>

---

