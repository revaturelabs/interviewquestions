1. What are the different types of joins in SQL?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details><summary><b> Show Answer</b></summary>
  
<blockquote>
There are several types of joins in SQL:

- INNER JOIN: returns only the matching records from both tables.
- LEFT JOIN: returns all records from the left table and matching records from the right table.
- RIGHT JOIN: returns all records from the right table and matching records from the left table.
- FULL OUTER JOIN: returns all records when there is a match in either left (table1) or right (table2) table records.
- CROSS JOIN: returns the Cartesian product of both tables, which means it returns all possible combinations of the rows from both tables.

</blockquote>

</details>


---

2. What is a join in SQL?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details><summary><b> Show Answer</b></summary>
  
<blockquote>
In SQL, a join is used to combine rows from two or more tables based on a related column between them. A join is performed using the JOIN keyword and can be used to extract data from multiple tables as if they were a single table. The relationship between tables is usually defined by a foreign key constraint that specifies which columns in one table match which columns in another table.
</blockquote>

</details>

---

3. What happens to a genre if there are no movies associated with it?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details><summary><b> Show Answer</b></summary>
  
<blockquote>
 The genre will still be included in the result set, but the movie column values for that genre will be NULL. This is because the SQL engine still includes all rows from the first table (the one specified before the LEFT JOIN or RIGHT JOIN keyword) in the result set, regardless of whether there is a match in the second table (the one specified after the JOIN keyword).
</blockquote>

</details>

---

4. What is a cartesian join?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details><summary><b> Show Answer</b></summary>
  
<blockquote>
A Cartesian join, also known as a cross join, is a join operation in SQL that returns the Cartesian product of two tables. In other words, it returns all possible combinations of rows from both tables, regardless of whether there is a matching value in the related columns. The result of a Cartesian join between two tables with n and m rows, respectively, is a table with n x m rows.
</blockquote>

</details>

---


5. What is a left outer join?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details><summary><b> Show Answer</b></summary>
  
<blockquote>
A left outer join, also known as a left join, is a type of join operation in SQL that returns all records from the left table and matching records from the right table. If there is no match in the right table, the result will contain NULL values for the right table's columns. The LEFT JOIN keyword is used to perform a left outer join. Here is an example query:

```sql
SELECT *
FROM table1
LEFT JOIN table2
ON table1.column_name = table2.column_name;
```

This query will return all records from 'table1' and matching records from 'table2', based on the condition that 'column_name' in 'table1' matches 'column_name' in 'table2'.
</blockquote>

</details>

---

6. What is the difference between a Union and a Join in SQL? 

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>
A join in SQL combines rows from two or more tables based on a related column between them. It is used to extract data from multiple tables as if they were a single table. A union, on the other hand, combines rows from two or more SELECT statements into a single result set. The result set of a union operation contains all the rows from each SELECT statement, with duplicates removed.

In other words, a join combines columns from different tables into a single result set, while a union combines rows from different SELECT statements into a single result set.
</blockquote>

</details>

---

7. What are Outer Join and Full Outer Join?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details><summary><b> Show Answer</b></summary>
  
<blockquote>
An outer join is a join operation in SQL that returns all records from one table and matching records from another table. There are two types of outer joins: left outer join and right outer join. A left outer join returns all records from the left table and matching records from the right table, while a right outer join returns all records from the right table and matching records from the left table. If there is no match in the right or left table, the result will contain NULL values for the unmatched table's columns.

A full outer join, on the other hand, returns all records from both tables, with matching records from both tables, and NULL values for non-matching records. The FULL OUTER JOIN keyword is used to perform a full outer join. Here is an example query:

```sql
SELECT *
FROM table1
FULL OUTER JOIN table2
ON table1.column_name = table2.column_name;
```

This query will return all records from both 'table1' and 'table2', based on the condition that 'column_name' in 'table1' matches 'column_name' in 'table2', with NULL values for non-matching records.
</blockquote>

</details>

---

8. What is a Cross Join?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>
A cross join, also known as a Cartesian product, is a type of join operation in SQL that returns the combination of every row from two or more tables. It does not require any join conditions. In other words, a cross join returns the product of the number of rows in each table.

Here is an example query that performs a cross join between two tables 'table1' and 'table2':

```sql
SELECT *
FROM table1
CROSS JOIN table2;
```

This query will return the combination of every row from 'table1' and 'table2', resulting in a Cartesian product of the two tables.
</blockquote>

</details>

---

9. Let's say you have two tables with a common column between them (primary key and foreign key), how do you join these tables so that each row says which table it belongs to: Table A, Table B, or Both Tables?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>
To join two tables with a common column between them and indicate the source table of each row, you can use the UNION ALL operator to combine the results of two SELECT statements that use the same columns and aliases to identify the source table. Here is an example query:

```sql
SELECT 'Table A' AS table_name, column1, column2, column3
FROM tableA
UNION ALL
SELECT 'Table B' AS table_name, column1, column2, column3
FROM tableB;
```

This query will return a result set that includes all the rows from both 'tableA' and 'tableB', with an additional column called 'table_name' that indicates whether the row came from 'tableA', 'tableB', or both.
</blockquote>

</details>

---

10. How would you combine the data of two different SQL tables? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>
To combine the data of two different SQL tables, you can use the UNION operator to combine the results of two SELECT statements that have the same number of columns and compatible data types. The UNION operator removes any duplicate rows from the combined result set.

Here is an example query that combines the data of two tables 'table1' and 'table2':

```sql
SELECT column1, column2
FROM table1
UNION
SELECT column1, column2
FROM table2;
```

This query will return a result set that combines the rows from 'table1' and 'table2' and removes any duplicate rows.
</blockquote>

</details>

---


11. How to write a SQL query using joins for a database with 3 tables?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>
To write an SQL query that joins 3 tables, you need to use multiple join operations. The specific type of join operation depends on the relationship between the tables and the data you want to extract. Here is an example of a query that joins 3 tables:

Consider we have three tables, 'customers', 'orders', and 'order_details', with the following columns:

- customers: customer_id, customer_name, customer_email
- orders: order_id, customer_id, order_date
- order_details: order_id, product_name, quantity, price

We want to retrieve the following information: customer_name, order_date, product_name, quantity, and price. Here is a sample query:

```sql
SELECT c.customer_name, o.order_date, od.product_name, od.quantity, od.price
FROM customers c
INNER JOIN orders o
ON c.customer_id = o.customer_id
INNER JOIN order_details od
ON o.order_id = od.order_id;
```

This query joins the 'customers' table with the 'orders' table based on the 'customer_id' column, and then joins the resulting table with the 'order_details' table based on the 'order_id' column. The SELECT statement then specifies the columns we want to retrieve from the joined tables. Note that we used INNER JOIN for both joins, which means that only rows with matching values in both tables are included in the result set. You can also use other types of join operations, such as LEFT JOIN or RIGHT JOIN, depending on your needs.
</blockquote>

</details>

---


12. Difference between INNER JOIN and FULL OUTER JOIN
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>
INNER JOIN returns only the matching records from both tables while FULL OUTER JOIN returns all records from both tables along with the matching records.
</blockquote>

</details>

---

13. What is the difference between a right join and a left join?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>
LEFT JOIN returns all records from the left table and matching records from the right table, while RIGHT JOIN returns all records from the right table and matching records from the left table.
</blockquote>

</details>

---

14. How can you join tables without a primary key?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>
You can join tables without a primary key by using a common field between the tables as a join condition. However, this can result in slower query performance and potential data inaccuracies, so it is generally recommended to have a primary key for each table and use that as the join condition.
</blockquote>

</details>

---

15. What is the difference between a join and a join with a select statement?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>
A join combines data from two or more tables based on a specified condition, while a join with a select statement involves joining a subquery with a table based on a specified condition. The subquery can be used to filter or aggregate data before joining it with the table.
</blockquote>

</details>

---



16. What is an inner join?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>
An inner join is a type of join in SQL that returns only the matching records from both tables based on a specified condition. The join condition is typically a shared column or set of columns between the tables.
</blockquote>

</details>

---


17. Describe right join

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>
A right join is a type of join in SQL that returns all records from the right table and matching records from the left table based on a specified condition. If there is no match in the left table, the result will contain NULL values for the left table columns.
</blockquote>

</details>

---

18. Differentiate between Outer join and minus with a example.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary><b> Show Answer</b></summary>
  
<blockquote>
An outer join and a minus operation are two different types of SQL operations. 

An outer join is used to return all the records from one or both of the tables being joined, along with matching records where the specified join condition is met. There are three types of outer join: LEFT, RIGHT, and FULL. The syntax for a left outer join, for example, is as follows:

```sql
SELECT *
FROM Table1
LEFT OUTER JOIN Table2
ON Table1.ID = Table2.ID;
```

The minus operator, also known as EXCEPT, is used to return only the distinct rows that appear in one query but not in another. The syntax for a minus operation is as follows:

```sql
SELECT *
FROM Table1
MINUS
SELECT *
FROM Table2;
```

The minus operator is useful for finding differences between two sets of data, while an outer join is useful for combining data from multiple tables.

</blockquote>

</details>

---

19. Explain Intersect operator with an example.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>
The INTERSECT operator in SQL is used to return only the distinct rows that are returned by both the SELECT statements on either side of the operator. The syntax for an intersect operation is as follows:

```sql
SELECT *
FROM Table1
INTERSECT
SELECT *
FROM Table2;
```

The INTERSECT operator can be useful for finding common rows between two tables or sets of data. It returns only the matching rows and eliminates duplicates, so it can be used to validate data and ensure consistency between multiple sources.

</blockquote>

</details>

---

20. Differentiate between right outer join and  left outer join 

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary><b> Show Answer</b></summary>

<blockquote>

A LEFT OUTER JOIN and a RIGHT OUTER JOIN are similar types of join operations in SQL, with the main difference being the table from which all the rows are included. 
In a LEFT OUTER JOIN, all the rows from the table on the left side of the JOIN clause are included, along with the matching rows from the table on the right side of the JOIN clause. Any unmatched rows from the table on the left side will be included with NULL values in the result set.

In a RIGHT OUTER JOIN, all the rows from the table on the right side of the JOIN clause are included, along with the matching rows from the table on the left side of the JOIN clause. Any unmatched rows from the table on the right side will be included with NULL values in the result set.

The syntax for a LEFT OUTER JOIN is as follows:

```sql
SELECT *
FROM Table1
LEFT OUTER JOIN Table2
ON Table1.ID = Table2.ID;
```

The syntax for a RIGHT OUTER JOIN is as follows:

```sql
SELECT *
FROM Table1
RIGHT OUTER JOIN Table2
ON Table1.ID = Table2.ID;
```

</blockquote>

</details>

---

21. What is the difference between an inner join and a cartesian product?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Inner join returns the rows that have matching values in both tables based on the specified join condition. Cartesian product, on the other hand, returns the combination of all rows in both tables regardless of whether or not there is a match based on the join condition. It is also known as cross join, and can be generated by simply using the keyword "CROSS JOIN" between two tables.

</blockquote>

</details>

---

22. Consider You have three tables, "Customers", "Orders", and "Payments". Each customer can have multiple orders, and each order can have multiple payments. Write a query to retrieve all customers along with their total order count and total payment count.

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

```sql

SELECT c.CustomerID, c.CustomerName, COUNT(DISTINCT o.OrderID) AS TotalOrders, COUNT(p.PaymentID) AS TotalPayments
FROM Customers c
LEFT JOIN Orders o ON c.CustomerID = o.CustomerID
LEFT JOIN Payments p ON o.OrderID = p.OrderID
GROUP BY c.CustomerID, c.CustomerName;

```

</blockquote>

</details>

---

23. Consider You have two tables, "Students" and "Courses". The "Students" table contains student information, and the "Courses" table contains course information. There is a many-to-many relationship between students and courses through a junction table called "Enrollments". Write a query to retrieve the names of students along with the course names they are enrolled in.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

```sql

SELECT s.StudentName, c.CourseName
FROM Students s
INNER JOIN Enrollments e ON s.StudentID = e.StudentID
INNER JOIN Courses c ON e.CourseID = c.CourseID

```


</blockquote>

</details>

---


24. Write a query to retrieve the total count of customers for each country in the Customers table.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

```sql

SELECT Country, COUNT(*) AS TotalCustomers
FROM Customers
GROUP BY Country

```

</blockquote>

</details>

---

25. Consider you have three tables: "Employees", "Departments", and "Projects". The "Employees" table contains employee information, the "Departments" table contains department information, and the "Projects" table contains project information. Each employee is assigned to a department, and each department is associated with multiple projects. Write a query to retrieve the names of employees along with their department name and project name(s) they are assigned to.

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

```sql

SELECT e.EmployeeName, d.DepartmentName, p.ProjectName
FROM Employees e
INNER JOIN Departments d ON e.DepartmentID = d.DepartmentID
LEFT JOIN Projects p ON d.DepartmentID = p.DepartmentID


```

</blockquote>

</details>

---

26. How do you get the second highest salary from the database?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>MySQL</b></summary>

<blockquote>

```sql
SELECT MAX(salary) AS second_highest_salary
FROM employees
WHERE salary < (
    SELECT MAX(salary)
    FROM employees
);
```

Explanation: In MySQL, we can find the second highest salary by using a subquery. The subquery `(SELECT MAX(salary) FROM employees)` retrieves the maximum salary from the `employees` table. The outer query then selects the maximum salary from the `employees` table that is less than the maximum salary, effectively giving us the second highest salary.

</blockquote>

</details>

<details><summary><b>PostgreSQL</b></summary>

<blockquote>

```sql
SELECT salary AS second_highest_salary
FROM employees
ORDER BY salary DESC
OFFSET 1 LIMIT 1;
```

Explanation: In PostgreSQL, we can find the second highest salary by ordering the salaries in descending order using `ORDER BY salary DESC`. Then, we use `OFFSET 1` to skip the first row (which has the highest salary), and `LIMIT 1` to retrieve the next row, which corresponds to the second highest salary.

</blockquote>
</details>

---

27. How do you create a number list that contains only unique values while preserving the order of the numbers from another number list. 

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>MySQL</b></summary>

<blockquote>

```sql
SELECT DISTINCT number
FROM your_table
ORDER BY (SELECT NULL);
```

Explanation: In MySQL, to create a number list with unique values while preserving the order, we can use the `DISTINCT` keyword to eliminate duplicates from the `number` column. By including `ORDER BY (SELECT NULL)`, we ensure that the result set is ordered in the same order as the original data without changing the order.

</blockquote>
</details>

<details><summary><b>PostgreSQL</b></summary>

<blockquote>

```sql
SELECT number
FROM your_table
GROUP BY number
ORDER BY MIN(ctid);
```

Explanation: In PostgreSQL, we can achieve the same result by using the `GROUP BY` clause on the `number` column. The `GROUP BY` clause groups the rows with the same `number` value, effectively removing duplicates. By including `ORDER BY MIN(ctid)`, we ensure that the result set is ordered in the same order as the original data without changing the order.

</blockquote>
</details>

---

28. How to remove duplicates from a list while preserving the order of unique values in SQL

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>MySQL</b></summary>

<blockquote>

```sql
SELECT DISTINCT column_name
FROM your_table;
```

Explanation: In MySQL, we can remove duplicates from a list while preserving the order by using the `DISTINCT` keyword. The `DISTINCT` keyword eliminates duplicate values from the `column_name` column, giving us a result set with unique values in the original order.

</blockquote>

</details>

<details><summary><b>PostgreSQL</b></summary>

<blockquote>

```sql
SELECT column_name
FROM your_table
GROUP BY column_name
ORDER BY MIN(ctid);
```

Explanation: In PostgreSQL, we can achieve the same result by using the `GROUP BY` clause on the `column_name` column. The `GROUP BY` clause groups the rows with the same `column_name` value, effectively removing duplicates. By including `ORDER BY MIN(ctid)`, we ensure that the result set is ordered in the same order as the original data without changing the order.

</blockquote>

</details>


---

29. How do you remove duplicate values from a table without using a separate table ?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> MySQL</b></summary>

<blockquote>

To remove duplicate values from a table without using a separate table, you can use the `DELETE` statement with a self-join. Here's an example:

```sql
DELETE t1
FROM your_table t1
JOIN your_table t2 ON t1.column1 = t2.column1
                  AND t1.column2 = t2.column2
                  AND t1.id > t2.id;
```

This query deletes rows from `your_table` where there are duplicates based on the columns `column1` and `column2`. It compares each row with all other rows in the table and keeps only the row with the lowest `id` value.

Note: Replace `your_table` with the actual name of your table, and adjust the column names as per your table structure.

</blockquote>

</details>

<details><summary><b> PostgreSQL</b></summary>

<blockquote>

To remove duplicate values from a table without using a separate table in PostgreSQL, you can use the `DELETE` statement with a self-join, similar to MySQL. Here's an example:

```sql
DELETE FROM your_table
WHERE (column1, column2, id) IN (
    SELECT t1.column1, t1.column2, t1.id
    FROM your_table t1
    JOIN your_table t2 ON t1.column1 = t2.column1
                      AND t1.column2 = t2.column2
                      AND t1.id > t2.id
);
```

This query deletes rows from `your_table` where there are duplicates based on the columns `column1` and `column2`. It compares each row with all other rows in the table and keeps only the row with the lowest `id` value.

Note: Replace `your_table` with the actual name of your table, and adjust the column names as per your table structure.

</blockquote>

</details>

---



30. How do you retrieve all the data from a  table in SQL? 

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary><b>MySQL</b></summary>

<blockquote>

```sql
SELECT * FROM table_name;
```

Explanation:
- Replace `table_name` with the actual name of the table you want to select from.
- The `*` symbol is a wildcard that represents all columns in the table.
- This query will return all rows and columns from the specified table.

</blockquote>

</details>

<details><summary><b>PostgreSQL</b></summary>

<blockquote>

```sql
SELECT * FROM table_name;
```

Explanation:
- Replace `table_name` with the actual name of the table you want to select from.
- The `*` symbol is a wildcard that represents all columns in the table.
- This query will return all rows and columns from the specified table.

</blockquote>

</details>

---

31. Write a query to join the tables employees and employee salaries to return the 3rd highest employee salary.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary><b>MySQL</b></summary>

<blockquote>

```sql
SELECT salary
FROM employee_salaries
WHERE salary IN (
    SELECT DISTINCT salary
    FROM employee_salaries
    ORDER BY salary DESC
    LIMIT 2, 1
)
```

Explanation:
1. The subquery `(SELECT DISTINCT salary FROM employee_salaries ORDER BY salary DESC LIMIT 2, 1)` retrieves the 3rd highest salary from the "employee_salaries" table.
   - `ORDER BY salary DESC` sorts the salaries in descending order.
   - `LIMIT 2, 1` skips the first two highest salaries and retrieves the third highest salary.
2. The outer query selects the employees' salary from the "employee_salaries" table that matches the 3rd highest salary obtained from the subquery.



</blockquote>

</details>


<details><summary><b>PostgreSQL</b></summary>

<blockquote>

```sql
SELECT salary
FROM employee_salaries
WHERE salary IN (
    SELECT DISTINCT salary
    FROM employee_salaries
    ORDER BY salary DESC
    OFFSET 2
    LIMIT 1
)
```

Explanation:
1. The subquery `(SELECT DISTINCT salary FROM employee_salaries ORDER BY salary DESC OFFSET 2 LIMIT 1)` retrieves the 3rd highest salary from the "employee_salaries" table.
   - `ORDER BY salary DESC` sorts the salaries in descending order.
   - `OFFSET 2` skips the first two highest salaries.
   - `LIMIT 1` retrieves only one salary, which will be the 3rd highest.
2. The outer query selects the employees' salary from the "employee_salaries" table that matches the 3rd highest salary obtained from the subquery.



</blockquote>

</details>

---

32. Write a query to find the duplicate records from a table.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary><b>MySQL</b></summary>

<blockquote>

```sql
SELECT column1, column2, ..., columnN, COUNT(*)
FROM your_table
GROUP BY column1, column2, ..., columnN
HAVING COUNT(*) > 1;
```

Explanation:
1. Replace `your_table` with the actual name of your table.
2. Specify the columns (`column1, column2, ..., columnN`) based on which you want to identify duplicate records. These columns should uniquely identify each record.
3. The `GROUP BY` clause groups the rows based on the specified columns.
4. The `HAVING` clause filters the grouped rows and only returns the groups that have a count greater than 1, i.e., the duplicate records.

</blockquote>

</details>

<details><summary><b>PostgreSQL</b></summary>

<blockquote>

```sql
SELECT column1, column2, ..., columnN, COUNT(*)
FROM your_table
GROUP BY column1, column2, ..., columnN
HAVING COUNT(*) > 1;
```

Explanation:
1. Replace `your_table` with the actual name of your table.
2. Specify the columns (`column1, column2, ..., columnN`) based on which you want to identify duplicate records. These columns should uniquely identify each record.
3. The `GROUP BY` clause groups the rows based on the specified columns.
4. The `HAVING` clause filters the grouped rows and only returns the groups that have a count greater than 1, i.e., the duplicate records.

