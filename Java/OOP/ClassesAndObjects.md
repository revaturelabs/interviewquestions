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

4.What are the benifits of using Objects?

<details><summary>Show Answer</summary>
	<b>Ans:</b>
	
	- Modularity: the source code for every object can be maintained independently and once an object is created it can be easily propagated inside the system.
	- Information-hiding: since an object is used to implement methods, the internal working of the class can be hidden using an object.
	- Code - reusability:  once an object is created, it can be reused anywhere in the program.
	- Pluggability and debugging: if an existing object fails to staisfy the requiremts of the developer or causes any abnormality in the code, it can be 
	  deleted.
	
</details>

5. Variables declared in an interface are?

- A. public,static and final
- B. private and final
- C. public and final
- D. Default or public, static.


<details><summary>Show answer</summary>

	<b>Ans:</b> A
	<b>Explanation:</b>
	- final: variables in an interface are accessed by many classes and its not ideal, if any of the classes appends the value of the variable, to avoid this
	         variables are declared final.
	- public: interfaces are accessed by any class present in any package, so to support this all variables are declared public.
	- static: interface itself cant be initialized, so objects of a class are used to access variables, but if a class is imcomplete, an object cant be created.
	          All variables are static so that they can be accessed without an object.
	

</details>

6. choose the right answer.

1. local class                                  a. used to create more than one instance of a class, 
2. Anonymous class
3. lambda expression
4. Nested class
	
	











