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

56. How is a yield different from a return?

<details><summary><b> Show Answer</b></summary> 

<blockquote> 

In Java, "yield" and "return" are two different keywords with distinct meanings.

1. `return` is used to exit a method and return a value to the caller. for example:

```java
public int add(int a, int b) {
    int sum = a + b;
    return sum; // using "return" to exit the method and return the value of sum to the caller
}
```
In the example above, the "add" method takes two integer arguments and returns their sum using the "return" keyword.

2. `yield` is used in switch expressions to provide a value based on a specific condition. for example:

```java
public String getDayOfWeek(int day) {
    return switch (day) {
        case 1 -> "Monday";
        case 2 -> "Tuesday";
        case 3 -> "Wednesday";
        case 4 -> "Thursday";
        case 5 -> "Friday";
        case 6 -> "Saturday";
        case 7 -> "Sunday";
        default -> throw new IllegalArgumentException("Invalid day of the week: " + day);
    };
}
```

In the above example  the "case" keyword is used to define a specific case or condition, and the "-> yield" expression is used to provide the value to be returned for that case.

</blockquote> 

</details>

57. What is a primitive data type?

<details><summary><b> Show Answer</b></summary> 

<blockquote> 

In Java, a primitive data type is a data type that is not an object and has no methods. It is a basic data type that is predefined by the language and is represented by a reserved keyword. Primitive data types are used to represent simple values, such as numbers or characters, and are stored directly in memory.

</blockquote> 

</details>

58.  List any primitives you know
<details><summary><b> Show Answer</b></summary> 

<blockquote> 

Here are some examples of primitive data types in Java:
- boolean: represents a true or false value
- byte: represents an 8-bit integer value
- short: represents a 16-bit integer value
- int: represents a 32-bit integer value
- long: represents a 64-bit integer value
- float: represents a single-precision floating-point value
- double: represents a double-precision floating-point value
- char: represents a single Unicode character

</blockquote> 

</details>

59. What is the difference between float and double? (Why do we use these two data types?)
<details><summary><b> Show Answer</b></summary> 

<blockquote> 

In Java, float and double are both used to represent floating-point numbers, which are numbers that have a fractional part. The main difference between float and double is their precision and the amount of memory they require to store values.

- float: represents a 32-bit floating-point value, with a range of approximately ±3.4 x 10^38 and a precision of about 6-7 decimal digits.
- double: represents a 64-bit floating-point value, with a range of approximately ±1.7 x 10^308 and a precision of about 15-16 decimal digits.

Double is generally used when more precision is needed, such as in scientific calculations or financial applications. Float is used when memory is a concern and the extra precision is not necessary. In practice, double is the more commonly used floating-point data type in Java.

</blockquote> 

</details>


60. Why do we use public and private access modifiers.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The access modifiers are used to control the visibility and accessibility of class members such as variables, methods, and inner classes.

When a class, method, or variable is declared as `public`, it can be accessed from any other part of the program. For example, if a method is declared as `public`, it can be called from any other class in the program. When a class, method, or variable is declared as `private`, it can only be accessed within the same class. This is useful when we want to restrict access to certain classes or methods to only the class in which they are declared. 

</blockquote>

</details>

---

61. Object class methods

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The object class have methods like:

- `toString()`: This method returns a string representation of the object.

- `equals(Object obj)`: This method checks whether the current object is equal to the specified object.

- `hashCode()`: This method returns a hash code for the object.

- `getClass()`: This method returns the class object of the current object.

- `clone()`: This method creates a new object with the same values as the current object.

- `finalize()`: This method is called by the garbage collector before the object is destroyed.

- `notify()`: This method wakes up a single thread that is waiting on the object's monitor.

- `notifyAll()`: This method wakes up all threads that are waiting on the object's monitor.

</blockquote>

</details>

---


62. super class of all java classes. 

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The superclass of all Java classes is the `Object` class. So, all classes in Java inherit the methods defined in the Object class, such as `toString()`, `equals()`, and `hashCode()`.

</blockquote>

</details>

---

25. Volatile keywords?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The `volatile` keyword in Java is used to indicate that a variable's value may be modified by multiple threads at the same time. Without the `volatile` keyword, different threads may create their own copy of that variable which will contain a different value for a different thread. This can lead to incorrect results. The `volatile` keyword helps to prevent this by forcing threads to always read the variable's value from main memory, rather than from a cached copy.

