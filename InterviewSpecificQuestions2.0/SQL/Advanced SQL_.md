1.  How do you sort data after it has been pulled from a database?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

To sort data after it has been pulled from a database, you can use the `ORDER BY` clause in SQL. Here's an example query:

```sql
SELECT column1, column2, ...
FROM your_table
ORDER BY column1 ASC/DESC;
```

Explanation:
- Replace `column1, column2, ...` with the actual columns you want to select from the table.
- Replace `your_table` with the name of your table.
- Replace `column1` with the specific column you want to sort the data by.
- Replace `ASC` or `DESC` to specify the sorting order. `ASC` stands for ascending order (smallest to largest), and `DESC` stands for descending order (largest to smallest).

For example, if you have a table named `employees` with columns `employee_id`, `first_name`, and `last_name`, and you want to retrieve the data sorted by `employee_id` in ascending order, the query would be:

```sql
SELECT employee_id, first_name, last_name
FROM employees
ORDER BY employee_id ASC;
```

This query will retrieve the data from the `employees` table and sort it based on the `employee_id` column in ascending order.

Adjust the table name, column names, and sorting criteria as per your specific table structure and requirements.

</details>

---

2.  How to change an entry to null in sql ?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Show Answer</b></summary>

To change an entry to `NULL` in SQL, you can use the `UPDATE` statement along with the `SET` clause. Here's an example query:

```sql
UPDATE your_table
SET column_name = NULL
WHERE condition;
```

Explanation:
- Replace `your_table` with the name of your table.
- Replace `column_name` with the name of the column where you want to change the entry to `NULL`.
- Replace `condition` with the specific condition that identifies the row(s) you want to update.

For example, let's say you have a table named `customers` with columns `customer_id` and `email`, and you want to change the email of a specific customer with `customer_id = 123` to `NULL`. The query would be:

```sql
UPDATE customers
SET email = NULL
WHERE customer_id = 123;
```

After executing this query, the email of the customer with `customer_id = 123` will be set to `NULL`.

Make sure to adjust the table name, column name, and condition as per your specific table structure and requirements.

</details>

---

3. How do you delete duplicate record with no key or timestamp.

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
    
<details><summary>Show Answer</summary>

<blockquote>

To delete duplicate records when you don't have a key or timestamp to uniquely identify them, you can use a combination of temporary tables and self-joins. Here's an example of how you can approach this:

```sql
-- Step 1: Create a temporary table with a unique identifier
CREATE TEMPORARY TABLE temp_table AS
SELECT *, ROW_NUMBER() OVER (ORDER BY column1, column2) AS row_num
FROM your_table;

-- Step 2: Identify the duplicate records based on the columns that define duplication
SELECT column1, column2, COUNT(*) AS duplicate_count
FROM temp_table
GROUP BY column1, column2
HAVING COUNT(*) > 1;

-- Step 3: Delete the duplicate records except for one occurrence
DELETE FROM your_table
WHERE (column1, column2) IN (
    SELECT column1, column2
    FROM temp_table
    GROUP BY column1, column2
    HAVING COUNT(*) > 1
) AND row_num > 1;

-- Step 4: Drop the temporary table
DROP TABLE temp_table;
```

Explanation:
1. Step 1: Create a temporary table (`temp_table`) that includes all columns from `your_table` and assigns a unique row number to each record using the `ROW_NUMBER()` window function. Adjust the `ORDER BY` clause to define the order of records based on your preference.
2. Step 2: Identify the duplicate records by grouping the records based on the columns that define duplication (`column1`, `column2`, etc.) and selecting the count of duplicates (`duplicate_count`).
3. Step 3: Delete the duplicate records from `your_table` by using a subquery with the `IN` operator. The subquery selects the duplicate records based on the same grouping criteria and excludes the first occurrence (`row_num > 1`).
4. Step 4: Finally, drop the temporary table (`temp_table`).

Note: This approach assumes that the combination of columns used for identifying duplicates is sufficient to determine uniqueness. If you have additional criteria, you can modify the `GROUP BY` clause and the conditions in the `DELETE` statement accordingly.

</blockquote>

</details>

---

4. How can you calculate the total amount for each month using the SQL CASE statement along with aggregation functions?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary><b>Show Answer</b></summary>


SQL Query to Get the Amount for Each Month (with Null for Non-Matching Months):

```sql
SELECT 
    SUM(CASE WHEN MONTH(transaction_date) = 1 THEN amount ELSE NULL END) AS January,
    SUM(CASE WHEN MONTH(transaction_date) = 2 THEN amount ELSE NULL END) AS February,
    SUM(CASE WHEN MONTH(transaction_date) = 3 THEN amount ELSE NULL END) AS March,
    -- Add more months here as needed
FROM transactions;
```

Explanation:
This MySQL query uses the `SUM` function with conditional statements (`CASE WHEN`) to calculate the sum of the `amount` column for each month. Each month is represented as a separate column in the result. The `CASE WHEN` statement checks the month of the `transaction_date` and returns the `amount` if it matches the respective month, otherwise it returns `NULL`.

</details>

---

5. What is the use of  "Merge" Command in SQL ?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary><b>Show Answer</b></summary>

SQL Command "MERGE" (also known as UPSERT) is used to perform both INSERT and UPDATE operations on a target table based on a condition specified in the query. It combines the functionality of both INSERT and UPDATE statements into a single statement.
  
Let's say we have a target table named `employees` with columns `employee_id`, `name`, and `salary`, and a source table named `employee_updates` with columns `employee_id` and `salary_updates`. We want to update the salary of employees if their records exist in the source table, otherwise, we want to insert a new record.

