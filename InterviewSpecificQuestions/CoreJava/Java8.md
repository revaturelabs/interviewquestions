## Technical
1. In Java 8 how can I filter a collection using the stream?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

```Java
    public static void main(String[] args)
    {
        // Creating a list of Integers
        List<Integer> list = Arrays.asList(3, 4, 6, 12, 20);
        // Getting a stream consisting of the
        // elements that are divisible by 5
        // Using Stream filter(Predicate predicate)
        list.stream()
            .filter(num -> num % 5 == 0)
            .forEach(System.out::println);
    }
```
</blockquote>

**Output**<br>
    
    20
    
<details> <summary> <b> Explanation </b> </summary>

<blockquote>
    
- It provides a method `filter ()` to filter stream elements on the basis of given predicate. 
- This method take predicate as an argument and returns a stream of consisting of resulted elements.
    
</blockquote>

</details>
    
</details>

---

2. Can we define default method without using default keyword in Java8?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
    
<blockquote>

- No, for defining default method inside interface `default` keyword is must and it should prefix method declaration.
- Without prefixing default keyword results in compilation error.
- **Compile-time error**: Abstract methods do not specify a body.
- **Reason**: without default keyword, compiler consider it as abstract method which doesn’t have body.

</blockquote>
    
</details>

---

3. What actual advantage does Java 8 brings?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Code is more concise and readable.
- More reusable,testable and maintable.
- User can write parallel code.
- User can write database like operations.
</blockquote>
</details>

---

4. Explain us about Functional interfaces.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

An Interface that contains exactly one abstract method is known as functional interface. It can have any number of defaults, static methods but can contain only one abstract method. It can also declare methods of object class. Functional Interface is also known as Single Abstract Method Interfaces or SAM Interfaces.
    
</blockquote>
</details>

---


5. How lambda expressions and functional interface are related?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Lambda expressions express instances of functional interfaces (An interface with single abstract method is called functional interface. An example is `java.lang.Runnable`). 
- Lambda expressions implement the only abstract function and therefore implement functional interfaces

</blockquote>
</details>

---

6. What is your understanding about stream pipelining?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

It is the process of chaining different operations together. It accomplishes this function by dividing stream operations into two categories, intermediate operation, and terminal operations.

</blockquote>
</details>

---

7. Can you create your own functional interface?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Yes, we can create our own functional interface.
- We must do these two things:
    - Annotate the interface with `@FunctionalInterface`, which is the Java 8 convention for custom functional interfaces.
    - Ensure that the interface has just one abstract method.

</blockquote>
</details>

---

8. What will happen if we define multiple abstract methods inside the Functional interface?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Inside Functional Interface we can take only one abstract method, if we take more than one abstract method then compiler raise an error. Interface can declares an abstract method overriding one of the public method from `java.lang.Object`, that still can be considered as functional interface.

</blockquote>
</details>

---

9. Why default methods needed in the interface?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

 Java 8 has introduced the concept of default methods which allow the interfaces to have methods with implementation without affecting the classes that implement the interface.

</blockquote>
</details>

---

10. What is the behavior of `findFirst()` method in Java 8  streams?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Stream `findFirst()` returns an Optional (a container object which may or may not contain a non-null value) describing the first element of this stream, or an empty Optional if the stream is empty.

</blockquote>

<details> <summary> <b> Explanation </b> </summary>
<blockquote>

```Java
    import java.util.stream.Stream;
    public class Main 
    {
        public static void main(String[] args) 
        {
            //sequential stream
            Stream.of("one", "two", "three", "four")
            .findFirst()
            .ifPresent(System.out::println);
            //parallel stream
            Stream.of("one", "two", "three", "four")
            .parallel()
            .findFirst()
            .ifPresent(System.out::println);
        }
    }
```

**Output**

one<br>
one

</blockquote>
</details>
</details>

---

11. What is the behavior of `findAny()` method in Java 8  streams?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Stream `findAny()` returns an Optional (a container object which may or may not contain a non-null value) describing some element of the stream, or an empty Optional if the stream is empty.
</blockquote>
</details>

