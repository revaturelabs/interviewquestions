1. find the index of an int in an array[];

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

**Java**1. find the index of an int in an array[];

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

**Java**

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
**C#**

``` C#


using System;
 
public static class Extensions
{
    public static int findIndex<T>(this T[] array, T item) {
        return Array.IndexOf(array, item);
    }
}
 
public class Example
{
    public static void Main()
    {
        int[] array = { 1, 2, 3, 4, 5 };
        int item = Convert.ToInt32(Console.ReadLine());
        int index = array.findIndex(item);
        if (index != -1) {
            Console.WriteLine(String.Format("Element {0} is found at index {1}", item, index));
        }
        else {
            Console.WriteLine("Element not found in the given array.");
        }
    }
}

```

**Python**

```python

lst = [13, 4, 20, 15, 6, 20, 20]

print(lst.index(6))

```

</blockquote>

</details>

---

2. build a calculator console app to get average.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Code for calculator application is mentioned below:
**Java**

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
**C#**

```C#
 
//Program to calculate the average of array elements.

using System;

class Avg
{
    public static void Main()
    {
        int n = Convert.ToInt32(Console.ReadLine());
        int[] arr = new int[n];
        int sum = 0;
        float average = 0.0F;
        for(int i = 0; i < n; i++) {
            arr[i] = Convert.ToInt32(Console.ReadLine());
            //Console.WriteLine(i);
            sum += arr[i];
        }
        average=(float)sum/n;
        Console.WriteLine(average);
    }
}

```

**Python**

```python

# Python code to get average of list

def Average(lst):
	sum_of_list = 0
	for i in range(len(lst)):
		sum_of_list += lst[i]
	average = sum_of_list/len(lst)
	return average


# Driver Code
lst = [15, 9, 55, 41, 35, 20, 62, 49]
average = Average(lst)
print("Average of the list =", round(average, 2))

```
</blockquote>

</details>

---


3. reverse a string.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Suppose we have an sample string as "Hello, World!" to reverse this string we can use following code.

**Java**

```java

String str = "Hello, World!";
String reversedStr = "";
for (int i = str.length() - 1; i >= 0; i--) {
    reversedStr += str.charAt(i);
}
System.out.println(reversedStr); 


```
**C#**

```C#
using System;
namespace Exercises
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Enter a String : ");
            string originalString = Console.ReadLine();
            string reverseString = string.Empty;
            for (int i = originalString.Length - 1; i >= 0; i--)
            {
                reverseString += originalString[i];
            }
            Console.Write($"Reverse String is : {reverseString} ");
            
        }      
    }
}

```

**Python**

```python
# Function to reverse a string
def reverse(string):
    string = string[::-1]
    return string
 
s = input("Enter the string: ")
 
print("The original string is : ", end="")
print(s)
 
print("The reversed string(using extended slice syntax) is : ", end="")
print(reverse(s))

```
</blockquote>

</details>

---

4. Find the second largest number in a given array.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

**Java**

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
**C#**

```C#
using System;

class Program
{
    public static void Main()
    {
        int n = Convert.ToInt32(Console.ReadLine());
        int largest,secondLargest,i,j=0;
        int[] arr = new int[n];
        
        for(i = 0; i < n; i++) {
            arr[i] = Convert.ToInt32(Console.ReadLine());
        }
         largest = 0;
 
            for (i = 0; i < n; i++)
            {
                if (largest < arr[i])
                {
                    largest = arr[i];
                    j = i;
                }
            }
            /* ignore the largest element and find the 2nd largest element in the array */
            secondLargest = 0;
            for (i = 0; i < n; i++)
            {
                if (i == j)
                {
                    continue;  /* ignoring the largest element */
                    
                }
                else
                {
                    if (secondLargest < arr[i])
                    {
                        secondLargest = arr[i];
                    }
                }
            }
 
            Console.Write("The Second largest element in the array is :  {0} \n\n", secondLargest);
    }
}

```

**Python**

```python
# Python program to find largest number
# in a list

# List of numbers
list1 = [10, 20, 20, 4, 45, 45, 45, 99, 99]

# Removing duplicates from the list
list2 = list(set(list1))

# Sorting the list
list2.sort()

# Printing the second last element
print("Second largest element is:", list2[-2])

```

