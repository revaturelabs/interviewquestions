1. How to connect to a MongoDB or a PostgreSQL database?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
<blockquote>

**Java**

*MongoDB*

To connect to a MongoDB database in Java, you can use the MongoDB Java driver. Here's an example of connecting to a MongoDB database using the driver:

```java

import com.mongodb.client.MongoClients;
import com.mongodb.client.MongoClient;
import com.mongodb.client.MongoDatabase;

// Connection URI
String connectionString = "mongodb://localhost:27017";

// Database name
String databaseName = "mydatabase";

// Create a MongoDB client
MongoClient mongoClient = MongoClients.create(connectionString);

// Get the database
MongoDatabase database = mongoClient.getDatabase(databaseName);
```

In this example, we create a MongoClient object using the `MongoClients.create()` method and the connectionString variable, which specifies the connection string. We then use this client to get the mydatabase database using the databaseName variable.

*PostgreSQL*

To connect to a PostgreSQL database in Java, you can use the JDBC driver. Here's an example of connecting to a PostgreSQL database using the driver:

```java

import java.sql.Connection;
import java.sql.DriverManager;
import java.sql.SQLException;

// Connection details
String databaseHost = "localhost";
String databasePort = "5432";
String databaseName = "mydatabase";
String databaseUser = "myuser";
String databasePassword = "mypassword";

// Connection string
String connectionString = String.format("jdbc:postgresql://%s:%s/%s", databaseHost, databasePort, databaseName);

// Connect to the database
Connection connection = null;
try {
    connection = DriverManager.getConnection(connectionString, databaseUser, databasePassword);
} catch (SQLException e) {
    e.printStackTrace();
} finally {
    if (connection != null) {
        try {
            connection.close();
        } catch (SQLException e) {
            e.printStackTrace();
        }
    }
}
```
In this example, we create a connection string using the `String.format()` method, which takes the database host, port, and name as parameters. We then use this connection string to create a connection using the `DriverManager.getConnection()` method, passing in the username and password as parameters. Note that you will need to download and add the PostgreSQL JDBC driver to your project to use this code.

**C#**

*MongoDB*

To connect to a MongoDB database in C#, you can use the official MongoDB .NET driver. Here's an example of connecting to a MongoDB database using this driver:

```csharp

using MongoDB.Driver;

// Connection string
string connectionString = "mongodb://localhost:27017";

// Database name
string databaseName = "mydatabase";

// Create a MongoDB client
var client = new MongoClient(connectionString);

// Get the database
var database = client.GetDatabase(databaseName);
```

In this example, we create a MongoClient object using the connection string, and then use this client to get the mydatabase database.

*PostgreSQL*

To connect to a PostgreSQL database in C#, you can use the Npgsql library. Here's an example of connecting to a PostgreSQL database using Npgsql:

```csharp

using Npgsql;

// Connection details
string host = "localhost";
string port = "5432";
string databaseName = "mydatabase";
string username = "myuser";
string password = "mypassword";

// Connection string
string connectionString = $"Host={host};Port={port};Database={databaseName};Username={username};Password={password}";

// Connect to the database
var connection = new NpgsqlConnection(connectionString);
connection.Open();
```

In this example, we create a connection string using the `NpgsqlConnection` class, which takes the database name, username, password, host, and port as parameters. We then use this connection to execute queries. Note that you will need to install the Npgsql library to use this code.

**Python**

*MongoDB*

To connect to a MongoDB database in Python, you can use the PyMongo library. Here's an example of connecting to a MongoDB database using PyMongo:

```python

from pymongo import MongoClient

# Connection string
uri = "mongodb://localhost:27017"

# Database name
database_name = "mydatabase"

# Create a MongoDB client
client = MongoClient(uri)

# Get the database
database = client[database_name]
```

In this example, we create a MongoClient object using the connection string, and then use this client to get the mydatabase database.

*PostgreSQL*

To connect to a PostgreSQL database in Python, you can use the Psycopg2 library. Here's an example of connecting to a PostgreSQL database using Psycopg2:

```python

import psycopg2

# Connection details
host = "localhost"
port = "5432"
database_name = "mydatabase"
username = "myuser"
password = "mypassword"

# Connection string
connection_string = f"host={host} port={port} dbname={database_name} user={username} password={password}"

# Connect to the database
connection = psycopg2.connect(connection_string)
```

In this example, we create a connection string using the Psycopg2 library, which takes the database name, username, password, host, and port as parameters. We then use this connection to execute queries. Note that you will need to install the Psycopg2 library to use this code.

