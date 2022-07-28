# Technical

1. Do inner classes have access to private members of the outer class?

<details><summary>Show Answer</summary>
Ans: yes, inner classes have access to all the members of outer class that include private members of class.
</details>

2. What are the uses of nested classes?

- A. grouping interrelated classes.
- B. achieving encapsulation
- C. create code that is easy to read and maintain
- D. All of the above.

<details><summary>Show Answer</summary>
<b>Ans:</b> D
</details>

# problem-Solving
 1. What is the output of the following code?

 ``` java
 public class Main {
    public int i = 0;
    public static void main(String[] args) {
        Main m = new Main();
        Main.Nested mn = m. new Nested();
        mn.printVariable(10);   
    }
    class Nested{
        public int i = 2;
        void printVariable(int i)
        {
            System.out.print(i+" ");
            System.out.print(this.i+" ");
            System.out.print(Main.this.i+" ");
        }
    }   
}
```
- A. 0
     2
     10

- B. 10
     2
     0

- C. 0
     10
     2

- D. Compile-time error

<details><summary>Show Answer</summary>

<b>Ans:</b> B

</details>
     





