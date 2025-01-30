# CSS Fonts, Colors, and Backgrounds

## Fonts in CSS

### Setting a Font Family
CSS allows you to define the font style of your text using `font-family`.
```css
body {
  font-family: Arial, sans-serif;
}
```
- Use **fallback fonts** to ensure readability if the primary font is unavailable.
- Example: `font-family: 'Roboto', Arial, sans-serif;`

Sure! Here’s an **easy way** to add Google Fonts to your website using two methods: **importing in CSS** and **linking in the `<head>` section**.


### **1. Linking Google Fonts in the `<head>` (Recommended)**
This is the easiest method! You add a `<link>` inside the `<head>` of your HTML file.

#### **Steps:**
1. Go to [Google Fonts](https://fonts.google.com/).
2. Select a font you like.
3. Copy the `<link>` tag provided.
4. Paste it inside the `<head>` of your HTML file.

```html
<head>
  <link href="https://fonts.googleapis.com/css2?family=Open+Sans:wght@400;700&display=swap" rel="stylesheet">
</head>
```

5. Now, use the font in your CSS:
```css
body {
  font-family: 'Open Sans', sans-serif;
}
```

✔️ **Best for beginners** – quick and works right away!


### **2. Importing Google Fonts in CSS**
This method adds Google Fonts inside your CSS file using `@import`.

#### **Steps:**
1. Go to [Google Fonts](https://fonts.google.com/) and choose a font.
2. Copy the `@import` link.
3. Paste it at the **top** of your CSS file.

```css
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap');

body {
  font-family: 'Roboto', sans-serif;
}
```

✔️ **Great for modular CSS** – but loads fonts slightly slower than the `<link>` method.


### **Which One Should You Use?**
- **Use the `<link>` method** if you want a faster page load and better performance.
- **Use `@import`** if you want to include fonts inside a specific CSS file.

### Font Styling Properties
- `font-size`: Adjusts text size.
- `font-weight`: Defines text thickness (`normal`, `bold`, `lighter`, or numerical values like `400`, `700`).
- `font-style`: `normal`, `italic`, or `oblique`.
- `text-transform`: `uppercase`, `lowercase`, or `capitalize`.

Example:
```css
h1 {
  font-size: 2rem;
  font-weight: bold;
  text-transform: uppercase;
}
```

## Colors in CSS

### Setting Colors
CSS supports multiple color formats:
- **Named Colors**: `red`, `blue`, `green`
- **HEX Codes**: `#ff5733`
- **RGB Values**: `rgb(255, 87, 51)`
- **RGBA (Transparency)**: `rgba(255, 87, 51, 0.5)`
- **HSL/HSLA**: `hsl(0, 100%, 50%)`

Example:
```css
p {
  color: #333;
}
```

### Applying Transparency
RGBA allows transparency control.
```css
h2 {
  color: rgba(255, 0, 0, 0.5);
}
```

### Using CSS Variables for Colors
CSS variables make it easier to manage a consistent color scheme.
```css
:root {
  --primary-color: #3498db;
  --secondary-color: #2ecc71;
}

button {
  background-color: var(--primary-color);
  color: white;
}
```

## Backgrounds in CSS

### Setting Background Color
```css
body {
  background-color: #f4f4f4;
}
```

### Applying Background Images
```css
.hero {
  background-image: url('background.jpg');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
}
```
- **`background-size`**: `cover` (scales to fit), `contain` (fits inside container), or specific values (`100% 100%`).
- **`background-position`**: `center`, `top left`, `50% 50%`.
- **`background-repeat`**: `no-repeat`, `repeat`, `repeat-x`, `repeat-y`.

### Gradient Backgrounds
```css
section {
  background: linear-gradient(to right, #ff7e5f, #feb47b);
}
```

### Overlay Effect
To add a color overlay on a background image:
```css
.overlay {
  background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), url('image.jpg');
  background-size: cover;
}
```


## Best Practices
- Use readable font sizes and line heights for accessibility.
- Stick to a **limited color palette** for a consistent design.
- Optimize background images to avoid slowing down page load times.


