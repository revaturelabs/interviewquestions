1. What are the sublanguages of SQL.


<details><summary> Show Answer </summary>

<blockquote>

SQL (Structured Query Language) is a programming language designed for managing relational databases. There are several sub-languages of SQL, each with its own syntax and purpose. 

- Data Definition Language (DDL): DDL is used to define and modify the structure of a database. It includes commands such as CREATE, ALTER, and DROP, which are used to create, modify, and delete tables, views, indexes, and other database objects.

- Data Manipulation Language (DML): DML is used to manipulate the data stored in a database. It includes commands such as SELECT, INSERT, UPDATE, and DELETE, which are used to retrieve, add, modify, and remove data from tables.

- Data Query Language (DQL):  DQL is used to retrieve data from a database. DQL is a subset of the larger Data Manipulation Language (DML) and includes commands such as SELECT, which is used to query data from one or more tables in a database.

- Data Control Language (DCL): DCL is used to control access to a database. It includes commands such as GRANT and REVOKE, which are used to grant and revoke privileges to users and roles.

- Transaction Control Language (TCL): TCL is used to manage transactions in a database. It includes commands such as COMMIT, ROLLBACK, and SAVEPOINT, which are used to commit or rollback changes made to a database.

</blockquote>

</details>

---

2. What is an Alias?

<details><summary> Show Answer </summary>

<blockquote>

In SQL, an alias is a temporary name assigned to a table or column in a query. Aliases can be used to make column names more meaningful or to distinguish between multiple tables with similar names.

Aliases are created using the AS keyword, which is optional. Here's an example of creating an alias for a table:
```sql
SELECT * FROM employees AS emp;
```
In this example, the table "employees" is given the alias "emp". From this point forward in the query, the table can be referred to as "emp" instead of "employees". This can make the query more readable and easier to understand.

Aliases can also be used for columns. Here's an example:
```sql
SELECT first_name AS "First", last_name AS "Last" FROM employees;
```
In this example, the column "first_name" is given the alias "First", and the column "last_name" is given the alias "Last". This can be useful for making the column names more descriptive or easier to read.

Aliases are a powerful feature in SQL that can be used to make queries more readable and easier to understand.

</blockquote>

</details>

---
3. What is a record type?

<details><summary> Show Answer </summary>

<blockquote>
In SQL, a record type is a user-defined data type that represents a collection of related values. A record type is similar to a struct in other programming languages, and it allows you to define a custom data structure with its own fields and data types.

To define a record type in SQL, you use the CREATE TYPE statement. Here's an example:
```sql
CREATE TYPE person_type AS (
    first_name VARCHAR(50),
    last_name VARCHAR(50),
    email VARCHAR(100)
);
```
In this example, we define a record type called "person_type" with three fields: "first_name", "last_name", and "email". Each field has its own data type, which is specified after the field name.

Once you have defined a record type, you can use it as a data type for columns in tables or as a return type for stored procedures and functions. Here's an example of using the "person_type" record type as a column type:
```sql
CREATE TABLE employees (
    id INT,
    name person_type
);
```
In this example, we define a table called "employees" with two columns: "id" and "name". The "name" column is of type "person_type", which means it can store values with the same structure as the "person_type" record type we defined earlier.

Record types are a powerful feature in SQL that allow you to define custom data structures and make your database schema more expressive and easier to understand.

</blockquote>

</details>

---
4. replace and rank function in SQL?

<details><summary> Show Answer </summary>

<blockquote>
In SQL, the REPLACE function is used to replace all occurrences of a substring within a string with a new substring. The basic syntax for the REPLACE function is:
```sql
REPLACE(string, old_substring, new_substring)
```
Here, "string" is the original string that you want to modify, "old_substring" is the substring that you want to replace, and "new_substring" is the substring that you want to replace it with.

For example, if you have a string "Hello, world!" and you want to replace the comma with a space, you can use the following query:
```sql
SELECT REPLACE('Hello, world!', ',', ' ');
```
This will return the string "Hello world!" with the comma replaced by a space.

The RANK function in SQL is used to assign a rank to each row within a result set based on the values in one or more columns. The basic syntax for the RANK function is:
```sql
RANK() OVER (ORDER BY column1 [ASC/DESC], column2 [ASC/DESC], ...)
```
Here, "column1", "column2", etc. are the columns that you want to use for sorting the rows. You can specify multiple columns separated by commas, and you can specify the sort order (ascending or descending) for each column.