</blockquote>

</details>

---


5. How would you find unique words in a String?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The following code will give you the unique characters from the string.

**Java**

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
**C#**

```C#
using System;
using System.Linq;
class HelloWorld {
  static void Main() {
    string input = "C# Corner is a popular online community popular online community";
    string[] words = input.Split(' ');
    string[] distinctWords = words.Distinct().ToArray();
    string output = string.Join(" ", distinctWords);
    Console.WriteLine(output);
  }
}
```
**Python**

```python
def printWords(l):
     
    # for loop for iterating
    for i in l:
        print(i)
 
 
# Driver code
str = input("Enter the string: ")
 
# storing string in the form of list of words
s = set(str.split(" "))
 
# passing list to print words function
printWords(s)

```
</blockquote>

</details>

---


6. Code N factorial

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The following code will give you the factorial of given number N.

**Java**

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
**C#**

```C#
using System;
namespace Exercises
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Enter a Number : ");
            int number = int.Parse(Console.ReadLine());

            long factorial = RecursiveFactorial(number);
            Console.Write($"Factorial of {number} is: {factorial}");    
            
            
        }

        static long RecursiveFactorial(int number)
        {
            if (number == 1)
            {
                return 1;
            } 
            else
            {
                return number * RecursiveFactorial(number - 1);
            }    
        }
    }
}

```

**Python**

```python

num = int(input("Enter a number: "))

factorial = 1

# check if the number is negative, positive or zero
if num < 0:
   print("Sorry, factorial does not exist for negative numbers")
elif num == 0:
   print("The factorial of 0 is 1")
else:
   for i in range(1,num + 1):
       factorial = factorial*i
   print("The factorial of",num,"is",factorial)

```

</blockquote>

</details>

---


7. Can you write a Java method to determine whether a string is a palindrome.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The following programme checks if the given string is palindrome or not. It will return "Yes" if the string is palindrome and "No" if the string is not a palindrome.

**Java**

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
**C#**

```C#
using System;
namespace LogicalPrograms
{
    public class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Enter a string to Check Palindrome : ");
            string name = Console.ReadLine();
            string reverse = string.Empty;
            
            for (int i = name.Length - 1; i >= 0; i--)
            {
                reverse += name[i];
            }
            
            if (name == reverse)
            {
                Console.WriteLine($"{name} is Palindrome.");
            }
            else
            {
                Console.WriteLine($"{name} is not Palindrome");
            }
            
        }
    }
}
```
**Python**

```python
def isPalindrome(s):
    return s == s[::-1]
  
  
# Driver code
s = input("Enter the string: ")
ans = isPalindrome(s)
  
if ans:
    print("Yes, It is a Palindrome")
else:
    print("No, It is not a Palindrome")
```
</blockquote>

</details>

---


8. Move all the 0's to the end in a 1D array.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The following code will move all the 0's present in the array at the end.

**Java**

```java

import java.util.*;

public class test {
 
    
    public static void moveZeroesToEnd(int[] arr) {
        int nonZeroIndex = 0;
    
        for (int i = 0; i < arr.length; i++) {
            if (arr[i] != 0) {
                arr[nonZeroIndex++] = arr[i];
            }
        }
     
        while (nonZeroIndex < arr.length) {
            arr[nonZeroIndex++] = 0;
        }

        System.out.println(arr[1]);
    }
 
    
    public static void main(String[] args)
    {
       
        Scanner scn=new Scanner(System.in);
       int[] arr={1,0,2,0,3,4,5};
        moveZeroesToEnd(arr);
        
    }
}

```
**C#**

```C#

using System;

class PushZero
{

	static void pushZerosToEnd(int []arr, int n)
	{
	
		int count = 0;
		for (int i = 0; i < n; i++)
		if (arr[i] != 0)
	
		arr[count++] = arr[i];
	
		while (count < n)
		arr[count++] = 0;
	}
	
	
	public static void Main ()
	{
		int []arr = {1, 9, 8, 4, 0, 0, 2, 7, 0, 6, 0, 9};
		int n = arr.Length;
		pushZerosToEnd(arr, n);
		Console.WriteLine("Array after pushing all zeros to the back: ");
		for (int i = 0; i < n; i++)
		Console.Write(arr[i] +" ");
	}
}
```


