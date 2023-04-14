1. What is an Inner Join?

<details> <summary>Show Answer</summary>
 
<blockquote>

An inner join is a type of relational database operation that combines data from two or more tables based on a common column or key. The result set of an inner join includes only the rows where the join condition is true, i.e., the values in the common column or key match between the tables being joined.

For example, consider two tables: "Customers" and "Orders". The "Customers" table has columns for customer ID, name, and email, while the "Orders" table has columns for order ID, customer ID, and order date. To combine data from these two tables based on the customer ID, you could use an inner join:

```java
SELECT *
FROM Customers
INNER JOIN Orders
ON Customers.CustomerID = Orders.CustomerID;
```
- This query would return all columns from both tables for only those rows where the customer ID matched between the two tables. The resulting table would contain information about customers who have placed orders, but would exclude customers who have not yet placed orders.

</blockquote>

</details>

---

2. What is an Outer Join?

<details> <summary>Show Answer</summary>
 
<blockquote>

An outer join is a type of database join operation that includes all records from one table and only matching records from another table. It is used to combine data from two or more tables based on a common field.

There are three types of outer joins:

**1. Left outer join:** This type of join returns all records from the left table (or the first table mentioned in the SQL statement) and matching records from the right table (or the second table mentioned in the SQL statement). If there is no matching record in the right table, the result will contain NULL values.

**2. Right outer join:** This type of join returns all records from the right table and matching records from the left table. If there is no matching record in the left table, the result will contain NULL values.

**3. Full outer join:** This type of join returns all records from both tables. If there is no matching record in one of the tables, the result will contain NULL values for the columns of that table.

Outer joins are useful when you want to include all the data from one table, even if there is no matching data in the other table.
  
</blockquote>

</details>

---

3. What is a join in SQL.

<details> <summary>Show Answer</summary>
 
<blockquote>
  
In SQL (Structured Query Language), a join is an operation that combines rows from two or more tables based on a related column between them. The main purpose of using a join is to retrieve and combine data from different tables that have a relationship.

To perform a join in SQL, you need to specify the tables to be joined and the columns that are used to relate the tables. There are different types of joins, like:

**1. Inner join:** This is the most common type of join, and it returns only the rows that have matching values in both tables. Inner join is also known as an equi-join.

**2. Left join:** Also known as a left outer join, this type of join returns all the rows from the left table and the matching rows from the right table. If there are no matching rows in the right table, NULL values are returned.

**3. Right join:** Also known as a right outer join, this type of join returns all the rows from the right table and the matching rows from the left table. If there are no matching rows in the left table, NULL values are returned.

**Full join:** Also known as a full outer join, this type of join returns all the rows from both tables. If there are no matching rows in one of the tables, NULL values are returned.

Joins are important in SQL because they allow you to combine data from multiple tables, which can be useful for generating reports, performing analysis, and querying complex data sets.


</blockquote>

</details>

---

4. What are SQL procedures?

<details> <summary>Show Answer</summary>
 
<blockquote>

SQL procedures are a set of SQL statements that are stored in the MySQL database server as a single unit, which can be called repeatedly by a program or a user. Procedures can be used to encapsulate complex logic, and they can also improve the performance of applications that access the database.

A procedure is created using the CREATE PROCEDURE statement, which defines the name of the procedure, its input parameters, and its SQL statements. Here is an example of creating a simple MySQL procedure:

```SQL
CREATE PROCEDURE get_employee(IN employee_id INT)
BEGIN
    SELECT * FROM employees WHERE id = employee_id;
END;

```

In this example, the procedure is named get_employee and it takes an input parameter called employee_id. The SQL statement inside the procedure selects all the columns from the employees table where the id column matches the input parameter value.

To execute the procedure, you can use the CALL statement:

```SQL
CALL get_employee(123);
```
This will execute the procedure and pass the value 123 as the employee_id parameter.

MySQL procedures can also return values using the OUT parameter. They can be used to perform transactions, loops, and other programming constructs. They can be very powerful tools for managing complex SQL operations in your application.
  
</blockquote>

</details>

---

5. SQL Procedures vs Functions?

<details> <summary>Show Answer</summary>
 
<blockquote>