For example, if you have a table "employees" with columns "name" and "salary", and you want to assign a rank to each employee based on their salary, you can use the following query:
```sql
SELECT name, salary, RANK() OVER (ORDER BY salary DESC) AS rank
FROM employees;
```
This will return a result set with the employee name, salary, and rank, where the rank is assigned based on the salary in descending order. The employee with the highest salary will have a rank of 1, the employee with the second-highest salary will have a rank of 2, and so on.

</blockquote>

</details>

---

5. What are some Constraints in SQL?

<details><summary> Show Answer </summary>

<blockquote>

In SQL, a constraint is a rule that is defined on a table column or a group of columns to limit the type of data that can be inserted or updated in the table. Constraints help ensure data integrity and consistency by preventing invalid data from being stored in the table. Here are some common types of constraints in SQL:

- NOT NULL constraint: This constraint ensures that a column cannot contain NULL values. When a NOT NULL constraint is defined on a column, it means that every row in the table must have a value for that column.

- UNIQUE constraint: This constraint ensures that each value in a column or a group of columns is unique. When a UNIQUE constraint is defined on a column, it means that no two rows in the table can have the same value for that column.

- PRIMARY KEY constraint: This constraint is a combination of NOT NULL and UNIQUE constraints, and it ensures that each row in the table has a unique identifier. When a PRIMARY KEY constraint is defined on one or more columns, those columns become the primary key of the table.

- FOREIGN KEY constraint: This constraint ensures that a value in a column or a group of columns matches the value in another table's primary key or unique column. When a FOREIGN KEY constraint is defined on a column, it means that the values in that column must exist in the primary key or unique column of another table.

- CHECK constraint: This constraint ensures that the values in a column meet a certain condition. When a CHECK constraint is defined on a column, it means that the values in that column must meet the condition specified in the constraint.

- DEFAULT constraint: This constraint specifies a default value for a column if no value is provided during an insert operation. When a DEFAULT constraint is defined on a column, it means that if a value is not provided for that column during an insert operation, the default value will be used.

Constraints are an essential feature in SQL that helps maintain the quality and consistency of data in a database. By enforcing rules on the data, constraints ensure that the data is accurate and reliable, and it can be used effectively for various purposes.
</blockquote>

</details>

---

6. What is the difference between Primary Key and Unique Key?

<details><summary> Show Answer </summary>

<blockquote>
Both primary key and unique key are used to ensure the uniqueness of values in a column or a group of columns in a table. However, there are some differences between the two:

- Primary key: A primary key is a column or a group of columns that uniquely identifies each row in a table. It is used to enforce the integrity of the data and to ensure that each row has a unique identifier. A primary key can be defined on one or more columns, and it cannot contain NULL values. Each table can have only one primary key.

- Unique key: A unique key is a column or a group of columns that must contain unique values. It is used to ensure that no two rows in a table have the same values in the specified column(s). A unique key can be defined on one or more columns, and it can contain NULL values. Each table can have multiple unique keys.

Some key differences between primary key and unique key are:

- Primary keys are used to uniquely identify each row in a table, while unique keys are used to ensure that each row has unique values in the specified column(s).

- A primary key cannot contain NULL values, while a unique key can.

- Each table can have only one primary key, while it can have multiple unique keys.

- A foreign key in another table can reference a primary key in the current table, while a foreign key can reference a unique key as well.

Both primary key and unique key are used to ensure the uniqueness of values in a table, but primary key is used to uniquely identify each row in a table, while unique key is used to ensure unique values in a column or a group of columns.

</blockquote>

</details>

---
7. What is DDL?

<details><summary> Show Answer </summary>

<blockquote>

DDL stands for Data Definition Language. It is a set of SQL statements used to define, modify, and delete database objects such as tables, indexes, views, and constraints. DDL statements are used to create the database schema, which defines the structure and layout of the database.

Some common DDL statements in SQL include:

- CREATE: This statement is used to create a new database object such as a table, index, or view.

- ALTER: This statement is used to modify the structure of an existing database object such as a table, index, or view.

- DROP: This statement is used to delete an existing database object such as a table, index, or view.

- TRUNCATE: This statement is used to delete all the rows from a table, but the table structure remains intact.

