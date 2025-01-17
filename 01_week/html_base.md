# HTML Base

HTML (HyperText Markup Language) is the foundation of web development. It provides the structure of a web page, defining the content and how it is organized. Let's explore the essential concepts to get started with HTML.

## How It Works?

HTML works as the backbone of a web page. Here's how:

1. **HTML Documents:**
   - HTML files are plain text files with a `.html` extension.
   - Browsers interpret these files to display content.

2. **Structure:**
   - HTML organizes content into elements, each defined by tags.
   - Elements can contain text, images, links, or other elements.

3. **Rendering:**
   - Browsers read the HTML document, apply styles (CSS), and execute scripts (JavaScript) to create the final web page.

## HTML DOM (Document Object Model)

The DOM represents the structure of an HTML document as a tree of objects:

- **Root Element:**
  - `<html>` is the root of the document.
- **Nested Elements:**
  - `<head>`: Contains metadata and links to resources (e.g., CSS, JavaScript).
  - `<body>`: Contains visible content.

Example DOM structure:
```html
<!DOCTYPE html>
<html>
  <head>
    <title>My Web Page</title>
  </head>
  <body>
    <h1>Welcome!</h1>
    <p>This is a paragraph.</p>
  </body>
</html>
```

## HTML Attributes

Attributes provide additional information about elements:

- **Syntax:**
  ```html
  <tag attribute="value">Content</tag>
  ```

- **Common Attributes:**
  - `id`: Uniquely identifies an element.
    ```html
    <div id="main">Content</div>
    ```
  - `class`: Groups elements for styling.
    ```html
    <p class="highlight">Text</p>
    ```
  - `src`: Specifies the source for media (e.g., images, videos).
    ```html
    <img src="image.jpg" alt="Description">
    ```
  - `alt`: Provides alternative text for images.
    ```html
    <img src="logo.png" alt="Company Logo">
    ```
  - `href`: Specifies the destination for links.
    ```html
    <a href="https://example.com">Visit</a>
    ```

## Comments

Comments are ignored by browsers but help developers document their code:

```html
<!-- This is a comment -->
<p>This is visible content.</p>
```

## Including CSS and JavaScript Files

1. **CSS (Cascading Style Sheets):**
   - Add styles to your HTML content.
   - Use a `<link>` tag to include an external CSS file:
     ```html
     <link rel="stylesheet" href="styles.css">
     ```

2. **JavaScript:**
   - Add interactivity to your web page.
   - Use a `<script>` tag to include an external JavaScript file:
     ```html
     <script src="script.js"></script>
     ```

## Practical Example

Here's a complete example combining everything:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>HTML Basics</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <h1>Welcome to HTML Basics</h1>
  <p>This page demonstrates HTML essentials.</p>
  <img src="example.jpg" alt="An example image">
  <a href="https://example.com">Learn More</a>
  <script src="script.js"></script>
</body>
</html>
```