---

12. When to use `findAny()` method in Java 8 streams?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

There are instances where you have a stream, but you only want to select a random element as long as it meets certain conditions and the operation itself takes the shortest time possible.

</blockquote>
</details>

---

13. What do you mean by stream?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Streams are just sequence of data from a source.
- With Java 8, we can do manipulation on data using stream API.
- Example: Youtube
    - If we are watching a video all the content of the video will not be loaded at once. As the time elapses, we will get the content.

</blockquote>
</details>

---

14. Can you tell me difference between Collection API and Stream API?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Collection API is used for storing data in different kinds of data structures.
- Stream API is used for computation of data on a large set of objects.
- With Collection API we can store a finite number of elements in a data structure.
- With Stream API, we can handle streams of data that can contain infinite number of elements.
- Collection API constructs objects in an eager manner.
- Stream API creates objects in a lazy manner.
- Multiple consumption: Most of the Collection APIs support iteration and consumption of elements multiple times.
- With Stream API we can consume or iterate elements only once.

</blockquote>
</details>

---

15. Do you know what are the various forms of writing lambda expressions?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>
We can declare a lambda expression by-
    
- () -> expression
- (parameters) -> expression
- (parameters) -> { multiple statements}

</blockquote>
</details>

---

16. What do you understand by `@Functional Interface` annotation in Java 8?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- `@Functional interface `- used to force the compiler to check whether the given interface has single-abstract method or not.
- If not, compiler will throw error `"Unexpected @FunctionalInterface annotation"`

</blockquote>
</details>

---

17. How do you create a custom annotation in Java?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

```Java
import java.lang.annotation.Retention;
import java.lang.annotation.RetentionPolicy;
@Retention(RetentionPolicy.RUNTIME)
@interface TestAnnotationForClass {
   String author();
   String date();
   int currentRevision() default 1;
   String lastModified() default "Not applicable";
   String lastModifiedBy() default "Not applicable";
}

//Now, we’ll use TestAnnotationForClass annotation for Test class.

   @TestAnnotationForClass (
   author = "Editorial Team",
   date = "9/18/2020",
   currentRevision = 6,
   lastModified = "9/18/2020",
   lastModifiedBy = "Editorial Team"
    )
    public class Test {
        public static void main(String[] args) {
        Test t = new Test();
        //print annotations of class Test
        System.out.println(t.getClass().getAnnotations()[0]);
        }
    }
```

</blockquote>

<details> <summary> <b> Explanation </b> </summary>
<blockquote>

In this example, we have used RetentionPolicy.RUNTIME because we want to demonstrate and read annotation at runtime. RetentionPolicy.RUNTIME indicates that annotations are to be recorded in the class file by the compiler and retained by the virtual machine at run time, so they may be read reflectively.

**Output**

@TestAnnotationForClass(currentRevision=6, lastModified=9/18/2020, lastModifiedBy=Editorial Team, author=Editorial Team, date=9/18/2020)

</blockquote>
</details>
</details>

---

18. How to avoid  `NullPointer exception ` in Java 8?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Java 8 provides concept of Optional
- Optional can be used to avoid `NullPointer Exception`

Example:

    ```Java
    String value=null;<br>
    Optional <String> value=Optional.empty();
    ```
</blockquote>
</details>

---

19. What are the different types of functional interfaces in Java 8?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Consumer
- Predicate
- Function 
- Supplier

</blockquote>
</details>

---

20. How would you convert object of type Iterable to Stream?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Let’s have an example:
```Java
import java.util.*;
import java.util.stream.*;
class Main{
    // Function to get the Stream
    public static <T> Stream<T>
    getStreamFromIterable(Iterable<T> iterable)
    {
        // Convert the Iterable to Spliterator
        Spliterator<T>
            spliterator = iterable.spliterator();
        // Get a Sequential Stream from spliterator
        return StreamSupport.stream(spliterator, false);
    }
    public static void main(String[] args)
    {
        // Get the Iterator
        Iterable<Integer>
            iterable = Arrays.asList(10,20,30,40,50);
        // Get the Stream from the Iterable
        Stream<Integer>
            stream = getStreamFromIterable(iterable);
        // Print the elements of stream
        stream.forEach(s -> System.out.println(s));
    }
}
// Output:
// 10
// 20
// 30
// 40
// 50
```


