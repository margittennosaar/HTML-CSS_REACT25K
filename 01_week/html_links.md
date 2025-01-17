# HTML Links

Links are one of the most important features of HTML, enabling navigation between web pages and resources. This guide covers everything you need to know about creating and managing links in HTML.

## What is a Link?
- An **HTML link** is created using the `<a>` (anchor) tag.
- Links connect web pages, external resources, files, or specific parts of a page.

```html
<a href="https://example.com">Visit Example</a>
```

## Attributes of the `<a>` Tag

### **`href` (Hypertext Reference)**
- Specifies the destination of the link.
- Can be:
  - **Absolute URL** (full web address):
    ```html
    <a href="https://www.google.com">Google</a>
    ```
  - **Relative URL** (path to a resource on the same site):
    ```html
    <a href="about.html">About Us</a>
    ```

### **`target`**
- Defines where to open the linked document.
- Common values:
  - `_self` (default): Opens in the same tab.
    ```html
    <a href="home.html" target="_self">Home</a>
    ```
  - `_blank`: Opens in a new tab.
    ```html
    <a href="https://example.com" target="_blank">Visit Example</a>
    ```

### **`title`**
- Adds a tooltip when hovering over the link.
  ```html
  <a href="contact.html" title="Go to Contact Page">Contact</a>
  ```

### **`rel`**
- Specifies the relationship between the current document and the linked resource.
  - Common values:
    - `nofollow`: Prevents search engines from following the link.
    - `noopener noreferrer`: Enhances security when opening links in new tabs.
  ```html
  <a href="https://example.com" rel="noopener noreferrer">Secure Link</a>
  ```

## Types of Links

### **External Links**
- Direct to another website.
  ```html
  <a href="https://www.wikipedia.org">Wikipedia</a>
  ```

### **Internal Links**
- Navigate within the same website.
  ```html
  <a href="about.html">About Us</a>
  ```

### **Email Links**
- Opens the default email client to send an email.
  ```html
  <a href="mailto:someone@example.com">Send Email</a>
  ```

### **Telephone Links**
- Opens the phone dialer on mobile devices.
  ```html
  <a href="tel:+1234567890">Call Us</a>
  ```

### **Anchor Links**
- Navigate to a specific section of the same page or another page using IDs.
  ```html
  <!-- Link -->
  <a href="#section1">Go to Section 1</a>

  <!-- Target Section -->
  <h2 id="section1">Section 1</h2>
  ```

## Styling Links

### Basic CSS Styling
- Change link color:
  ```css
  a {
    color: blue;
  }
  ```

- Remove underline:
  ```css
  a {
    text-decoration: none;
  }
  ```

### Pseudo-Classes for Links
- Use CSS pseudo-classes to style links based on their state:
  - `:link`: Default state of unvisited links.
  - `:visited`: Links already clicked.
  - `:hover`: When the user hovers over a link.
  - `:active`: When the link is clicked.

```css
a:link {
  color: blue;
}
a:visited {
  color: purple;
}
a:hover {
  text-decoration: underline;
}
a:active {
  color: red;
}
```

## Example: Comprehensive Link Usage

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>HTML Links</title>
  <style>
    a {
      color: blue;
      text-decoration: none;
    }
    a:hover {
      text-decoration: underline;
    }
  </style>
</head>
<body>
  <h1>HTML Links</h1>
  <p><a href="https://example.com" target="_blank" title="Go to Example">Visit Example</a></p>
  <p><a href="about.html">About Us</a></p>
  <p><a href="mailto:info@example.com">Email Us</a></p>
  <p><a href="tel:+1234567890">Call Us</a></p>
  <p><a href="#section1">Jump to Section 1</a></p>

  <h2 id="section1">Section 1</h2>
  <p>This is Section 1.</p>
</body>
</html>
```