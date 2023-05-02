
1. Do you know about Java 8?

<details> <summary>Show Answer</summary>
 
<blockquote>

Java 8 is a major release of the Java programming language and its development kit (JDK).It introduced several new features and enhancements to the language, including:

**1. Lambda Expressions:** Lambda expressions provide a concise way of representing an anonymous function in Java. They enable the use of functional programming concepts and allow developers to write more concise and readable code.

**2. Streams:** Streams provide a new way of processing collections in Java. They allow developers to easily perform operations such as filtering, mapping, and reducing on collections with a declarative syntax.

**3. Functional Interfaces:** Functional interfaces are interfaces that have exactly one abstract method. They are used in conjunction with lambda expressions to provide a functional programming style in Java.

**4. Default Methods:** Default methods allow interfaces to have implementation code, which makes it easier to evolve interfaces without breaking existing implementations.

**5. Date and Time API:** Java 8 introduced a new Date and Time API, which is more comprehensive and flexible than the old java.util.Date and java.util.Calendar classes.

**6. Method References:** Method references provide a way to refer to a method without invoking it. They are used along with lambda expressions to simplify code.

**7. Optional:** Optional is a new class in Java 8 that represents a value that may or may not be present. It provides a more elegant way of handling null values and helps to avoid NullPointerExceptions.


- These features aim to improve the readability and conciseness of Java code, as well as make it easier to write parallel code and take advantage of multicore processors. Additionally, Java 8 includes various API improvements and performance optimizations.
  
</blockquote>

</details>

---

2. What are optional objects?

<details> <summary>Show Answer</summary>
 
<blockquote>

- In Java, an `Optional` object is a container object that may or may not contain a non-null value. It is a way of representing a value that may or may not exist, without using null references.
- The purpose of `Optional` is to provide a way to explicitly indicate that a value may be absent, and to avoid NullPointerExceptions. It forces the developer to consider the possibility that a value may not be present and to handle that case explicitly, rather than relying on a null check.
- 


  
</blockquote>

</details>

---

3. Sort elements in a String ArrayList. – Alphabetically - By String length

<details> <summary>Show Answer</summary>

<blockquote>

In Java, this can be achieved by using `Collections.sort()` method and Comparator to compare the string lengths.

```java
import java.util.ArrayList;
import java.util.Collections;
import java.util.Comparator;

public class SortArrayList {
    public static void main(String[] args) {
        ArrayList<String> list = new ArrayList<>();
        list.add("banana");
        list.add("apple");
        list.add("orange");
        list.add("kiwi");
        list.add("pear");


        Comparator<String> lengthComparator = new Comparator<String>() {
            @Override
            public int compare(String s1, String s2) {
                return Integer.compare(s1.length(), s2.length());
            }
        };
        Collections.sort(list, lengthComparator);
        Collections.sort(list);

        System.out.println("Sorted alphabatically and by string length: " + list);
    }
}

```

  
</blockquote>

</details>

---

4. What is your experience with Postman?

<details> <summary>Show Answer</summary>
 
<blockquote>

- Postman is a popular tool for API development, testing, and collaboration. It provides a user-friendly interface for making HTTP requests, and it supports a wide range of protocols and data formats, making it a versatile tool for working with APIs.

- Postman allows you to easily create and send requests, set headers and parameters, and view the responses. It also includes features for testing and debugging APIs, such as automatic testing scripts, debugging tools, and performance testing.

- Postman also allows you to collaborate with team members and share API documentation and test results. It integrates with version control systems like Git, allowing you to keep track of changes and collaborate on API development.
  
</blockquote>

</details>

---


5. What are some best practices for creating interfaces?


<details> <summary>Show Answer</summary>
 
<blockquote>

Creating interfaces in Java is a powerful feature that enables you to define a contract for the behavior of classes. Here are some best practices for creating interfaces in Java:

**1. Keep interfaces simple:** An interface should define only the necessary methods required for implementing a specific behavior. Avoid adding methods that are not essential or may be better implemented in a class.

**2. Use clear and concise naming conventions:** Naming conventions should be clear and concise to help other developers understand the purpose of the interface.

**3. Favor composition over inheritance:** Interfaces should be used to define contracts, not to provide implementations. Favor composition over inheritance to achieve a more flexible and maintainable codebase.