</blockquote>
</details>

---

21.  How to overcome, multiple inheritance problem in Java 8?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>
    
we can do that by overriding the default method in the implementation class. Altogether provide new implementation or invoke either one of the `default()` method using `super` keyword
For example, `\<interfaceName\>.super.\<defaultMethodName\>`

</blockquote>
</details>

---

22. What happens, if a class implements two interfaces having exactly same method with same signature (consider one as default and another abstract)?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Compilation fails with error saying conflicting method.
- **Compile-time error**: The default method `displayDefaultMethod()` inherited from DemoInterfaceA conflicts with another method inherited from DemoInterfaceB
- To overcome this error, override this conflicting method and provide new implementation or invoke default method’s implementation using `super` keyword

</blockquote>
</details>

---


23. What is the purpose of `joining ()` method introduced in Java 8 ?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The `joining ()` method of the Collectors class in Java 8 returns a Collector that concatenates the input elements into a String.
    
``` java
    public class Example {
        public static void main (String[] args) {
            List<Character> list = Arrays.asList('D', 'e', 'm', 'o');
            String str = list. stream().map(String::valueOf).collect(Collectors.joining());
            System.out.println("Concatenated = "+str);
        }
    }
```

**Output**

Concatenated = Demo

</blockquote>
</details>

---

24. What is the use of the `String::Value of` expression in Java 8?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

`String::ValueOf` is a simple static method referencing the `valueOf` method, belonging to the class 
`String`.

</blockquote>
</details>

---

25. What do you mean by method reference in Java 8?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

It refers to methods of functional interfaces. It can be considered as a short-code version of using a lambda expression.

The following is the expression for a method reference:

    `Class::methodname`

</blockquote>
</details>

---

26. What is the easiest way to print the current date and time using the new APIs in Java 8?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The `now` method, which is a part of `LocalDate`, can be used to get the current date as shown below:

    ```Java
    LocalDate currentDate = LocalDate.now();
    System.out.println(currentDate);
    ```

Similarly, it can also be used to get the current time:

    ```Java
    LocalTime currentTime = LocalTime.now();
    System.out.println(currentTime);
    ```

</blockquote>
</details>

---

27. Differentiate between intermediate and terminal operations in Java 8.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

**Intermediate Operation**

- Used for the transition to a new state.	
- Lazy execution of code, i.e., code is not executed as soon as it is encountered Not lazy.

**Terminal Operation**

- Used to end the process under execution.
- Code is immediately executed upon encounter.

</blockquote>
</details>

---
28. Can the following piece of code compile successfully?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<blockquote>

```Java
@FunctionalInterface
public interface Function2<T, U, V> {
public V apply(T t, U u);
default void count() {
    // increment counter
}
}
```

</blockquote>

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Yes, the code can compile and execute without any errors. It uses functional interface specifications when the single abstract method is being defined.

</blockquote>
</details>

---

29. What is the code to sort strings using the Java 8 lambda expression?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The below piece of code sorts of strings using the lambda expression:

//Sorting using Java 8 lambda expression

```Java
private void sortUsingJava8(List<String> names) {

Collections.sort(names, (s1, s2) -> s1.compareTo(s2));

}
```

</blockquote>
</details>

---

30. Is it possible to call a static method of any interface in a class using Java 8?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Yes, it is possible to call a static method in a class by making use of the name as shown below:

```Java
    interface Student {
        static void Present() {
        System.out.println("Student is there!");
        }
    }

    class Associates implements Student {
        public void print() {
            Student.Present();
        }
    }
```

</blockquote>
</details>

---

31. Do you know how the `random` keyword in Java 8 works?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The `random` keyword, as the name suggests, is used to generate random values for computations and operations in Java 8.

