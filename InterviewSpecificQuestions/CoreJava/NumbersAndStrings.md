1. How do Strings work? (or) Brief us on strings

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>
 
 String is a sequence of characters. String objects are immutable which means a constant and cannot be changed once created. Also, it stored in a special memory area inside heap known as string constant pool.
 
 String objects can be created as a literal or using new operators.

- **String name1 = “Java”;** 
  - The above statement creates a string object and places it in a string pool if it is not already present in the string pool and a reference is assigned to name1.

- **String name2 = new String(“newJava”);**
  - The above statement creates a string object in heap memory and checks whether it is present in the string pool or not. If the ‘newJava’ is not present in the string pool, then it will place this string in the string pool else it will skip it. In this case, two objects are created that is one in heap memory and the other in the string pool.

</blockquote>
</details>

--- 

2. What is the difference between String Buffer and String Builder?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>
 
 |                                                              StringBuffer                                                             |                                                            StringBuilder                                                           |
|:-------------------------------------------------------------------------------------------------------------------------------------:|:----------------------------------------------------------------------------------------------------------------------------------:|
|       StringBuffer is synchronized i.e., thread safe. It means two threads can't call the methods of StringBuffer simultaneously.      | StringBuilder is non-synchronized i.e., not thread safe. It means two threads can call the methods of StringBuilder simultaneously. |
| Faster than String class due to mutability but slower than StringBuilder class as it allows multiple threads simultaneous operations. |              Fastest among all as it allows mutability and does not allow multiple threads operating at the same time.             |
|                                           Syntax: StringBuffer var = new StringBuffer(str);                                           |                                         Syntax: StringBuilder var = new StringBuilder(str);                                        |


</blockquote>
</details>

--- 

3. What classes are mutable strings? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>
 
 StringBuilder and StringBuffer 

</blockquote>
</details>

--- 

4. Why Strings in Java are immutable?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>
 
 In the String constant pool, a String object is likely to have one or many references. If several references point to the same String without even knowing it, it would be bad if one of the references modified that String value. That's why String objects are immutable.

</blockquote>
</details>

--- 

5. How would you reverse a string of your name?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>

StringBuilder or StringBuffer class has an in-build method reverse() to reverse the characters in the string. 

```java
public static void main(String[] args) {		
		
		Scanner sc = new Scanner(System.in);
		String str = sc.next();
		
		StringBuilder sb = new StringBuilder(str);
		sb.reverse();
		
		System.out.println(sb);
}
```
 
</blockquote>
</details>

--- 

6. What are Wrapper classes?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>
 
A Wrapper class is a class whose object wraps or contains primitive data types. Each of the 8 primitive types has corresponding wrapper classes.

| Primitive Type | Wrapper Class |
|----------------|---------------|
| byte           | Byte          |
| boolean        | Boolean       |
| char           | Character     |
| double         | Double        |
| float          | Float         |
| int            | Integer       |
| long           | Long          |
| short          | Short         |

</blockquote>
</details>

--- 

7. Why do we use wrapper classes? or What is the purpose of the Wrapper class in java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>
 
 - Java need wrapper classes to be a pure Object-Oriented Programming language, so Java needs everything to look like an object.
 - Classes in Collection framework & java.util package, such as ArrayList and Vector, store only objects (reference types) and not primitive types
 - Wrapper classes has lot of utility methods, it really helpful and easier.

 
</blockquote>
</details>

--- 
8. What is autoboxing and unboxing?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>
 
The process of converting a primitive value into an object of the corresponding wrapper class is called autoboxing.

The process of converting an object of a wrapper type to its corresponding primitive value is called as unboxing.

</blockquote>
</details>

--- 

9. Differentiate between `str1 == str2` and `str1.equals(str2)`, where both str1 & str2 are String objects.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

- In Java both the `equals()` method and the `==` operator compares the objects.

- The `==` operator can be used for comparing references (addresses) and the `.equals()` method can be used to compare the content.
`==` checks if the objects point to the same memory location, whereas `.equals()` compares the values of the objects.

  </blockquote>

