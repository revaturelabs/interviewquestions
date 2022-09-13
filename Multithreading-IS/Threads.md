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

8.How can we differentiate `wait()` and `sleep()` methods?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>


`wait()` :It is a non-static method that causes the current thread to wait and go to sleep until some other threads call the `notify ()` or `notifyAll()` method for the object’s monitor (lock). It simply releases the lock and is mostly used for inter-thread communication. It is defined in the object class, and should only be called from a synchronized context. 

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

---

21. Explain context switching.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Context switching is referred to as switching of CPU from one thread or process to another one. It allows multiple processes to share the same CPU. In context switching, the state of thread or process is stored so that the execution of the thread can be resumed later if required. 

</blockquote>

</details>

---

22. Explain CyclicBarrier and CountDownLatch?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- CyclicBarrier: It is a tool to synchronize threads processing using some algorithm. It enables a set of threads to wait for each other till they reach a common execution point or common barrier points, and then let them further continue execution. One can reuse the same CyclicBarrier even if the barrier is broken by setting it. 

- CountDownLatch: It is a tool that enables main threads to wait until mandatory operations are performed and completed by other threads. In simple words, it makes sure that a thread waits until the execution in another thread completes before it starts its execution. One cannot reuse the same CountDownLatch once the count reaches 0. 

</blockquote>

</details>

---

23. What do you mean by inter-thread communication?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Inter-thread communication is a process or mechanism using which multiple threads can communicate with each other. It is especially used to avoid thread polling in java and can be obtained using wait(), notify(), and notifyAll() methods. 

</blockquote>

</details>

---

24. Explain Thread Scheduler and Time Slicing?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- Thread Scheduler: It is a component of JVM that is used to decide which thread will execute next if multiple threads are waiting to get the chance of execution. By looking at the priority assigned to each thread that is READY, the thread scheduler selects the next run to execute. To schedule the threads, it mainly uses two mechanisms: Preemptive Scheduling and Time slicing scheduling.  

- Time Slicing: It is especially used to divide CPU time and allocate them to active threads. In this, each thread will get a predefined slice of time to execute. When the time expires, a particular thread has to wait till other threads get their chances to use their time in a round-robin fashion. Every running thread will get executed for a fixed time period

</blockquote>

</details>

---

25. Explain shutdown hook?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

A shutdown hook is simply a thread that is invoked implicitly before JVM shuts down. It is one of the most important features of JVM because it provides the capacity to do resource cleanup or save application state JVM shuts down.  By calling the halt(int) method of the Runtime class, the shutdown hook can be stopped. Using the following method, one can add a shutdown hook. 

```java

public void addShutdownHook(Thread hook){}     
Runtime a=Runtime.getRuntime();   
a.addShutdownHook(new MyThread());

```

</blockquote>

</details>

---

26. What do you mean by busy spinning?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>


Busy Spinning, also known as Busy-waiting, is a technique in which one thread waits for some condition to happen, without calling wait or sleep methods and releasing the CPU. In this condition, one can pause a thread by making it run an empty loop for a certain time period, and it does not even give CPY control. Therefore, it is used to preserve CPU caches and avoid the cost of rebuilding cache

</blockquote>

</details>

---

27. What is ConcurrentHashMap and Hashtable? In java, why is ConcurrentHashMap considered faster than Hashtable?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- ConcurrentHashMap: It was introduced in Java 1.5 to store data using multiple buckets. As the name suggests, it allows concurrent read and writes operations to the map. It only locks a certain portion of the map while doing iteration to provide thread safety so that other readers can still have access to the map without waiting for iteration to complete.  

- Hashtable: It is a thread-safe legacy class that was introduced in old versions of java to store key or value pairs using a hash table.  It does not provide any lock-free read, unlike ConcurrentHashMap. It just locks the entire map while doing iteration. 

- ConcurrentHashMap and Hashtable, both are thread-safe but ConcurrentHashMap generally avoids read locks and improves performance, unlike Hashtable. ConcurrentHashMap also provides lock-free reads, unlike Hashtable. Therefore, ConcurrentHashMap is considered faster than Hashtable especially when the number of readers is more as compared to the number of writers. 

</blockquote>

</details>

---

28. Explain thread priority.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Thread priority simply means that threads with the highest priority will get a chance for execution prior to low-priority threads. One can specify the priority but it's not necessary that the highest priority thread will get executed before the lower-priority thread. Thread scheduler assigns processor to thread on the basis of thread priority. The range of priority changes between 1-10 from lowest priority to highest priority. 

</blockquote>

</details>

---

29.What do you mean by the ThreadLocal variable in Java?Explain with an example?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

ThreadLocal variables are special kinds of variables created and provided by the Java ThreadLocal class. These variables are only allowed to be read and written by the same thread. Two threads cannot be able to see each other’s ThreadLocal variable, so even if they will execute the same code, then there won't be any race condition and the code will be thread-safe.  

