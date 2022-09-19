1. What are the ways to declare a string in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

There are two ways to declare a String in Java

Using `string` literal: Double quotes are used to create Java String literals. 
Example: `String str= "Welcome"; ` 
Using `new` keyword: Keyword `new` is used to create a Java string.
Example: `String str=new String ( "Welcome");`


 </blockquote>

</details>


---

2. Why strings are of derived type in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

 Strings are Java objects that represent sequences of characters. String objects are created using the `java.lang.String class`. There are many functions to be invoked when processing a string, such as `substring()`, `indexof()`, `equals()`, `toUppercase()`, etc, which primitives types do not have.

  </blockquote>

</details>


---

3. Is String immutable in Java? If so state the reason.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

Yes, Strings are immutable in Java. Which mean that they can't be changed or altered once created. However, we can only modify the reference to the string object. 

  </blockquote>

</details>


---

4. Differentiate between `str1 == str2` and `str1.equals(str2)`.


![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

- In Java both the `equals()` method and the `==` operator compares the objects.

- The `==` operator can be used for comparing references (addresses) and the `.equals()` method can be used to compare the content.
`==` checks if the objects point to the same memory location, whereas `.equals()` compares the values of the objects.

  </blockquote>

</details>


---

5. Can we use a string in the switch case in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

Yes, Java allows to use strings in switch case conditions to be declared in double quotes. 

   </blockquote>

</details>


---

6. How can two strings be compared in Java?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

- `String Equals Method`- strings are compared based on the values within them.
- `String Equals Ignore Case`:the two strings are compared without taking case into account.
- `Object Equals Method`:The method returns true if its arguments are equal, otherwise, it returns false.
- `String Compare To Method`:This method compares input strings with each other and returns some value based on the condition.

   </blockquote>

</details>


---

7. Is String thread-safe in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

Yes

</blockquote>

<details><summary><b> Explanation </b></summary>

<blockquote>

Strings are immutable objects,so they can't be changed or altered once created. As a result, whenever we manipulate a String object, it creates a new String rather than modifying the original string object. In Java, every immutable object is thread-safe, which means String is also thread-safe in Java.

</blockquote>

</details>

</details>

---

8. What is the use of string `subSequence` method?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

The Java String `subSequence()` method is a built-in function that returns a charSequence (a subsequence) from a string.

</blockquote>

<details><summary><b> Explanation </b></summary>

<blockquote>

``` java
 String Str ="Nothing can stop a good idea";
 System.out.println(Str.subSequence(0, 6));
 ```

 - here it will return `Nothing` using `subSequence()` method

 </blockquote>

</details>

</details>

---

9. How do you convert a string to an integer and vice versa in Java?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

Integer class in the Java lang package provides different methods for converting strings to integers and vice versa. The `parseInt()` method allows you to convert a String into an integer and the `toString()` method allows you to convert an Integer into a String. 

 </blockquote>

</details>

---

10. How to check whether a String is empty in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

The `isEmpty()`method in Java String class determines whether or not a string is empty. . In the case where the length of the string is zero, it returns true, or else it returns false.

 </blockquote>

</details>

---

11. What is the use of String pool in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

- It is a special type of memory maintained by the JVM to store unique string objects.

- When you assign the same string literal to different string variables, JVM saves only one copy of the String object in the String pool.

 </blockquote>

</details>

---

12. How many objects will be created in the following code?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

```java

String s1=" Java ";
String s2=" Java";

```

<details><summary><b> Show Answer </b></summary>

<blockquote>

Only one object will be created. 

</blockquote>

<details><summary><b> Explanation </b></summary>

<blockquote>

Here, for line1 (s1), one new object will get created in String constant pool, whereas for line 2, string s2 will create a reference to the String s1 because the string constant pool already has a String object s1 with the same string value (Java).


 </blockquote>

</details>

</details>

---

13. Why is it safer to store passwords in a Char[] array rather than a string?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

- When we use string we cannot do overwriting, modifying, or zeroing out its contents, so it is unsuitable for storing sensitive information.

- By using a `char[]array`, we have complete control over that information. We can modify it or wipe it completely without even relying on the garbage collector.

 </blockquote>

</details>

---

14. Whcih method is used to creates an exact copy of a String object in the heap?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

- The `intern()` method creates an exact copy of a String object in the heap and stores it in the String constant pool, which the JVM maintains.

- Java automatically interns all strings created using string literals.`intern()` method is used to tell the JVM to add it to the string pool if it doesn't already exist there, and return a reference of that interned string.

 </blockquote>

</details>

---

15. How does the method `int compareTo()` works?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

It is to compares the input argument with the Number object. It returns 1 (positive number) if the value of Number object is greater than the argument, -1 (negative number) if it is less than the value of argument and 0 if it is equal to the argument.

 </blockquote>

</details>

---

16. What is the use of `valueof()` method?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

- It converts the value of an argument into the relevant Number Object. The argument can be any numeric primitive data type or String.

- However if there is a radix mentioned in the argument, the respective data is converted into the base of the radix first and then converted to an Integer object.


 </blockquote>

</details>

---

17. Differentiate between `ceil()` and `floor()`.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

- `ceil()`-Returns the smallest integer that is greater than or equal to the argument in double format.
- `floor()`-Returns the largest integer that is less than or equal to the argument in double format.

 </blockquote>

</details>

---

18. Is it possible to count the number of times a given character appears in a String?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

The `charAt()` method of the String class can be used to find out the number of times a specified character appears in a string.

 </blockquote>

</details>

---

19. How many objects will be created for the following code:

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

``` java
String str1 = "Java";
String str2 = new String("Java");
```

<details><summary><b> Show Answer </b></summary>

<blockquote>

Here, Two objects are created. Object created using new operator is stored in the heap memory (str2).
Object created using String literal str1 is stored in the string constant pool.

 </blockquote>

</details>

---

20. Give the example for mutable and immutable objects in java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

- Mutable objects value can be changed. StringBuilder and StringBuffer are the examples of the mutable objects.

- mmutable objects value can not be changed once created. String is an immutable class in java.

 </blockquote>

</details>

---

21. Explain about Delimiters  in Java.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

- In Java, delimiters are characters that separate the strings into tokens. We can define any character as a delimiter in Java. 

 </blockquote>

</details>

---

22. What is the use of `split ()` method in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

The method `split(String regex)` to split the String into String array based on the provided regular expression

 </blockquote>

</details>

---

23. If the invoking string is less than the string compared, what value will be returned by the function `compareTo`?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

negative value 

 </blockquote>

</details>

---

24. Differentiate between `format()` and `printf()` methods in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

Both the methods are used to format String and the key difference is that `format()` method returns a formatted String while the `printf(`) method prints the formatted String to console. So, if you need a formatted String, use the `format()` method and if you want to print the string use `printf()` method.


 </blockquote>