</blockquote>

</details>

---

33. How do you select unique rows from a table in sql ?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>MySQL</b></summary>

<blockquote>

```sql
SELECT DISTINCT * FROM your_table;
```

Explanation:
- Replace `your_table` with the actual name of your table.
- The `DISTINCT` keyword ensures that only unique rows are returned from the query.
- `*` represents all columns in the table, so this query will select all unique rows with all columns from the table.

</blockquote>

</details>

<details><summary><b>PostgreSQL</b></summary>

```sql
SELECT DISTINCT * FROM your_table;
```

Explanation:
- Replace `your_table` with the actual name of your table.
- The `DISTINCT` keyword ensures that only unique rows are returned from the query.
- `*` represents all columns in the table, so this query will select all unique rows with all columns from the table.

</details>

---

34. How do you obtain unique values in SQL without using the DISTINCT keyword?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary><b>MySQL</b></summary>

<blockquote>

```sql
SELECT column_name
FROM your_table
GROUP BY column_name;
```

Explanation:
This query selects the `column_name` from the `your_table` and groups the rows based on the values in that column using `GROUP BY`. As a result, it returns one row for each distinct value in the `column_name` column, effectively achieving the same result as `DISTINCT`.

</blockquote>

</details>

<details><summary><b>PostgreSQL</b></summary>

<blockquote>

```sql
SELECT column_name
FROM your_table
GROUP BY column_name;
```

Explanation:
The query is the same as the MySQL version. It selects the `column_name` from the `your_table` and groups the rows based on the values in that column using `GROUP BY`. This groups the rows and returns one row for each distinct value in the `column_name` column, achieving the same result as `DISTINCT`.

</blockquote>

</details>

---

35. write a query to find the most recent purchase from each customer.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary><b>MySQL</b></summary>

<blockquote>

```sql
SELECT c.customer_id, MAX(s.purchase_date) AS most_recent_purchase
FROM customers c
INNER JOIN sales s ON c.customer_id = s.customer_id
GROUP BY c.customer_id;
```

Explanation: 
This query combines the `customers` and `sales` tables using an inner join on the `customer_id` column. It then uses the `GROUP BY` clause to group the rows by the `customer_id`. The `MAX()` function is applied to the `purchase_date` column to find the most recent purchase for each customer. The result includes the `customer_id` and the corresponding `most_recent_purchase` date for each customer.

</blockquote>

</details>

<details><summary><b>PostgreSQL</b></summary>

<blockquote>

```sql
SELECT c.customer_id, MAX(s.purchase_date) AS most_recent_purchase
FROM customers c
INNER JOIN sales s ON c.customer_id = s.customer_id
GROUP BY c.customer_id;
```

Explanation:
This query is similar to the MySQL query. It combines the `customers` and `sales` tables using an inner join on the `customer_id` column. The `GROUP BY` clause is used to group the rows by the `customer_id`. The `MAX()` function is applied to the `purchase_date` column to find the most recent purchase for each customer. The result includes the `customer_id` and the corresponding `most_recent_purchase` date for each customer.

</blockquote>

</details>

---

36. Consider if table T1 has 1 Column named "ID" and 2 Rows: (1;1) and table T2 has 1 Column named "ID" and 2 Rows: (1;1), how many rows would `SELECT T1.ID, T2.ID FROM T1 INNER JOIN T2 ON T1.ID = T2.ID` return?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

The query `SELECT T1.ID, T2.ID FROM T1 INNER JOIN T2 ON T1.ID = T2.ID` would return 4 rows.

Explanation:
The query performs an inner join on the `ID` column between table T1 and table T2. Since both tables have 2 rows each with the same value for `ID`, the join condition is satisfied for every combination of rows where `T1.ID` matches `T2.ID`. As a result, each row from T1 is matched with both rows from T2, resulting in a Cartesian product. Therefore, the query would return 4 rows in total.

</details>

---

37. Consider if im having a table containing 10 rows with 2 duplicates, how can I identify and retrieve the duplicate rows?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>MySQL</b></summary>

<blockquote>

```sql
SELECT col1, col2, COUNT(*) as cnt
FROM your_table
GROUP BY col1, col2
HAVING cnt > 1;
```

Explanation:
This query selects `col1` and `col2` columns from `your_table`, groups the rows by the values in these columns using `GROUP BY`, and counts the number of rows in each group using `COUNT(*)`. Then, it filters the results to show only the groups with more than one row using `HAVING cnt > 1`. These are the rows that are duplicates.

</blockquote>

</details>

<details><summary><b>PostgreSQL</b></summary>

<blockquote>

```sql
SELECT col1, col2, COUNT(*) as cnt
FROM your_table
GROUP BY col1, col2
HAVING COUNT(*) > 1;
```

Explanation:
This query is the same as the MySQL version. It selects `col1` and `col2` columns from `your_table`, groups the rows by the values in these columns using `GROUP BY`, and counts the number of rows in each group using `COUNT(*)`. Then, it filters the results to show only the groups with more than one row using `HAVING COUNT(*) > 1`. These are the rows that are duplicates.

</blockquote>

</details>

---


38. What is a Subquery?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

<blockquote>

 A subquery is a SQL query that is nested inside another query. It is also known as an inner query or nested query. A subquery is used to retrieve data that will be used by the main query to filter, group, or order the results.

For example, consider the following SQL query:

```sql
SELECT *
FROM customers
WHERE country IN (
    SELECT country
    FROM orders
    WHERE order_date >= '2022-01-01'
)
```

In this query, the subquery `(SELECT country FROM orders WHERE order_date >= '2022-01-01')` retrieves a list of countries that have orders placed after January 1st, 2022. This list is then used by the main query to filter the `customers` table to show only the customers from those countries.

</details>

---

39. How to avoid duplicates in a query?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

<blockquote>

- `DISTINCT`: This keyword is used to remove duplicate rows from the query result set. It is placed after the `SELECT` keyword and before the columns you want to retrieve.

For example:
```sql
SELECT DISTINCT column1, column2, column3
FROM my_table;
```

- `GROUP BY`: This clause is used to group rows with similar values in a column or set of columns. It is placed after the `SELECT` clause and before the `ORDER BY` or `HAVING` clause.

For example:
```sql
SELECT column1, column2, COUNT(*)
FROM my_table
GROUP BY column1, column2;
```

In this example, the `GROUP BY` clause groups rows by the values in `column1` and `column2`, and the `COUNT(*)` function returns the number of rows in each group. This will avoid duplicate rows in the result set.

</blockquote>

</details>

---

40. How do you  create a new Table from another Table, where just the structure of the table is copied but none of the rows are copied? 

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary><b>MySQL</b></summary>

```sql
CREATE TABLE new_table
SELECT *
FROM original_table
WHERE 1 = 0;
```

Explanation:
This MySQL query creates a new table called `new_table` by selecting all columns from the `original_table` using the `SELECT` statement. However, the `WHERE 1 = 0` condition is always false, which means no rows will be selected. As a result, the new table `new_table` will have the same structure as `original_table`, but without any rows.

</details>

<details><summary><b>PostgreSQL</b></summary>

```sql
CREATE TABLE new_table AS
SELECT *
FROM original_table
WHERE false;
```

Explanation:
This PostgreSQL query creates a new table called `new_table` using the `CREATE TABLE AS SELECT` syntax. The `SELECT` statement selects all columns from the `original_table`. The `WHERE false` condition is always false, which means no rows will be selected. As a result, the new table `new_table` will have the same structure as `original_table`, but without any rows.

</details>

---


41. Write a query to Count the number of 's' characters in the string "Infosys" using SQL

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>MySQL</b></summary>

```sql
SELECT 
    LENGTH('Infosys') - LENGTH(REPLACE('Infosys', 's', '')) AS count_of_s
FROM 
    your_table;
```

Explanation:
This MySQL query calculates the count of 's' characters in the string 'Infosys' by subtracting the length of the string after removing all occurrences of 's' (using the `REPLACE()` function) from the original length of the string (using the `LENGTH()` function). The result is returned as `count_of_s`.

</details>

<details><summary><b>PostgreSQL</b></summary>

```sql
SELECT 
    LENGTH('Infosys') - LENGTH(REPLACE('Infosys', 's', '', 'g')) AS count_of_s
FROM 
    your_table;
```

Explanation:
This PostgreSQL query is similar to the MySQL version. It calculates the count of 's' characters in the string 'Infosys' by subtracting the length of the string after removing all occurrences of 's' (using the `REPLACE()` function with the `'g'` flag to replace globally) from the original length of the string (using the `LENGTH()` function). The result is returned as `count_of_s`.

</details>

---

42. How do you find duplicate records in a table?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary><b>MySQL</b></summary>

```sql
SELECT column1, column2, COUNT(*) AS count
FROM your_table
GROUP BY column1, column2
HAVING count > 1;
```

Explanation:
This MySQL query selects `column1` and `column2` from the `your_table` and groups the rows by the values in these columns using `GROUP BY`. The `COUNT(*)` function is used to count the number of rows in each group. The `HAVING` clause filters the groups and returns only those groups that have a count greater than 1, indicating duplicate records.

</details>

<details><summary><b>PostgreSQL</b></summary>

```sql
SELECT column1, column2, COUNT(*) AS count
FROM your_table
GROUP BY column1, column2
HAVING COUNT(*) > 1;
```

Explanation:
This PostgreSQL query is similar to the MySQL version. It selects `column1` and `column2` from the `your_table` and groups the rows by the values in these columns using `GROUP BY`. The `COUNT(*)` function is used to count the number of rows in each group. The `HAVING` clause filters the groups and returns only those groups that have a count greater than 1, indicating duplicate records.

</details>

---

43. Write a query using the `LIKE` keyword?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>MySQL</b></summary>

```sql
SELECT column1, column2
FROM your_table
WHERE column1 LIKE 'abc%';
```

Explanation:
In this MySQL query, the `LIKE` keyword is used to filter rows where the value of `column1` starts with the pattern 'abc'. The `%` is a wildcard character that matches any sequence of characters. So, the condition `column1 LIKE 'abc%'` will return rows where `column1` starts with 'abc' followed by any characters.

</details>

<details><summary><b>PostgreSQL</b></summary>

```sql
SELECT column1, column2
FROM your_table
WHERE column1 LIKE 'abc%';
```