```java

public class ThreadLocal {   
     public static class MyRunnable implements Runnable {   
       private ThreadLocal<Integer> threadLocal = new ThreadLocal<Integer>();   
       
       public void run() {   
           threadLocal.set( (int) (Math.random() * 50D) );   
           try{   
               Thread.sleep(1000);   
           } catch (InterruptedException e) {   
           }   
           System.out.println(threadLocal.get());   
       }   
   }   
   public static void main(String[] args){   
       MyRunnable Instance = new MyRunnable();    
       Thread t1 = new Thread(Instance);   
       Thread t2 = new Thread(Instance);   
       t1.start();   
       t2.start();   
   }   
} 
Output: 

10 
33 
10 33


```

</blockquote>

</details>

---
	
30. What is semaphore?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Semaphore is regarded as a thread synchronization construct that is usually required to control and manage the access to the shared resource using counters. It simply sets the limit of the thread. The semaphore class is defined within the package java.util.concurrent and can be used to send signals between threads to avoid missed signals or to guard critical sections. It can also be used to implement resource pools or bounded collection

</blockquote>

</details>
	
---
	
31.Explain Thread Group. Why we should not use it?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>


ThreadGroup is a class that is used to create multiple groups of threads in a single object. This group of threads is present in the form of three structures in which every thread group has a parent except the initial thread. Thread groups can contain other thread groups also. A thread is only allowed to have access to information about its own thread group, not other thread groups. 

Previously in the old version of Java, the only functionality that did not work without a thread group was `uncaughtException( Thread t, Throwable e)`. But  now in  latest versions of Java , there is `Thread.setUncaughtExceptionHandler(UncaughtExceptionHandler)`. So now even that works without thread groups and therefore, there is no need to use thread groups.  

```java

t1.setUncaughtExceptionHandler(new UncaughtExceptionHandler() { 
public void uncaughtException(Thread t, Throwable e)  {  
System.out.println("exception occured:"+e.getMessage()); 
}  
}; 

```

</blockquote>

</details>
	
---

32.What is the ExecutorService interface?Explain with an example.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

ExecutorService interface is basically a sub-interface of Executor interface with some additional methods or features that help in managing and controlling the execution of threads. It enables us to execute tasks asynchronously on threads.

```java

import java.util.concurrent.ExecutorService;   
import java.util.concurrent.Executors;   
import java.util.concurrent.TimeUnit;   
  
public class TestThread {   
public static void main(final String[] arguments) throws InterruptedException {   
ExecutorService e = Executors.newSingleThreadExecutor();   
 
     try {   
       e.submit(new Thread());   
        System.out.println("Shutdown executor");   
        e.shutdown();   
        e.awaitTermination(5, TimeUnit.SECONDS);   
  } catch (InterruptedException ex) {   
       System.err.println("tasks interrupted");   
  } finally {   
  
        if (!e.isTerminated()) {   
           System.err.println("cancel non-finished tasks");   
     }   
        e.shutdownNow();   
        System.out.println("shutdown finished");   
  }   
  }   
  
  static class Task implements Runnable {   
        
     public void run() {   
          
        try {   
        Long duration = (long) (Math.random() * 20);   
           System.out.println("Running Task!");   
           TimeUnit.SECONDS.sleep(duration);   
     } catch (InterruptedException ex) {   
           ex.printStackTrace();   
     }   
  }   
 }          
}   
Output:

Shutdown executor 
shutdown finished

```

</blockquote>

</details>

---
	
33.What will happen if we don’t override the thread class run() method?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Nothing will happen as such if we don’t override the `run()` method. The compiler will not show any error. It will execute the `run()` method of thread class and we will just don’t get any output because the `run()` method is with an empty implementation. 

```java

class MyThread extends Thread { 
 
} 
public class DontOverrideRun { 
  public static void main(String[] args) { 
         System.out.println("Started Main."); 
         MyThread thread1=new MyThread(); 
      thread1.start(); 
         System.out.println("Ended Main."); 
  } 
} 

Output: 

Started Main. 
Ended Main.  

```

</blockquote>

</details>

---
	
34. What is the lock interface? Why is it better to use a lock interface rather than a synchronized block.?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

- Lock interface  is generally used as a synchronization mechanism to provide important operations for blocking.  


- Advantages of using Lock interface over Synchronization block: Methods of Lock interface i.e., `Lock()` and `Unlock()` can be called in different methods. It is the main advantage of a lock interface over a synchronized block because the synchronized block is fully contained in a single method.  
Lock interface is more flexible and makes sure that the longest waiting thread gets a fair chance for execution, unlike the synchronization block.

</blockquote>

</details>
	
---

35. Is it possible to call the `run()` method directly to start a new thread?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

No, it's not possible at all. You need to call the start method to create a new thread otherwise run method won't create a new thread. Instead, it will execute in the current thread