The MERGE statement would look like this:

```sql
MERGE INTO employees AS target
USING employee_updates AS source
ON (target.employee_id = source.employee_id)
WHEN MATCHED THEN
    UPDATE SET target.salary = source.salary_updates
WHEN NOT MATCHED THEN
    INSERT (employee_id, name, salary)
    VALUES (source.employee_id, target.name, source.salary_updates);
```

In this example, the `MERGE INTO` clause specifies the target table (`employees`) and the `USING` clause specifies the source table (`employee_updates`). The `ON` clause defines the condition for matching rows between the target and source tables.

The `WHEN MATCHED THEN` block specifies the action to be taken when a matching row is found. In this case, it performs an update on the `salary` column of the target table using the value from the `salary_updates` column of the source table.

The `WHEN NOT MATCHED THEN` block specifies the action to be taken when no matching row is found. It inserts a new record into the target table using the values from the source table.

This way, the MERGE statement allows you to handle both INSERT and UPDATE operations in a single query, based on the specified conditions.

</details>

---

6. How would you do a SQL call for employees with a salary over 150K?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
<blockquote>

To retrieve employees with a salary over 150K in SQL and PostgreSQL, you can use the SELECT statement along with the WHERE clause to filter the results based on the salary column. Here's an example query:

```sql

SELECT * FROM employees WHERE salary > 150000;
```

This query selects all columns from the "employees" table where the "salary" column is greater than 150000.

Note that you'll need to replace "employees" and "salary" with the actual names of your table and salary column, respectively.

</blockquote>

</details>

---
7. What is difference between Table and View in SQL?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

A `table` in SQL is a database object that stores data in `rows` and `columns`, whereas a `view` in SQL is a virtual table that does not store data physically but presents data from one or more tables in a structured manner. 

</blockquote>

</details>

---
8. What is a View?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

A `view` in SQL is a virtual table that does not store data physically but presents data from one or more tables in a structured manner. `Views` are used to simplify complex queries, hide the complexity of underlying tables, and restrict access to certain data for security purposes.

</blockquote>

</details>

---
9. Does a view contain any data in it?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

No, a `view` does not contain any data in it. It is a virtual table that presents data from one or more tables in a structured manner. The data in a `view` is stored in the underlying `tables` and is retrieved and presented by the `view` as if it were a table.

</blockquote>

</details>

---
10. Can you create a view from another view?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Yes, you can create a view from another view in SQL. This is known as a `nested view`. The syntax for creating a nested view is similar to creating a regular view. However, instead of specifying a table as the source of data, you specify another view. 

Here is an example syntax for creating a nested view:

```sql
CREATE VIEW nested_view AS
SELECT column1, column2, ...
FROM another_view
WHERE condition;
```

</blockquote>

</details>

---
11. How do you create a table view?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

To create a table view in SQL, you use the `CREATE VIEW` statement. The syntax for creating a view is similar to that of creating a table, but instead of specifying the columns and data types, you specify the columns and data that you want to include in the view. Here is an example syntax:

```sql
CREATE VIEW my_view AS
SELECT column1, column2, ...
FROM my_table
WHERE condition;
```

In this example, `my_view` is the name of the view, `column1`, `column2`, etc. are the columns that you want to include in the view, `my_table` is the name of the table that the view is based on, and `condition` is the optional condition that filters the data in the view.

</blockquote>

</details>

---
12. How to use 'as' with unions and views. 

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

In the case of a `UNION` operation, the `AS` keyword can be used to provide an alias for the resulting combined table. For example:

```sql
SELECT column1, column2
FROM table1
UNION
SELECT column1, column2
FROM table2
AS combined_table;
```

In this query, the resulting table from the `UNION` operation will be named "combined_table" due to the use of the `AS` keyword.

Similarly, the `AS` keyword can be used in a `CREATE VIEW` statement to give an alias for a view or to rename columns in the view's result set. For example:

```sql
CREATE VIEW my_view AS
SELECT column1 AS new_name1, column2 AS new_name2
FROM my_table;
```

In this query, the resulting view will be named "my_view" and the column names in the view's result set will be "new_name1" and "new_name2" instead of "column1" and "column2" from the original table.

</blockquote>

</details>

---
13. What is the best practice for using triggers?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Triggers are powerful tools in SQL, but they should be used with caution to avoid unintended consequences. Here are some best practices for using triggers:

1. Only use triggers when necessary: Triggers should only be used when there is no other alternative for achieving the same result. In some cases, a stored procedure or application code may be a better option.

2. Keep triggers simple: Triggers should be simple and easy to understand. Avoid complex logic or multiple triggers on the same table.

3. Test thoroughly: Before deploying a trigger to a production environment, it should be thoroughly tested in a development or test environment.

4. Document: Triggers should be clearly documented, including the purpose, functionality, and any potential side effects.

5. Use caution with `DML` statements: Triggers that execute DML statements (such as `INSERT`, `UPDATE`, `DELETE`) can have a significant impact on performance. Use caution when using `DML` statements in triggers.

</blockquote>

</details>

---
14. Create a trigger to delete an account if it has more than zero contacts.

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Assuming a table named "accounts" with a primary key "id" and a table named "contacts" with a foreign key "account_id" that references "accounts.id":

```SQL
CREATE TRIGGER delete_account_trigger
BEFORE DELETE ON accounts
FOR EACH ROW
BEGIN
  DECLARE contact_count INT;
  SELECT COUNT(*) INTO contact_count FROM contacts WHERE account_id = OLD.id;
  IF contact_count > 0 THEN
    SIGNAL SQLSTATE '45000' SET MESSAGE_TEXT = 'Cannot delete account with contacts';
  END IF;
END
```

