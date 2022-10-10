1.Which block has to be followed after the try block?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b> Show Answer</b></summary>
	
>catch or finally block.
	
</details>

---

2.Why the rest of the code in the try block will not be execute?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
	
> Whenever an exception is occurred in the try block the rest of the code will not execute.
	
</details>

---

3.What is the syntax for the try-catch block? 	

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>
	
``` java
 try{

 }
 catch(Exceptionclass Exceptionobject){

 }
```
	
</blockquote>
</details>

---	

4.Can we have multiple catch blocks with the single try block?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b> Show Answer</b></summary>	
	
> yes, we can have multiple catch blocks with the single try block.
	
</details>


---

5.Who handles the exception if the exception is not handled by the programmer itself?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b> Show Answer</b></summary>
	
> Java Virtual Machine(JVM), handles the exception if the exception is not handled by the programmer itself.
	
</details>

---

6.What is the role of JVM in default Exception Handling mechanism?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
	
>JVM prints out the exception description,prints the stacktrace and causes the program to terminate.
	
</details>

---

7.How the normal flow of the program is maintained in the exception handling mechanism?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
	
> If the programmer handles the exception, the normal flow of the program is maintained in the exception handling mechanism.

</details>

---

8.Predict the output of the following code.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

 ``` java   
public class Example1 {    
  public static void main(String[] args) {    
     int a=10/0;   
        System.out.println("Exception Occurred");   
  }    
}
```
<details><summary><b> Show Answer</b></summary>
	
> /by zero
	
<details><summary><b> Explanation </b></summary>

> A number is divided by zero.
	
</details>
</details>

---

9.Predict the output of the following code.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

 ``` java   
public class TryCatchExample1 {  
  
    public static void main(String[] args) {  
        try  
        {  
        int b=5/0;  
        }  
        catch(ArithmeticException e)  
        {  
            System.out.println(e);  
        }  
        System.out.println("Exception Occurred");  
    }  
      
}  
```
<details><summary> <b> Show Answer</b></summary>

<blockquote>
	
```java
/by zero
Exception Occurred
```

</blockquote>
	
<details><summary><b> Explanation </b></summary>

> A number is divided by zero which throws an ArithmeticException.
	
</details>
</details>

---

10.Predict the output of the following code.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

 ``` java   
import java.util.*;
public class TryCatchExample3 {  
  
    public static void main(String[] args) {  
    Scanner sc = new Scanner(System.in);
    int number;
        try  
        {  	  
		System.out.println("Enter a number : ");
		number = Integer.parseInt(sc.next());
		System.out.println("You entered: "+number);
        }  
        catch(NumberFormatException e)  
        {  
            System.out.println(" NumberFormatException occurred");  
        }    
    }  
      
}  
```
<details><summary><b> Show Answer</b></summary>
	
> NumberFormatException occurred

<details><summary><b> Explanation </b></summary>

> If the input is not a number or if the input is string then NumberFormatException will be occurred otherwise it will print the number.
	
</details>
</details>

---

11.Predict the output of the following code.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

 ``` java   
public class TryCatchExample4 {  
    public static void main(String[] args) {  
        try  
        {  
        int c[]=new int[10];  
        c[22]=50;
        }  
        catch(ArrayIndexOutOfBoundsException e)  
        {  
            System.out.println("Array index error");  
        }    
    }  
      
}  
```
<details><summary><b> Show Answer</b></summary>
	
> Array index error

<details><summary><b> Explanation </b></summary>

>If the element is stored in unspecified array index then ArrayIndexOutOfBoundsException will be occurred.

</details>
</details>

---

12.Predict the output of the following code.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

 ``` java   
import java.io.*;
public class TryCatchExample5 {  
    public static void main(String[] args) {  
        PrintWriter p;  
        try {  
            p = new PrintWriter("abc.txt");  
            p.println("Exception Occurred");  
            }  
        catch (FileNotFoundException e) {      
            System.out.println("The File location is not found");  
        }         
    }  
}  
```
<details><summary><b> Show Answer</b></summary>
	
>The File location is not found
	
<details><summary><b> Explanation </b></summary>

>If the file does not exist then FileNotFoundException will be thrown.
	
</details>
</details>

---

13.How catch block is executed in multiple catch blocks?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
	
>All the catch blocks must be ordered from most specific to most generic i.e it should start from ArithmeticException class and then to the Exception class.
	
</details>

---

14.What is a nested try block?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
	
>The try block inside another try block is called as nested try block.When any try block does not have a catch block for a particular exception, then the catch block of the outer or parent  try block are checked for that exception, and if it matches, the catch block of outer try block is executed.
	
</details>

---

15.When should we use nested try block?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b> Show Answer</b></summary>
	
>A situation may arise where a part of block of code may cause one error and the entire block of code itself may cause another error. In such cases, exception handlers have to be nested.
	
</details>

---

16.Predict the output of the following code.

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

 ``` java   
public class NestedTryBlock1{    
 public static void main(String args[]){   
  try{    
    try{    
     System.out.println("Divide by zero error");    
     int b =50/0;    
   }  
    catch(ArithmeticException e)  
    {  
      System.out.println(e);  
    }    
    try{    
    int b[]=new int[10];    
     b[20]=40;    
     }  
    catch(ArrayIndexOutOfBoundsException e)  
    {  
       System.out.println(e);  
    }      
    System.out.println("other statement");    
  }  
  catch(Exception e)  
  {  
    System.out.println("handled the exception (outer catch)");  
  }     
  System.out.println("normal flow..");    
 }    
}  
```
<details><summary><b> Show Answer</b></summary>

<blockquote>
	
```java
Divide by zero error
/by zero
Index 10 out of bounds for length 10
```

</blockquote>
<details><summary><b> Explanation </b></summary>

> When any try block does not have a catch block for a particular exception, then the catch block of the outer (parent) try block are checked for that exception, and if it matches, the catch block of outer try block is executed.

</details>
</details>

---

17.What is a finally block?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
	
>In Java finally block is always executed whether an exception is handled or not. Therefore, it contains all the necessary statements that need to be printed regardless of the exception occurs or not.The finally block follows the try-catch block.
	
</details>

---

18.When a finally block gets executed?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
	
>When a Java program does not throw any exception a finally block gets executed.
	
</details>

---

19.Predict the output of the following code.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)


 ``` java   
public class Finallyblock1 {    
        public static void main(String args[]){    
             try{    
                     int data=50/10;    
                     System.out.println(data);    
                 }    
                 catch(ArithmeticException e){  
	                        System.out.println(e);  
	                }    
                    finally {  
                                	System.out.println("finally block is executed");  
	                        }     
                        }    
                }    
```
<details><summary><b> Show Answer</b></summary>
	
<blockquote>
	
```java
5
finally block is executed
```

</blockquote>

<details><summary><b> Explanation </b></summary>

> Even if the Exception is occurred or not,the finally block gets executed.
	
</details>
</details>

---

20.Predict the output of the following code.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

 ``` java   
public class FinallyBlock2{    
      public static void main(String args[]){   
      try {    
        System.out.println("Inside try block");  
       int data=10/0;      
      }   
      catch(ArithmeticException e){  
        System.out.println("Exception handled");  
        System.out.println(e);  
      }   
      finally {  
        System.out.println("finally block is  executed");  
      }      
      }    
    }  
```
<details><summary><b> Show Answer</b></summary>

<blockquote>
	
 ``` java  
Inside try block
Exception handled
/ by zero
finally block is executed
 ```
	
</blockquote>

<details><summary><b> Explantion </b></summary>
	
> Here the exception is occurred then also finally block gets executed.
	
</details>
</details>

---
