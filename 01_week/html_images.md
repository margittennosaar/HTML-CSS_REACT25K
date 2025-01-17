# HTML Images

Images are a vital part of web design, adding visual appeal and enhancing content. HTML provides powerful tools to include and control images on your web pages. Here’s how you can work with images in HTML.

## The `<img>` Tag
- The `<img>` tag is used to embed images in a web page.
- It is a self-closing tag, meaning it does not require a closing `</img>` tag.

```html
<img src="image.jpg" alt="Description of the image">
```

### Attributes of the `<img>` Tag

#### **`src` (Source)**
- Specifies the path to the image file.
- Can be:
  - **Absolute URL:** A full web address.
    ```html
    <img src="https://example.com/image.jpg" alt="Example Image">
    ```
  - **Relative URL:** A path relative to your HTML file.
    ```html
    <img src="images/photo.jpg" alt="Photo">
    ```

#### **`alt` (Alternative Text)**
- Provides a text description of the image.
- Essential for accessibility and is displayed if the image fails to load.
  ```html
  <img src="image.jpg" alt="A scenic mountain view">
  ```

#### **`width` and `height`**
- Set the dimensions of the image (in pixels or percentages).
  ```html
  <img src="image.jpg" alt="Example" width="300" height="200">
  ```

#### **`title`**
- Adds a tooltip when the user hovers over the image.
  ```html
  <img src="image.jpg" alt="Example" title="Hover text">
  ```

## Responsive Images

### Using CSS
Make images responsive by setting their maximum width to 100% and height to auto:
```css
img {
  max-width: 100%;
  height: auto;
}
```

### Using the `<picture>` Element
The `<picture>` element provides multiple sources for different screen sizes:
```html
<picture>
  <source srcset="image-large.jpg" media="(min-width: 800px)">
  <source srcset="image-small.jpg" media="(max-width: 799px)">
  <img src="image-default.jpg" alt="Responsive Image">
</picture>
```
## Image Formats

### Common Formats
- **JPEG:** Best for photographs; supports millions of colors.
- **PNG:** Supports transparency and high-quality images.
- **GIF:** Suitable for simple animations.
- **WebP:** Modern format with better compression and quality.
- **SVG:** Scalable Vector Graphics, ideal for icons and illustrations.

### Choosing the Right Format
- Use **JPEG** for photos to save space.
- Use **PNG** for images requiring transparency.
- Use **WebP** when supported for better performance.

## Accessibility Best Practices
- Always include the `alt` attribute with meaningful descriptions.
- Use `role="img"` for decorative images with ARIA labels when needed.
- Avoid using images for text unless absolutely necessary.


## Example: Comprehensive Image Usage

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>HTML Images</title>
  <style>
    img {
      max-width: 100%;
      height: auto;
      border: 1px solid #ccc;
    }
  </style>
</head>
<body>
  <h1>Working with Images</h1>

  <h2>Basic Image</h2>
  <img src="image.jpg" alt="A beautiful view of the sunset">

  <h2>Responsive Image</h2>
  <picture>
    <source srcset="large.jpg" media="(min-width: 800px)">
    <source srcset="small.jpg" media="(max-width: 799px)">
    <img src="default.jpg" alt="Responsive example">
  </picture>

  <h2>Decorative Image</h2>
  <img src="decorative.jpg" alt="" role="img">
</body>
</html>
```