This trigger will prevent the deletion of any account that has one or more contacts associated with it.

</blockquote>

</details>

---

15. List the Types of triggers in SQL?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

There are two types of triggers in SQL:

1. DML Triggers: DML triggers execute automatically in response to certain data manipulation language (DML) events, such as `INSERT`, `UPDATE`, and `DELETE` statements.

2. DDL Triggers: DDL triggers execute automatically in response to certain data definition language (DDL) events, such as `CREATE`, `ALTER`, and `DROP` statements.

Both types of triggers can be defined as either "BEFORE" or "AFTER" triggers. BEFORE triggers execute before the triggering statement, and can be used to modify the data before it is inserted, updated, or deleted. AFTER triggers execute after the triggering statement, and can be used to audit changes or enforce business rules.

</blockquote>

</details>

---
16. What are triggers?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

In SQL, a `trigger` is a special type of stored procedure that automatically executes in response to certain events or changes in the database. Triggers can be used to enforce business rules, maintain data integrity, and perform complex tasks based on changes to the data. There are two main types of triggers: "before" triggers and "after" triggers, which fire before or after the event or change occurs.

</blockquote>

</details>

---

17. What are procedures in SQL?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

SQL procedures are a set of pre-written SQL codes that are saved in the database server. These procedures can be called and executed by applications or other database users. SQL procedures help in simplifying the development process by creating reusable code that can be called multiple times.
</blockquote>

</details>

---

18. What is a stored procedure?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

A `stored procedure` is a type of SQL procedure that is stored in the database server. `Stored procedures` are precompiled SQL codes that can be executed multiple times by different applications or users. They help in improving the performance of database applications by reducing network traffic and database overhead. `Stored procedures` can take input parameters, perform data manipulation operations, and return output values.
</blockquote>

</details>

---

19. How to check the performance of a stored procedure?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg) 

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

There are different ways to check the performance of a stored procedure in SQL. Some of them are:

1. Using Execution Plan: Execution plan shows the performance of a stored procedure by displaying the query optimization and execution path. To view the execution plan of a stored procedure, use the "SET SHOWPLAN_TEXT" command or use the "Display Estimated Execution Plan" option in SQL Server Management Studio.

2. Using Profiler: SQL Server Profiler is a tool that helps in analyzing and monitoring the performance of SQL queries and stored procedures. You can use this tool to trace the stored procedure execution and identify any performance issues.

3. Using Execution Statistics: SQL Server provides execution statistics for stored procedures that show the performance details like execution time, CPU time, memory usage, and I/O usage. You can view the execution statistics using the "SET STATISTICS TIME ON" command or the "Include Actual Execution Plan" option in SQL Server Management Studio.

</blockquote>

</details>

---
20. Where do we use SQL procedures?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>
  
SQL procedures can be used in many places, such as:

- To encapsulate business logic that needs to be executed frequently
- To improve performance by precompiling and caching frequently executed statements
- To enforce security by restricting access to sensitive data or operations
- To implement complex data validation rules and data transformations
- To automate repetitive tasks and reduce the workload on the application layer
- To create a standard interface for data access and manipulation that can be reused across multiple applications

</blockquote>

</details>

---

21. How to write a stored procedure?


