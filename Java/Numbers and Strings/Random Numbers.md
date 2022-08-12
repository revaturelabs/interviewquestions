1: How can we generate random numbers in java?
<details>
<summary><b> Show answer <b></summary>

- We generate random numbers using `Random` class that presents in `java.util` package.
- `Random` class has the methods to generate random number in int, double, float, long etc.
-  We can give range to random number or we can give the upper bound number.
-  We didn't give the boundry, it will generate the random number between its maximum value and minimum value of the datatype.
**Example**
``` java
import java.util.Random;

public class Main {
	public static void main(String[] args) {
		Random random = new Random();
		double d = random.nextDouble(1000.8); // The value generated upto 1000.8
		int i = random.nextInt(100,10000);    // The value range in between 100 to 10000
	}
}
```
> The value differs each time when we run it.
</details>

---

2: Which is the best inbetween `Math.random()` and `Random` class method `nextDouble()`?
<details>
<summary><b> Show answer <b></summary>

>`Math.random()` will give the random number in `double` datatype which uses `nextDouble()` from `Random` class. So, both the methods will give the same value.

---

