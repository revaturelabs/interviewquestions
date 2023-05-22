## Technical

1. What is the difference between `Spring JDBC` and `Spring Data JDBC`?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- `Spring JDBC`, a sub-module under the Spring framework project, provides Spring abstractions over the plain JDBC `DataSource` that we can use with the Spring Framework.
- `Spring JDBC` nicely hooks support for `Transaction Management`, `Exception Handling`, `DB connection management`, `Connection pool configuration`, avoiding boilerplate code using `JdbcTemplate` etc.
- `Spring Data JDBC`, a sub-module under the Spring Data project, makes it easy to implement JDBC-based repositories.
- `Spring Data JDBC` is an Object Relational Mapper (ORM) based on the `Repository` abstraction.
- `Spring Data JDBC` nicely hooks support for `CrudRepository`, `@Query`, `PagingAndSortingRepository`, `@Value` in persistence constructors etc. 

</blockquote> 

</details>

---

2. What do you mean by database dialect? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- A database dialect is a configuration setting for platform-independent software (`JPA`, `Hibernate`, etc.) which allows such software to translate its generic SQL statements into vendor-specific DDL, DML.
</blockquote> 

</details>

---

3. Why does Spring Data JDBC need database dialect?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- One of the core features of `Spring Data JDBC` is to generate automatic queries using `CrudRepository` for vendor-specific databases.
- To generate the queries `Spring Data JDBC` internally uses database dialects.
</blockquote> 

</details>

---

4. `Spring Data JDBC` includes direct support for which database dialects?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- In terms of databases, `Spring Data JDBC` requires a dialect to abstract common `SQL` functionality over vendor-specific flavors. 
- `Spring Data JDBC` includes direct support for the following databases:
    - `DB2`
    - `H2`
    - `HSQLDB`
    - `MariaDB`
    - `Microsoft SQL Server`
    - `MySQL`
    - `Oracle`
    - `Postgres`
</blockquote> 

</details>

---

5. Why do we use `PagingAndSortingRepository` in Spring?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- `Spring Data JDBC` sub-module under the Spring Data project provides `PagingAndSortingRepository` which is an extension of `CrudRepository` to provide additional methods to retrieve entities using the pagination and sorting abstraction.

</blockquote> 

</details>

---
6. The `CrudRepository` interface does not have an `update` method then how do we update the record in the database? 

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- `CrudRepository` has only `save` but it acts as an `update` as well.
- When we `save` an entity with an empty `id` it will do a save.
- When you do `save` on the entity wan its existing `id` it will do an `update`.
- This means after we used findById and changed something in returned object, we can call save on that object and it will do an update because after findById you get an object with a populated id that exists in our database.
- `save` in `CrudRepository` can accept a single entity or Iterable of our entity type.
</blockquote> 

</details>

---
7. Is it mandatory to call the `save` method to update an object inside a transactional method for `CrudRepository`?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Calling the `save` method to update an object inside a transactional method is not mandatory.
- When we use the `findById` method to retrieve an entity within a transactional method, the returned entity is managed by the persistence provider. 
- Hence, any change to that entity will be automatically persisted in the database, regardless of whether we are invoking the save method inside a transactional method.
</blockquote> 

</details>

---
8. What is the use of `@Query` annotation in Spring Data?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- `Spring Data` provides multiple ways to define a query that we can execute.
- One of these popular methods is using `@Query` annotation.
- We can annotate the `Spring Data` repository method with the `@Query` annotation where its `value` attribute contains the `JPQL` or `SQL` to be executed.
- It's a convenient approach to place a query definition just above the method inside the repository rather than inside our domain model as named queries.
</blockquote> 

</details>

---
9. Explain the query builder mechanism in the Spring Data repository?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- The query builder mechanism built into the `Spring Data` repository infrastructure is useful for building constraining queries over entities of the repository.
- The query method names are divided into `subject` and `predicate`.
- The first part (`find…By`, `exists…By`) defines the subject of the query, and the second part forms the predicate.
- Few Queries subject keywords - `find…By`, `get…By`, `count…By`, `…Distinct…`, `delete…By`,`Top<number>…`
- Few Queries predicate keywords - `Containing`, `After`, `Before`, `Between`, `EndingWith`, `StartsWith`, `LessThan`, `GreaterThan`
- Few Query predicate modifier keywords - `IgnoreCase`, `OrderBy…`
- Example-
```java
interface PersonRepository extends Repository<Person, Long> {

  List<Person> findByEmailAddressAndLastname(EmailAddress emailAddress, String lastname);

  // Enables the distinct flag for the query
  List<Person> findDistinctPeopleByLastnameOrFirstname(String lastname, String firstname);
  List<Person> findPeopleDistinctByLastnameOrFirstname(String lastname, String firstname);

  // Enabling ignoring the case for an individual property
  List<Person> findByLastnameIgnoreCase(String lastname);
 
  // Enabling ignoring the case for all suitable properties
  List<Person> findByLastnameAndFirstnameAllIgnoreCase(String lastname, String firstname);

  // Enabling static ORDER BY for a query
  List<Person> findByLastnameOrderByFirstnameAsc(String lastname);
  List<Person> findByLastnameOrderByFirstnameDesc(String lastname);
}
```

</blockquote> 

</details>