**4. Design for extension:** When designing interfaces, keep in mind the possibility of extending the interface in the future. Make sure the interface is designed to be easily extended without breaking existing implementations.

**5. Avoid duplicating code:** Interfaces should not duplicate code that is already defined in other interfaces or classes. Instead, use inheritance to reuse code and avoid code duplication.

**6. Document your interfaces:** Document your interfaces to provide clear and concise information on their intended use and the behavior of the methods defined in the interface.

**7. Use default methods with care:** Default methods were introduced in Java 8 to allow adding new methods to interfaces without breaking existing implementations. However, they should be used with care as they can lead to unexpected behavior and can make the code more complex.

Overall, creating interfaces in Java requires careful planning and consideration. Following these best practices can help ensure that your interfaces are well-designed, easy to use, and flexible for future changes.


</blockquote>

</details>

---

6. What is the difference between local variables and rule inputs?

<details> <summary>Show Answer</summary>
 
<blockquote>
  
- Local variables in Java are declared within a block of code, such as a method or a loop, and are only accessible within that block. They can only be accessed from within the block of code where they are declared and are destroyed once the block of code is exited. Local variables in Java must be declared and initialized before they can be used.

- Rule inputs in Java are typically passed as parameters to a method or function. They are used to provide input or conditions to a set of rules, which then determine the appropriate output or action. Rule inputs in Java are similar to local variables in that they are only accessible within the block of code where they are declared, but they are typically declared as parameters to a method or function, rather than being declared within the method or function itself.

- Both local variables and rule inputs can be of different data types, such as int, float, String, or boolean, and can be used in calculations, comparisons, and other operations. However, their specific use cases and scope differ: local variables are used to store intermediate values within a specific block of code, while rule inputs are used to provide input or conditions to a set of rules or function.

  
</blockquote>

</details>

---

7. Have you used any testing frameworks? Ex. JUnit, Mockito

<details> <summary>Show Answer</summary>
 
<blockquote>
  
Yes, JUnit and Mockito are two commonly used testing frameworks in Java.

**JUnit:**

- It is a testing framework for Java that is used to write and run unit tests. It provides a set of annotations and assertions that allow developers to define and verify the behavior of their code in a systematic way. 
- With JUnit, developers can write test cases that verify the output of methods or the behavior of classes, and can automate the testing process, ensuring that their code is working as expected. 


**Mockito:** 

- It is a mocking framework for Java that is used to create mock objects for testing. 
- It allows developers to simulate the behavior of objects and dependencies, and to write test cases that focus on specific aspects of their code. 
- It provides a simple API for creating and configuring mock objects, and integrates seamlessly with JUnit, making it a popular choice for unit testing in Java. 
- It allows developers to isolate the code under test and test specific scenarios, without having to set up complex dependencies or write redundant test code.

Both JUnit and Mockito are essential tools for Java developers who want to ensure that their code is robust, reliable, and maintainable.

</blockquote>

</details>

---

8. 4 pillars of OOP.

<details> <summary>Show Answer</summary>
 
<blockquote>

The Four Pillars of Object-Oriented Programming are
**1. Abstraction:**

Abstraction is an important concept of object-oriented programming that allows us to hide unnecessary details and only show the needed information.

A practical example of abstraction can be motorbike brakes. We know what brake does. When we apply the brake, the motorbike will stop. However, the working of the brake is kept hidden from us.

The major advantage of hiding the working of the brake is that now the manufacturer can implement brake differently for different motorbikes, however, what brake does will be the same.

<i><b>Abstraction lets you focus on what the object does instead of how it does it.</b></i>

There are two ways to achieve abstraction in java
1. Abstract class (0 to 100% abstraction)
2. Interface (100% abstraction)


**2. Encapsulation:**


Encapsulation is the way of binding the data (variables) and code acting on the data (methods) together as a single unit.  

For example, in a company, they are different sections like the accounts section, finance section, sales section etc. Consider a situation, a person from finance section needs all the data about sales in a particular month. In this case, he is not allowed to directly access the data of sales section. He will first have to contact some other officer in the sales section and then request him to give the particular data. This is what encapsulation is. 

In encapsulation, the variables of a class will be hidden from other classes and can be accessed only through the methods of their current class. Therefore, it is also known as data hiding.

