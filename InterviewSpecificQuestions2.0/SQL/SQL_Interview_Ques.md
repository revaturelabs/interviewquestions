
# SQL Interview Questions With Answer

1. What are the constraints SQL follows in all their databases tool?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

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

2. How are primary key constraints and unique key constraints different? 

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary> 

> In a table in SQL, there can be many columns that can be a unique key but only one primary key is allowed on one table. The primary key is a combination of unique key plus null constraint, whereas unique key has only unique constraint and it can be null.

</details>

---

3. When creating a table in SQL, you forget to make a column as the primary key, then is there any possibility to create a primary key on that column or do we have to delete the table from the database so that we can create a primary key while creating a table?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary> 

> We can add the primary key after the creation of the table also, for that we can use the `alter` command that will add the primary key column to an existing table. There is no need to delete the table and recreate it again in the database. Just we have to pass a query as:  
```sql
alter table table_name add primary key(column_name);
```
  
</details>

---

4. Suppose you want to create a student table having id, name, age and class as columns in it. Write down the query that will create that table in the "school" database.

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

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

5. While creating a table, how will you decide on the column that can be converted into primary key?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary> 

> There are set of rules that we can follow while creating a primary key:  
> 1. A column must have unique values.
> 2. A column shouldn't contain any null value.
> 3. Only one primary key can be created for one table.
> 4. Columns that are of type number are recommended for the primary key columns.

</details>

--- 

6. In SQL, what are the statements through which we can create a primary key in a table?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary> 

> By using `create table` and `alter table` statements we can create a primary key in a table in SQL. 

</details>

---

7. In SQL, what are the commands that are the part of Data Definition Language?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary> 

> Data Definition language or DDL commands are used to describe or define the structure of the database objects. In DDL, the following are the commands:  
> - create
> - alter
> - drop
> - truncate
> - comment
> - rename 

</details>

---

8. Is `drop` and `truncate` commands have the same usage in SQL?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary> 

> Both `drop` and `truncate` are part of DDL commands and also look similar while deleting records of the table in the database. But one major difference between both is that `drop` deletes all the records from the table as well as the table structure, whereas `truncate` will only delete all the records from the table but not the table structure. Also, the drop command can be used to delete the database, whereas truncate cannot be used to delete the database.

</details>

---

9. Suppose you have created a table called "student" with column fields as id, name, age, address and class. But now you want to rename the "id" column to "student_id", then how will you do that in SQL?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary> 

> Using `alter` command, we can rename the column name.  
```sql
alter table student 
rename column id to student_id;
```
> Here "id" column name is changed to "student_id" name.
</details>

---

10. How `rename` and `alter` command different from each other while renaming a table in SQL? 

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 

> `rename` command and `alter` both have similar working when renaming a table name in SQL except for the syntax. The only difference between both is that `rename` cannot be used to rename the temporary table, whereas `alter` command can rename a temporary table in SQL.

</details>

---

11. How normalization affects the performance in SQL?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary> 

> The main point to use the normalization forms in table data is to eliminate the repetition of data from it. So one thing we can do is say that it will guarantees the duplicate free data in the table. But achieving full normalization, it negatively affects the performance. 

</details>

---

12. Tell me the difference in 1nf, 2nf and 3nf forms of normalization

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 

> - In 1nf or 1st normal form, the composite attribute is converted into a single-value attribute. Each column must only have one single data entry in each row. 
> - In 2nf or 2nd normal form, the table should not have any partial dependency means the proper subset of the primary key shouldn't determine any non-prime attribute. 
> - In 3nf or 3rd normal form, there should not be any transitive dependency, which means non-prime attribute of the table should not be dependent on another non- prime attribute. 

</details>

---

13. Tell me about some of the benefits of normalization in SQL?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary> 

> - It is used to reduce or remove duplicates from the data.
> - To optimize storage space.
> - To prevent unwanted deletion of data.
> - To prevent data inconsistency.

</details>

---

14. Explain the different subsets of SQL?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary> 

> In SQL, the Most common subsets are DDL, DML, DQL, DCL and TCL. 

> - DDL allows the user to `create`, `alter` and `drop` objects of the database.
> - DML allows the user to manipulate the data in the database using  `insert`, `update` and `delete` commands.
> - DQL allows the user to fetch the data from the database using `select` command.
> - DCL commands like `grant` and `revoke` gives or remove permission to the user on the database elements.
> - TCL commands are used to control the data transaction using `commit`, `rollback` and `savepoint`. 

