## Technical Questions

 1.	What do you have in Java download file?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

There are two major things along with the Java Download file. 

- JDK - Java Development Kit

- JRE - Java Runtime Environment

</blockquote>

</details>


---

2.	Explain about ClassLoader.

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

It is a subsystem of Java Virtual Machine, for loading class files when a program is executed and to load the executable file.

Java has three type of ClassLoaders - Bootstrap, Extension, and Application classloaders.

</blockquote>

</details>


---

3.	Does the program run if we give `static public void main`?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

Yes, the program will execute successfully .  Because, in Java, there is no specific rule for the order of specifiers

</blockquote>

</details>


---

4. What could be the result, if the `main()` is not declared as static?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

When the main method is not declared as static, then the program may be compiled correctly but throws a run time error that reads 
`Error:Main method is not static in class classname,please defined the main method as public static void main(String args[])`. 

</blockquote>

</details>


---

5.	How can you differentiate between >> and >>> operators.


 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

`>> Binary Right Shift`
The left operand value is moved right by the number of bits specified by the right operand.

`>>> Shift right zero fill`
The left operand value is moved right by the number of bits specified by the right operand and shifted values are filled up with zeros.

</blockquote>

</details>


---

6.	Is Java Static or Dynamic?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

yes, Java is designed to adapt to an evolving environment. Java programs include a large amount of runtime information that is used to resolve access to objects in real-time. 

</blockquote>

</details>


---

7.	Whether we can run a code before executing the main method or not?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

- Yes, we can execute even before the main method. We will be using a static block of code when creating the objects at the class's load time. 
- Any statements within this static block of code will get executed at once while loading the class, even before creating objects in the main method.

</blockquote>

</details>


---

8.	Differentiate between `System. Out`, `System. Err`, and `System.in`?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

- `System.out` and `System.err` represent the monitor by default and can be used to send data or results to the monitor. 
- `System.out` is used to display normal messages and results. 
- `System.err` is used to display error messages. 
- `System.in` represents InputStream object which by default represents standard input device, i.e., keyboard.

</blockquote>

</details>


---

9.	Can a class be static ?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

-  A class in the Java program cannot be static except if it is the inner class. If it is an inner static class, then it exactly works like other static members of the class.

</blockquote>

</details>


---

10. How will you differentiate between `a=a+b` and `a+=b`?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

- The `a=a+b` statement has an assignment operator `=` and a arithmetic operator ` + ` , while `a+=b` has a arithmetic assignment operator `+=`. 

- For similar integer or byte or float data types both the expressions would compile.

- But if one value(a) is byte and the other(b) is int, `a=a+b` will not compile as ` byte+int ` is not byte

- Whereas `a+=b` will compile as the arithmetic assignment operator will do an implicit type casting.

</blockquote>

</details>


---

11. Does `System.exit()` in try block executes code in finally block?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

It will not execute finally block. The program will be terminated after `System.exit()` statement.

</blockquote>

</details>


---


12.	Can we write multiple main methods inside one class in Java?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

Throws a compiler error, that the method has been already defined inside the class.


</blockquote>

</details>


---

13.	Can we import the same class or package twice in a program and what happens to it during runtime?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

-  Yes, JVM internally loads the package or class only once, because of redundant.

</blockquote>

</details>


---

14.	Why the main method is static in Java?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

Java `main()` method is always static, so the compiler can call it without the creation of an object or before the creation of an object of the class, which is the starting point from where the compiler starts program execution. So, the compiler needs to call the `main()` method.

</blockquote>

</details>


---

15.	List the steps to set classpath in Java?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

- Select Start.
- Go to the Control Panel.
- Select System and Security.
- Select Advanced System settings.
- Click on Environment Variables.
- Click on New under System Variables.
- Add CLASSPATH as variable name and path of files as a variable value.
- Select OK

</blockquote>

</details>


---

16.	What is default value that a local variable holds?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

 The local variables are not initialized to any default values. We should not use local variables with out initialization. Even the Java compiler throws error.

</blockquote>

</details>


---

17.	Can variables be used in Java without initialization?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

In Java, if a variable is used in a code without prior initialization by a valid value, program doesn’t compile and gives an error as no default value is assigned to variables in Java.

</blockquote>

</details>


---

18.	Is it possible to compile a Java class successfully without even having a main method

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

Yes. main method is an entry point of Java class and is required for execution of the program , a class gets compiled successfully even if it doesn’t have a main method. It can’t be run successfully.

