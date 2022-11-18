## Technical

1.What is the difference between `Spring JDBC` and `Spring Data JDBC`?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1"> <summary> <b> Show Answer </b> </summary>

<blockquote markdown="1"> 
    
- `Spring JDBC`, a sub-module under the Spring framework project, provides Spring abstractions over the plain JDBC `DataSource` that we can use with the Spring Framework.
- `Spring JDBC` nicely hooks support for `Transaction Management`, `Exception Handling`, `DB connection management`, `Connection pool configuration`, avoiding boilerplate code using `JdbcTemplate` etc.
- `Spring Data JDBC`, a sub-module under the Spring Data project, makes it easy to implement JDBC-based repositories.
- `Spring Data JDBC` is an Object Relational Mapper (ORM) based on the `Repository` abstraction.
- `Spring Data JDBC` nicely hooks support for `CrudRepository`, `@Query`, `PagingAndSortingRepository`, `@Value` in persistence constructors etc.

</blockquote  markdown="1"> 

</details markdown="1">

---

2.What do you mean by database dialect? 

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1"> <summary> <b> Show Answer </b> </summary>

<blockquote markdown="1"> 
    
- A database dialect is a configuration setting for platform-independent software (`JPA`, `Hibernate`, etc.) which allows such software to translate its generic SQL statements into vendor-specific DDL, DML.
</blockquote  markdown="1"> 

</details markdown="1">

---

3.Why does Spring Data JDBC need database dialect?

![Medium](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Medium%20(2).svg)

<details markdown="1"> <summary> <b> Show Answer </b> </summary>

<blockquote markdown="1"> 
    
- One of the core features of `Spring Data JDBC` is to generate automatic queries using `CrudRepository` for vendor-specific databases.
- To generate the queries `Spring Data JDBC` internally uses database dialects.
</blockquote  markdown="1"> 

</details markdown="1">

---

4.`Spring Data JDBC` includes direct support for which database dialects?

![Medium](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Medium%20(2).svg)

<details markdown="1"> <summary> <b> Show Answer </b> </summary>

<blockquote markdown="1"> 
    
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
</blockquote  markdown="1"> 

</details markdown="1">

---

5.Why do we use `PagingAndSortingRepository` in Spring?

![Complex](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Complex%20(2).svg)

<details markdown="1"> <summary> <b> Show Answer </b> </summary>

<blockquote markdown="1"> 
    
- `Spring Data JDBC` sub-module under the Spring Data project provides `PagingAndSortingRepository` which is an extension of `CrudRepository` to provide additional methods to retrieve entities using the pagination and sorting abstraction.

</blockquote  markdown="1"> 

</details markdown="1">

---
6.The `CrudRepository` interface does not have an `update` method then how do we update the record in the database? 

![Complex](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Complex%20(2).svg)

<details markdown="1"> <summary> <b> Show Answer </b> </summary>

<blockquote markdown="1"> 
    
- `CrudRepository` has only `save` but it acts as an `update` as well.
- When we `save` an entity with an empty `id` it will do a save.
- When you do `save` on the entity wan its existing `id` it will do an `update`.
- This means after we used findById and changed something in returned object, we can call save on that object and it will do an update because after findById you get an object with a populated id that exists in our database.
- `save` in `CrudRepository` can accept a single entity or Iterable of our entity type.
</blockquote  markdown="1"> 

</details markdown="1">

---
7.Is it mandatory to call the `save` method to update an object inside a transactional method for `CrudRepository`?

![Complex](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Complex%20(2).svg)

<details markdown="1"> <summary> <b> Show Answer </b> </summary>

<blockquote markdown="1"> 
    
- Calling the `save` method to update an object inside a transactional method is not mandatory.
- When we use the `findById` method to retrieve an entity within a transactional method, the returned entity is managed by the persistence provider.
- Hence, any change to that entity will be automatically persisted in the database, regardless of whether we are invoking the save method inside a transactional method.
</blockquote  markdown="1"> 

</details markdown="1">

---
8.What is the use of `@Query` annotation in Spring Data?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1"> <summary> <b> Show Answer </b> </summary>

<blockquote markdown="1"> 
    
- `Spring Data` provides multiple ways to define a query that we can execute.
- One of these popular methods is using `@Query` annotation.
- We can annotate the `Spring Data` repository method with the `@Query` annotation where its `value` attribute contains the `JPQL` or `SQL` to be executed.
- It's a convenient approach to place a query definition just above the method inside the repository rather than inside our domain model as named queries.
</blockquote  markdown="1"> 

</details markdown="1">

---
9.Explain the query builder mechanism in the Spring Data repository?

![Medium](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Medium%20(2).svg)

<details markdown="1"> <summary> <b> Show Answer </b> </summary>

<blockquote markdown="1"> 
    
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

</blockquote  markdown="1"> 

</details markdown="1">

---
10.How you will implement the `SQL` `LIKE` query in Spring Data using method names? Give an example.

![Medium](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Medium%20(2).svg)

<details markdown="1"> <summary> <b> Show Answer </b> </summary>

<blockquote markdown="1"> 
    
- Let’s consider the Login entity comprising the userId attribute.
- There can be four different variations of LIKE query formed using method names as follows:
  - Exact Match `SELECT ...LIKE userId`
    - `List<User> findByUserIdLike(String userId);`
  - Starting With `SELECT ...LIKE userId%`
    - `List<User> findByUserIdStartingWith(String userId);`
  - Ending With `SELECT ...LIKE %userId`
    - `List<User> findByUserIdEndingWith(String userId);`
  - In Between `SELECT ...LIKE %userId%`
    - `List<User> findByUserIdContaining(String userId);`
</blockquote  markdown="1"> 

</details markdown="1">

---
11.What is `Spring Data JPA`?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)

<details markdown="1"> <summary> <b> Show Answer </b> </summary>

<blockquote markdown="1"> 
    
- `Spring Data JPA`, a sub-module under the Spring Data project, makes it easy to implement `JPA` based repositories.
- `Spring Data JPA` provides repository support for the `Java Persistence API (JPA)`.
- It eases the development of applications that need to access JPA data sources.
- `Spring Data JPA` nicely hooks support for `JpaRepository`, `Hibernate`, `OpenJPA`, `EclipseLink`, `Querydsl`, `@Modifying`
</blockquote  markdown="1"> 

</details markdown="1">

---
12.What is the use of `@Modifying` in Spring Data JPA?

![Medium](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Medium%20(2).svg)

<details markdown="1"> <summary> <b> Show Answer </b> </summary>

<blockquote markdown="1"> 
    
- Adding `@Modifying` annotation indicates the query is not for a `SELECT` query.
- `@Modifying` annotation lets you execute `DML` inserts, updates, and deletes)and `DDL` using `JPA` `@Query` annotations.
- `@Modifying` annotation is only relevant in combination with the `@Query` annotation, derived query methods or custom methods do not require this Annotation.
</blockquote  markdown="1"> 

</details markdown="1">

---

