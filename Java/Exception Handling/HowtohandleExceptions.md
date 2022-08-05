1:Which block has to be followed after the try block
<details><summary> <b> Show Answer</b>/summary>
catch or finally block.
</details>

2:Why the rest of the code in the try block will not execute.
<details><summary><b> Show Answer</b></summary>
whenever an exception is occurred in the try block the rest of the code will not execute.
</details>

3:What is the Syntax for the try-catch block? 
	
<details><summary><b> Show Answer</b></summary>
	
``` java
 try{

 }
 catch(Exceptionclass Exceptionobject){

 }
```
</details>
	

4:Can we have multiple catch blocks with the single try block.
	
<details><summary> <b> Show Answer</b></summary>
	
yes
</details>

5:Who handles the exception if the exception is not handled by the programmer itself.
<details><summary> <b> Show Answer</b></summary>
Java Virtual Machine(JVM).
</details>

6:What is the role of JVM in default ExceptionHandling mechanism.
<details><summary><b> Show Answer</b></summary>
<code>
Prints out the exception description
Prints the StackTrace
Causes the program to terminate.
</code>
</details>

7:How the normal flow of the program is maintained in the exception handling mechanism.
<details><summary><b> Show Answer</b></summary>
if the programmer handles the exception.
</details>

8:Predict the output of the following code.
 ``` java   
public class Example1 {    
  public static void main(String[] args) {    
     int a=10/0;   
        System.out.println("Exception Occurred");   
  }    
}
```
<details><summary><b> Show Answer</b></summary>
/by zero
</details>

9:Predict the output of the following code.
 ``` java   
public class trycatchexample1 {  
  
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
/by zero
Exception Occurred
</details>

10:Predict the output of the following code.
 ``` java   
public class trycatchexample3 {  
  
    public static void main(String[] args) {  
        try  
        {  
        int c=25/0;  
        }  
        catch(ArithmeticException e)  
        {  
            System.out.println("A number cannot be divided  by zero");  
        }    
    }  
      
}  
```
<details><summary><b> Show Answer</b></summary>
A number cannot be divided  by zero
</details>

11:Predict the output of the following code.
 ``` java   
public class trycatchexample4 {  
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
Array index error
</details>

12:Predict the output of the following code.
 ``` java   
import java.io.*;
public class trycatchexample5 {  
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
The File location is not found
</details>

13:How catch block is executed in multiple catch blocks?
<details><summary><b> Show Answer</b></summary>
All the catch blocks must be ordered from most specific to most generic i.e it should start from ArithmeticException class and then to the Exception class.
</details>

14:What is a nested try  block?
<details><summary><b> Show Answer</b></summary>
the try block inside another try block is called as nested try block.
</details>

15:When should we use nested try  block?
<details><summary> <b> Show Answer</b></summary>
A situation may arise where a part of  block of code may cause one error and the entire block of code itself may cause another error. In such cases, exception handlers have to be nested.
</details>

16: Predict the output of the following code.
 ``` java   
public class nestedtryblock1{    
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
<code>
Divide by zero error
/by zero
Index 10 out of bounds for length 10
</code>
</details>

17:What is a finally  block?
<details><summary><b> Show Answer</b></summary>
Java finally block is always executed whether an exception is handled or not. Therefore, it contains all the necessary statements that need to be printed regardless of the exception occurs or not.The finally block follows the try-catch block.
</details>

18:When a finally block gets executed?
<details><summary><b> Show Answer</b></summary>
When a Java program does not throw any exception a finally block gets  executed.
</details>

19: Predict the output of the following code.
 ``` java   
class finallyblock1 {    
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
<code> 5
finally block is executed
</code>
</details>

20: Predict the output of the following code.
 ``` java   
public class finallyblock2{    
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
<code>
Inside try block
Exception handled
/ by zero
finally block is executed
</code>
</details>