**Python**
```python
def pushZerosToEnd(arr, n):
	count = 0
	for i in range(n):
		if arr[i] != 0:
			arr[count] = arr[i]
			count+=1
	
	while count < n:
		arr[count] = 0
		count += 1
		

arr = [1, 9, 8, 4, 0, 0, 2, 7, 0, 6, 0, 9]
n = len(arr)
pushZerosToEnd(arr, n)
print("Array after pushing all zeros to end of array:")
print(arr)

```
</blockquote>

</details>

---

9. Given the set of numbers 1-100, code a program that would give fizz if it’s divisible by 5, buzz if divisible by 3, fizz buzz is divisible by both and the number of by neither.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

**Java**

```java
import java.util.*;

public class Test{
    public static void main(String[] args) {
        for (int num = 1; num <= 100; num++) {
            if (num % 3 == 0 && num % 5 == 0) {
                System.out.println("FizzBuzz");
            } else if (num % 3 == 0) {
                System.out.println("Buzz");
            } else if (num % 5 == 0) {
                System.out.println("Fizz");
            } else {
                System.out.println(num);
            }
        }
        
        
    }
}

```
**C#**
```C#
using System;
namespace LogicalPrograms
{
    public class Program
    {
        static void Main(string[] args)
        {
            for (int num = 1; num <= 100; num++) {
            if (num % 3 == 0 && num % 5 == 0) {
                Console.WriteLine("FizzBuzz");
            } else if (num % 3 == 0) {
                Console.WriteLine("Buzz");
            } else if (num % 5 == 0) {
                Console.WriteLine("Fizz");
            } else {
                Console.WriteLine(num);
            }
        }
        }
    }
}
```

**Python**

```python
def fizzBuzz(n):
    for n in range(1,n+1):
        if n % 3 == 0 and n % 5 == 0:
            print('FizzBuzz')
        elif n % 3 == 0:
            print('Fizz')
        elif n % 5 == 0:
            print('Buzz')
        else:
            print(n)

if __name__ == '__main__':
    n = int(input().strip())
    fizzBuzz(n)

```

</blockquote>

</details>

---


10. Write a function to create a list? The list should contain different elements every time the function is invoked?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The following code contains a  `generateList()` method which generates a list with random elements every time it is called. The size of the list must be passed as an argument to the `generateList()` method.

**Java**

```java 
import java.util.*;

public class Test{
    public static void main(String[] args) {
        ArrayList<Integer> list = new ArrayList<Integer>();
        
        list=generateList(3);
        System.out.println(list.toString());


        list=generateList(5);
        System.out.println(list.toString());
    }

    public static ArrayList<Integer> generateList(int size) {
        ArrayList<Integer> list = new ArrayList<Integer>();
        Random rand = new Random();

        for (int i = 0; i < size; i++) {
            int randNum = rand.nextInt(100);
            list.add(randNum);
        }

        return list;
    }
}

```

</blockquote>

</details>

---


11. Sort a list in ascending order?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The following code will sort a list of integers in ascending order using the built-in `Collections` class in Java:

**Java**

```java

import java.util.*;

public class Test{
    public static void main(String[] args) {
        ArrayList<Integer> numbers = new ArrayList<Integer>();
        numbers.add(5);
        numbers.add(2);
        numbers.add(8);
        numbers.add(1);

        Collections.sort(numbers);

        System.out.println(numbers);
    }

    
}

```
**C#**
```C#
// C# program to sort a list of integers
// Using OrderBy() method
using System;
using System.Linq;
using System.Collections.Generic;

class Exercise{
	
static void Main(string[] args)
{
	List<int> nums = new List<int>() { 50, 20, 40, 60, 33, 70 };
	
	var result_set = nums.OrderBy(num => num);
	
	Console.WriteLine("Sorted in Ascending order:");
	foreach (int value in result_set)
	{
		Console.Write(value + " ");
	}
}
}

```

**Python**
```python


numbers = [1, 3, 4, 2]

print(numbers.sort()) # None
print(numbers)		 # [1, 2, 3, 4]

print(sorted(numbers)) # [1, 2, 3, 4]
print(numbers)		 # [1, 3, 4, 2]



```
</blockquote>