</details>

---

15. Create an "employee" table and make one primary key and one foreign key in it. 

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary> 

> 
```sql
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

16. Can a primary key and foreign key contain null? 

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary> 

> A primary key field in the table cannot contain null as a value. But that is not the case with a foreign key. A foreign key is used to stabilize a relation between two tables and it can contain a  null value.

</details>

---

17. Explain the anomalies and their types?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 

> Anomaly generally happens when the database is not constructed well and when the normalization concepts were not applied. There are 3 types of anomalies that cause a problem:  
> 1. insertion anomaly: This can happen when we are trying to insert the data into the table, and it is not allowed because some data is not present.
> 2. update anomaly: This will happen when we have duplicate data in the table and updating one of those data will not reflects toe other data and the end user has no idea which data is the correct one.
> 3. deletion anomaly: This will happen when the deletion of one data will cause other data to be deleted from the table as well.


</details>

---

18. Assume you have created one table as "emp" and now you want to change that table name to "employee" then what are the ways, in SQL, through which we can change the table name? 

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

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

19. Suppose Jack has created a table as "Food" with id and food_name field as varchar datatype. But now he wanted to change the datatype of id from varchar to int. What query he should write that will do his task?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary> 

> 
```sql
alter table Food 
modify column id int;
```

</details>

---

20. Tell the difference between `alter` and `update` in SQL 

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary> 

> - The `alter` command is a DDL command, whereas `update` is a DML command
> - The `alter` command is used to perform the operation on the structure level. On the other hand, `update` is used to perform an operation on the data level.
> - The `alter` command is used to modify the attribute of the table. The `update` command is used to modify the rows of the table.

</details>

---

21. Is `truncate` and `delete` both are the same command? 

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary> 

> No, `truncate` is a DDL command, used to delete all the records from the table. Whereas `delete` is a DML command, used to delete the records based on some condition as well as it can delete all the data from the table as well.

</details>

---

22. Give the syntax of `delete`, `truncate` and `drop` commands in SQL.

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary> 

> Syntax of `delete` 
```sql
delete from table_name where condition;
```
> Syntax of `truncate`
```sql
truncate table table_name;
```
> Syntax of `drop` 
```sql
drop table table_name;
```

</details>

---

23. Henry has created a table as "school" with id and name field and now he wants to insert 5 records into it. What query he has to use to insert the data into a table? 

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary> 

> He has to use the `insert` command for inserting the data:  
```sql
insert into school(id, name) values(01, "Jack");
insert into school(id, name) values(02, "Henry");
insert into school(id, name) values(03, "Tom");
insert into school(id, name) values(04, "Tim");
insert into school(id, name) values(05, "EVE");
```

</details>

---

24. After inserting some of the documents into the "school" table, Tom wants to update the name of one student to EVA where id is 05. Write the query for it.

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary> 

> 
```sql
update school
set name = "EVA" 
where id = 05;
```

</details>

---

25. A user has to remove all of the data from the "order" table without removing the structure of the table. What query he has to write for this? 

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary> 

> He can use `delete from` statement or `truncate table` statement to delete all the records from the table.
```sql
delete from order;
truncate table order;
```


</details>

---

26. Let's imagine Amazon Prime no longer wishes to rent out the "Blue" movie and its movie id is 20. As an intern of Amazon company, what query you will write to remove that movie from the "movies" table?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary> 

>
```sql
delete from movies where id =20; 
```

</details>

---

27. Is the command line the only way to interact with SQL?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary> 

> No, the Command line is one of the ways through which we can interact with SQl, but there are 2 main ways also apart from the command line:  
> - using the web interface.
> - Through a programming language.

</details>

---

28. From someone you have heard about creating indexes in SQL will be better in terms of fast retrieval of data. Then, how will you create an index in a table? 

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary> 

> 
```sql
alter table Table_name
add index(column_name);
```

</details>

---

29. You have 4 indexes in your table "order" but now you want to remove one index named "author_id" from it. For the same task what will be your query for it?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary> 

> 
```sql
alter table order
drop index author_id;
```

</details>

---

30. Have you heard about BLOB in SQL?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary> 

> BLOB is a sub-type of string datatype in SQL and stands for a binary large object. It is used for a large amount of data like documents, images, etc. They are three types:  
> - TINYBLOB
> - MEDIUMBLOB
> - LONGBLOB

</details>

---

31. Tim is asking you to add him as a user in SQL so that he can access and manage the database. So, how will you add them?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>

> To add a user in SQL, we can use the `create user` statement.  
```sql
create user 'Tim' identified by 'password';
```


</details>

---

32. In SQL, how will you see the databases and tables that you have in that database?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary>

> - To list the databases we can use the `show databases;` 
> - To list the tables in a particular database, write:
```sql
use database_name;

