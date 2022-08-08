## Control Flow Statements

1: What are control flow statements?
 <details>
      <summary><b> Show Answer </b></summary> 

- The program flow goes from top to bottom. The control flow statetments are used to change the program flow.
- The control flow ststements are classified by following
    -   Conditional Statements
    -   Uncoditional Statements
    -   Looping Statements
  </details>

---

2: What are Conditional Statements?
 <details>
      <summary><b> Show Answer </b></summary> 
  
  - The control flow goes to the block based on the condition called as Conditional Statement.

  </details>

---

3: What will happen when if condition don't has else block?
 <details>
      <summary><b> Show Answer </b></summary> 

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
  </details>

---

4: What will happen when if condition has else if block?
 <details>
      <summary><b> Show Answer </b></summary> 

> While checking the condition, it fails and we want to check the other condition then we will use if else.
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
> The above code is used to find the price based the range of value.

</details>

---

5: How will you define nested if and give one example for it?
 <details>
      <summary><b> Show Answer </b></summary> 
    
> When we want to check the condition inside another condition, we can use nested if.

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
 > The above code is the example for finding the result. If any one condition fails, the else block will be executed.
</details>

---

6: Where can we use switch statement?
 <details>
      <summary><b> Show Answer </b></summary> 

  >Switch statement is used to select one of code from many blocks of code. It selects the code based on the expression.
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

</details>

---

7: Why do we use break after each cases in switch?
 <details>
      <summary><b> Show Answer </b></summary> 

>If we didn't use break or return, each cases of the switch will be executed which are present after that case.
  </details>

 ---

8: How will you define looping statement?
 <details>
      <summary><b> Show Answer </b></summary> 

>Looping statements are used to do repeatative tasks. If one process has to done more than one, we will use looping statement. The three types of looping statements are,
  -	for
  - while
  - do
  </details>

  ---

9: Where will we use for loop?
 <details>
      <summary><b> Show Answer </b></summary> 

>When we know the initialization of iteration value and the number of iterations, we can use for loop.
</details>
 
 ---

10: Where will we use while loop?
 <details>
      <summary><b> Show Answer </b></summary> 

>When we don't know the initialization of iteration value and numberof iterations, we will use while loop.
</details>

---

11: Can we use while loop instead of for loop
 <details>
      <summary><b> Show Answer </b></summary> 

>Yes, we can use while loop instead of for loop where we have to initialize outside of the loop.
</details>

12: Explain the difference between while and do while.
 <details>
      <summary><b> Show Answer </b></summary> 

**while**
>The condition is checked at the begining. If the condition is failed, the loop will not be executed.

**do while**
>The condition is checked at the end. If the condition is failed, the loop will be executed one time.
</details>

---

13: Explain the difference between break and continue.
 <details>
      <summary><b> Show Answer </b></summary> 

**break**
>It stops the current loop. It stops the loop irrespective of how many loops are remaining.

**continue**
>It skips the iteration loop. It skips the code which presents after continue.
</details>

---

14: What will happen when we use return in a method?
 <details>
      <summary><b> Show Answer </b></summary> 

>It exits the current method. There are two types of return statements they are return with value and return without value.
</details>	

---

15: What will happen when we use return instead of break in loop?
 <details>
      <summary><b> Show Answer </b></summary> 

**Using break**
>If we use break in loop, it will break the current loop. The other statements inside the method will be executed.
**Using return**
>If we use return in loop, it exits from the loop as well as the method.
</details>	  
---
