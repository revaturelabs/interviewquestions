1.Explain about StringBuffer?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details>
    <summary><b> Show Answer </b></summary> 
<blockquote>

- StringBuffer is in `java.lang package`.
- StringBuffer is mutable strings that are stored in heap memory.
- StringBuffer is synchronized methods.
- StringBuffer is not thread safe, so the performance is less than the string buffer.
</blockqoute> 
</details>

---

2.Explain the difference between StringBuffer and StringBuilder.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details>
    <summary><b> Show Answer </b></summary> 
<blockquote>

|                                 **StringBuffer**                                 |                                  **StringBuilder**                                  |
|:----------------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| StringBuffer is mutable strings that are stored in heap memory.              | StringBuilders are also mutable strings that are stored in heap memory.         |
| StringBuffer is thread safe. At a time only one thread is allowed to access. | StringBuilder is not thread-safe. At a time many threads are allowed to access. |
| The methods of StringBuffer are synchronized.                                | The methods of StringBuilder are non-synchronized.                              |
| The performance is less than StringBuilder.                                  | The performance is more than StringBuffer.                                      |
</blockqoute> 
</details>

---
