1.Explain `throw` statement?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

	
>The `throw` statement is used to throw an exception explicitly. We specify the exception object which is to be thrown. The Exception has some message with it that provides the error description. These exceptions may be related to user inputs, server, etc.We can throw either checked or unchecked exceptions in Java by throw keyword. 
	
</details>
	
---
	
2.What is the syntax of `throw` statement?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
	
> `throw new exceptionclass("error message");`
	
</details>
	
---
	
3.Predict the output of the following code.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

 ``` java   
public class throw1 {   
    public static void verify(int age) {  
        if(age<18) {  
            throw new ArithmeticException(" An individual is not eligible to vote ");    
        }  
        else {  
            System.out.println(" An individual is eligible to vote ");  
        }  
    }  
    public static void main(String args[]){  
        verify(10);  
  }    
}    
```
<details><summary><b> Show Answer</b></summary>
	
>An individual is not eligible to vote.

<details><summary><b> Explanation</b></summary>

>The age passed is less than 18 in the verify method that is why it throws an arithmetic exception.

</details>
	
</details>

---

4.Predict the output of the following code.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

 ``` java   
import java.io.*;   
public class throw2 {   
    public static void method1() throws FileNotFoundException {  
        FileReader f = new FileReader("C:\Users\Revature\Desktop\xyz.txt");  
        BufferedReader br = new BufferedReader(f);  
  	 throw new FileNotFoundException();    
    }  
    public static void main(String args[]){  
        try  
        {  
            method1();  
        }   
        catch (FileNotFoundException e)   
        {  
            e.printStackTrace();  
        }  
  }    
}    
```
<details><summary><b> Show Answer</b></summary>
	
>`java.io.FileNotFoundException`

<details><summary><b> Explanation</b></summary>

>The file doesn't exist in the location specified and it throws a FileNotFoundException.

</details>
	
</details>

---

5.What is a `throws` statement?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b> Show Answer</b></summary>
	
>`Throws` keyword is used to declare an exception. It gives an information to the programmer that there may occur an exception.It provides information to the caller of the method about the exception.  
	
</details>

---

6.What is the syntax of `throws` statement?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b> Show Answer</b></summary>

```java
return_type method_name() throws exception_class_name{  
//method code  
}   
```
	
</details>

---

7.Predict the output of the following code.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

 ``` java   
import java.io.*;  
class throws1{  
 void method1()throws IOException{  
  throw new IOException("IO Error");  
 }  
}  
public class throws2{  
   public static void main(String args[]){  
    try{  
    throws1 t=new throws1();  
     t.method1();  
    }
catch(Exception e){
System.out.println("exception handled");
	}     
  }  
}  
```
<details><summary><b> Show Answer</b></summary>
	
>exception handled

<details><summary><b> Explanation</b></summary>

>The Input Output resource is not available it throws an IOException.

</details>
</details>


---


8.Differentiate `throw` Vs `throws` statement.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
	
>`throw` Vs `throws`
	
<details><summary><b> Explanation</b></summary>
	
>- Throw keyword is used to throw an exception explicitly in the code, inside the function or the block of code.we can only propagate unchecked exception i.e., the checked exception cannot be propagated using throw only.The throw keyword is followed by an instance of Exception to be thrown.It is used within the method.We are allowed to throw only one exception at a time i.e. we cannot throw multiple exceptions.
>- Throws keyword is used in the method signature to declare an exception which might be thrown by the function while the execution of the code.we can declare both checked and unchecked exceptions. However, the throws keyword can be used to propagate checked exceptions only.It is followed by class names of Exceptions to be thrown.Throws is used with the method signature. We can declare multiple exceptions using throws keyword that can be thrown by the method. For example, main() throws IOException, SQLException.
	
</details>
</details>

---

9.Predict the output of the following code.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

 ``` java   
public class Throw1{  
    public static void calsquare(int n) {  
        if (num < 1) {  
            throw new ArithmeticException("\n Number is negative, cannot calculate square");  
        }  
        else {  
            System.out.println("Square of " + n + " is " + (n*n));  
        }  
    }    
    public static void main(String[] args) {  
            Throw1 obj = new Throw1();  
            obj.calsquare(-2);  
    }  
}  
```
<details><summary><b> Show Answer</b></summary>
	
>Number is negative, cannot calculate square.
	
<details><summary><b> Explanation</b></summary>

>The negative number has been passed to the calsquare method it throws an ArithmeticException.

</details>
	
</details>


---

10.Predict the output of the following code.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

 ``` java   
public class Throws2 {   
    public static int divide(int x, int y) throws ArithmeticException {  
        int z = x / y;  
        return z;  
    }  
    public static void main(String[] args) {  
        Throws2 t = new Throws2();  
        try {  
            System.out.println(t.divide(50, 0));  
        }  
        catch (ArithmeticException e){  
            System.out.println("\n Number cannot be divided by 0");  
        }  
 
    }  
}  
```
<details><summary><b> Show Answer</b></summary>
	
>Number cannot be divided by 0.

<details><summary><b> Explanation</b></summary>

>The number 0 has been passed to the divide method as a second argument it throws an ArithmeticException.

</details>
</details>

---

11.Differentiate `final`,`finally` and `finalize` statements.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>
	