</details>

---

12. Let's say you have a Student class with a name field and a grade field. If you put multiple Student objects in an array, then how would you sort them by name?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The following code the Student class implements the `Comparable` interface and overrides the `compareTo()` method to compare two Student objects based on their name field. 

```java

import java.util.*;

class Student implements Comparable<Student> {
    private String name;
    private int grade;

    public Student(String name, int grade) {
        this.name = name;
        this.grade = grade;
    }

    public String getName() {
        return name;
    }

    public int getGrade() {
        return grade;
    }

    @Override
    public int compareTo(Student other) {
        return this.name.compareTo(other.getName());
    }

}

public class Test{
    public static void main(String[] args) {
        Student[] students = new Student[3];
        students[0] = new Student("Ram", 80);
        students[1] = new Student("Sham", 52);
        students[2] = new Student("Manoj", 78);

        Arrays.sort(students);

        for (Student s : students) {
            System.out.println(s.getName() + " " + s.getGrade());
        }
    }
    
}

```

</blockquote>

</details>

---

13. You have an ArrayList of Strings. For each String in the array, display the String and the number of times that String appeared in the array.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The following code displays each String in an ArrayList along with the number of times that String appears in the list:

```java
import java.util.*;

public class Test{
    public static void main(String[] args) {
        ArrayList<String> strings = new ArrayList<String>();
        strings.add("Man");
        strings.add("Animal");
        strings.add("Animal");
        strings.add("Bird");

        Map<String, Integer> stringCount = new HashMap<String, Integer>();

        for (String s : strings) {
            if (stringCount.containsKey(s)) {
                stringCount.put(s, stringCount.get(s) + 1);
            } else {
                stringCount.put(s, 1);
            }
        }

        for (Map.Entry<String, Integer> entry : stringCount.entrySet()) {
            System.out.println(entry.getKey() + " : " + entry.getValue() + " time(s)");
        }
    }
    
}

```
**C#**
```C#
using System;
namespace Exercises
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Enter the string : ");
            string message = Console.ReadLine();
            message = message.Replace(" ", string.Empty);
            while (message.Length > 0)
            {
                Console.Write(message[0] + " : ");
                int count = 0;
                for (int j = 0; j < message.Length; j++)
                {
                    if (message[0] == message[j])
                    {
                        count++;
                    }
                }
                Console.WriteLine(count);
                message = message.Replace(message[0].ToString(), string.Empty);
            }
        }
    }
}
```
**python**

```python
inp_str = "Programming"
out = {x : inp_str.count(x) for x in set(inp_str )}
print ("Occurrence of all characters in the given string is :\n "+ str(out))
```


</blockquote>

</details>

---

14. reverse the string.  

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The following code will reverse using character array.

```java

import java.util.*;

public class Test{
    public static void main(String[] args) {
        String originalString = "hello world";
        char[] originalArray = originalString.toCharArray();
        char[] reversedArray = new char[originalArray.length];

        for (int i = 0; i < originalArray.length; i++) {
            reversedArray[i] = originalArray[originalArray.length - 1 - i];
        }

        String reversedString = new String(reversedArray);
        System.out.println(reversedString);    
}
   
}
```

</blockquote>

</details>

---

15. find the 2nd longest word in the string.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

```java

```

</blockquote>

</details>

---

16. Given a List of a List of Intergers: first index is start time. second index is end time. [[1, 5], [3, 6], [6, 8]] How would you implement a function to find out if there is an overlap between classes.


<details><summary><b> Show Answer</b></summary>
  
<blockquote>



</blockquote>

</details>

---

17. Given a list of Integers:first index is start time.second index is end time.[1,2][1,2] How would you implement a function that returns how many instructors are needed on the day"

<details><summary><b> Show Answer</b></summary>
  
<blockquote>



</blockquote>

</details>

---

18. write a method in java that iterates through a string?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>



</blockquote>

</details>

---

19. Write a program to add two numbers without using the arithmatic operator.
public static int add(int a, int b) {
    while (b != 0) {
        int carry = a & b;
        a = a ^ b;
        b = carry << 1;
    }
    return a;
}

<details><summary><b> Show Answer</b></summary>
  