The following piece of code is used to print out 20 random numbers using the for each loop:

```java

Random random = new Random();
random.ints().limit(20).forEach(System.out::println);

```
</blockquote>
</details>

---

32. Explain about collectors in Java 8?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Collectors are mainly used to combine the result after the processing of elements in a stream. They are used to return lists or strings.

</blockquote>
</details>

---

33. What is the easiest way to print the sum of all the numbers present in a list using Java 8?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

In Java 8, the following code is used to print the sum of all of the numbers that are present in a list:

```Java
    List<Integer> numbers = Arrays.asList(5, 4, 10, 12, 87, 33, 75);
    IntSummaryStatistics stats = integers.stream().mapToInt((x) −> x).summaryStatistics();
    System.out.println("Sum of all numbers : " + stats.getSum());
```

</blockquote>
</details>

---

34. When is an ideal situation to use the Stream API in Java 8?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The Stream API in Java 8 can be effectively used if the Java project calls for the following operations:

    - Perform database operations
    - Execute operations lazily
    - Write functional-style programming
    - Perform parallel processing
    - Use pipeline operations
    - Use internal iteration

</blockquote>
</details>

---

35. Can you tell me about supplier in Java 8?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

A supplier is a simple functional interface in Java 8 that does not take in any argument. It is used as an assignment target when making use of lambda expressions.

</blockquote>
</details>

---

36. Do you know about predicate in Java 8 ?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- The Predicate is also a functional interface in Java and it is defined in the java.util.function package.
- It improves the readability and manageability of our code. Also, it helps us in unit testing them separately.
- We can use Predicate anywhere where we need to evaluate a condition on a Collection of objects such that evaluation can result either in true or false.
</blockquote>
</details>

---

37. Can you name the common types of functional interfaces in the standard library?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

There are many functional interface types in the standard library, and some of them are as follows:

- BiFuction
- BinaryOperator
- Consumer
- Predicate
- Supplier
- UnaryOperator

</blockquote>
</details>

---

38. Can you give examples of intermediate operations in Java 8?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The examples that are widely used in intermediate operations are:

- `Distinct()`
- `Limit(long n)`
- `Filter(Predicate)`
- `Map(Function)`
- `skip(long n)`

</blockquote>
</details>

---

39. What are the similarities between `map` and `flatMap` stream operations in Java 8?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Both `map` and `flatMap` operations are a form of intermediate stream operations that take in a function and use the input function for performing various activities in the stream.

</blockquote>
</details>

---

40.How to find and remove duplicate elements from a list using Java 8?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Duplicate elements can be listed and removed easily by applying stream operations and performing a collection, later using the `Collections.toSet()` method. This should remove all the duplicate elements present in the list.

</blockquote>
</details>

---

41. What is the easiest way to convert an array into a stream in Java 8?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Any array in Java 8 can be converted into a stream easily using the stream class. The creation of a stream using a factory method is as shown below:

```Java
    String[] testarray = {"Hello", "Intellipaat", "learners"};
    Stream numbers = Stream.of(testarray);
    numbers.forEach(System.out::println);
```
</blockquote>
</details>

---

42. What is the use of the `peek()` method in Java 8?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The `peek()` method is a part of the stream class in Java 8, which is used to see actions performed through a stream pipeline. Peeking can be done at every step to print messages about the code being executed onto the console.

Peeking has a wide amount of usage when efficiency is a requirement, when debugging code with the lambda expression, or when performing stream processing.

</blockquote>
</details>

---

43.  What is the meaning of a `Spliterator` in Java 8?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Spliterator is a newly introduced iterator interface for Java 8. It is very efficient and handles API-related operations seamlessly across the runtime environment.

</blockquote>
</details>

---

44. Explain the different time and date APIs and when you may use them.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Important classes of Date-Time API are:
    - Local: It is used to simplify the date-time API with no complexity of timezone handling.
    - Zonal: It is a specialized date-time API to deal with various timezones.

