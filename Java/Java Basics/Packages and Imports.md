1: Why do we need packages?
 <details>
      <summary><b> Show Answer </b></summary> 

- Packages are used to organize classes, interfaces, enums and annotations.
- We can categorize and have secure access.
- It avoids the naming confliction. ie, We can have the same class names when they are in different packages.
- The first line of java program will be the package name. If the name package is not given, it will de in default package.
- They are two types of packages. They are,
    - <span style="color:blue">Built-in Packages</span> - Some examples are java, util, javax and sql etc.
    - <span style="color:blue">User-defined Packages</span> - user has to give packages name to organize. 
</details>

---

2: Why do we need imports?
<details>
    <summary><b> Show Answer </b></summary> 

- To get the access of classes from another package imports are used.
- The special character <span style="color:blue">*</span> is used to select all classes, interfaces, enums and annotation.
- We can also import the particular class of the package which will avoid neccessary imports and increases the performance.
</details>

---

3: What will happen when we use <span style="color:blue">*</span> while we use import?
 <details>
      <summary><b> Show Answer </b></summary> 

- <span style="color:blue">*</span> will import all the classes, interfaces, enums and annotations.
- It will not import the sub packages and components in sub packages.
- If we want to import sub package, we will have to specify the sub package.

---

4: Can you tell about the naming covertion of packages?
 <details>
      <summary><b> Show Answer </b></summary> 
  
  - To avoid naming collision in name with class interface, the package name should be in small letters.
  - The naming shold be in reverse form of the domain.
  - If the domain is `example.com`, the package name should be `com.example` which reverse od domain.
  - We can add subpackages along with this like `com.example.packagename`.
  - The special characters are not allowed for naming
  - If the domain contains number, we have to use underscore. `12example.com` domain can be coverted as package name as `com._12example`.
   
   ---
