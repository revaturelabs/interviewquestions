1. What is a CSS selector?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

CSS selectors are used to select the content you want to style. Selectors are the part of CSS rule set. CSS selectors select HTML elements according to its id, class, type, attribute etc.

There are several different types of selectors in CSS.

- CSS Element Selector
- CSS Id Selector
- CSS Class Selector
- CSS Universal Selector
- CSS Group Selector

</blockquote>
</details>

---

2. What is contextual selector?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Contextual selector addresses specific occurrence of an element. It is a string of individual selectors separated by white space (search pattern), where only the last element in the pattern is addressed providing it matches the specified context.

- It also checks the context of the class in the html tree, assigning the style to the element through a specific route, taking into account the order of depth in the tree.

**Example**:

```CSS
table p { property: value; } 
```
</blockquote>
</details>

---

3. Why do we use pseudo-class?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- A pseudo-class is used to define a special state of an element.
- For example, it can be used to:
  - Style an element when a user mouses over it.
  - Style visited and unvisited links differently.
  - Style an element when it gets focus.
  - Pseudo-class names are not case-sensitive.
  - Pseudo-classes can be combined with HTML classes.

- When you hover over the link in the example, it will change color:

```CSS
    selector:pseudo-class {
    property: value;
    }
    Like 
    /* mouse over link */
    a:hover {
    color: #FF00FF;
    }
    
    /* selected link */
    a:active ;
    color: #0000FF;
    }
```
</blockquote>
</details>

---

4. What are some pseudo classes you have used?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- pseudo class tells us specific state of an element. allow to style element dynamically. The most popular one is `:hover`. Besides i have used `:visited`, `:focus`, `:nth-child`,` nth-of-type`, `:link`, etc.

- pseudo classes is better if we don't want to mess up with JavaScript however, pseudo-classes is slow to process and apply rules.

</blockquote>
</details>

---

5. How do you optimize CSS selectors?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

This is very open and depend on what we are trying to achieve. If we order selectors in terms of render speed it would be like id, class, tag, siblings, child, descendant, universal, attribute, pseudo. Speed of ID and class is very close. However, your code should be readable, maintainable and DRY along with highly performant.

</blockquote>
</details>

---

6. Describe pseudo-elements and discuss what they are used for.

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

A CSS pseudo-element is a keyword added to a selector that lets you style a specific part of the selected element(s). They can be used for decoration (`:first-line, :first-letter`) or adding elements to the markup (combined with content: ...) without having to modify the markup (`:before, :after`).

Example of usage:

- `:first-line and :first-letter` can be used to decorate text.
- Used in the `.clearfix` hack to add a zero-space element with clear: both.
- Triangular arrows in tooltips use `:before and :after`. Encourages separation of concerns because the triangle is considered part of styling and not really the DOM, but not really possible to draw a triangle with just CSS styles.

</blockquote>
</details>

---

7. How a browser determines what elements match a CSS selector?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Browsers match selectors from rightmost (key selector) to left. Browsers filter out elements in the DOM according to the key selector and traverse up its parent elements to determine matches. The shorter the length of the selector chain, the faster the browser can determine if that element matches the selector.

For example with this selector p span, browsers firstly find all the `<span>` elements and traverse up its parent all the way up to the root to find the `<p>` element. For a particular `<span>`, as soon as it finds a `<p>`, it knows that the `<span>` matches and can stop its matching.

</blockquote>
</details>

---
