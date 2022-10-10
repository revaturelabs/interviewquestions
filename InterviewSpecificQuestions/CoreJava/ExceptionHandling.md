1. Brief us on Exception Handling. (or) What is execption?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>

An exception is an error event that can happen during the execution of a program and disrupts its normal flow.

Exceptions in Java can arise from different kinds of situations such as wrong data entered by the user, hardware failure, network connection failure, or a database server that is down. The code that specifies what to do in specific exception scenarios is called exception handling.

 
</blockquote>
</details>

--- 

2. What is the difference between Throw and Throws?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>

|                                       throw                                       |                                                                          throws                                                                         |
|:---------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------------------------------------------:|
| Used inside a method when it is required to throw an Exception logically.         | Used in the method signature when the method has some statements that can lead to exceptions                                                            |
| Used to throw an exception explicitly. It can throw only one exception at a time. | Used to declare multiple exceptions, separated by a comma. When exception occurs, it matches with the declared ones, then throw exception automatically |
| Syntax: throw new Exception()                                                     | Syntax: public static void writeToFile() throws Exception {}                                                                                            |

 
</blockquote>
</details>

--- 

3. How to handle class not found exception?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>

Java ClassNotFoundException occurs when the application tries to load a class but Classloader is not able to find it in the classpath. It is a checked exception, so it needed to be handled.

To fix ClassNotFoundException, firstly we must go through the exception stack trace clearly. Then,
- Make sure, you've specficed the exact class path.
- Check for classpath settings and make sure class it’s present at runtime.
- Verify the requesting Class name is correct.
 
</blockquote>
</details>

--- 

4. Brief us on the keywords - final, finally & static 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>

 - final is the keyword and access modifier which is used to apply restrictions on a class, method or variable.

 - finally is the block in Java Exception Handling to execute the important code whether the exception occurs or not.

 - static keyword is used to create a class level variable in java. static variables and methods are part of the class, not the instances of the class.
 
</blockquote>
</details>

--- 


6. Brief us on Errors

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>

- Errors represent irrecoverable conditions such as Java virtual machine (JVM) running out of memory, memory leaks, stack overflow errors, library incompatibility, infinite recursion, etc.

- Errors are usually beyond the control of the programmer and we should not try to handle errors.
 
</blockquote>
</details>

--- 

7. What is the difference between final and finally?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>
 
final is a keyword and it can be used to mark a variable "unchangeable" . Actually, it is used to apply restrictions on class, method and variable. Final class can't be inherited, final method can't be overridden and final variable value can't be changed.

Finally is a code block. It is used with try-catch block for handling exception. finally code block will be executed whether exception is handled or not
 
</blockquote>
</details>

--- 

8. Tell us about the different kinds of exceptions. What are some examples of checked and unchecked exceptions?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>
 There are 2 types of exceptions

- **Checked Exception(java.lang.Exception)** -> This exception forces the progarmmer to handle it at the compile time itself, until the programmer handles it, compiler wont allow to run. Some of Checked exceptions are FileNotFoundException, ClassNotFoundException,MethodNotFoundException, SQLException, etc.,

- **Unchecked Exceptions(java.lang.RuntimeException)** -> These exceptions occurs at a run time, it is upto programmer whether he wants to handle this or not, if he doesnt handle it, it will lead to abnormal termination. Some of unchecked exceptions are ArithmeticException, NullPointerException,ArrayIndexOutOfBoundException, etc.,
 
</blockquote>
</details>

--- 


1. Which block has to be followed after the try block?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b> Show Answer</b></summary>
	
> catch or finally block.
	
</details>

---

2. Does all the code inside try block will be executed?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
	
> Whenever an exception is occurred in the try block, the rest of the code after the exception occured line will not be executed.
	
</details>

---

5. Can we have multiple catch blocks with the single try block?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b> Show Answer</b></summary>	
<blockquote>

yes, we can have multiple catch blocks with the single try block. 


Important Rule: Order of the catch block must be from most specific to most general one i.e. catch for ArithmeticException must come before catch for Exception.
	
</blockquote>
</details>
---

6. When we can go for multiple catch block? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>
 
- When our program use various concepts like array, file handling, database, etc. at the same time and each of them may throw exception due one reason or other. 
- To catch the generic exception we simply use 'Exception' in the catch block parameter and it can catch every exceptions like ArrayIndexOutOfBound, FileNotFound, etc. But problem with this is we are not catching the specific exception.

</blockquote>
</details>

--- 

9. How can you handle exceptions in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>
 
 We can handle exceptions using

 1. try, catch, finally block
 2. throw, throws
 
</blockquote>
</details>

--- 

10. What is the difference between exception and error in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>
 
 Errors happen while an application is running. For instance, Out of Memory Error occurs in case the JVM runs out of memory. On the other hand, exceptions are mainly caused by the application. For instance, Null Pointer Exception happens when an app tries to get through a null object.
 
</blockquote>
</details>

--- 

11. What is a custom exception?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>
 
Java allow us to create our own exception based on our need is known as a custom exception or user-defined exception.
 
</blockquote>
</details>

--- 

12. How do you create custom exception in java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>
 
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