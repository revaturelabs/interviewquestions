## Technical

1. What is PL/SQL?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- PL/SQL (Procedural Language/Structured Query Language) is a procedural extension of SQL used in Oracle Database.
-  It allows you to write blocks of code that can be executed as a single unit, making it useful for developing database applications.

  
</blockquote> 

</details>

---
2. What is the difference between SQL and PL/SQL?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- SQL (Structured Query Language) is a language used for interacting with databases, primarily for querying and manipulating data.
- PL/SQL, on the other hand, is a procedural language that extends SQL to include procedural constructs like loops, conditions, and exception handling. 
- PL/SQL allows you to write blocks of code for executing complex logic and implementing business rules within the database.
 
    
</blockquote> 

</details>

---
3. What are the different types of PL/SQL blocks?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
PL/SQL supports three types of blocks:
**Anonymous blocks:** Unnamed blocks of code that can be executed directly.
**Named blocks:** Blocks of code defined using a name and can be stored in the database for reuse.
**Subprograms:**  Named blocks of code that can be called from other PL/SQL blocks. Subprograms include procedures, functions, and packages.


</blockquote> 

</details>

---
4. How do you declare variables in PL/SQL?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- You can declare variables in PL/SQL using the DECLARE keyword. 

**For example:**

DECLARE
   emp_name VARCHAR2(100);
   emp_id NUMBER(10);
BEGIN
   -- code goes here
END;

</blockquote> 

</details>

---
5. What are cursors in PL/SQL?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

 Cursors in PL/SQL allow you to retrieve and process multiple rows from a result set. There are two types of cursors:
-  implicit cursors (handled automatically by PL/SQL for queries) and
- explicit cursors (manually declared and used for more control).


</blockquote> 

</details>

---
6. Explain the Types of Cursors?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

-There are two types of cursors:

**Implicit Cursor:** When PL/SQL executes an SQL statement, it automatically constructs a cursor without specifying one; these cursors are known as implicit PL/SQL uses implicit cursors for the following statements:
- INSERT
- UPDATE
- DELETE
- SELECT

**Explicit Cursor:** A programmer declares and names an explicit cursor for the queries that return more than one row. An explicit cursor is a SELECT statement that is declared explicitly in the current block’s declaration section or in a package definition. The following are the commands that are used for explicit cursors in PL/SQL:
- OPEN
- FETCH
- CLOSE

</blockquote> 

</details>

---
7. What is an exception in PL/SQL?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
  
- Exceptions in PL/SQL are used for handling errors and exceptional conditions. They allow you to gracefully handle and recover from errors during program execution. 
- PL/SQL provides a set of predefined exceptions, and you can also define custom exceptions.


</blockquote> 

</details>

---
8. How do you handle exceptions in PL/SQL?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- Exceptions in PL/SQL can be handled using the EXCEPTION block. 
- You can specify specific exceptions to catch and handle or use a generic OTHERS exception to catch all other exceptions. 
- Additionally, you can use RAISE statement to raise custom exceptions.'

</blockquote> 

</details>

---
9. Mention a Few Predefined Exceptions

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

The following are some examples of predefined exceptions:

**NO DATA FOUND:** A single-row SELECT statement that returns no data
**TOO MANY ROWS:** A single row SELECT statement that returns many rows
**INVALID CURSOR:** An incorrect cursor operation is performed
**ZERO DIVIDE:** An attempt at zero division
</blockquote> 

</details>

---
10. How do you define and call a procedure in PL/SQL?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- You can define a procedure in PL/SQL using the CREATE PROCEDURE statement. 
**For example:**

```sql

CREATE OR REPLACE PROCEDURE my_procedure IS
BEGIN
   -- code goes here
END;

```
- To call a procedure, you can simply use its name followed by parentheses. For example: my_procedure();

</blockquote> 

</details>

---
11. What do you know about the Commands COMMIT, ROLLBACK, and SAVEPOINT?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

**COMMIT:** The COMMIT command saves changes to a database permanently during the current transaction.

**ROLLBACK:** The ROLLBACK command is used at the end of a transaction to undo any modifications made since the start of the transaction.

**SAVEPOINT:** The SAVEPOINT command saves the current point with a unique name during the processing of a transaction.

</blockquote> 

</details>

---

12. Explain the difference between a stored procedure and a function in PL/SQL.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- A stored procedure in PL/SQL is a named block of code that can be invoked using its name. It is primarily used to perform an action or a series of actions and may or may not return a value.

- A function in PL/SQL is also a named block of code, but it must return a value. It is used to perform a specific computation or operation and return the result to the caller.

