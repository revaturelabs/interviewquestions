1.What is String in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details>
    <summary><b> Show Answer </b></summary> 
<blockquote>


- String are sequence of characters in java.
- String is in `java.lang package`.
- String is immutable and are stored inside the string constant pool. 
- If we try to alter the value of String variable, new String object is created and assigned to same reference variable.
</blockqoute> 
</details>

---

2.What are the different ways to create a string in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details>
    <summary><b> Show Answer </b></summary> 
<blockquote>

There are two ways to create strings in java.
  - Using literal string, we can assign the value to a string with double quotes. The value is stored in a string constant pool.
	
**Example**
``` java
	String string = "Hello";
```
	
    - Using new keyword – It will create the new object in the heap memory
	
**Example**
``` java
	String string = new String("Hello");
```
</details>

---

3.What's the difference between == and `.equals()` in Java? 
	
![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details>
    <summary><b> Show Answer </b></summary> 
<blockquote>

Double equals (==) is an operator that compares the value and reference. Dot equals (.equals) is a method that checks the value only.

**Example**
``` java
public class Main {
    public static void main(String[] args) {
        String str1 = "Hello";
        String str2 = new String("Hello");
        System.out.println(str1==str2);//false
        System.out.println(str1.equals(str2));//true
    }
}
```
- The first output statement will give output as false where the values are the same but the reference differs.
- The second output statement will give output as true where the values are the same even after the reference differs.
</details>

---

4.Why String is immutable in Java?
	
![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details>
    <summary><b> Show Answer </b></summary> 
<blockquote>

- When create a string using string literal, a memory allocated at the string constant pool a reference assign to variable. 
- If we create a string with the same value, the same reference will be stored to the variable instead of creating new memory.
- If we change any the value of the string, the entire string is rewritten and new reference is created.
- Hence, the strings are immutable.
</details>

---
	
5.What will happen if we use `new` keyword while craeting a string?
	
![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details>
    <summary><b> Show Answer </b></summary> 
<blockquote>

- When we `new` keyword while creating, the memory is allocated at heap. 
- If we again create a variable with the same value, a new memory is created in heap.
- If we create without `new` keyword, it will be stored in String Constant Pool.
- If we create a string with the same value without `new`, the same reference will be stored to the variable instead of creating new memory. 

</details>

---

6.What's the difference between next() and nextLine() methods from Java `Scanner` class?
	
![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details>
    <summary><b> Show Answer </b></summary> 
<blockquote>

- `next()` will consider the spaces as seperation between each inputs.
- `nextLine()` will consider the line itself as a input with spaces.
</details>

---

7.How will you convert each word in the sentence as String array?
	
![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details>
    <summary><b> Show Answer </b></summary> 
<blockquote>

- In String class we have `split()` method ( String regex)  that returns array of strings(String[]) separated by the provided delimiting regular expression.
- A regular expression is a sequence of characters that forms a search pattern (usually letter, number and/or special character).
- When you search for data in a text, you can use this search pattern to describe what you are searching for.
The method returns array of String post delimiting it.
- We can also give limit to the string.
``` java
public class Main {
	public static void main(String[] args) {
	String setence = "This is the example for seperation of words from string";
	String[] words = setence.split(" ");
	for (int i = 0; i < words.length; i++) {
		System.out.println(words[i]);
	}
	}
}
```
</blockqoute> 
</details>
	
---

8.Name some methods which are used for the string operations.
	
![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details>
    <summary><b> Show Answer </b></summary> 
<blockquote>

| **Method**         | **Details**                                                                               |
|--------------------|-------------------------------------------------------------------------------------------|
| split()            | It returns **char** at specified position of string.                                          |
| compareTo()        | It returns **int** value based on comparison of two strings. If both are equal, it returns 0. |
| concat()           | It returns **String** by concatenating two strings.                                           |
| contains()         | It returns **boolean** based on the given sequence of character present in string or not.     |
| equals()           | It returns **boolean** based on comparison of two strings.                                    |
| equalsIgnoreCase() | It returns **boolean** based on comparison of two strings but ignores the case.               |
| format()           | It returns **String** in specified format.                                                    |
| indexOf()          | It returns **int** that represents first the position characters and -1 if it is not present. |
| isEmpty()          | It returns **boolean** that shows whether the string is empty or not.                         |
| lastIndexOf()      | It returns **int** that shows the last occurrence of the characters.                          |
| length()           | It returns **int** that shows the size of the string.                                         |
| replace()          | It returns **String** where specified values with specified values.                           |
| split()            | It returns Array of String (**String[]**) that splits a string into an array of substrings.   |
</blockqoute> 
</details>

---

9.How will you convert `String` to `int`?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details>
<summary><b> Show Answer </b></summary>

- `parseInt()` is the static method in java from `Integer` class.
- It takes `String` and convert into `int`.
``` java
public class Main {
	public static void main(String[] args) {
		String s = "1234";
		int i = Integer.parseInt(s);
		System.out.println(i); // It will give int 1234
	}
}
```
</blockqoute> 
</details>
	
---

10.How will you convert `int` to `String`?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details>
    <summary><b> Show Answer </b></summary> 
<blockquote>

- `toString()` is the static method in java from `Integer` class.
- It takes `int` and convert into `String`.
``` java
public class Main {
	public static void main(String[] args) {
		int i = 1234;
		String s = Integer.toString(i);
		System.out.println(s); //It will give string 1234
	}
}
```
</blockqoute> 
</details>

---

11.How will you convert number into String of length 8 with leading zero?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
<details>
    <summary><b> Show Answer </b></summary> 
<blockquote>

- If we add leading zeros in the left side of `int` type, it will become octal number.
- We convert the number into String and add leading zeros.
- We can use `format()` static method from `String`.
``` java
public class Main {
	public static void main(String[] args) {
		int i = 1234;
		String s = String.format("%08d",i );
		System.out.println(s);  //00001234
	}
}
```
In the above code, we are specifying that how many digits that the number should have.
</blockqoute> 
</details>

---

12.How will you limit decimal precision point?
	
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
<details>
    <summary><b> Show Answer </b></summary> 
<blockquote>

We can limit the precision point using `format()` static method from `String`.
	
``` java
public class Main {
	public static void main(String[] args) {
		float f = 12.3456f;
		String s = String.format("%.2f",f );
		System.out.println(s);  //12.35
	}
}
```
>In the above code, we are specifying that how many digits should be there after decimal point.
</blockqoute> 
</details>
	
---