</blockquote>

</details>

---

63. What are the control statements.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Control statements in Java are used to control the flow of execution in a program. They include conditional statements like if-else and switch-case, and iterative statements like for, while, and do-while. These statements are essential for programming logic and enable the developer to control the sequence of execution.

</blockquote>

</details>

---

64. When would you use the final keyword?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

In Java, the `final` keyword is used to declare that a variable, method, or class cannot be changed or overridden. Here are some scenarios where the `final` keyword would be useful:

1. Constants: If you want to define a value that should not be changed during runtime, you can declare it as a `final` variable. For example:

   ```java
   final int MAX_VALUE = 100;
   ```

2. Security: If you want to prevent a method from being overridden in a subclass, you can declare it as `final`. This can be useful for security-related methods, such as password verification or encryption.

3. Efficiency: Declaring a variable or parameter as `final` can help the compiler optimize your code, because it knows that the value cannot change and can make certain assumptions.


Overall, the `final` keyword is a useful tool for creating constants, improving security, optimizing code, and improving clarity.

</blockquote>

</details>

---

65. What is `finalize`?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

`finalize` is a method provided by the `Object` class in Java that is called by the garbage collector when an object is about to be destroyed. Its purpose is to perform any necessary cleanup operations before the object is destroyed, such as releasing resources like file handles, database connections, or network sockets.

</blockquote>

</details>
---

66. What is the difference between `final`, `finally`, and `finalize`, and what situations are they used in?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

`final` is a keyword used to create constants or immutable variables, `finally` is a block used to define a code section that will be executed after a try/catch block, regardless of whether an exception is thrown or not, and `finalize` is a method called by the garbage collector when an object is about to be destroyed, used for resource cleanup.

</blockquote>

</details>


--- 

67. Can the garbage collector be manually called?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The garbage collector in Java is automatically called by the JVM, and it cannot be manually called by the programmer. The garbage collector runs periodically in the background, and its behavior is influenced by various factors such as the heap size, the amount of available memory, and the type of garbage collector being used. The garbage collector is responsible for freeing up memory used by objects that are no longer referenced by any part of the program.

</blockquote>

</details>

--- 

68. What are the levels of garbage collection?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

There are several levels of garbage collection in Java, including:

- Young generation: This is where new objects are created, and the garbage collector runs frequently to remove short-lived objects that are no longer referenced.
- Old generation: This is where long-lived objects are stored, and the garbage collector runs less frequently to remove objects that are no longer referenced.
- Permanent generation: This is where metadata for the Java classes is stored, and the garbage collector runs even less frequently than in the old generation.
- Metaspace: This is where metadata for the Java classes is stored, and it is a replacement for the Permanent generation starting from Java 8.

The exact configuration and behavior of garbage collection in Java depend on the JVM implementation and the runtime options that are used.

</blockquote>

</details>

--- 

69. How does an object progress through those garbage collection levels?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

In Java, when a new object is created, it is initially allocated in the young generation. The young generation is divided into two spaces: an `eden` space and a `survivor` space. When the `eden` space becomes full, a minor garbage collection is triggered, and any objects that are still referenced are moved to the `survivor` space. If an object survives multiple minor garbage collections, it is promoted to the old generation.

Objects in the old generation are subject to major garbage collections, which run less frequently than minor garbage collections. The goal of a major garbage collection is to free up space in the old generation by identifying and removing objects that are no longer referenced. If an object survives a major garbage collection, it remains in the old generation until it is no longer referenced or until the program terminates.

</blockquote>

</details>

--- 

70. How does garbage collection work? 

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Garbage collection is used in Java to perform automatic memory management. It deletes the objects in memory that are no longer being used by the program, and freeup the space in memory. When an object is created, Java keeps track of its reference count. When an object is no longer referenced by the program, its reference count is reduced to zero, and it becomes eligible for garbage collection. The garbage collector periodically scan the heap for objects that have a reference count of zero and delete them. It helps prevent memory leaks and makes programming in Java more convenient and safe.

</blockquote>

</details>

---

71. How do you copy an array?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

In Java, you can copy an array using the `System.arraycopy` method or by using the `Arrays.copyOf` method. 
Here's an example using `Arrays.copyOf`:

