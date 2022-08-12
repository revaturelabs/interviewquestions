## Technical

1. What is Assertions?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

>- It is to compare the actual result and excepcted result to evaluate whether the executed testcase is 
  pass or fail.
  <img width="708" alt="Capture2" src="https://user-images.githubusercontent.com/92523245/184349147-a2fcf3a9-99c8-4e43-b247-f8f968f307fe.PNG">

>- All assertion methods are avaialable in JUnit `assert` class.So we need to import assert class in 
  JUnit as below. 

`@import static org.junit.Assert.*;`

</details>

--- 

2. List all the default assert methods in JUnit.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

>- `assertEquals`
>- `assertArrayEquals`
>- `assertNull`
>- `asserNottNull`
>- `assertSame`
>- `assertNotSame`
>- `assertTrue`
>- `assertFalse`

</details>

---

3. What will happen if assertion fails when it is execute?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

>JVM throws an error called <b>AssertionError</b> when the assertion fails while executing.

</details>

---

4. Write the syntax for declaring the assert methods?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Assert methods should be with boolean expression in two different ways

- `assert expression;`
- `assert expression1 : expression2;`

</blockquote>

</details>

---

5. Write the syntax for enabling assertion statement in Java source code?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

- By default assertions methods are disbled. To make it enabled need to run the below code
 `java –ea Test` or `java –enableassertions Test`

</blockquote>

</details>

---

6. What should we do,if we want to check all the asserts in a testcase even if a asserts fails in execution?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

- We can use `assertAll` method to ensure that all asserts are checked.
- <b>Example:</b>
``` java
@Test
void groupedAssertions() {
    Address address = new Address();
    assertAll("address name",
        () -> assertEquals("Andrew", address.getFirstName()),
        () -> assertEquals("User", address.getLastName())
    );
}
```
</blockquote>
<details><summary> Explanation </summary>

<blockquote>

- The two assertEquals method will exceute even if a assert fails , because of assertAll method in the testcase.

</blockquote>

</details>

</details>

---

7. How to disable assertions using a command?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Use the below command to disable assertions 

`java –da arguments`

Or

`java –disableassertions arguments`

</blockquote>

</details>

---
8. Can we catch an assertion error?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Yes 

</blockquote>

<details><summary> Explanation </summary>

<blockquote>

By declaring the assertion statement in the try block with the message to be displayed and catch the assertion error in the catch block.

</blockquote>

</details>

</details>

---

9. Differentiate between assertions and exception handling.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

- An exception is an abnormal event that occurs during the execution of the program and disrupts the normal flow of the program. 
- Assertion enables you to test your assumptions about the program logic, contains a boolean expression  will be true when the program executes. If it is not true, the JVM will throw an `AssertionError`.

</blockquote>

</details>

---

## Problem Solving

10. What will be the output of the program?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)


<blockquote>

``` java

public class Test 
{  
    public static void main(String[] args) 
    { 
        int x = 0;  
        assert (x > 0) ? "assertion failed" : "assertion passed" ; 
        System.out.println("finished");  
    } 
}
```
</blockquote>

<details><summary> Show Answer </summary>

<blockquote>

Compilation Fails

</blockquote>

<details><summary> Explanation </summary>

<blockquote>

We can't use the Assert statement as like ternary operator.Returns `incompatible types: bad type in conditional expression`.

</blockquote>

</details>

</details>

---