</blockquote>

</details>


---

19.	Is it possible to use its sub-packages when its package is imported in a class

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

In Java, when a package is imported, its sub-packages aren’t imported and developer needs to import them separately if required.

For example, if a developer imports a package `Company.*,` all classes in the package named Company are loaded but no classes from the sub-package are loaded. To load the classes from its sub-package ( say team), developer has to import it explicitly as follows:

`import Company.team.*`

</blockquote>

</details>


---

20.	Can we declare a class in Java as private?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

We can not declare top level class as private. Java allows only public and default modifier for top level classes in java. Inner classes can be private

</blockquote>

</details>


---

21. Why do we call JVM as virtual??

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

It provides a machine interface that does not depend on the underlying operating system and machine hardware architecture.

</blockquote>

</details>


---

22. Explain the types of ClassLoader.


 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

First <b>bootstrap class loader</b> tries to find the class. It scans the rt.jar file in JRE lib folder.
If class is not found then <b>extension class loader</b> searches the class file in inside jre\lib\ext folder.
Again if class is not found then application classloader searches all the Jar files and classes in CLASSPATH environment variable of system.
If class is found by any loader then class is loaded by class loader; else ClassNotFoundException is thrown

</blockquote>

</details>


---

23.	What will be the role of execution engine in JVM?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

All code assigned to JVM is executed by an execution engine. The execution engine reads the byte code and executes one by one. It uses two inbuilt interpreter and JIT compiler to convert the bytecode to machine code and execute it.

</blockquote>

</details>


---

24.How to convert byte-code instruction to corresponding native instruction?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

JIT compilers interact with the JVM at runtime and compile appropriate bytecode sequences into native machine code.

</blockquote>

</details>


---

25. Where does all the bundles of libraries, Java Virtual Machine, and other components reside in the Java?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

- It is a software package which bundles the libraries (jars) and the Java Virtual Machine, and other components to run applications written in the Java. JVM is just a part of JRE distributions.

- To execute any Java application, you need JRE installed in the machine. It’s the minimum requirement to run Java applications on any computer

</blockquote>

</details>


---

26.	What you need to develop a Java Application?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

JDK is a superset of JRE. JDK contains everything that JRE has along with development tools for developing, debugging, and monitoring Java applications. You need JDK when you need to develop Java applications.

</blockquote>

</details>


---

27.	Differentiate between JDK, JRE and JVM.

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

JRE = JVM + libraries to run Java application.

JDK = JRE + tools to develop Java Application.


</blockquote>

</details>


---

28.	Does Java support Pointers

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Pointer is a reference handle to a memory location. Java doesn't support pointers beacuse improper handling of pointers leads to memory leaks and reliability.
Java has references.A reference is a variable that refers to something else and can be used as an alias for that something else.

</blockquote>

</details>


---

29.	What is the difference between instance variable and a class variable?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

- An instance variable is a variable which has one copy per object/instance, every object will have one copy of it. 
- A class variable is a variable which has one copy per class, will not have a copy in the object. 

</blockquote>

</details>


---

30.	 Can a static method access non-static variables or methods? 

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

No,  A static method cannot access non-static variables or methods because static methods can be accessed without instantiating the class, so if the class is not instantiated the variables are not initialized and thus cannot be accessed from a static method.

</blockquote>

</details>


---

31.	How many types of variables are used in Java?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

There are three types of variables in Java

- Local Variables
- Instance Variables
- Static Variables


</blockquote>

</details>


---

32.	Why Data Type is mandatory in Java?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

It is an attribute which tells what kind of data that variable can have. Every Java variable takes up a certain amount of space in memory. Memory of a varaible depends on its datatype.


</blockquote>

</details>


---

33.	When do the static variables will be loaded in the memory?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

They are loaded at runtime when the respective Class is loaded.

</blockquote>

</details>


---

34. How many bytes void data type requires since every data type requires some bytes of memory in Java?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Void is nothing which doesn't return anything , so it has no memory allocated .

</blockquote>

</details>


---

35.	 Why do local variables don't have any default value, whereas the member variables have default values ?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

member variable are loaded into heap, so they are initialized with default values when an instance of a class is created. In case of local variables, they are stored in stack until they are being used.


</blockquote>

</details>


---

36.	 Why global variables are not supported in Java?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

They are not allowed in Java, as it wont fit good with the concept of encapsulation.


</blockquote>

</details>


---

37.	 When does <b>Garbage Collection</b> process reclaim the memory of object in Java?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