**3. Inheritance:**
Inheritance in OOP is a concept that acquires the properties from one class to other classes: for example, the relationship between father and son. Inheritance in Java is a process of acquiring all the behaviors of a parent object.

The parent-child relationship, also known as the **IS-A** relationship, is represented by inheritance.

**4. Polymorphism:**

- The word poly means many and morphs means forms, so polymorphism means many forms.
- It's an ability of an object to exhibit more than one form

For example: A man at the same time is a father, a husband, an employee. So, the same person possesses different behavior in different situations. This is called polymorphism. 
  
</blockquote>

</details>

---

9. What's the difference between a hashSet and hashMap

<details> <summary>Show Answer</summary>
 
<blockquote>

### HashSet vs HashMap

|                  | HashSet                                                | HashMap                                          |
| ---------------- | ------------------------------------------------------ |--------------------------------------------------
| Data type        | Collection of unique objects                           | Collection of key-value pairs                    |
| Storage          | Hash table                                             | Hash table                                       |
| Duplicates       | Not allowed                                            | Duplicate keys and values are allowed            |
| Retrieval        | Only elements                                          | Value associated with a key                      |
| Null values/keys | Does not allow null elements                           | Allows null values and keys                      |
| Performance      | Constant time for add, remove, and contains operations | Constant time for put, get, and remove operations|
| Order            | Elements are not stored in any particular order        | No order is                                      |
  
</blockquote>

</details>

---

10. What is a singleton?

<details><summary></summary>

<blockquote>

In software design patterns, a singleton is a creational design pattern that ensures only one instance of a class is created in the entire application. This pattern is useful in situations where a single instance of a class must be shared across the entire application, such as a configuration manager or a database connection pool. The singleton pattern helps reduce memory usage and avoid issues related to multiple instances of the same object.

</blockquote>

</details>

11. What is the difference between a singleton and static?

<details><summary></summary>

<blockquote>

- The main difference between a singleton and a static class is that a singleton can be instantiated, whereas a static class cannot. 
- A singleton class is designed to create only one instance of the class, which can be accessed globally. A static class, on the other hand, does not have any instance and its methods and properties can be accessed using the class name itself.
- A singleton can have state, and its instance can be passed around, whereas a static class cannot have any state and its methods are invoked directly using the class name. Therefore, singletons are useful for creating global, stateful objects, while static classes are useful for creating stateless utility classes with no instance methods.

</blockquote>

</details>

12.  How many types of constructors are there?

<details><summary></summary>

<blockquote>

In Java, there are three types of constructors:

**1. Default constructor:** This constructor is provided by Java automatically if no other constructor is defined explicitly. It has no arguments and initializes all instance variables to their default values.

**2. Parameterized constructor:** This constructor takes one or more arguments and initializes the instance variables with the values provided in the constructor call.

**3. Copy constructor:** This constructor is used to create a new object that is a copy of an existing object. It takes an object of the same class as an argument and initializes the new object's instance variables with the values from the existing object.


</blockquote>

</details>

13. How is a private constructor used?

<details><summary></summary>

<blockquote>


</blockquote>

</details>

14. merge two arrays in java


<details><summary></summary>

<blockquote>

In Java, a private constructor is a constructor that is declared with the private access modifier. A private constructor is not accessible outside of the class in which it is defined, which means it cannot be called directly by other classes.

**Private constructors are often used in Java for two main reasons:**

**1. To prevent instantiation:** If a class only contains static methods or fields, it may be designed to be used only as a utility class and should not be instantiated. By making the constructor private, the class cannot be instantiated from outside of the class, which ensures that it is only used as intended.

**2. To control object creation:** By making the constructor private and providing a static factory method, a class can control the creation of its objects. This can be useful when a class needs to perform certain checks or calculations before creating an object, or when it needs to maintain a limited number of instances of the class.

Overall, a private constructor can be used to control the instantiation and creation of objects of a class.

</blockquote>

</details>

15. How would you do check a palindrome with a string builder?

<details><summary></summary>

<blockquote>

To check if a string is a palindrome using StringBuilder, you can follow these steps:

