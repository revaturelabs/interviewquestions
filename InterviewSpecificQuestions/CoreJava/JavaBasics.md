## Technical

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


22. What is immutable in Java?

<details><summary> Show Answer </summary>

<blockquote>

In Java, an immutable object is an object whose state cannot be changed once it is created. Once the object is created, any attempt to modify its state will result in the creation of a new object with the modified state. Immutable objects are thread-safe and can be shared without the risk of concurrent modification. Examples of immutable classes in Java include String, Integer, and BigDecimal.

</blockquote>

</details>

---

23. Can you tell us something on mutable and immutable class in Java? 

<details><summary> Show Answer </summary>

<blockquote>

In Java, a mutable class is a class whose objects can be modified after creation, while an immutable class is a class whose objects cannot be modified after creation. In a mutable class, the state of the object can be changed by invoking methods or modifying fields, whereas in an immutable class, the state of the object is fixed and cannot be changed.

An example of a mutable class in Java is the StringBuilder class, which allows the modification of the string content by appending, deleting, or replacing characters. On the other hand, an example of an immutable class in Java is the String class, whose objects cannot be modified once created, and any operation on the string creates a new string object.

</blockquote>

</details>

---

24. What is the difference between extends and implements in Java? 

<details><summary> Show Answer </summary>

<blockquote>

In Java, `extends` and `implements` are both keywords used for inheritance, but they have different meanings.

`extends` is used to create a subclass that inherits properties and methods from a parent class. The subclass can add or override properties and methods of the parent class.

`implements` is used to make a class implement an interface. An interface is a collection of abstract methods that a class must implement. When a class implements an interface, it agrees to provide the implementations for all the methods defined in the interface.

</blockquote>

</details>

---

25. What is the use of getter and setter in java?

<details><summary> Show Answer </summary>

<blockquote>

In Java, getters and setters are methods used to access and modify the values of private fields in a class.

A getter method retrieves the value of a private field and returns it to the caller. This allows other classes to access the private field without exposing the implementation details of the class.

A setter method sets the value of a private field based on the value passed to it as a parameter. This allows other classes to modify the value of the private field without exposing the implementation details of the class.

</blockquote>

</details>

---

26. How does the Java ternary operator works?

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

27. How do you write for a phone number using regex in Java?

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

28. Do you know about Java Messaging Service in Java?

<details><summary> Show Answer </summary>

<blockquote>

Yes, Java Messaging Service (JMS) is a Java-based messaging standard that allows distributed applications to communicate with each other. It is a message-oriented middleware API that allows Java applications to send and receive messages asynchronously.

JMS provides a common way for applications to create, send, receive, and read messages. It defines a set of standard interfaces and protocols that enable seamless communication between different messaging systems, such as IBM MQ, Apache ActiveMQ, and RabbitMQ.

</blockquote>

</details>

---

29. How does JNDI works?

<details><summary> Show Answer </summary>

<blockquote>

JNDI stands for Java Naming and Directory Interface, and it is a standard interface to access naming and directory services in Java. It provides a common interface for accessing naming and directory services, regardless of the underlying technology used by the service.

In JNDI, you can bind objects to names in a hierarchical namespace, which can be accessed by clients using a standard API. This allows you to separate the location of objects from the code that uses them, making it easier to manage and maintain distributed systems.

</blockquote>

</details>

---

30. How do you differentiate groovy from java using syntax?


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

31. Write a program of map implementation in java?


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

32. Write a function in Java having two params n and m that returns an array of multiplications m times of given n

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

33. How do you go about printing a Map Employee with id numbers as keys and last names as values in java?

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

34. Write a Java code for Bubble sort ?

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

35. Can you write a Java code for Singleton design pattern ?

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

36. Write a Java code to reverse the linked list?

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

37. Predict the output of the following?

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

38. Where are strings stored stack or heap?

<details><summary><b> Show Answer </b></summary>

<blockquote>

In Java, strings are stored in the heap memory. This is because a String object is created dynamically using the new keyword or through string literals, which results in the allocation of memory on the heap. However, string literals that are created at compile-time are stored in a separate area called the String constant pool, which is part of the heap memory.

</blockquote>

</details>

---
