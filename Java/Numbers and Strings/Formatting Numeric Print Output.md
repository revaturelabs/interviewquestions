## Formatting Numeric Print Output

1.Find the output of the code.
``` java

public class Main {
	public static void main(String[] args) {
		int num1=11;
		int num2=011;
		System.out.println(num1 == num2);
	}
}
```

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)
<details>
<summary><b> Show Answer </b></summary>

`false`
<details>
<summary><b> Explanation </b></summary>
<blockquote>
	
- If we add zero before a number, the value will become octal number. 
- The octal number is converted into decimal value and assigned to `int` variable.
- The value of `num1` is `11` and value of `num2` is `9` that are not equal. The output is `false`.
</blockqoute> 
</details>
</details>

---

2.How decimal, octal, hexa decimal and binary value are assigned to `int` varaible?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
<details>
    <summary><b> Show Answer </b></summary> 
<blockquote>

``` java
public class Main {
	public static void main(String[] args) {
		int decimal = 100;      // for decimal number, no prefixes needed
		int octal = 0144;       // for octal number, 0 should be added
		int binary = 0b1100100; // for binary number, 0b should be added
		int hexaDecimal = 0x64; // for hexaDecimal number, 0x should be added
	}
}
```
>All the above int values represent `100` in different forms.
</blockqoute> 
</details>

---

3.Why is `f` added after the `float` value while using precision?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)
<details>
    <summary><b> Show Answer </b></summary> 
<blockquote>

When we have decimal value with precision that we will double by default. To specify that the value is `float` then we need to post-fix the value with `f`.
``` java
public class Main {
	public static void main(String[] args) {
		float f1 = 100.67;	//Error
		float f1 = 100.67f;	//No Error
		double d = 10.999;	//No Error
		System.out.format("%03d",decimal);
	}
}
```
</blockqoute> 
</details>

---
