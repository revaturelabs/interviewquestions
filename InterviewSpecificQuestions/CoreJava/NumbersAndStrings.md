1. How do Strings work? (or) Brief us on strings

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>
 
 String is a sequence of characters. String objects are immutable which means a constant and cannot be changed once created. Also, it stored in a special memory area inside heap known as string constant pool.
 
 String objects can be created as a literal or using new operators.

- **String name1 = “Java”;** 
  - The above statement creates a string object and places it in a string pool if it is not already present in the string pool and a reference is assigned to name1.

- **String name2 = new String(“newJava”);**
  - The above statement creates a string object in heap memory and checks whether it is present in the string pool or not. If the ‘newJava’ is not present in the string pool, then it will place this string in the string pool else it will skip it. In this case, two objects are created that is one in heap memory and the other in the string pool.

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
|       StringBuffer is synchronized i.e. thread safe. It means two threads can't call the methods of StringBuffer simultaneously.      | StringBuilder is non-synchronized i.e. not thread safe. It means two threads can call the methods of StringBuilder simultaneously. |
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
 
 - Java need wrapper classes to be a pure Object Oriented Programming language, so Java needs everything to look like an object.
 - Classes in Collection framework & java.util package, such as ArrayList and Vector, store only objects (reference types) and not primitive types
 - Wrapper classes has lot of utility methods, it really helpful and easier.

 
</blockquote>
</details>

--- 
9. What is autoboxing and unboxing?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>
 
The process of converting a primitive value into an object of the corresponding wrapper class is called autoboxing.

The process ofconverting an object of a wrapper type to its corresponding primitive value is called as unboxing.

</blockquote>
</details>

--- 

4. Differentiate between `str1 == str2` and `str1.equals(str2)`, where both str1 & str2 are String objects.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

- In Java both the `equals()` method and the `==` operator compares the objects.

- The `==` operator can be used for comparing references (addresses) and the `.equals()` method can be used to compare the content.
`==` checks if the objects point to the same memory location, whereas `.equals()` compares the values of the objects.

  </blockquote>

</details>

---

6. How can two strings be compared in Java?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

- `String Equals Method`: Compares this string to the specified object. The result is true if and only if the argument is not null and is a String object that represents the same sequence of characters as this object.
Syntax: `public boolean equals(Object anObject)` 
e.g., `str1.equals(str2)`

- `String Equals Ignore Case`: Two strings are compared without taking the case of the strings (lower or upper) into account.
Syntax: `public boolean equalsIgnoreCase(String anotherString)`
e.g. `str1.equalsIgnoreCase(str2);`

- `Objects Equals Method`: This is th `Objects` class method which returns true if the arguments are equal to each other and false otherwise. Consequently, if both arguments are null, true is returned and if exactly one argument is null, false is returned. Otherwise, equality is determined by using the equals method of the first argument.
Syntax: `public static boolean java.util.Objects.equals(Object a, Object b)`
e.g. `Objects.equals(str1, str2);`

- `String Compare To Method`: Compares two strings lexicographically based on the Unicode value of each character sequence represented by the String object being compared lexicographically to the character sequence represented by the argument string. The result is a negative integer if this String object lexicographically precedes the argument string. The result is a positive integer if this String object lexicographically follows the argument string. The result is zero if the strings are equal; compareTo returns 0 exactly when the equals(Object) method would return true.
Syntax: `public int compareTo(String anotherString)`
e.g. `str1.compareTo(str2);`

Note: == operator is avoided, since it checks for reference equality, i.e. if the strings point to the same object or not.

</blockquote>
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

16. What is the use of `valueof()` method?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

- It converts the value of an argument into the relevant Number Object. The argument can be any numeric primitive data type or String.

- However if there is a radix mentioned in the argument, the respective data is converted into the base of the radix first and then converted to an Integer object.

 </blockquote>

</details>

---

20. Give the example for mutable and immutable objects in java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

- Mutable objects value can be changed. StringBuilder and StringBuffer are the examples of the mutable objects.

- mmutable objects value cannot be changed once created. String is an immutable class in java.

 </blockquote>

</details>

---

2. What is the use of `split ()` method in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

The method `split(String regex)` to split the String into String array based on the provided regular expression

 </blockquote>

</details>

---

40. Which class should we use among String,StringBuffer and StringBuilder when there are lot of String concatenation and String modification operations with thread-safe code?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

<blockquote>

**StringBuffer**

Reason:

- If we use String , with every modification and concatenation operation, a new String is formed as String is immutable. It will lead to the memory allocation issues.
- StringBuilder cannot be used as it is not synchronized, i.e. thread-safe.

 </blockquote>

</details>

</details>

---
