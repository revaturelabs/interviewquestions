1. What is Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
<blockquote>

Java is one of the most popular high level programming languages. For example, its used to create mobile application like Netflix, Twitter, Spotify, and many more. Also, used in the server applications.

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

Access modifiers allow us to set the scope or accessibility, or visibility of a data member be it a field, constructor, class, or method.  The four different types of access specifiers
- Public
- Protected
- Private
- Default

Private is more protective. When the methods or data members declared as private, then we can access them only within the class in which they are declared.
 
</blockquote>
</details>

--- 


7. Tell us about non-access modifiers

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>

Non-access modifiers define the behavior of the entities to the JVM, used with classes, variables, methods, constructors, etc. Some of the non-access modifiers are

- static
- final
- abstract
- synchronized
 
</blockquote>
</details>

--- 

8. Brief us on Java Memory (or) How many memories are there in Java and what are they used for?

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

9. What is garbage collection?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>
 
 Garbage collection is the process of looking at heap memory, identifying which objects are in use and which are not, and deleting the unused objects.
 
</blockquote>
</details>

--- 

10. Where are objects stored? (or) When an object is instantiated where is it stored?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>

Whenever an object is created, it's always stored in the Heap memory and stack memory contains the reference of it.
 
</blockquote>
</details>

--- 

11. What is local scope?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>

<summary> <b>Show Answer</b></summary>

<blockquote>
 
When we create a variable within a method, it cannot be accessed outside that method. The scope of that variable is a local scope.

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

12. What is the difference between local scope and instance scope?

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

13. What are the different scopes in java?

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

14. What is static in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>

- It’s a non-access modifier.
- It’s used to share the same variable or method of a given class.
- When we declare a variable or method as static that will not belong to any object, it belongs to the class. 
- There is no need to create an object for the class to access the static variable or static method. 
- We can use the class name to call them with respect to the access modifier.
- If we use the object name to call the static method or variable, the compiler will replace the name of the object with class.
 
</blockquote>
</details>

--- 

15. What does the Final keyword mean for Variables, Methods, and Classes?

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


16. Explain each of the parts of `public static void main (String[] args)`

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>
 
 `public static void main(String[] args)` -  main method is the e**ntry point of any java program**

- `public` is an access specifier of the main method. It must be `public` so that java runtime can execute this method. 
- `static` is non-access modifier. When java runtime starts, there is no object of the class present. That’s why the main method must be static so that JVM can load the class into memory and call the main method.
- `void`is a return type, means main method not going to return anything. 
- `main` is a method name  
- `String[] args` - Java main method accepts a single argument of type String array. This is also called as java command line arguments.
 
</blockquote>
</details>

--- 

17. What happens if you don’t make the main method static?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>

If the main method won't be static, JVM would not be able to call it because there is no object of the class is present.

</blockquote>
</details>

--- 

18. What is the difference between a Heap and a Stack?

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

19. Does the program run if we give `static public void main`?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

Yes, the program will execute successfully.  Because, in Java, there is no specific rule for the order of specifiers

</blockquote>

</details>


---

20. Differentiate between `System. Out`, `System. Err`, and `System.in`?

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

21. Can a static method access non-static variables or methods? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

No, A static method cannot access non-static variables or methods because static methods can be accessed without instantiating the class, so if the class is not instantiated the variables are not initialized and thus cannot be accessed from a static method.

</blockquote>

</details>

22. What are hashes in java?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

In Java, hashes usually refer to the hash codes generated by the `hashCode()` method in object. The `hashCode()` method returns an integer value that is often used as an index in hash tables or for other purposes that require a unique identifier for an object. 

</blockquote>

</details>

---

23. Give me a few Object methods.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Few commonly used Object methods in Java are:

1. **`toString()`:** returns a string representation of the object.
2. **`equals(Object obj)`:** compares the current object with the specified object for equality.
3. **`hashCode()`:** returns a hash code value for the object.
4. **`getClass()`:** returns the runtime class of the object.
5. **`wait()`:** causes the current thread to wait until another thread invokes the `notify()` method or the `notifyAll()` method for this object.
6. **`notify()`:** wakes up a single thread that is waiting on this object's monitor.
7. **`notifyAll()`:** wakes up all threads that are waiting on this object's monitor.
8. **`clone()`:** creates and returns a copy of the object.
9. **`finalize()`:** called by the garbage collector before the object is destroyed.


