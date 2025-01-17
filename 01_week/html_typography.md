# HTML Typography

Typography plays a significant role in web design, ensuring content is readable, visually appealing, and well-structured. HTML offers various elements to handle text styling and quotations effectively.

## Typography Basics

### **Headings**
- HTML provides six levels of headings, from `<h1>` (most important) to `<h6>` (least important).
- Use headings to define the hierarchy of your content.

```html
<h1>Main Heading</h1>
<h2>Subheading</h2>
<h3>Section Heading</h3>
```

### **Paragraphs**
- The `<p>` tag defines a block of text.
- Use paragraphs to separate blocks of content.

```html
<p>This is a paragraph of text.</p>
```

### **Text Formatting**
- **Bold:** ~~`<b>` ~~or `<strong>` for emphasis.
  ```html
  <strong>Important text</strong>
  ```
- **Italic:** ~~`<i>`~~ or `<em>` for emphasis.
  ```html
  <em>Emphasized text</em>
  ```
- **Underline:** `<u>` for underlined text.
  ```html
  <u>Underlined text</u>
  ```
- **Superscript and Subscript:**
  ```html
  H<sub>2</sub>O (water), E=mc<sup>2</sup>
  ```

## Quotations

### **Blockquote**
- Use the `<blockquote>` tag for long quotes or citations.
- Usually indented by browsers.

```html
<blockquote>
  The only limit to our realization of tomorrow is our doubts of today.
</blockquote>
```

### **Inline Quotes**
- Use the `<q>` tag for short, inline quotes.
- Browsers add quotation marks automatically.

```html
<p>The philosopher said, <q>Knowledge is power.</q></p>
```

### **Citations**
- Use the `<cite>` tag to reference the source of a quote or text.

```html
<cite>Franklin D. Roosevelt</cite>
```

### **Abbreviations**
- Use the `<abbr>` tag to define abbreviations with a tooltip for the full form.

```html
<abbr title="HyperText Markup Language">HTML</abbr>
```

## Combining Typography and Quotations

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Typography and Quotations</title>
</head>
<body>
  <h1>Understanding Typography</h1>
  <p>Typography enhances the readability and structure of your content.</p>

  <h2>Example of Blockquote</h2>
  <blockquote>
    The journey of a thousand miles begins with a single step.
  </blockquote>

  <h2>Inline Quote</h2>
  <p>Lao Tzu said, <q>The journey of a thousand miles begins with a single step.</q></p>

  <h2>Citing Sources</h2>
  <p>This quote is attributed to <cite>Lao Tzu</cite>.</p>

  <h2>Using Abbreviations</h2>
  <p>The term <abbr title="Cascading Style Sheets">CSS</abbr> is essential in web development.</p>
</body>
</html>
```