## Control Flow Statements

1.What are control flow statements?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details>
    <summary><b> Show Answer </b></summary> 
<blockquote>

- The program flow goes from top to bottom. The control flow statetments are used to change the program flow.
- The control flow statements are classified by following
    -   Conditional Statements
    -   Uncoditional Statements
    -   Looping Statements
</blockqoute>  
</details>

---

2.What are Conditional Statements?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details>
    <summary><b> Show Answer </b></summary> 
<blockquote>
  
  - The control flow goes to the block based on the condition called as Conditional Statement.

</blockqoute>  
</details>

---

3.What will happen when if condition don't has else block?
	
![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details>
    <summary><b> Show Answer </b></summary> 
<blockquote>

> When the condition is true, it will execute the block. Otherwise it skips the code.
**Example**
  ```java

  public static int toPositive(int value) {
		if(value<0) {
			return -value;
		}
		return value;
	}
  ```
    The above code is used to change the negative value into positive value. If it is positive value, it will not do anything.
</blockqoute>  
</details>

---

4.What will happen when if condition has else if block?
	
![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details>
    <summary><b> Show Answer </b></summary> 
<blockquote>

While checking the condition, if it fails and we want to check the other condition then we will use if else.
  ```java
  public static int findPrice(int value) {
	int price ;
	if(value<100) {
		price = value;
	}
	else if(value<300) {
		price = value*2;
	}
	else {
		price = value*5;
	}
	return price;
	}
```
	
The above code is used to find the price based the range of value.
</blockqoute>  
</details>

---

5.How will you define nested if and give one example for it?
	
![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details>
    <summary><b> Show Answer </b></summary> 
<blockquote>

    
When we want to check the condition inside another condition, we can use nested if.

```java

	public static String findMonth(int english,int math,int science) {
		String result = null;
		if(english>=35) {
			if(math>=35) {
				if(science>=35) {
					result="Pass";
				}
			}
		}
		else {
			result="Fail";
		}
		return result;
	}
```
The above code is the example for finding the result. If any one condition fails, the else block will be executed.
</blockqoute>  
</details>
	
---

6.Where can we use switch statement?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details>
    <summary><b> Show Answer </b></summary> 
<blockquote>

 Switch statement is used to select one of code from many blocks of code. It selects the code based on the expression.
``` java
	public static String findDay(int n) {
		String day = null;
		switch(n) {
		case 1:
			day = "Monday";
			break;
		case 2:
			day = "Tuesday";
			break;
		case 3:
			day = "Wednesday";
			break;
		case 4:
			day = "Thurday";
			break;
		case 5:
			day = "Thurday";
			break;
		case 6:
			day = "Friday";
			break;
		case 7:
			day = "Saturday";
			break;
		default:
			day = "Wrong value";
			break;
		}
		return day;
	}
```
>The default is used when the input is wrong. The code is used to find the day in a week.
</blockquote>
</details>

---

7.Why do we use break after each cases in switch?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details>
    <summary><b> Show Answer </b></summary> 
<blockquote>

If we didn't use break or return, each cases of the switch will be executed which are present after that case.
</blockquote> 
</details>

 ---

8.How will you define looping statement?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details>
    <summary><b> Show Answer </b></summary> 
<blockquote>

Looping statements are used to do repeatative tasks. If one process has to done more than one, we will use looping statement. The three types of looping statements are,
  - for
  - while
  - do
</blockquote>
  </details>

  ---

9.Where will we use for loop?
	
![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details>
    <summary><b> Show Answer </b></summary> 
<blockquote>

- It is an entry controlled loop ie., the condition checked first.
- It contains three parts, initialization, condition, and increament or decreament.
- We can also use without any of these part.
- It is commonly used for arrays and collections.
</blockquote>
</details>
 
 ---

10.Where will we use while loop?
	
![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details>
    <summary><b> Show Answer </b></summary> 
<blockquote>

- It is an entry controlled loop ie., the condition checked first.
- It has only condition part.
- It will execute the block code untill the condition fails
</blockquote>
</details>

---

11.Can we use while loop instead of for loop?
	
![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details>
    <summary><b> Show Answer </b></summary> 
<blockquote>

Yes, we can use while loop instead of for loop where we have to initialize outside of the loop and increament or decreament inside the loop.
</blockqoute> 
</details>
	
---

12.Explain the difference between while and do while.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details>
    <summary><b> Show Answer </b></summary> 
<blockquote>

**while**
The condition is checked at the begining. If the condition is failed, the loop will not be executed.

**do while**
The condition is checked at the end. If the condition is failed, the loop will be executed one time.
</blockquote>
</details>

---

13.Explain the difference between break and continue.
	
![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details>
    <summary><b> Show Answer </b></summary> 
<blockquote>

**break**
A break statement results in the termination of the statement to which it applies for `switch`, `for`, `do`, or `while`.

**continue**
A continue statement is used to end the current loop iteration and return control to the loop statement.
</blockquote>
</details>

---

14: What will happen when we use return in a method?
	
![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details>
    <summary><b> Show Answer </b></summary> 
<blockquote>
	
It exits the current method. There are two types of return statements they are return with value when method has void return type and return without value.
</blockquote>
</details>

---

15: What will happen when we use return instead of break in loop?
	
![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details>
    <summary><b> Show Answer </b></summary> 
<blockquote>

**Using break**
>If we use break in loop, it will break the current loop. The other statements inside the method will be executed.
**Using return**
>If we use return in loop, it exits from the loop as well as the method.
</details>	  
</blockquote>
	
---
