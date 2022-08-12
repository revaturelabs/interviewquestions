1: What are strings?
<details>
<summary><b> Show Answer </b></summary>

- Strings are sequence of characters in java.
- StringBuffers are in `java.lang package`.
- Strings are immutable and are stored inside the string constant pool. 
- If we try to change the value of string, the string is rewritten and the reference changes.
</details>

---

2:What are the different ways to create a string in Java?
<details>
<summary><b> Show Answer </b></summary>

- There are two ways to create strings in java.
Using literal string, we can assign the value to a string with double quotes. The value is stored in a string constant pool.
**Example**
``` java
	String string = "Hello";
```
Using new keyword – It will create the new object in the heap memory
**Example**
``` java
	String string = new String("Hello");
```
</details>

---

3: What's the difference between == and .equals in Java? 
<details>
<summary><b> Show Answer </b></summary>

>Double equals (==) is an operator that compares the value and reference. Dot equals (.equals) is a method that checks the value only.
**Example**
	public class Main {
	    public static void main(String[] args) {
	        String str1 = "Hello";
	        String str2 = new String("Hello");
	        System.out.println(str1==str2);//false
	        System.out.println(str1.equals(str2));//true
	    }
	}
The first output statement will give output as false where the values are the same but the reference differs.
The second output statement will give output as true where the values are the same even after the reference differs.
</details>

---

4: Why Strings are immutable in java?
<details>
<summary><b> Show Answer </b></summary>

- When create a string using string literal, a memory allocated at the string constant pool a reference assign to variable. 
- If we create a string with the same value, the same reference will be stored to the variable instead of creating new memory.
- If we change any the value of the string, the entire string is rewritten and new reference is created.
- Hence, the strings are immutable.
</details>

---
5: What will happen if we use `new` keyword while craeting a string?
<details>
<summary><b> Show Answer </b></summary>

- When we `new` keyword while creating, the memory is allocated at heap. 
- If we again create a variable with the same value, a new memory is created in heap
- If we create without `new` keyword, it will be stored in String Constant Pool.
- If we create a string with the same value without `new`, the same reference will be stored to the variable instead of creating new memory. 

</details>

---

6: What is the difference between `next()` and `nextLine()`?
<details>
<summary><b> Show Answer </b></summary>

- `next()` will consider the spaces as seperation between each inputs.
- `nextLine()` will consider the line itself as a input with spaces.
</details>

---

7: How will you convert a sentence into words of String array?
<details>
<summary><b> Show Answer </b></summary>

- In java string has method `split` that returns array of strings which seperates the strings respected to the regex.
- It deletes the regex where regex can be letter, number or special character. The other substrings are stored in the string array.
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
</details>

8: Name some methods which are used for the string operations.
<details>
<summary><b> Show Answer </b></summary>

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
</details>

---

9: How will you convert String to int?
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
</details>

10: How will you convert int to String?
<details>
<summary><b> Show Answer </b></summary>

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
</details>

11: How will you add trailing zero to a number?
<details>
<summary><b> Show Answer </b></summary>

- If we add trailing zeros in the left side of `int` type, it will become octal number.
- We convert the number into String  and add trailing zeros.
``` java
public class Main {
	public static void main(String[] args) {
		int i = 1234;
		String s = String.format("%08d",i );
		System.out.println(s);  //00001234
	}
}
```
>In the above code, we are specifying that how many digits that the number should have.
</details>

---

11: How will you add trailing zero to a number?
<details>
<summary><b> Show Answer </b></summary>

- If we add trailing zeros in the left side of `int` type, it will become octal number.
- We convert the number into String and add trailing zeros.
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
>In the above code, we are specifying that how many digits that the number should have.
</details>

---

12: How will you limit decimal precision point?
<details>
<summary><b> Show Answer </b></summary>

> We can limit the precision point using `format()` static method from `String`.
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
</details>

---