```java
int[] arr1 = {1, 2, 3};
int[] arr2 = Arrays.copyOf(arr1, arr1.length);
```

This creates a new array `arr2` that is a copy of `arr1`.

</blockquote>

</details>

---

72. Write an array and give some values, then print them. What are different array methods you have used?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Here's an example of creating an array of integers, initializing it with some values, and then printing them:

```java
int[] numbers = { 1, 2, 3, 4, 5 };
for (int i = 0; i < numbers.length; i++) {
    System.out.println(numbers[i]);
}
```

This creates an array `numbers` with five integer values, and then loops through the array using a `for` loop to print each value to the console.

</blockquote>

</details>

---

73. Given an array, create a list of pairs of indexes that sum to a target value.

<details><summary><b> Show Answer</b></b></summary>

<blockquote>

In Java, you can create a list of pairs of indexes that sum to a target value using a hash map. Here's an example:

```java
int[] arr = { 2, 7, 11, 15 };
int target = 9;
Map<Integer, Integer> map = new HashMap<>();
List<List<Integer>> result = new ArrayList<>();
for (int i = 0; i < arr.length; i++) {
    int complement = target - arr[i];
    if (map.containsKey(complement)) {
        List<Integer> pair = Arrays.asList(map.get(complement), i);
        result.add(pair);
    }
    map.put(arr[i], i);
}
System.out.println(result);
```

This creates an array called `arr` with four integer values, and a target value of 9. It then uses a `for` loop to iterate through the array, checking if there is a complement value in a hash map. If there is a complement value, it creates a pair of indexes and adds them to a list called `result`. Finally, it prints the `result` list to the console. The output of this example will be `[[0, 1]]`, which indicates that the pairs of indexes that sum to 9 are (0,1) in the input array `arr`.

</blockquote>

</details>

74. Are you able to store integers in an array?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Yes, you can store integers in an array in Java. In fact, arrays are one of the primary data structures used for storing and manipulating collections of integers or other data types.

To create an array of integers in Java, you can use the following syntax:

```java
int[] numbers = new int[] { 1, 2, 3, 4, 5 };
```

This creates an array called `numbers` that contains five integer values.

</blockquote>

</details>

75. What are annotations and what are they good for?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Annotations in java provide metadata about the class, method, and interface. They are used to provide additional information to the compiler about a programming element like a method or class to provide additional functionality. In Java, annotations are represented using the @ symbol followed by the annotation name.

</blockquote>

</details>

---

76. Return the peak value index from an integer array mountain.

<details><summary><b> Show Answer</b></summary>

<blockquote>

To return the peak value index from an integer array mountain, you can use the following algorithm:

1. Initialize two pointers, `left` and `right`, to point to the first and last elements of the array, respectively.
2. While `left < right`:
   - Calculate the middle index, `mid`, as `(left + right) / 2`.
   - If `array[mid] < array[mid+1]`, set `left` to `mid+1`.
   - Otherwise, set `right` to `mid`.
3. Return `left` as the peak value index.

This algorithm works by repeatedly dividing the array in half and checking whether the middle element is part of an increasing or decreasing sequence. The peak value index is where the increasing sequence ends and the decreasing sequence begins.

</blockquote>

</details>

--- 

77. what is typecasting.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Typecasting is the process of converting a value of one data type to another data type. There are two types of typecasting implicit and explicit. In Implicit typecasting a smaller data type is converted to a larger data type. For example, converting an int to a long or a float to a double. The implicit typecasting happens automatically.In Explicit typecasting, also known as narrowing conversion, a larger data type is converted to a smaller data type. It requires the programmer to specify the type to which the value is going to be cased. For example, converting a double to an int.

</blockquote>

</details>

---

78. What is immutable in Java?

<details><summary> Show Answer </summary>

<blockquote>

In Java, an immutable object is an object whose state cannot be changed once it is created. Once the object is created, any attempt to modify its state will result in the creation of a new object with the modified state. Immutable objects are thread-safe and can be shared without the risk of concurrent modification. Examples of immutable classes in Java include String, Integer, and BigDecimal.

</blockquote>

</details>

---

79. Can you tell us something on mutable and immutable class in Java? 

<details><summary> Show Answer </summary>

<blockquote>