</blockquote>

</details>
	
---
	
36. Is it possible that each thread can have its stack in multithreaded programming?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Of course, it is possible. In multithreaded programming, each thread maintains its own separate stack area in memory because of which every thread is independent of each other rather than dependent.

</blockquote>

</details>
	
---

37. What are different states in lifecycle of Thread?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

When we create a Thread in java program, its state is New. Then we start the thread that change it's state to Runnable. Thread Scheduler is responsible to allocate CPU to threads in Runnable thread pool and change their state to Running. Other Thread states are Waiting, Blocked and Dead. .


</blockquote>

</details>
	
---
	
38. Can we call `run()` method of a Thread class?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>


Yes, we can call `run()` method of a Thread class but then it will behave like a normal method. To actually execute it in a Thread, we need to start it using `Thread.start()` method.

</blockquote>

</details>
	
---

39. How can we pause the execution of a Thread for specific time?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

We can use Thread class `sleep()` method to pause the execution of Thread for certain time. Note that this will not stop the processing of thread for specific time, once the thread awake from sleep, it's state gets changed to runnable and based on thread scheduling, it gets executed.

</blockquote>

</details>
	
---

40. What do you understand about Thread Priority?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Every thread has a priority, usually higher priority thread gets precedence in execution but it depends on Thread Scheduler implementation that is OS dependent. We can specify the priority of thread but it doesn't guarantee that higher priority thread will get executed before lower priority thread. Thread priority is an _int_ whose value varies from 1 to 10 where 1 is the lowest priority thread and 10 is the highest priority thread.

</blockquote>

</details>
	
---

41. How can we make sure `main()` is the last thread to finish in Java Program?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

We can use Thread `join()` method to make sure all the threads created by the program is dead before finishing the main function. 

</blockquote>

</details>
	
---

42. Why `wait()`, `notify()` and `notifyAll()` methods have to be called from synchronized method or block?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

When a Thread calls `wait()` on any Object, it must have the monitor on the Object that it will leave and goes in wait state until any other thread call `notify()` on this Object. Similarly when a thread calls `notify()` on any Object, it leaves the monitor on the Object and other waiting threads can get the monitor on the Object. Since all these methods require Thread to have the Object monitor, that can be achieved only by synchronization, they need to be called from synchronized method or block.
 

</blockquote>

</details>
	
---
	
43. Why Thread `sleep()` and `yield()` methods are static?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Thread `sleep()` and `yield()` methods work on the currently executing thread. So there is no point in invoking these methods on some other threads that are in wait state. That’s why these methods are made static so that when this method is called statically, it works on the current executing thread and avoid confusion to the programmers who might think that they can invoke these methods on some non-running threads.

</blockquote>

</details>
	
---
	
44. How can we achieve thread safety in Java?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

There are several ways to achieve thread safety in java - synchronization, atomic concurrent classes, implementing concurrent Lock interface, using volatile keyword, using immutable classes and Thread safe classes. 

</blockquote>

</details>

---
	
45. What is Deadlock? How to analyze and avoid deadlock situation?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Deadlock is a programming situation where two or more threads are blocked forever, this situation arises with at least two threads and two or more resources. To analyze a deadlock, we need to look at the java thread dump of the application, we need to look out for the threads with state as BLOCKED and then the resources it’s waiting to lock, every resource has a unique ID using which we can find which thread is already holding the lock on the object. Avoid Nested Locks, Lock Only What is required and avoid waiting indefinitely are common ways to avoid deadlock situation. 

</blockquote>

</details>
	
---
	
46. What is an atomic operation? What are the atomic classes in Java Concurrency API?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Atomic operations are performed in a single unit of task without interference from other operations. Atomic operations are necessity in multi-threaded environment to avoid data inconsistency. int++ is not an atomic operation. So by the time one thread read its value and increment it by one, another thread has read the older value leading to the wrong result. To solve this issue, we will have to make sure that increment operation on count is atomic, we can do that using synchronization but `java.util.concurrent.atomic` provides wrapper classes for int and long that can be used to achieve this atomically without the usage of Synchronization.

</blockquote>

</details>
	
---

47. What is Lock interface in Java Concurrency API? What are its benefits over synchronization?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Lock interface provides more extensive locking operations than can be obtained using synchronized methods and statements. They allow more flexible structuring, may have quite different properties and may support multiple associated Condition objects. The advantages of a lock are:
- it’s possible to make them fair.
- it’s possible to make a thread responsive to interruption while waiting on a Lock object.
- it’s possible to try to acquire the lock, but return immediately or after a timeout if the lock can’t be acquired.
- it’s possible to acquire and release locks in different scopes, and in different orders.

</blockquote>

</details>
	
---
	
48. What are Executors Framework?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

