47.  How do you sort data after it has been pulled from a database?

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

48.  How to change an entry to null in sql ?

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

56. How do you delete duplicate record with no key or timestamp.

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

58. How can you calculate the total amount for each month using the SQL CASE statement along with aggregation functions?

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

59. What is the use of  "Merge" Command in SQL ?

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

68. How would you do a SQL call for employees with a salary over 150K?

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
1. What is difference between Table and View in SQL?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

A `table` in SQL is a database object that stores data in `rows` and `columns`, whereas a `view` in SQL is a virtual table that does not store data physically but presents data from one or more tables in a structured manner. 

</blockquote>

</details>

---
2. What is a View?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

A `view` in SQL is a virtual table that does not store data physically but presents data from one or more tables in a structured manner. `Views` are used to simplify complex queries, hide the complexity of underlying tables, and restrict access to certain data for security purposes.

</blockquote>

</details>

---
3. Does a view contain any data in it?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

No, a `view` does not contain any data in it. It is a virtual table that presents data from one or more tables in a structured manner. The data in a `view` is stored in the underlying `tables` and is retrieved and presented by the `view` as if it were a table.

</blockquote>

</details>

---
