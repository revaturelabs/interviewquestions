1. Brief us on Exception Handling (or) What is an exception?

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
| Used to throw an exception explicitly. It can throw only one exception at a time. | Used to declare multiple exceptions, separated by a comma. When an exception occurs, it matches with the declared ones, and throws an exception automatically |
| Syntax: throw new Exception()                                                     | Syntax: public static void writeToFile() throws Exception {}                                                                                            |

 
</blockquote>
</details>

--- 

3. How to handle ClassNotFoundException?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>

Java ClassNotFoundException occurs when the application tries to load a class but Classloader is not able to find it in the classpath. It is a checked exception, so it needed to be handled.

To fix ClassNotFoundException, firstly we must go through the exception stack trace. Then,
- Make sure, you've specified the exact classpath.
- Check for classpath settings and make sure the class it’s present at runtime.
- Verify the requesting Class name is correct.
 
</blockquote>
</details>

--- 

4. Brief us on the keywords - final, finally & static 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>

 - final is the keyword and access modifier which is used to apply restrictions on a class, method, or variable.

 - finally, the block in Java Exception Handling executes important code whether the exception occurs or not.

 - static keyword is used to create a class-level variable in Java. static variables and methods are part of the class, not the instances of the class.
 
</blockquote>
</details>

--- 


5. What are Errors?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>

- Errors represent irrecoverable conditions such as Java virtual machine (JVM) running out of memory, memory leaks, stack overflow errors, library incompatibility, infinite recursion, etc.

- Errors are usually beyond the control of the programmer and we should not try to handle errors.
 
</blockquote>
</details>

--- 

6. What is the difference between final and finally?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>
 
final is a keyword and it can be used to mark a variable "unchangeable". It is used to apply restrictions on class, method and variable. A final class can't be inherited, the final method can't be overridden and the final variable value can't be changed.

Finally is a code block. It is used with a try-catch block for handling exceptions. Finally, a code block will be executed whether an exception is handled or not
 
</blockquote>
</details>

--- 

7. Tell us about the various kinds of exceptions. What are some examples of checked and unchecked exceptions?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>
 There are 2 types of exceptions

- **Checked Exception(java.lang.Exception)** -> This exception forces the programmer to handle it at the compile time itself, until the programmer handles it, the compiler won’t allow it to run. Some of the Checked exceptions are FileNotFoundException, ClassNotFoundException,MethodNotFoundException, SQLException, etc.,

- **Unchecked Exceptions(java.lang.RuntimeException)** -> These exceptions occur at a run time, it is up to the programmer whether he wants to handle this or not, if he doesn’t handle it, it will lead to abnormal termination. Some of the unchecked exceptions are ArithmeticException, NullPointerException,ArrayIndexOutOfBoundException, etc.,
 
</blockquote>
</details>

--- 


8. Which block has to be followed after the try block?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b> Show Answer</b></summary>
	
> catch or finally block.
	
</details>

---

9. Does all the code inside the try block be executed?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
	
In Java, the code inside the try block will be executed unless an exception occurs that causes the control flow to transfer to an appropriate catch block or finally block. The try block defines a section of code where an exception might occur, and the Java runtime system attempts to execute that code normally.

If no exception occurs, the code within the try block will execute in its entirety, statement by statement, from top to bottom. However, if an exception is thrown during the execution of the try block, the remaining code within the block will be skipped, and the flow of control will transfer to the corresponding catch block or finally block (if present).
	
</details>

---

10. Can we have multiple catch blocks with a single try block?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b> Show Answer</b></summary>	
<blockquote>

yes, we can have multiple catch blocks with a single try block. 


Important Rule: The order of the catch block must be from most specific to most general one i.e. catch for ArithmeticException must come before catching for Exception.
	
</blockquote>
</details>

---

11. When we can go for multiple catch blocks? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>
 
- When our program uses various concepts like an array, file handling, database, etc. at the same time and each of them may throw exceptions due to one reason or another. 
- To catch the generic exception we simply use 'Exception' in the catch block parameter and it can catch every exception like ArrayIndexOutOfBound, FileNotFound, etc. But the problem with this is we are not catching the specific exception.

</blockquote>
</details>

--- 

12. How will you handle exceptions in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>
 
 We can handle exceptions by using

 1. try, catch, and finally block
 2. throw, throws keywords
 
</blockquote>
</details>

--- 