![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>
  
To write a `stored procedure` in SQL, you can use the following syntax:

```sql
CREATE PROCEDURE procedure_name
    @parameter1 data_type,
    @parameter2 data_type,
    ...
AS
BEGIN
    /* SQL statements */
END
```

Here, `procedure_name` is the name of the stored procedure, and `@parameter1`, `@parameter2`, etc. are the input parameters that the procedure can accept. The `AS` keyword is used to start the body of the procedure, which contains the SQL statements that will be executed when the procedure is called.

</blockquote>

</details>

---
22. What is the difference between UNION and UNION ALL?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b>Answer</b></summary>
  
<blockquote>
UNION and UNION ALL are used to combine the result sets of two or more SELECT statements, but there is a significant difference between them. 

- UNION returns only distinct values whereas UNION ALL returns all the rows, including duplicates.
- UNION operation eliminates duplicate rows from the result set, whereas UNION ALL does not.
- UNION requires more overhead compared to UNION ALL because it has to sort the combined result set to remove duplicates.
- UNION ALL is faster than UNION when combining large data sets because it does not have to perform a sort operation.

So, we use UNION when we want to combine two or more tables with the same structure and eliminate duplicate rows, whereas UNION ALL is used when we want to combine two or more tables with the same structure, including duplicates.
</blockquote>

</details>

---
23. What are indexes in SQL?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>
Indexes are database structures that improve the performance of queries by enabling quick retrieval of data from the database. They are created on one or more columns of a table and contain a sorted list of values that reference the physical location of the data. Indexes are used to speed up data retrieval operations, such as searching, sorting, and grouping, by reducing the number of disk I/O operations required to access the data. However, indexes can also slow down write operations, such as INSERT, UPDATE, and DELETE, because the index must be updated whenever the data is changed. 
</blockquote>

</details>

---

24. Where would you place a COUNT() in SQL?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
<details><summary><b> Show Answer</b></summary>
  
<blockquote>
You can place COUNT() function in the SELECT clause of a SQL query to return the number of rows that match the specified condition.

Example for COUNT() function in given below:

```sql
SELECT COUNT(*) FROM customers;
```
This will return the total number of rows in the table "customers".
</blockquote>

</details>

---

25. What are aggregate functions?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary><b> Show Answer</b></summary>
  
<blockquote>
Aggregate functions are SQL functions that are used to perform calculations on a set of values and return a single value. The most commonly used aggregate functions in SQL are COUNT(), SUM(), AVG(), MIN(), and MAX().
</blockquote>

</details>

---


26. How do you use the MIN(), MAX() aggregation function?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>
The MIN() and MAX() functions are used to return the minimum and maximum value of a column in a table, respectively. 

Here's an example of using the MIN() function to find the minimum value in a table:

```sql
SELECT MIN(column_name)
FROM table_name;
```

Similarly, you can use the MAX() function to find the maximum value in a table:

```sql
SELECT MAX(column_name)
FROM table_name;
```

</blockquote>

</details>

---

27. Explain SQL GROUP BY clause.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The `GROUP BY` clause in SQL is used to group rows based on one or more columns. When you use `GROUP BY`, the result set is divided into groups based on the values in the specified columns. You can then use aggregate functions, such as `SUM`, `COUNT`,` AVG`, `MIN`, or `MAX`, to perform calculations on each group.

For example, if you have a table of sales data that includes columns for Salesperson, Product, and SalesAmount, and you want to group the data by Salesperson and Product and display the total sales for each combination of Salesperson and Product, you could use the following SQL statement:

```sql
SELECT Salesperson, Product, SUM(SalesAmount) as TotalSales
FROM Sales
GROUP BY Salesperson, Product;
```

This statement groups the sales data by the Salesperson and Product columns and calculates the sum of the SalesAmount column for each group. The output includes the Salesperson, Product, and TotalSales columns.

</blockquote>

</details>

---

28. List the aggregate functions.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

- **AVG():** This function is used to returns the average value from specified columns.
- **COUNT():** This function is used to returns the number of table rows, including rows with null values.
- **MAX():** This function is used to returns the largest value among the group.
- **MIN():** This function is used to returns the smallest value among the group.
- **SUM():** This function is used to returns the total summed values(non-null) of the specified column.

</blockquote>

</details>

---



29.When managing a contact_details table in SQL, you found out that some of the records are duplicates and now you want to delete those duplicate records only so that only distinct records are leftout in your table. Give the query for this that will delete the duplicate records. In contact_details table, columns are phoneNo, name, id etc. 

 ![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary> <b>Show Answer</b> </summary>

> 
```sql
delete d1 from contact_details d1
inner join contact_details d2
where d1.id > d2.id
and d1.phoneNo = d2.phoneNo;
```

</details>

---
30. List the scalar functions in SQL?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

SQL has a variety of built-in scalar functions that can be used to manipulate data in various ways. Here are some of the commonly used scalar functions in SQL:

- String Functions: `CONCAT`, `SUBSTRING`, `LENGTH`, `REPLACE`, and more.
- Numeric Functions: `ABS`, `CEILING`, `FLOOR`, `MOD`,and more.
- Date and Time Functions: `GETDATE`, `DATEADD`, `DATEDIFF`, YEAR.
- Aggregate Functions: COUNT, SUM, AVG, MIN, MAX, and more.
- Miscellaneous Functions: ISNULL, COALESCE, NULLIF, and more.

</blockquote>

</details>

---

31. How to troubleshoot a long query?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
<blockquote>

To troubleshoot a long query in SQL, you can follow these steps:

- *Analyze the query execution plan*: Use the EXPLAIN command to generate the query execution plan and analyze it to identify performance bottlenecks, such as table scans or inefficient join operations.

- *Check for indexing issues*: Ensure that the query is using the appropriate indexes by using the INDEX command to see which indexes are being used, and consider creating new indexes if necessary.

- *Optimize the query*: Consider rewriting the query or using query hints to force the optimizer to use a specific execution plan that may be more efficient.

- *Evaluate server and database configuration*: Review the server hardware and software configuration, as well as the database configuration, to ensure that they are optimized for performance.

- *Monitor query performance*: Use SQL performance monitoring tools to identify slow-running queries and analyze their execution patterns, and monitor query performance over time to identify trends and proactively address potential performance issues.

- *Consider scaling out the database*: If the database is experiencing high traffic or has large data volumes, consider scaling out the database by adding more servers or using sharding to distribute data across multiple servers.

</blockquote>

</details>

---

32. What is the difference between H2 Database and MySQL?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
<blockquote>

H2 and MySQL are both relational database management systems, but differ in their licensing, performance, features, and scalability. H2 is open-source, faster for small to medium-sized databases, and has advanced features, while MySQL is owned by Oracle, better for large-scale databases, and more scalable. The choice depends on the specific needs of the application.

</blockquote>

</details>

---

33. How do you compare the data in the Database?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
<blockquote>

To compare data in a database, you need to execute queries to retrieve the data from each data set, store the results in temporary tables or data structures, compare the data using a suitable method, and analyze the results to identify any differences or discrepancies. The specific approach will depend on the database system and the nature of the data being compared.

</blockquote>

</details>

---

34. What is an Alias?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

- In SQL, an alias is a temporary name assigned to a table or column in a query. Aliases can be used to make column names more meaningful or to distinguish between multiple tables with similar names.

- Aliases are created using the AS keyword, which is optional. Here's an example of creating an alias for a table:
```sql
SELECT * FROM employees AS emp;
```
In this example, the table "employees" is given the alias "emp". From this point forward in the query, the table can be referred to as "emp" instead of "employees". This can make the query more readable and easier to understand.

- Aliases can also be used for columns. Here's an example:
```sql
SELECT first_name AS "First", last_name AS "Last" FROM employees;
```
In this example, the column "first_name" is given the alias "First", and the column "last_name" is given the alias "Last". This can be useful for making the column names more descriptive or easier to read.

- Aliases are a powerful feature in SQL that can be used to make queries more readable and easier to understand.

</blockquote>

</details>

---

35. what is replace and rank function in SQL?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary> Show Answer </summary>

<blockquote>

- In SQL, the REPLACE function is used to replace all occurrences of a substring within a string with a new substring. The basic syntax for the REPLACE function is:
```sql
REPLACE(string, old_substring, new_substring)
```
Here, "string" is the original string that you want to modify, "old_substring" is the substring that you want to replace, and "new_substring" is the substring that you want to replace it with.

For example, if you have a string "Hello, world!" and you want to replace the comma with a space, you can use the following query:
```sql
SELECT REPLACE('Hello, world!', ',', ' ');
```
This will return the string "Hello world!" with the comma replaced by a space.

- The RANK function in SQL is used to assign a rank to each row within a result set based on the values in one or more columns. The basic syntax for the RANK function is:
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

36. How do you create a table and populate it in the same instance in PostgreSQL ?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

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


37. What is the substring function used for?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

The SUBSTRING function in SQL is used to extract a substring from a string value. The function takes three arguments: the input string, the starting position, and the length of the substring.

Here's the syntax of the SUBSTRING function:
```sql
SUBSTRING(input_string, start_position, length)
```
The first argument is the input string from which the substring will be extracted. The second argument is the starting position of the substring within the input string. The third argument is the length of the substring.

Here's an example of using the SUBSTRING function to extract a substring from a string value:
```sql
SELECT SUBSTRING('Hello World', 1, 5);
```
This SQL statement retrieves the substring "Hello" from the input string "Hello World". The start_position argument is 1, which means the substring will start at the first character of the input string. The length argument is 5, which means the substring will contain the first five characters of the input string.

The SUBSTRING function is useful for extracting parts of a string, such as a person's first name from a full name or a year from a date value. It's commonly used in combination with other string functions and operators to manipulate and analyze string data in SQL.

</blockquote>

</details>

---
38. Talk about transaction control language and its advantages

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

Transaction Control Language (TCL) is a set of SQL statements that are used to control transactions in a relational database. The three main TCL commands are COMMIT, ROLLBACK, and SAVEPOINT.

The advantages of TCL are:

- Data Consistency: TCL commands ensure data consistency in the database. A transaction may contain multiple queries that modify the data in the database. If any of the queries fail to execute, the entire transaction is rolled back to its original state. This helps to maintain the integrity of the data.

- Atomicity: Atomicity is one of the ACID properties of a database. It ensures that a transaction is treated as a single, indivisible unit of work. If any part of a transaction fails, the entire transaction is rolled back, and the database is returned to its original state. This ensures that the database remains consistent and that data is not lost or corrupted.

- Recovery: TCL commands help to recover data in the event of a system failure or unexpected shutdown. When a transaction is committed, the changes made by the transaction are written to the database's transaction log. If the system crashes, the database can use the transaction log to recover any changes that were not written to disk before the failure occurred.

- Concurrency Control: TCL commands help to manage concurrency in a database. Multiple users may be accessing the same data at the same time, and TCL commands ensure that transactions do not interfere with each other. When a transaction is executed, a lock is placed on the data that it accesses. This lock prevents other transactions from modifying the same data until the first transaction is committed or rolled back.

In summary, TCL provides a robust mechanism for managing transactions in a database. It ensures data consistency, atomicity, recovery, and concurrency control, which are critical to maintaining the integrity of the database and its data.

</blockquote>

</details>

---



39. What is the syntax for UPDATE in SQL?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

The UPDATE statement is used in SQL to modify existing records in a database table. Here is the syntax for the UPDATE statement in SQL:
```sql
UPDATE table_name
SET column1 = value1, column2 = value2, ...
WHERE condition;
```
Let's break down the syntax:

- UPDATE: This keyword tells the database to update existing records.
- table_name: This is the name of the table that you want to update.
- SET: This keyword indicates that you are going to set new values for one or more columns in the table.
- column1 = value1, column2 = value2, ...: This specifies the new values that you want to set for one or more columns in the table. Each column and its new value are separated by a comma.
- WHERE: This keyword is used to filter the records that you want to update. The condition specified after the WHERE keyword determines which records will be updated.
- condition: This specifies the condition that must be met for a record to be updated. If the condition is not met, the record will not be updated.
Here is an example of an UPDATE statement that sets a new value for the "price" column in a "products" table for all products with a "product_id" greater than or equal to 100:
```sql
UPDATE products
SET price = 19.99
WHERE product_id >= 100;
```
This statement sets the "price" column to 19.99 for all products with a "product_id" greater than or equal to 100. It's important to note that the WHERE clause is used to filter the records that are updated. If you omit the WHERE clause, all records in the table will be updated.

</blockquote>

</details>

---


40. What is SQL window functions?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> Show Answer </summary>

<blockquote>

In SQL, window functions are used to perform calculations across a set of rows that are related to the current row. These calculations are performed on a "window" of rows that are defined by a specific set of criteria, rather than on the entire table. Window functions are particularly useful for performing complex calculations on subsets of data, such as finding running totals, calculating moving averages, or ranking results.

Window functions are used in combination with the OVER clause, which defines the window or set of rows that the calculation will be performed on. The syntax for a window function is as follows:
```sql
function_name(expression) OVER (
    [PARTITION BY partition_expression, ... ]
    [ORDER BY sort_expression [ASC | DESC], ... ]
    [ROWS/RANGE BETWEEN window_specification]
)
```
Here's a brief explanation of each part of the syntax:

- function_name: This is the name of the window function that you want to use, such as SUM, AVG, RANK, or ROW_NUMBER.
- expression: This is the column or expression that you want to perform the calculation on.
- PARTITION BY: This is an optional clause that partitions the result set into smaller groups based on the values of one or more columns. The calculation is performed separately for each group.
- ORDER BY: This is an optional clause that specifies the order in which the rows are processed. The calculation is performed in the order specified by this clause.
- ROWS/RANGE BETWEEN: This is an optional clause that defines the window or set of rows that the calculation will be performed on. The window can be defined as a set of rows relative to the current row, or as a range of values based on the order specified by the ORDER BY clause.
Here's an example of a window function that calculates the running total of a "sales" column in a "sales_data" table partitioned by a "region" column and ordered by a "date" column:
```sql
SELECT region, date, sales,
       SUM(sales) OVER (PARTITION BY region ORDER BY date) as running_total
FROM sales_data;
```
This query uses the SUM window function to calculate the running total of the "sales" column for each region, ordered by date. The result set includes the original "region", "date", and "sales" columns, as well as a new "running_total" column that contains the result of the window function.

</blockquote>

</details>

---


41. How would you delete duplicate record in a database?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary><b> Show Answer</b></summary>

<blockquote>
To delete duplicate information in a database, you can use the DELETE statement in combination with a subquery that selects the duplicate rows. Here is a general approach to delete duplicate information from a table:

- Identify the columns that determine whether a row is a duplicate. For example, if you have a table of customers, you might consider the columns "first_name", "last_name", and "email" to determine whether two rows represent the same customer.

- Use a subquery to select the duplicate rows. The subquery should return the primary key values of the rows that you want to delete. For example, if your customers table has a primary key column named "id", you can use a subquery like this:
```sql
SELECT MIN(id) as id_to_keep
FROM customers
GROUP BY first_name, last_name, email
HAVING COUNT(*) > 1
```
This subquery selects the minimum value of the "id" column for each set of duplicate rows, based on the "first_name", "last_name", and "email" columns.

- Use the selected primary key values to delete the duplicate rows from the table. You can use a DELETE statement with a WHERE clause that matches the primary key values returned by the subquery. For example:
```sql
DELETE FROM customers
WHERE id NOT IN (
    SELECT MIN(id) as id_to_keep
    FROM customers
    GROUP BY first_name, last_name, email
    HAVING COUNT(*) > 1
)
```
This statement deletes all rows from the "customers" table whose "id" value is not in the set of primary key values selected by the subquery.

Note that you should always back up your data before deleting any rows from a table, and carefully review the results of the subquery before executing the DELETE statement to ensure that you are deleting the correct rows.
</blockquote>

</details>

---
42. Consider a database schema for an online shopping application. The schema consists of the following tables:

 - Customers (customer_id, name, email, address)
 - Orders (order_id, customer_id, order_date, total_amount)
 - OrderItems (order_item_id, order_id, product_id, quantity, price)
 - Products (product_id, name, price, description)
 - Categories (category_id, name)

Write an SQL query to retrieve the total revenue generated by each category, ordered by the highest revenue first.

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

```sql

SELECT c.name AS category, SUM(oi.quantity * oi.price) AS revenue
FROM Categories c
JOIN Products p ON c.category_id = p.category_id
JOIN OrderItems oi ON p.product_id = oi.product_id
GROUP BY c.name
ORDER BY revenue DESC;


```

</blockquote>

</details>

---

43. How do you grant or revoke privileges on database objects in SQL?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

you can grant or revoke privileges on database objects using the GRANT and REVOKE statements. Here's how you can use these statements:

To grant privileges:

```sql

GRANT privilege_name ON object_name TO user_or_role;

```

The privilege_name can be specific privileges such as SELECT, INSERT, UPDATE, DELETE, or ALL. The object_name represents the name of the database object (e.g., table, view, procedure) on which the privileges are granted. The user_or_role specifies the user or role to whom the privileges are granted.

For example, to grant SELECT and INSERT privileges on a table called "employees" to a user named "john":

```sql

GRANT SELECT, INSERT ON employees TO john;

```

To revoke privileges:

```sql
REVOKE privilege_name ON object_name FROM user_or_role;

```

The privilege_name, object_name, and user_or_role have the same meaning as in the GRANT statement.

For example, to revoke the INSERT privilege on the "employees" table from the user "john":

```sql

REVOKE INSERT ON employees FROM john;

```


</blockquote>

</details>

---

44. What are the constraints SQL follows in all their databases tool?

![Beginner](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

 
<details><summary> <b>Show Answer</b> </summary> 

> In all the SQL databases there are some constraints like: 
> - not null: This constraint restricts the values that are null from being inserted into columns.
> - unique: This will allow only unique values in the column along with the null value
> - primary key: This constraint allows only those values that are not null and unique.
> - foreign key: This constraint helps in forming the relationship between two or more tables in SQL.
> - index: This constraint helps in improving query performance and fast retrieval of data
> - check: This is used when we have to check if all the data that is being inserted satisfy a condition.

</details>

---

45. How are primary key constraints and unique key constraints different? 

 ![Beginner](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 

> In a table in SQL, there can be many columns that can be a unique key but only one primary key is allowed on one table. The primary key is a combination of unique key plus null constraint, whereas unique key has only unique constraint and it can be null.

</details>

---

46. When creating a table in SQL, if you forget to make a column as the primary key, then is there any possibility to create a primary key on that column or do we have to delete the table from the database so that we can create a primary key while creating a table?

 ![Beginner](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 

> We can add the primary key after the creation of the table also, for that we can use the `alter` command that will add the primary key column to an existing table. There is no need to delete the table and recreate it again in the database. Just we have to pass a query as:  
```sql
alter table table_name add primary key(column_name);
```
  
</details>

---

47. Create a student table having id, name, age and class as columns in it. Write down the query that will create that table in the "school" database.

![Beginner](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

 
<details><summary> <b>Show Answer</b> </summary> 

> 
```sql
create database school;

use school;

create table school( 
       id int, 
       name varchar(30), 
       age int, 
       class varchar(10)
       );
```

</details>

---
48. Is `drop` and `truncate` commands have the same usage in SQL?

 ![Beginner](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 

> Both `drop` and `truncate` are part of DDL commands and also look similar while deleting records of the table in the database. But one major difference between both is that `drop` deletes all the records from the table as well as the table structure, whereas `truncate` will only delete all the records from the table but not the table structure. Also, the drop command can be used to delete the database, whereas truncate cannot be used to delete the database.

</details>

---

49. Suppose you have created a table called "student" with column fields as id, name, age, address and class. But now you want to rename the "id" column to "student_id", then how will you do that in SQL?

 ![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 

> Using `alter` command, we can rename the column name.  
```sql
alter table student 
rename column id to student_id;
```
> Here "id" column name is changed to "student_id" name.
</details>

---

50. How `rename` and `alter` command different from each other while renaming a table in SQL? 

 ![Beginner](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

 
<details><summary> <b>Show Answer</b> </summary> 

> `rename` command and `alter` both have similar working when renaming a table name in SQL except for the syntax. The only difference between both is that `rename` cannot be used to rename the temporary table, whereas `alter` command can rename a temporary table in SQL.

</details>

---

51. Assume that you have created one table as "emp" and now you want to change that table name to "employee" then what are the ways, in SQL, through which we can change the table name? 

 ![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 

> For changing the table name in SQL, we can go for `rename` command or `alter` command:    
With `rename`
```sql
rename table emp to employee;
```
With `alter`
```sql
alter table emp
rename to employee; 
```

</details>

---

52. Suppose Jack has created a table as "Food" with id and food_name field as varchar datatype. But now he wanted to change the datatype of id from varchar to int. What query he should write that will do his task?

![Beginner](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

 
<details><summary> <b>Show Answer</b> </summary> 

> 
```sql
alter table Food 
modify column id int;
```

</details>

---

53. Differentiate between `alter` and `update` in SQL 

 ![Beginner](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 

> - The `alter` command is a DDL command, whereas `update` is a DML command
> - The `alter` command is used to perform the operation on the structure level. On the other hand, `update` is used to perform an operation on the data level.
> - The `alter` command is used to modify the attribute of the table. The `update` command is used to modify the rows of the table.

</details>

---

54. How do you create an index in a table? 

 ![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 

> 
```sql
alter table Table_name
add index(column_name);
```

</details>

---

55. You have 4 indexes in your table "order" but now you want to remove one index named "author_id" from it. what will be your query for it?

![Beginner](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
 
<details><summary> <b>Show Answer</b> </summary> 

> 
```sql
alter table order
drop index author_id;
```

</details>

---

56. In SQL, how do list all the databases and tables that are available?

![Beginner](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
 
<details><summary> <b>Show Answer</b> </summary>

> - To list the databases we can use the `show databases;` 
> - To list the tables in a particular database, write:
```sql
use database_name;

show tables;
``` 

</details>

---

57. In an employee table, the monthly salary is given to each employee. Your task is to find and fetch the annual salary of employees with their names.

 ![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary> <b>Show Answer</b> </summary>

> 
```sql
select name, 
monthly_salary * 12 as "annual_salary"
from employee;
```

</details>

---

58. In SQL, how will you get the last 3 records from the table "worker" having one unique column id.

 ![Beginner](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
 
<details><summary> <b>Show Answer</b> </summary>

>
```sql
select * from worker
order by id desc
limit 3;
```

</details>

---

59. I have a table called employee in SQL and now I want to create another table as employee_2 that has the same structure and data as the employee table. How can I do this?

![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

   
<details><summary> <b>Show Answer</b> </summary>

>
```sql
create table employee_2 
select * from employee;
```

</details>

---

60. In SQL, how will you display the first 50% of the records of any given table?

![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

 
<details><summary> <b>Show Answer</b> </summary>

>
```sql
select * from table_name
limit (select count(*)/2 from table_name);
```

</details>

---

61. Without using the distinct keyword, how will you get the distinct records from the table in SQL?

![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

   
<details><summary> <b>Show Answer</b> </summary>

> let's say we have an employee table having id and name as columns. We can use the `group by` clause to get the distinct records from the table.  
```sql
select id, name 
from employee
group by id, name;
```
This will group the table records by id and name and gives us distinct records only.
</details>

---

62. In SQL, what are the points that anyone has to keep in mind when using `group by` clause in SQL?

 ![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>

> Points to remember when using `group by` clause:  
> - Use `group by` clause with a select query
> - If `where` clause is used in the query, `group by` clause must be placed after it.
> - If `order by` clause is used in the query, `group by` clause must be placed before it.
> - Columns mentioned in the select query should either be part of the group by clause or an aggregation function is applied to those columns. 

</details>

---

63. Display the name and id of those employees from the employee table whose salary is greater than 40000 and DOJ in 2019.

 ![Beginner](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>

> 
```sql
select id, name 
from employee
where salary > 40000
and DOJ like "2019%";
```

</details>

---

64. In a student table, how you will find the count of repeated rows in SQL?

![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

 
<details><summary> <b>Show Answer</b> </summary>

> 
```sql
select id, count(id) as duplicate 
from student
group by id
having duplicate>1
order by duplicate;
```

</details>

---

65. In SQL, give a generalized query that will fetch the top N records from the table

 ![Beginner](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>

>
```sql
select *
from table_name
order by column_name desc 
limit N;
```

</details>

---

66. How to fetch only records that are present in an even position in SQL?

![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>

> 
```sql
select * from table_name
where id in
(select id from table_name 
where id % 2 = 0);
```

</details>

---

67. Consider you have a company table in SQL. Give the details of those employee who are from Florida, NY and Texas state and earning salary more than 50000 and department is either Finance or Training.

  ![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>

>
```sql
select * from company
where state in [ "Florida", "NY", "Texas"]
and salary > 50000
and department = "Finance" 
or department = "Training";
```

</details>

---
68. Assume you are handling a "student" table in the database having id, name, age, state, and class fields. Your task is to fetch the records of those students who are from "Texas" state.

 ![Beginner](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
 
<details><summary> <b>Show Answer</b> </summary>

> 
```sql
select * from student 
where state = "Texas";
```

</details>

---

69. Tell a way about how to give a different name to a field while executing a select query?

 ![Beginner](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>

> We can use the `as` as an alias name for the column, for example:  
```sql
select Name as "First_name" from table_name;
```

</details>

---

70. Give one single query which includes, select, where, order by, group by, and having clauses in it.  

![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
 
<details><summary> <b>Show Answer</b> </summary>

> The required query can be this:  
```sql
select id, name, class, marks from student 
where marks>= 33 and marks <=100 
order by id 
group by class 
having count(id);
```

</details>

---

71. In SQL, how will you give the count of the students from the student table whose name starts with 'H'.

![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
 
<details><summary> <b>Show Answer</b> </summary>

> 
```sql
select count(name) as Name_H_students from student
where name like 'H%';
```

</details>

---

72. Tell me about the ways through which we can search for a "string" pattern in SQL?

 ![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>

> To search "string" pattern, we can use the `like` operator with `where` class.  
> - To search only for a fixed number of characters we can use '_' with like. For example, we have to find the name of those students having 4 characters only. for that use four underscores.
```sql
select name from student where name like '____'; 
```
   
> - To search string starting with a particular character or substring we can write like this:   
```sql
select name from student where name like 'AK%';
```
   
> - To search string ending with a particular character or substring we can write like this: 
```sql
select name from student where name like '%SK';
```
  
</details>

---

73. Your boss has given you a work to find the details of the workers in "HR" deparment from the "Company" table whose salary ranges between 10000 and 50000.

![Beginner](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
 
<details><summary> <b>Show Answer</b> </summary>

> 
```sql
select * from company
where salary between 10000 and 50000 
and department = "HR";
```

</details>

---
74. From "employee" table give the "names" and "emp_id" of those employees who receive a higher salary than the employee with "emp_id" = 101.

![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

   
<details><summary> <b>Show Answer</b> </summary>

> 
```sql
select emp_id, name from employees 
where salary > 
( select salary from employee
where emp_id = 101
);

```

</details>

---
75. In an employee table, how will you find those employee’s name and emp_id whose salary matches the lowest salary of any of the departments in SQL?

![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

   
<details><summary> <b>Show Answer</b> </summary>

> 
```sql
select name, emp_id from employee
where salary IN 
( select min(salary)
from employee
group by department
);
```

</details>

---

76. In SQL, give the count of those employees who is getting a salary more than the average salary from "employee" table.

   ![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>

> 
```sql
select count(*) from employee
where salary >
(select avg(salary)
from employee
);

```
</details>

---
77. In SQL, what is a cross-join? Give a syntax.

   ![Beginner](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>

> `cross join` also known as `cartesian join`, is used to join each tuple of the 1st table with each tuple of 2nd table. 
> Syntax of cross join:  
```sql
select column_names from table1 
cross join table2 ;
```

</details>

---
78. Is it possible to make a `cross join` work as an `inner join` in SQL.

![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary> <b>Show Answer</b> </summary>

> Yes, it is possible to use `cross join` as an `inner join` in SQL by using `where` clause with it. For example:    
> 
```sql
select * from table1 
cross join table2
where table1.id = table2.id;
```

</details>

---
79. Assume, you have two tables’ "customers" and "orders". So, tell me how will you execute the right join between both tables?

![Beginner](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

 
<details><summary> <b>Show Answer</b> </summary> 

>  
```sql
select customers.* , orders.* 
from customers
right join orders 
on customers.id = orders.id;
```

</details>

---
80. Give the query in SQL that will replace the space with '-' in full name from the employee table.

![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
 
<details><summary> <b>Show Answer</b> </summary>

> For replacing something in SQL select query we can use the `replace` function.  
```sql
select replace(full_name, " ", "-")
from employee;
```

</details>

---
81. When managing a contact_details table in SQL, you found out that some of the records are duplicates and now you want to see the duplicate records only in your result set. What select query you will write for this that will fetch you the duplicate records? In contact_details table, columns are phoneNo, name, etc. 
 
   ![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary> <b>Show Answer</b> </summary>

>
```sql
select phoneNo, name 
from contact_details
group by phoneNo
having count(phoneNo) > 1;
```

</details>

---

