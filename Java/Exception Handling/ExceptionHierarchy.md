1:Explain default exception handling? 
<details><summary><b> Show Answer</b></summary>
<details><summary><b> Explanation</b></summary>
Whenever an exception has occurred, the method creates an Object known as an Exception Object and hands it off to the run-time system(JVM). The exception object contains the name and description of the exception and the current state of the program where the exception has occurred. Creating the Exception Object and handling it in the run-time system is called throwing an Exception. There might be a list of the methods that had been called to get to the method where an exception occurred. This ordered list of the methods is called Call Stack. The run-time system searches the call stack to find the method that contains a block of code that can handle the occurred exception. The block of the code is called an Exception handler.The run-time system starts searching from the method in which the exception occurred, and proceeds through the call stack in the reverse order in which methods were called.If it finds an appropriate handler, then it passes the occurred exception to it. An appropriate handler means the type of the exception object thrown matches the type of the exception object it can handle.
If the run-time system searches all the methods on the call stack and couldn’t have found the appropriate handler, then the run-time system handover the Exception Object to the default exception handler, which is part of the run-time system. 
</details>
</details>

---

2:Explain Exception types? 
<details><summary><b> Show Answer</b></summary>
Types of exceptions
<details><summary><b> Explanation</b></summary>
All exception types are subclasses of the built-in class Throwable. Which
is at the top of the exception class hierarchy. Immediately below Throwable class, there are two subclasses that partition exceptions into two distinct branches. One branch is headed by Exception. This class is used for exceptional conditions that user programs should catch. This is also the class that you will subclass to create your own custom exception
types. The another subclass of Exception is  RuntimeException class and 
exceptions of this type are automatically defined for the programs that you write and include things such as divide by zero,array index bounds.
The other branch is topped by Error, which defines exceptions that are not expected to be caught under normal circumstances by your program. Exceptions of type Error are used by the Java run-time system to indicate errors having to do with the run-time environment, itself. Stack overflow is an example of such an error.
</details>
</details>

---

3:Debug the error for the following code.
 ``` java 
class Catch {
public static void main(String args[]) {
try {
int a = 0;
int b = 42 / a;
} catch(Exception e) {
System.out.println("Generic Exception catch.");
}
catch(ArithmeticException e) { 
System.out.println("This is never reached.");
}
}
}
```
<details><summary><b> Show Answer</b></summary>
reverse the order of the catch statements.
<details><summary><b> Explanation</b></summary>

```java
	
catch(ArithmeticException e) { 
System.out.println("This is never reached.");
}
catch(Exception e) {
System.out.println("Generic Exception catch.");
}
	
```
	
</details>
</details>

---

4:Predict the output of  the following code.
 ``` java 
class TryCatch {
public static void main(String args[]) {
try {
int x = args.length;
int y = 42 / x;
System.out.println("x = " + x);
try { 
if(x==1) x = x/(x-x); 
if(x==2) {
int z[] = { 1 };
z[10] = 25; 
}
} catch(ArrayIndexOutOfBoundsException e) {
System.out.println("Array index out-of-bounds: " + e);
}
} catch(ArithmeticException e) {
System.out.println("Divide by 0: " + e);
}
}
}
```
<details><summary><b> Show Answer</b></summary>
<details><summary><b> Explanation</b></summary>
	
```java
C:\>java TryCatch
Divide by 0: java.lang.ArithmeticException: / by zero
C:\>java TryCatch One
a = 1
Divide by 0: java.lang.ArithmeticException: / by zero
C:\>java TryCatch One Two
a = 2
Array index out-of-bounds:
java.lang.ArrayIndexOutOfBoundsException
```
	
</details>
</details>

---

5:Explain Chained Exception? 
<details><summary><b> Show Answer</b></summary>
<details><summary><b> Explanation</b></summary>
The chained exception feature allows you to associate another exception with an exception.This second exception describes the cause of the first exception. For example,In a situation where a method throws an ArithmeticException because of an attempt to divide by zero. However, the actual cause of the problem was that an I/O error occurred, which caused the divisor to be set improperly. Although the method must certainly throw
an ArithmeticException, since that is the error that occurred, you might also want to let the calling code know that the underlying cause was an I/O error. Chained exceptions let you handle this, and any other situation in which layers of exceptions exist.
</details>
</details>

---

6:Predict the output of  the following code.
 ``` java 
class ChainDemo {
static void proc() {
NullPointerException e = new NullPointerException("top layer");
e.initCause(new ArithmeticException("cause"));
throw e;
}
public static void main(String args[]) {
try {
proc();
} catch(NullPointerException e) {
System.out.println("Caught: " + e);
System.out.println("Original cause: " +e.getCause());
}
}
}
```
<details><summary><b> Show Answer</b></summary>
Chained Exceptions
<details><summary><b> Explanation</b></summary>
	
```java
Caught: java.lang.NullPointerException: top layer
Original cause: java.lang.ArithmeticException: cause
```
	
</details>
</details>

---

7:What are the methods of `Throwable` class? 
<details><summary><b> Show Answer</b></summary>
methods of Throwable class
<details><summary><b> Explanation</b></summary>
	
`public String getMessage()` – This method returns the message String of Throwable and the message can be provided while creating the exception through its constructor.
	
`public String getLocalizedMessage() ` – This method is provided so that subclasses can override it to provide a locale-specific message to the calling program. Throwable class implementation of this method use getMessage() method to return the exception message.
	
