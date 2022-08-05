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
   
 2. What is Abstraction?

<details> <summary><b>Show Answer</b></summary>
	
> Abstraction is hiding the feilds and methods of a class or interface by extending or implementing them using a different class.
> In java Abstraction can be achieved in two ways	
> 1. By creating an abstract class with abstract methods.
> 2. By creating an interface with abstract methods.

</details>

## Error Detection

