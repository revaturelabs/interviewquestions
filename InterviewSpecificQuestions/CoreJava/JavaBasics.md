1. Tell us about Java

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
<blockquote>

Java is one of the most popular high level programming language. For example, its used to create mobile application like Netflix, Twitter, Spotify, and many more. Also, used in the server applications.

</blockquote>
</details>

--- 

2. What is the JDK?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>
 
- JDK - **J**ava **D**evelopment **K**it
- JDK contains everything that JRE has along with development tools for developing, debugging, and monitoring Java applications. 
- JDK used to develop Java applications.
- JDK contains compiler (javac.exe), Java application launcher (java.exe), Applet viewer, etc., 
    - javac - Java compiler translates java source code into byte code.

 
</blockquote>
</details>

--- 

3. What is the JRE?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>
 
- JRE - **J**ava **R**untime **E**nvironment 
- JRE is a software package which bundles the libraries (jars) and the JVM, and other components to run applications written in the Java. 
- To execute any Java application, you need JRE installed in the machine. It’s the minimum requirement to run Java applications on any computer.

 
</blockquote>
</details>

--- 

4. What is JVM?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>

- JVM - **J**ava **V**irtual **M**achine 
- JVM interprets the byte code into the machine code and execute it.
 
</blockquote>
</details>

--- 

5. What is the difference between JDK, JVM, & JRE?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>

**JDK** is a software development kit whereas **JRE** is a software bundle that allows Java program to run, whereas **JVM** is an environment for executing bytecode.
  
- JRE = JVM + libraries to run Java application
- JDK = JRE + tools to develop Java application

![image](https://user-images.githubusercontent.com/70228962/193740634-fbaf769e-ad53-45bd-86fb-36983e754ecc.png)

</blockquote>
</details>

--- 

6. What are the types of access modifiers? Which one is more protective?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>

Access modifiers allow us to set the scope or accessibility or visibility of a data member be it a field, constructor, class, or method.  The four different types of access specifiers
- Public
- Protected
- Private
- Default

Private is more protective. When the methods or data members declared as private, then we can access them only within the class in which they are declared.
 
</blockquote>
</details>

--- 


8. Tell us about non-access modifiers

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>

Non-access modifiers defines the behavior of the entities to the JVM, used with classes, variables, methods, constructors, etc. Some of the non access modifiers are

- static
- final
- abstract
- synchronized
 
</blockquote>
</details>

--- 

9. Brief us on Java Memory (or) How many memories are there in Java and what are they used for?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>

There are two kinds of memory used in Java:

- **Stack memory** stores primitive types and the addresses of objects. 
- **Heap memory** stores the value of the object. 

</blockquote>
</details>

--- 

10. What is garbage collection?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>
 
 Garbage collection is the process of looking at heap memory, identifying which objects are in use and which are not, and deleting the unused objects.
 
</blockquote>
</details>

--- 

11. Where are objects stored? (or) When an object is instantiated where is it stored?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>

Whenever an object is created, it's always stored in the Heap memory and stack memory contains the reference of it.
 
</blockquote>
</details>

--- 

12. What is local scope?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>

<summary> <b>Show Answer</b></summary>

<blockquote>
 
When we create a variable with in a method, it cannot be accessed outside that method. The scope of that variable is a local scope.

**Example:** Here `age` is a variable declared inside the `printAge()` method. It can be accessed only inside the `printAge()`. So, we can say `age` variable has a local scope

```java
public class Test {

	public void printAge() {
		int age = 7;
		System.out.println(age);
	}
}
```

 
</blockquote>
</details>

--- 

13. What is the difference between local scope and instance scope?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>

| Local Scope                                                                | Instance Scope                                                        |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------|
| Its the scope of the local variables                                       | Its the scope of the instance variables                               |
| Local variables are declared inside a method or a block.                   | Instance variables are declared inside a class, but outside a method. |
| Local variables are visible only in the method or block they are declared. | Instance variables can been seen by all methods in the class.         |
 
</blockquote>
</details>

--- 

14. What are the different scopes in java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>

Variables can be defined as having one of three types of scope: 

- **Class level scope or Instance scope** (instance variables): Any variable declared within a class is accessible by all methods in that class. 
- **Method level scope or Local scope** (local variables): Any variable declared within a method and arguments is only accessible inside that method.
- **Block scope** (loop variables): Any variable declared in a for loop condition is not accessible after the loop, unless you defined it beforehand.
 
</blockquote>
</details>

--- 

15. What is static in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>

- Its a non access modifier
- Its used to share the same variable or method of a given class
- When we declare a variable or method as static that will not belong to any object, it belongs to the class. 
- There is no need to create an object for the class to access the static variable or static method. 
- We can use the class name to call them with respect to the access modifier.
- If we use the object name to call the static method or variable, the compiler will replace the name of the object with class.
 
</blockquote>
</details>

--- 

16. What does the Final keyword mean for Variables, Methods, and Classes?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>

final keyword is a non-access specifier that can be used with class, variable, and method to restrict changes or make it as constant. 

- If we initialize a variable with the final keyword, then we cannot modify its value.
- If we declare a method as final, then it cannot be overridden by any subclasses. 
- And, if we declare a class as final, we restrict the other classes to inherit or extend it.

```

Final Variable  ---> To create constant variable
Final Method    ---> Prevents Method Overriding
Final Class     ---> Prevents Inheritance

```

 
</blockquote>
</details>

--- 


17. Explain each of the parts of `public static void main (String[] args)`

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>
 
 `public static void main(String[] args)` -  main method is the e**ntry point of any java program**

- `public` is an access specifierof the main method. It has to be `public` so that java runtime can execute this method. 
- `static` is non-access modifier. When java runtime starts, there is no object of the class present. That’s why the main method has to be static so that JVM can load the class into memory and call the main method.
- `void`is a return type, means main method not going to return anything. 
- `main` is a method name  
- `String[] args` - Java main method accepts a single argument of type String array. This is also called as java command line arguments.
 
</blockquote>
</details>

--- 

18. What happens if you don’t make the main method static?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>

If the main method won't be static, JVM would not be able to call it because there is no object of the class is present.

</blockquote>
</details>

--- 

19. What is the difference between a Heap and a Stack?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>
	
| Stack Memory                                                                                                                                                                            | Heap Memory                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Stack memory is the space allocated for a process where all the function calls, primitive data types (int, double, etc.) and local and reference variables of the functions are stored. | Heap memory is used to store the objects that are created during the execution of a Java program. The reference to the objects that are created is stored in stack memory. |
| Stack memory is always referenced in LIFO (Last-In-First-Out) order.                                                                                                                    | Heap follows dynamic memory allocation (memory is allocated during execution or runtime) and provides random access                                                     |


 
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

8.	Differentiate between `System. Out`, `System. Err`, and `System.in`?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

- `System.out` is used to display normal messages and results. 
- `System.err` is used to display error messages. 
- `System.in` represents InputStream object which by default represents standard input device, i.e., 
keyboard.

`System.out` and `System.err` represent the monitor by default and can be used to send data or results to the monitor. 

</blockquote>

</details>


---

19. Can a static method access non-static variables or methods? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

No,  A static method cannot access non-static variables or methods because static methods can be accessed without instantiating the class, so if the class is not instantiated the variables are not initialized and thus cannot be accessed from a static method.

</blockquote>

</details>