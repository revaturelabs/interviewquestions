##Technical

1. What are Threads?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>

A process is a program in execution. A thread is a subset of a process.

</blockquote>
</details>

--- 

2. How do you make a thread in java? or how do you create thread?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>

In Java, we can create a thread using

1. By Extending the Thread class
2. By Implementing Runnable interface in Java

 
</blockquote>
</details>

--- 

3. What is the life cycle of a thread?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details>
  <summary> <b>Show Answer</b></summary>
  
<blockquote>

At any given time, a thread can be in one of these states:

- New: newly created thread that has not started executing
- Runnable: either running or ready for execution but waiting for its resource allocation
- Blocked: waiting to acquire a monitor lock to enter or re-enter a synchronized block/method
- Waiting: waiting for some other thread to perform an action without any time limit
- Timed_Waiting: waiting for some other thread to perform a specific action for a specified time period
- Terminated: has completed its execution
 
</blockquote>
</details>

--- 

4.How can we differentiate `notify()` and `notifyAll()` methods ?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>


- `notify()`: It sends a notification and wakes up only a single thread instead of multiple threads that are waiting on the object’s monitor.

- `notifyAll()`: It sends notifications and wakes up all threads and allows them to compete for the object's monitor instead of a single thread. 

</blockquote>

</details>

---

5. Explain synchronization process? Why we use it?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Synchronization in java is the capability to control the access of multiple threads to any shared resource. In the Multithreading concept, multiple threads try to access the shared resources at a time to produce inconsistent results. The synchronization is necessary for reliable communication between threads.

</blockquote>
</details>

---

6. Explain thread starvation?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

Thread starvation is basically a situation or condition where a thread won’t be able to have regular access to shared resources and therefore is unable to proceed or make progress. This is because other threads have high priority and occupy the resources for too long. This usually happens with low-priority threads that do not get CPU for its execution to carry on. 

</blockquote>

</details>

---

7. Can you start a thread twice?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>

No, it's not at all possible to restart a thread once a thread gets started and completes its execution. Thread only runs once and if you try to run it for a second time, then it will throw a runtime exception i.e., `java.lang.IllegalThreadStateException`. 

</blockquote>

</details>

---

8. What is a deadlock?

<details><summary><b> Show Answer</b></summary>

<blockquote>

A deadlock condition occurs when two or more threads are blocking the resources and waiting for each other to release the resource. Consider for example, If one thread acquires a lock on one resource and then attempts to lock another resource that is already locked by another thread that is waiting for the first thread to release the lock on the first resource. So in this condition, a deadlock occurs. To prevent deadlock conditions we can avoid nested locks.

</blockquote>

</details>

---

9. What are the types of threads?

<details><summary><b> Show Answer</b></summary>

<blockquote>

There are two types of threads: daemon threads and user threads. User threads are created by the Java application and are used to perform application-specific tasks. Daemon threads are low-priority threads created by the JVM that run in the background and support the user threads.

</blockquote>

</details>

10. How do you do multi-threading?

<details><summary><b> Show Answer</b></summary>

<blockquote>

Multithreading in java allows a program to perform multiple tasks concurrently, which can improve the performance of the application. Threads in Java can be created by using two ways. The first way to create a thread in Java is by implementing the Runnable interface and the second way is by extending the Thread class.

</blockquote>

</details>

---

11. If you are approaching a situation where you are running out of memory what should you do? (thread dump)

<details><summary><b> Show Answer</b></summary>

<blockquote>

If you are running out of memory in a Java application, there are several steps you can take to diagnose and resolve the issue:

`Take a thread dump`: A thread dump provides a snapshot of the current state of the Java Virtual Machine (JVM), including all threads and their current stack traces. You can use tools like jstack or VisualVM to take a thread dump. Analyzing the thread dump can give you insights into which threads are consuming the most memory and help you identify potential memory leaks.

</blockquote>

</details>

---

12. What is concurrency in Multithreading?

<details><summary><b> Show Answer</b></summary>