The Executor framework is a framework for standardizing invocation, scheduling, execution, and control of asynchronous tasks according to a set of execution policies. Creating a lot many threads with no bounds to the maximum threshold can cause the application to run out of heap memory. So, creating a ThreadPool is a better solution as a finite number of threads can be pooled and reused. Executors framework facilitate the process of creating Thread pools in java.

</blockquote>

</details>
	
---
	
49. What is BlockingQueue? How can we implement Producer-Consumer problem using Blocking Queue?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

`java.util.concurrent.BlockingQueue` is a Queue that supports operations that wait for the queue to become non-empty when retrieving and removing an element, and wait for space to become available in the queue when adding an element. BlockingQueue doesn’t accept null values and throw NullPointerException if you try to store null value in the queue. BlockingQueue implementations are thread-safe. All queuing methods are atomic in nature and use internal locks or other forms of concurrency control. BlockingQueue interface is part of the Java collections framework and it’s primarily used for implementing the producer-consumer problem.

</blockquote>

</details>
	
---

50.How java provides ways to create a thread programmatically?Explain with an example?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Java provides ways to create a thread programmatically by the following ways:

- Implementing the `java.lang.Runnable` interface.
- Extending the `java.lang.Thread` class.

- Java Thread Example - implementing Runnable interface:To make a class runnable, we can implement `java.lang.Runnable` interface and provide implementation in `public void run()` method. To use this class as Thread, we need to create a Thread object by passing object of this runnable class and then call `start()` method to execute the `run()` method in a separate thread. 

```java

public class Work implements Runnable {

    public void run() {
        System.out.println("Doing processing - START "+Thread.currentThread().getName());
        try {
            Thread.sleep(1000);
            doDBProcessing();
        } catch (InterruptedException e) {
            e.printStackTrace();
        }
        System.out.println("Doing processing - END "+Thread.currentThread().getName());
    }

    private void doDBProcessing() throws InterruptedException {
        Thread.sleep(5000);
    }

}

```

- Java Thread Example - extending Thread class:We can extend `java.lang.Thread` class to create our own java thread class and override `run()` method. Then we can create it’s object and call `start()` method to execute our custom java thread class run method. Here is a simple java thread example showing how to extend Thread class.

```java

public class MyThread extends Thread {

    public MyThread(String name) {
        super(name);
    }

    @Override
    public void run() {
        System.out.println("MyThread - START "+Thread.currentThread().getName());
        try {
            Thread.sleep(1000);
            doDBProcessing();
        } catch (InterruptedException e) {
            e.printStackTrace();
        }
        System.out.println("MyThread - END "+Thread.currentThread().getName());
    }

    private void doDBProcessing() throws InterruptedException {
        Thread.sleep(5000);
    }
    
}

public class ThreadRunExample {

    public static void main(String[] args){
        Thread t1 = new Thread(new Work(), "t1");
        Thread t2 = new Thread(new Work(), "t2");
        System.out.println("Starting Runnable threads");
        t1.start();
        t2.start();
        System.out.println("Runnable Threads has been started");
        Thread t3 = new MyThread("t3");
        Thread t4 = new MyThread("t4");
        System.out.println("Starting MyThreads");
        t3.start();
        t4.start();
        System.out.println("MyThreads has been started");
        
    }
}

Output of the above java thread example program is:

Starting Runnable threads
Runnable Threads has been started
Doing heavy processing - START t1
Doing heavy processing - START t2
Starting MyThreads
MyThread - START Thread-0
MyThreads has been started
MyThread - START Thread-1
Doing processing - END t2
MyThread - END Thread-1
MyThread - END Thread-0
Doing processing - END t1

```

Once we start any thread, it’s execution depends on the OS implementation of time slicing and we can’t control their execution. However we can set threads priority but even then it doesn’t guarantee that higher priority thread will be executed first. Run the above program multiple times and you will see that there is no pattern of threads start and end.

</blockquote>

</details>

---

51.Explain Blocking Queue with producer - consumer example?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

A normal java object that will be produced by Producer and added to the queue. You can also call it as payload or queue message.

```java

public class Message {
    private String msg;
    
    public Message(String str){
        this.msg=str;
    }

    public String getMsg() {
        return msg;
    }

}

```

- Java BlockingQueue Example - Producer:Producer class that will create messages and put it in the queue.

```java

import java.util.concurrent.BlockingQueue;

public class Producer implements Runnable {

    private BlockingQueue<Message> queue;
    
    public Producer(BlockingQueue<Message> q){
        this.queue=q;
    }
    public void run() {
        for(int i=0; i<100; i++){
            Message msg = new Message(""+i);
            try {
                Thread.sleep(i);
                queue.put(msg);
                System.out.println("Produced "+msg.getMsg());
            } catch (InterruptedException e) {
                e.printStackTrace();
            }
        }
        Message msg = new Message("exit");
        try {
            queue.put(msg);
        } catch (InterruptedException e) {
            e.printStackTrace();
        }
    }

}

```

