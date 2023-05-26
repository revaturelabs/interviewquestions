1. What are the different multiplicity (cardinality) relationships? 

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Multiplicity is also known as cardinality defines the number of instances that can be associated between two entities. Here are the different types of multiplicity relationships:

- **One-to-One (1:1):** Each instance of one entity is associated with exactly one instance of another entity, and vice versa.

- **One-to-Many (1:N):** Each instance of one entity is associated with multiple instances of another entity, but each instance of the other entity is associated with only one instance of the first entity.

- **Many-to-One (N:1):** Multiple instances of one entity are associated with a single instance of another entity.

- **Many-to-Many (N:N):** Multiple instances of one entity can be associated with multiple instances of another entity through a junction table.

</blockquote>

</details>

---

2. How do you create a new Table from another Table, where just the structure of the table is copied but none of the rows?  

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
<blockquote>

We can use the following  to create a new table with the same structure as an existing table but no data. It works for both *SQL and PostgreSQL*

```sql

CREATE TABLE new_table_name AS
SELECT *
FROM existing_table_name
WHERE 1 = 2;
```

- In this statement, new_table_name is the name you want to give to the new table, and existing_table_name is the name of the existing table whose structure you want to copy.

- The SELECT statement retrieves the column structure of the existing table, but the WHERE clause always evaluates to false, so no data is actually selected. This means that the new table will have the same columns as the existing table, but it will be empty.

</blockquote>

</details>

---

3. Why would you use SQL over noSQL?  

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
<blockquote>

The choice between SQL and NoSQL databases depends on the specific needs of the application. While SQL databases provide strong guarantees of data consistency and are ideal for applications that require complex queries and data analysis, NoSQL databases are highly flexible, scalable, and performant, making them ideal for applications that require high throughput and large data volumes.

</blockquote>

</details>

---

4.  What is relational mapping?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
<blockquote>

Relational mapping, also known as object-relational mapping (ORM), is the process of mapping data from a relational database into an object-oriented programming language. By using an ORM framework, developers can define mappings between database tables and application objects, and the framework will automatically generate the necessary SQL queries to retrieve and persist data. This allows developers to work with data in an object-oriented manner, using familiar concepts such as classes, objects, and inheritance, while still leveraging the power and flexibility of relational databases.

</blockquote>

</details>

---

5. What type of storage would you use to store data which is requested often?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
<blockquote>

For data that is requested often, a high-performance storage solution should be used. This includes solid-state drives (SSDs) and in-memory databases.

- SSDs are a type of storage device that use flash memory to store data. They are faster than traditional hard disk drives (HDDs) because they have no moving parts, and they are better suited for handling random read and write operations. SSDs are often used as the primary storage device in servers and high-performance computing environments.

- In-memory databases, as the name suggests, store data in memory rather than on disk. This makes them much faster than traditional disk-based databases, which must read data from disk each time it is requested. In-memory databases are often used for applications that require fast data access, such as real-time analytics, high-speed transaction processing, and other time-sensitive applications.

</blockquote>

</details>

---

6. What is the difference between Oracle database and PostgresQL?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
<blockquote>

Oracle and PostgreSQL are both popular relational database management systems, but there are several key differences between them:

- *Licensing*: Oracle is a commercial database that requires licensing fees, while PostgreSQL is an open-source database that is free to use.

- *Features*: Oracle has a wider range of features and capabilities, such as advanced security, high availability, and scalability options. PostgreSQL also has a rich set of features, but it may not be as comprehensive as Oracle in some areas.

- *Performance*: Oracle is known for its high performance and scalability, especially in large enterprise environments. PostgreSQL is also performant, but may not be as fast as Oracle in some scenarios.

- *Ease of use*: Oracle can be complex and challenging to set up and configure, requiring specialized skills and knowledge. PostgreSQL, on the other hand, is generally considered to be more user-friendly and easier to work with.

</blockquote>

</details>

---

7. How do you decide whether to store data as JSON or in RDBMS ?
 
