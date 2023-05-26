
# SQL Interview Questions With Answer




























33. Assume you are handling a "student" table in the database having id, name, age, state, and class fields. Your task is to fetch the records of those students who are from "Texas" state.

 ![Beginner](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
 
<details><summary> <b>Show Answer</b> </summary>

> 
```sql
select * from student 
where state = "Texas";
```

</details>

---

34. Tell a way about how to give a different name to a field while executing a select query?

 ![Beginner](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>

> We can use the `as` as an alias name for the column, for example:  
```sql
select Name as "First_name" from table_name;
```

</details>

---

35. Give one single query which includes, select, where, order by, group by, and having clauses in it.  

![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
 
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

36. In SQL, how will you give the count of the students from the student table whose name starts with 'H'.

![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
 
<details><summary> <b>Show Answer</b> </summary>

> 
```sql
select count(name) as Name_H_students from student
where name like 'H%';
```

</details>

---

37. Tell me about the ways through which we can search for a "string" pattern in SQL?

 ![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

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

38. Your boss has given you a work to find the details of the workers in "HR" deparment from the "Company" table whose salary ranges between 10000 and 50000.

![Beginner](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
 
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

   ![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>

> 
```sql
select * from department 
where year(joined) = 2022 and month(joined) = 2;
```
</details>

---


40. In a company there are 5 departments and in each department, there is one manager you have to get the employee id "emp_id" and "name" of those employees who are working for the Manager having "Manager_id" as 432.[ take the table name as Employee]

![Beginner](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

 
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

![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

   
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

![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

   
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

![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

   
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

   ![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

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

![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

   
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

   ![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

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

  ![Beginner](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>

> 
```sql
select * from student
where state in ["NY", "Florida", "Alaska"] 
and class in [ "9th", "10th", "11th", "12th"];
```

</details>

---

48. What is  Denormalization and  when do we go use it in SQL.

![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

   
<details><summary> <b>Show Answer</b> </summary>

> - Denormalization can be described as the process to get back from all the normalized forms in the table to add some redundant data to it.   
> - It is a good idea to denormalize the tables to do the fast retrieval
> - When there are multiple small tables and applying joins on those tables will be a costly operation.

</details>

---

49. What is the purpose of using SQL and what are its applications?

![Beginner](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
 
<details><summary> <b>Show Answer</b> </summary>

> SQL is used to interact with the data that are present in tabular form.  
> The applications of SQL are:
> - It is used as a backend of a front-end system to store its data in the database.
> - It permits a user or group of users to access the database.
> - It is used on web sites where a need for storing the data is required.
> - It is used in maintaining old data or historical data.


</details>

---

50. In SQL, what is a cross-join? Give a syntax.

   ![Beginner](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

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

   ![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>

> Yes, we can use the `inner join` without `on` condition in SQL as it is an optional condition in the inner join or joins. If used without one condition, it will generate the same output as `cross join`.

</details>

---

52. Is it possible to make a `cross join` work as an `inner join` in SQL.

![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


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

53.  How will you execute a self-join SQL?

 ![Beginner](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

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

54. Talk about joins and its types in SQL.

 ![Beginner](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

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

![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

   
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

![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

 
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

![Beginner](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

 
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

![Beginner](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

 
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

![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
 
<details><summary> <b>Show Answer</b> </summary>

> For replacing something in SQL select query we can use the `replace` function.  
```sql
select replace(full_name, " ", "-")
from employee;
```

</details>

---

60. what is the difference between union and full join in SQL?

   ![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>

> - Union joins the two-table data vertically, whereas full join joins the two table data horizontally.
> - There are more restrictions when using a union between two tables than using full join. 
> - Union will take only distinct values from both tables, whereas full join combines all the data from both tables. 

</details>

---

61. Imagine there are two tables’ Workers and Managers, where the Workers table has all the employee names along with the employee id who are working for the company and the Managers table has all the manager’s names along with the manager id of that company. Give one SQL query that will print the names of Workers who are also Managers.

![Beginner](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
 
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

 ![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

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
 
   ![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


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

 ![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)


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









75. Andrew wants to create an empty table as new_students that has the same structure as of students’ table. What query does he need to execute in order to create an empty table from the old table?

 ![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>

> 
```sql
create table new_students
like students;
```

</details>

---

76. How to fetch only records that are present in an even position in SQL?

![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

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

   ![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

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

 ![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)
  
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

  ![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

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

  ![Advance](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details><summary> <b>Show Answer</b> </summary>

> The relationship between the two tables is established by the primary key- the foreign key. This foreign key constraint is also called a referential integrity constraint. The value of the foreign key is derived from the primary key of another table.     
> In SQL there is two referential integrity constraint presents:  
> - Insert Constraint: That says, we cannot insert values in a foreign key table if the value is not present in the primary key table. 
> - Delete Constraint: That says, we cannot delete any value from the primary key table if the value is present in the foreign key table. 

</details>

---

81. Consider you have a company table in SQL. Give the details of those employee who are from Florida, NY and Texas state and earning salary more than 50000 and department is either Finance or Training.

  ![Intermediate](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

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
