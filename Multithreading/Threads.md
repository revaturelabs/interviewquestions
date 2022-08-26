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

6.How can you differentiate User thread and Daemon thread?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>


User and Daemon are basically two types of thread used in Java by using a 'Thread Class'.  

- User Thread (Non-Daemon Thread): In Java, user threads have a specific life cycle and its life is independent of any other thread. JVM (Java Virtual Machine) waits for any of the user threads to complete its tasks before terminating it. When user threads are finished, JVM terminates the whole program along with associated daemon threads. JVM waits for user threads to finish their tasks before termination. These threads are normally created by the user for executing tasks concurrently. They are used for critical tasks or core work of an application. These threads are referred to as high-priority tasks, therefore are required for running in the foreground.


- Daemon Thread: In Java, daemon threads are basically referred to as a service provider that provides services and support to user threads. There are basically two methods available in thread class for daemon thread: setDaemon() and isDaemon(). JVM does not wait for daemon threads to finish their tasks before termination.These threads are normally created by JVM.They are not used for any critical tasks but to do some supporting tasks.These threads are referred to as low priority threads, therefore are especially required for supporting background tasks like garbage collection, releasing memory of unused objects, etc. 

</blockquote>

</details>

---

7.How can we create daemon threads?Explain with an example?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

We can create daemon threads in java using the thread class setDaemon(true). It is used to mark the current thread as daemon thread or user thread. isDaemon() method is generally used to check whether the current thread is daemon or not. If the thread is a daemon, it will return true otherwise it returns false. 
 
Example:   

```java

public class DaemonThread extends Thread { 
   public DaemonThread(String name){ 
       super(name); 
   } 
   public void run() {  
       if(Thread.currentThread().isDaemon())
	 {  
           System.out.println(getName() + " is Daemon thread");  
       }    
       else 
       {  
           System.out.println(getName() + " is User thread");  
       }  
   }   
   public static void main(String[] args) {  
       DaemonThread t1 = new DaemonThread("t1"); 
       DaemonThread t2 = new DaemonThread("t2"); 
       DaemonThread t3 = new DaemonThread("t3");   
       t1.setDaemon(true);       
       t1.start();  
       t2.start();   
       t3.setDaemon(true);  
       t3.start();         
   }  
} 

Output:  
t1 is Daemon thread 
t3 is Daemon thread 
t2 is User thread 

```

But one can only call the setDaemon() method before start() method otherwise it will definitely throw IllegalThreadStateException as shown below:   

```java

public class DaemonThread extends Thread { 
   public void run() { 
       System.out.println("Thread name: "+ Thread.currentThread().getName()); 
       System.out.println("Check if its DaemonThread:" + Thread.currentThread().isDaemon()); 
   } 
   public static void main(String[] args) { 
       DaemonThread t1 = new DaemonThread(); 
       DaemonThread t2 = new DaemonThread(); 
       t1.start();         
       t1.setDaemon(true); 
       t2.start(); 
   } 
} 

Output:  
Thread name: Thread-0 
Check if its DaemonThread: false 

```

</blockquote>

</details>

---

8.How can we differentiate wait() and sleep() methods?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>


wait(): As the name suggests, it is a non-static method that causes the current thread to wait and go to sleep until some other threads call the `notify ()` or `notifyAll()` method for the object’s monitor (lock). It simply releases the lock and is mostly used for inter-thread communication. It is defined in the object class, and should only be called from a synchronized context. 

Example:  

```java

synchronized(monitor) { 
monitor.wait();         
} 

```

- `sleep()`:It is a static method that pauses or stops the execution of the current thread for some specified period. It doesn’t release the lock while waiting and is mostly used to introduce pause on execution. It is defined in thread class, and no need to call from a synchronized context.  

Example:  

```java

synchronized(monitor) { 
Thread.sleep(1000);    
} 

```

</blockquote>

</details>

---

9.How can we differentiate `notify()` and `notifyAll()` methods ?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>


- `notify()`: It sends a notification and wakes up only a single thread instead of multiple threads that are waiting on the object’s monitor.

- `notifyAll()`: It sends notifications and wakes up all threads and allows them to compete for the object's monitor instead of a single thread. 

</blockquote>

</details>

---

10.Why `wait()`,`notify()`, and `notifyAll()` methods are present in Object class?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>


