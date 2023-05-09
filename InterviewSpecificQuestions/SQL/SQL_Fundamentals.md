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



