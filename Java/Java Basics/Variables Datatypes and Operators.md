## Variables, Datatypes and Operators

1: Explain the difference between primitive datatype and non-primitive datatype.
<details>
  <summary> Show Answer </summary>

- Primitive datatypes are prefined datatype. They are int, short, boolean, char, byte, long, float, and double.
- Non-primitive datatype are also called as object defined datatypes. Some examples are Strings and Array etc.
</details>

---

2: How will you define variables in java?
<details>
  <summary> Show Answer </summary>

- Variables are the name of the memory location in specified data type.
- There are three types of variable. They are,
    - **Local variables**
        - These variables are declare inside the method or in a block. 
        - It can't be used outside of the block.
    - **Instance variables** 
        - These variables are declare outside any of the method or block in class where local variable in declared inside the block.
        - These variables are used though out the class.
        - Instance variables are accessed only by creating the object.
        - If it is not initialised with a value, it will has the default values of which data type it is declared.
    - **Static variables**
        - Like instance variable it is declared outside of any of block or method but decleared with static variabled.
        - Static variables are accessed without object creating by using class name.
        - If the static variables are accessed using object name, the object name will be converted into class name while compiling.
        - There are only one copy of static variables. If any change is done any part of program, it will affect thought out the program.
</details>

---

3: How many type of operators are there in java?
<details>
  <summary> Show Answer </summary>
  - Operators are the symbols used in java for specifired operation.
      - Unary Operator
      - Arithmetic Operator
      - Shift Operator
      - Bitwise Operator
      - Relational Operator
      - Assignment Operator
      - Logical Operator
      - Ternary Operator
</details>

---

4: Find the output for the following code.
``` java 
class Main{
 public static void main(String[] args){
  int a=1;
		System.out.println(2*a++ + 5 + a);
		System.out.println(a++ + ++a + ++a);
}
}
```
<details>
<summary> Show Answer </summary>
9
11

**Explanation**
In postincreament the value is holded then it will be increamented. 
In preincrement the value is increamented on code flow itself.

In first line of output
(2*1)+5+2=9
The value of a is 1 and then increamented to 2
In second line of output
2+4+5 = 11
Initially the value of a is 2 and then increamented to 3, in pre increament the value will be 4 and 5.
</details>

---

5: Explain about Ternary operator.
<details>
<summary> Show Answer </summary>
  - The ternary operator(?:) is also called conditional operator used to evalute boolean expression.
  - It needs three operands.

  **Syntax**
  variable=condition?expression1:expression2

  - If the condition is true, first expression will be executed else second expression executed

  **Example**
  int max = a>b?a:b;

  - It is the code of finding maximum of two numbers.
</details>

---

6: Explain about bitwise operators.
<details>
<summary> Show Answer </summary>
  - Bitwise operators works with binary value of given integer value.
  - Integer type values are used for this operation which are long, int, short, char, and byte.
  - First the given interger is converted into equivalent binary value then the operation is performed

  <b>Example</b>

``` java
  int b = 5^6;
  System.out.println(b);
  ```

  - First the 5 and 6 are converted into binary form as 101 and 110
  - Then the EX-OR operation is executed ie if any value is 1 then the output is 1.
  ```
  101
  110
  ___
  111
  ```
  - 111 is coverted into integer ie 3.
  - Therefore the output is 3.

</details>

---

7: Explain about the naming convention of variable.
<details>
<summary> Show Answer </summary>

- Variables are case-sentive
- The variable name should start from letter, the dollar sign `$` or underscore `_` but conventionally starts with letter.
- The numbers are allowed for variable that should not used at begining.
- No special characters are used for variable declaration.
- The variable consisting one word should be in lower case.**Example:** `address`, `email`. 
- If it consists two words or more, it should have name first letter of first word in lower case and  first letter of upcoming words should be in upper case **Example:** `phoneNumber`.
- If the variable is constant, the letters of the variable should be in capital and words seperated by uderscore`_`.**Example:** `static final int DEPARTMENT_ID = 230`.

---