In Java, a mutable class is a class whose objects can be modified after creation, while an immutable class is a class whose objects cannot be modified after creation. In a mutable class, the state of the object can be changed by invoking methods or modifying fields, whereas in an immutable class, the state of the object is fixed and cannot be changed.

An example of a mutable class in Java is the StringBuilder class, which allows the modification of the string content by appending, deleting, or replacing characters. On the other hand, an example of an immutable class in Java is the String class, whose objects cannot be modified once created, and any operation on the string creates a new string object.

</blockquote>

</details>

---

80. What is the difference between extends and implements in Java? 

<details><summary> Show Answer </summary>

<blockquote>

In Java, `extends` and `implements` are both keywords used for inheritance, but they have different meanings.

`extends` is used to create a subclass that inherits properties and methods from a parent class. The subclass can add or override properties and methods of the parent class.

`implements` is used to make a class implement an interface. An interface is a collection of abstract methods that a class must implement. When a class implements an interface, it agrees to provide the implementations for all the methods defined in the interface.

</blockquote>

</details>

---

81. What is the use of getter and setter in java?

<details><summary> Show Answer </summary>

<blockquote>

In Java, getters and setters are methods used to access and modify the values of private fields in a class.

A getter method retrieves the value of a private field and returns it to the caller. This allows other classes to access the private field without exposing the implementation details of the class.

A setter method sets the value of a private field based on the value passed to it as a parameter. This allows other classes to modify the value of the private field without exposing the implementation details of the class.

</blockquote>

</details>

---

82. How does the Java ternary operator works?

<details><summary> Show Answer </summary>

<blockquote>

The Java ternary operator (also called conditional operator) is a shorthand way of writing an if-else statement. It takes three operands: a Boolean expression, a value to return if the expression is true, and a value to return if the expression is false. The syntax is:

```Java
variable = (condition) ? true-value : false-value;
```

If the condition is true, the variable will be assigned the value of true-value, otherwise it will be assigned the value of false-value.

</blockquote>

</details>

---

83. How do you write for a phone number using regex in Java?

<details><summary> Show Answer </summary>

<blockquote>

To write a regex pattern for a phone number in Java, you can use the following pattern:

```Java
String regex = "^\\+(?:[0-9] ?){6,14}[0-9]$";
```

This pattern matches phone numbers in the format of a plus sign, followed by six to fourteen digits, with optional spaces between the digits.

Here's an explanation of the different parts of the pattern:

`^` - Matches the start of the string
`\\+` - Matches a literal plus sign
`(?:[0-9] ?)` - Matches a single digit with an optional space character
`{6,14}` - Specifies the minimum and maximum number of times the previous match can occur, in this case, between 6 and 14 times.
`[0-9]` - Matches a single digit
`$` - Matches the end of the string.

</blockquote>

</details>

---

84. Do you know about Java Messaging Service in Java?

<details><summary> Show Answer </summary>

<blockquote>

Yes, Java Messaging Service (JMS) is a Java-based messaging standard that allows distributed applications to communicate with each other. It is a message-oriented middleware API that allows Java applications to send and receive messages asynchronously.

JMS provides a common way for applications to create, send, receive, and read messages. It defines a set of standard interfaces and protocols that enable seamless communication between different messaging systems, such as IBM MQ, Apache ActiveMQ, and RabbitMQ.

</blockquote>

</details>

---

85. How does JNDI works?

<details><summary> Show Answer </summary>

<blockquote>

JNDI stands for Java Naming and Directory Interface, and it is a standard interface to access naming and directory services in Java. It provides a common interface for accessing naming and directory services, regardless of the underlying technology used by the service.

In JNDI, you can bind objects to names in a hierarchical namespace, which can be accessed by clients using a standard API. This allows you to separate the location of objects from the code that uses them, making it easier to manage and maintain distributed systems.

</blockquote>

</details>

---

86. How do you differentiate groovy from java using syntax?


<details><summary> Show Answer </summary>

<blockquote>

Groovy and Java have similar syntax, but there are a few key differences:

`Semicolons`: In Java, semicolons are required at the end of each statement, but in Groovy, they are optional.

`Type Declaration`: Java is a statically typed language, which means that you must declare the data type of a variable before you use it. Groovy, on the other hand, is a dynamically typed language, so you do not need to declare the data type of a variable.

