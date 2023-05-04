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


22. Why do we use public and private access modifiers.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The access modifiers are used to control the visibility and accessibility of class members such as variables, methods, and inner classes.

When a class, method, or variable is declared as `public`, it can be accessed from any other part of the program. For example, if a method is declared as `public`, it can be called from any other class in the program. When a class, method, or variable is declared as `private`, it can only be accessed within the same class. This is useful when we want to restrict access to certain classes or methods to only the class in which they are declared. 

</blockquote>

</details>

---

23. Object class methods

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


24. super class of all java classes. 

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

26. What are the control statements.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Control statements in Java are used to control the flow of execution in a program. They include conditional statements like if-else and switch-case, and iterative statements like for, while, and do-while. These statements are essential for programming logic and enable the developer to control the sequence of execution.

</blockquote>

</details>

---

27. When would you use the final keyword?

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

28. What is `finalize`?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

`finalize` is a method provided by the `Object` class in Java that is called by the garbage collector when an object is about to be destroyed. Its purpose is to perform any necessary cleanup operations before the object is destroyed, such as releasing resources like file handles, database connections, or network sockets.

</blockquote>

</details>
---

29. What is the difference between `final`, `finally`, and `finalize`, and what situations are they used in?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

`final` is a keyword used to create constants or immutable variables, `finally` is a block used to define a code section that will be executed after a try/catch block, regardless of whether an exception is thrown or not, and `finalize` is a method called by the garbage collector when an object is about to be destroyed, used for resource cleanup.

</blockquote>

</details>


--- 

30. Can the garbage collector be manually called?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The garbage collector in Java is automatically called by the JVM, and it cannot be manually called by the programmer. The garbage collector runs periodically in the background, and its behavior is influenced by various factors such as the heap size, the amount of available memory, and the type of garbage collector being used. The garbage collector is responsible for freeing up memory used by objects that are no longer referenced by any part of the program.

</blockquote>

</details>

--- 

31. What are the levels of garbage collection?

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

32. How does an object progress through those garbage collection levels?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

In Java, when a new object is created, it is initially allocated in the young generation. The young generation is divided into two spaces: an `eden` space and a `survivor` space. When the `eden` space becomes full, a minor garbage collection is triggered, and any objects that are still referenced are moved to the `survivor` space. If an object survives multiple minor garbage collections, it is promoted to the old generation.

Objects in the old generation are subject to major garbage collections, which run less frequently than minor garbage collections. The goal of a major garbage collection is to free up space in the old generation by identifying and removing objects that are no longer referenced. If an object survives a major garbage collection, it remains in the old generation until it is no longer referenced or until the program terminates.

</blockquote>

</details>

--- 

33. How does garbage collection work? 

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Garbage collection is used in Java to perform automatic memory management. It deletes the objects in memory that are no longer being used by the program, and freeup the space in memory. When an object is created, Java keeps track of its reference count. When an object is no longer referenced by the program, its reference count is reduced to zero, and it becomes eligible for garbage collection. The garbage collector periodically scan the heap for objects that have a reference count of zero and delete them. It helps prevent memory leaks and makes programming in Java more convenient and safe.

</blockquote>

</details>

---

34. How do you copy an array?

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

35. Write an array and give some values, then print them. What are different array methods you have used?

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

36. Given an array, create a list of pairs of indexes that sum to a target value.

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

37. Are you able to store integers in an array?

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