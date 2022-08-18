1.Explain about StringBuilder?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details>
<summary><b> Show answer </b></summary>
<blockquote>

- StringBuilder is in `java.lang package`.
- StringBuilder is mutable strings that are stored in heap memory.
- StringBuilder is non-synchronized methods
- StringBuilder is not thread-safe, so the performance is more than StringBuffer.
</blockquote>
</details>

---

2.What are the advantages of using StringBuilder or StringBuffer over String?
	
![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details>
<summary><b> Show answer </b></summary>
<blockquote>

- As StringBuilders are mutable, we can change the values inbetween the string.
- The manipulation of strings is better because the reference of StringBuilder is not changed on this process.
- For storing and accessing the strings are prefered.
</blockquote>
</details>

---

3.How can we create StringBuilder object of any existing String?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details>
<summary><b> Show answer </b></summary>
<blockquote>

StringBuilder constructor accepts String object as shown bellow.

``` java
public class Main {
	public static void main(String[] args) {
		String s = "Hello";
		StringBuilder sb = new StringBuilder(s);
		System.out.println(sb);  //Hello
	}
}
```
We can pass the String on creation itself.
</blockquote>
</details>

---

4.How can we concatenate two String with StringBuilder? 
	
![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details>
<summary><b> Show answer </b></summary>
<blockquote>

We have to use the `append()` method to concatenate the value.

``` java
public class Main {
	public static void main(String[] args) {
		StringBuilder sb = new StringBuilder();
		sb.append("Hello");
		System.out.println(sb); 
	}
}
```
**Output**
```
Hello
```
The StringBuilder don't has value initially. So, the output is `Hello`.
</blockquote>
</details>

---

5.What is the difference between `insert()` and `append()`?
	
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
<details>
<summary><b> Show answer </b></summary>
<blockquote>

- The `append()` method inserts the value at the last position.
- The `insert()` method inserts the value at the specified position.
</blockquote>
</details>

---