- Java BlockingQueue Example - Consumer: Consumer class that will process on the messages from the queue and terminates when exit message is received.

```java

import java.util.concurrent.BlockingQueue;

public class Consumer implements Runnable{

private BlockingQueue<Message> queue;
    
    public Consumer(BlockingQueue<Message> q){
        this.queue=q;
    }

    @Override
    public void run() {
        try{
            Message msg;
            while((msg = queue.take()).getMsg() !="exit"){
            Thread.sleep(10);
            System.out.println("Consumed "+msg.getMsg());
            }
        }catch(InterruptedException e) {
            e.printStackTrace();
        }
    }
}

```

- Java BlockingQueue Example - Service:we have to create BlockingQueue service for producer and consumer. This producer consumer service will create the BlockingQueue with fixed size and share with both producers and consumers. This service will start producer and consumer threads and exit.

```java

import java.util.concurrent.ArrayBlockingQueue;
import java.util.concurrent.BlockingQueue;

public class ProducerConsumerService {

    public static void main(String[] args) {
        BlockingQueue<Message> queue = new ArrayBlockingQueue<>(10);
        Producer producer = new Producer(queue);
        Consumer consumer = new Consumer(queue);
        new Thread(producer).start();
        new Thread(consumer).start();
        System.out.println("Producer and Consumer has been started");
    }

}

Output:
Producer and Consumer has been started
Produced 0
Produced 1
Produced 2
Produced 3
Produced 4
Consumed 0
Produced 5
Consumed 1
Produced 6
Produced 7
Consumed 2
Produced 8

```

</blockquote>

</details>

---

52. When is it appropriate to create multiple streams?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Multi-threaded applications are used in cases where the program can be divided into several relatively independent parts. In this case, so that one code does not wait for the other, they are placed in different threads.

As an example, a program with a graphical interface can be given – as long as any lengthy computations are performed in one thread, the interface can be accessible to the user and not hang if it is running in another thread.

</blockquote>

</details>
	
---

53.Explain the ways to create and run streams with examples?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

There are several ways to create and launch streams.

- Using a class that implements Runnable.Create an object of class Thread.Create a class object that implements the Runnable interface.

- Call the start () method on the created Thread object (after that, the run () method of the passed object that implements Runnable will start )using a class that extends Thread

- Create an object of class ClassName extends Thread .Override run () in this class,using a class that implements `java.util.concurrent.Callable`

- Create a class object that implements the Callable interface.

- Create an ExecutorService object with an indication of the thread pool.

- Create a future object. The launch takes place through the `submit()` method ,`Signature:  <T> Future <T> submit (Callable <T> task)`.

```java

public static void howToRunThreads() {
       ThreadClass threadClass = new ThreadClass(“First”);

       threadClass.start(); 

       Thread thread = new Thread(new RunnableClass(“Second”));

       Thread thread2 = new Thread(new RunnableClass(“Third”));

       Thread thread3 = new Thread(new RunnableClass(“Fourth”));

       thread.start(); 

       thread2.start(); 

       thread3.start(); 

   }

public class RunnableClass implements Runnable {

   private String localName;

   public RunnableClass() {

   }

   public RunnableClass(String localName) {

       this.localName = localName;

   }

 
   public void run() {

       System.out.println(“run() ” + localName + ” running”);

   }

   public String getLocalName() {return localName;}

   public void setLocalName(String localName) {this.localName = localName;}

}

public class ThreadClass extends Thread {

   public ThreadClass() {

   }

   public ThreadClass(String name) {

       super(name);

   }

   public ThreadClass(Runnable target) {

       super(target);

       System.out.println(target + ” will running”);

   }

   public void run() {

     System.out.println(“ThreadClass run() method ” + “Thread name is: ” + this.getName());

   }

}


ThreadClass run() method Thread name is: First

run() Third running

run() Fourth running

run() Second running 


public class CallableExample {
 public static class WordLengthCallable implements Callable {

   private String word;

   public WordLengthCallable(String word) {

     this.word = word;

   }

   public Integer call() {

     return Integer.valueOf(word.length());

   }

 }

 public static void main(String args[]) throws Exception {

   ExecutorService pool = Executors.newFixedThreadPool(3);

   Set<Future<Integer>> set = new HashSet<Future<Integer>>();

   for (String word: args) {

     Callable<Integer> callable = new WordLengthCallable(word);

     Future<Integer> future = pool.submit(callable);

     set.add(future);

   }

   int sum = 0;

   for (Future<Integer> future : set) {

     sum += future.get();

   }

   System.out.printf(“The sum of lengths is %s%n”, sum);

   System.exit(sum);

 }

}

```

</blockquote>

</details>

---
	
54. Which method starts a thread for execution?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

