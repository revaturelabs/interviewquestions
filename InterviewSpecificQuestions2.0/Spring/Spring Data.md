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

4.Which database dialects are directly supported by `Spring Data JDBC`?

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
6. How can we update a record in the database when the CrudRepository interface does not have an update method?

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
7. Do we need to invoke the `save` method within a transactional method when updating an object using CrudRepository?

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
10. How do you implement the `SQL` `LIKE` query in Spring Data using method names? Give an example.

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

17. What is the sequence of choosing various connection pools inside the Spring application?

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
18. What is `Programmatic & Declarative Transaction Management` in the Spring application?

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
19. What does isolation and propagation attributes denote in @Transactional annotation 
Example: `@Transactional(isolation = xxx, propagation = xxx)`?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- While using Declarative Transaction management we can provide isolation & propagation attributes which serve below purpose:
    - `Isolation`: The degree to which this transaction is isolated from the work of other transactions. For example, can this transaction see uncommitted writes from other transactions?
    - `Propagation`: Typically, all code within a transaction scope runs in that transaction. However, you can specify the behaviour if a transactional method is run when a transaction context already exists. For example, code can continue running in the existing transaction (the common case), or the existing transaction can be suspended, and a new transaction created.

</blockquote> 

</details>

---
20. What is the PlatformTransactionManager?


