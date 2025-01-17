# Setting Up a Static HTML Project

Creating a static HTML project is the first step in building a website. This guide walks you through setting up a simple project structure for your HTML, CSS, and JavaScript files.


## Step 1: Create a Project Folder
1. **Create a new folder:**
   - Name it something meaningful, like `my-website` or `html-project`.

2. **Inside the folder, create subfolders:**
   - `css/`: For your stylesheets.
   - `js/`: For your JavaScript files.
   - `images/`: For storing images or media assets.

Your folder structure should look like this:
```
my-website/
├── css/
├── js/
├── images/
└── index.html
```

---

## Step 2: Create an HTML File
1. **Create a file named `index.html`** in the root of your project folder.
2. Add the basic HTML structure:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>My Static Website</title>
  <link rel="stylesheet" href="css/styles.css">
</head>
<body>
  <h1>Welcome to My Static Website</h1>
  <p>This is a simple static HTML project setup.</p>
  <script src="js/script.js"></script>
</body>
</html>
```

## Step 3: Add a CSS File
1. In the `css/` folder, create a file named `styles.css`.
2. Add some basic styles:

```css
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
  background-color: #f4f4f9;
  color: #333;
}

h1 {
  color: #0056b3;
  text-align: center;
  margin-top: 20px;
}
```

## Step 4: Add a JavaScript File
1. In the `js/` folder, create a file named `script.js`.
2. Add a simple script:

```javascript
console.log("Hello, world! Welcome to my static website.");
```

## Step 5: Test Your Project
1. Open the `index.html` file in your browser by double-clicking it.
2. Verify that:
   - The text appears with the styles applied.
   - The browser console shows the message from `script.js`.

## Step 6: Optional Enhancements

### Add More Pages
- Create additional HTML files, like `about.html` or `contact.html`.
- Link them using `<a>` tags:
  ```html
  <a href="about.html">About</a>
  ```

### Organize Images
- Place all image files in the `images/` folder.
- Use relative paths to include them in your HTML:
  ```html
  <img src="images/photo.jpg" alt="A sample image">
  ```

### Add a Favicon
- Place a small image (e.g., `favicon.ico`) in the root folder.
- Link it in the `<head>` section:
  ```html
  <link rel="icon" href="favicon.ico" type="image/x-icon">
  ```

## Final Project Folder Structure
```
my-website/
├── css/
│   └── styles.css
├── js/
│   └── script.js
├── images/
│   └── photo.jpg
├── favicon.ico
└── index.html
```