</details>

---

10. How can two strings be compared in Java?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

- `String Equals Method`: Compares this string to the specified object. The result is true if and only if the argument is not null and is a String object that represents the same sequence of characters as this object.
Syntax: `public boolean equals(Object anObject)` 
e.g., `str1.equals(str2)`

- `String Equals Ignore Case`: Two strings are compared without taking the case of the strings (lower or upper) into account.
Syntax: `public boolean equalsIgnoreCase(String anotherString)`
e.g., `str1.equalsIgnoreCase(str2);`

- `Objects Equals Method`: This is the `Objects` class method which returns true if the arguments are equal to each other and false otherwise. Consequently, if both arguments are null, true is returned and if exactly one argument is null, false is returned. Otherwise, equality is determined by using the equals method of the first argument.
Syntax: `public static boolean java.util.Objects.equals(Object a, Object b)`
e.g., `Objects.equals(str1, str2);`

- `String Compare To Method`: Compares two strings lexicographically based on the Unicode value of each character sequence represented by the String object being compared lexicographically to the character sequence represented by the argument string. The result is a negative integer if this String object lexicographically precedes the argument string. The result is a positive integer if this String object lexicographically follows the argument string. The result is zero if the strings are equal; compare To returns 0 exactly when the equals(Object) method would return true.
Syntax: `public int compareTo(String anotherString)`
e.g., `str1.compareTo(str2);`

Note: == operator is avoided, since it checks for reference equality, i.e. if the strings point to the same object or not.

</blockquote>
</details>

---

11. How do you convert a string to an integer and vice versa in Java?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

Integer class in the Java lang package provides different methods for converting strings to integers and vice versa. The `parseInt()` method allows you to convert a String into an integer and the `toString()` method allows you to convert an Integer into a String. 

 </blockquote>

</details>

---

12. What is the use of `valueof()` method?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

- It converts the value of an argument into the relevant Number Object. The argument can be any numeric primitive data type or String.

- However, if there is a radix mentioned in the argument, the respective data is converted into the base of the radix first and then converted to an Integer object.

 </blockquote>

</details>

---

13. Give the example for mutable and immutable objects in java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

- Mutable objects value can be changed. StringBuilder and StringBuffer are the examples of the mutable objects.

- mmutable objects value cannot be changed once created. String is an immutable class in java.

 </blockquote>

</details>

---

14. What is the use of `split ()` method in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

The method `split(String regex)` to split the String into String array based on the provided regular expression

 </blockquote>

</details>

---

15. Which class should we use among String,StringBuffer and StringBuilder when there are lot of String concatenation and String modification operations with thread-safe code?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

**StringBuffer**

Reason:

- If we use String , with every modification and concatenation operation, a new String is formed as String is immutable. It will lead to the memory allocation issues.
- StringBuilder cannot be used as it is not synchronized, i.e., thread-safe.

 </blockquote>

</details>

</details>

---
16. Difference between int and Integer   

<details><summary><b> Show Answer</b></summary>

<blockquote>

In Java, int and Integer are both used to represent integer values, but there are some key differences between them.

- int is a primitive data type, while Integer is a wrapper class that provides a way to use int values in object-oriented contexts. This means that int values are stored as simple binary values, while Integer objects are stored as instances with attributes and behaviors.

- int is a value type, while Integer is a reference type. This means that int values are passed by value, while Integer objects are passed by reference.

- int has a default value of 0, while Integer has a default value of null.

- int has a fixed range of values (-2,147,483,648 to 2,147,483,647), while Integer has a larger range of values (from -2^31 to 2^31-1) due to its ability to handle null values.

- int values can be used directly in arithmetic operations, while Integer objects need to be converted to int values using the intValue() method before they can be used in arithmetic operations.

Overall, int is generally preferred for basic arithmetic operations and where memory usage and performance are a concern, while Integer is more useful in situations where an object-oriented approach is needed, such as when dealing with collections or passing values between methods that require objects.

</blockquote>

</details>

---
17. What are Wrapper Classes?  

<details><summary><b> Show Answer</b></summary>

