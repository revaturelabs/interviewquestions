1. List the sublanguages of SQL with their commands.

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

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
2. While creating a table, how will you decide on the column that can be converted into primary key?

![Beginner](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

 
<details><summary> <b>Show Answer</b> </summary> 

> There are set of rules that we can follow while creating a primary key:  
> 1. A column must have unique values.
> 2. A column shouldn't contain any null value.
> 3. Only one primary key can be created for one table.
> 4. Columns that are of type number are recommended for the primary key columns.

</details>

--- 
3. Explain the different subsets of SQL?

 ![Beginner](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 

> In SQL, the Most common subsets are DDL, DML, DQL, DCL and TCL. 

> - DDL allows the user to `create`, `alter` and `drop` objects of the database.
> - DML allows the user to manipulate the data in the database using  `insert`, `update` and `delete` commands.
> - DQL allows the user to fetch the data from the database using `select` command.
> - DCL commands like `grant` and `revoke` gives or remove permission to the user on the database elements.
> - TCL commands are used to control the data transaction using `commit`, `rollback` and `savepoint`. 

</details>

---