Explanation:
This PostgreSQL query is the same as the MySQL version. It uses the `LIKE` keyword to filter rows where the value of `column1` starts with the pattern 'abc'. The `%` is a wildcard character that matches any sequence of characters. So, the condition `column1 LIKE 'abc%'` will return rows where `column1` starts with 'abc' followed by any characters.

</details>

---

44. How can you retrieve data from both employee tables in SQL and combine the results into a single result set?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>MySQL</b></summary>

```sql
SELECT * FROM employee_table1
UNION
SELECT * FROM employee_table2;
```

Explanation:
This MySQL query selects all columns from `employee_table1` and combines it with all columns from `employee_table2` using the `UNION` operator. The `UNION` operator removes duplicate rows from the final result set.

</details>

<details><summary><b>PostgreSQL</b></summary>

```sql
SELECT * FROM employee_table1
UNION
SELECT * FROM employee_table2;
```

Explanation:
This PostgreSQL query is similar to the MySQL version. It selects all columns from `employee_table1` and combines it with all columns from `employee_table2` using the `UNION` operator. The `UNION` operator removes duplicate rows from the final result set.

</details>

---

45. If you had 2 tables, how would you query all the records unique in the first table all the records that are unique in the second table and then all the records that they have in common.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>MySQL</b></summary>

```sql
SELECT * FROM table1
WHERE table1_id NOT IN (SELECT table1_id FROM table2)
UNION
SELECT * FROM table2
WHERE table2_id NOT IN (SELECT table2_id FROM table1)
UNION
SELECT * FROM table1
WHERE table1_id IN (SELECT table1_id FROM table2);
```

Explanation:
This MySQL query selects all records from `table1` where the `table1_id` is not present in `table2` (representing the unique records in the first table), then combines it with all records from `table2` where the `table2_id` is not present in `table1` (representing the unique records in the second table), and finally combines it with all records from `table1` where the `table1_id` is present in `table2` (representing the records they have in common).

</details>

<details><summary><b>PostgreSQL</b></summary>

```sql
SELECT * FROM table1
EXCEPT
SELECT * FROM table1
INTERSECT
SELECT * FROM table2;
```

Explanation:
This PostgreSQL query is a more concise version. It uses the `EXCEPT` operator to select all records from `table1` that are not present in `table2` (representing the unique records in the first table), and then uses the `INTERSECT` operator to select the records that are common to both `table1` and `table2`. The result is the combination of the unique records in `table1`, unique records in `table2`, and the common records between them.

</details>

---

46. Given 4 tables: Members, Checking Accounts (3 types), Savings Account (3 types), Loans(3 types) write a SQL query to find the most popular products along with the number of members who are attached to each product type. 

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

```sql
SELECT 
    CASE
        WHEN ca.account_type IS NOT NULL THEN 'Checking Account'
        WHEN sa.account_type IS NOT NULL THEN 'Savings Account'
        WHEN l.loan_type IS NOT NULL THEN 'Loan'
    END AS product_type,
    COUNT(DISTINCT m.member_id) AS member_count
FROM
    Members m
LEFT JOIN
    Checking_Accounts ca ON m.member_id = ca.member_id
LEFT JOIN
    Savings_Accounts sa ON m.member_id = sa.member_id
LEFT JOIN
    Loans l ON m.member_id = l.member_id
GROUP BY
    product_type
ORDER BY
    member_count DESC;
```

Explanation:
This query uses left joins to combine the `Members` table with the `Checking_Accounts`, `Savings_Accounts`, and `Loans` tables based on the common `member_id` column. It assigns the product type based on which table the join is successful. The `COUNT(DISTINCT m.member_id)` function is used to count the number of distinct members for each product type. The result is grouped by the product type and ordered by the member count in descending order.

</details>


---

47. How do you insert a data into a table Person.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

To insert data into the `Person` table, you need to provide the specific columns and their corresponding values that you want to insert. The exact column names will depend on the schema and structure of your `Person` table. Here's an example of how an `INSERT` statement can be written:

```sql
INSERT INTO Person (first_name, last_name, age)
VALUES ('John', 'Doe', 25);
```

Explanation:
In this  query, the `INSERT INTO` statement is used to specify the target table, which is `Person`. The column names (`first_name`, `last_name`, `age`) are specified within parentheses after the table name. The `VALUES` keyword is used to provide the corresponding values that you want to insert for each column. In this example, we are inserting the values 'John' for `first_name`, 'Doe' for `last_name`, and 25 for `age`.

Please note that you need to adjust the column names and values based on your specific `Person` table structure. Additionally, if the table has any columns with constraints or auto-generated values, you may need to provide appropriate values or handle those constraints accordingly during the insertion.

</details>

---

48. Write a query to find the most recently updated fields in a table.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

To find the most recently updated fields in a table, you can utilize the timestamp or date columns in your table that track the last update time. Here's an example of how you can write an SQL query to accomplish this:

```sql
SELECT *
FROM your_table
ORDER BY updated_at DESC
LIMIT 1;
```

Explanation:
In this query, `your_table` represents the name of your table. Assuming you have a column named `updated_at` that stores the timestamp or date of the last update, the query selects all columns from the table and orders the result set by the `updated_at` column in descending order. By using the `LIMIT 1` clause, only the most recently updated row is returned.

</details>

---

49. Consider you have a table named Customer with 3 columns - customer_id, name, and country. How do you get all names from the table?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary><b>Show Answer</b></summary>

To get all the names from the "Customer" table with the columns "customer_id", "name", and "country", you can use a simple SELECT statement. Here's an example:

```sql
SELECT name
FROM Customer;
```

Explanation:
This MySQL query selects the "name" column from the "Customer" table. It retrieves all the names stored in the table.

</details>

---

50. Consider you have a table named Customer with 3 columns - customer_id, name, and country. How do you Get all names in acsending order?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

To get all the names from the "Customer" table in ascending order, you can modify the SQL query with an ORDER BY clause. Here's an example:

```sql
SELECT name
FROM Customer
ORDER BY name ASC;
```

Explanation:
This query selects the "name" column from the "Customer" table and uses the ORDER BY clause to sort the result in ascending order based on the "name" column.

</details>


---

51. Consider you have a table named Customer with 3 columns - customer_id, name, and country. How do you get the number of countries from each table?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

To get the number of unique countries from the "Customer" table, you can use the COUNT and DISTINCT functions in SQL. Here's an example query:

```sql
SELECT COUNT(DISTINCT country) AS country_count
FROM Customer;
```

Explanation:
In this query, the `COUNT` function is used to count the number of distinct countries in the "Customer" table. The `DISTINCT` keyword ensures that only unique countries are considered. The result is displayed as "country_count".

</details>

---

52.  How do you update a record in SQL?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

```sql
UPDATE table_name
SET column1 = new_value1, column2 = new_value2, ...
WHERE condition;
```

Explanation:
In this example, `table_name` should be replaced with the actual name of the table you want to update. You need to specify the columns you want to update (`column1`, `column2`, ...) and their corresponding new values (`new_value1`, `new_value2`, ...). If you want to update specific records, you can provide a `WHERE` clause with a condition that identifies the target records. This condition can be based on one or more columns in the table.

</details>

---

53.  How would you do a SQL call for employees with a salary over 150K

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary><b>Show Answer</b></summary>

To retrieve employees with a salary over $150,000 from a table, you can use the SELECT statement along with a WHERE clause to filter the results based on the salary condition. Here's an example of how you can write the SQL query:

```sql
SELECT *
FROM employees
WHERE salary > 150000;
```

Explanation:
In this query, `employees` represents the name of the table that stores employee data. The query selects all columns (`*`) from the table and uses the WHERE clause to filter the results based on the condition `salary > 150000`. This condition retrieves only the employees whose salary is greater than $150,000.

</details>

---

54.  How do you select only the uncommon rows in two single column tables where the first x rows have the same value (ie 2 tables: 1 is 20 rows, 1 is 15 rows, each have the same values in the first 15 rows. How do you retrieve the other 5 rows)? Is there another way that isn't the MINUS function?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

To select only the uncommon rows between two single-column tables, where the first x rows have the same values, you can use various techniques such as the EXCEPT/NOT IN operator or a combination of LEFT JOIN and NULL check. Here's an example using the LEFT JOIN technique:

```sql
SELECT t1.column_name
FROM table1 t1
LEFT JOIN table2 t2 ON t1.column_name = t2.column_name
WHERE t2.column_name IS NULL;
```

Explanation:
In this MySQL query, `table1` and `table2` represent the names of the two single-column tables you want to compare. `column_name` should be replaced with the actual column name in your tables. The LEFT JOIN combines the two tables based on the common column values. The WHERE clause filters the result to include only those rows where the value in `column_name` from `table2` is NULL, indicating that the row is not present in `table2`.

</details>

---

55.  Write a query to select all people living in a specific city from the tables you created.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

- `Persons` table with columns: `person_id`, `name`
- `Addresses` table with columns: `address_id`, `person_id`, `city`

Here's an example query to select all people living in a specific city:

```sql
SELECT p.name
FROM Persons p
JOIN Addresses a ON p.person_id = a.person_id
WHERE a.city = 'specific_city';
```

Explanation:
In this MySQL query, we join the `Persons` and `Addresses` tables using the `person_id` column. We select the `name` column from the `Persons` table. The `JOIN` operation combines the matching rows between the two tables. The `WHERE` clause is used to filter the results based on the specified city, which should be replaced with the actual name of the specific city you want to query.

</details>

---

56. What are ways to speed up a specific query in SQL?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary><b>Show Answer</b></summary>


There are several ways to speed up a specific query in SQL:

1. Optimize the query: Review the query and optimize it to use the most efficient methods to retrieve the data. This may include optimizing the SELECT statement, using appropriate indexes, and reducing the number of joins.

2. Use indexes: Indexes can speed up queries by allowing the database to quickly find the data it needs. Make sure the columns being queried are properly indexed.

3. Cache data: Caching data can speed up queries that are frequently run. This involves storing frequently accessed data in memory, which reduces the number of times the database needs to access the disk.

4. Partition tables: If a table is very large, partitioning it into smaller tables can speed up queries that only need to access a subset of the data.

5. Upgrade hardware: If the database server is underpowered, upgrading the hardware can improve performance.

6. Use a query profiler: A query profiler can help identify which parts of a query are taking the most time, allowing you to focus on optimizing those parts.

7. Use stored procedures: Using stored procedures can speed up queries by reducing network traffic and optimizing the way data is retrieved from the database.

</details>

---

57.  How to manage a limitation in a program that only manages 100 objects whilst having a 1000 in my database.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary><b>Show Answer</b></summary>