</blockquote>

</details>

---


2. What is a relational database?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
<blockquote>

A relational database is a type of database that stores and organizes data in a tabular form, with each row representing a unique record and each column representing a specific attribute of that record. In a relational database, data is organized into tables, which can be related to each other using common fields. The relationships between tables are defined by primary and foreign keys, which ensure that data is stored in a consistent and structured manner. Relational databases are widely used in business and enterprise applications, as well as in web and mobile applications.

</blockquote>

</details>

---

6. Can you differentiate between RDBMS and NoSQL? 

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
<blockquote>


RDBMS and NoSQL are two different types of database management systems. Here's a brief overview of their differences:

*Data model*: RDBMS follows a relational data model, which means data is organized in tables with predefined relationships between them. NoSQL, on the other hand, follows a non-relational data model, which means data can be organized in a variety of ways, such as key-value pairs, document-based, or graph-based.

*Schema*: RDBMS has a rigid schema, which means the structure of the database is predefined and cannot be changed without altering the schema. NoSQL, on the other hand, has a flexible schema, which means the structure of the database can be changed without affecting the data.

*Scalability*: RDBMS is vertically scalable, which means it can handle more data by adding more resources to a single server. NoSQL, on the other hand, is horizontally scalable, which means it can handle more data by adding more servers to a distributed system.

*Transactions*: RDBMS supports ACID transactions, which ensures data consistency and reliability. NoSQL, on the other hand, does not necessarily support ACID transactions and may prioritize other features such as scalability or availability.

</blockquote>

</details>

---

7. What is Normalization?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
<blockquote>

- Normalization refers to the process of organizing data in a database in such a way that it reduces redundancy and dependency among the data. This helps to improve data consistency and accuracy while reducing data anomalies and inconsistencies. 
- In other words, normalization ensures that data is structured in a way that minimizes redundancy and maximizes efficiency, making it easier to store, update, and retrieve information. 
- Normalization typically involves breaking down large tables into smaller ones and creating relationships between them, so that each piece of data is stored only once and related data is stored in separate tables.

</blockquote>

</details>

---

8. How do we decide not to normalize a table? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
<blockquote>

There are situations where normalization may not be the best approach for organizing data in a table. Here are some examples:

*When performance is a priority*: Normalization can sometimes result in complex joins and slower query performance. In cases where performance is a key requirement, denormalization can be used to store redundant data in a single table to improve query speed.

*When the data is small and simple*: If the data is relatively small and straightforward, it may not be necessary to normalize it. Normalization is most useful for complex and large datasets where reducing redundancy is important.

*When the data is temporary or temporary storage is needed*: In cases where the data is temporary or used for a short period of time, normalization may not be necessary. In these cases, it may be more convenient to store the data in a single table, without worrying about normalization.

*When the data is highly variable*: In some cases, the data may have highly variable structure or content, making normalization difficult. In such cases, it may be more appropriate to store the data in a less structured format, such as a NoSQL database.

</blockquote>

</details>

---

9.  Differentiate between BigData and RDBMS?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
<blockquote>

Yes, there are some key differences between big data and RDBMS (Relational Database Management Systems):

*Data Structure*: RDBMS relies on a structured approach to data storage, where data is stored in tables with fixed columns and rows. Big data, on the other hand, can be both structured and unstructured and doesn't require a fixed schema. This allows for more flexible storage of data that can be processed and analyzed in various ways.

*Scalability*: RDBMS typically has limitations on scalability due to its structured approach to data storage. Big data, on the other hand, is designed to handle large volumes of data and can scale horizontally to accommodate growing data volumes.

*Processing*: RDBMS typically relies on SQL queries to process data, which can be limiting in terms of the types of analysis that can be performed. Big data, on the other hand, relies on distributed computing technologies such as Hadoop and Spark, which allow for parallel processing of data across multiple nodes, enabling more complex and sophisticated analysis.

*Data Variety*: RDBMS typically works well with structured data but struggles with unstructured data such as text, images, and videos. Big data, on the other hand, can handle both structured and unstructured data, making it suitable for a wide range of use cases.

</blockquote>

</details>

---

10. What is the difference between SQL and MongoDB?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
<blockquote>

SQL and MongoDB are both database technologies, but they differ in several ways:

*Data Model*: SQL is a relational database management system (RDBMS), which means it stores data in tables with fixed columns and rows. MongoDB, on the other hand, is a NoSQL document database, which means it stores data in flexible, JSON-like documents.