`String Concatenation`: In Java, you can concatenate strings using the "+" operator, while in Groovy, you can use either "+" or the string interpolation syntax, which uses "${}".

`Method Definition`: In Java, you define a method using the "public static void" syntax, while in Groovy, you can omit the "public" and "void" keywords.

`Collection Literal`: In Java, you define a collection using the "new" keyword and the type of the collection. In Groovy, you can use shorthand syntax to define a collection literal, such as "[1, 2, 3]" for a list of integers.

</blockquote>

</details>

---

87. Write a program of map implementation in java?


<details><summary><b> Show Answer </b></summary>

<blockquote>

```Java 

import java.util.HashMap;
import java.util.Map;

public class Main {
    public static void main(String[] args) {
        // create a new HashMap object
        Map<String, Integer> map = new HashMap<>();

        // add key-value pairs to the map
        map.put("apple", 1);
        map.put("banana", 2);
        map.put("orange", 3);

        // get the value for a specific key
        int value = map.get("banana");

        // check if the map contains a specific key
        boolean containsKey = map.containsKey("orange");

        // remove a key-value pair from the map
        map.remove("apple");

        // loop over the key-value pairs in the map
        for (Map.Entry<String, Integer> entry : map.entrySet()) {
            System.out.println("Key: " + entry.getKey() + ", Value: " + entry.getValue());
        }
    }
}

```

In this example, we create a new HashMap object and add key-value pairs to it using the put() method. We can retrieve the value for a specific key using the get() method and check if the map contains a specific key using the containsKey() method. We can remove a key-value pair from the map using the remove() method. Finally, we loop over the key-value pairs in the map using a for-each loop and the entrySet() method.

</blockquote>

</details>

---

88. Write a function in Java having two params n and m that returns an array of multiplications m times of given n

**ex.: myFunction(5, 4) --> returns [5, 10, 15, 20]**

<details><summary><b> Show Answer </b></summary>

<blockquote>

```Java

import java.util.HashMap;
import java.util.Map;
import java.util.*;
import java.io.*;


public class Main {
    public static void main(String[] args) {
       Scanner sc=new Scanner(System.in);
       int n1=sc.nextInt();
       int n2=sc.nextInt();
       System.out.println(Arrays.toString(myFunction(n1,n2)));
    }


public static int[] myFunction(int n, int m) {
    int[] result = new int[m];
    for (int i = 0; i < m; i++) {
        result[i] = n * (i + 1);
    }
    return result;
}
}
```

This function first creates an integer array of length m to store the results. It then uses a loop to iterate m times, multiplying n by the current iteration number (i + 1) and storing the result in the corresponding index of the array. Finally, the function returns the array of results.

</blockquote>

</details>

---

89. How do you go about printing a Map Employee with id numbers as keys and last names as values in java?

<details><summary><b> Show Answer </b></summary>

<blockquote>

```Java

import java.util.HashMap;
import java.util.Map;
import java.util.*;
import java.io.*;


public class Main {
    public static void main(String[] args) {
        Map<Integer, String> employeeMap = new HashMap<>();
        employeeMap.put(1, "Smith");
        employeeMap.put(2, "Johnson");
        employeeMap.put(3, "Williams");
        employeeMap.put(4, "Jones");

        for(Map.Entry<Integer, String> entry : employeeMap.entrySet()) {
                System.out.println("Employee " + entry.getKey() + ": " + entry.getValue());
            }

    }
}


```

In this example, the keys are Integer ID numbers and the values are String last names. The loop iterates over each entry in the map and prints out the key and value for each employee.

</blockquote>

</details>

---

90. Write a Java code for Bubble sort ?

<details><summary><b> Show Answer </b></summary>

<blockquote>

``` Java

public class BubbleSort {
    public static void main(String[] args) {
        int[] arr = { 5, 2, 9, 1, 5, 6 };
        bubbleSort(arr);
        System.out.println(Arrays.toString(arr));
    }
    
    public static void bubbleSort(int[] arr) {
        int n = arr.length;
        for (int i = 0; i < n - 1; i++) {
            for (int j = 0; j < n - i - 1; j++) {
                if (arr[j] > arr[j + 1]) {
                    // swap arr[j] and arr[j+1]
                    int temp = arr[j];
                    arr[j] = arr[j + 1];
                    arr[j + 1] = temp;
                }
            }
        }
    }
}

```
**Output**
`[1,2,5,5,6,9]`