13. What is the main difference between Exception and Error in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>
 
 The main difference between Exception and Error in Java is that exceptions represent problems that can occur during the normal execution of a program and are meant to be caught and handled, while errors indicate severe problems that are typically unrecoverable and are not meant to be caught or handled by regular application code.
 
</blockquote>
</details>

--- 

14. What is a custom exception?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>
 
Java allows us to create our exception based on our needs known as a custom exception or user-defined exception.
 
</blockquote>
</details>

--- 

15. How do you create a custom exception in Java?

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

16. How to avoid Exceptions?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

To avoid exception exception in Java you can :

1. Check for null values: Whenever you are working with an object, check whether it is null before using it. This can help to avoid NullPointerExceptions.

2. Use try-catch blocks: Use try-catch blocks to catch exceptions and handle them gracefully. This can help to prevent your program from crashing and provide a more user-friendly experience.

3. Validate input: Validate user input and make sure it conforms to the expected format. This can help to avoid exceptions caused by invalid input.

4. Use conditional statements: Use conditional statements, such as if-else and switch statements, to check for potential problems before executing code that may cause exceptions.

</blockquote>

</details>

---

17. How to handle Exceptions?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

In Java, exceptions are a way to handle errors and unexpected situations that occur during program execution. To handle exceptions in Java, you can use a try-catch block. Here's how it works:

1. The code that might throw an exception is placed inside a try block.
2. If an exception occurs in the try block, the program jumps to the catch block.
3. The catch block contains code that handles the exception. It can print an error message or take other actions to recover from the error.

</blockquote>

</details>

---

18. What is the purpose of a try, catch block?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The `try-catch` block in Java is used to handle exceptions that may occur during the execution of a program.

The `try` block contains the code that may throw an exception. If an exception is thrown within the `try` block, the code execution is immediately transferred to the catch block.

The `catch` block contains the code that handles the exception. It specifies the type of exception that it can handle and what should be done when an exception of that type occurs. Multiple catch blocks can be used to handle different types of exceptions.

The `try-catch` block helps to prevent the program from crashing when an unexpected error occurs and continue its execution.

</blockquote>

</details>

---

19. Can you have more than one finally block?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

No, In Java we can not have more the one finally block for one try block.

</blockquote>

</details>

---

20. What is the purpose of exception handling in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Exception handling allows developers to handle and manage errors or exceptional conditions that may occur during program execution.

</blockquote>

</details>

---

21. What is a NullPointerException?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

A NullPointerException is a common runtime exception that occurs when a program tries to use a null reference.

Null pointer exceptions can occur in various situations, such as when trying to call a method or access a property on a null reference, when trying to iterate over a null collection.

To avoid null pointer exceptions we can check for null references before attempting to use them and handle them appropriately by throwing a different exception.

</blockquote>

</details>

---

22. List the Exception class hierarchy.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

In Java, the Exception class hierarchy is a tree-like structure of classes that represent various types of exceptions. At the top of the hierarchy is the `Throwable` class, which is the superclass of all exceptions and errors. The `Throwable` class has two subclasses: `Error` and `Exception`.

The `Error` class represents problems that are typically beyond the control of the program.

The `Exception` class represents problems that can be caught and handled by the program. The `Exception` class has several subclasses that represent different types of exceptions, including `RuntimeException`, `IOException`, `SQLException`, and `ClassNotFoundException`.

The `RuntimeException` class have subclasses, like `NullPointerException` or `ArrayIndexOutOfBoundsException`. The `IOException` class have subclasses, like ` FileNotFoundException` or `SocketException`.

</blockquote>

</details>

---

23. How do you call a custom exception containing a unique error message?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

To call a custom exception containing a unique error message, you need to create the custom exception class that extends the `Exception` or `RuntimeException` class and override its constructors to accept the custom error message.

Here is an example,

```java

public class MyException extends Exception {

    public MyException(String message) {
        super(message);
    }
    
}

```
To throw the MyException with a custom error message, you can simply create a new instance of the MyException class and pass the error message to its constructor, like below:

```java
throw new MyException("This is a custom error message.");
```

</blockquote>

</details>

---

24. What is a try with resources?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

A try-with-resources statement in Java is a way to declare one or more resources that will be automatically closed at the end of the statement.

Before try with resources, it was necessary to manually manage and release resources such as file streams, network connections, and database connections within a finally block. This approach was error-prone and could lead to resource leaks or errors in handling exceptions.

With try with resources, you can declare one or more resources in the parentheses of the statement. The resources are initialized before the try block begins, and are automatically closed when the try block ends, even if an exception is thrown.

