1.We never went over the differences between java version 8 and other versions?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details><summary><b> Show Answer</b></summary>

<blockquote>
Java 8 brings the most anticipated feature for the programming language called Lambda Expressions, a new language feature which allows users to code local functions as method arguments.Java 8 brings its own new specialized API for Date and Time manipulation.
</blockquote>

</details>

------------------------------------------------------------------------------------------------------------------------------------------------------------------------

2.Java static keyword 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details><summary><b> Show Answer</b></summary>

<blockquote>
Static keyword in java in Java indicates that a particular member is not an instance, but rather part of a type. The static member will be shared among all instances of the class, so we will only create one instance of it.
</blockquote>

</details>

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

3.when is memory allocated for static blocks?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details><summary><b> Show Answer</b></summary>

<blockquote>
A static block initializes the static variables. It executes whenever the class is loaded in memory. One class can have numerous static blocks, which will be executed in the same sequence in which they are written.
</blockquote>

</details>

----------------------------------------------------------------------------------------------------------------------------------------------------------------------

4.static/non-static?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details><summary><b> Show Answer</b></summary>

<blockquote>
Static variables are shared by all objects of a class and have a single instance, while non-static variables are unique to each object and have different values for different objects.

</blockquote>

</details>

----------------------------------------------------------------------------------------------------------------------------------------------------------------------

5.What is the difference between static variable and instance variable?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details><summary><b> Show Answer</b></summary>

<blockquote>
Static variables are created when the program starts and destroyed when the program stops.Instance variables are created when an object is created with the use of the keyword 'new' and destroyed when the object is destroyed. Instance variables can be accessed directly by calling the variable name inside the class.

</blockquote>

</details>

----------------------------------------------------------------------------------------------------------------------------------------------------------------------

6.How does the Java ternary work?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details><summary><b> Show Answer</b></summary>

<blockquote>
The ternary operator (? :) consists of three operands. It is used to evaluate Boolean expressions. The operator decides which value will be assigned to the variable. It is the only conditional operator that accepts three operands. It can be used instead of the if-else statement. It makes the code much more easy, readable, and shorter.

</blockquote>

</details>

----------------------------------------------------------------------------------------------------------------------------------------------------------------------

7.how to compile java code?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details><summary><b> Show Answer</b></summary>

<blockquote>
Compiling a Java program is very easy after JDK installation. 

Open a command prompt window and go to the directory where you saved the java program. Assume it's C:\.

Type 'javac Welcome.java' and press enter to compile your code. If there are no errors in your code, the command prompt will take you to the next line.

</blockquote>

</details>

----------------------------------------------------------------------------------------------------------------------------------------------------------------------

8.What is the static keyword?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details><summary><b> Show Answer</b></summary>

<blockquote>
The static keyword is a non-access modifier used for methods and attributes. Static methods/attributes can be accessed without creating an object of a class.

</blockquote>

</details>

----------------------------------------------------------------------------------------------------------------------------------------------------------------------

9.what happens if we remove static from the main method?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details><summary><b> Show Answer</b></summary>

<blockquote>
If you don't add the 'static' modifier in your main method definition, the compilation of the program will go through without any issues but when you'll try to execute it, a "NoSuchMethodError" error will be thrown.

</blockquote>

</details>

----------------------------------------------------------------------------------------------------------------------------------------------------------------------

10.What is JVM?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details><summary><b> Show Answer</b></summary>

<blockquote>
A Java Virtual Machine (JVM) is a program that interprets Java bytecode to run as a program by providing a runtime environment that executes this process. Furthermore, this is separate from its operating environment, supporting the “write once, run anywhere” philosophy.

</blockquote>

</details>

----------------------------------------------------------------------------------------------------------------------------------------------------------------------

11.What are wrapper class?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details><summary><b> Show Answer</b></summary>

<blockquote>

A Wrapper class is a class which contains the primitive data types (int, char, short, byte, etc).It provides a way to use primitive data types (int, char, short, byte, etc) as objects. 

</blockquote>

</details>

----------------------------------------------------------------------------------------------------------------------------------------------------------------------

12. what is immutable object?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details><summary><b> Show Answer</b></summary>

<blockquote>
An object is considered immutable if its state cannot change after it is constructed. Maximum reliance on immutable objects is widely accepted as a sound strategy for creating simple, reliable code. Immutable objects are particularly useful in concurrent applications.

</blockquote>

</details>

----------------------------------------------------------------------------------------------------------------------------------------------------------------------

13.what is autoboxing?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details><summary><b> Show Answer</b></summary>

<blockquote>
Autoboxing is the automatic conversion that the Java compiler makes between the primitive types and their corresponding object wrapper classes. For example, converting an int to an Integer, a double to a Double.

</blockquote>

</details>

----------------------------------------------------------------------------------------------------------------------------------------------------------------------

14.Mutable/Immutable classes in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details><summary><b> Show Answer</b></summary>

<blockquote>

A mutable object can be changed after it's created, and an immutable object can't.If you're defining your own class, you can make its objects immutable by making all fields final and private. Strings can be mutable or immutable depending on the language. Strings are immutable in Java.

