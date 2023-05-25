24. What are the different multiplicity (cardinality) relationships? 

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Multiplicity is also known as cardinality defines the number of instances that can be associated between two entities. Here are the different types of multiplicity relationships:

- **One-to-One (1:1):** Each instance of one entity is associated with exactly one instance of another entity, and vice versa.

- **One-to-Many (1:N):** Each instance of one entity is associated with multiple instances of another entity, but each instance of the other entity is associated with only one instance of the first entity.

- **Many-to-One (N:1):** Multiple instances of one entity are associated with a single instance of another entity.

- **Many-to-Many (N:N):** Multiple instances of one entity can be associated with multiple instances of another entity through a junction table.

</blockquote>

</details>

---

75. How do you create a new Table from another Table, where just the structure of the table is copied but none of the rows?  

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>
<blockquote>

We can use the following  to create a new table with the same structure as an existing table but no data. It works for both *SQL and PostgreSQL*

```sql

CREATE TABLE new_table_name AS
SELECT *
FROM existing_table_name
WHERE 1 = 2;
```

- In this statement, new_table_name is the name you want to give to the new table, and existing_table_name is the name of the existing table whose structure you want to copy.

- The SELECT statement retrieves the column structure of the existing table, but the WHERE clause always evaluates to false, so no data is actually selected. This means that the new table will have the same columns as the existing table, but it will be empty.

</blockquote>

</details>

---