`Thread.start ()` starts a child thread. For the Callable interface, the thread is launched using the 
`submit()`method.

</blockquote>

</details>

---

55. When does the thread finish its execution?Explain with an example?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

The thread finishes execution when its `run()` or `call()` method completes. For the main thread, this is the `main()` method.

</blockquote>56.How to forcibly stop the flow of a thread?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

The Thread class contains a hidden boolean field called the interrupt flag. You can set this flag by calling the threads `interrupt()` method. There are two ways to check if this flag is set. The first way is to call the bool `isInterrupted()` method of the thread object, the second is to call the static method bool `Thread.interrupted()`.

The first method returns the state of the interrupt flag and leaves this flag intact. The second method returns the state of the flag and resets it. Notice that `Thread.interrupted()` is a static method of the Thread class, and calling it returns the value of the interrupt flag of the thread from which it was called. Therefore, this method is called only from within the thread and allows the thread to check its interrupt state.

Methods that suspend the execution of a thread, such as `sleep()`, `wait()` and `join()`, have one feature – if the `interrupt()` method of this thread is called during their execution, they will wait for the end of the wait time to throw an InterruptedException exception.

```java

public class JoinThread implements Runnable {
   public void run() {
       for (int i=0; i<100; i++) {
           if(!Thread.interrupted()) {
               System.out.println(i);
               try {
                   Thread.sleep(100);
               } catch (InterruptedException e) {
                   System.out.println(“InterruptedException!”);
                   System.err.println(“Exception msg: ” + e.getMessage());
                   return;
               }

           } else {
               System.out.println(“Interrupted!”);
               return;
           }
       }
   }
}
public class TestThread {
   public static void main(String[] args) {
       Thread thread = new Thread(new JoinClass());
       thread.start();
       try {
           Thread.sleep(1000); 
       } catch (InterruptedException e) {
           e.printStackTrace();
       }
       thread.interrupt();
   }
}

Output:

0

1

…

8

9 // counter was up to 100

InterruptedException!

Exception msg: sleep interrupted

```

In the `main()` method, we create an object of the JoinThread class and run it with the `run()` method  . First, it is checked whether this stream is already completed, and then the counter value is output every 100 ms.
He orders the main method to wait 1000ms so that the meter has time to count a little.Call the interrupt method on an object of the class JoinClass . After that, an exception is immediately caught in the loop and the return is raised in the catch block .


</blockquote>

</details>



</details>

---
	
56. How to use monitor in threads?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>


- Multiple threads can interfere with each other when accessing the same data. To solve this problem, a mutex was created (a monitor). It has two states – the object is busy and the object is free. Monitor (mutex) is a high-level mechanism for interaction and synchronization of threads, providing access to unshared resources.

- When a thread needs an object common to all threads, it checks the mutex associated with this object. If the mutex is free, the thread locks it (marks as busy) and starts using the shared resource. After she has done her work, the mutex is unlocked (marked as free).

- If the thread wants to use the object, and the mutex is blocked, then the thread falls asleep while waiting. When the mutex is finally released by a busy thread, our thread will immediately block it and start work. The mutex is built into the Object class and therefore every object has it.

- When one thread goes inside a block of code marked with the word synchronized, the Java machine immediately blocks the mutex of the object, which is indicated in parentheses after the word synchronized.

- No other thread can enter this block until our thread leaves it. As soon as our thread comes out of the block marked synchronized, the mutex will immediately unlock automatically and be free to be captured by another thread. If the mutex was busy, then our thread will stand still and wait for it to be released.

</blockquote>

</details>
	
---
	
57. How to suspend the flow of a thread?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

`Thread.sleep ()` is a static method of class Thread, which suspends the execution of the thread in which it was called. During the execution of the `sleep()` method, the system stops allocating CPU time to the thread, distributing it among other threads.The `sleep()` method can run either for a specified amount of time (milliseconds or nanoseconds) or until it is stopped by an interrupt 

</blockquote>

</details>

---
	
58. Explain the functionality of the notify and notifyAll methods with examples?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

The notify method awakens one of the threads that called the `wait()` method on this monitor. The notifyAll method wakes up all threads. The order of execution in this case will be determined by the priority of the thread.