</blockquote> 

</details>

---

13. What is a PL/SQL record? How is it different from a database table?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- A PL/SQL record is a composite data type that can hold multiple values of different data types. It is similar to a row in a database table but does not have a fixed structure like a table.

</blockquote> 

</details>

---

14. Explain the difference between a cursor and a cursor variable in PL/SQL.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- A cursor in PL/SQL is a named control structure that allows you to process a result set returned by a query. It is static and needs to be explicitly declared and opened.
- A cursor variable, also known as a REF CURSOR, is a data type that allows dynamic fetching of query results. It can be used to pass result sets between PL/SQL blocks or store them in variables.

</blockquote> 

</details>

---

15. How do you handle NULL values in PL/SQL?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- A cursor in PL/SQL is a named control structure that allows you to process a result set returned by a query. It is static and needs to be explicitly declared and opened.
- A cursor variable, also known as a REF CURSOR, is a data type that allows dynamic fetching of query results. It can be used to pass result sets between PL/SQL blocks or store them in variables.

</blockquote> 

</details>

---

16. What are PL/SQL triggers? How are they used?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- PL/SQL triggers are stored programs that are automatically executed or fired in response to specific events or changes in the database.
- Triggers can be used to enforce data integrity rules, perform auditing or logging, or automate complex business logic.

</blockquote> 

</details>

---

17. What are the advantages of using PL/SQL records over the %ROWTYPE attribute?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- PL/SQL records allow you to define custom data structures with specific fields, while %ROWTYPE attribute automatically creates a record type that matches a table's structure. The advantages of using records include flexibility, reusability, and improved code readability.

</blockquote> 

</details>

---
18. Explain the difference between a PL/SQL package and a standalone procedure or function.

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- A PL/SQL package is a named container that includes one or more procedures, functions, variables, and cursors. 
- It provides a modular and organized approach to code implementation. In contrast, a standalone procedure or function is not contained within a package and is typically used for smaller, isolated tasks.

</blockquote> 

</details>

---

19. Explain the difference between a database trigger and a PL/SQL trigger.

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- A database trigger is a trigger defined at the database level and is executed automatically when a specified event occurs. 
- On the other hand, a PL/SQL trigger is a trigger defined within a PL/SQL block and is executed explicitly as part of the PL/SQL code.

</blockquote> 

</details>

---

20. What are autonomous transactions in PL/SQL? When and why would you use them?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

-  Autonomous transactions in PL/SQL are independent transactions that are not affected by the main transaction. 
- They are useful when you need to perform actions that are independent of the main transaction, such as logging or auditing. Autonomous transactions are created using the PRAGMA AUTONOMOUS_TRANSACTION directive.

</blockquote> 

</details>

---

21. How do you handle bulk data processing in PL/SQL?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

-  Bulk data processing in PL/SQL can be achieved using bulk operations such as BULK COLLECT and FORALL.
-  BULK COLLECT allows you to fetch multiple rows at once into a collection, while FORALL allows you to perform DML operations on a collection of data in a single statement, improving performance.

</blockquote> 

</details>

---

22. How do you write a basic SELECT statement in PL/SQL?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

```sql
DECLARE
   variable_name data_type;
BEGIN
   SELECT column_name INTO variable_name FROM table_name WHERE condition;
END;

```

</blockquote> 

</details>

---

23. Consider that we are fetching details of employees from ib_employee table where salary is a parameter for filter.Write a PL/SQL procedure for selecting some records from the database using some parameters as filters.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

```sql

CREATE PROCEDURE get_employee_details @salary nvarchar(30)
AS
BEGIN
   SELECT * FROM ib_employee WHERE salary = @salary;
END;


```

</blockquote> 

</details>

---

24. What is the difference between a mutating table and a constraining table?

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- A table that is being modified by the usage of the DML statement currently is known as a mutating table. It can also be a table that has triggers defined on it.
- A table used for reading for the purpose of referential integrity constraint is called a constraining table

</blockquote> 

</details>

---

25. In what cursor attributes the outcomes of DML statement execution are saved?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

The outcomes of the execution of the DML statement is saved in the following 4 cursor attributes:
- **SQL%FOUND:** This returns TRUE if at least one row has been processed.
- **SQL%NOTFOUND:** This returns TRUE if no rows were processed.
- **SQL%ISOPEN:** This checks whether the cursor is open or not and returns TRUE if open.
- **SQL%ROWCOUNT:** This returns the number of rows processed by the DML statement.

</blockquote> 

</details>


---