</blockquote>

</details>

---


24.  How is garbage collection done in Java? Does it stop our program from running? (Apparently, there is another type of garbage collector which occurs when the program is running out of memory. This second type DOES stop the JVM while the normal one runs on a daemon thread).


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

- The most common garbage collector in Java is the concurrent mark and sweep collector, which runs on a background daemon thread and does not stop the application's threads from running. This collector identifies unused objects and frees their memory as needed, without causing significant interruptions to the application's performance.

- The secont one is stop-the-world collector, it is triggered when the JVM detects that the application is running low on available memory. When this occurs, the collector will pause the application's threads and perform a full garbage collection cycle to reclaim as much memory as possible. This pause can potentially cause a noticeable interruption in the application's performance, particularly if the heap is large and the garbage collection process takes a significant amount of time to complete.


</blockquote>

</details>

---

25. What would you change about Java ?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Suggestions for improving Java are:

1. Reduced Boilerplate
2. Better Integration with Functional Programming
3. Improved Performance
4. Simplified Concurrency
5. Better Support for Reactive Programming


</blockquote>

</details>

---

26. what is dynamic hashing?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Dynamic hashing is a technique used to optimize hash table performance in Java and other programming languages. It involves creating a hash table that can dynamically resize itself when the number of keys or elements in the table exceeds a certain threshold.

In Java, dynamic hashing can be implemented using classes such as HashMap, Hashtable, or ConcurrentHashMap. These classes use a hash function to map keys to indices in an array, where the correspon

</blockquote>

</details>

---

27. what is dynamic hashing?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

| Feature           | `this`                                                       | `super`                                                                                                   |
| ----------------- | ------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------- |
| Usage             | Refers to the current object instance                        | Refers to the parent class of the current object instance                                                 |
| Accessing Fields  | Used to access fields and methods in the current class       | Used to access fields and methods in the parent class                                                     |
| Method Overriding | Used to call a method or access a field in the current class | Used to call a method or access a field in the parent class, even if it's been overridden in the subclass |
| Method Scope      | Can be used in any class method                              | Can only be used in a subclass that inherits from a parent class                                          |
| Constructor Usage | Used to call another constructor in the same class           | Used to call a constructor in the parent class                                                            |
| Syntax Example    | `this.fieldName` or `this.methodName()`                      | `super.fieldName` or `super.methodName()`                                                                 |


</blockquote>

</details>

---

28. What are different array methods ?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

There are several array methods in Java that can be used to manipulate arrays. Some commonly used array methods:

1. **`length`:** This method returns the length of an array, i.e., the number of elements in the array.

2. **`clone`:** This method creates a new array with the same elements as the original array.

3. **`copyOf`:** This method creates a new array with the specified length, and copies elements from the original array into the new array. If the original array is shorter than the specified length, the new array is padded with default values.

4. **`fill`:** This method fills the elements of an array with a specified value.

5. **`sort`:** This method sorts the elements of an array in ascending order.

6. **`binarySearch`:** This method searches an array for a specified value using the binary search algorithm.

7. `equals`: This method compares two arrays for equality. Two arrays are considered equal if they have the same length and contain the same elements in the same order.

An example that uses some of these array methods:

```java
int[] arr1 = {2, 5, 1, 9, 7};
int[] arr2 = arr1.clone(); // creates a new array with the same elements
int[] arr3 = Arrays.copyOf(arr1, 7); // creates a new array with length 7, padded with default values
Arrays.fill(arr1, 0); // fills all elements of arr1 with the value 0
Arrays.sort(arr2); // sorts the elements of arr2 in ascending order
int index = Arrays.binarySearch(arr2, 5); // searches for the value 5 in arr2 using binary search
boolean equal = Arrays.equals(arr1, arr3); // compares arr1 and arr3 for equality
```

</blockquote>

</details>

---


29. What are the features of Java?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Some features of Java include: 
- Object-oriented programming
- Platform independence
- Memory management through garbage collection
- Exception handling
- Multithreading 
- Security features
- Rich API 
- High performance and scalability
- Open-source community

</blockquote>

</details>

---

30. how would you make an object immutable?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

To make an object immutable in Java, you can follow these steps:

1. Declare the class as final to prevent inheritance.
2. Declare all fields as private and final to prevent modification.
3. Do not provide any setter methods for the fields.
4. Initialize all fields via constructor.
5. Prevent any methods from changing the state of the object.


</blockquote>

</details>

---



31. What do you need to have to actually run a Java application?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

To run a Java application, you need to have the Java Runtime Environment (JRE) installed on your system, which includes the Java Virtual Machine (JVM) that is responsible for executing Java bytecode. You also need the Java application itself, which is typically compiled into bytecode and saved in a .class file.

</blockquote>

</details>

---

32. Volatile keywords?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The `volatile` keyword in Java is used to indicate that a variable's value may be modified by multiple threads at the same time. Without the `volatile` keyword, different threads may create their own copy of that variable which will contain a different value for a different thread. This can lead to incorrect results. The `volatile` keyword helps to prevent this by forcing threads to always read the variable's value from main memory, rather than from a cached copy.

</blockquote>

</details>

---

33. What is finalize?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

`finalize()` is a method in Java that gets called by the garbage collector when an object is about to be destroyed. It can be used to perform any necessary cleanup operations before the object is removed from memory.

</blockquote>

</details>

---

34. What would you use if you couldn't instantiate an object in Java (referring to static, I believe)?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Yes, you can use static variables and methods in Java, which belong to the class rather than any specific instance of the class. You can access static variables and methods without creating an object of the class.

</blockquote>

</details>

---

35. What is immutability?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Immutability is the property of an object that once created, cannot be modified. In Java, you can make an object immutable by declaring all of its fields as final and not providing any setter methods.

</blockquote>

</details>

---

36. How to compile Java code?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

To compile Java code, you need to use the Java compiler (javac) that comes with the Java Development Kit (JDK). You can compile a Java file by running the command "javac filename.java" on the command line. This will generate a .class file that contains the compiled bytecode.

</blockquote>

</details>

---

37. What is JVM?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

JVM stands for Java Virtual Machine. It is a software environment that runs Java bytecode. The JVM is responsible for interpreting the bytecode and executing it on the underlying operating system. It provides a platform-independent way of running Java code.

</blockquote>

</details>

---

38. Tell me about Java.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Java is a general-purpose programming language that is used to build a wide variety of applications, including desktop software, web applications, and mobile apps. It is an object-oriented language that is designed to be platform-independent, meaning that Java programs can run on any operating system that has a Java Virtual Machine (JVM) installed.

</blockquote>

</details>

---

39. What is the default directory for a Jar file?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The default directory for a Jar file is the directory from which the Java command is executed. If you are executing the Jar file from the command line, you can use the "-jar" option to specify the Jar file to be executed, like this: "java -jar filename.jar".

</blockquote>

</details>

---

40. What does System.out.println() mean?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

System.out.println() is a Java statement that is used to print output to the console. The System class is a predefined class in Java, and the out object represents the standard output stream. The println() method is used to print a string to the console, followed by a newline character.

</blockquote>

</details>

---

41. Java different versions.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

There are four types of Java editions:

1. **Java Standard Edition (Java SE):** This edition is used to develop desktop applications and is the foundation for developing other editions. It includes the core language and libraries used to build Java applications.

2. **Java Enterprise Edition (Java EE):** This edition is used for developing web applications and enterprise software. It includes additional libraries and APIs for building web applications, such as servlets, JavaServer Pages (JSP), and Enterprise JavaBeans (EJB).

3. **Java Micro Edition (Java ME):** This edition is used for developing applications for small devices, such as mobile phones and PDAs. It includes a small-footprint runtime environment and APIs for building mobile applications.

4. **JavaFX:** This is a platform for building rich media and interactive applications. It includes a scripting language, APIs for building UI components, and support for multimedia and web services.


</blockquote>

</details>

---


42.  Does Java allow static classes?
    
<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Yes, Java allows the creation of static classes, which are often used as utility classes. Static classes can only contain static members, such as static variables, methods, and nested classes.

</blockquote>

</details>

---

43.  Explain what a static method is in Java.
<details><summary><b> Show Answer</b></summary>
  
<blockquote>

In Java, a static method is a method that belongs to a class rather than to an instance of the class. This means that you can call a static method on the class itself, without needing to create an instance of the class first. A static method can access only other static members of the class and can't access non-static members.

</blockquote>

</details>

---

44. Can you override static method? can you override the main method?


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

