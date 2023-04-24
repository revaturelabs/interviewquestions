1. What does Hibernate do ? 


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Hibernate is an Object-Relational Mapping (ORM) tool that automates the mapping of Java objects to database tables. It is database independent and uses a query language similar to SQL called HQL. The HQL queries written by the user are converted into database-specific queries by hibernate. Because of this functionality, the user can write a generalized query to perform the database-related operation without worrying about the database being used in the application. It reduces development time and improves application performance by simplifying database access in Java applications.

</blockquote>

</details>

---

2. What annotation use in Hibernate

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

In hibernate we can use annotations like `@Entity`, `@Table`, `@Id`, `@Column`, `@GeneratedValue`, `@NamedQuery` etc.

</blockquote>

</details>

---

3. What to put in `application.properties` for hibernate

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The `application.properties` file is used to configure Hibernate properties. In this file we can mention the values for properties like `spring.jpa.database`, `spring.jpa.hibernate.ddl-auto`, `spring.datasource.url`,  `spring.datasource.username`, `spring.datasource.password` etc.


</blockquote>

</details>

---

4. How to write SQL statements, in Hibernate.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

To write SQL statements in Hibernate, you can use either native SQL. To use native SQL queries we have to create a Session object using a SessionFactory instance, and then we use the `createSQLQuery()` method to create a SQL query object. The `createSQLQuery()` method contains the SQL query which we want to execute on the database. To add dynamic values into the query `setParameter()` method is used.

</blockquote>

</details>

---
