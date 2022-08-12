1: Explain about StringBuilder?
<details>
<summary><b> Show answer <b></summary>
<blockquote>

- StringBuilders are in `java.lang package`.
- StringBuilders are mutable strings that are stored in heap memory.
- StringBuilders are non-synchronized methods
- StringBuilder is not thread-safe, so the performance is more than StringBuffer.
</blockquote>
</details>

---

2. What are the advantages of using StringBuilders or StringBuffer?
<details>
<summary><b> Show answer <b></summary>
<blockquote>

- As StringBuilders are mutable, we can change the values inbetween the string.
- The manipulation of strings is better because the reference of StringBuilder is not changed on this process.
- For storing and accessing the strings are prefered.
</blockquote>
</details>

---

3. Can we pass string to StringBuilder to convert String into StringBuilder?
<details>
<summary><b> Show answer <b></summary>
<blockquote>

- Yes, we can pass the String while creating the object of StringBuilder.

``` java
public class Main {
	public static void main(String[] args) {
		String s = "Hello";
		StringBuilder sb = new StringBuilder(s);
		System.out.println(sb);  //Hello
	}
}
```
- We can pass the String on creation itself.
</blockquote>
</details>

---

4. Can we assign a value to StringBuilder using String literal?
<details>
<summary><b> Show answer <b></summary>
<blockquote>

- We can't directly assign a value to StringBuilder.
- We have to use the `append()` method to assign the value.

``` java
public class Main {
	public static void main(String[] args) {
		StringBuilder sb = new StringBuilder();
		sb.append("Hello");
		System.out.println(sb);  //Hello
	}
}
```
</blockquote>
</details>

---

5. What is the difference between `insert()` and `append()`?
<details>
<summary><b> Show answer <b></summary>
<blockquote>

- The `append()` method inserts the value at the last position.
- The `insert()` method inserts the value at the specified position.
</blockquote>
</details>

---