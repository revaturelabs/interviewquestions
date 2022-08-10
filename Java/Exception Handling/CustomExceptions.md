## Custom Exceptions

1.What is use of Custom Exceptions?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
>  - When we create our own exceptions that are derived classes of the `Exception` class is known as custom exception or user-defined exception. 
>  - Custom exceptions are used to customize the exception according to the user needs.
  
</details>
</details>

---

2.Why we use custom exceptions?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
> - Custom Exception are used to catch and provide specific treatment to a subset of existing java exceptions.
> - We also have exceptions related to business logic and workflow. 
> - It is useful for the application users or the developers to understand the exact problem.
> - In order to create custom exception, we need to extend `Exception` class that belongs to <code>java.lang</code> package.

 </details>
</details>

---

3.Predict the output of the following code.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

 ``` java 
class InvalidAgeException  extends Exception  
{  
    public InvalidAgeException (String str)  
    {  
        super(str);  
    }  
}  
public class CustomException1  
{  
    static void valid(int age) throws InvalidAgeException{    
       if(age < 18){  
        throw new InvalidAgeException("An individual age is not eligible to vote");    
    }  
       else {   
        System.out.println("An individual is eligible to vote ");   
        }   
     }    
    public static void main(String args[])  
    {  
        try  
        {    
            valid(16);  
        }  
        catch (InvalidAgeException e)  
        {   
            System.out.println("Exception occured: " + e);  
        }   
    }  
}  
```
<details><summary><b> Show Answer</b></summary>
 
 ```java
Exception occured:InvalidAgeException:An individual age is not eligible to vote
 ```

<details><summary><b> Explanation</b></summary>
  
>constructor of InvalidAgeException takes a string as an argument. This string is passed to constructor of parent class Exception using the super() method. Also the constructor of Exception class can be called without using a parameter and calling super() method is not mandatory.
  
</details
</details>

---

4.Predict the output of  the following code.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

 ``` java 
class CustomException extends Exception {
 private int number;
 CustomException(int x) {
  number = x;
 }
 public String toString() {
  return "CustomException[" + number + "]";
 }
}
class CustomDemo {
 static void validate(int x) throws CustomException {
  System.out.println("Called validate(" + x + ")");
  if(x > 100)
   throw new CustomException(x);
  System.out.println("Normal exit");
}
public static void main(String args[]) {
 try {
  validate(55);
  validate(101);
 } catch (CustomException e) {
  System.out.println("Caught " + e);
 }
 }
}
```
<details><summary><b> Show Answer</b></summary>
 
```java
Called compute(55)
Normal exit
Called compute(101)
Caught MyException[101]
```

<details><summary><b> Explanation</b></summary>
  
>A subclass of Exception called CustomException is defined. This subclass
is quite simple: it has only a constructor plus an overloaded `toString( )` method that
displays the value of the exception. The CustomDemo class defines a method
named `validate( )` that throws a CustomException object. The exception is thrown when
`validate( )` integer parameter is greater than 100. The `main( )` method sets up an
exception handler for CustomException, then calls `validate( )`  with a legal value (less
than 100) and an illegal one to show both paths through the code.
  
</details>
</details>

---

