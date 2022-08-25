
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

6. In SQL, what are the statements through which we can create a primary key in a table.

<details><summary> <b>Show Answer</b> </summary> 

> By using `create table` and `alter table` statements we can create a primary key in a table in SQL. 

</details>

---

7. In SQL, What are the commands that are the part of Data Definition Language?

<details><summary> <b>Show Answer</b> </summary> 

> Data Definition language or DDL commands are used to describe or define the structure of the database objects. In DDL, following are the commands:  
> - create
> - alter
> - drop
> - truncate
> - comment
> - rename 

</details>

---

8. Is `drop` and `truncate` commands have the same usage in SQL?

<details><summary> <b>Show Answer</b> </summary> 

> Both `drop` and `truncate` are the part of DDL commands and also looks similar while deleting records of the table in database. But one major difference between both is that, `drop` deletes all the records from the table as well as the table structure, whereas `truncate` will only deletes all the records from the table but not the table structure. Also drop command can be used to delete the database, whereas truncate cannot be used to delete database.

</details>

---

9. Suppose you have created a table called as "student" with column fields as id, name, age, address and class. But now you want to rename the "id" column to "student_id", then how will you do that in SQL?

<details><summary> <b>Show Answer</b> </summary> 

> Using `alter` command, we can rename the column name.  
```
alter table student 
rename column id to student_id;
```
> Here "id" column name is changed to "student_id" name.
</details>

---

10. How `rename` and `alter` command different from each other while renaming a table in SQL? 

<details><summary> <b>Show Answer</b> </summary> 

> `rename` command and `alter` both have similar working when renaming a table name in SQL except for the syntax. The only difference between both of them are that `rename` cannot be used to rename temporary table, whereas `alter` command can rename a temporary table in SQL.

</details>

---

11. How normalization affects the performance in SQL?

<details><summary> <b>Show Answer</b> </summary> 

> The main point to use the normalization forms in table data is to eliminate repetition of data from it. So one thing we can say that it will guarantees the duplicate free data in the table. But achiving full normalization can affects negitively in the performance. 

</details>

---

12. Tell me the difference in 1nf, 2nf and 3nf forms of normalization

<details><summary> <b>Show Answer</b> </summary> 

> - In 1nf or 1st normal form, the composite attribute are converted into single value attribute. Each column must only have one single data entry in each row. 
> - In 2nf or 2nd normal form, the table should not have any partial dependency means the proper subset of primary key shouldn't determines any non-prime attribute. 
> - In 3nf or 3rd normal form, there should not be any transitive dependency, that means non- prime attribute of the table should not dependent on other non- prime attribute. 

</details>

---

13. Tell me about some of the benifits of normalization in SQL?

<details><summary> <b>Show Answer</b> </summary> 

> - It is used to reduce or remove the duplicates from the data.
> - To optimize storage space.
> - To prevent unwanted deletion of data.
> - To prevent data inconsistency.

</details>

---

14. explain the different subsets of SQL?

<details><summary> <b>Show Answer</b> </summary> 

> In SQL, Most common subsets are DDL, DML, DQL, DCL and TCL. 

> - DDL allows user to `create`, `alter` and `drop` objects of the database.
> - DML allows user to manipulate the data in database using  `insert`, `update` and `delete` commands.
> - DQL allows user to fetch the data from the database using `select` command.
> - DCL commands like `grant` and `revoke` gives or removes permission to the user on the database elements.
> - TCL commands are used to control the data transaction using `commit`, `rollback` and `savepoint`. 

</details>

---

15. Create an "employee" table and make one primary key and one foreign key in it. 

<details><summary> <b>Show Answer</b> </summary> 

> 
```
create table employee(
       emp_id int,
       emp_name varchar(20),
       dept_id int,
       primary key (emp_id),
       foreign key (dept_id) references department(dept_id)
       );
```

</details>

---

16. Can a primary key and foreign key contains null? 

<details><summary> <b>Show Answer</b> </summary> 

> A primary key field in the table cannot contains null as a value. But that is not the case with foreign key. A foreign key is used to stablize a relation between two tables and it can contain null value.

</details>

---

17. Explain about the anomalies and its types?
 
<details><summary> <b>Show Answer</b> </summary> 