In this example, we have an array of integers arr. We call the bubbleSort function passing in this array as an argument. The function sorts the array using bubble sort, and then we print the sorted array using the Arrays.toString method.

The bubbleSort function uses two nested loops to compare adjacent elements in the array and swap them if they are in the wrong order. The outer loop iterates over the array from the first element to the second-to-last element, while the inner loop iterates over the unsorted part of the array. If the element at index j is greater than the element at index j+1, the two elements are swapped. After the inner loop completes, the largest element in the unsorted part of the array is placed at the end. This process is repeated until the entire array is sorted.

</blockquote>

</details>

---

91. Can you write a Java code for Singleton design pattern ?

<details><summary><b> Show Answer </b></summary>

<blockquote>

```Java

public class Singleton {
    // Private static variable to hold the single instance of the class
    private static Singleton instance;
    
    // Private constructor to prevent creation of new instances
    private Singleton() {}
    
    // Public static method to get the single instance of the class
    public static Singleton getInstance() {
        // If instance is null, create a new instance
        if (instance == null) {
            instance = new Singleton();
        }
        // Return the instance
        return instance;
    }
    
    // Other methods and variables of the class
    public void doSomething() {
        System.out.println("Doing something...");
    }
}

```

In this example, we have a class Singleton with a private constructor and a private static variable instance that holds the single instance of the class. We also have a public static method getInstance() that returns the single instance of the class. The getInstance() method checks if the instance variable is null, and if so, creates a new instance of the class. Otherwise, it simply returns the existing instance.

</blockquote>

</details>

---

92. Write a Java code to reverse the linked list?

<details><summary><b> Show Answer </b></summary>

<blockquote>

```Java

import java.util.HashMap;
import java.util.Map;
import java.util.*;
import java.io.*;


public class Main {
    Node head;
 
    static class Node {
        int data;
        Node next;
 
        Node(int data) {
            this.data = data;
            next = null;
        }
    }
 
    public void reverse() {
        Node current = head;
        Node prev = null;
        Node next = null;
        while (current != null) {
            next = current.next;
            current.next = prev;
            prev = current;
            current = next;
        }
        head = prev;
    }
 
    public void printList() {
        Node node = head;
        while (node != null) {
            System.out.print(node.data + " ");
            node = node.next;
        }
    }
 
    public static void main(String[] args) {
        Main list = new Main();
        list.head = new Node(1);
        list.head.next = new Node(2);
        list.head.next.next = new Node(3);
        list.head.next.next.next = new Node(4);
        System.out.println("Original Linked list");
        list.printList();
        list.reverse();
        System.out.println("");
        System.out.println("Reversed linked list ");
        list.printList();
    }
}

```

This code defines a LinkedList class with a Node inner class. The reverse() method reverses the linked list by iterating through each node and changing its next pointer to point to the previous node. Finally, the head of the linked list is set to the last node, which becomes the new head of the reversed linked list. The printList() method simply prints the values in the linked list. The main() method creates a linked list with four nodes and prints the original and reversed linked lists.

</blockquote>

</details>

---

93. Predict the output of the following?

```Java

public class superclass {
    public void displayResult() {
        system.out.println("Printing from superclass");
    }
}
public class subclass extends superclass {
    public void displayResult() {
        system.out.println("Displaying from subClass");
        super.displayResult();
    }
    public static void main(String args[]) {
        subclass obj = new superclass();
        obj.displayResult();
        superclass obj = new subclass();
        obj.displayResult();
    }
}
```

Can you tell the output of the code?

<details><summary><b> Show Answer </b></summary>

<blockquote>

The code has a syntax error in the main method where the object obj is being declared twice with conflicting types. 

</blockquote>

</details>

---

94. Where are strings stored stack or heap?

<details><summary><b> Show Answer </b></summary>

<blockquote>

In Java, strings are stored in the heap memory. This is because a String object is created dynamically using the new keyword or through string literals, which results in the allocation of memory on the heap. However, string literals that are created at compile-time are stored in a separate area called the String constant pool, which is part of the heap memory.

</blockquote>

</details>

---