*Query Language*: SQL uses a standardized query language called SQL (Structured Query Language) to retrieve data from tables. MongoDB uses its own query language, which is based on JSON and allows for more flexible querying of documents.

*Scalability*: SQL databases can scale vertically (by adding more CPU, memory, or storage to a single server) but have limitations in horizontal scalability (adding more servers to a cluster). MongoDB is designed to scale horizontally, which makes it easier to handle large amounts of data and high traffic loads.

*Data Consistency*: SQL databases are typically ACID compliant, which ensures data consistency and integrity. MongoDB, on the other hand, is designed for high availability and scalability, which means it may sacrifice some consistency in favor of availability and performance.

- SQL is a mature and reliable technology that is best suited for structured data storage and retrieval, while MongoDB is a more flexible and scalable technology that is ideal for handling unstructured data and high-traffic applications.

</blockquote>

</details>

---

11. How to set up a database?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
<blockquote>

Setting up a database involves the following steps:

*Identify the purpose and scope of the database*: The first step is to identify the purpose of the database and the scope of the data that will be stored in it. This will help determine the requirements for the database, including its structure, security, and performance.

*Choose a database management system (DBMS)*: Once the requirements have been identified, the next step is to choose a DBMS that meets those requirements. Popular DBMS options include MySQL, PostgreSQL, Oracle, MongoDB, and SQL Server.

*Design the database schema*: The database schema is the blueprint for how data will be organized and stored in the database. This involves identifying the tables, fields, and relationships that will be used to represent the data.

*Define data types and constraints*: Each field in the database must have a defined data type, such as text, integer, or date. Constraints can also be defined to ensure data consistency and integrity, such as unique keys, foreign keys, and check constraints.

*Implement the database schema*: With the database schema defined, the next step is to create the database and tables, and define the fields and relationships.

*Populate the database with data*: Once the database has been set up, it can be populated with data. This can be done manually or by importing data from external sources.

*Test and optimize the database*: The final step is to test the database and optimize it for performance. This involves running queries and monitoring system resources to ensure that the database is running efficiently and meeting performance requirements. Indexes and other optimizations may also be added to improve query performance.

</blockquote>

</details>

---

13. What are the relationships in RDBMS?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
<blockquote>

In a relational database management system (RDBMS), there are three main types of relationships between tables:

*One-to-one (1:1) relationship*: This relationship exists when each record in one table is associated with exactly one record in another table, and vice versa.

*One-to-many (1:N) relationship*: This relationship exists when each record in one table is associated with one or more records in another table, but each record in the second table is associated with only one record in the first table.

*Many-to-many (N:M) relationship*: This relationship exists when each record in one table is associated with one or more records in another table, and each record in the second table is associated with one or more records in the first table.

</blockquote>

</details>

---

14. What is a data dictionary?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
<blockquote>

- A data dictionary is a centralized repository of information about the data in a database or information system. It provides a comprehensive description of each data element or attribute in the system, such as the data type, length, allowed values, default values, and relationships to other data elements.
- It is an essential tool for managing and understanding the data in a complex information system or database.

</blockquote>

</details>

---

17. What is Dynamic Hashing?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
<blockquote>

Dynamic hashing is a technique used in database systems to manage hash tables with a flexible size that can be increased or decreased as needed to store and retrieve data efficiently. It handles collisions by splitting and rehashing the table or combining it with a neighbor, depending on the number of records stored in it. This approach is commonly used in applications that handle large amounts of data.

</blockquote>

</details>

---

19. What is Referential Integrity?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary> <b>Show Answer</b> </summary>
<blockquote>

Referential Integrity is a feature in RDBMS that ensures the consistency and accuracy of data relationships between tables. It enforces rules for how related data should be handled when changes are made to the data to maintain data integrity. This is typically done through the use of foreign keys, which refer to the primary key of another table.

</blockquote>

</details>

---

20. List the different types of databases?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
<blockquote>

There are several types of databases, each designed to handle specific data storage and management needs. Here are some common types of databases:

- *Relational databases*: These databases use a structured format with well-defined tables, columns, and relationships between them. Examples include MySQL, Oracle, and Microsoft SQL Server.

- *NoSQL databases*: These databases use a non-structured format that allows for flexible data storage and retrieval, with no fixed schema. Examples include MongoDB, Cassandra, and Redis.

- *Object-oriented databases*: These databases store data in objects, which can include methods, attributes, and relationships with other objects. Examples include db4o and ObjectStore.