---
10. How you will implement the `SQL` `LIKE` query in Spring Data using method names? Give an example.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Let’s consider the Login entity comprising the userId attribute.
- There can be four different variations of LIKE query formed using method names as follows:
  - Exact Match `SELECT ... LIKE userId`
    - `List<User> findByUserIdLike(String userId);`
  - Starting With `SELECT ... LIKE userId%`
    - `List<User> findByUserIdStartingWith(String userId);`
  - Ending With `SELECT ... LIKE %userId`
    - `List<User> findByUserIdEndingWith(String userId);`
  - In Between `SELECT ... LIKE %userId%`
    - `List<User> findByUserIdContaining(String userId);`
</blockquote> 

</details>

---
11. What is `Spring Data JPA`?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- `Spring Data JPA`, a sub-module under the Spring Data project, makes it easy to implement `JPA` based repositories.
- `Spring Data JPA` provides repository support for the `Java Persistence API (JPA)`. 
- It eases the development of applications that need to access JPA data sources. 
- `Spring Data JPA` nicely hooks support for `JpaRepository`, `Hibernate`, `OpenJPA`, `EclipseLink`, `Querydsl`, `@Modifying`
</blockquote> 

</details>

---
12.  What is the use of `@Modifying` in Spring Data JPA?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Adding `@Modifying` annotation indicates the query is not for a `SELECT` query.
- `@Modifying` annotation lets you execute `DML` inserts, updates, and deletes)and `DDL` using `JPA` `@Query` annotations.
- `@Modifying` annotation is only relevant in combination with the `@Query` annotation, derived query methods or custom methods do not require this Annotation.
</blockquote> 

</details>

---

13. Why do we need `Spring JDBC` when we already have Java JDBC?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- `JDBC` is the core API to connect your java application with any database vendor.
- When we use Java `JDBC` there are multiple configuration steps, starting from loading the river to closing the DB connection developer has to manage.
- When we use the `Spring JDBC` module under the Spring framework, it takes care of all low-level common `JDBC` operations and allows the developer to focus only on business logic.
</blockquote> 

</details>

---

14. What is `DataSource` in Java application?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- `DataSource` is a factory for connections to the physical data source.
- In enterprise applications, the `DataSource` object is the preferred means of getting a connection to your database.
  
</blockquote> 

</details>

---

15. What are the three types of implementations of `DataSource` in Java applications?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- The `DataSource` interface is implemented by a driver vendor. There are three types of implementations:
    - `Basic implementation` - produces a standard Connection object
    - `Connection pooling implementation` -- produces a Connection object that will automatically participate in connection pooling. 
    - `Distributed transaction implementation` -- produces a Connection object that may be used for distributed transactions and almost always participates in connection pooling. 

</blockquote> 

</details>

---
16. What is `Connection Pooling` in an enterprise application?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- `Connection pooling` is a technique of creating and managing a pool of connections that are reused rather than created each time a connection is requested. 
- `Connection pooling` can greatly increase the performance of your Java application, while reducing overall resource usage.
-  Connection pool is a memory cache of database connections which is maintained by a connection pooling provider as a layer on top of any standard JDBC driver.

</blockquote> 

</details>

---
17. What default connection pool does spring boot use?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- `Spring Boot` uses `HikariCP` as the default connection pool.
- `HikariCP` has great performance and concurrency.

</blockquote> 

</details>

---

18. What connection pool does spring boot supports?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

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
19. What is the sequence of choosing various connection pools inside the Spring application?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

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
20. What is `Programmatic & Declarative Transaction Management` in the Spring application?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Spring provides both `Programmatic` and `Declarative` transaction management.
- In Programmatic Transaction management we have transaction management code surrounding our business code. 
- It gives extreme flexibility but is difficult to maintain.
- Whereas in Declarative Transaction management we separate the transaction management code from the business code. 
- We can configure Declarative Transaction management using both annotations and XML-based configuration.
- Most Spring Framework users choose declarative transaction management as this option has the least impact on application code.
- To summarize, Programmatic Transaction management is more flexible during development time but less flexible during application life. whereas Declarative Transaction management is less flexible during development time but more flexible during the application life

 </blockquote> 

</details>

---
21. What does isolation and propagation attributes denote in @Transactional annotation e.g. `@Transactional(isolation = xxx, propagation = xxx)`?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- While using Declarative Transaction management we can provide isolation & propagation attributes which serve below purpose:
    - `Isolation`: The degree to which this transaction is isolated from the work of other transactions. For example, can this transaction see uncommitted writes from other transactions?
    - `Propagation`: Typically, all code within a transaction scope runs in that transaction. However, you can specify the behaviour if a transactional method is run when a transaction context already exists. For example, code can continue running in the existing transaction (the common case), or the existing transaction can be suspended, and a new transaction created.

</blockquote> 

</details>

---
22. What configurations do `Spring JDBC` & developer need to perform in the application?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- The table shows which actions Spring takes care of and which are developers’ responsibilities.
  
| **Steps** | **Action**                                               | **Spring** | **Developer** |
| --------- | -------------------------------------------------------- | ---------- | ------------- |
| 1         | Define connection parameters.                            |            | X             |
| 2         | Open the connection.                                     | X          |               |
| 3         | Specify the SQL statement.                               |            | X             |
| 4         | Declare parameters and provide parameter values          |            | X             |
| 5         | Prepare and run the statement.                           | X          |               |
| 6         | Set up the loop to iterate through the results (if any). | X          |               |
| 7         | Do the work for each iteration.                          |            | X             |
| 8         | Process any exception.                                   | X          |               |
| 9         | Handle transactions.                                     | X          |               |
| 10        | Close the connection, the statement, and the result set. | X          |               |

</blockquote> 

</details>

---
