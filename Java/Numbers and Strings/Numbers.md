## Numbers

1: How to find the maximum and minimum value of a datatype?
<details>
<summary><b> Show Answer </b></summary>

- To find the maximum value of a data type, we have to use the corresponding wrapper class and their staic variable `MAX_VALUE`.
- For minivalue, we can use `MIN_VALUE`.
**Eaxmple**
``` java
public class Main {
	public static void main(String[] args) {
		int i = Integer.MAX_VALUE;
		System.out.println(i);
	}
}
```
The output for the code line is given by,
```
2147483647
```
>It gives the maximum value of `int` datatype.
</details>

---

2:  Explain about type casting.
<details>
<summary><b> Show Answer </b></summary>

- Type casting is the process changing from primitive datatype to another type.
- There are two types of type casting
    - Widening Casting
    - Norrowing Casting
</details>

---

3:  Explain about Widening casting.
<details>
<summary><b> Show Answer </b></summary>

- Widening casting also called implicit type casting is the process changing from smaller datatype to larger datatype.
- The convertion is done automatically.
**Example**
``` java
public class Main {
	public static void main(String[] args) {
	    int i = 9;
	    float f = i;
	    System.out.println(f); //9.0
	}
}

```
- In the above example, the variable `f` is assigned as `i` where the value is `9`. Now the value of `f` is `9.0`. Here the `int` value is automatically converted into `float`.
</details>

---

4:  Explain about Narrowing casting.
<details>
<summary><b> Show Answer </b></summary>

- Narrowing casting also called explicit type casting is the process changing from larger datatype to smaller datatype.
- The convertion is done manually. We have specify the datatype.
**Example**
``` java
public class Main {
	public static void main(String[] args) {
	    float f = 9.84f;
	    int i = (int)f;
	    System.out.println(i);  //9
	}
}
```
- In the above example, the variable `i` is assigned as `f` where the value is `9.84`. Now the value of `i` is `9`. Here the `float` value is manually converted into `int`. We have to specify the name manually.
</details>

---

5: Can we convert `char` to `int` with exact numeric value of `char`?
<details>
<summary><b> Show Answer </b></summary>

> Yes, we can convert `char` to `int` with exact numeric value using wrapper class.
``` java
public class Main {
	public static void main(String[] args) {
		char c = '9'; 
		int i = Character.getNumericValue(c);
		System.out.println(i); //9
	}
}
```
- In the above code, the method `Character.getNumericValue(c)` gets the numeric value.
</details>

---

6: Why don't we create object to use `getNumericValue()`?
<details>
<summary><b> Show Answer </b></summary>

> `getNumericValue` is a static method of `Character` wrapper class. For static methods, we don't object need objects to access it.
</details>

7:  How will you assign the number from `char` to `int` without using wrapper classes in java?
<details>
<summary><b> Show Answer </b></summary>

  - If we directly assign the value of `char` to `int`, it will assign the ascii value. Therefore we have subract `48` to get the integer value.
    **Example**
    ``` java
    public class Main {
	public static void main(String[] args) {
		char c = '9'; 
		int i = c - 48; // ascii value of 9 is 57.
		System.out.println(i); // 9
	}
    }
    ```
    - In the above code, the value of c is automatcally converted into `57` integer value that is ascii value.
    - Then the subtraction is done to get `9`.
  
  
</details>