- Java LocalDate Time Class:
    - It is an immutable date-time object that represents a date-time, with the default format as yyyy-MM-dd-HH-mm-ss.zzz. It is used when time zones are NOT required.

- ZonedDate Time Class in Java:
    - It is an immutable representation of a date-time with a time-zone. Use it when time zones are to be considered. It is used to store all date and time fields.
    
</blockquote>
</details>

---

45. In Java, how do you convert a String to a LocalDate or a LocalDateTime? ?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>
The Java 8 `LocalDate-Time API` includes a `parse()` method, which can be used to parse a given input string using a specified format.

For example,

```java

LocalDate newDate = LocalDate.parse("2016-08-23");
System.out.println("Parsed date : " + newDate);

```
</blockquote>
</details>

---

46. What is the difference between a predicate and a function?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- A predicate takes one argument and returns a boolean value.
- A function takes one argument and returns an object.
- Both are useful for evaluating lambda expressions.

</blockquote>
</details>

---

47. Can a functional interface extend/inherit another interface?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

A functional interface cannot extend another interface with abstract methods as it will void the rule of one abstract method per functional interface. 

Example:

```Java
    interface Parent { 
        public int parentMethod(); 
    } 
    @FunctionalInterface // This cannot be FunctionalInterface 
    interface Child extends Parent { 
        public int childMethod(); 
            // It will also extend the abstract method of the Parent Interface 
            // Hence it will have more than one abstract method 
            // And will give a compiler error 
        }
```
It can extend other interfaces which do not have any abstract method and only have the default, static, another class is overridden, and normal methods.

</blockquote>
</details>

---

48. What are the advantages of using the Optional class?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

It encapsulates optional values, i.e., null or not-null values, which helps in avoiding null checks, which results in better, readable, and robust code It acts as a wrapper around the object and returns an object instead of a value, which can be used to avoid run-time NullPointerExceptions.

</blockquote>
</details>

---
49. What are lambda expressions or lambda functions

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Lambda expressions are a feature introduced in Java 8 that allow you to write anonymous functions in a more concise and expressive way.

A lambda expression is a short block of code that represents a function, which can be passed around and executed as if it were an object. The syntax for a lambda expression is as follows:
```code
(parameter_list) -> { expression }
```
It consists of a parameter list, an arrow token (->), and a body that can be an expression or a block of statements. 
Here, parameter_list is a comma-separated list of the function's parameters (if any), and expression is the code that performs the function's computation.

For example, here is a lambda expression that takes two integers and returns their sum:
```java
(int a, int b) -> { return a + b; }
```
Lambda expressions can also be used in functional interfaces, which are interfaces that define exactly one abstract method. A lambda expression can be used to provide an implementation for the abstract method of a functional interface, allowing the interface to be used like a regular Java method.

</blockquote>
</details>

---
50. How would you define a lambda function

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

In Java, a lambda function (also known as a lambda expression) is defined using the following syntax:
```code
(parameter_list) -> { expression }
```
It consists of a parameter list, an arrow token (->), and a body that can be an expression or a block of statements. 
Here, parameter_list is a comma-separated list of the function's parameters (if any), and expression is the code that performs the function's computation.

For example, the following lambda function takes two integers and returns their sum:
```java
(int a, int b) -> { return a + b; }
```
In this case, the parameter_list consists of two integers (int a and int b), and the expression simply adds them together and returns the result.

Lambda functions can also have no parameters, as in this example:
```java
() -> { System.out.println("Hello, world!"); }
```
In this case, the lambda function takes no parameters and simply prints the message "Hello, world!" to the console.

Lambda functions can be used in a variety of contexts in Java, including with collections, streams, and functional interfaces. They are a powerful and flexible tool for writing functional-style code in Java.

</blockquote>
</details>

---
51. Why do you use lambdas?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Lambdas in Java are used for writing more concise and expressive code, especially when working with functional programming constructs like streams and collections. They provide a way to represent a function as an object, which can then be passed around and used like any other object.

Some of the benefits of using lambdas in Java are as follows:

Conciseness: Lambdas allow you to write shorter and more concise code, which can be easier to read and maintain.