The syntax of a try-with-resources block is as follows:

```java
try (ResourceType resource1 = new ResourceType(); ResourceType resource2 = new ResourceType()) {
    // code that uses the resources
} catch (ExceptionType e) {
    // exception handling code
} finally {
    // any necessary cleanup code
}

```

</blockquote>

</details>

---

25. Explain final, finally, and finalize?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>


In Java, `final`, `finally`, and `finalize` are three different keywords that serve different purposes.

`final` is a keyword that can be applied to variables, methods, and classes. When applied to a variable, it indicates that the value of the variable cannot be changed once it has been assigned. When applied to a method, it indicates that the method cannot be overridden by subclasses. When applied to a class, it indicates that the class cannot be subclassed.

`finally` is a block of code that is used in exception handling. The code in the finally block is executed whether an exception is thrown or not.

`finalize` is a method that is called by the garbage collector on an object when it determines that there are no more references to the object in the program. It is used to perform any final cleanup operations on the object before it is destroyed. 

</blockquote>

</details>

---

26. What are throws and Throwable?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

`throws` is a keyword that is used in a method signature to indicate that the method may throw an exception. It is used when the method itself is not handling the exception but instead wants to pass the responsibility of handling the exception to its caller method.

On the other hand, `Throwable` is the root class of all Java exceptions and errors. It has subclasses, such as `Exception` and `Error` classes. All exceptions and errors inherit from the `Throwable` class, either directly or indirectly.

</blockquote>

</details>

---

27. Is it possible to handle OutOfMemoryError by using try/catch block?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

If your program is using excessive memory Java will give you an `OutOfMemoryError` and we can not handle that error using `try-catch` block. As this error indicates that the JVM has run out of memory, and it can't be recovered by simply catching the error. 

</blockquote>

</details>

---

28. What is exception propogation?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Exception propagation in Java refers to the mechanism by which an exception that is thrown in a method is passed on to the calling method, and then to the next method in the call stack until it is caught or reaches the main method.

When an exception is thrown in a method, the Java runtime system searches for an exception handler in the method itself. If it doesn't find one, it looks for an exception handler in the calling method, and continues to do so up the call stack until it finds a handler or reaches the top of the stack. If no handler is found, the Java runtime system terminates the program and displays a stack trace, which shows the method call stack at the point where the exception occurred.

</blockquote>

</details>

---

29. When there are two statements in a try/catch block with the first statement catching an exception, will the second statement run or stop?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

If the first statement in a try/catch block catches an exception, the second statement will not run. Instead, control will be transferred to the catch block to handle the exception. Once the exception is handled in the catch block, the program will continue executing after the catch block.

</blockquote>

</details>

---

30. Is it possible to nest try-catch blocks?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Yes, it is possible to nest try-catch blocks in Java. This means that you can have one try-catch block inside another try-catch block. if an exception is thrown in the inner try block, the inner catch block will handle it. If no exception is thrown, the inner try block will complete, and the outer try block will continue to execute. If an exception is thrown in the outer try block (either before or after the inner try block), the outer catch block will handle it.

</blockquote>

</details>

---

31. Differentiate throw vs throws vs Throwable.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

throw: The `throw` keyword is used to explicitly throw an exception within a method. It is followed by an instance of a subclass of Throwable or a derived class. When an exception is thrown, it interrupts the normal flow of the program and transfers control to an appropriate exception handler.

throws: The `throws` keyword is used in a method signature to declare that the method may throw one or more types of exceptions. It specifies the exceptions that might be thrown by the method, allowing the calling code to handle them appropriately. It is used to indicate that the method doesn't handle the exceptions itself but passes the responsibility to the caller or higher-level exception handlers.

Throwable: `Throwable` is the superclass of all exceptions and errors in Java. It represents any object that can be thrown using the throw statement. Throwable has two direct subclasses: Exception and Error (typically caused by system-level issues or unrecoverable errors).

</blockquote>

</details>

---

32. What is the difference between a ClassNotFoundException and NoClassDefFoundError?  

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

ClassNotFoundException: This exception is thrown when the Java Virtual Machine (JVM) tries to load a class at runtime using the Class.forName() method or by directly referencing the class with its fully qualified name, but the class cannot be found in the classpath. It typically occurs when the class being loaded is missing or not available in the specified classpath or when the class name is misspelled. ClassNotFoundException is a checked exception, which means it must be declared in a method's throws clause or caught and handled within a try-catch block.

