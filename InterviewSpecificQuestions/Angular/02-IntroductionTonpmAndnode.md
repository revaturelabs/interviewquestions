1. Why we need Node.js for Angular?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

- We use Node.js and npm as tools for building Angular or React apps. 
- Angular is a front-end framework used to create a web application and is written in **Typescript**. 
- The **browser only understands JavaScript code**, so we need to compile Typescript (.ts file) to plain JavaScript (.js file). 
- We use Node.js and npm to perform this compilation, then we can deploy them in production.

</blockquote>
</details>
  
---

2. How do you install node and npm?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

- Download Node.js from nodejs.org and install it. 
- The npm CLI gets installed with Node.js by default. 
- To check that you have installed npm, run `npm -v` in a  terminal. 
- **NOTE:** npm can install packages in a node_modules folder in angular working directory.

</blockquote>
</details>
  
---

3. What is the use of Node.js?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>
  
- Node.js is an open-source, cross-platform run-time environment built on Chrome's V8 JavaScript engine.
- Node.js is used to execute JavaScript code outside of a web browser. It provides a library of various JavaScript modules, which simplifies the development of web applications.
- Global companies like Netflix, Facebook, Walmart Linkedin, Uber, etc., use Node.js for building their applications. 
  
</blockquote>

</details>
  
---

4. What is NPM?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>
 
- NPM stands for Node Package Manager, responsible for managing all the packages and modules for Node.js.

- Node Package Manager provides two main functionalities:
    - Provides online repositories for node.js packages/modules, which are searchable on search.nodejs.org
    - Provides command-line utility to install Node.js packages and also manages Node.js versions and dependencies  
  
</blockquote>

</details>
  
---

5. What is the difference between Angular and Node.js?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

|                           Angular                           |                                 Node.js                                 |
|:-----------------------------------------------------------:|:-----------------------------------------------------------------------:|
|            It is a frontend development framework           |                     It is a server-side environment                     |
|                 It is written in TypeScript                 |                    It is written in C, C++ languages                    |
| Used for building single-page, client-side web applications | Used for building fast and scalable server-side networking applications |
 
</blockquote>

</details>
  
---

6. How do you check whether Node.js installed successfully in your system?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

To check the node.js is install, open power shell or command prompt (cmd) and type `node –v`. If the node.js is install properly in your system print something like that v4.4.3.

</blockquote>
</details>
  
---
 
7. What kind of information we can find in `package.json` file?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

 `package.json` file used to store the metadata related to the project such as a project description, the version of the project in a particular distribution, license information, as well as to store the list of dependency packages.

</blockquote>
</details>
  
---
 
8. Differentiate `dependencies` and `devDependencies` in the `package.json` file?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

In `package.json`, regular `dependencies` are packages that are required for your production-ready site or app to work. Production-ready means the online version of your website or app that the audience experiences.

`devDependencies` are packages used for development purposes, e.g for running tests or transpiling your code.

</blockquote>
</details>
  
---
 
9. What happens if I run `npm install` in the terminal?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

`npm install` command is used for installing JavaScript packages on your local computer.

</blockquote>
</details>
  
---
 
10. What happens if I run `npm uninstall` in the terminal

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

`npm uninstall` command is used to remove installed npm packages on your computer.

</blockquote>
</details>
  
---
 
11. Differentiate between `npm update` and `npm update -g` command?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

`npm update` command is used to update the node package manager to the latest version.
  
It will also install missing packages.

If the -g flag is specified, this command will update globally installed packages.

If no package name is specified, all packages in the specified location (global or local) will be updated.
  
</blockquote>
</details>
  
---
 
12. What happens if I run `npm init` in the terminal?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

The `npm init` command in the JSON language creates a package.json file for your project’s frontend. 

</blockquote>
</details>
  
---
 
13. Can I run angular application using `npm start` command?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details>
<summary><b>Show Answer</b></summary>
<blockquote>

 Yes, it can run angular application.

</blockquote>
</details>
  
---
 
14. Why do we need `package.json` file?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

`package.json` contains just JSON. The main purpose of this file is to hold various metadata related to the project. The file is used to provide the information to the node package manager (NPM) that allows identifying the project and its dependencies.

</blockquote>
</details>
  
---

15. Where you can find `package.json` file?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

The `package.json` file is normally present at the root directory of a project folder structure.

</blockquote>
</details>
  
---