<blockquote>



</blockquote>

</details>

---

20. Had me do a coding exercise to analyze an ArrayList of Strings, and print out any strings that contain duplicates and how many, in the order they appear.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>



</blockquote>

</details>

---



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
**C#**

``` C#


using System;
 
public static class Extensions
{
    public static int findIndex<T>(this T[] array, T item) {
        return Array.IndexOf(array, item);
    }
}
 
public class Example
{
    public static void Main()
    {
        int[] array = { 1, 2, 3, 4, 5 };
        int item = Convert.ToInt32(Console.ReadLine());
        int index = array.findIndex(item);
        if (index != -1) {
            Console.WriteLine(String.Format("Element {0} is found at index {1}", item, index));
        }
        else {
            Console.WriteLine("Element not found in the given array.");
        }
    }
}

```

**Python**

```python

lst = [13, 4, 20, 15, 6, 20, 20]

print(lst.index(6))

```

</blockquote>

</details>

---

2. build a calculator console app to get average.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Code for calculator application is mentioned below:
	
**Java**

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
**C#**

```C#
 
//Program to calculate the average of array elements.

using System;

class Avg
{
    public static void Main()
    {
        int n = Convert.ToInt32(Console.ReadLine());
        int[] arr = new int[n];
        int sum = 0;
        float average = 0.0F;
        for(int i = 0; i < n; i++) {
            arr[i] = Convert.ToInt32(Console.ReadLine());
            //Console.WriteLine(i);
            sum += arr[i];
        }
        average=(float)sum/n;
        Console.WriteLine(average);
    }
}

```

**Python**

```python

# Python code to get average of list

def Average(lst):
	sum_of_list = 0
	for i in range(len(lst)):
		sum_of_list += lst[i]
	average = sum_of_list/len(lst)
	return average


# Driver Code
lst = [15, 9, 55, 41, 35, 20, 62, 49]
average = Average(lst)
print("Average of the list =", round(average, 2))

```
</blockquote>

</details>

---


3. reverse a string.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

Suppose we have an sample string as "Hello, World!" to reverse this string we can use following code.

**Java**

```java

String str = "Hello, World!";
String reversedStr = "";
for (int i = str.length() - 1; i >= 0; i--) {
    reversedStr += str.charAt(i);
}
System.out.println(reversedStr); 


```
**C#**

```C#
using System;
namespace Exercises
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Enter a String : ");
            string originalString = Console.ReadLine();
            string reverseString = string.Empty;
            for (int i = originalString.Length - 1; i >= 0; i--)
            {
                reverseString += originalString[i];
            }
            Console.Write($"Reverse String is : {reverseString} ");
            
        }      
    }
}

```

**Python**

```python
# Function to reverse a string
def reverse(string):
    string = string[::-1]
    return string
 
s = input("Enter the string: ")
 
print("The original string is : ", end="")
print(s)
 
print("The reversed string(using extended slice syntax) is : ", end="")
print(reverse(s))

```
</blockquote>

</details>

---

4. Find the second largest number in a given array.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

**Java**

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
**C#**

```C#
using System;

class Program
{
    public static void Main()
    {
        int n = Convert.ToInt32(Console.ReadLine());
        int largest,secondLargest,i,j=0;
        int[] arr = new int[n];
        
        for(i = 0; i < n; i++) {
            arr[i] = Convert.ToInt32(Console.ReadLine());
        }
         largest = 0;
 
            for (i = 0; i < n; i++)
            {
                if (largest < arr[i])
                {
                    largest = arr[i];
                    j = i;
                }
            }
            /* ignore the largest element and find the 2nd largest element in the array */
            secondLargest = 0;
            for (i = 0; i < n; i++)
            {
                if (i == j)
                {
                    continue;  /* ignoring the largest element */
                    
                }
                else
                {
                    if (secondLargest < arr[i])
                    {
                        secondLargest = arr[i];
                    }
                }
            }
 
            Console.Write("The Second largest element in the array is :  {0} \n\n", secondLargest);
    }
}

```

**Python**

```python
# Python program to find largest number
# in a list

# List of numbers
list1 = [10, 20, 20, 4, 45, 45, 45, 99, 99]

# Removing duplicates from the list
list2 = list(set(list1))

# Sorting the list
list2.sort()

# Printing the second last element
print("Second largest element is:", list2[-2])

```

