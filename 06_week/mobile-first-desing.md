# Mobile-First Design

Mobile-first design means building a website for **mobile devices first**, then making it look great on larger screens. This helps your site load faster, work smoothly, and be easy to use on any device.

## Why start with mobile?
- More people browse on their phones than on computers.
- A mobile-friendly site is **easier to use** for everyone.
- Google gives priority to mobile-friendly websites in search results.

## How to build a Mobile-First website
Start with **simple styles for small screens** and add more for bigger screens.

```css
/* Default styles for mobile */
body {
  font-size: 16px;
  line-height: 1.5;
}

.container {
  display: flex;
  flex-direction: column;
  padding: 10px;
}
```

## Making it work on bigger screens
Use **CSS media queries** to adjust the layout when the screen is wider.

```css
@media (min-width: 768px) {
  .container {
    flex-direction: row;
    justify-content: space-between;
  }
}
```
- `min-width: 768px;` means these styles apply **only** when the screen is at least **768 pixels wide**.
- This way, the design **grows smoothly** as screens get bigger.

## Common screen sizes

| Device   | Screen Width |
| -------- | ------------ |
| Phones   | 0 - 767px    |
| Tablets  | 768 - 1023px |
| Desktops | 1024px+      |

You can change these sizes based on your needs.

## Making images responsive
Images should **resize** based on screen size to load faster and look better.

### The `<picture>` Tag: Show the right image
This method lets you load a smaller image for mobile and a bigger one for large screens.

```html
<picture>
  <source srcset="image-small.jpg" media="(max-width: 767px)">
  <source srcset="image-medium.jpg" media="(max-width: 1023px)">
  <img src="image-large.jpg" alt="A beautiful scene">
</picture>
```
- Phones get the **smallest** image.
- Bigger screens get **larger** images.
- This **saves data** and loads faster.

### `srcset`: Adjust image quality
This method loads clearer images on high-quality screens like **retina displays**.

```html
<img src="image.jpg" 
     srcset="image-2x.jpg 2x, image-3x.jpg 3x" 
     alt="A beautiful scene">
```
- `2x` and `3x` tell the browser to pick the right image **for high-resolution screens**.