To manage the limitation in your program where it can only handle 100 objects while you have 1000 objects in your database, you can implement pagination or limit the result set using SQL queries. Here are two approaches you can consider:

1. **Pagination**: Implement pagination in your program to retrieve data in smaller chunks or pages. This allows you to fetch a limited number of objects at a time, based on the program's capacity. You can use the `LIMIT` and `OFFSET` clauses in your SQL queries to retrieve a specific number of records per page and navigate through the result set. By fetching data in smaller portions, you can work within the limitations of your program.

   For example, if your program can handle 100 objects at a time, you can retrieve the first 100 objects using a query like this:

   ```sql
   SELECT * FROM your_table LIMIT 100;
   ```

   Then, when the user requests more data or navigates to the next page, you can retrieve the next 100 objects using an offset:

   ```sql
   SELECT * FROM your_table LIMIT 100 OFFSET 100;
   ```

   By incrementing the `OFFSET` value with each subsequent page, you can retrieve the data in manageable chunks.

2. **Limiting the result set**: Alternatively, you can limit the result set directly in your SQL queries to retrieve only a specific number of objects. This ensures that your program receives a limited number of records that it can handle.

   For example, if you want to retrieve only 100 objects from your database, you can modify your query like this:

   ```sql
   SELECT * FROM your_table LIMIT 100;
   ```

   This query will return only the first 100 objects from the table, respecting the limitation of your program.

By implementing pagination or limiting the result set, you can effectively manage the limitation in your program and work with a subset of objects from your database that fits within your program's capacity.

</details>

---

58. How to find common records in two tables ?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

To find common records in two tables, you can use the SQL JOIN operation to combine the tables based on a common column. Here's how you can approach it:

```sql
SELECT t1.column1, t1.column2, ...
FROM table1 t1
JOIN table2 t2 ON t1.common_column = t2.common_column;
```

Explanation:
In this query, `table1` and `table2` represent the names of the two tables you want to compare. You need to specify the columns you want to select from `table1` using `t1.column1`, `t1.column2`, and so on. Replace `common_column` with the actual column name that is common between the two tables.

The `JOIN` operation combines the rows from both tables based on matching values in the common column. This will return only the common records that exist in both tables.

</details>

---

59. How to find min and max in a salary column?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

To find the minimum and maximum values of a salary column in a table, you can use the SQL MIN() and MAX() aggregate functions. Here's how you can do it:

```sql
SELECT MIN(salary) AS min_salary, MAX(salary) AS max_salary
FROM your_table;
```

Explanation:
In this query, replace `your_table` with the actual name of the table you're working with. The MIN() function returns the minimum value of the salary column, and the MAX() function returns the maximum value. The AS keyword is used to assign aliases to the result columns, `min_salary` and `max_salary`, respectively.

</details>

---

60.  Consider if you have an id column like 1,2,3,4,5,... how would you return the records with odd ID's

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary><b>Show Answer</b></summary>

To return the records with odd IDs from a table with an ID column, you can use the modulo operator (%) in your SQL query. Here's how you can do it:

```sql
SELECT *
FROM your_table
WHERE id % 2 = 1;
```

Explanation:
In this MySQL query, replace `your_table` with the actual name of the table you're working with, and `id` with the actual name of the ID column. The condition `id % 2 = 1` checks if the ID value is odd. The modulo operator `%` returns the remainder when the ID is divided by 2. If the remainder is 1, it indicates an odd ID.

</details>

---

61.  How do you select top 10 employees with highest salary in table?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

To select the top 10 employees with the highest salary in a table, you can use the SQL query below:

```sql
SELECT *
FROM employees
ORDER BY salary DESC
LIMIT 10;
```

Explanation:
In this query, `employees` represents the name of the table containing employee records. The `ORDER BY` clause is used to sort the records based on the `salary` column in descending order. The `DESC` keyword specifies a descending sort. The `LIMIT` clause limits the result to 10 rows, giving you the top 10 employees with the highest salary.

This query will work for both MySQL and PostgreSQL databases as the syntax is the same.

</details>

---

62. How would you get the individual transactions and the total transaction amount over the course of a month for a customer from a Customers table and a Transactions table?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

To retrieve the individual transactions and the total transaction amount over the course of a month for a customer from a Customers table and a Transactions table, you can use the following SQL query:

```sql
SELECT t.transaction_id, t.transaction_date, t.amount, c.customer_name, SUM(t.amount) AS total_amount
FROM Customers c
JOIN Transactions t ON c.customer_id = t.customer_id
WHERE t.transaction_date >= '2023-05-01' AND t.transaction_date < '2023-06-01'
GROUP BY t.transaction_id, t.transaction_date, t.amount, c.customer_name;
```

Explanation:
In this query, `Customers` and `Transactions` represent the names of the Customers table and Transactions table, respectively. The `customer_id` is the common column that establishes the relationship between the two tables. Adjust the date range in the `WHERE` clause to match the desired month.

The query joins the Customers and Transactions tables based on the customer_id column. It selects the transaction ID, transaction date, transaction amount, and customer name. The `SUM()` function calculates the total transaction amount. The result is grouped by the individual transaction details.

This query can be used in both MySQL and PostgreSQL databases as the syntax is the same.

</details>

---

63. How do you delete duplicate Records in SQL?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>MySQL</b></summary>

```sql
DELETE FROM your_table
WHERE (column1, column2, ...) IN (
    SELECT column1, column2, ...
    FROM your_table
    GROUP BY column1, column2, ...
    HAVING COUNT(*) > 1
);
```

Explanation:
In this MySQL query, replace `your_table` with the actual name of the table you're working with, and `column1, column2, ...` with the column names that define the duplicates. The subquery selects the duplicate rows by grouping them based on the specified columns and then filters only those groups that have a count greater than 1, indicating duplicates. The `DELETE` statement deletes the rows that match the conditions specified in the subquery, effectively removing the duplicates from the table.

</details>

<details><summary><b>PostgreSQL</b></summary>

```sql
DELETE FROM your_table a
WHERE EXISTS (
    SELECT 1
    FROM your_table b
    WHERE a.column1 = b.column1
    AND a.column2 = b.column2
    ...
    AND a.ctid < b.ctid
);
```

Explanation:
This PostgreSQL query deletes the duplicate rows from the `your_table`. Replace `your_table` with the actual name of the table, and `column1, column2, ...` with the column names that define the duplicates. The subquery checks for the existence of rows with the same values in the specified columns, but with a lower `ctid` (the internal identifier of each row). This ensures that only duplicates are deleted, keeping one copy of each unique row.

</details>

---

64.  Consider you are given two tables "employee" and "sale_details", 
How do you fetch the details of the 
 -  employee who have sold nothing.  
 -  employee who is the top sales.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary><b>Show Answer</b></summary>

```sql
SELECT e.employee_id, e.employee_name
FROM employee e
LEFT JOIN sale_details sd ON e.employee_id = sd.employee_id
WHERE sd.employee_id IS NULL;
```

Explanation:
In this MySQL query, the `employee` table is joined with the `sale_details` table using a `LEFT JOIN` based on the `employee_id` column. The `LEFT JOIN` ensures that all employees from the `employee` table are included in the result, even if they have no corresponding rows in the `sale_details` table. The `WHERE` clause filters out the rows where `sale_details.employee_id` is `NULL`, indicating that the employee has sold nothing.

</details>


---

65.  Consider you are have table "Employee". How do you write a query to fetch the employees name and the department of the employees whose salary is over 30,000?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary><b>MySQL</b></summary>

```sql
SELECT e.employee_name
FROM employee e
JOIN department d ON e.department_id = d.department_id
WHERE e.salary > 30000 AND d.department_name = 'Engineering';
```

Explanation:
In this MySQL query, the "employee" table is joined with the "department" table using the common column "department_id". The `WHERE` clause filters the result to include only employees with a salary over 30,000 and who belong to the "Engineering" department.

</details>

<details><summary><b>PostgreSQL</b></summary>

```sql
SELECT e.employee_name
FROM employee e
JOIN department d ON e.department_id = d.department_id
WHERE e.salary > 30000 AND d.department_name = 'Engineering';
```

Explanation:
This PostgreSQL query is the same as the MySQL version. It joins the "employee" and "department" tables based on the "department_id" column and applies the same conditions in the `WHERE` clause to filter the result.

</details>
</details>

---

66. Write a sql query to update the table?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

SQL Query to Update a Table:

```sql
UPDATE your_table
SET column1 = 'new_value1', column2 = 'new_value2'
WHERE condition;
```

Explanation:
This MySQL query updates the specified columns (`column1`, `column2`, etc.) in the table `your_table` with the new values (`new_value1`, `new_value2`, etc.). The `WHERE` clause is optional and can be used to specify conditions to determine which rows should be updated. If no condition is provided, all rows in the table will be updated.

Please replace `your_table` with the actual name of your table, and modify the column names, new values, and conditions as per your requirements.

</details>

---
    
