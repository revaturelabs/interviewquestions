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
  
</blockquote>

</details>

---

6. How do you get the second highest salary from the database?

<details> <summary>Show Answer</summary>
 
<blockquote>
  
</blockquote>

</details>

---

7. The use of GROUP BY clause?

<details> <summary>Show Answer</summary>
 
<blockquote>
  
</blockquote>

</details>

---

8. What is a cartesian join?

<details> <summary>Show Answer</summary>
 
<blockquote>
  
</blockquote>

</details>

---

9. What is a primary key in SQL.

<details> <summary>Show Answer</summary>
 
<blockquote>
  
</blockquote>

</details>

---

10. What is a view in SQL;

<details> <summary>Show Answer</summary>
 
<blockquote>
  
</blockquote>

</details>

---

11. what is a foreign key?

<details> <summary>Show Answer</summary>
 
<blockquote>
  
</blockquote>

</details>

---

12. What is difference between Table and View in SQL?

<details> <summary>Show Answer</summary>
 
<blockquote>
  
</blockquote>

</details>

---

13. How would you add a column to the database via SQL?


<details> <summary>Show Answer</summary>
 
<blockquote>
  
</blockquote>

</details>

---

14. How to create a table in SQL?

<details> <summary>Show Answer</summary>
 
<blockquote>
  
</blockquote>

</details>

---

15. What do you need to change in the SELECT statement if you use a GROUP BY statement

<details> <summary>Show Answer</summary>
 
<blockquote>
  
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











