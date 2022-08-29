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

26. What do you mean by busy spinning?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>


Busy Spinning, also known as Busy-waiting, is a technique in which one thread waits for some condition to happen, without calling wait or sleep methods and releasing the CPU. In this condition, one can pause a thread by making it run an empty loop for a certain time period, and it does not even give CPY control. Therefore, it is used to preserve CPU caches and avoid the cost of rebuilding cache

</blockquote>

</details>

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

Nothing will happen as such if we don’t override the `run() method. The compiler will not show any error. It will execute the `run()` method of thread class and we will just don’t get any output because the `run()` method is with an empty implementation. 

Example:  

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


- Advantages of using Lock interface over Synchronization block: 
Methods of Lock interface i.e., `Lock()` and `Unlock()` can be called in different methods. It is the main advantage of a lock interface over a synchronized block because the synchronized block is fully contained in a single method.  
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