67.  write a SQL Join query to combine two employee tables where the salary is between 5000 and 8000
  
  ![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

  SQL Query to Join Two Employee Tables based on Salary Range:

```sql
SELECT *
FROM employee_table1
JOIN employee_table2 ON employee_table1.employee_id = employee_table2.employee_id
WHERE employee_table1.salary BETWEEN 5000 AND 8000;
```

Explanation:
This MySQL query performs an inner join between `employee_table1` and `employee_table2` based on the common column `employee_id`. The `WHERE` clause filters the result to include only those employees whose salary is between 5000 and 8000.

Please replace `employee_table1` and `employee_table2` with the actual names of your employee tables, and adjust the column names (`employee_id`, `salary`) as per your table structure.

</details>

---


68. How would you write a query to get employee's name from an employees table with an id of 123?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

To retrieve the employee's name from an employees table with an ID of 123, you can use the `SELECT` statement along with a `WHERE` clause. Here's the query:

```sql
SELECT name
FROM employees
WHERE id = 123;
```

Explanation:
- Replace `name` with the column name that stores the employee's name in your employees table.
- Replace `employees` with the name of your employees table.
- Replace `id` with the column name that represents the employee ID in your employees table.
- Replace `123` with the specific ID you want to retrieve the name for.

For example, if you have a table named `employees` with columns `id` and `name`, and you want to get the name of the employee with ID 123, the query would be:

```sql
SELECT name
FROM employees
WHERE id = 123;
```

This query will retrieve the name of the employee with ID 123 from the employees table.

Adjust the table name, column names, and ID value as per your specific table structure and requirements.

</details>

---

69.  How would you get the department of an employee from a given employee table ? 
    -Employee table columns: id, name, department_name
    -Department table columns: id, department_name"

    ![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

To retrieve the department of an employee based on the employee table and department table, you can use a simple `JOIN` between the two tables. Here's the query:

```sql
SELECT e.name, d.department_name
FROM employee e
JOIN department d ON e.department_name = d.department_name
WHERE e.id = 123;
```

Explanation:
- Replace `e.name` with the column name that stores the employee's name in the employee table.
- Replace `d.department_name` with the column name that stores the department names in the department table.
- Replace `employee` with the name of your employee table.
- Replace `department` with the name of your department table.
- Replace `e.department_name` and `d.department_name` with the respective column names in both tables that represent the department names.
- Replace `e.id = 123` with the condition that matches the desired employee ID.

For example, if you have an employee table with columns `id`, `name`, and `department_name`, and a department table with columns `id` and `department_name`, and you want to retrieve the department of an employee with ID 123, the query would be:

```sql
SELECT e.name, d.department_name
FROM employee e
JOIN department d ON e.department_name = d.department_name
WHERE e.id = 123;
```

This query will retrieve the name of the employee and the corresponding department based on the department name in both tables.

Adjust the table names, column names, and conditions as per your specific table structure and requirements.

</details>

---

70.  Explain left join?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

To perform a left join in SQL, you can use the `LEFT JOIN` keyword in your query. Here's the syntax:

```sql
SELECT columns
FROM table1
LEFT JOIN table2 ON join_condition;
```

Explanation:
- Replace `columns` with the columns you want to select from the tables.
- Replace `table1` and `table2` with the names of the tables you want to join.
- Replace `join_condition` with the condition that specifies how the tables should be joined.

For example, let's say you have two tables named `orders` and `customers`, and you want to retrieve all orders along with their corresponding customer information (if available) using a left join on the `customer_id` column. The query would be:

```sql
SELECT o.order_id, o.order_date, c.customer_name
FROM orders o
LEFT JOIN customers c ON o.customer_id = c.customer_id;
```

This query selects the `order_id` and `order_date` columns from the `orders` table and the `customer_name` column from the `customers` table. It performs a left join based on the matching `customer_id` column, retrieving all orders and including the customer name if a matching customer exists.

Adjust the table names, column names, and join conditions as per your specific table structure and requirements.

</details>

---


71. Condiser you are given a table Employee. How do you group employee according to their department and put the 1st/last name of the employees in that department in a single cell?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

To group employees by department and concatenate the first and last names of employees within each department into a single cell, you can use the `GROUP_CONCAT` function along with the `GROUP BY` clause. Here's an example query:

```sql
SELECT department, GROUP_CONCAT(CONCAT(first_name, ' ', last_name)) AS employees
FROM employees
GROUP BY department;
```

Explanation:
- The query selects the `department` column from the `employees` table.
- The `GROUP_CONCAT` function concatenates the `first_name` and `last_name` columns using the `CONCAT` function.
- The result of the concatenation is aliased as `employees`.
- The `GROUP BY` clause groups the rows by the `department` column.
- The query returns the department and the concatenated names of employees within each department in a single cell.

Adjust the table name, column names, and aliases as per your specific table structure and requirements.

</details>

---

72.  Consider you are given with two tables employees and employee salaries. 
How do you return the 3rd highest employee salary.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary><b>Show Answer</b></summary>

To return the 3rd highest employee salary from the `employees` and `employee_salaries` tables, you can use the `ORDER BY` and `LIMIT` clauses. Here's an example query:

```sql
SELECT salary
FROM employee_salaries
ORDER BY salary DESC
LIMIT 1 OFFSET 2;
```

Explanation:
- The query selects the `salary` column from the `employee_salaries` table.
- The `ORDER BY` clause sorts the salaries in descending order, placing the highest salary first.
- The `LIMIT` clause with `1` specifies that only one row should be returned.
- The `OFFSET 2` clause skips the first two rows, effectively returning the 3rd highest salary.

Please note that this query assumes that the `employee_salaries` table contains a column named `salary` that stores the salaries of the employees.

Adjust the table names, column names, and `LIMIT` and `OFFSET` values as per your specific table structure and requirements.

</details>

---

73.  How to find common records in two tables?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary><b>Show Answer</b></summary>

To find common records in two tables, you can use the `INNER JOIN` operation. Here's an example query:

```sql
SELECT t1.column1, t1.column2, ...
FROM table1 t1
INNER JOIN table2 t2 ON t1.common_column = t2.common_column;
```

Explanation:
- Replace `t1.column1, t1.column2, ...` with the actual columns you want to select from `table1`.
- Replace `table1` with the name of the first table.
- Replace `table2` with the name of the second table.
- Replace `t1.common_column` and `t2.common_column` with the common column on which you want to join the two tables.

The `INNER JOIN` operation returns only the rows that have matching values in both tables based on the specified common column. This effectively gives you the common records between the two tables.

Here's an example query that demonstrates finding common records between two tables based on a common column named `id`:

```sql
SELECT t1.id, t1.name, t2.address
FROM table1 t1
INNER JOIN table2 t2 ON t1.id = t2.id;
```

This query selects the `id`, `name`, and `address` columns from `table1` and `table2`, respectively, and returns only the rows where the `id` values match in both tables.

Adjust the column names, table names, and common column as per your specific scenario.

</details>

---


74.  Write a SQL query where we combine a customers table and sales table to find the most recent purchase from each customer?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)



<details><summary><b>MySQL</b></summary>

To find the most recent purchase from each customer by combining the `customers` table and the `sales` table, you can use a subquery and the `MAX` function. Here's an example query:

```sql
SELECT c.customer_id, c.customer_name, s.purchase_date, s.purchase_amount
FROM customers c
INNER JOIN sales s ON c.customer_id = s.customer_id
WHERE s.purchase_date = (
    SELECT MAX(purchase_date)
    FROM sales
    WHERE customer_id = c.customer_id
);
```

Explanation:
- The query uses an `INNER JOIN` to combine the `customers` and `sales` tables based on the `customer_id` column.
- The subquery `(SELECT MAX(purchase_date) FROM sales WHERE customer_id = c.customer_id)` is used to find the maximum (most recent) purchase date for each customer.
- The outer query selects the relevant columns (`customer_id`, `customer_name`, `purchase_date`, `purchase_amount`) from both tables.
- The `WHERE` clause filters the results to include only the rows where the purchase date matches the most recent purchase date for each customer.

</details>

<details><summary><b>PostgreSQL</b></summary>

In PostgreSQL, you can use the `DISTINCT ON` clause along with the `ORDER BY` clause to find the most recent purchase from each customer. Here's an example query:

```sql
SELECT DISTINCT ON (c.customer_id)
    c.customer_id, c.customer_name, s.purchase_date, s.purchase_amount
FROM customers c
INNER JOIN sales s ON c.customer_id = s.customer_id
ORDER BY c.customer_id, s.purchase_date DESC;
```

Explanation:
- The query uses an `INNER JOIN` to combine the `customers` and `sales` tables based on the `customer_id` column.
- The `DISTINCT ON (c.customer_id)` clause ensures that only the first row with a unique `customer_id` is returned for each customer.
- The `ORDER BY` clause orders the rows first by `customer_id` and then by `purchase_date` in descending order, so the most recent purchase for each customer appears first.
- The selected columns (`customer_id`, `customer_name`, `purchase_date`, `purchase_amount`) are returned in the result.

</details>
</details>

---

75.  Write a SQL query to filter results and search with conditions 
    
![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

Filtering results and searching with conditions in SQL can be achieved using the `WHERE` clause in combination with various operators and functions. Here's an example:

```sql
SELECT column1, column2, ...
FROM your_table
WHERE condition;
```

Explanation:
- Replace `column1, column2, ...` with the actual column names you want to select from the table.
- Replace `your_table` with the name of your table.
- Replace `condition` with the specific condition or set of conditions you want to apply to filter the results.

Examples of Conditions:
- Equality condition: `column = value`
- Inequality condition: `column <> value`
- Comparison operators: `<, >, <=, >=`
- Logical operators: `AND, OR, NOT`
- Pattern matching using `LIKE`: `column LIKE 'pattern'`
- Null check: `column IS NULL` or `column IS NOT NULL`
- Range condition: `column BETWEEN value1 AND value2`
- List of values: `column IN (value1, value2, ...)`

Here's an example query that demonstrates filtering results based on conditions:

```sql
SELECT employee_name, salary
FROM employees
WHERE department = 'Engineering' AND salary > 50000;
```

This query selects the `employee_name` and `salary` columns from the `employees` table, filtering the results to include only employees from the Engineering department with a salary greater than 50,000.

Please adjust the column names, table name, and conditions as per your specific requirements.

</details>

---

76.  how do you create a table and select specific records from that table created.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>MySQL</b></summary>
SQL Query to Create a Table and Select Specific Data:

To create a table, you can use the `CREATE TABLE` statement in MySQL. Here's an example:

```sql
CREATE TABLE your_table (
    column1 datatype1,
    column2 datatype2,
    ...
);

-- Example table creation
CREATE TABLE students (
    student_id INT PRIMARY KEY,
    student_name VARCHAR(50),
    age INT,
    address VARCHAR(100)
);

-- Select specific data from the created table
SELECT student_name, age
FROM students;
```

Explanation:
The first part of the query demonstrates how to create a table named `your_table` with the specified columns and data types. You can replace `your_table` with the desired table name and define the appropriate columns and data types according to your needs.

The second part shows an example of creating a `students` table with columns `student_id`, `student_name`, `age`, and `address`. The `PRIMARY KEY` constraint is used to define the primary key column.

After creating the table, you can use the `SELECT` statement to query and retrieve specific data from the table. In this example, the query selects the `student_name` and `age` columns from the `students` table.

Please modify the table name, column names, and data types to match your requirements.

</details>

<details><summary><b>PostgreSQL</b></summary>

To create a table and select specific data in PostgreSQL, you can use the `CREATE TABLE` statement followed by the `SELECT` statement. Here's an example:

```sql
CREATE TABLE your_table (
    column1 datatype1,
    column2 datatype2,
    ...
);

-- Example table creation
CREATE TABLE students (
    student_id SERIAL PRIMARY KEY,
    student_name VARCHAR(50),
    age INT,
    address VARCHAR(100)
);

-- Select specific data from the created table
SELECT student_name, age
FROM students;
```

Explanation:
The first part of the query demonstrates how to create a table named `your_table` with the specified columns and data types. Replace `your_table` with the desired table name and define the appropriate columns and data types based on your requirements.

The second part shows an example of creating a `students` table with columns `student_id`, `student_name`, `age`, and `address`. The `SERIAL` data type is used for the `student_id` column, which automatically generates a unique value for each new row. The `PRIMARY KEY` constraint is applied to the `student_id` column.

After creating the table, the `SELECT` statement is used to query and retrieve specific data from the `students` table. In this example, the query selects the `student_name` and `age` columns.

Please adjust the table name, column names, and data types as per your requirements.

</details>
</details>

---

77. table 1: student name, student id, address, age. 
table 2: student rank, score, student id.
write a query to fetch the data of the student whose rank is < 10 along with the student name, student age and score.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

SQL Query to Join Tables and Filter by Student Rank:

```sql
SELECT t1.student_name, t1.student_id, t1.address, t1.age, t2.student_rank, t2.score
FROM table1 t1
JOIN table2 t2 ON t1.student_id = t2.student_id
WHERE t2.student_rank < 10;
```

Explanation:
This MySQL query performs an inner join between `table1` and `table2` based on the common column `student_id`. It selects the columns `student_name`, `student_id`, `address`, `age`, `student_rank`, and `score` from both tables. The `WHERE` clause filters the result to include only those students whose `student_rank` is less than 10.

Please replace `table1` and `table2` with the actual names of your tables, and adjust the column names (`student_name`, `student_id`, `address`, `age`, `student_rank`, `score`) as per your table structure.

</details>

---



78. Write a query to find the Max and Min amount from a table.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

SQL Query to Find the Maximum and Minimum Amounts in a Column:


```sql
SELECT MAX(amount) AS max_amount, MIN(amount) AS min_amount FROM your_table;
```

Explanation:
This MySQL query uses the `MAX` and `MIN` aggregate functions to calculate the maximum and minimum values, respectively, in the specified column (`amount`). The `AS` keyword is used to provide aliases `max_amount` and `min_amount` for the resulting columns, representing the maximum and minimum amounts, respectively.

Please replace `your_table` with the actual name of your table.

</details>

---


79.  How do you get data from two separate tables using a single query?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary> <b> Show Answer</b> </summary>
<blockquote>

- To get data from two separate tables in a single query in *SQL and PostgreSQL*, you can use the JOIN clause.

- The JOIN clause allows you to combine rows from two or more tables based on a related column between them. There are several types of JOIN clauses, including *INNER JOIN, LEFT JOIN, RIGHT JOIN, and FULL OUTER JOIN*, each with its own specific behavior.

Here's an example of a basic INNER JOIN query:

```sql

SELECT *
FROM table1
INNER JOIN table2
ON table1.column = table2.column;
```

- In this query, table1 and table2 are the names of the two tables you want to join. column is the name of the related column between the two tables that you want to use to match up rows.

- Replace the * with the column names that you want to select from the combined table.

- For example, if you have two tables named customers and orders with a related column named customer_id, and you want to get a list of all customers and their corresponding orders, you would use the following query:

```sql

SELECT customers.customer_id, customers.first_name, customers.last_name, orders.order_id, orders.order_date
FROM customers
INNER JOIN orders
ON customers.customer_id = orders.customer_id;
```

This query will return the customer ID, first name, last name, order ID, and order date for all customers who have placed an order.

</blockquote>

</details>

---

80. How do you create a sub-query in SQL and PostgreSQL?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>SQL</b> </summary>

<blockquote>

- To create a subquery in SQL and PostgreSQL, you can use a query nested inside another query. The result of the inner query is used as input to the outer query.

- Here's the basic syntax for creating a subquery:

```sql

SELECT column1, column2, ...
FROM table1
WHERE columnN IN (SELECT columnN FROM table2 WHERE condition);

```

- In this example, the subquery is enclosed in parentheses and is executed first. The result of the subquery is then used in the outer query to filter the results.

</blockquote>

</details>

<details><summary> <b> PostgreSQL </b></summary>

<blockquote

- Here's an example of a subquery in SQL and PostgreSQL that selects the names of customers who have placed an order:

```sql

SELECT first_name, last_name
FROM customers
WHERE customer_id IN (
  SELECT customer_id
  FROM orders
);
```
- In this example, the inner query selects the customer_id from the orders table. The outer query then uses the customer_id to select the corresponding first_name and last_name from the customers table.

</blockquote>

</details>

---

81. How to get all contacts associated with an account where the account name contains the word 'public' assuming tables 'accounts' and 'contacts' with a corresponding column named 'account_id' in the 'contacts' table?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
<blockquote>

- Assuming we have a table named accounts and a table named contacts, and there is a column named account_id in the contacts table that corresponds to the id column in the accounts table, we can use the following query in SQL and PostgreSQL to retrieve all contacts associated with an account where the account name contains the word "public":

```sql

SELECT contacts.*
FROM contacts
INNER JOIN accounts
ON contacts.account_id = accounts.id
WHERE accounts.name LIKE '%public%';
```

- In this query, the INNER JOIN clause is used to combine the contacts and accounts tables based on their corresponding columns (contacts.account_id and accounts.id). The `WHERE` clause is used to filter the results to only include rows where the accounts.name column contains the word "public". The `SELECT` clause selects all columns from the contacts table for the resulting rows.

</blockquote>

</details>

---

82. Write an Sql query to retrieve the 3rd highest salaries of all 3 departments from a table with columns: department, employee, salary?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
<blockquote>

Here's a SQL query that retrieves the third highest salaries of each department from a table named employees with columns department, employee, and salary:

```sql

SELECT department, MAX(salary) AS third_highest_salary
FROM employees
WHERE salary < (
  SELECT MAX(salary)
  FROM employees
  WHERE salary < (
    SELECT MAX(salary) FROM employees
  )
)
GROUP BY department;
```

In this query, the subquery `(SELECT MAX(salary) FROM employees)` retrieves the highest salary in the entire table, and the subquery `(SELECT MAX(salary) FROM employees WHERE salary < (SELECT MAX(salary) FROM employees))` retrieves the second-highest salary in the entire table. The outer query then selects the third-highest salary in each department by selecting the maximum salary for each department that is less than the second-highest salary in the entire table.

</blockquote>

</details>

---

83. Explain the given query: "SELECT column a, column b FROM table T ORDER BY 2"

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)


<details><summary> <b>Show Answer</b> </summary>
<blockquote>


- The table name 'table' exists in your database.
- Column 'a' and 'b' exist in 'table'.
- Column '2' refers to the second column 'column b' in the select list.
- The query will select the values from 'column a' and 'column b' from the table 'table' and order the results by the second column in the select list, which is 'column b'. So, the output of the query will be a list of values from 'column a' and 'column b', ordered by the values in 'column b'.

</blockquote>

</details>

---

84. If there are two employee tables how do you return both tables?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b> SQL </b> </summary>

<blockquote>

- In both SQL and PostgreSQL, you can use the UNION operator to combine the results of two SELECT statements into a single result set. Here's an example of how to return both tables in SQL:

```SQL

SELECT * FROM table1
UNION
SELECT * FROM table2;
```
</details>

<details><summary> <b>PostgreSQL</b> </summary>

- And here's an example of how to do it in PostgreSQL:

```SQL

SELECT * FROM table1
UNION ALL
SELECT * FROM table2;
```

- Note that in PostgreSQL, you need to use the "ALL" keyword after UNION to include all rows from both tables, while in SQL, "ALL" is assumed by default.

</blockquote>

</details>

---

85. Write a query to select an employee from a table whose salary matches the rank?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
<blockquote>

- Assuming you have a table named employee with columns employee_id, employee_name, employee_salary and rank in both SQL and PostgreSQL, you can use the following SQL queries to select an employee from the table and match their salary to the rank:

```SQL

SELECT e.employee_id, e.employee_name, e.employee_salary, r.rank
FROM employee e
INNER JOIN rank r ON e.employee_salary = r.salary
WHERE e.employee_name = 'John Doe';

```

- In both XQL and PostgreSQL, we are joining the employee table with the rank table on the employee_salary column and selecting the columns employee_id, employee_name, employee_salary, and rank for the employee whose name is 'John Doe'.

</blockquote>

</details>

---

86. Imagine you have a table with the column (id,name and price). Write a query to get entity with the biggest price?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
<blockquote>

The query to get the entity with the biggest price in SQL and PostgreSQL is the same. Here's the query you can use:

```sql

SELECT * FROM table ORDER BY price DESC LIMIT 1;
```

This query selects all columns from the table, sorts the rows in descending order by price, and limits the result to just the first row, which will have the highest price.

Note that you'll need to replace "table" in the query with the actual name of your table.

</blockquote>

</details>

---


87. Write a query to get just a last name from the name field without using MINUS function? 

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary> <b> SQL </b> </summary>
<blockquote>

We can extract just the last name from the "name" field in SQL and PostgreSQL using string manipulation functions:

```sql

SELECT SUBSTRING(name, CHARINDEX(' ', name) + 1) AS last_name FROM table;
```

This query uses the CHARINDEX function to find the position of the first space character in the "name" field, and then uses the SUBSTRING function to extract the substring starting from the position of the space character + 1 (which is the first character of the last name).

</details>

<details><summary> <b> PostgreSQL </b> </summary>

```sql

SELECT SPLIT_PART(name, ' ', 2) AS last_name FROM table;
```
This query uses the SPLIT_PART function to split the "name" field into two parts based on the space separator, and then selects the second part (which is the last name).

</blockquote>

</details>

---

88. How do you delete a single record from a table?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
<blockquote>

To delete a single record in *SQL and PostgreSQL*, you can use the DELETE statement along with the WHERE clause to specify the record to be deleted. Here's an example query:

```sql

DELETE FROM table WHERE id = 123;
```
This query deletes the record from the "table" where the "id" column has a value of 123.

</blockquote>

</details>

---

89. How would you account having multiple shows of the same movie at the same time? 

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
<blockquote>

- If you have multiple showings of the same movie at the same time, you can account for it in your *SQL and PostgreSQL* database by adding a unique identifier for each showing. One way to do this is to create a composite primary key for the showings table that includes both the movie ID and the showing time.

- Here's an example schema for a showings table that accounts for multiple showings of the same movie at the same time:

```sql

CREATE TABLE showings (
    id INT NOT NULL PRIMARY KEY,
    movie_id INT NOT NULL,
    showing_time TIMESTAMP NOT NULL,
    theater_id INT NOT NULL
);
```

- In this example schema, the showings table has an additional "id" column that serves as a primary key to uniquely identify each showing, even if multiple showings have the same movie ID and showing time. The movie ID, showing time, and theater ID columns are included to specify which movie is being shown, when and where it's being shown.

- When inserting data into the showings table, you would need to ensure that each showing has a unique combination of movie ID, showing time, and theater ID, and that the "id" column is assigned a unique value for each new showing.

</blockquote>

</details>

---

90. Consider you are given with two tables "departments" and "expenses". Write a SQL query to find the sums of department spending?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
<blockquote>

- Assuming you have two tables, "departments" and "expenses", where "expenses" contains the individual expenses for each department, and "departments" contains information about each department, including the department ID, you can find the sums of department spending with the following SQL and PostgreSQL queries:

```SQL

SELECT departments.department_name, SUM(expenses.amount) as total_spending
FROM departments
INNER JOIN expenses ON departments.department_id = expenses.department_id
GROUP BY departments.department_name;

```

- In these queries, the INNER JOIN is used to join the "departments" and "expenses" tables based on the department ID. The SUM function is used to calculate the total amount spent by each department, and the GROUP BY clause is used to group the results by department name.

</blockquote>

</details>

---

91. Show us how you'd  CREATE TABLE statements to set up SQL tables to store the street addresses of multiple people (there can be multiple people at the same address). Write a query to select all people living in a specific city from the tables you created

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
<blockquote>

Here's an example of how to write CREATE TABLE statements to set up SQL tables to store the street addresses of multiple people. This query works for both *SQL and PostgreSQL*:

```sql

CREATE TABLE addresses (
    id INTEGER PRIMARY KEY,
    street VARCHAR(255) NOT NULL,
    city VARCHAR(255) NOT NULL,
    state VARCHAR(2) NOT NULL,
    zip_code VARCHAR(10) NOT NULL
);

CREATE TABLE people (
    id INTEGER PRIMARY KEY,
    name VARCHAR(255) NOT NULL,
    address_id INTEGER NOT NULL,
    FOREIGN KEY (address_id) REFERENCES addresses(id)
);
```

- In this example, the "addresses" table includes columns for the street, city, state, and ZIP code, while the "people" table includes a foreign key column referencing the "id" column of the "addresses" table to associate each person with a specific address.

- Here's an example query to select all people living in a specific city:

```sql

SELECT people.name, addresses.street, addresses.city, addresses.state, addresses.zip_code
FROM people
INNER JOIN addresses ON people.address_id = addresses.id
WHERE addresses.city = 'New York';
```

- This query uses an INNER JOIN to join the "people" and "addresses" tables based on the "address_id" foreign key column, and then uses a WHERE clause to filter the results to only include people living in the specified city (in this case, "New York"). The SELECT clause is used to select the relevant columns from both tables for display in the query result.

</blockquote>

</details>

---


92. If T1 has 1 Column named *ID* and 2 Rows: (1;1) and T2 has 1 Column named *ID* and 2 Rows: (1;1), How many rows would SELECT T1.ID, T2.ID FROM T1 INNER JOIN T2 ON T1.ID = T2.ID return?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
<blockquote>

The query SELECT T1.ID, T2.ID FROM T1 INNER JOIN T2 ON T1.ID = T2.ID would return 2 rows. This is because there is only one matching row in T1 and T2 with the same ID value of 1, so the inner join would only return that one row. The resulting table would have two columns, T1.ID and T2.ID, both containing the value 1.

</blockquote>

</details>

---

93. How to count the number of "s" in the string Infosys in SQL?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
<blockquote>

- In both *SQL and PostgreSQL*, you can use the `LEN() or LENGTH()` function along with the `REPLACE()` function to count the number of occurrences of a specific character in a string.

For example, to count the number of "s"s in the string "Infosys", you can use the following SQL query:

```SQL

SELECT LEN('Infosys') - LEN(REPLACE('Infosys', 's', '')) AS num_of_s;
```

- In PostgreSQL, you can use the LENGTH() function instead of LEN():

```SQL

SELECT LENGTH('Infosys') - LENGTH(REPLACE('Infosys', 's', '')) AS num_of_s;
```

</blockquote>

</details>

---

94. Do you know anything about Query optimization or Performance Tuning?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary> <b>Show Answer</b> </summary>
<blockquote>

Query optimization and performance tuning are techniques used to improve the performance of SQL queries and database systems. The goal is to make queries run faster and more efficiently, leading to improved application performance and user experience. It involves various strategies such as indexing, query rewriting, optimizing join operations, using appropriate data types, and analyzing execution plans to identify bottlenecks and optimize query execution.

</blockquote>

</details>

---

95. Assume you have an employee table which stores the details of all employees and one department table which stores the department information, and both these tables have a primary-foreign key relationship, where emp_id of the employee table is a primary key and dept_id of the department table is a foreign key. Your boss has given you the task of fetching the details of those employees who have not been assigned any department yet. How will you do that?

![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

 <details><summary> <b>Show Answer</b> </summary>

> 
```sql
select * from employee
where emp_id not in (
select dept_id from department);
```

</details>

---

96. Let's say you have two tables, one is an employee which has employee details like id, name, etc and another one is a salary table having columns like id, salary, etc. Give the query in SQL which will return the employee’s name, id and salary of those employees. Also, display the name and id of those employees even if salary details are not present.

 ![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
<details><summary> <b>Show Answer</b> </summary>

>
```sql
select e.id, e.name, s.salary
from employee e 
left join salary s
on e.id = s.id;
```


</details>

---

97. Can we use `join` to join more than 2 tables in SQL? If yes, then give a query for it as an example.

   ![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>

> Yes, we can join more than 2 tables with `join`.  
```sql
select column1 
from table1
join table2
on table1.column2 = table2.column2
join table3
on table1.column3 = table3.column3;
```

</details>

---

98. In SQL, give the query that will fetch the records of those employees who are from the product department and assigned to one project. [Consider two tables employee and project, which has the same column as id] 

  ![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>

>
```sql
select * from employee
where department = "product" 
and employee.id in ( 
select id from project);
```

</details>

---
99. Imagine you are handling a "company" database which has one table as "department" and your manager is asking you to give the details of those employees who joined in January of 2022.

   ![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>

> 
```sql
select * from department 
where year(joined) = 2022 and month(joined) = 2;
```
</details>

---


100. In a company there are 5 departments and in each department, there is one manager you have to get the employee id "emp_id" and "name" of those employees who are working for the Manager having "Manager_id" as 432.[ take the table name as Employee]

![Beginner](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

 
<details><summary> <b>Show Answer</b> </summary>

> 
```sql
select emp_id, name
from Employee
where Manager_id = 432;
```


</details>

---
101. Suppose you are having a "employee" table, in which you are trying to find out those employee’s details having the same department as the employee whose id is 121.

![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

   
<details><summary> <b>Show Answer</b> </summary>

> 
```sql
select * from employee
where department = 
( select department 
from employee
where id = 121
);
```

</details>

---
102. Suppose you are handling two tables, one is an employee table and another one is a department table and there is a primary-foreign key relationship between both. Assume your boss asked you to give the emp_id and name of those employees who works in the product department. 

![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

   
<details><summary> <b>Show Answer</b> </summary>

> 
```sql
select e.name , e.id from employee e , department d
where e.id = d.id
and d.department = "product"
```

</details>

---

103. In an "employee" table , give me the query that will fetch the employee detail of those employees who are getting the second highest salary in the company. 

   ![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>

> 
```sql
select * from employee
where salary in 
( select max(salary) from employee
where salary not in 
( select max(salary) from employee
);
```
</details>

---

104. Write a SQL query that will give the details of those students, from the student table, who comes from NY, Florida and Alaska state and who are from 9th, 10th, 11th and 12th class. 

  ![Beginner](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>

> 
```sql
select * from student
where state in ["NY", "Florida", "Alaska"] 
and class in [ "9th", "10th", "11th", "12th"];
```

</details>

---
105. Can we use `inner join` without the `on` condition?

   ![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>

> Yes, we can use the `inner join` without `on` condition in SQL as it is an optional condition in the inner join or joins. If used without one condition, it will generate the same output as `cross join`.

</details>

---
106.  How will you execute a self-join SQL?

 ![Beginner](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>

> A self-join can be executed by joining the table to itself. for example: 
```SQL
select t1.name, t1.id
from table1 t1
join table1 t2 
on t1.id = t2.emp_id;
```

</details>

---

107. Talk about joins and its types in SQL.

 ![Beginner](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>

> Joins, in SQL, are useful to combine records of two or more different tables. 
> We have various types of joins like:  
> - Inner Join: After join, it returns matching rows of both tables only.
> - Outer Join: After join, it returns matching rows of both the tables plus left out rows of left table and right table.
> - left Join: It returns matching rows of both the tables plus left out rows from the left table.
> - right Join: It returns matching rows of both the tables plus left out rows from the right table.

</details>

---

108. Give the query that will display the total marks of all the students by adding mid-term and final_term marks. return name and roll_no also.

![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

   
<details><summary> <b>Show Answer</b> </summary>

> 
```sql
select name, roll_no,
mid_term + final_term as Total_marks
from student;
```

</details>

---

109. Imagine you have two tables, "customers" and "orders" and you have to find all customers who placed 0 or more orders. How will you do that in SQL?

![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

 
<details><summary> <b>Show Answer</b> </summary>

> Using `left join` we can find the details of all the customers who placed 0 or more orders.  
```SQL
select customer_number, name
from customers
left join orders 
on orders.customer_number = customer_number;
```

</details>

---
110. In SQL, suppose you are handling two tables, "customers" and "orders", how would you execute the outer join between both tables?

![Beginner](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

 
<details><summary> <b>Show Answer</b> </summary>

> Suppose we are taking customer names and order_id from both tables while doing the full join.    
```SQL
select customers.name, orders.order_id
from customers
full join orders
on customers.id = orders.order_id;
```

</details>

---
111. what is the difference between union and full join in SQL?

   ![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>

> - Union joins the two-table data vertically, whereas full join joins the two table data horizontally.
> - There are more restrictions when using a union between two tables than using full join. 
> - Union will take only distinct values from both tables, whereas full join combines all the data from both tables. 

</details>

---

112. Imagine there are two tables’ Workers and Managers, where the Workers table has all the employee names along with the employee id who are working for the company and the Managers table has all the manager’s names along with the manager id of that company. Give one SQL query that will print the names of Workers who are also Managers.

![Beginner](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
 
<details><summary> <b>Show Answer</b> </summary>

> 
```sql
select Workers.name from Workers
inner join Managers
on Workers.empID = Managers.managerID;
```

</details>

---

113. Assume you have a Worker table having columns like name, id, department, salary, address, etc. How will you find the number of workers in each department in descending order?

 ![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>

> 
```sql
select department, count(id) as number_of_emp 
from Worker
group by department
order by number_of_emp desc;
```

</details>

---
