## Technical
1: In which package does the Date Time API reside in Java 8?

<details><summary><b> Show Answer </b></summary>
 
 Newly introduced Data Time API will be included in the package java.time.

</details>

--- 


2: List the classes in Date and Time API in java 8.

<details><summary><b> Show Answer </b></summary>
 
- Local DateTime API- Simplified form of date - time API without any complexities.
- Zoned DateTime API- Special form of date - time API  with varaiations.

</details>

--- 

3: When do you use Local DateTime API and Zoned DateTime API  in Java 8?

<details><summary><b> Show Answer </b></summary>

- It can be used when there is no need for time zones.
- It can be used when we need to consider time zones.

</details>

--- 


4: List the drawbacks of existing date and time API before Java 8.

<details><summary><b> Show Answer </b></summary>
 
- It is not thread safe 
- It was poorly Designed with less number of features
- Need to write a seperate code for handling time zone logic in older version. 

</details>

--- 

5: Write the pattern of DateTime using DateTimeFormatter class.
 
<details><summary><b> Show Answer </b></summary>
 
DateTimeFormatter format = DateTimeFormatter.ofPattern("dd-MM-yyyy HH:mm:ss");  

</details>

--- 

6: Explain about Period and Duration classes.

<details><summary><b> Show Answer </b></summary>

- Period handles date based amount of time . 
- Example : "3 months and 1 day"
- Duration handles time based amount of time (measured in terms of time).
- Example : "3 seconds and 3 nanoseconds".

</details>

--- 

7: Write the syntax for LocalTime class to find the current time in java 8?

<details><summary><b> Show Answer </b></summary>

LocalTime time = LocalTime.now();  

 </details>
 
 --- 

 
8: Explain about time-zone offset?

<details><summary><b> Show Answer </b></summary>

- Its is an amount of time that a time -zone varies from Greenwich/UTC. 
- It is measured in fixed number of hours and minutes.

</details>

--- 

9: Write the syntax to print the current date and time in Java 8?

<details><summary><b> Show Answer </b></summary>

LocalTime currentTime = LocalTime.now(); <br>

LocalDate currentDate = LocalDate.now();<br>

LocalDateTime currentDateTime = LocalDateTime.now(); <br>

</details>

--- 

## Predict the output

10: Predict the output of the following code.

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

LocalDate class resides in java.time package and the factory method now() will display the current date. 

</details>

--- 



