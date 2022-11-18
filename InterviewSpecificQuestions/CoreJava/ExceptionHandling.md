1.Brief us on Exception Handling (or) What is an exception?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1">
  <summary> <b>Show Answer</b></summary>
  
<blockquote markdown="1">

An exception is an error event that can happen during the execution of a program and disrupts its normal flow.

Exceptions in Java can arise from different kinds of situations such as wrong data entered by the user, hardware failure, network connection failure, or a database server that is down.The code that specifies what to do in specific exception scenarios is called exception handling.

 
</blockquote>
</details>

--- 

2.What is the difference between Throws and Throws?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1">
  <summary> <b>Show Answer</b></summary>
  
<blockquote markdown="1">

|                                       throw                                       |                                                                          throws                                                                         |
|:---------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------------------------------------------:|
| Used inside a method when it is required to throw an Exception logically.     | Used in the method signature when the method has some statements that can lead to exceptions                                                            |
| Used to throw an exception explicitly.It can throw only one exception at a time.| Used to declare multiple exceptions, separated by a comma.When an exception occurs, it matches with the declared ones, and throws an exception automatically |
| Syntax: throw new Exception()                                                     | Syntax: public static void writeToFile() throws Exception {}                                                                                            |

 
</blockquote>
</details>

--- 

3.How to handle class not found exceptions?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1">
  <summary> <b>Show Answer</b></summary>
  
<blockquote markdown="1">

Java ClassNotFoundException occurs when the application tries to load a class but Classloader is not able to find it in the classpath.It is a checked exception, so it needed to be handled.

To fix ClassNotFoundException, firstly we must go through the exception stack trace.Then,
- Make sure, you've specified the exact classpath.
- Check for classpath settings and make sure the class it’s present at runtime.
- Verify the requesting Class name is correct.
 
</blockquote>
</details>

--- 

4.Brief us on the keywords - final, finally & static 

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1">
  <summary> <b>Show Answer</b></summary>
  
<blockquote markdown="1">

 - final is the keyword and access modifier which is used to apply restrictions on a class, method, or variable.

 - finally, the block in Java Exception Handling executes important code whether the exception occurs or not.

 - static keyword is used to create a class-level variable in java.static variables and methods are part of the class, not the instances of the class.
 
</blockquote>
</details>

--- 


5.Brief us on Errors

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1">
  <summary> <b>Show Answer</b></summary>
  
<blockquote markdown="1">

- Errors represent irrecoverable conditions such as Java virtual machine (JVM) running out of memory, memory leaks, stack overflow errors, library incompatibility, infinite recursion, etc.

- Errors are usually beyond the control of the programmer and we should not try to handle errors.
 
</blockquote>
</details>

--- 

6.What is the difference between final and finally?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1">
  <summary> <b>Show Answer</b></summary>
  
<blockquote markdown="1">
 
final is a keyword and it can be used to mark a variable "unchangeable".It is used to apply restrictions on class, method and variable.A final class can't be inherited, the final method can't be overridden and the final variable value can't be changed.

Finally is a code block.It is used with a try-catch block for handling exceptions.Finally, a code block will be executed whether an exception is handled or not
 
</blockquote>
</details>

--- 

7.Tell us about the various kinds of exceptions.What are some examples of checked and unchecked exceptions?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1">
  <summary> <b>Show Answer</b></summary>
  
<blockquote markdown="1">
 There are 2 types of exceptions

- **Checked Exception(java.lang.Exception)** -> This exception forces the programmer to handle it at the compile time itself, until the programmer handles it, the compiler won’t allow it to run.Some of the Checked exceptions are FileNotFoundException, ClassNotFoundException,MethodNotFoundException, SQLException, etc.,

- **Unchecked Exceptions(java.lang.RuntimeException)** -> These exceptions occur at a run time, it is up to the programmer whether he wants to handle this or not, if he doesn’t handle it, it will lead to abnormal termination.Some of the unchecked exceptions are ArithmeticException, NullPointerException,ArrayIndexOutOfBoundException, etc.,
 
</blockquote>
</details>

--- 


8.Which block has to be followed after the try block?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1"><summary> <b> Show Answer</b></summary>
	
> catch or finally block.
	
</details>

---

9.Does all the code inside the try block will be executed?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1"><summary><b> Show Answer</b></summary>
	
> Whenever an exception is occurred in the try block, the rest of the code after the exception occurs line will not be executed.
	
</details>

---

10.Can we have multiple catch blocks with the single try block?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1"><summary> <b> Show Answer</b></summary>	
<blockquote markdown="1">

yes, we can have multiple catch blocks with the single try block.


Important Rule: The order of the catch block must be from most specific to most general one i.e.catch for ArithmeticException must come before catching for Exception.
	
</blockquote>
</details>

---

11.When we can go for multiple catch blocks? 

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1">
  <summary> <b>Show Answer</b></summary>
  
<blockquote markdown="1">
 
- When our program uses various concepts like an array, file handling, database, etc.at the same time and each of them may throw exceptions due to one reason or another.
- To catch the generic exception we simply use 'Exception' in the catch block parameter and it can catch every exception like ArrayIndexOutOfBound, FileNotFound, etc.But the problem with this is we are not catching the specific exception.

</blockquote>
</details>

--- 

12.How can you handle exceptions in Java?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1">
  <summary> <b>Show Answer</b></summary>
  
<blockquote markdown="1">
 
 We can handle exceptions using

 1.try, catch, and finally block
 2.throw, throws
 
</blockquote>
</details>

--- 

13.What is the difference between exception and error in Java?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1">
  <summary> <b>Show Answer</b></summary>
  
<blockquote markdown="1">
 
 Errors happen while an application is running.For instance, an Out of Memory Error occurs in case the JVM runs out of memory.On the other hand, exceptions are mainly caused by the application.For instance, Null Pointer Exception happens when an app tries to get through a null object.
 
</blockquote>
</details>

--- 

14.What is a custom exception?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1">
  <summary> <b>Show Answer</b></summary>
  
<blockquote markdown="1">
 
Java allows us to create our exception based on our needs known as a custom exception or user-defined exception.
 
</blockquote>
</details>

--- 

15.How do you create custom exceptions in java?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1">
  <summary> <b>Show Answer</b></summary>
  
<blockquote markdown="1">
 
To create a custom exception, we have to extend the Exception class.

Example: 

```java
public class IncorrectUserNameException extends Exception { 
    public IncorrectUserNameException(String errorMessage) {
        super(errorMessage);
    }
}
```
 
</blockquote>
</details>

---
