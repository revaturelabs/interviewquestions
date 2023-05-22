1. What are the different types of joins in SQL?
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
<details><summary><b> Show Answer</b></summary>
  
<blockquote>
In SQL, a join is used to combine rows from two or more tables based on a related column between them. A join is performed using the JOIN keyword and can be used to extract data from multiple tables as if they were a single table. The relationship between tables is usually defined by a foreign key constraint that specifies which columns in one table match which columns in another table.
</blockquote>

</details>

---

3. If there is no respective item I.E. a genre but no movie with that genre, what will happen to that genre?
<details><summary><b> Show Answer</b></summary>
  
<blockquote>
If there is no respective item, i.e., a genre but no movie with that genre, the genre will still be included in the result set, but the movie column values for that genre will be NULL. This is because the SQL engine still includes all rows from the first table (the one specified before the LEFT JOIN or RIGHT JOIN keyword) in the result set, regardless of whether there is a match in the second table (the one specified after the JOIN keyword).
</blockquote>

</details>

---

4. What is a cartesian join?
<details><summary><b> Show Answer</b></summary>
  
<blockquote>
A Cartesian join, also known as a cross join, is a join operation in SQL that returns the Cartesian product of two tables. In other words, it returns all possible combinations of rows from both tables, regardless of whether there is a matching value in the related columns. The result of a Cartesian join between two tables with n and m rows, respectively, is a table with n x m rows.
</blockquote>

</details>

---

5. Take a list of entries and make a second list of the unique elements from the first.
<details><summary><b> Show Answer</b></summary>
  
<blockquote>
To create a list of unique elements from a list of entries in SQL, you can use the DISTINCT keyword with the SELECT statement. Here is an example query that selects unique values from a table called 'mytable' with a column called 'mycolumn':

```sql
SELECT DISTINCT mycolumn FROM mytable;
```

This query will return a list of all unique values in the 'mycolumn' column of the 'mytable' table.
</blockquote>

</details>

---

6. What is a left outer join?
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

7. What is the difference between a Union and a Join in SQL? 
<details><summary><b> Show Answer</b></summary>
  
<blockquote>
A join in SQL combines rows from two or more tables based on a related column between them. It is used to extract data from multiple tables as if they were a single table. A union, on the other hand, combines rows from two or more SELECT statements into a single result set. The result set of a union operation contains all the rows from each SELECT statement, with duplicates removed.

In other words, a join combines columns from different tables into a single result set, while a union combines rows from different SELECT statements into a single result set.
</blockquote>

</details>

---

8. What are Outer Join and Full Outer Join?
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

9. What is a Cross Join?
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

10. Let's say you have two tables with a common column between them (primary key-foreign key), how do you join these tables so that each row says which table it comes from: Table A, Table B, or Both Tables?
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

11. How would you combine the data of two different SQL tables? 
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


12. How to write an SQL query (joins) for a database with 3 tables?
<details><summary><b> Show Answer</b></summary>
  
<blockquote>
To write an SQL query that joins 3 tables, you need to use multiple join operations. The specific type of join operation depends on the relationship between the tables and the data you want to extract. Here is an example of a query that joins 3 tables:

Suppose we have three tables, 'customers', 'orders', and 'order_details', with the following columns:

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

13. How to write an SQL query (joins)?
<details><summary><b> Show Answer</b></summary>
  
<blockquote>
To write an SQL query with joins, you need to specify the tables you want to join, the join conditions based on their relationships, the type of join operation you want to use, and the columns you want to retrieve using the SELECT statement.

Here are the basic steps to follow:

1. Identify the tables you want to join.
2. Determine the join conditions based on the relationships between the tables.
3. Choose the type of join operation you want to use (e.g., INNER JOIN, LEFT JOIN, RIGHT JOIN, FULL OUTER JOIN).
4. Specify the columns you want to retrieve using the SELECT statement.

For example, to join two tables 'students' and 'grades', you could use the following SQL query:

```sql
SELECT students.name, grades.subject, grades.grade
FROM students
INNER JOIN grades
ON students.id = grades.student_id;
```

This query retrieves the student name, subject, and grade for all matching rows between the 'students' and 'grades' tables, based on the join condition that the student ID in the 'students' table matches the student ID in the 'grades' table.
</blockquote>

</details>

---

14. Difference between INNER JOIN and FULL OUTER JOIN:
<details><summary><b> Show Answer</b></summary>
  
<blockquote>
INNER JOIN returns only the matching records from both tables while FULL OUTER JOIN returns all records from both tables along with the matching records.
</blockquote>

</details>

---

15. What is the difference between a right join and a left join?
<details><summary><b> Show Answer</b></summary>
  
<blockquote>
LEFT JOIN returns all records from the left table and matching records from the right table, while RIGHT JOIN returns all records from the right table and matching records from the left table.
</blockquote>

</details>

---

16. How can I join tables without a primary key?
<details><summary><b> Show Answer</b></summary>
  
<blockquote>
You can join tables without a primary key by using a common field between the tables as a join condition. However, this can result in slower query performance and potential data inaccuracies, so it is generally recommended to have a primary key for each table and use that as the join condition.
</blockquote>

</details>

---

17. What is the difference between a join and a join with a select statement?
<details><summary><b> Show Answer</b></summary>
  
<blockquote>
A join combines data from two or more tables based on a specified condition, while a join with a select statement involves joining a subquery with a table based on a specified condition. The subquery can be used to filter or aggregate data before joining it with the table.
</blockquote>

</details>

---

18. How to combine two tables with related data?
<details><summary><b> Show Answer</b></summary>
  
<blockquote>
You can combine two tables with related data by using a join statement that specifies the common field between the tables as the join condition. The most common type of join is an INNER JOIN, which returns only the matching records from both tables.
</blockquote>

</details>

---

19. What is an inner join?
<details><summary><b> Show Answer</b></summary>
  
<blockquote>
An inner join is a type of join in SQL that returns only the matching records from both tables based on a specified condition. The join condition is typically a shared column or set of columns between the tables.
</blockquote>

</details>

---

20. What is the condition for joining tables?
<details><summary><b> Show Answer</b></summary>
  
<blockquote>
The condition for joining tables is typically a shared column or set of columns between the tables. The join condition can be specified in the ON clause of the join statement, which defines how the tables are related to each other.
</blockquote>

</details>

---

21. Describe right join?
<details><summary><b> Show Answer</b></summary>
  
<blockquote>
A right join is a type of join in SQL that returns all records from the right table and matching records from the left table based on a specified condition. If there is no match in the left table, the result will contain NULL values for the left table columns.
</blockquote>

</details>

---

22. Outer join vs minus, cases of usage and syntax.
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

23. Intersect: cases of usage and syntax.
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

24. SQL right vs left outer joins
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

25. What is the difference between an inner join and a cartesian product?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Inner join returns the rows that have matching values in both tables based on the specified join condition. Cartesian product, on the other hand, returns the combination of all rows in both tables regardless of whether or not there is a match based on the join condition. It is also known as cross join, and can be generated by simply using the keyword "CROSS JOIN" between two tables.

</blockquote>

</details>

---