>- `final` is the keyword and it is an access modifier which is used to apply restrictions on a class, method or variable.final variable becomes constant and cannot be modified once it is declared.It cannot be overridden by sub class.final class cannot be inherited.It is executed only when we call it.
>- `finally` is the block in Exception Handling to execute the important code whether the exception occurs or not.It is always related to the try and catch block in exception handling.finally block cleans up all the resources used in try block.It is executed as soon as the try-catch block is executed.It's execution is not dependant on the exception.
>- `finalize` is the method in Java which is used to perform clean up processing for the object which is garbage collected.finalize() method is used with the objects.It performs the cleaning activities with respect to the object before its destruction.It is executed just before the object is destroyed.
	
</details>

---

12.Predict the output of the following code.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

 ``` java   
public class finalvariable {   
    final int age = 10;  
    void display() {  
    age = 15;  
    }      
    public static void main(String[] args) {  
    finalvariable f = new finalvariable();  
    f.display();  
    }  
}  
```
<details><summary><b> Show Answer</b></summary>
	
>`Cannot assign a value to the final variable age=15`
	
<details><summary><b> Explanation</b></summary>

>The final variable cannot be re-initialized again.

</details>
	
</details>

---

13.Predict the output of the following code.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

  ``` java   
 public class finally1{    
      public static void main(String args[]){   
      try {    
        System.out.println("Inside try block");  
       int data=5/0;    
       System.out.println(data);    
      }   
      catch (ArithmeticException e){  
        System.out.println("Exception handled");  
        System.out.println(e);  
      }   
      finally {  
        System.out.println("finally block is executed");  
      }     
      }    
    }  
 ```   
<details><summary><b> Show Answer</b></summary>
	
>Inside try block Exception handled / by zero finally block is executed.

<details><summary><b> Explanation</b></summary>

>The finally block gets executed if the exception is occurred or not.

</details>
</details>

---

14.Predict the output of the following code.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

 ``` java 
 public class finalize1 {    
     public static void main(String[] args){     
        finalize1 obj = new finalize1();         
        System.out.println("Hashcode is: " + obj.hashCode());           
        obj = null;      
        System.gc();     
        System.out.println("garbage collection ended");     
    }     
    protected void finalize()     
    {     
        System.out.println("The finalize() method called");     
    }     
}    
 ``` 
<details><summary><b> Show Answer</b></summary>

<blockquote>
	
```java
Hashcode is:3456787673
garbage collection ended
The finalize() method called
```

</blockquote>
	
<details><summary><b> Explanation</b></summary>

>`finalize` method is executed just before the object obj is destroyed.

</details>
</details>

---

15.Explain Exception Propagation.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
	
>An exception is first thrown from the top of the stack and if it is not caught, it drops down the call stack to the previous method. If not caught there, the exception again drops down to the previous method, and so on until they are caught or until they reach the very bottom of the call stack. This is called exception propagation.
	
</details>
</details>

---

16.Predict the output of the following code.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

 ``` java 
 class Propagation1{  
  void method1(){  
    int data=20/0;  
  }  
  void method2(){  
    method1();  
  }  
  void method3(){  
   try{  
    method2();  
   }catch(Exception e){
	System.out.println("exception handled");}  
  }  
  public static void main(String args[]){  
   Propagation1 obj=new Propagation1();  
   obj.method3();  
   System.out.println("normal flow...");  
  }  
}  
```
<details><summary><b> Show Answer</b></summary>
	
>exception handled normal flow

<details><summary><b> Explanation</b></summary>

>Exception occurs in the method1() method where it is not handled, so it is propagated to the previous method2() method where it is not handled, again it is propagated to the method3() method where exception is handled.
	
</details>
</details>

---

17.Explain Exception Handling with Method Overriding.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>	
	
>- If the superclass method does not declare an exception, subclass overridden method cannot declare the checked exception but it can declare unchecked exception.
>- If the superclass method declares an exception, subclass overridden method can declare same, subclass exception or no exception but cannot declare parent exception.
	
</details>
</details>

---

18.Predict the output of the following code.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

 ``` java 
import java.io.*;    
class Message{   
  void msg() {  
    System.out.println("Exception in parent method");  
    }    
}    
    
public class ExceptionChild extends Message{     
  void msg() throws IOException {    
    System.out.println("Exception in Child method");    
  }  
  public static void main(String args[]) {    
   Message m = new ExceptionChild();    
   m.msg();    
  }    
}   
```
<details><summary><b> Show Answer</b></summary>
	
```java
msg() in ExceptionChild cannot override msg() in Message
```
<details><summary><b> Explanation</b></summary>

>Method overriding is not done by the derived class method msg() to the parent class method msg() when it throws a checked exception i.e IOException in exception handling.

</details>
</details>

---

19.Predict the output of the following code.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

``` java 
import java.io.*;    
class Parent{    
  void msg() {  
    System.out.println("parent method");  
  }    
}    
    
class Child1 extends Parent{    
  void msg()throws ArithmeticException {    
    System.out.println("child method");    
  }    
  
  public static void main(String args[]) {    
   Parent p =  new Child1();    
   p.msg();    
  }    
}   
```
<details><summary><b> Show Answer</b></summary>
	
>child method

<details><summary><b> Explanation</b></summary>

>Method overriding can be  done by the derived class method msg() to the parent class method msg() when it throws a unchecked exception i.e ArithmeticException in exception handling.

</details>
</details>

---