All Java objects automatically grab the memory that they need when they are created, and when the object is no longer required , garbage collector will reclaim the memory.

</blockquote>

</details>


---

38. Which is the form of automatic memory management?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Garbage collector is a program which runs on the JVM which gets rid of unused objects which are not being used by a Java application anymore.

</blockquote>

</details>


---

39. Assume there are 2 variables declared as `int` in a program and in later part of the program we need to use the same variables to hold in `Char`. How can we achieve this.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Using Type-casting we can achieve this, it is a way to cast a variable into another datatype.

</blockquote>

</details>


---

40.	Which operators are used in looping and branching statements to create conditions?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

To create a condition in looping statements we can use Relational operators in Java , that are used to perform the comparison between two numeric values or two quantities. 

</blockquote>

</details>


---

41. What will be the return value of the main () method in Java?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

In java, main() method can’t return any data and hence, it’s always declared with a void return type.


</blockquote>

</details>


---

42.In which loop the keyword `break` cannot be simply used?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

In `if-else` we cannot use break statement , since it is to simply come out of the loop


</blockquote>

</details>


---

43. Which type of loop will execute the statements at least once no matter the condition fails?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

A `do-while loop` checks the loop condition after execution of the loop body. This ensures it always executes at least once even if the condition fails.


</blockquote>

</details>


---

44. Which keyword is used to end the current loop iteration and proceed execution with the next iteration of that loop?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

The `continue` keyword is used to end the loop iteration immediately and resume execution at the next iteration.

</blockquote>

</details>


---

45. Which access modifiers can be used with a class in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Public and Default access modifiers can be used with a class.

</blockquote>

</details>


---

46. Can we declare a top-level class as protected?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

 No, we cannot declare a class as protected. An inner class can be protected but not an outer class.

 </blockquote>

</details>


---

47. Why are access modifiers used?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

It is used to restrict the access of a class and its members and used to reduce the visibility of the members of a class.

 </blockquote>

</details>


---

48.  Which one is the least restrictive access modifier in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

 Public -  Classes, methods, or data members that are declared as public are accessible from everywhere in the program

 </blockquote>

</details>


---

49. Which is the most restrictive access modifier in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Private - The methods or data members declared as private are accessible only within the class in which they are declared.

 </blockquote>

</details>


---

50. Which access modifier is also known as Universal access modifier?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Public-  Classes, methods, or data members that are declared as public are accessible from everywhere in the program

 </blockquote>

</details>


---

51. Is it possible to combine more than one access modifier in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

No. A method, variable or class can be marked with only one access modifier.

 </blockquote>

</details>


---

52. What you have to do to access a protected variable or method of a Class outside the package in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

- Create a Subclass and call the protected variable or method.

- Protected variables and methods must be called from inside subclasses or subclass objects only.

 </blockquote>

</details>


---

53. How will you make a class to execute first in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

If you declare a class as static, that class will be executed first. Static modifier is used to check that a member is a class member or instance member.

 </blockquote>

</details>


---

54. When does the class cannot be subclassed?