- *Graph databases*: These databases use a graph-based data model, where data is represented as nodes, edges, and properties. Examples include Neo4j and Amazon Neptune.

- *Time-series databases*: These databases are optimized for storing and querying large volumes of time-series data, such as stock prices or sensor readings. Examples include InfluxDB and TimescaleDB.

- *Spatial databases*: These databases are optimized for storing and querying spatial data, such as maps or geographic information. Examples include PostGIS and ArcGIS.

- *Cloud databases*: These databases are designed to run on cloud platforms and offer features such as scalability, high availability, and global access. Examples include Amazon Aurora, Google Cloud SQL, and Microsoft Azure SQL Database.

</blockquote>

</details>

---

21. What is OLTP and OLAP?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
<blockquote>

OLTP and OLAP are two types of systems used for managing and analyzing data.

`OLTP (Online Transaction Processing)` is a database management system designed for managing real-time transaction processing. It is optimized for handling high volumes of simple, short, and quick transactions, such as those in banking, retail, or airline reservation systems. The focus of OLTP is on data processing speed, data consistency, and transactional integrity.

`OLAP (Online Analytical Processing)` is a database management system designed for complex data analysis and business intelligence reporting. It is optimized for querying and analyzing large datasets, typically using complex queries that aggregate data across multiple dimensions. The focus of OLAP is on data analysis, decision-making, and business insights.

</blockquote>

</details>

---

25. what is a cluster?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
<blockquote>

A cluster is a group of servers or nodes that work together to provide higher performance, availability, and scalability than a single server could provide on its own. They can be used to improve the performance and reliability of database systems by distributing the workload across multiple servers and providing redundancy in case of server failure.

</blockquote>

</details>

---

3. What is a record type?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary> Show Answer </summary>

<blockquote>

- In SQL, a record type is a user-defined data type that represents a collection of related values. A record type is similar to a struct in other programming languages, and it allows you to define a custom data structure with its own fields and data types.

To define a record type in SQL, you use the CREATE TYPE statement. Here's an example:
```sql
CREATE TYPE person_type AS (
    first_name VARCHAR(50),
    last_name VARCHAR(50),
    email VARCHAR(100)
);
```
In this example, we define a record type called "person_type" with three fields: "first_name", "last_name", and "email". Each field has its own data type, which is specified after the field name.

- Once you have defined a record type, you can use it as a data type for columns in tables or as a return type for stored procedures and functions. Here's an example of using the "person_type" record type as a column type:
```sql
CREATE TABLE employees (
    id INT,
    name person_type
);
```
In this example, we define a table called "employees" with two columns: "id" and "name". The "name" column is of type "person_type", which means it can store values with the same structure as the "person_type" record type we defined earlier.

- Record types are a powerful feature in SQL that allow you to define custom data structures and make your database schema more expressive and easier to understand.

</blockquote>

</details>

---

5. List some Constraints used in SQL?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary> Show Answer </summary>

<blockquote>

- In SQL, a constraint is a rule that is defined on a table column or a group of columns to limit the type of data that can be inserted or updated in the table. Constraints help ensure data integrity and consistency by preventing invalid data from being stored in the table. Here are some common types of constraints in SQL:

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

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

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

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

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
8. List the commands of DDL with its purpose?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

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

10. How to create a table in SQL?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary> Show Answer </summary>

<blockquote>

- To create a new table in SQL, you can use the CREATE TABLE statement followed by the table name and the column definitions. Here's the basic syntax:
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

12. Explain DML in SQL. 

 ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

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

15. Differentiate between SQL vs noSQL ?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

- SQL (Structured Query Language) and NoSQL (Not Only SQL) are two different approaches to storing and retrieving data.

- SQL databases are relational databases that store data in tables with predefined schemas, where data is structured into rows and columns. SQL databases are best suited for applications that require complex queries, transactions, and data integrity. SQL databases use the ACID (Atomicity, Consistency, Isolation, Durability) model to ensure data consistency and reliability. Popular examples of SQL databases include MySQL, Oracle, Microsoft SQL Server, and PostgreSQL.

- NoSQL databases, on the other hand, are non-relational databases that store data in flexible, unstructured formats such as documents, key-value pairs, and graphs. NoSQL databases are best suited for applications that require scalability, high availability, and fast, real-time data processing. NoSQL databases typically do not enforce a fixed schema, which makes them highly flexible and adaptable to changing data requirements. However, this flexibility can also make it harder to ensure data consistency and reliability. Popular examples of NoSQL databases include MongoDB, Cassandra, Redis, and Amazon DynamoDB.

