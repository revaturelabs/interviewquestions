# Technical

1. Do inner classes have access to private members of the outer class?

<details><summary>Show Answer</summary>

> Yes, inner classes have access to all the members of outer class that include private members of class.
</details>

2. What are the uses of nested classes?

- A. grouping interrelated classes.
- B. achieving encapsulation
- C. create code that is easy to read and maintain
- D. All of the above.

<details>
<summary><b>Show Answer</b><summary>
> D
	
	
</details>

3. What is Anonymous Inner class?

<details><summary><b>Show Answer</b></summary>

>Anonymous Inner class as the name clearly implies is a class inside a class without a name. A single object is created for anonymous inner class and its mostly used to override methods of a class or onterface for a single instance. Implementation of anonymous inner class is more concise than normal inner class.

</details>

4. What is Lambda?

<details><summary><b>Show Answer</b></summary>

> lambda is used to implemnet functional Interface( an interface with single abstract method), before lambda was interoduced, one as to use anonymous inner class to implement functional interfcae. lambda expressions made it simple, concise and redable.
</details>




5. When do we use Anonymous Inner class?

<details><summary><b>Show Answer</b></summary>

> Anonymous Inner classes are used to create a single instance of class or interfcae. it makes the code precise and consise.

</details>

6. Differentiate static nested class and Inner class?

<details><summary><b>Show Answer</b></summary>

| **Static Nested Class**                                                                                                                                   | **Inner Class**                                                                                              |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------ |
| A nested class which is declared static is called a static nested class                                                                                   | A nested class which is non-static is called an Inner class.                                                 |
| A static nested class can’t access the members of the enclosing class directly, an object reference is used to access the members of the enclosing class. | An inner class can directly access all the fields and methods of the enclosed class even if they are private |
</details>

7. What is the internal working of anonymous inner class and how is it different from normal inner class?
<details><summary><b>Show Answer</b></summary>

> Anonymous inner class is an inner class with single instance so an inner class is created by JVM with name "outerclass$number". 

</details>


8. What is the Internal working of lambda?
<details><summary><b>Show Answer</b></summary>

> lambda is not an inner class, when lambda expression is used a private private static class with an object return type and Object parameter is created to implement the functional interface.
> This is the reason why an anonymous class "Outer$1" is not crrated in case of lambda expression.

</details>

# problem-Solving
 1. What is the output of the following code?

 ``` java
 public class Main {
    public int i = 0;
    public static void main(String[] args) {
        Main m = new Main();
        Main.Nested mn = m. new Nested();
        mn.printVariable(10);   
    }
    class Nested{
        public int i = 2;
        void printVariable(int i)
        {
            System.out.print(i+" ");
            System.out.print(this.i+" ");
            System.out.print(Main.this.i+" ");
        }
    }   
}
```
- A. 0
     2
     10

- B. 10
     2
     0

- C. 0
     10
     2

- D. Compile-time error

<details><summary>Show Answer</summary>


> B

<details><summary><b>Explanation</b></summary>

> The first print statement accesses the agrument passed in the printVriable method, the second print statemnt accesss the intance variable of Nested class and the third print variable access the instance variable of the Main class( outer class).

</details>



</details>

2. What is the error int the following code?

``` java 
interface Shape{
	void area();
	void circuference();
}

public class Circle{
	
	Shape s = new Shape(){

		@Override
		public void area() {
			System.out.println("area of circle is 3.14*r*r");	
		}	
	};

}

```

<details><summary><b>Show Answer</b></summary>

>A compile time error is caused beacuse the anonymous inner class doesnt Implement all the methods of the interface Shape. The method circuference is not implemented. 

</details>

3. What is the output of following code?

``` java

interface Shape{
	void area();
	void circuference();
}

public class Circle{
	public static void main(String[] args) {
		Shape s = new Shape(){

			@Override
			public void area() {
				System.out.println("area of circle is 3.14*r*r");	
				
			}

			@Override
			public void circuference() {
				System.out.println("circunference of circle is 2*3.14*r");
			}
			
			static void printShape()
			{
				System.out.println("I am a Circle");
			}
		};
		
		
		
	}
	
}


```

<details><summary><b>Show Answer</b></summary>

>The code gets executed successfully, the anonymous inner class executes all the methods of the interface and the method printShape() is a new method created in anonymous class. Since anonymous inner class is a class it can implement its own methods.

</details>



4. what is the output of the following code?

``` java 
interface Shape{
	void area();
	void circuference();
}

public class Circle{
	public static void main(String[] args) {
		Shape s = new Shape(){

			@Override
			public void area() {
				System.out.println("area of circle is 3.14*r*r");	
			}

			@Override
			public void circuference() {
				System.out.println("circunference of circle is 2*3.14*r");
			}
			
			void printShape()
			{
				System.out.println("I am a Circle");
			}
		};
		
		s.printShape();
		
	}
	
}


```

<details><summary><b>Show Answer</b></summary>

>A compile time error is caused beacuse the anonymous inner class implements a new method called printShape(). and the method call is outside the scope of anonymous inner class.

</details>

5. What is the output of the following code?

``` java
public class Circle{
	
	static class SemiCircle{
		void printShape()
		{
			System.out.println("I am a Semi Circle");
		}
	}
	public static void main(String[] args) {
		Circle  c = new Circle();
		SemiCircle sc = new SemiCircle();
		sc.printShape();
		c.printShape();	
	}
	void printShape()
	{
		System.out.println("I am a circle");
	}
	
}



```

<details><summary><b>Show Answer</b></summary>

I am a Semi Circle
I am a circle

> The above code is an example for static inner class. Circle is outer class and SemiCircle is static nested class. the method printShape() is present in both Circle and SemiCircle and based on the method call the method is implemented.

</details>



## Senario Based

1. Apple launched a new iphone named iphone 14 with new features, and it has 3 modeles, iphone 14 basic, iphone 14 pro and  iphone 14 pro max and iphone 13 mini, which  implementation is better for this senario?

- A. an interface iphone with class iphone 14 and 4 classes for four models that inherit iphone 14.
- B. a class iphone 14 and inner class for each model.
- C. individulal classes for every model.
- D. none of the above.

<details><summary><b>Show Answer</b></summary>

B
<details><summary><b>Explanation</b></summary>

since all the iphone models are part of iphone14 they can be nested under the class iphone 14.
</details>
</details>


2. A DigitalThermometer needs to be configured only once and after that initial configuration, it'll detect the temperature perfectly. Which implementation is better for this senario?

- A. DigitalThermometer class which inherits and overrides the methods of Configuration Class.
- B. DigitalThermometer class which inherits and overrides the methods of Configuration interface.
- C. DigitalThermometer class which inherits and overrides the methods of Configuration interface using anonymous inner class.
- D. none of the above.


<details><summary><b>Show Answer</b></summary>

C

<details><summary><b>Explanation</b></summary>
DigitalThermometer(Class) , like any other machine should be configured before being used. Configuration(Interface ) has some procedure( methods) to configure a machine. any mechine is configured only once so we can use anonymous class to configure DigitalThermometer.

</details>
</details>


     





