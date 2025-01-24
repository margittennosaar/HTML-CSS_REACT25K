# CSS Syntax, Selectors, Specificity, Inheritance, and Cascade

## CSS Syntax
CSS rules follow this basic structure:
```css
selector {
  property: value;
}
```
- **Selector**: Specifies the HTML element(s) to style.
- **Property**: Defines the style attribute (e.g., color, font-size).
- **Value**: Specifies the desired style for the property.

Example:
```css
p {
  color: blue;
  font-size: 16px;
}
```

## Selectors
CSS selectors are used to target HTML elements. Here are the most common types:

### Universal Selector (`*`):**
Targets all elements.

```css
* {
  margin: 0;
  padding: 0;
}
```

### Type Selector:**
Targets elements by their tag name.

```css
h1 {
  color: red;
}
```

### Class Selector (`.`):**
Targets elements with a specific class.

```css
.card {
  background-color: lightgray;
}
```

### ID Selector (`#`):**
Targets a single element with a specific ID.

```css
#header {
  text-align: center;
}
```

### Combinators**
Define relationships between elements:

#### Descendant Combinator (` `):
Targets elements inside another element.
```css
div p {
  color: gray;
}
```

#### Child Combinator (`>`):
Targets direct children of an element.
```css
ul > li {
  list-style: square;
}
```

#### Adjacent Sibling Combinator (`+`):
Targets the next sibling of an element.
```css
h1 + p {
  font-size: 14px;
}
```

#### General Sibling Combinator (`~`):
Targets all siblings of an element.
```css
h1 ~ p {
  color: blue;
}
```

## Specificity
Specificity determines which CSS rule is applied when multiple rules target the same element. Higher specificity overrides lower specificity.

### Specificity Weight:
1. **Inline styles**: `1000`
2. **ID selectors**: `100`
3. **Classes, attributes, pseudo-classes**: `10`
4. **Type selectors and pseudo-elements**: `1`

```css
/* Specificity: 1 */
p {
  color: black;
}

/* Specificity: 10 */
.text {
  color: blue;
}

/* Specificity: 100 */
#highlight {
  color: green;
}

/* Inline style: 1000 */
<p style="color: red;">Red text</p>
```

## Inheritance
Some CSS properties, like `color` and `font-family`, are **inherited** by child elements, while others (e.g., `margin` and `padding`) are not.

### Forcing inheritance:
Use `inherit` to explicitly inherit a property:
```css
p {
  color: inherit;
}
```

Example:
```html
<div style="color: red;">
  <p>This paragraph inherits red color.</p>
</div>
```

## Cascade
The cascade determines how CSS rules are applied when there are conflicts:
1. **Importance**: Rules with `!important` override all others.
2. **Specificity**: More specific selectors take precedence.
3. **Source Order**: Later rules overwrite earlier ones.

```css
/* Lowest priority */
p {
  color: black;
}

/* Higher specificity */
.text {
  color: blue;
}

/* Inline style: Highest specificity */
<p style="color: red;">This is red text</p>

/* !important: Overrides everything */
p {
  color: green !important;
}
```

## Practical Example
Combine what you’ve learned to style a simple layout:

HTML:
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>CSS Fundamentals</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <header id="main-header" class="header">
    <h1>Welcome to CSS Basics</h1>
  </header>
  <nav class="nav">
    <a href="#">Home</a>
    <a href="#">About</a>
    <a href="#">Contact</a>
  </nav>
  <main class="content">
    <p>This is the main content area.</p>
  </main>
</body>
</html>
```

CSS:
```css
/* Universal Selector */
* {
  margin: 0;
  padding: 0;
}

/* ID Selector */
#main-header {
  background-color: lightblue;
  padding: 20px;
}

/* Class Selector */
.nav {
  text-align: center;
}

.nav a {
  margin: 0 10px;
  color: blue;
  text-decoration: none;
}

/* Type Selector */
p {
  font-size: 16px;
  line-height: 1.5;
}
```