![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
<blockquote>

Deciding whether to store data as JSON or in a relational database management system (RDBMS) depends on several factors, such as the type of data, its complexity, and how it will be used. Here are some general guidelines:

- JSON is suitable for storing data with a flexible or dynamic structure, such as social media feeds or web analytics data, where the schema may evolve over time.

- RDBMS is more suitable for storing structured data with a fixed schema, such as financial transactions or customer data, where the data is organized into tables with well-defined columns and relationships.

- If the data requires complex queries or joins with other tables, an RDBMS may be a better choice.

- If the data will be accessed primarily through API calls or web services, using JSON may be more efficient as it can be easily serialized and deserialized.

Ultimately, the choice between JSON and RDBMS depends on the specific requirements of the application and the type of data being stored. It is also possible to use a hybrid approach, where data is stored both in JSON and RDBMS, depending on the type of data and how it will be used.

</blockquote>

</details>

---

8. How do you add a column to an existing table?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

To add a new column to an existing table in SQL, you can use the ALTER TABLE statement with the ADD keyword. Here's the basic syntax:
```sql
ALTER TABLE table_name
ADD column_name data_type;
```
where table_name is the name of the table to which you want to add the column, column_name is the name of the new column, and data_type is the data type of the column.

For example, if you want to add a new column "email" of data type VARCHAR(50) to a table named "customers", you can use the following SQL statement:
```sql
ALTER TABLE customers
ADD email VARCHAR(50);
```


</blockquote>

</details>

---

9. How to change the data type for an attribute in a table ?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary> Show Answer </summary>

<blockquote>

To change the data type of an attribute in a table, you can use the ALTER TABLE statement with the MODIFY keyword. Here's the basic syntax:
```sql
ALTER TABLE table_name
MODIFY column_name new_data_type;
```
where table_name is the name of the table, column_name is the name of the column whose data type you want to change, and new_data_type is the new data type for the column.

For example, if you want to change the data type of the "age" column in the "employees" table from INT to FLOAT, you can use the following SQL statement:
```sql
ALTER TABLE employees
MODIFY age FLOAT;
```
This will change the data type of the "age" column to FLOAT in the "employees" table.

Note that when you change the data type of a column, you may also need to update the values in that column to match the new data type. For example, if you change a column from INT to VARCHAR, you will need to make sure that all values in that column are converted to strings. Also, if the column you're modifying is used in any indexes or constraints, you may need to modify those as well.


</blockquote>

</details>

---

10. Can you have more than one primary key? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

No, a table can have only one primary key. The primary key constraint ensures that each row in the table is unique, so having more than one primary key would violate this constraint. However, a primary key can be made up of multiple columns, so a combination of columns can serve as the primary key. In this case, the combination of columns must be unique for each row in the table.

</blockquote>

</details>

---

11. how would you establish the relationship between employee and department tables?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

To establish a relationship between an "employee" table and a "department" table in SQL, you can use a foreign key constraint.

Here's an example of how to create the two tables and establish the relationship:

```sql
CREATE TABLE department (
  department_id INT PRIMARY KEY,
  department_name VARCHAR(50)
);

CREATE TABLE employee (
  employee_id INT PRIMARY KEY,
  employee_name VARCHAR(50),
  department_id INT,
  FOREIGN KEY (department_id) REFERENCES department(department_id)
);
```
In this example, the "department" table is the parent table, and the "employee" table is the child table. The "department" table contains the primary key "department_id", and the "employee" table contains a foreign key "department_id" that references the primary key in the "department" table.

This relationship means that each employee belongs to a single department, and each department can have multiple employees. The foreign key constraint ensures that an employee can only be associated with an existing department.

</blockquote>

</details>

---

12. What is a composition in SQL?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>

<blockquote>
In SQL, composition refers to the ability to combine multiple SQL queries to form a more complex query. This is typically achieved using the keywords "UNION", "INTERSECT", and "EXCEPT".

- UNION: This keyword is used to combine the results of two or more SELECT statements into a single result set. The SELECT statements must return the same number of columns and compatible data types.

- INTERSECT: This keyword is used to combine the results of two or more SELECT statements and return only the rows that are common to all the SELECT statements. Again, the SELECT statements must return the same number of columns and compatible data types.

- EXCEPT: This keyword is used to combine the results of two SELECT statements and return only the rows that are unique to the first SELECT statement and not present in the second SELECT statement. Once again, the SELECT statements must return the same number of columns and compatible data types.

By using these keywords in combination with parentheses, SQL allows you to create complex queries that can perform more sophisticated data analysis.

</blockquote>

</details>

---
13. What is a schema in a database?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

A schema in a database is a logical structure that represents the organization of data in a database. It defines the tables, columns, and relationships between the data, as well as the data types and other constraints for each column.

</blockquote>

</details>

---
14. In SQL, name the statements through which we can create a primary key in a table?

 ![Beginner](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 

> By using `create table` and `alter table` statements we can create a primary key in a table in SQL. 

</details>

---

15. In SQL, List the commands that are the part of Data Definition Language?

![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 

> Data Definition language or DDL commands are used to describe or define the structure of the database objects. In DDL, the following are the commands:  
> - create
> - alter
> - drop
> - truncate
> - comment
> - rename 

</details>

---
16. How normalization affects the performance in SQL?

![Advance](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

 
<details><summary> <b>Show Answer</b> </summary> 

> The main point to use the normalization forms in table data is to eliminate the repetition of data from it. So one thing we can do is say that it will guarantees the duplicate free data in the table. But achieving full normalization, it negatively affects the performance. 

</details>

---

17. Differentiated 1nf, 2nf and 3nf forms of normalization

![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 

> - In 1nf or 1st normal form, the composite attribute is converted into a single-value attribute. Each column must only have one single data entry in each row. 
> - In 2nf or 2nd normal form, the table should not have any partial dependency means the proper subset of the primary key shouldn't determine any non-prime attribute. 
> - In 3nf or 3rd normal form, there should not be any transitive dependency, which means non-prime attribute of the table should not be dependent on another non- prime attribute. 

</details>

---

18. can you List some of the benefits of normalization in SQL?

![Beginner](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


 
<details><summary> <b>Show Answer</b> </summary> 

> - It is used to reduce or remove duplicates from the data.
> - To optimize storage space.
> - To prevent unwanted deletion of data.
> - To prevent data inconsistency.

</details>

---
19. Create an "employee" table and make one primary key and one foreign key in it. 

![Beginner](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

 
<details><summary> <b>Show Answer</b> </summary> 

> 
```sql
create table employee(
       emp_id int,
       emp_name varchar(20),
       dept_id int,
       primary key (emp_id),
       foreign key (dept_id) references department(dept_id)
       );
```

</details>

---

20. Can a primary key and foreign key contain null? 
![Beginner](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


 
<details><summary> <b>Show Answer</b> </summary> 

> A primary key field in the table cannot contain null as a value. But that is not the case with a foreign key. A foreign key is used to stabilize a relation between two tables and it can contain a  null value.

</details>

---

21. Explain anomalies and its types?

![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
 
<details><summary> <b>Show Answer</b> </summary> 

> Anomaly generally happens when the database is not constructed well and when the normalization concepts were not applied. There are 3 types of anomalies that cause a problem:  
> 1. insertion anomaly: This can happen when we are trying to insert the data into the table, and it is not allowed because some data is not present.
> 2. update anomaly: This will happen when we have duplicate data in the table and updating one of those data will not reflects toe other data and the end user has no idea which data is the correct one.
> 3. deletion anomaly: This will happen when the deletion of one data will cause other data to be deleted from the table as well.


</details>

---
22. Can you talk about BLOB in SQL?

![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 

> BLOB is a sub-type of string datatype in SQL and stands for a binary large object. It is used for a large amount of data like documents, images, etc. They are three types:  
> - TINYBLOB
> - MEDIUMBLOB
> - LONGBLOB

</details>

---
