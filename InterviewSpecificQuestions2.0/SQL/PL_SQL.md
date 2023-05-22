## Technical

1. What is PL/SQL?

![Beginner](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- PL/SQL (Procedural Language/Structured Query Language) is a procedural extension of SQL used in Oracle Database.
-  It allows you to write blocks of code that can be executed as a single unit, making it useful for developing database applications.

  
</blockquote> 

</details>

---
2. What is the difference between SQL and PL/SQL?

![Beginner](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
    
- SQL (Structured Query Language) is a language used for interacting with databases, primarily for querying and manipulating data.
- PL/SQL, on the other hand, is a procedural language that extends SQL to include procedural constructs like loops, conditions, and exception handling. 
- PL/SQL allows you to write blocks of code for executing complex logic and implementing business rules within the database.
 
    
</blockquote> 

</details>

---
3. What are the different types of PL/SQL blocks?

![Beginner](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

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

![Beginner](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

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

![Beginner](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

 Cursors in PL/SQL allow you to retrieve and process multiple rows from a result set. There are two types of cursors:
-  implicit cursors (handled automatically by PL/SQL for queries) and
- explicit cursors (manually declared and used for more control).



</blockquote> 

</details>

---
6. Explain the Types of Cursors?

![Beginner](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

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

![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 
  
- Exceptions in PL/SQL are used for handling errors and exceptional conditions. They allow you to gracefully handle and recover from errors during program execution. 
- PL/SQL provides a set of predefined exceptions, and you can also define custom exceptions.


</blockquote> 

</details>

---
8. How do you handle exceptions in PL/SQL?

![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- Exceptions in PL/SQL can be handled using the EXCEPTION block. 
- You can specify specific exceptions to catch and handle or use a generic OTHERS exception to catch all other exceptions. 
- Additionally, you can use RAISE statement to raise custom exceptions.'

</blockquote> 

</details>

---
9. Mention a Few Predefined Exceptions

![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

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

![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- You can define a procedure in PL/SQL using the CREATE PROCEDURE statement. 
**For example:**
CREATE OR REPLACE PROCEDURE my_procedure IS
BEGIN
   -- code goes here
END;

- To call a procedure, you can simply use its name followed by parentheses. For example: my_procedure();

</blockquote> 

</details>

---
11. What do you know about the Commands COMMIT, ROLLBACK, and SAVEPOINT?

![Beginner](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>

<blockquote> 

- **COMMIT:** The COMMIT command saves changes to a database permanently during the current transaction.

**ROLLBACK:** The ROLLBACK command is used at the end of a transaction to undo any modifications made since the start of the transaction.

**SAVEPOINT:** The SAVEPOINT command saves the current point with a unique name during the processing of a transaction.