You can't override a static method in Java because a static method is associated with a class rather than with an instance of the class. However, you can declare a static method with the same name as a method in a superclass, which is known as method hiding. You can override the main method in Java, but doing so is not recommended because it can cause confusion and make your code harder to maintain.

</blockquote>

</details>

---

45.  What was the difference between static and non-static methods?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The main difference between static and non-static methods is that a static method belongs to a class, while a non-static method belongs to an instance of the class. This means that you can call a static method on the class itself, while you can only call a non-static method on an instance of the class. Static methods can't access non-static members, while non-static methods can access both static and non-static members.

</blockquote>

</details>

---

46.  What is the difference between a static variable and a non-static variable?
  
<details><summary><b> Show Answer</b></summary>
  
<blockquote>
A static variable belongs to a class, while a non-static variable belongs to an instance of the class. This means that you can access a static variable using the class name, while you need to create an instance of the class to access a non-static variable. Static variables are shared among all instances of the class, while non-static variables have separate values for each instance.

</blockquote>

</details>

---

47.  Can a static variable be private?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>
Yes, a static variable can be private in Java. Access modifiers like private, public, and protected can be used with static variables just like with non-static variables.

</blockquote>

</details>

---

48.  When is memory allocated for static blocks?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Memory for static blocks is allocated when the class is loaded into memory by the JVM. Static blocks are executed only once, when the class is loaded, so any memory allocation required by the static block is done at that time.

</blockquote>

</details>

---

49.  What is the difference between static variable and instance variable?


<details><summary><b> Show Answer</b></summary>
<blockquote>

In Java, a static variable is a class-level variable that is shared among all instances of that class. It can be accessed using the class name followed by the dot operator, like ClassName.staticVariable. On the other hand, an instance variable is a variable that belongs to a specific instance of a class. It is not shared among other instances of that class and can be accessed using the instance name followed by the dot operator, like instanceName.instanceVariable.

</blockquote>
</details>

---

50. static method in Java.


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

A static method is a method which belongs to a class and can be called directly using the class without creating an object of that class. To define a method as a static method, `static` keyword is used in the method signature. Static methods are often used for utility functions, factory methods, or defining constants associated with a class. The static methods cannot access non-static members of a class and cannot be overridden by subclasses.

</blockquote>

</details>

---

51. can we override static methods. 


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

No, static methods cannot be overridden in Java. When a subclass defines a static method with the same signature as a static method in the superclass, the method in the subclass is not considered as an override of the method and the method in superclass gets executed whenever we call the method.

</blockquote>

</details>

---

52. How would you optimize memory in Java?

<details><summary><b> Show Answer</b></summary> 

<blockquote> 

Here are some ways to optimize memory in Java:

1. Avoid creating unnecessary objects.
2. Use primitive types instead of wrapper classes.
3. Use immutable objects when possible.
4. Use static final variables for constants.
5. Avoid using String concatenation in loops.
6. Use StringBuilder or StringBuffer for String manipulation.
7. Use object pooling to reuse objects.

</blockquote> 

</details>

---

53.  How do you make sure memory is being utilized optimally in Java?

<details><summary><b> Show Answer</b></summary> 

<blockquote> 

To make sure memory is being utilized optimally in Java, you can follow these steps:

1. Monitor the memory usage of your application using tools like JConsole or VisualVM.
2. Use a profiler to identify memory leaks or areas where memory usage can be optimized.
3. Avoid creating unnecessary objects and make sure to release resources when they are no longer needed.
4. Use object pooling to reuse objects instead of creating new ones.

</blockquote> 

</details>

---

54.  Can you have the garbage collector immediately de-allocate memory?

<details><summary><b> Show Answer</b></summary> 

<blockquote> 

In Java, you cannot directly control when the garbage collector deallocates memory. The garbage collector runs automatically in the background, deallocating memory for objects that are no longer in use. You can suggest to the garbage collector to run by calling `System.gc()`, but there is no guarantee that it will run immediately.

</blockquote> 

</details>

---

55. What is object pooling?

<details><summary><b> Show Answer</b></summary> 

<blockquote> 

Object pooling is a technique used in software development to improve performance and reduce memory usage. It involves creating a pool of reusable objects and reusing them instead of creating new objects each time they are needed. This reduces the overhead of object creation and garbage collection, which can improve performance and reduce memory usage.

</blockquote> 

</details>