We know that every object has a monitor that allows the thread to hold a lock on the object. But the thread class doesn't contain any monitors. Thread usually waits for the object’s monitor (lock) by calling the `wait()` method on an object, and notify other threads that are waiting for the same lock using `notify()` or `notifyAll()` method.  Therefore, these three methods are called on objects only and allow all threads to communicate with each that are created on that object

</blockquote>

</details>

---

11.Explain deadlock and when it can occurs?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Deadlock, as the name suggests, is a situation where multiple threads are blocked forever. It generally occurs when multiple threads hold locks on different resources and are waiting for other resources to complete their task.
Deadlock situation arises where two threads are blocked forever.  Thread 1 is holding Object 1 but needs object 2 to complete processing whereas Thread 2 is holding Object 2 but needs object 1 first. In such conditions, both of them will hold lock forever and will never complete tasks

</blockquote>

</details>

---

12. Explain volatile variables in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

A volatile variable is basically a keyword that is used to ensure and address the visibility of changes to variables in multithreaded programming. This keyword cannot be used with classes and methods, instead can be used with variables. It is simply used to achieve thread-safety. If you mark any variable as volatile, then all the threads can read its value directly from the main memory rather than CPU cache, so that each thread can get an updated value of the variable.

</blockquote>

</details>

---

13. How do threads communicate with each other?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Threads can communicate using three methods i.e., wait(), notify(), and notifyAll().

</blockquote>

</details>

---

14. Can two threads execute two methods (static and non-static concurrently)?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Yes, it is possible. If both the threads acquire locks on different objects, then they can execute concurrently without any problem.

</blockquote>

</details>

---

15.Explain `finalize()` method?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

`finalize()` method is basically a method of Object class specially used to perform cleanup operations on unmanaged resources just before garbage collection. It is not at all intended to be called a normal method. After the complete execution of `finalize()` method, the object gets destroyed automatically.

</blockquote>

</details>

---

16. Explain synchronization process? Why we use it?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Synchronization is basically a process in java that enables a simple strategy for avoiding thread interference and memory consistency errors. This process makes sure that resource will be only used one thread at a time when one thread tries to access a shared resource. It can be achieved by the synchronized method,synchronized block,static synchronization.

```java

Syntax:  

synchronized (object) 
{        
   //statement to be synchronized 
}

```

</blockquote>

</details>

---

17. Differentiate synchronized method and synchronized block? Which one should be preferred?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>


- Synchronized Method: In this method, the thread acquires a lock on the object when they enter the synchronized method and releases the lock either normally or by throwing an exception when they leave the method.  No other thread can use the whole method unless and until the current thread finishes its execution and release the lock. It can be used when one wants to lock on the entire functionality of a particular method. 

- Synchronized Block: In this method, the thread acquires a lock on the object between parentheses after the synchronized keyword, and releases the lock when they leave the block. No other thread can acquire a lock on the locked object unless and until the synchronized block exists. It can be used when one wants to keep other parts of the programs accessible to other threads.
 
- Synchronized blocks should be preferred more as it boosts the performance of a particular program. It only locks a certain part of the program or critical section rather than the entire method and therefore leads to less contention.

</blockquote>

</details>

---

18. Explain thread starvation?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Thread starvation is basically a situation or condition where a thread won’t be able to have regular access to shared resources and therefore is unable to proceed or make progress. This is because other threads have high priority and occupy the resources for too long. This usually happens with low-priority threads that do not get CPU for its execution to carry on. 

</blockquote>

</details>

---

19. Describe BlockingQueue?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>


BlockingQueue basically represents a queue that is thread-safe. Producer thread inserts resource/element into the queue using `put()` method unless it gets full and consumer thread takes resources from the queue using take() method until it gets empty. But if a thread tries to dequeue from an empty queue, then a particular thread will be blocked until some other thread inserts an item into the queue, or if a thread tries to insert an item into a queue that is already full, then a particular thread will be blocked until some threads take away an item from the queue.  

</blockquote>

</details>

---

20. Can you start a thread twice?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

No, it's not at all possible to restart a thread once a thread gets started and completes its execution. Thread only runs once and if you try to run it for a second time, then it will throw a runtime exception i.e., `java.lang.IllegalThreadStateException`. 

</blockquote>

</details>



