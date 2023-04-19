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

4. Find the second largest number in a given array.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

```Java

public class test {


    public static int findSecondLargest(int[] arr) {
        int largest = arr[0];
        int secondLargest = Integer.MIN_VALUE;
    
        for (int i = 1; i < arr.length; i++) {
            if (arr[i] > largest) {
                secondLargest = largest;
                largest = arr[i];
            } else if (arr[i] > secondLargest && arr[i] != largest) {
                secondLargest = arr[i];
            }
        }
    
        return secondLargest;
    }

    public static void main(String[] args) {
        
        int[] arr={1,2,3,4,5,6,7,8,9,9,8};

        System.out.println(findSecondLargest(arr));
    }
}

```

</blockquote>

</details>

---


5. How would you find unique words in a String?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The following code will give you the unique characters from the string.

```java

import java.util.*;

public class test {


    public static ArrayList<Character> findUniqueChars(String str) {
        
        str=str.toLowerCase();
        Map<Character,Integer> charCount=new HashMap<>();
        ArrayList<Character> chArray=new ArrayList<>();
    
        for (int i = 0; i < str.length(); i++) {
            char ch = str.charAt(i);
            if (!Character.isWhitespace(ch)) {
                if(null != charCount.putIfAbsent(ch,1)){
                    int count=charCount.get(ch);
                    charCount.put(ch,++count);
                }
            }
        }
        
        for (Map.Entry<Character,Integer> entry : charCount.entrySet()){
            if(entry.getValue()==1){
                chArray.add(entry.getKey());
            }
        }

        return chArray;
    
    }

    public static void main(String[] args) {
        String str="Hello there";

        System.out.println(findUniqueChars(str));
    }
}

```

</blockquote>

</details>

---


6. Code N factorial

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The following code will give you the factorial of given number N.

```Java

import java.util.*;

public class test {

        public static void main(String[] args) {

            Scanner scn=new Scanner(System.in);
            System.out.println("Enter the value of N :");
            int n = scn.nextInt(); 
            
            int factorial = 1;
            
            for(int i=1; i<=n; i++){
                factorial *= i;
            }
            
            System.out.println("Factorial of " + n + " is: " + factorial);
        }
    
}

```

</blockquote>

</details>

---


7. Can you write a Java method to determine whether a string is a palindrome.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The following programme checks if the given string is palindrome or not. It will return "Yes" if the string is palindrome and "No" if the string is not a palindrome.

```java

import java.util.*;

public class test {
 
    
    static boolean isPalindrome(String str)
    {
 
       
        int i = 0;
        int j = str.length() - 1;
        while (i < j) {
            if (str.charAt(i) != str.charAt(j))
                return false;
            i++;
            j--;
        }
        return true;
    }
 
    
    public static void main(String[] args)
    {
       
        Scanner scn=new Scanner(System.in);
        System.out.println("Enter the string:");
        String str = scn.nextLine(); 

        str = str.toLowerCase();
        if (isPalindrome(str))
            System.out.print("Yes");
        else
            System.out.print("No");
    }
}

```

</blockquote>

</details>

---


</blockquote>

</details>

---


8. Move all the 0's to the end in a 1D array.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>



</blockquote>

</details>

---