- The choice between SQL and NoSQL databases depends on the specific needs and requirements of your application. SQL databases are typically better suited for applications that require complex queries, transactions, and data integrity, while NoSQL databases are better suited for applications that require scalability, high availability, and real-time data processing. However, there are also hybrid databases that combine SQL and NoSQL features, offering the best of both worlds.

</blockquote>

</details>

---

16. Difference between global and local tables in sql.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

- In SQL, the terms "global" and "local" tables are not commonly used. However, there are concepts of global temporary tables and local temporary tables, which are specific to certain SQL implementations such as Oracle and SQL Server.

- Global temporary tables are tables that are created once and shared across all users and sessions. They are typically used for temporary data storage and are automatically dropped at the end of the session or transaction. Global temporary tables can be accessed by any user or session, and their contents are visible to all sessions.

- Local temporary tables, on the other hand, are tables that are created and accessed only within the context of a single session. They are typically used for temporary data storage within a particular session or transaction and are automatically dropped when the session or transaction ends. Local temporary tables are visible only within the session that created them, and their contents are not visible to other sessions or users.

- The choice between global and local temporary tables depends on the specific needs and requirements of your application. Global temporary tables are useful for scenarios where multiple sessions or users need to share temporary data, while local temporary tables are useful for scenarios where temporary data is needed within a single session or transaction.

</blockquote>

</details>

---

18. what is SQLite?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

- SQLite is a lightweight, open-source, self-contained, and serverless relational database management system (RDBMS) that is embedded in applications. It is widely used in mobile and desktop applications, as well as in small-scale web applications.

- One of the main advantages of SQLite is its small size and low memory footprint, which makes it easy to integrate into applications and use on devices with limited resources. It also supports standard SQL syntax and provides a number of features common to larger RDBMSs, such as transactions, indexing, and triggers.

- SQLite databases are stored as single files on disk, making them easy to distribute and manage. They can be accessed using a variety of programming languages, including C, C++, Java, Python, and others.

Some common use cases for SQLite include:

- Storing user data in mobile and desktop applications
- Caching data in web applications
- Storing configuration settings
- Storing temporary data
- Storing data for embedded systems and Internet of Things (IoT) devices

</blockquote>

</details>

---
19. what is sql?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  

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

20. What are parallel queries in sql?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

- Parallel queries in SQL are a feature that allows multiple processors or cores to work together to process a single SQL query in parallel, thereby reducing the query execution time. In other words, it enables the database to divide a single query into smaller parts that can be executed simultaneously on multiple processors, rather than executing the query sequentially on a single processor.

- This feature is particularly useful for large, complex queries that involve multiple tables, joins, and aggregations, as it can significantly reduce the time it takes to process the query and return the results.

- Parallel queries are supported by many relational database management systems, including Oracle, Microsoft SQL Server, and PostgreSQL. However, not all queries can benefit from parallel execution, and the performance gain achieved by parallel queries depends on several factors, including the complexity of the query, the hardware configuration, and the workload on the database server.

</blockquote>

</details>

---
21. What are Ranking Functions?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

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
22. What is a primary key in SQL ?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>


In SQL, a primary key is a column or a set of columns in a table that uniquely identifies each row in the table. The primary key constraint is used to enforce this uniqueness requirement and ensure that the data in the table is consistent and correct.

The primary key serves as a reference point for other tables in the database to establish relationships between tables. For example, in a sales database, the primary key in the customer table could be used as a foreign key in the sales order table to link each order to a specific customer.

Some key characteristics of a primary key in SQL include:

- It must contain unique values for each row in the table.
- It cannot contain null values.
- It should be composed of one or more columns that have an appropriate data type, such as integer or character.
Creating a primary key in SQL involves specifying the PRIMARY KEY constraint when creating a table or altering an existing table. A table can have only one primary key, but it can be composed of multiple columns if necessary.
</blockquote>

</details>

---
24. How do you create a primary key?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

In SQL, you can create a primary key constraint on a column or a set of columns when you create a table or alter an existing table. Here are the steps to create a primary key in SQL:

- When creating a new table, include a column or a set of columns that uniquely identify each row in the table.

For example, if you are creating a table for customers, you might include a column for the customer ID that is unique for each customer:
```sql
CREATE TABLE customers (
    customer_id INT PRIMARY KEY,
    first_name VARCHAR(50),
    last_name VARCHAR(50),
    email VARCHAR(255)
);
```
- If you already have a table, you can alter the table to add a primary key constraint using the ALTER TABLE statement.