</blockquote>

</details>

---


5. How would you find unique words in a String?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The following code will give you the unique characters from the string.

**Java**

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
**C#**

```C#
using System;
using System.Linq;
class HelloWorld {
  static void Main() {
    string input = "C# Corner is a popular online community popular online community";
    string[] words = input.Split(' ');
    string[] distinctWords = words.Distinct().ToArray();
    string output = string.Join(" ", distinctWords);
    Console.WriteLine(output);
  }
}
```
**Python**

```python
def printWords(l):
     
    # for loop for iterating
    for i in l:
        print(i)
 
 
# Driver code
str = input("Enter the string: ")
 
# storing string in the form of list of words
s = set(str.split(" "))
 
# passing list to print words function
printWords(s)

```
</blockquote>

</details>

---


6. Code N factorial

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The following code will give you the factorial of given number N.

**Java**

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
**C#**

```C#
using System;
namespace Exercises
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Enter a Number : ");
            int number = int.Parse(Console.ReadLine());

            long factorial = RecursiveFactorial(number);
            Console.Write($"Factorial of {number} is: {factorial}");    
            
            
        }

        static long RecursiveFactorial(int number)
        {
            if (number == 1)
            {
                return 1;
            } 
            else
            {
                return number * RecursiveFactorial(number - 1);
            }    
        }
    }
}

```

**Python**

```python

num = int(input("Enter a number: "))

factorial = 1

# check if the number is negative, positive or zero
if num < 0:
   print("Sorry, factorial does not exist for negative numbers")
elif num == 0:
   print("The factorial of 0 is 1")
else:
   for i in range(1,num + 1):
       factorial = factorial*i
   print("The factorial of",num,"is",factorial)

```

</blockquote>

</details>

---


7. Can you write a Java method to determine whether a string is a palindrome.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The following programme checks if the given string is palindrome or not. It will return "Yes" if the string is palindrome and "No" if the string is not a palindrome.

**Java**

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
**C#**

```C#
using System;
namespace LogicalPrograms
{
    public class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Enter a string to Check Palindrome : ");
            string name = Console.ReadLine();
            string reverse = string.Empty;
            
            for (int i = name.Length - 1; i >= 0; i--)
            {
                reverse += name[i];
            }
            
            if (name == reverse)
            {
                Console.WriteLine($"{name} is Palindrome.");
            }
            else
            {
                Console.WriteLine($"{name} is not Palindrome");
            }
            
        }
    }
}
```
**Python**

```python
def isPalindrome(s):
    return s == s[::-1]
  
  
# Driver code
s = input("Enter the string: ")
ans = isPalindrome(s)
  
if ans:
    print("Yes, It is a Palindrome")
else:
    print("No, It is not a Palindrome")
```
</blockquote>

</details>

---


8. Move all the 0's to the end in a 1D array.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The following code will move all the 0's present in the array at the end.

**Java**

```java

import java.util.*;

public class test {
 
    
    public static void moveZeroesToEnd(int[] arr) {
        int nonZeroIndex = 0;
    
        for (int i = 0; i < arr.length; i++) {
            if (arr[i] != 0) {
                arr[nonZeroIndex++] = arr[i];
            }
        }
     
        while (nonZeroIndex < arr.length) {
            arr[nonZeroIndex++] = 0;
        }

        System.out.println(arr[1]);
    }
 
    
    public static void main(String[] args)
    {
       
        Scanner scn=new Scanner(System.in);
       int[] arr={1,0,2,0,3,4,5};
        moveZeroesToEnd(arr);
        
    }
}

```
**C#**

```C#

using System;

class PushZero
{

	static void pushZerosToEnd(int []arr, int n)
	{
	
		int count = 0;
		for (int i = 0; i < n; i++)
		if (arr[i] != 0)
	
		arr[count++] = arr[i];
	
		while (count < n)
		arr[count++] = 0;
	}
	
	
	public static void Main ()
	{
		int []arr = {1, 9, 8, 4, 0, 0, 2, 7, 0, 6, 0, 9};
		int n = arr.Length;
		pushZerosToEnd(arr, n);
		Console.WriteLine("Array after pushing all zeros to the back: ");
		for (int i = 0; i < n; i++)
		Console.Write(arr[i] +" ");
	}
}
```