![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

 If you declare the class as Final, it will restrict further modification of a class, field, or method. which cannot be subclassed.

  </blockquote>

</details>


---

55. Which class cannot be instantiated in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

When we declare the class or method as abstract, whcih is used for further modification and it cannot be instantiated.

  </blockquote>

</details>


---

56. What will happen , if no access specifiers is mentioned?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

If no access modifier is mentioned (i.e. public-private or protected). It means that it is visible to all within a particular package.

  </blockquote>

</details>


---

57. Differentiate between a keyword and a modifier ?	

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>


 - Keywords are the reserved words that have a pre defined meaning for a compiler whereas modifiers are the type of keywords that modifies the state or definition of a programming construct.

- for, while are keywords but not modifiers.
private , public , final , abstract etc are keywords as well as modifiers.

  </blockquote>

</details>


---

58. What is the difference between public class and class ?	

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

- Class without any access specifier has the default scope i.e it can be accessed by any class within same package.

- Class declared public can be accessed from anywhere.

  </blockquote>

</details>

---

59. Can we change the return type Of `Main()` method? what will be the output if we change if we change the type?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

We can change the return type for main method but java compiler will refuse to acknowledge it as entry point for the Java application.


</blockquote>

<details><summary> Explanation </summary>

<blockquote>

It will throw an exception that Main method must return a value of type void in class Main.

</blockquote>

</details>

</details>

---

60. Can we declare main method as non static in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

No, JVM invokes main method even before the instantiation of the class. As non-static members or methods cannot be called with the class name directly so `main()` method should be declared as static

</blockquote>

</details>

---

61. Can we declare `Main()` method as private or protected or with no access specifier?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

No

</blockquote>

<details><summary> Explanation </summary>

<blockquote>

 if we declare so, `main()` will not be accessible to JVM. Class will compile successfully but will get run time error as no main method found.

 </blockquote>

</details>

</details>

---

62. Can we define package statement after import statement in Java? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

We can’t define package statement after import statement in Java. package statement must be the first statement in source file. We can have comments before the package statement.

 </blockquote>

</details>

---

63. What access modifiers can be used for class in Java? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

We can use only public and default access modifiers for classes in Java

 </blockquote>

</details>

---

## Problem Solving

64. The program throws a compile-time error? State the reason and number of errors it will throw. 

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

``` java
abstract final class Syllabus{
   public abstract void printMessage();
 }
 class JavaSyllabus extends Syllabus{
    public void printMessage(){
              System.out.println("Welcome to Java Syllabus");
   }
   }
 class SQLSyllabus  extends JavaSyllabus{
    public void printMessage(){
       System.out.println("Welcome to SQL Syllabus");
  }
 }
public class Main{
	public static void main(String[] args) {
	 	    Syllabus sy = new SQLSyllabus();
 	    sy.printMessage();
	}
}
```
<details><summary> Show Answer </summary>

<blockquote>

The above program will give a compile-time error. The compiler will throw 2 errors in this.

- `[Illegal Combination of modifiers: abstract and final] at line 1.`
- `[Cannot inherit from final ‘InterviewBit’] at line 4.`
- Abstract classes are incomplete classes that need to be inherited for creating their concrete classes,  the final keywords in class are used for avoiding inheritance. So these combinations are not allowed in Java.

</blockquote>

</details>


---

65.	Predict the output of the code snippet

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

``` java
public class Test {
public static void main(String[] args)
{
 int x = 10, y = 5;
 
 int exp1 = (y * (x / y + x / y));
 int exp2 = (y * x / y + y * x / y);
 
 System.out.println(exp1);
 System.out.println(exp2);
  }
}
```


<details><summary> Show Answer </summary>

<blockquote>

20
20

</blockquote>

<details><summary> Explanation </summary>

<blockquote>

- wo priority levels of arithmetic operations are used here . They are as follows:
- High priority ⇒ * / %
- Low priority ⇒ + –


</blockquote>

</details>

</details>

---

66. What should be in Line 4 to get the output 97?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

``` java
public class Main
{
	public static void main (String[] args) {
		Line 4;
		System.out.print(a);
	}
}
```


<details><summary> Show Answer </summary>

<blockquote>

int a = 'a'; 

</blockquote>

<details><summary> Explanation </summary>

<blockquote>

97 is the ASCII value of a. Since we declared the variable a as integer so it converts into ASCII value

</blockquote>


</details>

</details>

---

67. Predict the output of the following code snippet

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

```java
public class Main {
public static void main(String[] args)
{
   int a, b, Value = 10;
   a = b = 5;
   Value += ++a * b++;
   System.out.println("Final Value is = " +Value); 
  }
}
```
<details><summary> Show Answer </summary>

<blockquote>

40

</blockquote>

<details><summary> Explanation </summary>

<blockquote>

The value a holds 6 since its a pre increment operator and b holds 5 (post increment operator). value+= ++a * b++ gives value=value + ++a * b++. which returns 40 (value=10+(6*5)).

</blockquote>


</details>

</details>

---

68. Predict the output of the following code.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

``` java
public class Main {
public static void main (String[] args){
 int a = 10;
 System.out.println(++a++);
}
}
```
<details><summary> Explanation </summary>

<blockquote>

It will throw Compilation error. Preincrement & Postincrement operators are not allowed on same variable and same time.

</blockquote>


</details>

---

69.	Predict the output of the following output.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

```java

public class Main
{
    public void getval()
    {  
        int localVar = 0;
        localVar = localVar + 11;
      
    }
    public static void main(String args[])
    {
        Main obj = new Main();
        obj.getval();
          System.out.println("value of local variable" + " is: " + localVar);
    }
}
```
<details><summary> Show Answer </summary>

<blockquote>

If we use the local variable `localVar` outside `getLocalVarValue()` function, the compiler will produce an error as `Cannot find the symbol localVar`.


</blockquote>


</details>

---

70. How many times the output 'Have a nice day' will be printed?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

``` java

public class Main {
public static void main(String[] args){
 for(int i = 0; i<5; i++)
 {
 System.out.println("Have a nice day");
 break;
 }
}
}

```
<details><summary> Show Answer </summary>

<blockquote>

Only one time

</blockquote>

<details><summary> Explanation </summary>

<blockquote>

Because break is used in the for loop which will terminate the current loop

</blockquote>

</details>

</details>

---

71. How many times the output 'Good Day' will be printed?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

``` java 
public class Main {
public static void main(String[] args){
 for(int i = 0; i<5; i++)
 {
 System.out.println("Good Day");
 i++;
 }
}
}
```
<details><summary> Show Answer </summary>

<blockquote>

Good Day will be printed 3 times

</blockquote>

<details><summary> Explanation </summary>

<blockquote>

It is printed 3 times becuase the variable i is incremented 2 times for one iteration(in the loop and post increment is used after the display statement )

</blockquote>

</details>

</details>

---

72. Write the for loop statement in Line 4 to declare infinitive loop

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

``` java
public class Main {
    public static void main(String[] args)
    {
        // Line 4
        {
            System.out.println("infinitive loop");
        }
    }
}
```
<details><summary> Show Answer </summary>

<blockquote>

for (;;) using two semicolons ;; in the for loop will declare the infinitive for loop

</blockquote>

</details>

---

73. Can you find out the error in the below code?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

``` java
private class A
{
    private class B
    {
        //Inner class
    }
}
```

<details><summary> Show Answer </summary>

<blockquote>

Inner classes can be private, but outer classes can not be private.

</blockquote>

</details>

---

74. Predict the error in the following code snippet.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

``` java

class A
{
    private class B
    {
        //inner class
    }
}
 
public class MainClass extends A
{
    public static void main(String[] args)
    {
        B b = new B();
    }
}
```
<details><summary> Show Answer </summary>

<blockquote>

Here Private inner Class B can not be instantiated outside the Class A.

</blockquote>

</details>

---

75. Predict the error in the following code snippet.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

``` java

package pack1;
 
class A
{
     
}
 
package pack2;
 
class B extends A
{
     
}
```
<details><summary> Show Answer </summary>

<blockquote>

Class with default (no) access modifiers can not have subclass outside the package.

</blockquote>

</details>

---

76. Mr.XYZ has written the code like below but it is showing compile time error. Can you help him to remove the error?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

``` java
private class A
{
    private class B
    {
        private class C
        {
             
        }
    }
}
```
<details><summary> Show Answer </summary>

<blockquote>

Outer class can’t be private. Don’t declare Class A as private.

</blockquote>

</details>

---

77. Predict the output of the following code snippet.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

```java

public class Main
{
	public static String main(String[] args) {
		System.out.println("main method with ");
		return "Java Program without void";
	}
}
```

<details><summary> Show Answer </summary>

<blockquote>

Compilation error will occur stating that Main method must return a value of type void in class Main.

</blockquote>

</details>

</details>

---

78. Predict the output of the following code snippet.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

```java

public class Main{  
   int data=30;  
  static class Innerclass{  
   static void msg(){System.out.println("data is "+data);}  
  }  
  public static void main(String args[]){  
  Main.Innerclass.msg();
  }  
} 
```
<details><summary> Show Answer </summary>

<blockquote>

It will throw compilation error

</blockquote>

<details><summary> Explanation </summary>

<blockquote>

non-static variable cannot be used in a static class

</blockquote>

</details>

</details>

---

79. Predict the order of execution in the following program.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

```java

class Main {
    Main()
    {
        System.out.println("No  argument constructor");
    }
    static
    {
        System.out.println("1st static init");
    }
    {
        System.out.println("1st instance init");
    }
    public static void main(String[] args)
    {
        new Main();
    }
} 
```
<details><summary> Show Answer </summary>

<blockquote>

1st static init <br>
1st instance init <br>
No  argument constructor <br>

</blockquote>

</details>

---

80. How can we make the below code to work perfectly to print numbers from 0 to 9?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

```java
public class Main {
    public static void main(String[] args) {
        for(int i=0; i<10; i++) {
            System.out.println(i);
        }
        continue;
    }
}
```
<details><summary> Show Answer </summary>

<blockquote>

Continue cannot be declared outside the loop. so it should be moved from line 7  to line 5. 

</blockquote>

</details>

---

