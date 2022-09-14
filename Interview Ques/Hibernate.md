1. Explain about ORM in Hibernate.

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Hibernate ORM stands for Object Relational Mapping. Which is a mapping tool pattern used for converting data stored in a relational database to an object used in object-oriented programming constructs. It helps in simplifying data retrieval, creation, and manipulation.

</blockquote>

</details>

---

2. What do you mean by session in Hibernate?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

It is an object that maintains the connection between Java object application and database. Which has methods for storing, retrieving, modifying or deleting data from database using methods like persist(), load(), get(), update(), delete(), etc. 

</blockquote>

</details>

---

3. What is a SessionFactory?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>


Which provides an instance of Session. It is a factory class that gives the Session objects based on the configuration parameters in order to establish the connection to the database.

</blockquote>

</details>

---

4. What are the main elements of the Hibernate framework?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

It consists of 

- SessionFactory
- Session 
- Transaction
- TransactionFactory
- ConnectionProvider

</blockquote>

</details>

---

5. How will SQL query created in Hibernate?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

The SQL query is created by executing the following syntax:

`Session.createSQLQuery`

</blockquote>

</details>

---

6. Is SessionFactory a thread-safe object?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Yes, it is a thread-safe object, many threads cannot access it simultaneously.

</blockquote>

</details>

---

7. Is Session a thread-safe object?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

No, It is not a thread-safe object, many threads can access it simultaneously. In other words, you can share it between threads.

</blockquote>

</details>

---

8. Explain the states of the object in hibernate?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

There are 3 states of the object (instance) in hibernate.

- Transient: The object is in a transient state if it is just created but has no primary key (identifier) and not associated with a session.
- Persistent: The object is in a persistent state if a session is open, and you just saved the instance in the database or retrieved the instance from the database.
- Detached: The object is in a detached state if a session is closed. After detached state, the object comes to persistent state if you call `lock()` or `update()` method.

</blockquote>

</details>

---

9. List some of the important interfaces of Hibernate framework?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

There are some interfaces like

- SessionFactory (`org.hibernate.SessionFactory`)
- Session (`org.hibernate.Session`)
- Transaction (`org.hibernate.Transaction`)

</blockquote>

</details>

---

10. What is the use of Hibernate Configuration File?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Which mainly contains database-specific configurations and are used to initialize SessionFactory. Some important parts of the Hibernate Configuration File are Dialect information, so that hibernate knows the database type and mapping file or class details.

</blockquote>

</details>

---

11. What will be stored in hibernate.cfg.xml file?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

- It is one of the most required configuration files in Hibernate. By default, this file is placed under the src/main/resource folder.
- The file contains database related configurations and session-related configurations.

</blockquote>

</details>

---

12. What does lazy loading do in hibernate?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

- Which improves the performance. It loads the child objects on demand.

- Since Hibernate 3, lazy loading is enabled by default, and you don't need to do lazy="true". It means not to load the child objects when the parent is loaded.

</blockquote>

</details>

---

13. Explain about caching levels in Hibernate.

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

It offers two caching levels:

`The first level cache` is the session cache. Objects are cached within the current session and they are only alive until the session is closed.
`The second level cache` exists as long as the session factory is alive. 

</blockquote>

</details>

---

14. What are Hibernate's callback interfaces?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Which is used in a Hibernate application to receive a notification when an object event occurs, such as loading, saving, or deletion.

</blockquote>

</details>

---

15. How to achieve mapping in Hibernate?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote> 

Association mappings are one of the key features of Hibernate. It supports the same associations as the relational database model. They are:

- One-to-One associations
- Many-to-One associations
- Many-to-Many associations

</blockquote>

</details>

---

16. Can we use SQL inside the Hibernate?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote> 

Yes,  Hibernate gives a facility to execute SQL commands directly on the database with a technique called native SQL.

To execute SQL commands from hibernate, Hibernate given us SQLQuery. SQLQuery is an interface which is coming from the org.hibernate package.

</blockquote>

</details>

---

17. Any idea about O-R (Object relational) impedance mismatch? Explain about.


![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

When we load or store graph of objects using a relational database we come across five mismatch problem and this mismatch between the object model and relational model is called object relational impedance mismatch or paradigm mismatch.

</blockquote>

</details>

---

18. What do you mean by Named SQL Query?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote> 

Hibernate provides an important feature called Named Query, using which you can define at a central location and use them anywhere in the code.

We can create named queries for both HQL as well as for Native SQL. These Named Queries can be defined in Hibernate mapping files with the help of JPA annotations `@NamedQuery` and `@NamedNativeQuery`.

</blockquote>

</details>

---

19. Explain about JPA.

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote> 

Java Persistence API (JPA) defines the management of relational data in the Java applications. Which is defined in `javax.persistence` package.

</blockquote>

</details>

---

20. What is the use of EntityManagerFactory interface?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote> 

Which is used to interact with the entity manager factory for the persistence unit. Thus, it provides an entity manager.

</blockquote>

</details>

---

21. Explain about EntityManager interface.

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote> 

It is used to create, read, and delete operations for instances of mapped entity classes. This interface interacts with the persistence context.


</blockquote>

</details>

---

22. What are the possible methods that can be used for detached state?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote> 

`session.close();` 
`session.clear();` 
`session.detach(e);`
`session.evict(e)`

</blockquote>

</details>

---

23.  What are the possible methods that can be used for persistent state?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote> 

`session.save(e);`  
`session.persist(e);`  
`session.update(e);`  
`session.saveOrUpdate(e);`  
`session.lock(e);`  
`session.merge(e);`

</blockquote>

</details>

---

24. How to solve impedance mismatch problem?

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote> 

We can use an ORM tool that converts the data between relational databases and object oriented programming languages.

</blockquote>

</details>

---

25. Differentiate between the first and second level cache in Hibernate? 

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote> 

The first-level cache is maintained at Session level while the second level cache is maintained at a SessionFactory level and is shared by all sessions.

</blockquote>

</details>

---