1. Create a StringBuilder object and append the input string to it.
2. Use the reverse() method of the StringBuilder class to reverse the string.
3. Convert the StringBuilder object back to a string using the toString() method.
4. Compare the original input string with the reversed string to check if it is a palindrome.


```java
public static boolean isPalindrome(String input) {
    StringBuilder sb = new StringBuilder(input);
    String reversed = sb.reverse().toString();
    return input.equals(reversed);
}
```

</blockquote>

</details>

16.  how to make hashmap thread safe?


<details><summary></summary>

<blockquote>

**1. Use ConcurrentHashMap:** ConcurrentHashMap is a thread-safe version of HashMap that provides better performance than synchronizing access to a regular HashMap. It uses a technique called lock striping to allow multiple threads to modify the map concurrently without blocking each other.

**2. Synchronize access to the HashMap:** You can use the synchronized keyword to synchronize access to the HashMap. This ensures that only one thread can access the HashMap at a time, which prevents concurrent modifications.


</blockquote>

</details>

17. How do you handle exceptions in java

<details><summary></summary>

<blockquote>

In Java, exceptions are a way to handle errors and unexpected situations that occur during program execution. To handle exceptions in Java, you can use a try-catch block. Here's how it works:

1. The code that might throw an exception is placed inside a try block.
2. If an exception occurs in the try block, the program jumps to the catch block.
3. The catch block contains code that handles the exception. It can print an error message or take other actions to recover from the error.

</blockquote>

</details>


18. Given a sentence with punctuation stored as a string. print the words (case insensitive) that occur more than 1 times. and their occurrence.

<details><summary></summary>

<blockquote>

To print the words that occur more than once in a sentence and their occurrence, you can use a HashMap to store the words and their frequency. Here's an example implementation in Java:

```java
import java.util.HashMap;
import java.util.Map;

public class WordCounter {
    
    public static void printWordFrequency(String sentence) {
        String[] words = sentence.split("\\W+"); // Split sentence by non-word characters

        Map<String, Integer> wordFreq = new HashMap<>();
        for (String word : words) {
            word = word.toLowerCase(); // Convert to lowercase to ignore case
            if (wordFreq.containsKey(word)) {
                wordFreq.put(word, wordFreq.get(word) + 1); // Increment frequency if word already in map
            } else {
                wordFreq.put(word, 1); // Add word to map with frequency 1
            }
        }

        // Print words that occur more than once
        for (Map.Entry<String, Integer> entry : wordFreq.entrySet()) {
            if (entry.getValue() > 1) {
                System.out.println(entry.getKey() + " occurs " + entry.getValue() + " times.");
            }
        }
    }

}

```

- In this example, we define a WordCounter class with a static method printWordFrequency() that takes a sentence as a parameter. The method works the same way as the previous example, using a HashMap to count the frequency of each word and then printing the words that occur more than once.

</blockquote>

</details>

19. what do you know about collection?

<details><summary></summary>

<blockquote>


</blockquote>

</details>


20. what is the process to create servlet api in spring; 

<details><summary></summary>

<blockquote>

In Java, a collection is a group of objects that can be stored, manipulated, and iterated together. The Java Collection Framework is a set of classes and interfaces that provide implementations of different types of collections.

Some common types of collections in Java include:

- **List:** an ordered collection of elements that allows duplicates and can be accessed by index.
Set: an unordered collection of unique elements.
- **Map:** a collection of key-value pairs, where each key is unique and maps to a value.
- **Queue:** a collection that orders elements in a first-in, first-out (FIFO) manner.


Each type of collection has its own methods and behavior, but they all share common methods and interfaces defined by the Collection Framework. For example, all collections implement the Iterable interface, which allows them to be iterated over using a for-each loop.

The Collection Framework also provides algorithms for searching, sorting, and manipulating collections, as well as utility classes for working with collections, such as Collections and Arrays.

Overall, collections are an important part of the Java language and provide a flexible and efficient way to work with groups of objects.

</blockquote>

</details>

21. Tell me about how you implement an interface?

<details><summary></summary>

<blockquote>

To implement an interface in an object-oriented programming language like Java, you need to declare the interface with its methods, create a class that implements the interface, override the methods defined in the interface in the implementing class, and then instantiate the implementing class to use its methods.


</blockquote>

</details>

22. What kind of method does a class need to be created