|   | Procedures                                                                                    | Functions     |
| ----------------- | -------------------------------------------------------------------------------------- |-----------------------|
| Definition        | A named block of SQL code that can accept input parameters and return multiple values. | A named block of SQL code that returns a single value and can accept input parameters. |
| Purpose           | To perform a series of operations that may or may not return a result.                 | To perform a calculation and return a single value. |
| Return Value      | Can return multiple values, but not required.                                          | Must return a single value. |
| Data Modification | Can modify data.                                                                       | Cannot modify data. |
| Execution         | Executed using the CALL statement.                                                     | Executed as part of a SELECT statement. |
| Use in Query      | Cannot be used in a SELECT statement.                                                  | Can be used in a SELECT statement. |
  
</blockquote>

</details>

---

6. How do you get the second highest salary from the database?

<details> <summary>Show Answer</summary>
 
<blockquote>

To get the second highest salary from a database, you can use the following SQL query:

```mysql
SELECT MAX(salary) 
FROM employees 
WHERE salary < (SELECT MAX(salary) FROM employees);
```
or

```mysql
SELECT salary FROM employees ORDER BY salary DESC LIMIT 1 OFFSET 1 
```
  
  
</blockquote>

</details>

---

7. The use of GROUP BY clause?

<details> <summary>Show Answer</summary>
 
<blockquote>

The `GROUP BY` clause is a SQL statement used to group rows based on one or more columns in a table. The GROUP BY clause is typically used in combination with aggregate functions such as `SUM`, `AVG`, `MAX`, `MIN`, or `COUNT` to calculate summary statistics for each group.

</blockquote>

</details>

---

8. What is a cartesian join?

<details> <summary>Show Answer</summary>
 
<blockquote>

A cartesian join, also known as a cross join, is a type of join operation in SQL where all possible combinations of rows from two or more tables are returned in the result set. This means that every row from the first table is combined with every row from the second table, resulting in a result set that has a number of rows equal to the product of the number of rows in each table.

Synatx

```mysql
SELECT *
FROM table1
CROSS JOIN table2;
```
  
</blockquote>

</details>

---

9. What is a primary key in SQL.

<details> <summary>Show Answer</summary>
 
<blockquote>

In SQL, a table is a database object that stores data in rows and columns, while a view is a virtual table that is based on the result set of a SELECT statement.

Here are some of the key differences between tables and views:

**1. Data storage:** Tables are physical objects that store data on disk, while views are virtual objects that do not store data directly. Instead, views retrieve data from one or more tables, based on a query specified in the view definition.

**2. Definition:** A table has a fixed structure defined by its columns and data types, while a view can be defined dynamically by a SELECT statement. This means that the data in a view can change as the underlying data in the base tables changes.

**3. Data modification:** Tables can be used to add, modify, and delete data directly, while views are read-only by default. Some views can be made updatable, but only if they meet certain conditions.

**4. Security:**Views can be used to restrict access to certain columns or rows of data, while allowing users to access other columns or rows. This can help to enforce security policies and prevent unauthorized access to sensitive data.

**5. Performance:** Views can be used to simplify complex queries and reduce the amount of data that needs to be transferred over the network. However, views can also slow down queries if they are not well-optimized, or if they are based on large, complex queries.
  
</blockquote>

</details>

---

10. What is a view in SQL;

<details> <summary>Show Answer</summary>
 
<blockquote>

In SQL, a view is a virtual table that is based on the result set of a SELECT statement. A view allows you to create a customized, simplified view of the data that is easier to work with, and can be used to enforce security and abstract away details of the underlying tables.
  
</blockquote>

</details>

---

11. what is a foreign key?

<details> <summary>Show Answer</summary>
 
<blockquote>

A foreign key in SQL is a column or set of columns in one table that refers to the primary key of another table. It allows you to establish relationships between tables and enforce referential integrity.
  
</blockquote>

</details>

---

12. What is difference between Table and View in SQL?

<details> <summary>Show Answer</summary>
 
<blockquote>

