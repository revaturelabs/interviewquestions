## Packages and Imports

1.Why do we need packages?

![Medium](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/Medium%20(2).svg)
<details markdown="1">
    <summary><b> Show Answer </b></summary> 
<blockquote markdown="1">

- Packages are used to organize classes, interfaces, enums and annotations.
- We can categorize and have secure access.
- It avoids the naming confliction. ie, We can have the same class names when they are in different packages.
- The first line of java program will be the package name. If the name package is not given, it will de in default package.
- They are two types of packages. They are,
    - **Built-in Packages** - Some examples are java, util, javax and sql etc.
    - **User-defined Packages** - user has to give packages name to organize. 

</blockqoute> 
</details>

---

2.What is the purpose of `import` statement?

![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)
<details markdown="1">
    <summary><b> Show Answer </b></summary> 
<blockquote markdown="1">

- To get the access of classes/interfaces/enumns from another package, we need to use `import` statement.
- Example: `import java.util.*` or `import java.util.Scanner`
- The special character <span style="color:blue">*</span> is used to select all classes, interfaces, enums and annotation from the package.
- We can also import the particular class of the package which will avoid neccessary imports and increases the performance.
</blockqoute> 
</details>

---

3.What will happen when we use `*` while we use import?

 ![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)
<details markdown="1">
    <summary><b> Show Answer </b></summary> 
<blockquote markdown="1">

- `*` will import all the classes, interfaces, enums and annotations.
- It will not import the sub packages and components in sub packages.
- If we want to import sub package, we will have to specify the sub package.
</blockqoute> 
</details>

---

4.Can you tell about the naming convention of packages?

 ![Easy](https://raw.githubusercontent.com/revaturelabs/interviewquestions/aef8eff919a3b083089641381ed9a9101ed21fba/ComplexityTags/simple%20(2).svg)
<details markdown="1">
    <summary><b> Show Answer </b></summary> 
<blockquote markdown="1">
  
  - To avoid naming collision in name with class interface, the package name should be in small letters.
  - The naming should be in reverse form of the domain.
  - If the domain is `example.com`, the package name should be `com.example` which is reverse form of domain.
  - We can add subpackages along with `com.example` like `com.example.packagename`.
  - The special characters are not allowed for naming a  packages.
  - If the domain contains number, we have to use underscore. `12example.com` domain can be coverted as package name as `com._12example`.
 
</blockqoute> 
</details>
 
---