<details><summary></summary>

<blockquote>

To create a class in Java, you need to define at least a constructor method to initialize the object when it is created. Additionally, the class may require other methods such as getters and setters to set and retrieve the values of the object's properties, as well as other methods that perform operations on the object's data. The specific methods needed will depend on the requirements of the application or system being developed.

</blockquote>

</details>

23. Tell me 2 methods of changing a method (polymorphism)?

<details><summary></summary>

<blockquote>

The two methods for method chaining are:

1. Method overloading: Calling a method from other method of the same class.
2. Method Overriding: Calling a method of a class from a method of a class that extends the class.

</blockquote>

</details>


24. Do you know the purpose of logging?, Lets say there is an issue where no trades are going through. How would you go about searching the log for the issue?

<details><summary></summary>

<blockquote>

Logging is the practice of generating log messages during the execution of a program. 
- The purpose of logging isto recording important events and information about the program's behavior. Logging is a key tool for troubleshooting issues in software applications, as it can provide valuable insight into what happened leading up to an error or unexpected behavior.

In the case of an issue where no trades are going through, one approach to searching the logs for the issue would be to look for log messages related to trade processing. This could involve searching for log messages related to the trade processing workflow, such as messages indicating that a trade was received, processed, and sent to a third-party system. Additionally, it might be useful to look for error messages or exceptions that occurred during the trade processing workflow, as these can provide clues about what went wrong.


</blockquote>

</details>

25.  Why would you use a String Builder vs a String? 

<details><summary></summary>

<blockquote>

You should use StringBuilder instead of String when you need to concatenate a large number of strings or when performance is a concern, because StringBuilder is a mutable class that allows for efficient concatenation of multiple strings without creating new objects in memory.

</blockquote>

</details>

26. What is the JVM, JRE, and JDK?

<details><summary></summary>

**JDK:** JDK (Java Development Kit) is a software development kit that includes the JRE, as well as tools and libraries for developing and compiling Java applications. It provides everything needed to write, compile, and run Java code.

**JRE:** JRE (Java Runtime Environment) is a software package that includes the JVM, along with libraries and other components required for running Java applications.

**JVM:** JVM (Java Virtual Machine) is the runtime environment for Java applications, providing a layer of abstraction between the Java code and the underlying hardware and operating system.

<blockquote>


</blockquote>

</details>

27. What is a singleton class in java and how would you make one?


<details><summary></summary>

<blockquote>

In Java, a singleton class is a class that allows only one instance of itself to be created and provides a global point of access to that instance.


To create a singleton class in Java, you can follow these steps:

1. Declare the class as final to prevent it from being extended.
2. Declare a private constructor to prevent the class from being instantiated from outside the class.
3. Declare a private static variable of the same type as the class, which will hold the single instance of the class.
4. Declare a public static method that returns the single instance of the class. This method should create the instance if it doesn't already exist, and return the existing instance if it does.


```java
public final class MySingletonClass {
    private static MySingletonClass instance = null;
    private MySingletonClass() {
    }
    public static MySingletonClass getInstance() {
        if (instance == null) {
            instance = new MySingletonClass();
        }
        return instance;
    }
}

```


</blockquote>

</details>


28. What is the difference between a hash map and hash table?

<details><summary></summary>

<blockquote>

| Feature          | HashMap                     | HashTable                          |
| ---------------- | --------------------------- | ---------------------------------- |
| Synchronization  | Not synchronized            | Synchronized                       |
| Thread-safety    | Not thread-safe             | Thread-safe                        |
| Null keys/values | Allows null keys and values | Does not allow null keys or values |
| Iterator         | Fail-fast iterator          | Enumeration (legacy)               |
| Performance      | Faster than HashTable       | Slower than HashMap                |


</blockquote>

</details>



<details><summary></summary>

<blockquote>


</blockquote>

</details>



<details><summary></summary>

<blockquote>


</blockquote>

</details>



<details><summary></summary>

<blockquote>


</blockquote>

</details>



<details><summary></summary>

<blockquote>


</blockquote>

</details>



<details><summary></summary>

<blockquote>


</blockquote>

</details>



<details><summary></summary>

<blockquote>


</blockquote>

</details>



<details><summary></summary>

<blockquote>


</blockquote>

</details>