DDL statements are used by database administrators and developers to define the structure of a database and to manage database objects. They play a crucial role in maintaining the integrity and consistency of the database, as they define the rules that govern the data stored in the database.

</blockquote>

</details>

---
8. Tell me some of the keywords for DDL?

<details><summary> Show Answer </summary>

<blockquote>

Here are some of the keywords used in DDL (Data Definition Language) in SQL:

- CREATE: This keyword is used to create a new database object such as a table, index, view, or constraint.

- ALTER: This keyword is used to modify the structure of an existing database object such as a table, index, view, or constraint.

- DROP: This keyword is used to delete an existing database object such as a table, index, view, or constraint.

- TRUNCATE: This keyword is used to delete all the rows from a table, but the table structure remains intact.

- RENAME: This keyword is used to rename an existing database object such as a table, column, or view.

- CONSTRAINT: This keyword is used to define a constraint on a database object such as a table, column, or view.

- INDEX: This keyword is used to create an index on a table.

- VIEW: This keyword is used to create a virtual table that is based on a select statement.


</blockquote>

</details>

---
9. How do you add a column to an existing table?

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
10. How to create a table in SQL?

<details><summary> Show Answer </summary>

<blockquote>

To create a new table in SQL, you can use the CREATE TABLE statement followed by the table name and the column definitions. Here's the basic syntax:
```sql
CREATE TABLE table_name (
   column1 datatype constraint,
   column2 datatype constraint,
   ...
);
```
where table_name is the name of the table you want to create, column1, column2, etc. are the column names, datatype is the data type of the column, and constraint is an optional constraint that can be added to the column.

For example, if you want to create a table named "employees" with columns for employee ID, name, age, and department, you can use the following SQL statement:
```sql
CREATE TABLE employees (
   emp_id INT PRIMARY KEY,
   name VARCHAR(50) NOT NULL,
   age INT,
   department VARCHAR(50)
);
```
This will create a new table "employees" with four columns: "emp_id", "name", "age", and "department". The "emp_id" column is defined as the primary key, while the "name" column is defined as not null, which means it cannot be left blank.

You can also add other constraints such as UNIQUE, CHECK, and FOREIGN KEY to the columns as required. Once the table is created, you can insert data into it using the INSERT INTO statement.


</blockquote>

</details>

---
11. How to change the data type for an attribute to a table 

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
12. DML in SQL. 

<details><summary> Show Answer </summary>

<blockquote>

DML stands for Data Manipulation Language, which is a sub-language of SQL used to manipulate the data stored in a database. DML commands are used to insert, update, delete, and retrieve data from a table. Some of the commonly used DML commands in SQL are:

- SELECT - used to retrieve data from one or more tables
- INSERT - used to insert new rows of data into a table
- UPDATE - used to modify existing data in a table
- DELETE - used to delete rows of data from a table
- MERGE - used to update or insert data based on a condition

</blockquote>

</details>

---
13. What is the difference between DELETE, TRUNCATE, and DROP?

<details><summary> Show Answer </summary>

<blockquote>

DELETE, TRUNCATE, and DROP are all SQL commands used to remove data or objects from a database, but they differ in their scope and level of impact.

DELETE is a DML (Data Manipulation Language) command that removes rows of data from a table. It is used to selectively remove specific rows of data based on a condition specified in the WHERE clause. DELETE only removes data from the table and does not remove the table itself.

TRUNCATE is a DDL (Data Definition Language) command that removes all rows from a table, but does not remove the table structure. TRUNCATE is much faster than DELETE because it does not need to log the individual row deletions, but it also cannot be rolled back once it is executed. TRUNCATE also resets the identity seed value for the table, so any subsequent inserts will start with the initial value.

DROP is a DDL command that removes a table or other database object from the database. When a table is dropped, all data, indexes, and constraints associated with the table are also removed. DROP is a very powerful command and should be used with caution, as it can lead to data loss if used incorrectly.

In summary, DELETE is used to remove individual rows of data based on a condition, TRUNCATE is used to remove all rows from a table, and DROP is used to remove a table or other database object entirely. The level of impact and scope of each command should be considered carefully before using it in a production environment.

</blockquote>

</details>

---
14. Will a sql database throw an exception 

<details><summary> Show Answer </summary>

