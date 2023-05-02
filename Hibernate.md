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

5. What is ORM?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

ORM stands for Object-Relational Mapping, it isused to map data between an object-oriented programming language and a relational database. It helps developers work with database records as if they were objects in their programming language, making it easier to manage database interactions. Java also have a ORM framework tool called Hibernate.
</blockquote>

</details>

---


6. How do you define a many to one relationship in hibernate

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

In many-to-one relationship type many records from one table("many" side) belong to only one record of another table("one" side). To define this type of relationship in Hibernate, you can use the `@ManyToOne` annotation on the field of the "many" side of the association. 

</blockquote>

</details>

---

7. In Hibernate, what is the difference between save, update and persist?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The `save()` method is used to save a new entity to the database. If the object has already been saved before, then it will throw an exception. The `update()` method is used to update an existing entity object in the database. It throws an exception if the object is not found in the database. The `persist()` method is similar to the `save()` method, but the difference between them is that `save()` method returns the saved object with generated primary key, whereas the `persist()` method does not return anything.

</blockquote>

</details>

---

8. What does the @entity annotation do in hibernate?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The @Entity annotation is used to inform Hibernate that the marked class  represents a table in the database. It also tells Hibernate to create or update the corresponding table of the class in the database schema when the application is deployed.

</blockquote>

</details>

---

9. Name some other annotation and explain what the do.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The hibernate annotations and their functionality is mentioned below:

- `@Entity`: It marks a Java class as a entity and maps it to a database table.
- `@Table`: It specifies the name of the table that corresponds to an entity.
- `@Id`: It specifies the primary key column of an entity.
- `@GeneratedValue`: It specifies the strategy for generating primary key values.
- `@Column`: It is used to customize the column's name, type, and constraints.
- `@ManyToOne` and `@OneToMany`: Defines a many-to-one or one-to-many relationship between entities.

</blockquote>

</details>

---
