1. What are Threads?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1">
  <summary> <b>Show Answer</b></summary>
  
<blockquote markdown="1">

A process is a program in execution. A thread is a subset of a process.

</blockquote>
</details>

--- 

2. How do you make a thread in java? or how do you create thread?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1">
  <summary> <b>Show Answer</b></summary>
  
<blockquote markdown="1">

In Java, we can create a thread using

1. By Extending the Thread class
2. By Implementing Runnable interface in Java

 
</blockquote>
</details>

--- 

3. What is the life cycle of a thread?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1">
  <summary> <b>Show Answer</b></summary>
  
<blockquote markdown="1">

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

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1"><summary><b> Show Answer</b></summary>

<blockquote markdown="1">


- `notify()`: It sends a notification and wakes up only a single thread instead of multiple threads that are waiting on the object’s monitor.

- `notifyAll()`: It sends notifications and wakes up all threads and allows them to compete for the object's monitor instead of a single thread. 

</blockquote>

</details>

---

5. Explain synchronization process? Why we use it?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1"><summary><b> Show Answer</b></summary>

<blockquote markdown="1">

Synchronization in java is the capability to control the access of multiple threads to any shared resource. In the Multithreading concept, multiple threads try to access the shared resources at a time to produce inconsistent results. The synchronization is necessary for reliable communication between threads.

</blockquote>
</details>

---

6. Explain thread starvation?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1"><summary><b> Show Answer</b></summary>

<blockquote markdown="1">

Thread starvation is basically a situation or condition where a thread won’t be able to have regular access to shared resources and therefore is unable to proceed or make progress. This is because other threads have high priority and occupy the resources for too long. This usually happens with low-priority threads that do not get CPU for its execution to carry on. 

</blockquote>

</details>

---

7. Can you start a thread twice?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1"><summary><b> Show Answer</b></summary>

<blockquote markdown="1">

No, it's not at all possible to restart a thread once a thread gets started and completes its execution. Thread only runs once and if you try to run it for a second time, then it will throw a runtime exception i.e., `java.lang.IllegalThreadStateException`. 

</blockquote>

</details>

---