show tables;
``` 

</details>

---

33. Assume you are handling a "student" table in the database having id, name, age, state, and class fields. Your task is to fetch the records of those students who are from "Texas" state.

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary>

> 
```sql
select * from student 
where state = "Texas";
```

</details>

---

34. Tell me the way about how to give a different name to a field while executing a select query?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary>

> We can use the `as` as an alias name for the column, for example:  
```sql
select Name as "First_name" from table_name;
```

</details>

---

35. Give one query to me which includes, select, from, where, order by, group by, and having clauses.  

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

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

36. In SQL, how will you give the count of those students from the student table whose name starts with 'H'.

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary>

> 
```sql
select count(name) as Name_H_students from student
where name like 'H%';
```

</details>

---

37. Tell me about the ways through which we can search for a "string" pattern in SQL?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

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

38. Your boss has given you a work to find the details of those workers from the "Company" table whose salary lies between 10000 and 50000 and the department is 'HR'

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary>

> 
```sql
select * from company
where salary between 10000 and 50000 
and department = "HR";
```

</details>

---

39. Imagine you are handling a "company" database which has one table as "department" and your manager is asking you to give the details of those employees who joined in January of 2022.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary> <b>Show Answer</b> </summary>

> 
```sql
select * from department 
where year(joined) = 2022 and month(joined) = 2;
```
</details>

---


40. In a company there are 5 departments and in each department, there is one manager you have to get the employee id "emp_id" and "name" of those employees who are working for the Manager having "Manager_id" as 432.[ take the table name as Employee]

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary>

> 
```sql
select emp_id, name
from Employee
where Manager_id = 432;
```


</details>

---

41. From "employee" table give the "names" and "emp_id" of those employees who receive a higher salary than the employee with "emp_id" = 101.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
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

42. Suppose you are having a "employee" table, in which you are trying to find out those employee’s details having the same department as the employee whose id is 121.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary> <b>Show Answer</b> </summary>

> 
```sql
select * from employee
where department = 
( select department 
from employee
where id = 121
);
```

</details>

---

43. In an employee table, how will you find those employee’s name and emp_id whose salary matches the lowest salary of any of the departments in SQL?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
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

44. In SQL, give the count of those employees who is getting a salary more than the average salary from "employee" table.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
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

45. Suppose you are handling two tables, one is an employee table and another one is a department table and there is a primary-foreign key relationship between both. Assume your boss asked you to give the emp_id and name of those employees who works in the product department. 

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary> <b>Show Answer</b> </summary>

> 
```sql
select e.name , e.id from employee e , department d
where e.id = d.id
and d.department = "product"
```

</details>

---

46. In an "employee" table , give me the query that will fetch the employee detail of those employees who are getting the second highest salary in the company. 

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary> <b>Show Answer</b> </summary>

> 
```sql
select * from employee
where salary in 
( select max(salary) from employee
where salary not in 
( select max(salary) from employee
);
```
</details>

---

47. Write a SQL query that will give the details of those students, from the student table, who comes from NY, Florida and Alaska state and who are from 9th, 10th, 11th and 12th class. 

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary>

> 
```sql
select * from student
where state in ["NY", "Florida", "Alaska"] 
and class in [ "9th", "10th", "11th", "12th"];
```

</details>

---

48. Tell me about Denormalization and when can we go for it in SQL.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary> <b>Show Answer</b> </summary>

> - Denormalization can be described as the process to get back from all the normalized forms in the table to add some redundant data to it.   
> - It is a good idea to denormalize the tables to do the fast retrieval
> - When there are multiple small tables and applying joins on those tables will be a costly operation.

</details>

---

49. Where SQL language is used and what are its applications?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary>

> SQL is used to interact with the data that are present in tabular form.  
> The applications of SQL are:
> - It is used as a backend of a front-end system to store its data in the database.
> - It permits a user or group of users to access the database.
> - It is used on web sites where a need for storing the data is required.
> - It is used in maintaining old data or historical data.


</details>

---

50. In SQL, what is a cross-join? Give syntax.

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  
  
<details><summary> <b>Show Answer</b> </summary>

> `cross join` also known as `cartesian join`, is used to join each tuple of the 1st table with each tuple of 2nd table. 
> Syntax of cross join:  
```sql
select column_names from table1 
cross join table2 ;
```

</details>

---

51. Can we use `inner join` without the `on` condition?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary> <b>Show Answer</b> </summary>

> Yes, we can use the `inner join` without `on` condition in SQL as it is an optional condition in the inner join or joins. If used without one condition, it will generate the same output as `cross join`.

</details>

---

52. Is it possible to make a `cross join` work as an `inner join` in SQL.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)  

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

53. How will you execute a self-join SQL?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary>

> A self-join can be executed by joining the table to itself. for example: 
```SQL
select t1.name, t1.id
from table1 t1
join table1 t2 
on t1.id = t2.emp_id;
```

</details>

---

54. Tell me about the joins in SQL and their types.

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary>

> Joins, in SQL, are useful to combine records of two or more different tables. 
> We have various types of joins like:  
> - Inner Join: After join, it returns matching rows of both tables only.
> - Outer Join: After join, it returns matching rows of both the tables plus left out rows of left table and right table.
> - left Join: It returns matching rows of both the tables plus left out rows from the left table.
> - right Join: It returns matching rows of both the tables plus left out rows from the right table.

</details>

---

55. Give the query that will display the total marks of all the students by adding mid-term and final_term marks. return name and roll_no also.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary> <b>Show Answer</b> </summary>

> 
```sql
select name, roll_no,
mid_term + final_term as Total_marks
from student;
```

</details>

---

56. Imagine you have two tables, "customers" and "orders" and you have to find all customers who placed 0 or more orders. How will you do that in SQL?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>

> Using `left join` we can find the details of all the customers who placed 0 or more orders.  
```SQL
select customer_number, name
from customers
left join orders 
on orders.customer_number = customer_number;
```

</details>

---

57. Assume, you have two tables’ "customers" and "orders". So, tell me how will you execute the right join between both tables?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

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

58. In SQL, suppose you are handling two tables, "customers" and "orders", how would you execute the outer join between both tables?

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary>

> Suppose we are taking customer names and order_id from both tables while doing the full join.    
```SQL
select customers.name, orders.order_id
from customers
full join orders
on customers.id = orders.order_id;
```

</details>

---

59. Give the query in SQL that will replace the space with '-' in full name from the employee table.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>

> For replacing something in SQL select query we can use the `replace` function.  
```sql
select replace(full_name, " ", "-")
from employee;
```

</details>

---

60. Tell the difference between union and full join in SQL?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary> <b>Show Answer</b> </summary>

> - Union joins the two-table data vertically, whereas full join joins the two table data horizontally.
> - There are more restrictions when using a union between two tables than using full join. 
> - Union will take only distinct values from both tables, whereas full join combines all the data from both tables. 

</details>

---

61. Imagine there are two tables’ Workers and Managers, where the Workers table has all the employee names along with the employee id who are working for the company and the Managers table has all the manager’s names along with the manager id of that company. Give one SQL query that will print the names of Workers who are also Managers.

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary>

> 
```sql
select Workers.name from Workers
inner join Managers
on Workers.empID = Managers.managerID;
```

</details>

---

62. Assume you have a Worker table having columns like name, id, department, salary, address, etc. How will you find the number of workers in each department in descending order?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>

> 
```sql
select department, count(id) as number_of_emp 
from Worker
group by department
order by number_of_emp desc;
```

</details>

---

63. When managing a contact_details table in SQL, you found out that some of the records are duplicates and now you want to see the duplicate records only in your result set. What select query you will write for this that will fetch you the duplicate records? In contact_details table, columns are phoneNo, name, etc. 
 
![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
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

64. When managing a contact_details table in SQL, you found out that some of the records are duplicates and now you want to delete those duplicate records only so that only distinct records are leftout in your table. Give the query for this that will delete the duplicate records. In contact_details table, columns are phoneNo, name, id etc. 

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

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

65. In an employee table, the monthly salary is given to each employee. Your task is to find and fetch the annual salary of employees with their names.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>

> 
```sql
select name, 
monthly_salary * 12 as "annual_salary"
from employee;
```

</details>

---

66. In SQL, how will you get the last 3 records from the table "worker" having one unique column id.

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

<details><summary> <b>Show Answer</b> </summary>

>
```sql
select * from worker
order by id desc
limit 3;
```

</details>

---

67. I have a table called employee in SQL and now I want to create another table as employee_2 that has the same structure and data as the employee table. How can I do this?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
<details><summary> <b>Show Answer</b> </summary>

>
```sql
create table employee_2 
select * from employee;
```

</details>

---

68. In SQL, how will you display the first 50% of the records of any table?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>

>
```sql
select * from table_name
limit (select count(*)/2 from table_name);
```

</details>

---

69. Assume you have an employee table which stores the details of all employees and one department table which stores the department information, and both these tables have a primary-foreign key relationship, where emp_id of the employee table is a primary key and dept_id of the department table is a foreign key. Your boss has given you the task of fetching the details of those employees who have not been assigned any department yet. How will you do that?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
<details><summary> <b>Show Answer</b> </summary>

> 
```sql
select * from employee
where emp_id not in (
select dept_id from department);
```

</details>

---

70. Without using the distinct keyword, how will you get the distinct records from the table in SQL?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
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
 
71. In SQL, what are the points anyone has to keep in mind when using `group by` clause in SQL?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>

> Points to remember when using `group by` clause:  
> - Use `group by` clause with a select query
> - If `where` clause is used in the query, `group by` clause must be placed after it.
> - If `order by` clause is used in the query, `group by` clause must be placed before it.
> - Columns mentioned in the select query should either be part of the group by clause or an aggregation function is applied to those columns. 

</details>

---

72. Display the name and id of those employees from the employee table whose salary is greater than 40000 and DOJ in 2019.

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

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

73. In a student table, how you will find the count of repeated rows in SQL?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

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

74. In SQL, give a generalized query that will fetch the top N records from the table

![Simple](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)  

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

75. Andrew wants to create an empty table as new_students that has the same structure as of students’ table. What query does he need to execute in order to create an empty table from the old table?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>

> 
```sql
create table new_students
like students;
```

</details>

---

76. How to fetch only records that are present in an even position in SQL?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
  
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

77. Can we use `join` to join more than 2 tables in SQL? If yes, then give a query for it as an example.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
 
<details><summary> <b>Show Answer</b> </summary>

> Yes, we can join more than 2 tables with `join`.  
```sql
select column1 
from table1
join table2
on table1.column2 = table2.column2
join table3
on table1.column3 = table3.column3;
```

</details>

---

78. Let's say you have two tables, one is an employee which has employee details like id, name, etc and another one is a salary table having columns like id, salary, etc. Give the query in SQL which will return the employee’s name, id and salary of those employees. Also, display the name and id of those employees even if salary details are not present.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)
 
<details><summary> <b>Show Answer</b> </summary>

>
```sql
select e.id, e.name, s.salary
from employee e 
left join salary s
on e.id = s.id;
```


</details>

---

79. In SQL, give the query that will fetch the records of those employees who are from the product department and assigned to one project. [Consider two tables employee and project, which has the same column as id] 

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>

>
```sql
select * from employee
where department = "product" 
and employee.id in ( 
select id from project);
```

</details>

---

80. Explain referential integrity constraint in SQL.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>

> The relationship between the two tables is established by the primary key- the foreign key. This foreign key constraint is also called a referential integrity constraint. The value of the foreign key is derived from the primary key of another table.     
> In SQL there is two referential integrity constraint presents:  
> - Insert Constraint: That says, we cannot insert values in a foreign key table if the value is not present in the primary key table. 
> - Delete Constraint: That says, we cannot delete any value from the primary key table if the value is present in the foreign key table. 

</details>

---

81. Consider you have a company table in SQL. Give the details of those employee who are from Florida, NY and Texas state and earning salary more than 50000 and department is either Finance or Training.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

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
