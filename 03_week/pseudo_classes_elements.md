# CSS Pseudo-Classes and Pseudo-Elements

Pseudo-classes and pseudo-elements are powerful tools in CSS that allow you to style elements based on their state or specific parts of their content without adding extra HTML.

## Pseudo-Classes
A **pseudo-class** selects elements based on their state, position, or interaction. It’s written as `selector:pseudo-class {}`.

### Common Pseudo-Classes

### Hover, Focus, and Active
Used for interactive elements like buttons and links.

```css
a:hover {
  color: red; /* Changes color when hovered */
}

input:focus {
  border-color: blue; /* Highlights input when clicked */
}

button:active {
  background-color: darkblue; /* Changes color when clicked */
}
```

### First and Last Child
Targets the first or last element within a parent.

```css
p:first-child {
  font-weight: bold;
}

p:last-child {
  font-style: italic;
}
```

### nth-Child and nth-of-Type
Allows targeting elements in a pattern.

```css
li:nth-child(odd) {
  background-color: lightgray; /* Styles every odd list item */
}

li:nth-child(3) {
  color: blue; /* Styles the third list item */
}

p:nth-of-type(2) {
  color: red; /* Styles only the second paragraph inside a section */
}
```

### Empty, Not, and Checked

```css
div:empty {
  border: 1px solid red; /* Styles empty divs */
}

input:not([type="text"]) {
  background: lightblue; /* Styles all inputs except text inputs */
}

input:checked {
  outline: 2px solid green; /* Highlights selected checkboxes or radio buttons */
}
```

## Pseudo-Elements
A **pseudo-element** selects and styles specific parts of an element’s content. It’s written as `selector::pseudo-element {}` (with double colons `::`).

### First Letter and First Line
Used for typography styling.

```css
p::first-letter {
  font-size: 2em;
  font-weight: bold;
  color: red;
}

p::first-line {
  font-style: italic;
}
```

### Selection Styling
Changes how text appears when highlighted by the user.
```css
p::selection {
  background: yellow;
  color: black;
}
```

### Before and After
Adds content before or after an element without modifying the HTML.

```css
h1::before {
  content: "🔥 "; /* Adds an emoji before every h1 */
}

h1::after {
  content: " 🎉"; /* Adds an emoji after every h1 */
}
```

## Practical Use Cases

**Highlight required form fields:**
```css
input:required {
  border: 2px solid red;
}
```
**Create a striped table with nth-child:**
```css
tr:nth-child(even) {
  background-color: #f2f2f2;
}
```
**Style placeholder text:**
```css
input::placeholder {
  color: gray;
  font-style: italic;
}
```

## Summary
- **Pseudo-classes** apply styles based on state (`:hover`, `:nth-child`, `:checked`).
- **Pseudo-elements** style parts of an element (`::before`, `::after`, `::first-letter`).
- Use `::before` and `::after` for content injection.
- `:not()` helps exclude elements from styles.
