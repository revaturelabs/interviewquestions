## Access Modifiers

1.Explain about Access Modifier.

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)
<details markdown="1">
    <summary><b> Show Answer </b></summary> 
<blockquote markdown="1">

- Access Modifiers are used to limit the accessibility or visibility of class, method, variable, and constructor.

There are four type of access modifier:
 - Default
 - Public
 - Private
 - Protected
</blockquote>
</details>

---

2.Explain about Default Access Modifier.

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)
<details markdown="1">
    <summary><b> Show Answer </b></summary> 
<blockquote markdown="1">

- If we do not specify the access modifier, the default will be the access modifier.
- When we declare default access modifier, the visibility will be only within the package.
- If we declare class as default, we can't access the class outside the package and we can't import in another class.
</blockquote>
</details>

---

3.Explain about `public` Access Modifier.

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)
<details markdown="1">
    <summary><b> Show Answer </b></summary> 
<blockquote markdown="1">

- If we specify with public the access modifier, the accessibility will be anywhere within or outside the package.
- We can import the class from any package when it is declared as public.
</blockquote>
</details>

---

4.Explain about `private` Access modifier.

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)
<details markdown="1">
    <summary><b> Show Answer </b></summary> 
<blockquote markdown="1">

- If we specify with private access modifier to any field,the accessibility will be within the class.
- It is the most retrictive access modifier.
- It can't be used for class and interface.
</blockquote>
</details>

---

5.Can we use private variables outside the class?

![Medium](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Medium%20(2).svg)
<details markdown="1">
    <summary><b> Show Answer </b></summary> 
<blockquote markdown="1">

- No, we can't access the private variables outside the class.
- If we want to use the private variable outside the class, we will have to create public methods to access it.
- In general, we will create getter and setter method to access private variables.

</blockquote>
</details>

---

6.Explain about Protected Access modifier.

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)
<details markdown="1">
    <summary><b> Show Answer </b></summary> 
<blockquote markdown="1">
	
If we specify with protected the access modifier, the accessibility will be within the class and subclasses which are extended from it.
</blockquote>
</details>

---

7.Explain the difference between Private and Protected.

![Medium](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Medium%20(2).svg)
<details markdown="1">
    <summary><b> Show Answer </b></summary> 
<blockquote markdown="1">

| Private                                              |Protected                                             |
|------------------------------------------------------|------------------------------------------------------|
|The visibility is only within the class               |The visibility is only within the class and subcalsses|
|We can use public method to access private variable and private method out side of class   |We can use public method to access protected variable and proctected variable out side of class and subclass |
</blockquote>
</details>

---

8.Find the error in the program.
``` java
package com.example.model;

public class Employee {
	private String name;
	private String address;
	public Employee(String name, String address) {
		super();
		this.name = name;
		this.address = address;
	}
	
}
```

``` java
 package com.example;

import com.example.model.Employee;

public class Main {
	public static void main(String[] args) {
		Employee emp = new Employee("Arnold","Washington");
        System.out.println(emp.name)
	}
}
```

![Medium](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Medium%20(2).svg)
<details markdown="1">
    <summary><b> Show Answer </b></summary> 
<blockquote markdown="1">

We can't use private variable outside the class. If we want to access the variable outside the class, we have to use public method such as getter method from the class.

</blockquote>
</details>

---

9.Find the error in the program.
``` java
package com.example.model;

public class Employee {
	protected String name;
	protected String address;
	public Employee(String name, String address) {
		super();
		this.name = name;
		this.address = address;
	}	
}
```

``` java
package com.example;

import com.example.model.Employee;

public class Main {
	public static void main(String[] args) {
		Employee emp = new Employee("Arnold","Washington");
        System.out.println(emp.name)
	}
}
```

![Medium](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Medium%20(2).svg)
<details markdown="1">
    <summary><b> Show Answer </b></summary> 
<blockquote markdown="1">

We can't use protected variable outside the class. If we want to access the variable outside the class, we have to use public method such as getter method from the class.

</details>
</blockquote>

---

10.Predict the output.
``` java
package com.example.model;

public class Employee {
	protected String name;
	protected String address;
	public Employee(String name, String address) {
		super();
		this.name = name;
		this.address = address;
	}
	public Employee() {
	}
	public String getName() {
		return name;
	}
	public String getAddress() {
		return address;
	}
}
```
``` java
package com.example.model;

public class Department extends Employee {
	public Department() {
		super();
	}
	public Department(String name, String address) {
		super(name, address);
	}
}

```
``` java
package com.example;

import com.example.model.Department;
import com.example.model.Employee;

public class Main {
	public static void main(String[] args) {
		Employee emp = new Employee("Arnold","Washington");
		Department dep = new Department();
		System.out.println(dep.getName());
	}
}
```
![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)
<details markdown="1">
    <summary><b> Show Answer </b></summary> 
**Output**
```
null
```
</details>
<details markdown="1">
    <summary><b> Explanation </b></summary> 
<blockquote markdown="1">

- The output of the program is `null`. The object `dep` for `Department` isn't initialized with any value. Only `emp` object for `Employee` class is initialized.
- The subclass methods can access `default`, `public`, and `protected` fields.
- Therefore, `dep` object can access the `getName()` method from `Employee` class.
- If the value for instance variable is not initialized, the default value will be assigned to it.For string, the value is `null`.
</blockquote>
</details>

---

11. Find the error in the program.

``` java
package com.example.model;

public class Employee {
	public String name;
	public String address;
	public Employee(String name, String address) {
		super();
		this.name = name;
		this.address = address;
	}	
}

class Department{
	public String team;
	public String product;
	public Department(String team, String product) {
		super();
		this.team = team;
		this.product = product;
	}
}
```
``` java
package com.example;

import com.example.model.Department;
import com.example.model.Employee;

public class Main {
	public static void main(String[] args) {
		Employee emp = new Employee("Arnold","Washington");
		Department dep = new Department("Action","Terminator");
		System.out.println(emp.name);
		System.out.println(dep.team);
	}
}
```

![Complex](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Complex%20(2).svg)
<details markdown="1">
    <summary><b> Show Answer </b></summary> 
<blockquote markdown="1">

-  The class `Department` is not a public class. We can't import the `default` class.
-  Also, we can't create two public classes in the same file. We have to create a seperate file and add the department class as public.
  </blockquote>
</details>

---