> Anomaly generally happens when the database is not constructed well and when the normalization concepts were not applied. There are 3 types of anomalies that causes problem:  
> 1. insertion anomaly: This can happen when we are trying to insert the data into the table and it is not allowed because some data is not present.
> 2. update anomaly: This will happen when we have duplicate data into the table and updating one of those data will not reflects to the other data and the end user has no idea which data is the correct one.
> 3. deletion anomaly: This will happen when deletion of one data will cause other data to be deleted from the table as well.


</details>

---

18. Assume you have created one table as "emp" and now you want to change that table name to "employee" then what are the ways, in SQL, through which we can chnage the table name? 

<details><summary> <b>Show Answer</b> </summary> 

> For changinf the table name in SQL, we can go for `rename` command or `alter` command:    
With `rename`
```
rename table emp to employee;
```
With `alter`
```
alter table emp
rename to employee; 
```

</details>

---

19. Suppose Jack has created a table as "Food" with id and food_name field as varchar datatype. But now he wanted to change the datatype of id from varchar to int. What query he should write that will do his task?

<details><summary> <b>Show Answer</b> </summary> 

> 
```
alter table Food 
modify column id int;
```

</details>

---

20. Tell the difference between `alter` and `update` in SQL 

<details><summary> <b>Show Answer</b> </summary> 

> - The `alter` command is a DDL command, whereas `update` is a DML command
> - The `alter` command is used to perform the operation on the structure level. On the other hand, `update` is used to perform operation on the data level.
> - The `alter` command is used to modify the attribute of table. The `update` command is used to modify the rows of the table.

</details>

---

21. Is `truncate` and `delete` both are same command? 

<details><summary> <b>Show Answer</b> </summary> 

> No, `truncate` is a DDL command, used to delete all the records from the table. Whereas `delete` is a DML command, used to delete the records based on the some condition as well as it can delete all the data from the table as well.

</details>

---

22. Give the syntax of `delete`, `truncate` and `drop` command in SQL.

<details><summary> <b>Show Answer</b> </summary> 

> Syntax of `delete` 
```
delete from table_name where condition;
```
> Syntax of `truncate`
```
truncate table table_name;
```
> Syntax of `drop` 
```
drop table table_name;
```

</details>

---

23. Henry has created a table as "school" with id and name field and now he wants to insert 5 records to it. What query he has to use to insert the data into a table? 

<details><summary> <b>Show Answer</b> </summary> 

> He has to use the `insert` command for inserting the data:  
```
insert into school(id, name) values(01, "Jack");
insert into school(id, name) values(02, "Henry");
insert into school(id, name) values(03, "Tom");
insert into school(id, name) values(04, "Tim");
insert into school(id, name) values(05, "EVE");
```

</details>

---

24. After inserting some of the documents into the "school" table, Tom wants to update the name of one student to EVA where id is 05. Write the query for it.

<details><summary> <b>Show Answer</b> </summary> 

> 
```
update school
set name = "EVA" 
where id = 05;
```

</details>

---

25. A user has to remove all of the data from the "order" table without removing the structure of the table. What query he has to write for this? 

<details><summary> <b>Show Answer</b> </summary> 

> He can use `delete from` statement or `truncate table` statement to delete all the records form the table.
```
delete from order;
truncate table order;
```


</details>

---

26. Let's imagine The Amazone Prime no longer wishes to renting out the "Blue" movie and its movie id is 20. As a intern of Amazone company what query you will write to remove that movie from the "movies" table?

<details><summary> <b>Show Answer</b> </summary> 

>
```
delete from movies where id =20; 
```

</details>

---

27. Is command line the only way to interact with SQL?

<details><summary> <b>Show Answer</b> </summary> 

> No, Command line is one of the ways through which we can interact with SQl, but there are 2 main ways also apart from command line:  
> - using web interface.
> - Through a programming language.

</details>

---

28. From someone you have heard about creating indexes in SQL will be more good in terms of fast retrival of data. Then how will you create a index into a table? 

<details><summary> <b>Show Answer</b> </summary> 

> 
```
alter table Table_name
add index(column_name);
```

</details>

---

29. You have 4 indexes into your table "order" but now you wants to remove one index named as "author_id" from it. For the same task what will be your query for it?

<details><summary> <b>Show Answer</b> </summary> 

> 
```
alter table order
drop index author_id;
```

</details>

---

30. Have you heared about BLOB in SQL?

<details><summary> <b>Show Answer</b> </summary> 

> BLOB is a sub-type of string datatype in SQL and is stands for binary large object. It is used to large amount of data like documents, images, etc.  

</details>

---




