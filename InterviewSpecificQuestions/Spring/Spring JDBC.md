## Technical

1.Why do we need `Spring JDBC` when we already have Java JDBC?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- `JDBC` is the core API to connect your java application with any database vendor.
- When we use Java `JDBC` there are multiple configuration steps, starting from loading the river to closing the DB connection developer has to manage.
- When we use the `Spring JDBC` module under the Spring framework, it takes care of all low-level common `JDBC` operations and allows the developer to focus only on business logic.
</blockquote> 

</details>

---

2.What is `DataSource` in Java application?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- `DataSource` is a factory for connections to the physical data source.
- In enterprise applications, the `DataSource` object is the preferred means of getting a connection to your database.
  
</blockquote> 

</details>

---

3.What are the three types of implementations of `DataSource` in Java applications?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- The `DataSource` interface is implemented by a driver vendor.There are three types of implementations:
    - `Basic implementation` - produces a standard Connection object
    - `Connection pooling implementation` -- produces a Connection object that will automatically participate in connection pooling.
    - `Distributed transaction implementation` -- produces a Connection object that may be used for distributed transactions and almost always participates in connection pooling.

</blockquote> 

</details>

---
4.What is `Connection Pooling` in an enterprise application?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- `Connection pooling` is a technique of creating and managing a pool of connections that are reused rather than created each time a connection is requested.
- `Connection pooling` can greatly increase the performance of your Java application, while reducing overall resource usage.
-  Connection pool is a memory cache of database connections which is maintained by a connection pooling provider as a layer on top of any standard JDBC driver.

</blockquote> 

</details>

---
5.What default connection pool does spring boot use?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- `Spring Boot` uses `HikariCP` as the default connection pool.
- `HikariCP` has great performance and concurrency.

</blockquote> 

</details>

---

6.What connection pool does spring boot supports?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Spring Boot supports various popular connection pool providers as listed below:
    - `HikariCP`
    - `Tomcat pooling Datasource`
    - `Commons DBCP2`
    - `Oracle UCP & OracleDataSource`
    - `Spring Framework’s SimpleDriverDataSource`
    - `H2 JdbcDataSource`
    - `PostgreSQL PGSimpleDataSource`
    - `C3P0`

</blockquote> 

</details>

---
7.What is the sequence of choosing various connection pools inside the Spring application?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Spring Boot uses the following algorithm for choosing a specific implementation:
    - If HikariCP is available, Spring always chooses it.
    - Otherwise, if the Tomcat pooling DataSource is available, Spring will use it.
    - Otherwise, if Commons `DBCP2` is available, Spring will use that.
- If none of `HikariCP`, `Tomcat`, and `DBCP2` are available and if `Oracle UCP` is available, Spring will use it.

</blockquote> 

</details>

---
8.What is `Programmatic & Declarative Transaction Management` in the Spring application?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Spring provides both `Programmatic` and `Declarative` transaction management.
- In Programmatic Transaction management we have transaction management code surrounding our business code.
- It gives extreme flexibility but is difficult to maintain.
- Whereas in Declarative Transaction management we separate the transaction management code from the business code.
- We can configure Declarative Transaction management using both annotations and XML-based configuration.
- Most Spring Framework users choose declarative transaction management as this option has the least impact on application code.
- To summarize, Programmatic Transaction management is more flexible during development time but less flexible during application life.whereas Declarative Transaction management is less flexible during development time but more flexible during the application life

 </blockquote> 

</details>

---
9.What does isolation and propagation attributes denote in @Transactional annotation e.g.`@Transactional(isolation = xxx, propagation = xxx)`?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- While using Declarative Transaction management we can provide isolation & propagation attributes which serve below purpose:
    - `Isolation`: The degree to which this transaction is isolated from the work of other transactions.For example, can this transaction see uncommitted writes from other transactions?
    - `Propagation`: Typically, all code within a transaction scope runs in that transaction.However, you can specify the behaviour if a transactional method is run when a transaction context already exists.For example, code can continue running in the existing transaction (the common case), or the existing transaction can be suspended, and a new transaction created.

</blockquote> 

</details>

---
10.What configurations do `Spring JDBC` & developer need to perform in the application?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- The table shows which actions Spring takes care of and which are developers’ responsibilities.
  
| **Steps** | **Action**                                               | **Spring** | **Developer** |
| --------- | -------------------------------------------------------- | ---------- | ------------- |
| 1         | Define connection parameters.                           |            | X             |
| 2         | Open the connection.                                    | X          |               |
| 3         | Specify the SQL statement.                              |            | X             |
| 4         | Declare parameters and provide parameter values          |            | X             |
| 5         | Prepare and run the statement.                          | X          |               |
| 6         | Set up the loop to iterate through the results (if any).| X          |               |
| 7         | Do the work for each iteration.                         |            | X             |
| 8         | Process any exception.                                  | X          |               |
| 9         | Handle transactions.                                    | X          |               |
| 10        | Close the connection, the statement, and the result set.| X          |               |

</blockquote> 

</details>

---
