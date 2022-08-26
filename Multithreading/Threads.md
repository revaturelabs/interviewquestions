1. How can you describe multithreading is beneficial in java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Multithreading allows the program to run continuously even if a part of it is blocked. It improves performance as compared to traditional parallel programs that use multiple processes. It allows to write effective programs that utilize maximum CPU time.It improves the responsiveness of complex applications or programs. It increases use of CPU resources and reduce costs of maintenance. It saves time and parallelism tasks. If an exception occurs in a single thread, it will not affect other threads as threads are independent. It requires less resource-intensive than executing multiple processes at the same time.

</blockquote>

</details>

---

2.Explain Threads in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Threads are basically the lightweight and smallest unit of processing that can be managed independently by a scheduler. Threads are referred to as parts of a process that simply let a program execute efficiently with other parts or threads of the process at the same time. Using threads, one can perform complicated tasks in the easiest way. It is considered the simplest way to take advantage of multiple CPUs available in a machine. They share the common address space and are independent of each other

</blockquote>

</details>

---

3.How can you implement threads in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>


There are basically two ways of implementing thread in java as given below: 

- By Extending the Thread class

Example:

```java

class ThreadingDemo extends Thread 
{   
  public void run() 
 {   
     System.out.println("My thread is in running state.");    
 } 
  public static void main(String args[]) 
 {   
    ThreadingDemo obj=new ThreadingDemo();  
        obj.start();  
  }  
} 

Output:

My thread is in running state.

```
- By Implementing Runnable interface in Java

Example:  

```java

class ThreadingDemo implements Runnable 
{  
   public void run() 
 {  
      System.out.println("My thread is in running state.");  
  }  
    public static void main(String args[]) 
 {  
      ThreadingDemo obj=new ThreadingDemo();   
      Thread t=new Thread(obj);       
      t.start();  
 }   
} 

Output: 
My thread is in running state.

```
 
</blockquote>

</details>

---

4.How can you differentiate threads and process in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Threads:
- It is a subset of a subunit of a process.	
- In this, inter-thread communication is faster, less expensive, easy and efficient because threads share the same memory address of the process they belong to. 
- These are easier to create, lightweight, and have less overhead. 
- It requires less time for creation, termination, and context switching.	
- Processes with multiple threads use fewer resources.
- Threads are parts of a process, so they are dependent on each other but each thread executes independently.
- There is a need for synchronization in threads to avoid unexpected scenarios or problems.
- They share data and information with each other. 

Process:	
- It is a program in execution containing multiple threads.
- In this, inter-process communication is slower, expensive, and complex because each process has different memory space or address.,
- These are difficult to create, heavyweight, and have more overhead.
- It requires more time for creation, termination, and context switching.
- Processes without threads use more resources.
- Processes are independent of each other.
- There is no need for synchronization in each process.
- They do not share data with each other. 

</blockquote>

</details>

---

5.How can you differentiate class lock and object lock?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- Class Lock: In java, each and every class has a unique lock usually referred to as a class level lock. These locks are achieved using the keyword 'static synchronized' and can be used to make static data thread-safe. It is generally used when one wants to prevent multiple threads from entering a synchronized block. 

Example:  

```java

public class ClassLevelLockExample  
{    
  public void classLevelLockMethod()  
 {       
     synchronized (ClassLevelLockExample.class)  
       {         
               
       }    
 } 
} 

```

- Object Lock: In java, each and every object has a unique lock usually referred to as an object-level lock. These locks are achieved using the keyword 'synchronized' and can be used to protect non-static data. It is generally used when one wants to synchronize a non-static method or block so that only the thread will be able to execute the code block on a given instance of the class.  

Example:  

```java

public class ObjectLevelLockExample  
{    
  public void objectLevelLockMethod()  
 {   
     synchronized (this)  
       {     
               
       } 
 }
} 

```

</blockquote>

</details>

---