Expressiveness: Lambdas allow you to express complex operations in a more natural and intuitive way, making the code easier to understand.

Flexibility: Lambdas can be used in a wide range of contexts, including with collections, streams, and functional interfaces, making them a versatile tool for writing functional-style code in Java.

Composability: Lambdas can be combined and composed in various ways to create more complex operations, making it easier to build up complex algorithms from simpler building blocks.

Overall, lambdas in Java are a powerful and flexible feature that enable more expressive and functional-style programming, making it easier to write efficient, readable, and maintainable code.

</blockquote>
</details>

---
52. What is the purpose of lambdas and Streams API? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The purpose of lambdas and the Streams API in Java is to provide a more concise and expressive way to work with collections and perform operations on them in a functional style.

Lambdas provide a way to represent a function as an object, which can be passed around and used like any other object. This allows you to write more concise and expressive code, especially when working with functional programming constructs like streams and collections.

The Streams API provides a set of high-level operations that can be used to perform common data processing tasks, such as filtering, sorting, mapping, and reducing, on collections of data. The API is designed to be used with lambdas, allowing you to write code that is both concise and expressive.

Together, lambdas and the Streams API provide a powerful and flexible way to work with collections and perform complex data processing tasks with minimal boilerplate code. They are especially useful for working with large datasets and performing complex data transformations and analysis.

</blockquote>
</details>

---
53. What are optional objects? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- In Java, an `Optional` object is a container object that may or may not contain a non-null value. It is a way of representing a value that may or may not exist, without using null references.
- The purpose of `Optional` is to provide a way to explicitly indicate that a value may be absent, and to avoid NullPointerExceptions. It forces the developer to consider the possibility that a value may not be present and to handle that case explicitly, rather than relying on a null check.


</blockquote>
</details>

---

54. What are Projections in Java? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

In Java, projections can be performed using the Streams API, which provides a set of operations for processing collections of data.

In the Streams API, a projection operation is typically performed using the map() method, which takes a lambda expression as an argument and applies it to each element in the stream. The lambda expression defines the transformation to be applied to each element, and the result is a new stream that contains the transformed elements.

Here's an example of how to perform a projection using the Streams API:
```java
List<String> names = Arrays.asList("John", "Mary", "Bob", "Jane");

List<Integer> nameLengths = names.stream()
                                  .map(name -> name.length())
                                  .collect(Collectors.toList());
```
In this example, we have a list of names, and we want to create a new list containing the length of each name. We use the stream() method to create a stream from the list, then use the map() method to apply a lambda expression that computes the length of each name. Finally, we use the collect() method to collect the transformed elements into a new list.

Projections are a powerful tool for working with collections of data, allowing you to extract and transform specific subsets of data in a concise and expressive way.


</blockquote>
</details>

---
55. Use Java Streams to sort items based on price? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>
To sort a collection of items based on price using Java Streams, you can use the sorted() method along with a lambda expression that compares the prices of each item. Here's an example:

Suppose you have a list of Item objects, where each object has a price field:
```java
class Item {
    String name;
    double price;

    public Item(String name, double price) {
        this.name = name;
        this.price = price;
    }

	public String getName() {
		return name;
	}

	public void setName(String name) {
		this.name = name;
	}

	public double getPrice() {
		return price;
	}

	public void setPrice(double price) {
		this.price = price;
	}
}
```
To sort the items based on price, you can create a stream from the list using the stream() method, and then call the sorted() method with a lambda expression that compares the prices of the items:
```java
import java.util.Arrays;
import java.util.List;
import java.util.stream.Collectors;

public class ItemManager {
public static void main(String[] args) {
	List<Item> items = Arrays.asList(
		    new Item("Book", 9.99),
		    new Item("Phone", 599.99),
		    new Item("Laptop", 1299.99),
		    new Item("Tablet", 499.99)
		);

		List<Item> sortedItems = items.stream()
		    .sorted((item1, item2) -> Double.compare(item1.getPrice(), item2.getPrice()))
		    .collect(Collectors.toList());

		sortedItems.forEach(item->{System.out.println(item.getName()+" : "+item.getPrice());});
}
}
```
```code
Output :
Book : 9.99
Tablet : 499.99
Phone : 599.99
Laptop : 1299.99
```
In this example, we create a list of Item objects, and then use the stream() method to create a stream from the list. We then call the sorted() method, passing in a lambda expression that compares the prices of the items using the Double.compare() method. Finally, we use the collect() method to collect the sorted items into a new list.