**Python**
```python
def pushZerosToEnd(arr, n):
	count = 0
	for i in range(n):
		if arr[i] != 0:
			arr[count] = arr[i]
			count+=1
	
	while count < n:
		arr[count] = 0
		count += 1
		

arr = [1, 9, 8, 4, 0, 0, 2, 7, 0, 6, 0, 9]
n = len(arr)
pushZerosToEnd(arr, n)
print("Array after pushing all zeros to end of array:")
print(arr)

```
</blockquote>

</details>

---

9. Given the set of numbers 1-100, code a program that would give fizz if it’s divisible by 5, buzz if divisible by 3, fizz buzz is divisible by both and the number of by neither.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

```java
import java.util.*;

public class Test{
    public static void main(String[] args) {
        for (int num = 1; num <= 100; num++) {
            if (num % 3 == 0 && num % 5 == 0) {
                System.out.println("FizzBuzz");
            } else if (num % 3 == 0) {
                System.out.println("Buzz");
            } else if (num % 5 == 0) {
                System.out.println("Fizz");
            } else {
                System.out.println(num);
            }
        }
        
        
    }
}

```
**C#**
```C#
using System;
namespace LogicalPrograms
{
    public class Program
    {
        static void Main(string[] args)
        {
            for (int num = 1; num <= 100; num++) {
            if (num % 3 == 0 && num % 5 == 0) {
                Console.WriteLine("FizzBuzz");
            } else if (num % 3 == 0) {
                Console.WriteLine("Buzz");
            } else if (num % 5 == 0) {
                Console.WriteLine("Fizz");
            } else {
                Console.WriteLine(num);
            }
        }
        }
    }
}
```

**Python**

```python
def fizzBuzz(n):
    for n in range(1,n+1):
        if n % 3 == 0 and n % 5 == 0:
            print('FizzBuzz')
        elif n % 3 == 0:
            print('Fizz')
        elif n % 5 == 0:
            print('Buzz')
        else:
            print(n)

if __name__ == '__main__':
    n = int(input().strip())
    fizzBuzz(n)

```

</blockquote>

</details>

---


10. Write a function to create a list? The list should contain different elements every time the function is invoked?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The following code contains a  `generateList()` method which generates a list with random elements every time it is called. The size of the list must be passed as an argument to the `generateList()` method.

**Java**

```java 
import java.util.*;

public class Test{
    public static void main(String[] args) {
        ArrayList<Integer> list = new ArrayList<Integer>();
        
        list=generateList(3);
        System.out.println(list.toString());


        list=generateList(5);
        System.out.println(list.toString());
    }

    public static ArrayList<Integer> generateList(int size) {
        ArrayList<Integer> list = new ArrayList<Integer>();
        Random rand = new Random();

        for (int i = 0; i < size; i++) {
            int randNum = rand.nextInt(100);
            list.add(randNum);
        }

        return list;
    }
}

```

</blockquote>

</details>

---


11. Sort a list in ascending order?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The following code will sort a list of integers in ascending order using the built-in `Collections` class in Java:

**Java**

```java

import java.util.*;

public class Test{
    public static void main(String[] args) {
        ArrayList<Integer> numbers = new ArrayList<Integer>();
        numbers.add(5);
        numbers.add(2);
        numbers.add(8);
        numbers.add(1);

        Collections.sort(numbers);

        System.out.println(numbers);
    }
}

```
**C#**
```C#
// C# program to sort a list of integers
// Using OrderBy() method
using System;
using System.Linq;
using System.Collections.Generic;

class Exercise{
	
static void Main(string[] args)
{
	List<int> nums = new List<int>() { 50, 20, 40, 60, 33, 70 };
	
	var result_set = nums.OrderBy(num => num);
	
	Console.WriteLine("Sorted in Ascending order:");
	foreach (int value in result_set)
	{
		Console.Write(value + " ");
	}
}
}

```

**Python**
```python


numbers = [1, 3, 4, 2]

print(numbers.sort()) # None
print(numbers)		 # [1, 2, 3, 4]

print(sorted(numbers)) # [1, 2, 3, 4]
print(numbers)		 # [1, 3, 4, 2]



```
</blockquote>

