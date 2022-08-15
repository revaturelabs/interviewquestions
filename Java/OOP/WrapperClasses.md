


## Technical

1. Can java be considered an absolute Object Oriented language? Explain the reason.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> No
  
<details> <summary><b>Explanation</b></summary>
  
> Java is not perfectly object-oriented because Primitive datatypes are included in java for fast execution. Wrapper classes are used to convert primitives to objects.
  
</details>
</details>

---

2. What is boxing?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


    
<details><summary> <b>Show Answer</b> </summary>

 > The conversion of Primitive data types to Object is called Boxing.
  
</details>

---

3. What is unboxing?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
  
> The conversion of Object to primitive datatype is called Unboxing.
  
</details>

---



4. How to convert a primitive datatype to an Object wrapper class?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


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

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)




<details><summary> <b>Show Answer</b> </summary>
 
  ``` java
  // wrapper object of type Integer
  Integer i =1;
  // Unboxing
  int j = i;
  ``` 
<blockquote>
  
 - This is only possible from jdk 1.5 onwards not before that.
The automatic conversion of primitive data types into its equivalent Wrapper type is known as boxing and opposite operation is known as unboxing. This is the new feature of Java5. So java programmer doesn't need to write the conversion code.

</blockquote>

</details>

---

6. Are wrapper classes immutable? justify the answer.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details>
  
<summary><b>Show Answer</b></summary>
  
 > Yes, wrapper classes are immutable.
 > Immutable class in java means that once an object is created, we cannot change its content. In Java, primitive wrapper classes (Integer, Byte, Long, Float, Double, Character, Boolean, Short) and String class is immutable, so operations like addition and subtraction create a new object and not modify the old. 
 > wrapper classes are used to store data in collections and as a developer one doesn't wish that all the values in a collection are changed just because a primitive value is changed. 
 
  
  

  
</details>

 ---

7. How does wrapper class work Internally?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details>
  
<summary><b>Show Answer</b></summary>
  
> Primitive data type is stored as a field in the wrapper class and an object reference is created, there are multiple methods provided by wrapper classs 
</details>







  









