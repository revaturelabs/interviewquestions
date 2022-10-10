1. What does `ng test` do?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

The `ng test` command builds the application in watch mode, and launches the Karma test runner. 

</blockquote>
</details>
  
---

2. What are the testing files in Angular?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

The test file extension **must be `.spec.ts`** so that tooling can identify it as a file with tests (also known as a spec file).

</blockquote>
</details>
  
---

3. Have you heard of Jasmine? Explain a bit.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

- Jasmine is free and open-source Behavior Driven Development (BDD) framework.
- Using Jasmine, one can perform test cases similar to user behavior on a website. It is very beneficial for front-end testing.

</blockquote>
</details>
  
---

4. What does Karma do for?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

Karma is a task runner for our tests. It allows the users to execute their Jasmine test codes in multiple real-time browsers from the command line. This command-line also displays the result of the tests. It watches the files for changes and re-runs the tests automatically. By default, Angular runs on Karma.

</blockquote>
</details>
  
---

5. How to write a unit test in Angular?


![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details>
<summary><b>Show Answer</b></summary>
<blockquote>

The Angular testing package includes two utilities called `TestBed` and `async`. `TestBed` is the main utility package. 

There are three main methods in this test file:

- `describe()` – It’s a suite of Test scripts that calls a global Jasmine function with two parameters: a string and a function. It also consists of beforeEach block.
- `it()` – It’s the smallest unit test case that is written to be executed, which calls a global Jasmine function with two parameters: a string and a function. Multiple `it()` statements can be written inside the `describe()`
- `expect()` – Every `it()` statement has a `expect()` function which takes a value and expects a return in true form

</blockquote>
</details>
  
---