![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

The PlatformTransactionManager is an interface in Spring that provides a consistent abstraction for managing transactions across different transactional resources, such as relational databases, message queues, or any other resource that supports transactions. It defines methods for beginning, committing, and rolling back transactions.

</blockquote> 

</details>

---

21. What is a PersistenceContext?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- A PersistenceContext, in the context of Java Persistence API (JPA), is a first-level cache of managed entities. It represents the set of persistent entities that are currently being managed by the JPA provider within a particular unit of work.

- A PersistenceContext is a temporary storage space that holds the objects retrieved from the database or created within the application. 

</blockquote> 

</details>

---

22. What is Spring ORM?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- Spring ORM is a module within the Spring Framework that provides integration with Object-Relational Mapping (ORM) frameworks, primarily Hibernate, JPA (Java Persistence API), and other ORM technologies. It simplifies the development of database access code by providing a consistent and declarative way to interact with the database.

- Spring ORM offers features such as transaction management, object-to-relational mapping, query execution, and caching. It allows developers to work with database entities as regular Java objects and abstracts away the complexities of SQL queries and database interactions.


</blockquote>

</details>

---

23.  what is the JDBC template?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- The JDBC template is a class provided by the Spring Framework that implements the Template design pattern for database access using the JDBC (Java Database Connectivity) API. It simplifies the process of working with relational databases by encapsulating common database operations such as querying, updating, and deleting records. The JDBC template handles low-level details such as database connections, statement creation, and result set handling, allowing developers to focus on writing business logic instead of dealing with boilerplate code.

</blockquote>

</details>

---

24.  What is transaction propagation?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

Transaction propagation refers to how a transaction is propagated from one method to another within a transactional context. It defines the behavior of nested method invocations when it comes to transaction management.

In the context of Spring and its transaction management, transaction propagation determines whether a method should join an existing transaction or create a new one. It controls how transactions are inherited or shared between multiple methods.

There are different transaction propagation options available, such as:

- REQUIRED: The method must run within a transaction. If a transaction already exists, the method joins it; otherwise, a new transaction is created.
- REQUIRES_NEW: The method always creates a new transaction. If an existing transaction exists, it is suspended until the new transaction completes.
- SUPPORTS: The method can run with or without a transaction. If an existing transaction exists, the method joins it; otherwise, it executes non-transactionally.
- NOT_SUPPORTED: The method always runs without a transaction, even if an existing transaction exists.


</blockquote>

</details>

---

25. What are the different modules available in Spring Data?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

The different modules available in Spring Data are:

1. Spring Data JPA: Provides support for working with JPA (Java Persistence API) to access relational databases.

2. Spring Data MongoDB: Offers support for working with MongoDB NoSQL database.

3. Spring Data Redis: Provides support for working with Redis, an in-memory data store.

4. Spring Data JDBC: Offers support for working with JDBC (Java Database Connectivity) to access relational databases using a lightweight and simplified approach.

5. Spring Data Elasticsearch: Provides support for working with Elasticsearch, a distributed search and analytics engine.

6. Spring Data Neo4j: Offers support for working with Neo4j, a graph database.

7. Spring Data Cassandra: Provides support for working with Apache Cassandra, a highly scalable and distributed NoSQL database.

8. Spring Data Couchbase: Offers support for working with Couchbase, a NoSQL document database.

9. Spring Data Solr: Provides support for working with Apache Solr, a search platform built on Apache Lucene.



</blockquote>

</details>

---

26. How does Spring Data simplify database access and reduce boilerplate code?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

Spring Data simplifies database access and reduces boilerplate code by providing a set of abstractions and ready-to-use implementations for common database operations. 

1. It offers a unified and consistent programming model across different databases, allowing developers to work with different database technologies using a common API.

2. Spring Data provides automatic repository implementations based on conventions and naming conventions, eliminating the need to write repetitive data access code.

3. It supports query methods, where developers can define queries by simply declaring method names with specific prefixes or using annotations, reducing the need to write complex SQL or query DSLs.

4. Spring Data supports pagination, sorting, and other common data access patterns out-of-the-box, making it easier to handle large datasets and perform efficient data retrieval.

5. It integrates with the Spring Framework's transaction management, allowing developers to easily manage database transactions without writing explicit transaction code.


</blockquote>

</details>

---

27. List some of the Spring Data Annotations with its purpose?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

Some of the commonly used Spring Data annotations are:

1. `@Entity`: Marks a class as an entity in JPA (Java Persistence API) and maps it to a database table.

2. `@Table`: Specifies the name of the database table associated with an entity class.

3. `@Id`: Marks a field as the primary key of an entity.

4. `@GeneratedValue`: Specifies the strategy for generating values for an entity's primary key.

5. `@Column`: Specifies the mapping between an entity's field and a database column.

6. `@Transient`: Marks a field as not persistent, meaning it will not be stored in the database.

7. `@Repository`: Marks a class as a repository, which is responsible for data access and manipulation.

8. `@Query`: Defines a custom query method in a repository interface using JPQL (Java Persistence Query Language) or native SQL.

9. `@Transactional`: Specifies that a method or class should be executed within a transaction.

10. `@EnableJpaRepositories`: Enables Spring Data JPA repositories in a Spring Boot application.


</blockquote>

</details>

---

28.  How do you handle database migrations in Spring Data and Spring JDBC?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

In Spring Data, database migrations can be handled using external tools such as Flyway or Liquibase. These tools allow you to define and manage database schema changes using versioned migration scripts. Spring Data integrates with these tools by providing support for executing the migration scripts during application startup.

In Spring JDBC, you can handle database migrations by executing SQL scripts manually. You can create SQL scripts that contain the necessary database schema changes and execute them using the `JdbcTemplate` provided by Spring JDBC. This approach requires you to manage the versioning and execution of the scripts manually.


</blockquote>

</details>

---

29.  How do you handle database transactions in Spring JDBC?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

In Spring JDBC, you can handle database transactions using the `TransactionTemplate` or by annotating your methods with the `@Transactional` annotation.

1. Using `TransactionTemplate`: You can create an instance of `TransactionTemplate` and use its `execute` method to execute database operations within a transaction. You can define the transaction boundaries and handle transactional behavior programmatically.

2. Using `@Transactional` annotation: You can annotate your methods or classes with `@Transactional` to enable declarative transaction management. Spring will automatically manage the transactions for annotated methods, ensuring that they are executed within a transactional context. You can configure transaction propagation, isolation level, and other transaction attributes using the `@Transactional` annotation.


</blockquote>

</details>

---