For example, if you have a table called orders and you want to add a primary key constraint on the order ID column, you can use the following statement:
```sql
ALTER TABLE orders
ADD CONSTRAINT pk_orders PRIMARY KEY (order_id);
```
This will add a primary key constraint to the order_id column in the orders table.

</blockquote>

</details>

---
25. What is a foreign key and how do you create it ?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>
A foreign key is a column or a set of columns in a table that refers to the primary key or the unique key of another table. It is used to establish a relationship between two tables in a relational database.

When you create a foreign key, it creates a constraint that ensures data integrity and consistency between the two tables. The foreign key constraint ensures that any value in the foreign key column of the referencing table must exist in the primary key or unique key column of the referenced table.

Here are the steps to create a foreign key in SQL:

- Create the referenced table and define a primary key or a unique key constraint on the column(s) that you want to reference.

For example, if you have a table called products and you want to reference the product_id column in another table, you can create the products table with a primary key on the product_id column:
```sql
CREATE TABLE products (
    product_id INT PRIMARY KEY,
    product_name VARCHAR(50),
    category VARCHAR(50),
    price DECIMAL(10, 2)
);
```
- Create the referencing table and include a foreign key column that refers to the primary key or unique key of the referenced table.

For example, if you have a table called orders and you want to reference the product_id column in the products table, you can create the orders table with a foreign key on the product_id column:
```sql
CREATE TABLE orders (
    order_id INT PRIMARY KEY,
    order_date DATE,
    product_id INT,
    quantity INT,
    FOREIGN KEY (product_id) REFERENCES products (product_id)
);
```
This will create a foreign key constraint on the product_id column in the orders table that references the product_id column in the products table. The foreign key constraint ensures that any value in the product_id column of the orders table must exist in the product_id column of the products table.

</blockquote>

</details>

---
26. What are CRUD operations?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>
CRUD stands for Create, Read, Update, and Delete. It's a set of basic operations that can be performed on data in a database or other data storage systems. These operations are fundamental to the management of data in most software applications.

Here's what each operation does:

- Create: This operation creates new data and stores it in the database. For example, creating a new user account in a social media application.
- Read: This operation retrieves data from the database. For example, reading a user's profile information from a social media application.
- Update: This operation modifies existing data in the database. For example, updating a user's profile picture in a social media application.
- Delete: This operation removes data from the database. For example, deleting a user account from a social media application.

Together, these four operations provide the basic functionality needed to manage data in most software applications

</blockquote>

</details>

---

27. What is the use of LIKE operator?


![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

The LIKE operator is used in SQL (Structured Query Language) to search for a pattern within a string column of a table.

It's used in the WHERE clause of a SELECT statement to filter the results based on a pattern match. The pattern can include wildcard characters to match any number of characters or a specific character.

Here's an example:
```sql
SELECT * FROM employees
WHERE last_name LIKE 'Sm%';
```
This SQL statement retrieves all rows from the "employees" table where the "last_name" column starts with the letters "Sm".

The % symbol is a wildcard character that matches any number of characters in the pattern. So, in this case, the query would return any employee with a last name that starts with "Sm", such as "Smith", "Smythe", or "Smeaton".

The LIKE operator is useful for searching for data that matches a specific pattern, such as email addresses, phone numbers, or names that follow a certain format.

</blockquote>

</details>

---
28. what is Parent-child relationship SQL?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

In SQL, a parent-child relationship refers to a type of relationship between two tables, where one table is the parent and the other table is the child. The parent table is usually the table that contains the primary key, and the child table is the table that contains a foreign key that references the primary key in the parent table.

Here's an example of how to create a parent-child relationship between two tables:
```sql
CREATE TABLE orders (
  order_id INT PRIMARY KEY,
  customer_id INT,
  order_date DATE,
  total_amount DECIMAL(10,2)
);

CREATE TABLE order_items (
  order_item_id INT PRIMARY KEY,
  order_id INT,
  product_id INT,
  quantity INT,
  price DECIMAL(10,2),
  FOREIGN KEY (order_id) REFERENCES orders(order_id)
);
```
In this example, the "orders" table is the parent table, and the "order_items" table is the child table. The "orders" table contains the primary key "order_id", and the "order_items" table contains a foreign key "order_id" that references the primary key in the "orders" table.

This relationship means that each order can have multiple items, and each item belongs to a single order. The foreign key constraint ensures that an order item can only be associated with an existing order.

</blockquote>

</details>

---