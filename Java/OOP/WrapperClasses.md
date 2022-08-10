


## Technical

1. Can java be considered an absolute Object Oriented language? Explain the reason.



<details><summary> <b>Show Answer</b> </summary>
  
> No
  
<details> <summary><b>Explanation</b></summary>
  
> Java is not perfectly object-oriented because Primitive datatypes are included in java for fast execution. Wrapper classes are used to convert primitives to objects.
  
</details>
</details>

---

2. What is boxing?


    
<details><summary> <b>Show Answer</b> </summary>

 > The conversion of Primitive data types to Object is called Boxing.
  
</details>

---

3. What is unboxing?

<details><summary> <b>Show Answer</b> </summary>
  
> The conversion of Object to primitive datatype is called Unboxing.
  
</details>

---



4. How to convert a primitive datatype to an Object wrapper class?


<details><summary> <b>Show Answer</b> </summary>
  
  
  ``` java
  // primitive int i
  int i =1;
  // Wrapping primitive datatype int to Wrapper object Integer
  Integer k = new  Integer(i);
  ```
  
</details>

---

5. How to convert wrapper objects to a primitive data type?




<details><summary> <b>Show Answer</b> </summary>
 
  ``` java
  // wrapper object of type Integer
  Integer i =1;
  // Unboxing
  int j = i;
  ``` 


</details>

---

6. Are wrapper classes immutable? justify the answer.

<details>
  
<summary><b>Show Answer</b></summary>
  
 > Yes, wrapper classes are immutable.
 > wrapper classes are used to store data in collections and as a developer one doesn't wish that all the values in a collection are changed just because a primitive value is changed. 
 
  
  

  
</details>

 ---

7. How does wrapper class work Internally?

<details>
  
<summary><b>Show Answer</b></summary>
  
> when a wrapper class is created the primitive data type is stored as a field in the wrapper class and an object reference is created.
</details>







  