<blockquote>

Yes, a SQL database can throw exceptions or errors when there is an issue with executing a SQL statement.

For example, if you try to insert a row into a table with a primary key value that already exists, the database will throw a primary key violation error. Similarly, if you try to create a table with a column name that already exists in another table, the database will throw a column name conflict error.

In addition to syntax errors, databases can also throw exceptions for various reasons such as constraints violations, transaction failures, deadlocks, and other issues.

It's important to handle these exceptions properly in your application code to ensure that your application can recover from errors gracefully and provide a good user experience.

</blockquote>

</details>

---
15. SQL vs noSQL

<details><summary> Show Answer </summary>

<blockquote>

SQL (Structured Query Language) and NoSQL (Not Only SQL) are two different approaches to storing and retrieving data.

SQL databases are relational databases that store data in tables with predefined schemas, where data is structured into rows and columns. SQL databases are best suited for applications that require complex queries, transactions, and data integrity. SQL databases use the ACID (Atomicity, Consistency, Isolation, Durability) model to ensure data consistency and reliability. Popular examples of SQL databases include MySQL, Oracle, Microsoft SQL Server, and PostgreSQL.

NoSQL databases, on the other hand, are non-relational databases that store data in flexible, unstructured formats such as documents, key-value pairs, and graphs. NoSQL databases are best suited for applications that require scalability, high availability, and fast, real-time data processing. NoSQL databases typically do not enforce a fixed schema, which makes them highly flexible and adaptable to changing data requirements. However, this flexibility can also make it harder to ensure data consistency and reliability. Popular examples of NoSQL databases include MongoDB, Cassandra, Redis, and Amazon DynamoDB.

The choice between SQL and NoSQL databases depends on the specific needs and requirements of your application. SQL databases are typically better suited for applications that require complex queries, transactions, and data integrity, while NoSQL databases are better suited for applications that require scalability, high availability, and real-time data processing. However, there are also hybrid databases that combine SQL and NoSQL features, offering the best of both worlds.

</blockquote>

</details>

---
16. What would you change about SQL

<details><summary> Show Answer </summary>

<blockquote>

Here are some common criticisms and potential improvements for SQL:

- Complexity: SQL can be complex and difficult to learn, especially for non-technical users. Improvements could be made to simplify the language and make it more accessible to beginners.

- Performance: SQL can be slow and inefficient for certain types of queries and data processing tasks. Improvements could be made to optimize the language for better performance and scalability.

- Lack of flexibility: SQL's fixed schema can make it difficult to adapt to changing data requirements. Improvements could be made to make the language more flexible and adaptable to changing data structures.

- Standardization: SQL is a widely used language, but there are many variations and dialects that can make it difficult to use across different platforms and systems. Improvements could be made to standardize the language and make it more consistent across different implementations.

Overall, SQL is a powerful and widely used language that has evolved over time to address many of its shortcomings. However, there is always room for improvement, and ongoing research and development are needed to ensure that SQL remains a relevant and effective tool for data management and analysis.

</blockquote>

</details>

---
17. difference between global and local tables in sql.

<details><summary> Show Answer </summary>

<blockquote>

In SQL, the terms "global" and "local" tables are not commonly used. However, there are concepts of global temporary tables and local temporary tables, which are specific to certain SQL implementations such as Oracle and SQL Server.

Global temporary tables are tables that are created once and shared across all users and sessions. They are typically used for temporary data storage and are automatically dropped at the end of the session or transaction. Global temporary tables can be accessed by any user or session, and their contents are visible to all sessions.

Local temporary tables, on the other hand, are tables that are created and accessed only within the context of a single session. They are typically used for temporary data storage within a particular session or transaction and are automatically dropped when the session or transaction ends. Local temporary tables are visible only within the session that created them, and their contents are not visible to other sessions or users.

The choice between global and local temporary tables depends on the specific needs and requirements of your application. Global temporary tables are useful for scenarios where multiple sessions or users need to share temporary data, while local temporary tables are useful for scenarios where temporary data is needed within a single session or transaction.

</blockquote>

</details>

---
18. PostgreSQL-how do you create a table and populate it in the same instance

<details><summary> Show Answer </summary>

<blockquote>

The CREATE TABLE AS statement creates a new table and fills it with the data returned by a query. The following shows the syntax of the CREATE TABLE AS statement:

```sql
CREATE TABLE new_table_name
AS query;
```
In this syntax:

- First, specify the new table name after the CREATE TABLE clause.
- Second, provide a query whose result set is added to the new table after the AS keyword.
```sql
CREATE TABLE action_film AS
SELECT
    film_id,
    title,
    release_year,
    length,
    rating
FROM
    film
INNER JOIN film_category USING (film_id)
WHERE
    category_id = 1;
```

</blockquote>

</details>

---
19. what is sqllite

<details><summary> Show Answer </summary>

<blockquote>

SQLite is a lightweight, open-source, self-contained, and serverless relational database management system (RDBMS) that is embedded in applications. It is widely used in mobile and desktop applications, as well as in small-scale web applications.

One of the main advantages of SQLite is its small size and low memory footprint, which makes it easy to integrate into applications and use on devices with limited resources. It also supports standard SQL syntax and provides a number of features common to larger RDBMSs, such as transactions, indexing, and triggers.

SQLite databases are stored as single files on disk, making them easy to distribute and manage. They can be accessed using a variety of programming languages, including C, C++, Java, Python, and others.

Some common use cases for SQLite include:

- Storing user data in mobile and desktop applications
- Caching data in web applications
- Storing configuration settings
- Storing temporary data
- Storing data for embedded systems and Internet of Things (IoT) devices

</blockquote>

</details>

---
20. what is sql  

<details><summary> Show Answer </summary>

<blockquote>
SQL (Structured Query Language) is a programming language used to manage and manipulate relational databases. It is the standard language used by most RDBMSs (Relational Database Management Systems) such as MySQL, Oracle, PostgreSQL, and Microsoft SQL Server, to perform tasks such as creating and modifying tables, inserting, updating and deleting data, and querying data from the database.

SQL provides a standardized syntax and set of commands for interacting with relational databases. It consists of several types of statements, including:

- Data definition language (DDL) statements: used to create, modify, and delete database objects such as tables, indexes, and constraints.
- Data manipulation language (DML) statements: used to insert, update, delete, and query data in tables.
- Data control language (DCL) statements: used to manage user access and permissions to database objects.
- Transaction control statements: used to manage transactions, which are groups of database operations that are executed as a single unit.

SQL is widely used in data-driven applications, from simple web applications to complex enterprise systems. It is a powerful and flexible language that can be used to manage and manipulate large amounts of data efficiently and effectively.

</blockquote>

</details>

---

21. What are parallel queries in sql

<details><summary> Show Answer </summary>

<blockquote>

Parallel queries in SQL are a feature that allows multiple processors or cores to work together to process a single SQL query in parallel, thereby reducing the query execution time. In other words, it enables the database to divide a single query into smaller parts that can be executed simultaneously on multiple processors, rather than executing the query sequentially on a single processor.

This feature is particularly useful for large, complex queries that involve multiple tables, joins, and aggregations, as it can significantly reduce the time it takes to process the query and return the results.

Parallel queries are supported by many relational database management systems, including Oracle, Microsoft SQL Server, and PostgreSQL. However, not all queries can benefit from parallel execution, and the performance gain achieved by parallel queries depends on several factors, including the complexity of the query, the hardware configuration, and the workload on the database server.

</blockquote>

</details>

---
22. What are Ranking Functions

<details><summary> Show Answer </summary>

<blockquote>

Ranking functions in SQL are a set of built-in functions that assign a rank or row number to each row in a result set based on certain criteria, such as the value of a specific column. These functions can be used to calculate rankings, percentiles, and other statistical measures in SQL queries.

There are several types of ranking functions in SQL, including:

- RANK: assigns a unique rank to each row within a result set, with ties receiving the same rank value.

- DENSE_RANK: assigns a unique rank to each row within a result set, with ties receiving the same rank value, but no gaps between ranks.

- ROW_NUMBER: assigns a unique row number to each row within a result set, with no regard for ties.

- NTILE: divides a result set into a specified number of groups, assigning a rank to each row based on which group it belongs to.

Ranking functions are commonly used in business intelligence and data analysis applications to identify trends, patterns, and outliers in large data sets. They can also be used to sort and filter data based on specific criteria, such as the top 10% of sales by region or the lowest 5% of customer satisfaction scores.
</blockquote>

</details>

---

















