## Technical
1. Explain Method Reference.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>
 
 <blockquote>

It is to refer the method of functional interface. While using a lambda expression to refer to a method, we can use a method reference instead of a lambda expressison.
  
  </blockquote>

</details>
 
 ---

2. List the types of Method References.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>
 <blockquote>
  
- Reference to a static method.
  
- Reference to an instance method.
  
- Reference to an instance method of an arbitrary object of a particular type
  
- Reference to a constructor.
  
 </blockquote>
</details>

 ---
 
3. Write the syntax for referring to a static method?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>
 
 <blockquote>
  
- ContainingClass::staticMethodName
- We can refer to the static method by calling its name with the class where it resides.
  
 </blockquote>
 
</details>
 
 ---

4. Write the syntax for Reference to an instance method of a particular object?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>
 
 <blockquote>
  
- containingObject::instanceMethodName
- use the instance method name of the particular object name.
  
 </blockquote>
 
</details>

 ---
 
5. Write the syntax for Reference to an instance method of an arbitrary object of a particular type?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>
 
 <blockquote>
  
- We can mention the type with the instance method name of the object.
- ContainingType::methodName
  
 </blockquote>
 
</details>
 
 ---

6. Write the syntax for Reference to a constructor?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>
 
 <blockquote>
  
- ClassName::new
- new is the keyword to refer to the constructor with the class name.
  
 </blockquote>
</details>

 ---
 
 7. Explain the parts of the method reference.

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
 
<details><summary><b> Show Answer </b></summary>
 
 <blockquote>
  
- It has 2 parts. class/object and method/constructor.
- Separated by :: (double colons)
- No additional parameters are passed in method reference.
  
 </blockquote>
 
</details>
 
 ---

8. How to print all the elements in the list using method reference?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer </b></summary>


 ``` java 
 list.forEach(System.out::println);  
 ``` 
<details><summary><b>Explanation</b></summary>
  <blockquote>
- Here we are using the forEach method to display the elements one by one in the list.
 </blockquote>
</details>
 
 </details>

 ---
 
## Problem Solving

9. Predict the output of the following code.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

``` java
import java.io.*;
import java.util.*;
public class MethodReference{
    public static void main(String[] args)
    {
        List<String> bookList = new ArrayList<>();
        bookList .add("Java Programming");
        bookList .add("Data Strcutures and Alogrithms");
        bookList .add("Python Programming");
        Collections.sort(bookList ,String::compareToIgnoreCase);
        bookList .forEach(System.out::println);
    }
}
``` 

<details><summary><b> Show Answer </b></summary>
 
 <blockquote>
  
   Data Structures and Alogrithms<br>
   Java Programming<br>
   Python Programming
  
  </blockquote>
 
 <details><summary><b>Explanation</b></summary>
  
   <blockquote>
    
   -  This is an example of Reference to an instance method of an arbitrary object of a particular type.
   -  First, it will sort the list and apply compareToIgnoreCase to return the result.
    
 </blockquote>
  
</details>
 
 </details>

 ---
 
10. What should be the code in line 9  to get the result "Hello, this is a static method." using a reference to the static methods?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

``` java
interface Sample{  
    void print();  
}  
public class MethodReference {  
    public static void printhello(){  
        System.out.println("Hello, this is static method.");  
    }  
    public static void main(String[] args) {  
        // Line 9
        sample.print();  
    }  
} 
```
<details><summary><b> Show Answer </b></summary>
 
 ``` java

 Sample sample = MethodReference::printhello; 
 
 ```
 
 <details><summary><b>Explanation</b></summary>
  
   <blockquote>
    
 - Here the static method reference printhello() refers to its functional method print() in the interface Sample.
    
 </blockquote>
  
 </details>
 
 </details>
 
 ---



