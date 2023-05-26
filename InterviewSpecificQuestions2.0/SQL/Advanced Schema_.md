24. What are the different multiplicity (cardinality) relationships? 

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

75. How do you create a new Table from another Table, where just the structure of the table is copied but none of the rows?  

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

15. What type of storage would you use to store data which is requested often?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
<blockquote>

For data that is requested often, a high-performance storage solution should be used. This includes solid-state drives (SSDs) and in-memory databases.

- SSDs are a type of storage device that use flash memory to store data. They are faster than traditional hard disk drives (HDDs) because they have no moving parts, and they are better suited for handling random read and write operations. SSDs are often used as the primary storage device in servers and high-performance computing environments.

- In-memory databases, as the name suggests, store data in memory rather than on disk. This makes them much faster than traditional disk-based databases, which must read data from disk each time it is requested. In-memory databases are often used for applications that require fast data access, such as real-time analytics, high-speed transaction processing, and other time-sensitive applications.

</blockquote>

</details>

---

16. What is the difference between Oracle database and PostgresQL?

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

18. How do you decide whether to store data as JSON or in RDBMS ?
 
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

