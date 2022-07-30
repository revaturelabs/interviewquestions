## Error Detection

1. Find the error in the following code?

``` java
public class Game {
	public static void main(String[] args) {
		Game g;
		g.playCricket();
		
		
	}
	void playCricket() {
		System.out.println("I am a Batsman");
	}

}

```

<details><summary>Show Answer</summary>

<b>Ans:</b> The above code creates a compile-time error, The object "g" is declared but not initialized, and It is not possible to use an object of a class without Initializing it.

</details>

2. What is the error in the following code snippet?

``` java
public class Child extends Parent, Grandparent{
	// code
}
```
<details><summary>Show Answer</summary>

<b>Ans:</b> compilation error is caused because a class can extend only one parent class.

</details>

3.  What is the error in the following code snippet?

``` java

private class Main{
	// code	
}

```

<details><summary>Show Answer</summary>

<b>Ans:</b> compilation error is caused because a class can be public, abstract and final but not private, unless its a nested class.

</details>

## Technical

1.Which of the following can be declared private?

- A. Class
- B. Interface
- C. Nested Class
- D. None of the above

<details><summary>Show Answer</summary>

<b>Ans:</b> C
	
<b>Explanation:</b> classes and interfces can not be declared private, nested classes can be declared private.

</details>

2.What are parameters and arguments?

- A. parameters: list of variables in method decleration.
     Arguments:  Values that are passed when a method is invoked.
- B. parameters: list of variables in method decleration.
     Arguments:  Values that are passed when a method is invoked.
     
<b>Ans:</b> A </details>

3.What is the implicit super class for all java classes.

- A. Arrays
- B. Collections
- C. Object
- D. None of the above

<details><summary>Show Answer</summary>

<b>Ans:</b> C
	
<b>Explanation:</b> The default constructor of any class with call the no arg constructor of the superclass, So, java provieds an implicit super class "Object" which has a default constructor.

</details>

4.









