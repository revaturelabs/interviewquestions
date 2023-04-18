1. find the index of an int in an array[];

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

```java
import java.util.Scanner;

public class demo {

    public static int findIndex(int[] arr, int n) {
        for (int i = 0; i < arr.length; i++) {
            if (arr[i] == n) {
                return i;
            }
        }
        return -1; // return -1 if the element is not found
    }
    
    public static void main(String[] args){
        Scanner scn=new Scanner(System.in);

        int[] arr={1,2,3,4,5,6}; 
        
        System.out.println("Enter the number whose index you want to find");
        int no=scn.nextInt();

        System.out.println(findIndex(arr, no));
    }
 
}

```

</blockquote>

</details>

---

2. build a calculator console app to get average.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Code for calculator application is mentioned below:

```java

import java.util.*;

public class Calculator {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter the total number of elements: ");
        int n = scanner.nextInt();

        int sum = 0;
        for (int i = 0; i < n; i++) {
            System.out.print("Enter element : ");
            int num = scanner.nextInt();
            sum += num;
        }

        double average = (double) sum / n;
        System.out.println("The average is: " + average);

    }
}


```

</blockquote>

</details>

---


3. reverse a string.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Suppose we have an sample string as "Hello, World!" to reverse this string we can use following code.

```java

String str = "Hello, World!";
String reversedStr = "";
for (int i = str.length() - 1; i >= 0; i--) {
    reversedStr += str.charAt(i);
}
System.out.println(reversedStr); 


```

</blockquote>

</details>

---