<blockquote>

Concurrency in multithreading refers to the ability of multiple threads to run simultaneously and make progress on a task. This is achieved by the CPU rapidly switching between executing different threads, giving the illusion of parallelism. Concurrency can improve program performance by utilizing the available system resources more effectively. 

</blockquote>

</details>

---

13. Can you list out the thread methods?

<details><summary><b> Show Answer</b></summary>

<blockquote>

Sure, here are some of the commonly used methods in the Thread class:

`start()`: Starts the execution of the thread by calling the run() method.
`run()`: Contains the code that is executed when the thread is started.
`sleep(long millis)`: Causes the current thread to sleep for the specified number of milliseconds.
`join()`: Waits for the thread to die.
`interrupt()`: Interrupts the thread, causing it to stop executing.
`isInterrupted()`: Checks whether the thread has been interrupted.
`yield()`: Causes the thread to yield its current use of the CPU.
`setName(String name)`: Sets the name of the thread.
`setPriority(int priority)`: Sets the priority of the thread.
`getState()`: Returns the state of the thread.

</blockquote>

</details>

---

14. Is Java a single threaded or multi threaded programming language?

<details><summary><b> Show Answer</b></summary>

<blockquote>

Java supports both single-threaded and multi-threaded programming. It allows programmers to create and manage multiple threads of execution within a single program. Therefore, Java is a multi-threaded programming language.

</blockquote>

</details>

---

15. How would you make three threads execute at the same time?

<details><summary><b> Show Answer</b></summary>

<blockquote>

In Java, you can make three threads execute at the same time by using the Thread class and its associated methods. Here's a sample code that creates three threads and runs them concurrently:

```Java
public class ThreeThreadsExample {
    public static void main(String[] args) {
        // Create three threads
        Thread thread1 = new Thread(new MyRunnable(), "Thread 1");
        Thread thread2 = new Thread(new MyRunnable(), "Thread 2");
        Thread thread3 = new Thread(new MyRunnable(), "Thread 3");

        // Start all three threads
        thread1.start();
        thread2.start();
        thread3.start();

        // Wait for all three threads to complete
        try {
            thread1.join();
            thread2.join();
            thread3.join();
        } catch (InterruptedException e) {
            System.out.println("Main thread interrupted");
        }

        System.out.println("All threads have finished executing");
    }

    private static class MyRunnable implements Runnable {
        public void run() {
            System.out.println(Thread.currentThread().getName() + " is starting");

            // Do some processing here

            System.out.println(Thread.currentThread().getName() + " is finishing");
        }
    }
}

```

</blockquote>

</details>

---

16. What is multithreading and multiprocessing?

<details><summary><b> Show Answer</b></summary>

<blockquote>

In Java, multithreading is the ability to execute multiple threads within the same process concurrently, whereas multiprocessing is the ability to execute multiple processes concurrently, each with its own memory space and resources. Both multithreading and multiprocessing are used to achieve parallelism and improve the performance of software applications.

</blockquote>

</details>

---

17. Can you tell us the pros/cons of multithreading?

<details><summary><b> Show Answer</b></summary>

<blockquote>

**Pros**:

`Improved performance`: Multithreading can improve the performance of an application by allowing multiple threads to execute simultaneously and thus utilizing available resources more efficiently.
`Responsiveness`: Multithreading can improve the responsiveness of an application by allowing the UI thread to remain responsive while other threads perform long-running tasks.
`Resource sharing`: Multithreading enables multiple threads to share the same resources, such as memory and I/O devices, which can result in better resource utilization and reduced overhead.

**Cons**:

`Complexity`: Multithreading can make an application more complex and difficult to debug due to the increased complexity of managing multiple threads.
`Synchronization`: Multithreading requires careful management of shared resources to avoid synchronization issues, such as race conditions and deadlocks.
`Overhead`: Multithreading can introduce overhead due to the additional management required to create, manage, and synchronize threads, which can result in reduced performance if not implemented properly.

