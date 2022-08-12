## Access Modifiers

1: Explain about Access modifier.
<details>
    <summary><b> Show Answer </b></summary> 

- Access modifiers are used to limit the accessibility or visibility of class, method, variable, and constructor.
- There are four type of access modifier.
  - Default
  - Public
  - Private
  - Protected

</details>

---

2: Explain about Default Access modifier.
<details>
    <summary><b> Show Answer </b></summary> 

- If we do not specify the access modifier, the default will be the access modifier.
- When we declare default access modifier, the visibility will be only within the package.
- If we declare class as default, we can't access the class outside the package and we can't import in another class.

</details>

---

3: Explain about Public Access modifier.
<details>
    <summary><b> Show Answer </b></summary> 

- If we specify with public the access modifier, the accessibility will be anywhere within or outside the package
- We can import the class from any package when it is declared as public.

</details>

---

4: Explain about Private Access modifier.
<details>
    <summary><b> Show Answer </b></summary> 

- If we specify with private the access modifier, the accessibility will be within the class.

</details>

---

5: Can we use private variables outside the class?
<details>
    <summary><b> Show Answer </b></summary> 

- No, we can't access the private variables outside the class.
- If we want to use the private variable outside the class, we will have to create public methods to access it.
- In general, we will create getter and setter method to access private variables.

</details>

---

6: Explain about Protected Access modifier.
<details>
    <summary><b> Show Answer </b></summary> 

- If we specify with protected the access modifier, the accessibility will be within the class and subclasses which are extended from it.

</details>

---

7: Explain the difference between private and protected.
<details>
    <summary><b> Show Answer </b></summary> 

| Private                                              |Protected                                             |
|------------------------------------------------------|------------------------------------------------------|
|The visibility is only within the class               |The visibility is only within the class and subcalsses|
|We can use public method to access private variable and private method out side of class   |We can use public method to access protected variable and proctected variable out side of class and subclass |
</details>

---

## Debugg the program

8: Find the error in the program
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
<details>
    <summary><b> Show Answer </b></summary> 

- We can't use private variable outside the class. If we want to access the variable outside the class, we have to use public method such as getter method from the class.

</details>

9: Find the error in the program
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
<details>
    <summary><b> Show Answer </b></summary> 

- We can't use protected variable outside the class. If we want to access the variable outside the class, we have to use public method such as getter method from the class.

</details>

10: Debugg the code and find the output for the program
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
}
```
``` java
package com.example.model;

public class Department extends Employee {
	public String getName() {
		return name;
	}
	public String getAddress() {
		return address;
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
<details>
    <summary><b> Show Answer </b></summary> 

- There is no error in the program. We can access the protected fields from the sub classess. 
- The output of the program is `null`. The object `dep` for `Department` isn't initialized with any value. Only `emp` object for `Employee` is initialized. 
- If the value for instance variable is not initialized, the default value will be assigned to it.For string, the value is `null`.
</details>

11: Find the error in the program

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

<details>
    <summary><b> Show Answer </b></summary>

-  The class `Department` is not a public class. We can't import the `default` class.
-  Also, we can't create two public classes in the same file. We have to create a seperate file and add the department class as public.
  
  ---