<blockquote>

Wrapper classes are the classes that allow primitive data types to be treated as objects. There is a wrapper class for each primitive data type, and they provide utility methods for converting between primitive data types and objects, as well as for performing various other operations on the data. Wrapper classes are useful in situations where an object is required, but only a primitive data type is available. Some examples of wrapper classes are `Boolean`, `Byte`,`Character`, `Short`, `Integer`,`Long`, `Float`, and `Double`.

</blockquote>

</details>

---
18. The differences between String, StringBuffer, and StringBuilder. 

<details><summary><b> Show Answer</b></summary>

<blockquote>

Strings, StringBuilder, and StringBuffer are classes in Java used to manipulate character sequences and the main differences between them are Strings are immutable, while StringBuilder and StringBuffer are mutable. StringBuffer and StringBuilder both provide the same functionality to the use with differences like StringBuffer is thread-safe, while StringBuilder is not thread-safe. The performance of StringBuilder is high as compared to StringBuffer. Strings create a new object in memory every time they are modified, while StringBuilder and StringBuffer use a single buffer.

</blockquote>

</details>

---

19. What types of Methods are in a String class 

<details><summary><b> Show Answer</b></summary>

<blockquote>

The String class in Java has several built-in methods that allow you to manipulate and work with strings. Some of the most commonly used methods include:

- length(): This method returns the length of a string.

- charAt(int index): This method returns the character at the specified index in the string.

- substring(int beginIndex): This method returns a new string that is a substring of the original string, starting from the specified index.

- substring(int beginIndex, int endIndex): This method returns a new string that is a substring of the original string, starting from the specified begin index and ending at the specified end index.

- indexOf(char c): This method returns the index of the first occurrence of the specified character in the string.

- indexOf(String str): This method returns the index of the first occurrence of the specified substring in the string.

- lastIndexOf(char c): This method returns the index of the last occurrence of the specified character in the string.

- lastIndexOf(String str): This method returns the index of the last occurrence of the specified substring in the string.

- toUpperCase(): This method returns a new string with all characters in uppercase.

- toLowerCase(): This method returns a new string with all characters in lowercase.

- equals(Object obj): This method compares the string to the specified object and returns true if they are equal.

- equalsIgnoreCase(String str): This method compares the string to the specified string, ignoring case differences.

- startsWith(String prefix): This method returns true if the string starts with the specified prefix.

- endsWith(String suffix): This method returns true if the string ends with the specified suffix.

- replace(char oldChar, char newChar): This method returns a new string with all occurrences of the specified old character replaced with the specified new character.

- replaceAll(String regex, String replacement): This method returns a new string with all occurrences of the specified regular expression replaced with the specified replacement string.

</blockquote>

</details>

---
20. What is the substring function used for?

<details><summary><b> Show Answer</b></summary>

<blockquote>

The substring() function in Java is a method of the String class that is used to extract a part of a string. It returns a new string that is a substring of the original string. The substring() method takes two parameters: the starting index and the ending index of the substring.

The syntax of the substring() method is as follows:
```java
String substring(int startIndex)
String substring(int startIndex, int endIndex)
```
The first form of the method returns the substring starting from the given index to the end of the string.

The second form of the method returns the substring starting from the given start index up to, but not including, the specified end index.

For example, the following code snippet extracts a substring from a given string:
```java
String str = "Hello World";
String substr1 = str.substring(6); // Returns "World"
String substr2 = str.substring(0, 5); // Returns "Hello"
```
Note that the index starts at 0, so the first character in the string has an index of 0.

</blockquote>

</details>

---
21. Tell me about Strings in java

<details><summary><b> Show Answer</b></summary>

<blockquote>

In Java, a String is an object that represents a sequence of characters. It is one of the most commonly used classes in Java and is part of the java.lang package, which is automatically imported into every Java program.

Strings in Java are immutable, which means that once a string is created, its value cannot be changed. This property is enforced by the final keyword, which is used to declare the internal character array of the String class.

The String class provides a wide range of methods that allow you to manipulate and extract information from strings. Some of the most commonly used methods include:

- length(): returns the number of characters in the string
- charAt(int index): returns the character at the specified index
- substring(int beginIndex, int endIndex): returns a substring of the original string from the beginIndex to the endIndex
- indexOf(String str): returns the index of the first occurrence of the specified string
- toUpperCase(): returns a new string with all characters in uppercase
- toLowerCase(): returns a new string with all characters in lowercase
- equals(Object obj): compares the current string to the specified object for equality
- compareTo(String str): compares the current string to the specified string lexicographically
Strings can be concatenated using the + operator or the concat() method. For example:
```java
String str1 = "Hello";
String str2 = "world";
String str3 = str1 + " " + str2; // "Hello world"
String str4 = str1.concat(" ").concat(str2); // "Hello world"
```
Java also provides a shorthand for creating String objects using string literals. For example:
```java
String str = "Hello world";
```
This creates a new String object with the value "Hello world".
</blockquote>

</details>

---
22. difference between instantiating a string = "dog" vs = new String("dog")?;

<details><summary><b> Show Answer</b></summary>

<blockquote>

In Java, there are two ways to create a string:

Using string literal - "dog"
Using the new keyword - new String("dog")
When a string is created using a string literal, Java creates a string object and adds it to the string pool. When a new string object is created using the new keyword, Java creates a new object on the heap memory, even if a string with the same value already exists in the string pool.

Here are some of the differences between these two ways of creating a string:

Performance: String literals are faster and more efficient as they use the string pool. String objects created using the new keyword are slower as they create a new object every time.

Object references: When a string literal is used, only one object reference is created, and all the variables with the same string literal point to the same object. When the new keyword is used, a new object reference is created every time.

String pool: String literals are added to the string pool, which is a special memory area reserved for storing strings. Strings created using the new keyword are not added to the string pool.

In general, it is recommended to use string literals instead of creating new string objects using the new keyword, as string literals are more efficient and easier to use. However, in certain situations, such as when comparing strings using the == operator, it is recommended to use the new keyword to create new string objects.
</blockquote>

</details>

---
23. do you understand immutable classes?

<details><summary><b> Show Answer</b></summary>

<blockquote>

In Java, immutable classes are classes whose instances cannot be modified once they are created. This means that the values of the instance variables of an immutable class cannot be changed after the object is created.

Immutable classes are typically used to represent values that do not change over time, such as dates, times, and other types of data. By making these classes immutable, Java provides a level of safety and predictability in the code, as developers can be sure that the objects they are working with will not change unexpectedly.

Examples of immutable classes in Java include String, Integer, and LocalDate. These classes are all final, which means they cannot be subclassed and their methods cannot be overridden, further ensuring their immutability.

</blockquote>

</details>

---
24. What is StringBuilder?

<details><summary><b> Show Answer</b></summary>

<blockquote>

StringBuilder is a class in Java that provides a mutable sequence of characters. It is similar to the String class, but unlike String, StringBuilder allows modification of its characters without creating a new object. This makes it more efficient for applications that require frequent string manipulations.

StringBuilder provides methods for appending, inserting, deleting, and replacing characters in the sequence. It also provides methods for converting the sequence to a String object or to a character array.

StringBuilder is often used in situations where the contents of a string need to be modified frequently, such as in a loop that builds a long string incrementally. The use of StringBuilder in such cases can improve performance compared to using String, as creating a new String object for each iteration of the loop can be slow and inefficient.

In summary, StringBuilder is a mutable class in Java that provides methods for modifying sequences of characters, making it more efficient than the immutable String class for certain types of applications.

</blockquote>

</details>

---
25. String vs StringTokenizer 

<details><summary><b> Show Answer</b></summary>

<blockquote>

String is more commonly used and provides greater flexibility and functionality, while StringTokenizer is used for simpler tasks that involve splitting a string into smaller substrings based on a delimiter. However, since StringTokenizer is a legacy class, it is recommended to use the String class and its built-in methods for more advanced string manipulation tasks.

</blockquote>

</details>

---