NoClassDefFoundError: This error occurs when the JVM successfully finds the class during the compilation phase but cannot find the class during runtime. It means that the class was present at compile time but is missing at runtime. It can happen if the class was available during compilation, but it is not present in the classpath when the program is being executed. NoClassDefFoundError is an unchecked error, which means it is not required to be declared or caught explicitly. It usually indicates a more severe issue that prevents the JVM from initializing the class.

</blockquote>

</details>

---

33. Provide some examples when a finally block won't be executed in Java?   

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

In Java, the finally block is used in exception handling to define a block of code that will be executed regardless of whether an exception is thrown or not. However, there are a few scenarios where the finally block may not be executed:

- System.exit(): If the program terminates abruptly by calling System.exit() within the try or catch block, the finally block will not be executed. The System.exit() method immediately terminates the Java Virtual Machine (JVM), bypassing any remaining code.
- Infinite Loop: If the code within the try or catch block enters into an infinite loop, the finally block will not be executed. The program will keep running within the loop indefinitely, preventing the execution of any subsequent code.
- Sudden Power Loss or System Crash: In cases where there is a sudden power loss or a system crash, the finally block may not get a chance to execute. These scenarios are beyond the control of the Java program, and the JVM may not have an opportunity to complete the execution of the finally block.

</blockquote>

</details>

---

34. Predict the output of the following program.

```java
class Test
{
	String str = "a";

	void A()
	{
		try
		{
			str +="b";
			B();
		}
		catch (Exception e)
		{
			str += "c";
		}
	}

	void B() throws Exception
	{
		try
		{
			str += "d";
			C();
		}
		catch(Exception e)
		{
			throw new Exception();
		}
		finally
		{
			str += "e";
		}

		str += "f";

	}
	
	void C() throws Exception
	{
		throw new Exception();
	}

	void display()
	{
		System.out.println(str);
	}

	public static void main(String[] args)
	{
		Test object = new Test();
		object.A();
		object.display();
	}

}
```

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

**Output**

abdec

</blockquote>

<blockquote>

<details> <summary> <b> Explanation </b> </summary>

‘throw’ keyword is used to explicitly throw an exception.
finally block is always executed even when an exception occurs.
Call to method C() throws an exception. Thus, control goes in catch block of method B() which again throws an exception. So, control goes in catch block of method A().

</details>
</details>

---

35. Predict the output of the following program.

```java
class Test
{ int count = 0;

	void A() throws Exception
	{
		try
		{
			count++;
			try
			{
				count++;
				try
				{
					count++;
					throw new Exception();
				}
				catch(Exception ex)
				{
					count++;
					throw new Exception();
				}
			}
			catch(Exception ex)
			{
				count++;
			}
		}
		
		catch(Exception ex)
		{
			count++;
		}

	}

	void display()
	{
		System.out.println(count);
	}

	public static void main(String[] args) throws Exception
	{
		Test obj = new Test();
		obj.A();
		obj.display();
	}
}
```
![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

**Output**

5

</blockquote>

<blockquote>

<details> <summary> <b> Explanation </b> </summary>

‘throw’ keyword is used to explicitly throw an exception.
In third try block, exception is thrown. So, control goes in catch block.
Again, in catch block exception is thrown. So, control goes in inner catch block.

</details>
</details>

---

36. Predict the output of the following program.

``` java
class NestedTry {
	// main method
	public static void main(String args[])
	{
		// Main try block
		try {
			// initializing array
			int a[] = { 1, 2, 3, 4, 5 };
			// trying to print element at index 5
			System.out.println(a[5]);
			// try-block2 inside another try block
			try {
				// performing division by zero
				int x = a[2] / 0;
			}
			catch (ArithmeticException e2) {
				System.out.println("division by zero is not possible");
			}
		}
		catch (ArrayIndexOutOfBoundsException e1) {
			System.out.println("ArrayIndexOutOfBoundsException");
			System.out.println("Element at such index does not exists");
		}
	}
	// end of main method
}
```
![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

**Output**

ArrayIndexOutOfBoundsException
Element at such index does not exists

</blockquote>

<blockquote>

<details> <summary> <b> Explanation </b> </summary>

Whenever a try block does not have a catch block for a particular exception, then the catch blocks of parent try block are inspected for that exception, and if a match is found then that catch block is executed. If none of the catch blocks handles the exception then the Java run-time system will handle the exception and a system generated message would be shown for the exception.

</details>
</details>

---