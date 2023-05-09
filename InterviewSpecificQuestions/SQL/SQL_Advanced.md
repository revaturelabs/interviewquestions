1. What is difference between Table and View in SQL?
<details><summary><b> Show Answer</b></summary>
  
<blockquote>
A table in SQL is a database object that stores data in rows and columns, whereas a view in SQL is a virtual table that does not store data physically but presents data from one or more tables in a structured manner. A view can be considered as a saved SQL query that can be used to access and retrieve data as if it were a table.
</blockquote>

</details>

---

2. What is a View?
<details><summary><b> Show Answer</b></summary>
  
<blockquote>
A view in SQL is a virtual table that does not store data physically but presents data from one or more tables in a structured manner. A view can be considered as a saved SQL query that can be used to access and retrieve data as if it were a table. Views are used to simplify complex queries, hide the complexity of underlying tables, and restrict access to certain data for security purposes.
</blockquote>

</details>

---

3. Does a view contain any data in it?
<details><summary><b> Show Answer</b></summary>
  
<blockquote>
No, a view does not contain any data in it. It is a virtual table that presents data from one or more tables in a structured manner. The data in a view is stored in the underlying tables and is retrieved and presented by the view as if it were a table.
</blockquote>

</details>

---

4. Can you create a view from another view?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>
Yes, you can create a view from another view in SQL. This is known as a nested view. The syntax for creating a nested view is similar to creating a regular view. However, instead of specifying a table as the source of data, you specify another view. 

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

5. How do you create a table view?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>
To create a table view in SQL, you use the CREATE VIEW statement. The syntax for creating a view is similar to that of creating a table, but instead of specifying the columns and data types, you specify the columns and data that you want to include in the view. Here is an example syntax:

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

6. as with unions and views. 

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

In the case of a UNION operation, the AS keyword can be used to provide an alias for the resulting combined table. For example:

```sql
SELECT column1, column2
FROM table1
UNION
SELECT column1, column2
FROM table2
AS combined_table;
```

In this query, the resulting table from the UNION operation will be named "combined_table" due to the use of the AS keyword.

Similarly, the AS keyword can be used in a CREATE VIEW statement to give an alias for a view or to rename columns in the view's result set. For example:

```sql
CREATE VIEW my_view AS
SELECT column1 AS new_name1, column2 AS new_name2
FROM my_table;
```

In this query, the resulting view will be named "my_view" and the column names in the view's result set will be "new_name1" and "new_name2" instead of "column1" and "column2" from the original table.

</blockquote>

</details>

---

7. What is the best practice for using triggers?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>
Triggers are powerful tools in SQL, but they should be used with caution to avoid unintended consequences. Here are some best practices for using triggers:

1. Only use triggers when necessary: Triggers should only be used when there is no other alternative for achieving the same result. In some cases, a stored procedure or application code may be a better option.

2. Keep triggers simple: Triggers should be simple and easy to understand. Avoid complex logic or multiple triggers on the same table.

3. Test thoroughly: Before deploying a trigger to a production environment, it should be thoroughly tested in a development or test environment.

4. Document: Triggers should be clearly documented, including the purpose, functionality, and any potential side effects.

5. Use caution with DML statements: Triggers that execute DML statements (such as INSERT, UPDATE, DELETE) can have a significant impact on performance. Use caution when using DML statements in triggers.

</blockquote>

</details>

---

8. Create a trigger to delete an account if it has more than zero contacts.

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

9. Types of triggers in SQL?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

There are two types of triggers in SQL:

1. DML Triggers: DML triggers execute automatically in response to certain data manipulation language (DML) events, such as INSERT, UPDATE, and DELETE statements.

2. DDL Triggers: DDL triggers execute automatically in response to certain data definition language (DDL) events, such as CREATE, ALTER, and DROP statements.

Both types of triggers can be defined as either "BEFORE" or "AFTER" triggers. BEFORE triggers execute before the triggering statement, and can be used to modify the data before it is inserted, updated, or deleted. AFTER triggers execute after the triggering statement, and can be used to audit changes or enforce business rules.

</blockquote>

</details>

---

10. What is the maximum number of records returned by a trigger at once?
<details><summary><b> Show Answer</b></summary>
  
<blockquote>
The maximum number of records returned by a trigger at once depends on the database system being used. Different database systems have different limitations and it's important to consult the documentation of your specific database to determine the limit.
</blockquote>

</details>

---

11. What are triggers?
<details><summary><b> Show Answer</b></summary>
  
<blockquote>
In SQL, a trigger is a special type of stored procedure that automatically executes in response to certain events or changes in the database. Triggers can be used to enforce business rules, maintain data integrity, and perform complex tasks based on changes to the data. There are two main types of triggers: "before" triggers and "after" triggers, which fire before or after the event or change occurs.
</blockquote>

</details>

---

12. What are SQL procedures?
<details><summary><b> Show Answer</b></summary>
  
<blockquote>
SQL procedures are a set of pre-written SQL codes that are saved in the database server. These procedures can be called and executed by applications or other database users. SQL procedures help in simplifying the development process by creating reusable code that can be called multiple times.
</blockquote>

</details>

---

13. What is a stored procedure?
<details><summary><b> Show Answer</b></summary>
  
<blockquote>
A stored procedure is a type of SQL procedure that is stored in the database server. Stored procedures are precompiled SQL codes that can be executed multiple times by different applications or users. They help in improving the performance of database applications by reducing network traffic and database overhead. Stored procedures can take input parameters, perform data manipulation operations, and return output values.
</blockquote>

</details>

---

14. How to check the performance of a stored procedure?
<details><summary><b> Show Answer</b></summary>
  
<blockquote>
There are different ways to check the performance of a stored procedure in SQL. Some of them are:

1. Using Execution Plan: Execution plan shows the performance of a stored procedure by displaying the query optimization and execution path. To view the execution plan of a stored procedure, use the "SET SHOWPLAN_TEXT" command or use the "Display Estimated Execution Plan" option in SQL Server Management Studio.

2. Using Profiler: SQL Server Profiler is a tool that helps in analyzing and monitoring the performance of SQL queries and stored procedures. You can use this tool to trace the stored procedure execution and identify any performance issues.

3. Using Execution Statistics: SQL Server provides execution statistics for stored procedures that show the performance details like execution time, CPU time, memory usage, and I/O usage. You can view the execution statistics using the "SET STATISTICS TIME ON" command or the "Include Actual Execution Plan" option in SQL Server Management Studio.
</blockquote>

</details>

---

15. What is the difference between a stored procedure and a function in SQL?
<details><summary><b> Show Answer</b></summary>
  
<blockquote>
  
A stored procedure is a set of precompiled SQL statements that perform a specific task or a series of tasks. It is used to encapsulate a set of operations that are frequently used together and can be called multiple times. Stored procedures can be called from within another SQL statement, such as a SELECT, INSERT, or UPDATE statement.

A function is a precompiled SQL statement that returns a single value or a table. Functions are usually used in the SELECT statement or as a part of a WHERE clause. Unlike a stored procedure, a function cannot modify the database state, and it can be used in a SQL expression.

</blockquote>

</details>

---


16. Where can we use SQL procedures?
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

17. How to write a stored procedure?
<details><summary><b> Show Answer</b></summary>
  
<blockquote>
  
To write a stored procedure in SQL, you can use the following syntax:

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
