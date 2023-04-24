## Technical

1. What is the difference between `Spring JDBC` and `Spring Data JDBC`?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

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

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- A database dialect is a configuration setting for platform-independent software (`JPA`, `Hibernate`, etc.) which allows such software to translate its generic SQL statements into vendor-specific DDL, DML.
</blockquote> 

</details>

---

3. Why does Spring Data JDBC need database dialect?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- One of the core features of `Spring Data JDBC` is to generate automatic queries using `CrudRepository` for vendor-specific databases.
- To generate the queries `Spring Data JDBC` internally uses database dialects.
</blockquote> 

</details>

---

4. `Spring Data JDBC` includes direct support for which database dialects?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/Medium%20(2).svg)

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

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- `Spring Data JDBC` sub-module under the Spring Data project provides `PagingAndSortingRepository` which is an extension of `CrudRepository` to provide additional methods to retrieve entities using the pagination and sorting abstraction.

</blockquote> 

</details>

---
6. The `CrudRepository` interface does not have an `update` method then how do we update the record in the database? 

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/Complex%20(2).svg)

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

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Calling the `save` method to update an object inside a transactional method is not mandatory.
- When we use the `findById` method to retrieve an entity within a transactional method, the returned entity is managed by the persistence provider. 
- Hence, any change to that entity will be automatically persisted in the database, regardless of whether we are invoking the save method inside a transactional method.
</blockquote> 

</details>

---
8. What is the use of `@Query` annotation in Spring Data?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

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

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/Medium%20(2).svg)

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

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/Medium%20(2).svg)

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

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/simple%20(2).svg)

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

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- Adding `@Modifying` annotation indicates the query is not for a `SELECT` query.
- `@Modifying` annotation lets you execute `DML` (inserts, updates, and deletes)and `DDL` using `JPA` `@Query` annotations.
- `@Modifying` annotation is only relevant in combination with the `@Query` annotation, derived query methods or custom methods do not require this Annotation.
</blockquote> 

</details>

---

13. What are finder methods in Spring Data JPA?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

Finder methods are the methods written in specific format and it has a specific naming convention. These methods are then converted into low level SQL queries.

If we want to fetch the details of an Employee by the name, then we can write the method name as below in the Repository interface. The initial’s will be common across all method names, i.e. findBy , and then we will have the field name of the entity (mapped to the database column) , here in the below case it is empName

```Java
List<Employee> findByEmpName(String name);

```

</blockquote>

</details>

---

14. What is `@JoinColumn` annotation in Spring DATA JPA?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

`@JoinColumn` is used to specify a column for joining an entity association. This annotation indicates that the enclosing entity is the owner of the relationship and the corresponding table has a foreign key column which references to the table of the non-owning side.

```Java
@Entity
class Employee {                //non-owning side of the relationship
 
    @Id
    private String employee_id;
 
    @OneToMany(mappedBy = "patient")
    private Collection<Address> addresses = new ArrayList<Address>();
 
}

@Entity
class Address {                //owning side of the relationship
 
    @ManyToOne(fetch = FetchType.LAZY)
    @JoinColumn(name="employee_id")
    private Employee employee;
 
}
```

</blockquote>

</details>

---

15. How to generate Primary Key in Spring JPA?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

Basically there are 4 options to generate primary keys in spring jpa

**GenerationType.AUTO**

  - GenerationType.AUTO is the default generation type which lets the persistence provider choose the generation type. If you talk about Hibernate, then it mostly uses GenerationType.SEQUENCE.

**GenerationType.IDENTITY**

 - GenerationType.IDENTITY relies on an auto-incremented database column and lets the database generate a new value with each insert operation. From the database perspective, this is very efficient because the auto-increment columns are highly optimized, and it doesn’t require any additional statements.

**GenerationType.SEQUENCE**

 - The GenerationType.SEQUENCE uses a database sequence to generate unique values. It requires additional select statements to get the next value from a database sequence.

**GenerationType.TABLE**

 - Most of the developers have stopped using this technique as it slows down the application.

</blockquote>

</details>

---

16. What is the difference between Hibernate and Spring Data JPA?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/InterviewSpecificQuestions/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote>

- Hibernate is a JPA implementation, while Spring Data JPA is a JPA Data Access Abstraction. Spring Data offers a solution to GenericDao custom implementations. It can withal engender JPA queries on your behalf through method name conventions. 
- Spring Data JPA is not an implementation or JPA provider, it's just an abstraction used to significantly minimize the quantity of boilerplate code required to implement data access layers for various persistence stores.

</blockquote>

</details>

---

 
