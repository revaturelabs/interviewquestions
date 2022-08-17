## Real-Time Applications

1. Physics Department in Caltech got a new 3D printer, Sheldon used the printer for printing prototypes for his hadron collider. Howard used the printer to print his mini action figure. this is an example for?

  ![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

- A.Polymorphism
- B.Inheritance
- C.Abstarction
- D.Encapsulation

</details>
<details><summary> <b>Show Answer</b> </summary>
  
> A
  
  <details><summary><b>Explanation</b></summary> <i>printing using a 3D printer is a method in the Caltech Physics department</i>, which is a class. Sheldon used the method for research and Howard used the same method for fun.
 </details>
</details>

---

2. John got a recipe for cookies from his mother, but john likes choco chips, so he altered the original cookie recipe, 
   this is an example for?
 
 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

- A.Method Overriding
- B.Method Overloading
- C.Inheritance
- D.Abstraction

<details><summary> Show Answer </summary>
> A
  <details><summary><b>Explanation</b><summary>
> John inherited The original recipe(a method) is  from his mother(parent class) and he altered the recipe.
   </details>
    </details>
    
---

## Technical

1. The following code snippet is an example for?

  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

``` java
public class Languages {
     public static void main(String[] args) {
      Languages l= new Languages();
      l.speakGerman();
    
  }
  public void speakGerman() {
    System.out.println("Guten Tag");
  }
  public String speakGerman() {
    return "Wiedersehen";
  }

}
```
- A.Method Overloading
- B.Method Overriding
- C.Inheritance
- D.None of the above



<details><summary> <b>Show Answer</b> </summary>

  > D
  
  <details><summary><b>Explanation</b></summary>
  <blockquote>
    `speakGerman()` is written twice with different signatures in the same class, So it can not be considered as method overloading. it is just a duplicate method.

  </blockquote>
</details>
 </details>
   
 ---

2. What is static polymorphism?


![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary> <b>Show Answer</b> </summary>
  
> Static Polymorphism is also called Compile time Polymorphism or Method overloading. The method behavior is decided during compile-time in static polymorphism.
  
</details>
    
 ---

3. What is Dynamic polymorphism?
    
![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary> <b>Show Answer</b> </summary>
  
> Dynamic Polymorphism is also called Run-time Polymorphism or Method overriding. The method behavior is decided during runtime in static polymorphism.
  
</details>
    
 ---

4. Which of the following is an example of static binding?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

- A.method overriding
- B.method overloading
- C.abstraction
- D.none of the above

<details><summary> <b>Show Answer</b> </summary>
  
> B

  <details>
  <summary>Explanation</summary> 
    
> static binding is linking method call with method definition during compile-time. compile-time polymorphism is
  also called method overloading. 

</details>
  </details>
    
 ---


## Problem solving

1. What is the output of the following java code?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

``` java
  class Animal {
        
    public void barkingDog() {
    System.out.println("Wolf Wolf!");
  }
  public void barkingDog(String a) {
    System.out.println(a);
    
  }
  public static void main(String[] args) {
    Animal a = new Animal();
    a.barkingDog("Barking!");
  }
}
        
   ```

<details><summary> <b>Show Answer</b> </summary>
  
 Barking!
  
<details>
 <summary><b>Explanation</b></summary> the concept of method overloading is implemented here, In the main method we are calling barkingDog() with a
  parameter "Barking!". So bakringDog(String a) is implemented.

</details>
</details>
    
 ---



## Error Detection

1. Predict the output of the program and debug the program.  

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)      

``` java
public class Vacation{
    public void visitLondon(){
        System.out.println("I met the Queen of England");
    }  
     public static void main(String[] args) {
      BusinessTrip b = new BusinessTrip();
      b.visitLondon();
    
  }
 
} 
class BusinessTrip extends Vacation{
    public String visitLondon(){
        return "The London branch is totally off the charts";
    }


}
``` 
  - A.Compile time error
  - B.Runtime error
  - C.No output
  - D.The London branch is totally off the charts
  
  
  <details>
  <summary> <b>Show Answer</b> </summary>
>  A
    
<details>
<summary> <b>Explanation</b> </summary>

The outcome of the program is the compile-time error and it's caused because the method signature for visitLondoon(), which is being overloaded is different in the parent class(Vacation) and Child class(BusinessTrip).
  
  </details>
   </details>
    
 ---


  2. Find the error in the following program.  

  
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

``` java
public class Area{

  public static void main(String[] args) {
      Area a= new Area();
      System.out.println(a.calculateTriangleArea(1.0,2.0));
    
  }
    
    public double calculateTriangleArea(double d, double e)
    {
      return  0.5*d*e;
      
    }
    public int calculateTriangleArea(int base, int height) {
      return base*height;
      
    }
   
} 

``` 
  - A.Compile-time error
  - B.Run-time error
  - C.1.0
  - D.2
  
  
  <details>
  <summary> <b>Show Answer</b> </summary>
    
  > C
 <details>
    <summary><b>Explanation</b></summary>
   > calculateTriangleArea(double base, double height) is implemented when 1.0 and 2.0 are passed as method parameters.
  
  </details>
     </details>
    
 ---





  