`public synchronized Throwable getCause() ` – This method returns the cause of the exception or null if the cause is unknown.
	
`public String toString()` – This method returns the information about Throwable in String format, the returned String contains the name of Throwable class and localized message.
	
`public void printStackTrace()` – This method prints the stack trace information to the standard error stream, this method is overloaded and we can pass PrintStream or PrintWriter as an argument to write the stack trace information to the file or stream.
	
</details>
</details>

---

8:Explain the best practices  of Exception Handling? 
<details><summary><b> Show Answer</b></summary>
	
best practices  of Exception Handling
	
<details><summary><b> Explanation</b></summary>
	
– Base classes of Exception hierarchy don’t provide any useful information, that’s why Java has so many exception classes, such as IOException with further sub-classes as FileNotFoundException, EOFException, etc. We should always throw and catch specific exception classes so that caller will know the root cause of the exception easily and process them. This makes debugging easy and helps client applications handle exceptions appropriately.
	
– Since java enforces to either handle the checked exception or to declare it in the method signature, sometimes developers tend to catch the exception and log the error. But this practice is harmful because the caller program doesn’t get any notification for the exception. We should catch exceptions only when we can handle them appropriately.While implementing any feature, we should always throw exceptions back to the caller and let them decide how to handle it.
	
– Since exceptions halt the processing of the program, we should close all the resources in finally block.
	
– We should always log exception messages and while throwing exceptions provide a clear message so that caller will know easily why the exception occurred. We should always avoid an empty catch block that just consumes the exception and doesn’t provide any meaningful details of the exception for debugging.

– It’s always better to define an exception handling strategy at the design time and rather than throwing and catching multiple exceptions, we can create a custom exception with an error code and the caller program can handle these error codes. It’s also a good idea to create a utility method to process different error codes and use them.
	
– When you create your custom exception, make sure it ends with Exception so that it will be clear from the name itself that it’s an exception class. 
	
– Exceptions are costly and sometimes it’s not required to throw exceptions at all and we can return a boolean variable to the caller program to indicate whether an operation was successful or not. This is helpful where the operation is optional and you don’t want your program to get stuck because it fails. 
	
</details>
</details>

---

9:What is a Call Stack in exceptions? 
<details><summary><b> Show Answer</b></summary>
The call stack is the ordered list of methods that had been called to get to a specific method.These are the methods which were called to get to the method in which the error occurred.
</details>

---

10:Explain the types of RunTime exceptions? 
<details><summary><b> Show Answer</b></summary>
Types of RunTime exceptions
<details><summary><b> Explanation</b></summary>
	
- ArithmeticException is thrown when an exceptional condition has occurred in an arithmetic operation.
	
- ArrayIndexOutOfBoundsException is thrown to indicate that an array has been accessed with an illegal index. The index is either negative or greater than or equal to the size of the array.
	
- ClassNotFoundException is raised when we try to access a class whose definition is not found.
	
- FileNotFoundException is raised when a file is not accessible or does not open.
	
- IOException is thrown when an input-output operation is failed or interrupted.
	
- InterruptedException is thrown when a thread is waiting, sleeping, or doing some processing, and it is interrupted.
	
</details>
</details>

---

11:What is an Error class in exceptions? 
<details><summary><b> Show Answer</b></summary>
Error class in exceptions
<details><summary><b> Explanation</b></summary>
An Error class in exception handling is a subclass of Throwable which represents a serious problem that a reasonable application should not try to catch. The method does not have to declare an Error or any of its subclasses in its throws clause for it to be thrown during the execution of a method. The most common subclasses of the Error class are Java OutOfMemoryError and StackOverflowError classes.
</details>
</details>

---

12:What is a SocketException? 
<details><summary><b> Show Answer</b></summary>
SocketException
<details><summary><b> Explanation</b></summary>
SocketException occurs on the server-side when the client closed the socket connection before the response could be returned over the socket. For example, by quitting the browser before the response was retrieved. Connection reset simply means that a TCP(Tranmission control protocol) reset  was received. 
</details>
</details>

---

13:Predict the output of  the following code.
 ``` java 
class ExceptionNumber
{
   public static void main(String args[])
   {
      try{
	 int n=Integer.parseInt ("ABC") ;
	 System.out.println(n);
      }catch(NumberFormatException e){
	  System.out.println("Number format exception occurred");
       }
   }
}
```
<details><summary><b> Show Answer</b></summary>
Number format exception occurred
</details>

---

14:Predict the output of  the following code.
 ``` java 
public class ExceptionString
{
   public static void main(String args[])
   {
      try{
	 String s="Revature";
	 System.out.println(s.length());;
	 char t = s.charAt(0);
	 t = str.charAt(15);
	 System.out.println(t);
      }catch(StringIndexOutOfBoundsException e){
	  System.out.println("StringIndexOutOfBoundsException!!");
       }
   }
}
```
<details><summary><b> Show Answer</b></summary>
StringIndexOutOfBoundsException
</details>

---

15:Predict the output of  the following code.
 ``` java 
class ExceptionString1
{
   public static void main(String args[])
   {
	try{
		String s=null;
		System.out.println (s.length());
	}
        catch(NullPointerException e){
		System.out.println("NullPointerException");
	}
   }
}
```
<details><summary><b> Show Answer</b></summary>
NullPointerException
</details>