</details>

---

12. Let's say you have a Student class with a name field and a grade field. If you put multiple Student objects in an array, then how would you sort them by name?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The following code the Student class implements the `Comparable` interface and overrides the `compareTo()` method to compare two Student objects based on their name field. 

```java

import java.util.*;

class Student implements Comparable<Student> {
    private String name;
    private int grade;

    public Student(String name, int grade) {
        this.name = name;
        this.grade = grade;
    }

    public String getName() {
        return name;
    }

    public int getGrade() {
        return grade;
    }

    @Override
    public int compareTo(Student other) {
        return this.name.compareTo(other.getName());
    }

}

public class Test{
    public static void main(String[] args) {
        Student[] students = new Student[3];
        students[0] = new Student("Ram", 80);
        students[1] = new Student("Sham", 52);
        students[2] = new Student("Manoj", 78);

        Arrays.sort(students);

        for (Student s : students) {
            System.out.println(s.getName() + " " + s.getGrade());
        }
    }
    
}

```

</blockquote>

</details>

---

13. You have an ArrayList of Strings. For each String in the array, display the String and the number of times that String appeared in the array.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The following code displays each String in an ArrayList along with the number of times that String appears in the list:

```java
import java.util.*;

public class Test{
    public static void main(String[] args) {
        ArrayList<String> strings = new ArrayList<String>();
        strings.add("Man");
        strings.add("Animal");
        strings.add("Animal");
        strings.add("Bird");

        Map<String, Integer> stringCount = new HashMap<String, Integer>();

        for (String s : strings) {
            if (stringCount.containsKey(s)) {
                stringCount.put(s, stringCount.get(s) + 1);
            } else {
                stringCount.put(s, 1);
            }
        }

        for (Map.Entry<String, Integer> entry : stringCount.entrySet()) {
            System.out.println(entry.getKey() + " : " + entry.getValue() + " time(s)");
        }
    }
    
}

```

</blockquote>

</details>

---

14. reverse the string.  

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

The following code will reverse using character array.

```java

import java.util.*;

public class Test{
    public static void main(String[] args) {
        String originalString = "hello there";
        char[] originalArray = originalString.toCharArray();
        char[] reversedArray = new char[originalArray.length];

        for (int i = 0; i < originalArray.length; i++) {
            reversedArray[i] = originalArray[originalArray.length - 1 - i];
        }

        String reversedString = new String(reversedArray);
        System.out.println(reversedString);    
}
   
}
```
In this example, we first convert the originalString to a character array using the `toCharArray()` method. We then create a new character array reversedArray of the same length as originalArray. We loop over each element in originalArray, copy it to the corresponding position in reversedArray, and reverse the order. Finally, we create a new `String` object from the reversed character array.

</blockquote>

</details>

---

15. find the 2nd longest word in the string.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>

```java


```

</blockquote>

</details>

---

16. Given a List of a List of Intergers: first index is start time. second index is end time. [[1, 5], [3, 6], [6, 8]] How would you implement a function to find out if there is an overlap between classes.


<details><summary><b> Show Answer</b></summary>
  
<blockquote>



</blockquote>

</details>

---

17. Given a list of Integers:first index is start time.second index is end time.[1,2][1,2] How would you implement a function that returns how many instructors are needed on the day"

<details><summary><b> Show Answer</b></summary>
  
<blockquote>



</blockquote>

</details>

---

18. write a method in java that iterates through a string?

<details><summary><b> Show Answer</b></summary>
  
<blockquote>



</blockquote>

</details>

---

19. Write a program to add two numbers without using the arithmatic operator.
public static int add(int a, int b) {
    while (b != 0) {
        int carry = a & b;
        a = a ^ b;
        b = carry << 1;
    }
    return a;
}

<details><summary><b> Show Answer</b></summary>
  
<blockquote>



</blockquote>

</details>

---

20. Had me do a coding exercise to analyze an ArrayList of Strings, and print out any strings that contain duplicates and how many, in the order they appear.

<details><summary><b> Show Answer</b></summary>
  
<blockquote>



</blockquote>

</details>

---

