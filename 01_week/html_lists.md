# HTML Lists

Lists are a fundamental way to organize and display content in a structured and readable format. HTML provides several types of lists to suit different needs.

## Types of HTML Lists

### 1. **Unordered List (`<ul>`)**
- Displays items with bullet points by default.
- Ideal for lists where the order doesn’t matter.

```html
<ul>
  <li>Item 1</li>
  <li>Item 2</li>
  <li>Item 3</li>
</ul>
```

### 2. **Ordered List (`<ol>`)**
- Displays items with numbers or letters.
- Ideal for lists where the order matters.

```html
<ol>
  <li>Step 1</li>
  <li>Step 2</li>
  <li>Step 3</li>
</ol>
```

### 3. **Definition List (`<dl>`)**
- Used to define terms and their descriptions.
- Consists of `<dt>` (term) and `<dd>` (description).

Example:
```html
<dl>
  <dt>HTML</dt>
  <dd>HyperText Markup Language</dd>
  <dt>CSS</dt>
  <dd>Cascading Style Sheets</dd>
</dl>
```

## Nesting Lists
Lists can be nested to create multi-level structures.

```html
<ul>
  <li>Fruits
    <ul>
      <li>Apple</li>
      <li>Banana</li>
    </ul>
  </li>
  <li>Vegetables
    <ul>
      <li>Carrot</li>
      <li>Broccoli</li>
    </ul>
  </li>
</ul>
```

---

## Attributes for Lists

### **`type` (Ordered Lists)**
- Changes the numbering style.
- Values: `1`, `A`, `a`, `I`, `i`.

```html
<ol type="A">
  <li>Option A</li>
  <li>Option B</li>
</ol>
```

### **`start` (Ordered Lists)**
- Specifies the starting number.

```html
<ol start="5">
  <li>Item 5</li>
  <li>Item 6</li>
</ol>
```

### **`reversed` (Ordered Lists)**
- Displays the list in reverse order.

```html
<ol reversed>
  <li>Third Place</li>
  <li>Second Place</li>
  <li>First Place</li>
</ol>
```

## Styling Lists with CSS

### Removing Bullets
```css
ul {
  list-style-type: none;
  padding: 0;
}
```

### Customizing Bullets
```css
ul {
  list-style-type: square;
}
```

### Changing Marker Position
```css
ul {
  list-style-position: inside;
}
```

### Styling Ordered List Numbers
```css
ol {
  list-style-type: upper-roman;
}
```

## Example: Comprehensive List Usage

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>HTML Lists</title>
  <style>
    ul {
      list-style-type: square;
      padding-left: 20px;
    }
    ol {
      list-style-type: upper-roman;
      padding-left: 20px;
    }
  </style>
</head>
<body>
  <h1>HTML Lists</h1>

  <h2>Unordered List</h2>
  <ul>
    <li>Apple</li>
    <li>Banana</li>
    <li>Cherry</li>
  </ul>

  <h2>Ordered List</h2>
  <ol type="I">
    <li>Introduction</li>
    <li>Body</li>
    <li>Conclusion</li>
  </ol>

  <h2>Definition List</h2>
  <dl>
    <dt>HTML</dt>
    <dd>HyperText Markup Language</dd>
    <dt>CSS</dt>
    <dd>Cascading Style Sheets</dd>
  </dl>
</body>
</html>
```