</blockquote>

</details>

----------------------------------------------------------------------------------------------------------------------------------------------------------------------

15.Object class methods in java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details><summary><b> Show Answer</b></summary>

<blockquote>
Class Object is the root of the class hierarchy. Every class has Object as a superclass. All objects, including arrays, implement the methods of this class.

</blockquote>

</details>

----------------------------------------------------------------------------------------------------------------------------------------------------------------------

16.Example the difference between == and equals in java?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
<details><summary><b> Show Answer</b></summary>

<blockquote>
 == operator is  for reference comparison (address comparison) and .equals() method for content comparison. == checks if both objects point to the same memory location whereas .equals() evaluates to the comparison of values in the objects.

``` java 
public class Compare {
    public static void main(String[] args)
    {
        String x = "REVATURE";
        String y = "REVATURE";
        String z =  new String("REVATURE");
 
        System.out.println(x == y); // true
        System.out.println(x == z); // false
        System.out.println(x.equals(y)); // true
        System.out.println(x.equals(z)); // true
    }
}

Output:
true
false
true
true

```
 
</details>
 
<details><summary><b> Explanation</b></summary>
<blockquote>
we create two objects, namely x and y . Both x  and y refer to same objects.
When we use the == operator for x and y comparison, the result is true as both have the same addresses in the string constant pool.
Using equals, the result is true because it’s only comparing the values given in x and y.
</blockquote>
</details>


---------------------------------------------------------------------------------------------------------------------------------------------------------------------
 
17.Where are strings stored stack or heap?
 
![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details><summary><b> Show Answer</b></summary>

<blockquote>
Strings are stored on the heap area in a separate memory location known as String Constant pool. String constant pool is a separate block of memory where all the String variables are held.

</blockquote>

</details>

--------------------------------------------------------------------------------------------------------------------------------------------------------------------
  
18.How does garbage collection work? 
 
![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details><summary><b> Show Answer</b></summary>

<blockquote>

In garbage collection process, the collector scans different parts of the heap, looking for objects that are no longer in use. If an object no longer has any references to it from elsewhere in the application, the collector removes the object, freeing up memory in the heap.

</blockquote>

</details>
  
--------------------------------------------------------------------------------------------------------------------------------------------------------------------
  
19.Can the garbage collector be manually called?
 
![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details><summary><b> Show Answer</b></summary>

<blockquote>
By using System class that has a static method gc(), which is used to request JVM to call garbage collector.

</blockquote>

</details>

--------------------------------------------------------------------------------------------------------------------------------------------------------------------
  
20.What is the difference between String and String Builder

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details><summary><b> Show Answer</b></summary>

<blockquote>
String is immutable in Java. So it’s suitable to use in a multi-threaded environment. We can share it across functions because there is no concern of data inconsistency.When we create a String using double quotes, JVM first looks for the String with the same value in the string pool. If found, it returns the reference of the string object from the pool. Otherwise, it creates the String object in the String pool and returns the reference. JVM saves a lot of memory by using the same String in different threads.
StringBuilder classes that should be used for String manipulation. StringBuilder are mutable objects in Java. They provide append(), insert(), delete(), and substring() methods for String manipulation.

</blockquote>

</details>

--------------------------------------------------------------------------------------------------------------------------------------------------------------------
  
  
21.The differences between String, StringBuffer, and StringBuilder?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details><summary><b> Show Answer</b></summary>

<blockquote>
String is immutable whereas StringBuffer and StringBuilder are mutable classes.
StringBuffer is thread-safe and synchronized whereas StringBuilder is not. That’s why StringBuilder is faster than StringBuffer.
String concatenation operator (+) internally uses StringBuffer or StringBuilder class.
For String manipulations in a non-multi threaded environment, we should use StringBuilder else use StringBuffer class.

</blockquote>

</details>

--------------------------------------------------------------------------------------------------------------------------------------------------------------------
  
22.differentiate String vs StringBuffer?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details><summary><b> Show Answer</b></summary>

<blockquote>
Since String is immutable in Java, whenever we do String manipulation like concatenation, substring, etc. it generates a new String and discards the older String for garbage collection. These are heavy operations and generate a lot of garbage in heap. So Java has provided StringBuffer and StringBuilder classes that should be used for String manipulation. StringBuffer and StringBuilder are mutable objects in Java. They provide append(), insert(), delete(), and substring() methods for String manipulation.

</blockquote>

</details>
  
--------------------------------------------------------------------------------------------------------------------------------------------------------------------

23.value and reference type?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details><summary><b> Show Answer</b></summary>

<blockquote>

A ValueType is a type that represents a value. This is similar to how primitive types are represented in Java. ReferenceType encompasses classes, interfaces, and array types as defined in The Java Language Specification . All ReferenceType objects belong to one of the following subinterfaces: ClassType for classes, InterfaceType for interfaces, and ArrayType for arrays.

</blockquote>

</details>
 
--------------------------------------------------------------------------------------------------------------------------------------------------------------------
