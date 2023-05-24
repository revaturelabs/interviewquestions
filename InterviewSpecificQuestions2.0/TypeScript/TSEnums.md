32. Can u explain a bit about Enum in TypeScript?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Enums or enumerations are a TypeScipt data type that allows us to define a set of named constants. Using enums can make it easier to document intent, or create a set of distinct cases. It is a collection of related values that can be numeric or string values.

**Example**
```typescript
enum Gender {  
  Male,  
  Female  
  Other  
}  
console.log(Gender.Female); // Output: 1  
//We can also access an enum value by its number value.  
console.log(Gender[1]); // Output: Female  
```

</blockquote>
</details>

---
