## Technical
1. In which package does the Date Time API reside in Java 8?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>
 
>Newly introduced Data Time API will be included in the <code>java.time </code> package

</details>

--- 


2. List the classes in Date and Time API in java 8.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>
 
<blockquote>
 
- `LocalDateTime` API - Simplified form of date - time API without any complexities.
- `ZonedDateTime` API - Special form of date - time API  with varaiations.

 </blockquote>
  
</details>

--- 

3. When do you use Local DateTime API and Zoned DateTime API in Java 8?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>

 <blockquote>

- Local DateTime API - It can be used when there is no need for time zones.
- Zoned DateTime API - It can be used when we need to consider time zones.
  
 </blockquote>

</details>

--- 


4. List the drawbacks of existing date and time API before Java 8.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer </b></summary>
 
  <blockquote>
 
- It is not thread safe 
- It was poorly Designed with less number of features
- Need to write a seperate code for handling time zone logic in older version. 

    </blockquote>
 
</details>

--- 

5. Write the pattern of DateTime using DateTimeFormatter class.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
 
<details><summary><b> Show Answer </b></summary>
 
 <blockquote>
  
```java
DateTimeFormatter format = DateTimeFormatter.ofPattern("dd-MM-yyyy HH:mm:ss");  
```
  
 </blockquote>
 
</details>

--- 

6. Explain about Period and Duration classes.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer </b></summary>
 
  <blockquote>

 - <code>Period</code> handles date based amount of time . 
  - Example : "3 months and 1 day"
 - <code> Duration </code>handles time based amount of time (measured in terms of time).
  - Example : "3 seconds and 3 nanoseconds".
   
    </blockquote>

</details>

--- 

7. Write the syntax for LocalTime class to find the current time in java 8?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer </b></summary>
 
 <blockquote>

```java
LocalTime time = LocalTime.now();  
```
  
</blockquote>
 
</details>
 
 --- 

 
8. Explain about time-zone offset?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer </b></summary>
 
 <blockquote>

- Its is an amount of time that a time -zone varies from Greenwich/UTC. 
- It is measured in fixed number of hours and minutes.
  
 </blockquote>

</details>

--- 

9. Write the syntax to print the current date and time in Java 8?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer </b></summary>
 
 <blockquote>

```java
LocalTime currentTime = LocalTime.now(); 

LocalDate currentDate = LocalDate.now();

LocalDateTime currentDateTime = LocalDateTime.now(); 
```

 </blockquote>
 
</details>

--- 

## Predict the output

10. Predict the output of the following code.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

 ``` java

import java.time.*;    
public class LocalDateExample1 {    
  public static void main(String[] args) {    
    LocalDate date = LocalDate.now();   
    System.out.println("Today date: "+date);    
  }    
}

```

<details><summary><b> Show Answer </b></summary>
 
  <blockquote>

<code>LocalDate</code> class resides in <code>java.time</code> package and the factory method <code>now()</code> will display the current date. 
   
 </blockquote>

</details>

--- 



