1. How to connect to a MongoDB or a PostgreSQL database?

<details> <summary>Show Answer</summary>
 
<blockquote>

To connect to a MongoDB or a PostgreSQL database in a Spring application, you'll need to follow these general steps:

**1. Add the necessary dependencies:** You'll need to add the database-specific dependencies to your project's build file (e.g., pom.xml for Maven or build.gradle for Gradle).

**2. Configure the database connection:** You'll need to add database connection properties to your application.properties or application.yml file to specify the connection details for your database.

**3. Create a data access object (DAO) or repository:** You'll need to create a DAO or repository interface that extends the appropriate Spring Data interface (e.g., MongoRepository for MongoDB or JpaRepository for PostgreSQL).

**4. Use the DAO or repository in your service layer:** You can use the DAO or repository in your service layer to perform CRUD (create, read, update, delete) operations on the database.
  
</blockquote>

</details>

2. What is a relational database?

<details> <summary>Show Answer</summary>
 
<blockquote>

A relational database is a type of database that organizes data into tables with columns and rows, and establishes relationships between the tables based on common data points. It is widely used for managing structured data and allows for efficient querying and data consistency. Examples include MySQL, Oracle, SQL Server, and PostgreSQL.
  
</blockquote>

</details>

3. How do we connect tables in RDS?

<details> <summary>Show Answer</summary>
 
<blockquote>

In Amazon Relational Database Service (RDS), you can connect tables using primary keys and foreign keys.

1. A primary key is a column or a set of columns that uniquely identifies each row in a table.
2. A foreign key is a column in a table that refers to the primary key of another table, establishing a relationship between the two tables.
To connect tables in RDS:

**Create a table with a primary key:** When creating a table, you'll need to define a primary key column or columns that will uniquely identify each row in the table.

**Create a table with a foreign key:** When creating another table that you want to relate to the first table, you'll need to define a column that will serve as a foreign key. This column will refer to the primary key column in the first table.

**Define the relationship:** Once you've created both tables, you'll need to define the relationship between them. This involves specifying the foreign key column in the second table and the primary key column in the first table.

**Use joins to query related data:** To query data from both tables, you can use a join operation that combines the rows from both tables based on the relationship established by the foreign key and primary key columns.

Note that the exact steps for connecting tables in RDS may vary depending on the specific database engine being used (e.g. MySQL, PostgreSQL, SQL Server).
  
</blockquote>

</details>

4. Why would you use SQL over noSQL?  Vice versa?

<details> <summary>Show Answer</summary>
 
<blockquote>
  
</blockquote>

</details>

5. Do you know what ACID is?

<details> <summary>Show Answer</summary>
 
<blockquote>
  
</blockquote>

</details>

<details> <summary>Show Answer</summary>
 
<blockquote>
  
</blockquote>

</details>

<details> <summary>Show Answer</summary>
 
<blockquote>
  
</blockquote>

</details>


<details> <summary>Show Answer</summary>
 
<blockquote>
  
</blockquote>

</details>