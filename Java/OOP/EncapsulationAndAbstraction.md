## Technical Questions

1. Explain and Implement Encapsulation.

<details>

<summary><b>Show Answer</b> </summary>
    
> Encapsulation is creating a class with related fields and methods and hiding the fields and methods from the rest of the world, this can be achieved by creating fields and methods and private and accessing the fields and methods using objects.
  
  ``` java
  
  import java.util.Random;

public class ATM {
    
    static double balance = 10000;
    
    double debitAmmount(double ammount) {
        balance-=ammount;
        return balance;
    }
    
    private String generateOTP( ) {
        Random rnd = new Random();
        int number = rnd.nextInt(999999);
        return String.format("%06d", number);   
    }
    
    double creditAmmount( double ammount) {
        
        balance+=ammount;
        return balance;
    }
    double displayBalance()
    {
        return balance;
    }
    public static void main(String[] args) {
        ATM a = new ATM();
        System.out.println("Ammount credited and Final balance: "+ a.creditAmmount(1000));
        System.out.println("Ammount debited and Final balance:" + a.debitAmmount(100));
        System.out.println("Account Balance: "+ a.displayBalance());
        System.out.println(a.generateOTP());
        
    }

}
  
  
  ```
  
  > In the above code, the class ATM contains fields and methods, and they are encapsulated into the class, all the fields and methods can be accessed by an object 'a'.
    
  </details>
   </details>
   
 ---
   
2. What is Abstraction?

<details> <summary><b>Show Answer</b></summary>
    
> Data abstraction is the process of hiding certain details and showing only essential information to the user.
> In java Abstraction can be achieved in two ways   
> 1. By creating an abstract class with abstract methods. (0 to 100%)
> 2. By creating an interface with abstract methods.(100%)
> The abstract keyword is a non-access modifier, used for classes and methods.
> Abstraction lets you focus on what the object does instead of how it does it.



</details>

---

3. When to use abstract class and interface?

<details><summary><b>Show Answer</b></summary>
    
<b>Abstract Class: </b>

> 1. When classes are closely related and share the implementation an abstract class can be used. 
> 2. To create unrelated classes with the same methods and fields but with access modifiers other than public, i.e. private and protected.
> 3. to declare non-static and non-final methods, which can be altered by creating methods and using an object of the class.
    
<b>Interface: </b>

> 1. When classes are not related, they have the same methods but different implementations an interface is used.
> 2. when behaviour is specified but the implementation of the behaviour can be altered.
> 3. To implement Multiple Inheritance of value.

</details>

---

4. What are the advantages of encapsulation?

<details> <summary><b>Show Answer</b></summary>
    
| **#** | ** Abstract Class**                                                                          | ** Interface**                                                                     |
| ----- | -------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| 1     |  An abstract class can extend only one class or one abstract class at a time                 |  An interface can extend any number of interfaces at a time                        |
| 2     |   An abstract class can extend another concrete (regular) class or abstract class            |  An interface can only extend another interface                                    |
| 3     |  An abstract class can have both abstract and concrete methods                               |  An interface can have only abstract methods                                       |
| 4     |  In abstract class keyword “abstract” is mandatory to declare a method as an abstract        |  In an interface keyword “abstract” is optional to declare a method as an abstract |
| 5     |  An abstract class can have protected and public abstract methods                            |  An interface can have only have public abstract methods                           |
| 6     |  An abstract class can have static, final or static final variable with any access specifier |  interface can only have public static final (constant) variable                   |

</details>

---

5. What members are allowed in an abstract class?

<details> <summary><b>Show Answer</b></summary>
    
> 1. fields
> 2. Abstract Method
> 3. Non-Abstract Method.
> 4. Constructor 
> 5. main() method.

</details>

---

6. Which of the following is true when an abstract class implements an Interface?

- A. Abstract class must override all the methods of an interface
- B. Abstract class must override all the abstract methods of an Interface.
- C. The abstract class does not need to override all the methods of the interface.
- D. None of the above.

<details> <summary><b>Show Answer</b></summary>
C
<details><summary><b>Explanation</b></summary>

> normally when a class doesn't implement all the abstract methods of an interface it leads to a compilation error, this can be avoided by declaring the class abstract because an abstract method can have unimplemented methods. 
    
</details>

</details>

---

7. Is it possible to create an object for an abstract class?

<details> <summary><b>Show Answer</b></summary>
    
> No, the abstract class can not be initialized as it contains incomplete methods( abstract methods or methods with no implementation).
> One way to create an object for an abstract class is using an Anonymous inner class.

</details>

---




## Real-Time Application.

1. A vending machine has different items and functions to take the cash and dispense the item, but all these occur internally and as an external user one can only access it using selection buttons. this is an example for?

- A. Polymorphism
- B. Inheritance
- C. Encapsulation
- D. None of the above.

<details><summary><b>Show Answer</b></summary>

C
    
<details><summary><b>Explanation</b></summary>

> We can consider vending machine as class with dispensable items as fields and dispense operation as methods combined as a single unit.
    
</details>


</details>

## Error Detection

1. What is the output of the following code?

``` java
interface Car{
    void engine();
    void brake();
}

abstract public class Audi implements Car{
    
    public static void main(String[] args) {
        
    }

    @Override
    public void engine() {
        // code 
    }
}

```

- A.Compiletime error caused by the main method
- B.compliletime error caused by not implementing all the methods of the interface
- C.Runtime error
- D.No error

<details> <summary><b>Show Answer</b></summary>
    
> D

<details><summary><b>Explanation</b></summary>


> it is not mandatory for an abstract class to implement all the methods of an interface.
    
</details>



</details>






