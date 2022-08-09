## Techical Questions

1. Explain and Implement Encapsulation.

<details>

<summary><b>Show Answer</b> </summary>
	
> Encapsulation is the creating a class with realted feilds and methods and hiding the feilds and methods from the rest of the world, this can be achived by creating feilds and methods and private and accesing the feilds and methods using objects.
  
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
  
  > In the above code, the class ATM contains feilds and methods, and they are encapsulated into the class, all the feilds and methods can be accessed by an object 'a'.
    
  </details>
   </details>
   
 ---
   
2. What is Abstraction?

<details> <summary><b>Show Answer</b></summary>
	
> Abstraction is hiding the feilds and methods of a class or interface by extending or implementing them using a different class.
> In java Abstraction can be achieved in two ways	
> 1. By creating an abstract class with abstract methods.
> 2. By creating an interface with abstract methods.

</details>

---

3. When to use abstract class and interface?

<details><summary><b>Show Answer</b></summary>
	
<b>Abstract Class: </b>

> 1. When classes are closely related and share the implementation an abstract class can be used. 
> 2. To create unrelated classes with same methods and fields but with access modifiers other than public, i.e. private and protected.
> 3. to declare non static and non final methods, which can be altered by creating methods and using an object of the class.
	
<b>Interface: </b>

> 1. When classes are not related, they have same methods but different imolementations an interface is used.
> 2. when behavior is specified but the implementation of the behavior can be altered.
> 3. To implement Multiple Inheritance of value.

</details>

---

4. What are the advatages of encapsulation?

<details> <summary><b>Show Answer</b></summary>
	
> 1. Encapsulation is used to implement data binding and data hinding.
> 2. Encapsulation allows code reusability.
> 3. It is used to maintain data security by restricting the access to only the non private members of the class.

</details>

---

5. What are the members of an abstract class?

<details> <summary><b>Show Answer</b></summary>
	
> 1. feilds
> 2. Absatract Method
> 3. Non Abstract Mtehod.
> 4. Constructor 
> 5. main() method.

</details>

---

6. Which of the following is true when an abstract class implements an Interface?

- A. Abstract class must override all the methods of an interface
- B. Abstract class must override all the abstract methods of an Interface.
- C. It is not mandatory for the abstract class to override all the methods of the interface.
- D. None of the above.

<details> <summary><b>Show Answer</b></summary>
C
<details><summary><b>Explanation</b></summary>

> normally when a class doesnt implement all the abstract methods of an interface it leads to an compilation error, this can be avoided by declaring the class abstract, because and abstract method can have unimplemented methods. 
	
</details>

</details>

---

7. Is it posssible to create an object for abstract class?

<details> <summary><b>Show Answer</b></summary>
	
> No, abstract class can not be initialized as it contains incomplete methods( abstract methods or methods with no imolementation).
> One way to create an object for an abstract class is use an Anonymous inner class.

</details>

---




## Real-Time Application.

1. A vending machine different items and functions to take the cash and dispense the item, but all these occur internally and as an external user one can only access it using selection buttons. this is an example for?

- A. Polymorphism
- B. Inheritance
- C. Encapsulation
- D. None of the above.

<details><summary><b>Show Answer</b></summary>

C
	
<details><summary><b>Explanation</b></summary>

> Vending machine is a class with items as feilds and fuctions as methods combined into a single unit.
	
</details>


</details>

## Error Detection

1. Class Extending abstract class but not implementing all abstrcat methods.


<details> <summary><b>Show Answer</b></summary>
	
> 

</details>