| Feature              | Table                                                                | View                                                                                                        |
| -------------------- | -------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------- |
| Definition           | A physical structure that stores data in the database                | A virtual table that is based on the result set of a SELECT statement                                       |
| Storage              | Stores data on disk                                                  | Does not store data; retrieves data from one or more tables when queried                                    |
| Data Modification    | Allows direct insertion, update, and deletion of data                | Cannot be used to modify data directly; must modify underlying tables                                       |
| Schema               | Has its own schema that defines columns, data types, and constraints | Inherits schema of the SELECT statement that defines it                                                     |
| Query Simplification | Represents actual data as it is stored in the database               | Can simplify complex queries by providing a customized view of the data                                     |
| Security             | Does not provide any security features                               | Can be used to restrict access to certain columns or rows of data, enforcing security at the database level |
  
</blockquote>

</details>

---

13. How would you add a column to the database via SQL?


<details> <summary>Show Answer</summary>
 
<blockquote>

To add a new column to an existing table in SQL, you can use the `ALTER TABLE` statement followed by the table name and the `ADD COLUMN` clause, specifying the name and data type of the new column. Here's an example of how to add a new column to an existing table:

```mysql
ALTER TABLE customers 
ADD COLUMN address VARCHAR(100);
```

</blockquote>

</details>

---

14. How to create a table in SQL?

<details> <summary>Show Answer</summary>
 
<blockquote>

To create a table in SQL, you can use the `CREATE TABLE` statement followed by the table name and the list of columns and their data types.

Example:

```mysql
CREATE TABLE customers (
    id INT PRIMARY KEY,
    name VARCHAR(50),
    email VARCHAR(100),
    phone VARCHAR(20)
);
```

This CREATE TABLE statement creates a table named customers with four columns: id, name, email, and phone. The id column is defined as an integer with the `PRIMARY KEY` constraint.
  
</blockquote>

</details>

---

15. What do you need to change in the SELECT statement if you use a GROUP BY statement

<details> <summary>Show Answer</summary>
 
<blockquote>

- If you are using a `GROUP BY` statement in your SQL query, you will need to make some changes to your `SELECT` statement to ensure that it returns the desired results.

- When using `GROUP BY`, you are essentially grouping rows with similar values together based on the specified column. You can then perform aggregate functions such as `SUM`, `AVG`, `MIN`, `MAX`, or `COUNT` on each group to get summary information about the data.

- To use `GROUP BY` effectively, you need to include at least one column in your `SELECT` statement that is also included in the `GROUP BY` statement. This is because each row in the result set will correspond to a unique combination of values in the specified columns.
  
</blockquote>

</details>

---

16. Where would you place a COUNT() in SQL?

<details> <summary>Show Answer</summary>
 
<blockquote>

- In SQL, the `COUNT()` function is used to count the number of rows that match a specific condition in a table. `The COUNT()` function is typically used along with the `SELECT` statement to return the count of the number of rows that match a specific condition.

- The `COUNT()` function can be placed in the SELECT statement or in the WHERE clause, depending on the specific requirement.

If you want to count all rows in a table, you can use the COUNT(*) function in the SELECT statement like this:

```SQL
SELECT COUNT(*) FROM table_name;
```

If you want to count the number of rows that meet a specific condition, you can use the COUNT() function in the WHERE clause like this:

```SQL
SELECT COUNT(*) FROM table_name WHERE condition;
```
  
</blockquote>

</details>

---

17. Difference between where and having?

<details> <summary>Show Answer</summary>
 
<blockquote>

`WHERE` and `HAVING` are two clauses used in SQL queries to filter data.

The main difference between them is that `WHERE` clause filters data before it is grouped, whereas `HAVING` clause filters data after it is grouped.

The `WHERE` clause is used to filter rows based on conditions that are applied to individual rows before they are grouped. For example, if you want to retrieve all the records from a table where the age is greater than 18, you can use a "WHERE" clause like this:

```SQL
SELECT * FROM mytable WHERE age > 18;
```

The `HAVING` clause is used to filter the result set after grouping has been applied. It is typically used along with the "GROUP BY" clause. For example, if you want to retrieve the average salary for each department, but only for departments where the average salary is greater than 50,000, you can use a `HAVING` clause like this:

```SQL
SELECT department, AVG(salary) as avg_salary FROM mytable GROUP BY department HAVING avg_salary > 50000;
```
  
</blockquote>

</details>

---











