## Lambda

1. What is lambda function?

<details><summary> <b>Show Answer</b> </summary>
  
Lambda function is an anonymous function is a function that is defined without a name.Lambda functions can have any number of arguments but only one expression. The expression is evaluated and returned. Lambda functions can be used wherever function objects are required.

Syntax:
   lambda arguments: expression
  
**Example**:
```python
double = lambda x: x * 2
print(double(5))
```
**Output**:
10
</details>

2.Look at the code carefully and Predict the output of the following code.

<details><summary> <b>Show Answer</b> </summary>
  
```python
list = [1, 5, 4, 6, 8, 11, 3, 12]
new_list = list(filter(lambda x: (x%2 == 0) ,list))
print(new_list)
```
**Output**:
new_list = list(filter(lambda x: (x%2 == 0) ,list))
TypeError: 'list' object is not callable
  
</details>

3.
  
  