After running this code, the sortedItems list will contain the items sorted in ascending order based on price.

</blockquote>
</details>

---
56. Please use the stream api to create a map of numbers excluding the number 5 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>
To create a map of numbers excluding the number 5 using Java Streams, you can use the filter() and collect() methods. Here's an example:
```java
import java.util.Arrays;
import java.util.List;
import java.util.Map;
import java.util.stream.Collectors;

public class MapExample {
public static void main(String[] args) {
	List<Integer> numbers = Arrays.asList(1, 2, 3, 4, 5, 6, 7, 8, 9);

	Map<Integer, Integer> map = numbers.stream()
	    .filter(num -> num != 5)
	    .collect(Collectors.toMap(num -> num, num -> num));

	System.out.println(map);
}
}
```
```code
Output :
{1=1, 2=2, 3=3, 4=4, 6=6, 7=7, 8=8, 9=9}
```
In this example, we have a list of numbers from 1 to 9. We create a stream from the list using the stream() method, and then use the filter() method to exclude the number 5 from the stream. We then use the collect() method to collect the remaining numbers into a map.

The Collectors.toMap() method is used to create the map, with the identity function num -> num used as the key mapper and value mapper, since we want to use the numbers themselves as both the keys and the values in the map.

After running this code, the map variable will contain a map of the numbers from 1 to 9 excluding the number 5. The output of the System.out.println(map) statement would be:


</blockquote>
</details>

---
57. Is Stream is better than for loop and why?  

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>
Whether the Stream API is better than a traditional for loop in Java depends on the context and the specific use case. Here are some factors to consider:

- Conciseness and readability: The Stream API can often make code more concise and readable compared to traditional for loops. This is because it provides a higher-level abstraction for working with collections, and its fluent API allows you to chain together multiple operations in a single expression.

- Parallelization: The Stream API provides built-in support for parallel processing, which can lead to significant performance improvements in some cases. This is because it can automatically split up the work across multiple threads, which can lead to better utilization of multi-core processors. However, not all operations can be parallelized effectively, and there is some overhead involved in setting up and coordinating the parallel processing, so it's important to measure the performance gains carefully.

- Control flow: Traditional for loops provide more fine-grained control over the iteration process, such as the ability to break out of a loop early or skip over certain elements. While it's still possible to achieve these same effects with the Stream API, it can require more complex logic and may be less intuitive.

- Compatibility: The Stream API was introduced in Java 8, so if you need to support older versions of Java, you may not be able to use it. In addition, some libraries and frameworks may not support or integrate well with the Stream API yet, so it's important to consider compatibility when deciding whether to use it.

Overall, the Stream API can be a powerful tool for working with collections in Java, but it's not always the best choice in every situation. It's important to consider the trade-offs and choose the approach that makes the most sense for your specific needs.


</blockquote>
</details>

---
58. Can you create a stream to take our employees from the findAll() and return just the names? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>
Assuming we have a class Employee with a getName() method, and a List of Employee objects returned by a method called findAll(), we can create a stream to get just the names of the employees like this:
```java
List<Employee> employees = findAll();

List<String> names = employees.stream()
                               .map(Employee::getName)
                               .collect(Collectors.toList());
```
In this code, we first call findAll() to get a list of Employee objects. We then create a stream from this list using the stream() method. We use the map() method to transform each Employee object into its name using a method reference to the getName() method. Finally, we collect the resulting stream of names into a List using the toList() method provided by the Collectors class.

This code will produce a List of String objects containing the names of all the employees in the original list.


</blockquote>
</details>

---
