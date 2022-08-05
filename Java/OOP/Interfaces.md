## Technical

1. Which access modifier is used to override the method of an Interface?

- A.public
- B.private
- C.protected
- D.default

<details>
<summary><b>Show Answer</b></summary>

A
  
<details>
  
<summary>Explanation</summary>
  
> All the methods in an interface are public by default and It is not possible to alter the access modifier while overriding the method.
    
</details>
  
</details>

---

2. What is Marker Interface?

<details>
  <summary><b>Show Answer</b></summary>

 A
 <details>
  <summary>Explanation</summary> 
    
>	Marker Interfaces are empty Interfaces (no fields or methods).
> Marker interfaces are used to pass the information to JVM that a certain object of a class can implement methods like Serializable, Cloneable etc.

  </details>
</details>

---

3. Is it possible to create an Object for Interface?

<details>
<summary><b>Show Answer</b></summary>  
 No 
<details>
  
  <summary>Explanation</summary> 
    
>	Interfaces contain abstract methods , Which means only method declerations are present but not implementation, so there is no purpose of an Object, But one can create an Object for a class that implements Interface and reference it to the Interface. 

  </details>
</details>

---

4. What methods can be created in an Interface?

- A.abstract
- B.static
- C.Default
- D. All the above

<details>
<summary><b>Show Answer</b></summary>  
 D
<details>
  
  <summary>Explanation</summary> 
    
>	 Interface is used to implement abstraction, so abstract methods are allowed in an Interface.
> Default methods are allowed to avoid the issue of madatory implementation of all methods in an Interface.
> static methods are gerneraly used to create elper methods, static methods are referenced to the interface, rather than the class that implements the interface.

  </details>
</details>

5. what are the advantages of using default methods in an interface?


<details>

  <summary><b>Show Answer</b> </summary>  
  
  ```  java 
  
  ```
    

   </details>





## Error Detection

1. Identify the error in the following code snippet?

``` java
interface Elevator{
	
	int goUP();
	int goDown();
	final void stop();
}

```

<details><summary><b>Show Answer</b></summary>

> methods in the interface can be abstract or default or static.
> methods in interface can not be final, because final methods can not be overriden. Interfaces are created so they can be implemented by a class and the methods of an inteface shoould have the possibility to be overriden.

</details>
