</blockquote>

</details>

---

18. Do you know how to initialize a thread in Java?

<details><summary><b> Show Answer</b></summary>

<blockquote>

Yes, in Java, there are two ways to initialize a thread:

1. `Extending the Thread class`: You can create a new class that extends the Thread class and override the run() method to define the thread's behavior. Then you can create an instance of the new class and call its start() method to start the thread.

```Java
class MyThread extends Thread {
    public void run() {
        // Define thread behavior here
    }
}
// Create and start the thread
MyThread thread = new MyThread();
thread.start();
```

2. `Implementing the Runnable interface`: You can create a new class that implements the Runnable interface and override the run() method to define the thread's behavior. Then you can create an instance of the new class and pass it to the Thread constructor to create a new thread object. Finally, you can call the start() method on the thread object to start the thread.

```java

class MyRunnable implements Runnable {
    public void run() {
        // Define thread behavior here
    }
}

// Create and start the thread
MyRunnable runnable = new MyRunnable();
Thread thread = new Thread(runnable);
thread.start();
```

Both methods are valid ways to create and initialize a thread in Java, and which one you choose depends on your specific needs and preferences.

</blockquote>

</details>

---

19. What does the keyword synchronize mean in Java?

<details><summary><b> Show Answer</b></summary>

<blockquote>

In Java, the synchronized keyword is used to control access to shared resources by multiple threads. When a method or block of code is declared as synchronized, only one thread can access the code at a time, while other threads are blocked until the first thread has completed its execution.

```Java

public class Counter {
    private int count = 0;

    public synchronized void increment() {
        count++;
    }

    public synchronized void decrement() {
        count--;
    }

    public synchronized int getCount() {
        return count;
    }
}

```

</blockquote>

</details>

---

20. Do you know anything about Synchronized list in Java?

<details><summary><b> Show Answer</b></summary>

<blockquote>

In Java, the java.util.Collections class provides a convenient way to synchronize access to a list by wrapping it in a synchronized collection. This is done by calling the Collections.synchronizedList() method, which returns a synchronized (thread-safe) list backed by the specified list.

Here's an example code snippet:

```Java

List<String> myList = new ArrayList<String>();
List<String> synchronizedList = Collections.synchronizedList(myList);

// Accessing synchronized list from multiple threads
synchronized (synchronizedList) {
    // Access or modify the synchronized list here
}

```

</blockquote>

</details>

---

21. How do you implement runnable in java? short answer

<details><summary><b> Show Answer</b></summary>

<blockquote>

To implement Runnable in Java, you need to follow these steps:

- Create a class that implements the Runnable interface.
- Override the run() method in the Runnable interface with the code you want to execute in the thread.
- Create an instance of the class you just created.
- Create a Thread object, passing in the instance of the class you created as a constructor argument.
- Call the start() method on the Thread object to start the thread.

Here's an example code snippet:

```Java
public class MyRunnable implements Runnable {
    @Override
    public void run() {
        // Code to execute in the thread
    }
}

// Create an instance of the class that implements Runnable
MyRunnable myRunnable = new MyRunnable();

// Create a Thread object and pass in the instance of the class that implements Runnable
Thread thread = new Thread(myRunnable);

// Start the thread
thread.start();
```

</blockquote>

</details>

---

22. How can you make a singleton thread-safe in Java?

<details><summary><b> Show Answer</b></summary>

<blockquote>

To make a singleton thread-safe in Java, you can use the double-checked locking pattern, which ensures that only one instance of the singleton is created, even in a multithreaded environment.

Here's an example code snippet:

```Java
public class MySingleton {
    private static volatile MySingleton instance;

    private MySingleton() {
        // Private constructor to prevent instantiation
    }

    public static MySingleton getInstance() {
        if (instance == null) {
            synchronized (MySingleton.class) {
                if (instance == null) {
                    instance = new MySingleton();
                }
            }
        }
        return instance;
    }
}
```

</blockquote>

</details>

---
