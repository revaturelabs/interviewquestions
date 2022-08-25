
# SQL Interview Questions With Answer

1. What are the constraints SQL follows in all their databases tool?

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

2. How primary key contraint and unique key contraint both are different? 

<details><summary> <b>Show Answer</b> </summary> 

> In a table in SQL, there can be many columns that can be a unique key but only one primary key is allowed on one table. Primary key is a combination of unique key plus null constraint, whereas unique key has only unique constraint and it can be null.

</details>

---

3. When creating a table in SQL, you forget to make a column as primary key, then is there any possibility to create a primary key on that column or we have to delete the table from the database so that we can create a primary key while creating table?

<details><summary> <b>Show Answer</b> </summary> 

> We can add the primary key after the creation of table also, for that we can use the `alter` command that will add the primary key column to an existing table. There is no need to delete the table and recreate again in the database. Just we have to pass a query as:  
```
alter table table_name add primary key(column_name);
```
  
</details>

---

4. Suppose you want to create a student table having id, name, age and class as columns in it. Write down the query that will create that table in "school" database.

<details><summary> <b>Show Answer</b> </summary> 

> 
```
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

5. While creating a table how will you decide which column can be converted into primary key?

<details><summary> <b>Show Answer</b> </summary> 

> There are set of rules that we can follow while creating a primary key:  
> 1. A column must have unique values.
> 2. A column shouldn't contain any null value.
> 3. Only one primary key can be created for one table.
> 4. Columns that are of type number is recommended for primary key column.

</details>

---