```java

public class NotifyClass {
   private List synchedList;
   public NotifyClass() {
       synchedList = Collections.synchronizedList(new LinkedList());
   }
   public String removeElement() throws InterruptedException {
       synchronized (synchedList) {
           while (synchedList.isEmpty()) {
               System.out.println("List is empty");
               synchedList.wait();
               System.out.println("Waiting");
           }
           String element = (String) synchedList.remove(0);
           return element;
       }
   }
   public void addElement(String element) {
       System.out.println("Opening");
       synchronized (synchedList) {
           synchedList.add(element);
           System.out.println("New Element:'" + element + "'");
           synchedList.notifyAll();
           System.out.println(“notifyAll called”);
       }
       System.out.println(“Closing”);
   }

   public static void main(String[] args) {
       final NotifyClass demo = new NotifyClass();
       Runnable runA = new Runnable() {
        public void run() {
               try {
                   String item = demo.removeElement();
                   System.out.println(“” + item);
               } catch (InterruptedException ix) {
                   System.out.println(“Interrupted Exception”);
               } catch (Exception x) {
                   System.out.println(“Exception thrown.”);
               }
           }
       };
       Runnable runB = new Runnable() {
           public void run() {
               demo.addElement(“Hello”);
           }
       };

       try {
           Thread threadA1 = new Thread(runA, “A”);
           threadA1.start();
           Thread.sleep(500);
           Thread threadA2 = new Thread(runA, “B”);
           threadA2.start();
           Thread.sleep(500);
           Thread threadB = new Thread(runB, “C”);
           threadB.start();
           Thread.sleep(1000);
           threadA1.interrupt();
           threadA2.interrupt();

       } catch (InterruptedException x) {
       }
   }
}

Output:
List is empty
List is empty
Opening
New Element:Hello
notifyAll called
Closing
Waiting
Waiting
List is empty
Hello
Interrupted Exception

```


</blockquote>

</details>

59. Explain the implementation of `join()` method?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

One thread can call the `join()` method on another thread. As a result, the first thread (which called the method) suspends its work and waits for the second thread to finish (the object whose `call()` method was called).

```java

public class Testthread {
   public static void main(String[] args) {
       Thread threadExample = new Thread(new JoinClass());
       threadExample.start();
       try {
           threadExample.join(); 
       } catch (InterruptedException e) {
           e.printStackTrace();
       }
       System.out.println(“END: ” + Calendar.getInstance().getTime());
   }
}
public class Jointhread implements Runnable {
   public void run() {
             System.out.println(“Jointhread.run() ” + Calendar.getInstance().getTime());
       try {
           Thread.sleep(1000);
       } catch (InterruptedException e) {
           e.printStackTrace();
       }
       System.out.println(“aftersleep ” + Calendar.getInstance().getTime());
   }
}

Output:

JoinClass.run() Tue Jan 19 00:00:37 MSK 2022

afterSleep Tue Jan 19 00:00:42 MSK 2022

END: Tue Jan 19 00:00:42 MSK 2022

```

After launching the main method , the main thread of the TestClass class is created .
Then we create a thread test threadExample and run it. We set the thread to stupit 5 seconds inside the `Jointhread.run()` method .Then we call the `join()` method on the second thread. At this point, the main thread connects to our second thread and waits for it to complete.We look at what time has passed – 1 second. Those. the main thread waited for threadExample to complete before going to the `System.out.println()` method . Otherwise, `System.out.println("END:")` was  executed immediately without waiting for threadExample to go.

</blockquote>

</details>

---
	
60.Explain the concept of "interlocking" with examples?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Interlocking,  is also called as deadlock, a phenomenon in which all threads are in standby mode. To reduce the chance of a deadlock, it is not recommended to use the `wait()` and `notify()` methods.

```java

final Object lock1 = new Object();
final Object lock2 = new Object();

// There will be deadlock

   void method01() {
       synchronized(lock1) {
           synchronized(lock2) {
           //doSomething()
           }
       }
   }
   void method1() {
       synchronized(lock2) {
           synchronized(lock1) {
           //doSomething()
           }
       }
   }

To avoid deadlock, you can use only one synchronized block, refuse from wait-notify, or use the following construction:

//To avoid deadlock
//If you can’t use only one lock, then use this scheme
   void method2() {
       if (identityHashCode(lock1)>=identityHashCode(lock2)) {
           synchronized(lock1) {
               synchronized(lock2) {
                 //doSomething()
               }
           }
       }
       else {
           synchronized(lock2) {
               synchronized(lock1) {
               //doSomething()
               }
           }
       }
   }

```

</blockquote>

</details>
	
---
	
61.What is a ThreadGroup and why is it needed?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

ThreadGroup is a set of threads that can also contain other groups of threads. A group of threads forms a tree in which every other group of threads has a parent (except the original one). A thread has the right to access data from its thread group, but does not have such access to other groups or to the parent group of threads.

</blockquote>

</details>


---
	
62.Why Thread Pool is needed?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Thread pools (threads) are a managed collection of threads that are available for various tasks. Thread pools usually provide increased productivity when performing a large number of tasks due to the reduction of overhead costs for the challenge of each task.It is a means of limiting the expenditure of resources when performing a set of tasks.Eliminate the need for thread life cycle management.

</blockquote>

</details>
	
---
	
63.How race condition is occurred in threads.Explain with an example?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

