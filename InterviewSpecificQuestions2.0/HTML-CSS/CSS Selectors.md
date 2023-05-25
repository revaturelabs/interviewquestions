1. What are CSS selectors and list their types.

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

8. What is the universal selector in CSS?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The universal selector, denoted by an asterisk (*), targets all elements on a webpage.

</blockquote>
</details>

---

9. What is the element selector in CSS?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The element selector targets elements based on their HTML tag name. For example, to target all `<p>` elements, you would use the selector `p`.

</blockquote>
</details>

---

10. How do you select elements with a specific class in CSS?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

To select elements with a specific class, you use the class selector. It is denoted by a period followed by the class name. For example, to target elements with the class "highlight", you would use the selector `.highlight`.

</blockquote>
</details>

---

11. How do you select elements with a specific ID in CSS?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

To select elements with a specific ID, you use the ID selector. It is denoted by a hash (#) followed by the ID name. For example, to target an element with the ID "header", you would use the selector #header.

</blockquote>
</details>

---

12. How do you select elements based on their attributes in CSS?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

You can select elements based on their attributes using attribute selectors. There are several types of attribute selectors, including selecting elements with a specific attribute, a specific attribute value, or specific attribute value patterns.

</blockquote>
</details>

---

13. What is the descendant selector in CSS?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The descendant selector selects elements that are descendants of a specific parent element. It is denoted by a space between two selectors. For example, to target all `<a>` elements within a `<div>`, you would use the selector `div a`.

</blockquote>
</details>

---

14. What is the child selector in CSS?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The child selector selects elements that are direct children of a specific parent element. It is denoted by a greater-than sign (>). For example, to target all `<li>` elements that are direct children of a `<ul>`, you would use the selector `ul > li`.

</blockquote>
</details>

---

15. What is the adjacent sibling selector in CSS?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The adjacent sibling selector, denoted by a plus sign (+), selects an element that is immediately preceded by another specific element. For example, to target a `<p>` element that directly follows a `<h2>` element, you would use the selector `h2 + p`.

</blockquote>
</details>

---

16. What is the general sibling selector in CSS?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The general sibling selector, denoted by a tilde (~), selects elements that follow a specific element. Unlike the adjacent sibling selector, it doesn't require the elements to be immediately adjacent. For example, to target all `<p>` elements that follow a `<h2>` element, you would use the selector `h2 ~ p`.

</blockquote>
</details>

---

17. What is the :not() selector in CSS?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The `:not()` selector is used to select elements that do not match a specific selector. It allows you to exclude certain elements from a selection. For example, to select all paragraphs except those with the class "highlighted", you would use the selector `p:not(.highlighted)`.

</blockquote>
</details>

---

18. What is the :nth-child() selector in CSS?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The `:nth-child()` selector allows you to select elements based on their position in a parent container. It accepts an argument in the form of `an+b`, where `a` and `b` are integers or keywords. For example, to select every odd `<li>` element within a `<ul>`, you would use the selector `ul li:nth-child(odd)`.

</blockquote>
</details>

---

19. What is the :hover selector in CSS used for?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The `:hover` selector is a pseudo-class that selects an element when the user hovers over it with their mouse. It is commonly used to apply styles such as changing the background color, adding transitions, or showing additional information when hovering over an element.

</blockquote>
</details>

---

20. What is the :focus selector in CSS used for?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The `:focus` selector is a pseudo-class that selects an element when it receives focus, typically through user interaction like clicking or tabbing onto the element. It is commonly used to style form inputs or create interactive elements.

</blockquote>
</details>

---

21. How do you select the first child element of a parent using CSS?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

To select the first child element of a parent, you can use the `:first-child` selector. For example, to target the first `<p>` element within a `<div>`, you would use the selector `div p:first-child`.

</blockquote>
</details>

---

22. How do you select the last child element of a parent using CSS?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

To select the last child element of a parent, you can use the `:last-child` selector. For example, to target the last `<li>` element within a `<ul>`, you would use the selector `ul li:last-child`.

</blockquote>
</details>

---

23. What is the difference between the child combinator (>) and the descendant combinator (space) in CSS?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The child combinator (`>`) selects only the direct children of an element, whereas the descendant combinator (space) selects all descendants regardless of their level of nesting. For example, `ul > li` selects only the `<li>` elements that are direct children of a `<ul>`, while `ul li` selects all `<li>` elements that are descendants of a `<ul>`.

</blockquote>
</details>

---

24. How does the :empty selector work in CSS?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The `:empty` selector targets elements that have no child elements or text content. It selects elements that are completely empty. For example, `p:empty` selects all empty `<p>` elements.

</blockquote>
</details>

---

25. What is the :checked selector used for in CSS?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The `:checked` selector targets elements that are checked, typically used with input elements like checkboxes or radio buttons. It allows you to apply styles to checked elements or control their appearance. For example, `input[type="checkbox"]:checked` targets checked checkboxes.

</blockquote>
</details>

---

26. What is the :first-of-type selector in CSS used for?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The `:first-of-type` selector selects the first element of its type among siblings. It targets elements based on their position relative to siblings of the same element type. For example, `h2:first-of-type` selects the first `<h2>` element among its siblings.

</blockquote>
</details>

---

27. How does the :focus-within selector work in CSS?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The `:focus-within` selector targets a parent element when any of its descendants are focused. It is used to apply styles to a container when an element within it gains focus. For example, `.container:focus-within` selects a container element when any of its descendant elements receive focus.

</blockquote>
</details>

---

28. What is the :target selector used for in CSS?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The `:target` selector targets the element that is currently being targeted by a URL fragment identifier (e.g., a specific section of a webpage). It allows you to style the targeted element dynamically. For example, `#section1:target` selects the element with the ID "section1" when it is the target of a URL.

</blockquote>
</details>

---

29. How does the :lang() selector work in CSS?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The `:lang()` selector targets elements based on the language specified in their `lang` attribute. It allows you to style elements based on their language. For example, `p:lang(fr)` selects all `<p>` elements with the language attribute set to "fr" (French).

</blockquote>
</details>

---

30. What is the :not() selector used for in combination with other selectors?

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The `:not()` selector can be used in combination with other selectors to create more specific selections while excluding certain elements. It helps to refine the targeting of elements. For example, `div:not(.special):not(.featured)` selects all `<div>` elements that do not have the classes "special" or "featured"

</blockquote>
</details>

---