</details>

---

25. Whcih method is to remove white space from String in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

`trim()` method is used to remove white space from String in Java. 

`public String trim()`- The `trim()` method accepts no parameters and returns omitted string with no leading and trailing spaces

 </blockquote>

</details>

---

26. Which class is the superclass of string class in Java?


![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

Object class is the superclass of string. String class extends object class.

 </blockquote>

</details>

---

27. How many objects will create for the identical string?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

Two identical string literal would create two separate string references but both will refer to the same object because string class is immutable in Java.

 </blockquote>

</details>

---

28. Why string class is declared as final in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

String class has been marked as final so that we could not override the immutable behavior of string class.

 </blockquote>

</details>

---

29. What will be the disadvantage of string class in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

we cannot extend String class to get additional features in Java

 </blockquote>

</details>

---

30. What are the ways to concatenate strings in Java?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

Using `concat() method`: Concatenates or joins the specified string to the end of current string and creates a new string object.
Using `+ (String concatenation) operator`: Used to add two or more strings.

 </blockquote>

</details>

---

31. Differentiate between length and capacity in Java StringBuffer?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

Capacity is the total number of characters hold in the StringBuffer object. Whereas, length is the number of characters already present in the StringBuffer object.

 </blockquote>

</details>

---

32. Why StringBuffer and StringBuilder classes are introduced in java when there already exist String class to represent the set of characters?


![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

The objects of String class are immutable in nature, so you can’t modify them once they are created. If you try to modify them, a new object will be created with modified content. This may cause memory and performance issues if you are performing lots of string modifications in the code. To overcome these issues, StringBuffer and StringBuilder classes are introduced in Java.

 </blockquote>

</details>

---

33. What package should be imported to use Integer class in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

To use the Integer class methods `import java.lang.Number` package should be imported.

 </blockquote>

</details>

---

34. Is Java Number class is an abstarct class?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

Yes

</blockquote>

<details><summary><b> Explanation </b></summary>

<blockquote>

It is an abstract class which is placed in `java.lang package`has four abstract methods and two concrete methods.which is the superclass of classes `BigDecimal`, `BigInteger`, `Byte`, `Double`, `Float`, `Integer`, `Long`, and `Short` with only one consructor `number()`.


 </blockquote>

</details>

</details>

---

35. How does the method `xxxValue()` works in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

This will Convert the value of this Number object to the xxx data type and returns the value.

 </blockquote>

</details>

---



## Problem Solving

36. Predict the output of the following code.

 ![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

 ``` java
 public class Main
{
   public static void main(String[] args)
   {
       String str1=new String("SQL"); 
       String str2=new String("SQL");    
       System.out.println(str1 == str2);  
       System.out.println(str1.equals(str2));
   }
}
```
<details><summary><b> Show Answer </b></summary>

<blockquote>

false
true

</blockquote>

<details><summary><b> Explanation </b></summary>

<blockquote>

If str1 and str2 are compared using the == operator, then the result will be false, because both have different addresses in the memory. Both must have the same address in the memory for the result to be true.
If you use the equals method, the result is true since it's only comparing the values given to str1 and str2, even though they are different objects.

 </blockquote>

</details>

</details>

---

37. What string method should be used in line 7 to display the message "gramming"?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)


``` java

import java.lang.Math;
public class Main
{  
   public static void main(String args[])
   {
         String str = "Java Programming";
         System.out.print("Message: ");
       // Line 7 
   }
}

```
<details><summary><b> Show Answer </b></summary>

<blockquote>

System.out.println(str.substring(9, 17));

</blockquote>

<details><summary><b> Explanation </b></summary>

<blockquote>

using `substring()` method to prints the substring from the index 9-17(exclusive 17th index).

 </blockquote>

</details>

</details>

---

38. What will be the output of the following code?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)


``` java

public class StringClass 
{
    public static void main(String args[])
    {
        String str = "Scaler";
        String str1 = "InterviewBit";   
        String str2 = "Scaler";
        System.out.println(str.equals(str1) + " " + str.equals(str2));
    }
}
```
<details><summary><b> Show Answer </b></summary>

<blockquote>

false true

</blockquote>

<details><summary><b> Explanation </b></summary>

<blockquote>

`equals()` method will check the values of strings are equal or not. 

 </blockquote>

</details>

</details>

---

39. How many strings can be collected by Garbage Collector in the following code snippet?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

``` java

public static void main(String[] fruits) {
  String s1 = new String("Java");
  String s2 = new String("Programming");
  String s3 = new String("Language");
  s3 = s1;
  s2 = s3;
  s1 = s2;
}

```
<details><summary><b> Show Answer </b></summary>

<blockquote>

2 (s2 and s3)

</blockquote>

<details><summary><b> Explanation </b></summary>

<blockquote>

All three strings (s1, s2, s3) point to the same string that is "Java". so, the two strings s2 and s3 can be collected by Garbage Collector before the end of `main()` method.

 </blockquote>

</details>

</details>

---


## Scenario Based Question


40. Which class should we use among String,StringBuffer and StringBuilder when there are lot of String concatenation and String modification operations with thread-safe code?

 ![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

StringBuffer

</blockquote>

<details><summary><b> Explanation </b></summary>

<blockquote>

- If we use String , with every modification and concatenation operation, a new String is formed as String is immutable. It will lead to the memory allocation issues.
- StringBuilder can not be used as it is not synchronized, i.e thread-safe.

 </blockquote>

</details>

</details>

---