A condition in which the critical section or a part of the program where shared memory is accessed and  is concurrently executed by two or more threads. It leads to incorrect behavior of a program.A race condition is a  condition in which two or more threads compete together to get certain shared resources.For example, if thread A is reading data from the linked list and another thread B is trying to delete the same data. This process leads to a race condition that may result in run time error.

There are two types of race conditions:

- Read-modify-write
- Check-then-act

The read-modify-write patterns signify that more than one thread first read the variable, then alter the given value and write it back to that variable. 

```java


public class number  
{  
protected long number = 0;  
public void add(long value)  
{  
this.number = this.number + value;  
}  
}  

```

It occurs when two or more threads operate on the same object without proper synchronization and their operation incorporates each other.Suppose, there are two processes A and B that are executing on different processors. Both processes are trying to call the function bankAccount() concurrently. The value of the shared variable that we are going to pass in the function is 1000.

Consider, A call the function bankAccount() and passing a value 200 as a parameter. In the same way, process B is also calling the function bankAccount() and passing a value of 100 as a parameter.

```java

class Counter implements Runnable{  
private int c = 0;  
public void increment(){  
try{  
Thread.sleep(10);  
}   
catch (InterruptedException e){   
e.printStackTrace();  
}  
c++;  
}  
public void decrement(){      
c--;  
}  
public int getValue(){  
return c;  
}  
public void run(){   
this.increment();  
System.out.println("Value for Thread After increment " + Thread.currentThread().getName() + " " + this.getValue());  
this.decrement();  
System.out.println("Value for Thread at last " + Thread.currentThread().getName() + " " + this.getValue());        
}  
}  
public class RaceDemo  
{  
public static void main(String args[])   
{  
Counter counter = new Counter();  
Thread t1 = new Thread(counter, "Thread-1");  
Thread t2 = new Thread(counter, "Thread-2");  
Thread t3 = new Thread(counter, "Thread-3");  
t1.start();  
t2.start();  
t3.start();  
}      
}  

Output:
Value for Thread After increment Thread-1 2
Value for Thread at last Thread-1 2
Value for Thread After increment Thread-3 3
Value for Thread at last Thread-3 1
Value for Thread After increment Thread-2 2
Value for Thread at last Thread-2 0

```

</blockquote>

</details>

	
---
	
64.How Race condition can be avoided.Explain with an example?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

There are the following two solutions to avoid race conditions.

- Mutual exclusion:The solution to avoid race condition is mutual exclusion. In mutual exclusion, if a thread is using a shared variable or thread, another thread will exclude itself from doing the same thing.

- Synchronize the process:In order to prevent the race conditions, one should ensure that only one process can access the shared data at a time. It is the main reason why we need to synchronize the processes.

```java

class Counter implements Runnable{  
private int c = 0;  
public void increment(){  
try{  
Thread.sleep(10);  
}   
catch (InterruptedException e){  
e.printStackTrace();  
}  
c++;  
}  
public void decrement(){      
c--;          
}  
public int getValue(){  
return c;  
}    
public void run() {  
synchronized(this) {   
this.increment();  
System.out.println("Value for Thread After increment " + Thread.currentThread().getName() + " " + this.getValue());  
this.decrement();  
System.out.println("Value for Thread at last " + Thread.currentThread().getName() + " " + this.getValue());  
}          
}  
}  
public class RaceAvoidDemo  
{  
public static void main(String args[])   
{  
Counter counter = new Counter();  
Thread t1 = new Thread(counter, "Thread-1");  
Thread t2 = new Thread(counter, "Thread-2");  
Thread t3 = new Thread(counter, "Thread-3");  
t1.start();  
t2.start();  
t3.start();  
}      
}  

Output:

Value for Thread After increment Thread-1 1
Value for Thread at last Thread-1 0
Value for Thread After increment Thread-3 1
Value for Thread at last Thread-3 0
Value for Thread After increment Thread-2 1
Value for Thread at last Thread-2 0

It can be seen from the output how threads are accessing the shared resource one at a time now. Synchronizing the access within the `run()` method made it happen.

```

</blockquote>

</details>

---
	
65.Describe the functionality of  yield method in a Thread-class?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

The `yield()` method of thread class causes the currently executing thread object to temporarily pause and allow other threads to execute.

```java

public class YieldThread extends Thread{  
    public void run(){  
        for (int i=0; i<3 ; i++)  
            System.out.println(Thread.currentThread().getName() + " in control");  
    }  
    public static void main(String[]args){  
        YieldThread t1 = new YieldThread();  
        YieldThread t2 = new YieldThread();   
        t1.start();  
        t2.start();  
        for (int i=0; i<3; i++)  
        {  
            t1.yield();  
            System.out.println(Thread.currentThread().getName() + " in control");  
        }  
    }  
} 

Output:

main in control
main in control
main in control
Thread-0 in control
Thread-0 in control
Thread-0 in control
Thread-1 in control
Thread-1 in control
Thread-1 in control

```

</blockquote>

</details>





	



