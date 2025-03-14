# Advanced CSS: Modern Features & Tricks

CSS has evolved significantly, introducing powerful features that improve styling, maintainability, and performance. 

## CSS Variables (Custom Properties)
CSS Variables allow you to **store and reuse values** throughout your stylesheets.

```css
:root {
  --primary-color: #3498db;
  --font-size-large: 20px;
}

body {
  color: var(--primary-color);
  font-size: var(--font-size-large);
}
```
Easy **theme customization**, better **code maintainability**, and dynamic updates with JavaScript.

## `clamp()`, `min()`, and `max()` for responsive design
These functions **dynamically adjust values** based on screen size.

```css
h1 {
  font-size: clamp(1.5rem, 5vw, 3rem);
}
```
- **Min size**: `1.5rem` (prevents text from being too small)
- **Preferred size**: `5vw` (relative to screen width)
- **Max size**: `3rem` (prevents text from being too big)

```css
div {
  width: min(50vw, 400px); /* Chooses the smaller value */
  height: max(300px, 10vh); /* Chooses the larger value */
}
```
Perfect for responsive typography and layout adjustments.

## Container Queries 
Unlike media queries, **container queries** apply styles based on a parent container’s size rather than the viewport.

### **Example**
```css
@container (min-width: 600px) {
  .card {
    font-size: 20px;
  }
}
```
Ideal for truly reusable components.

## `has()` selector (Parent Selector)
Allows you to **style an element based on its children**.

```css
div:has(img) {
  border: 2px solid red;
}
```
Removes the need for extra classes or JavaScript for parent-child interactions.

## Subgrid in CSS Grid (Advanced Layouts)
Allows nested grids to inherit and align with their parent grid.

```css
.grid-container {
  display: grid;
  grid-template-columns: 1fr 2fr;
}

.grid-item {
  display: grid;
  grid-template-columns: subgrid;
}
```
Maintains alignment across nested elements.

## `scroll-snap` for Smooth Scrolling
Allows precise control over scroll behavior.

### **Example**
```css
.container {
  scroll-snap-type: x mandatory;
}

.item {
  scroll-snap-align: center;
}
```
Great for image sliders, carousels, and full-page scrolling effects.

## `accent-color` for Form Elements
Changes the default color of checkboxes, radio buttons, and range sliders.

```css
input[type="checkbox"] {
  accent-color: #ff5733;
}
```
Easier customization without extra styles.

## `backdrop-filter` for Frosted Glass Effects
Applies effects like blur, brightness, or contrast to elements behind another element.

```css
.modal {
  background: rgba(255, 255, 255, 0.5);
  backdrop-filter: blur(10px);
}
```
Creates modern UI effects like Apple-style glass morphism.

## Logical Properties for Better Internationalization
Instead of `left` and `right`, use logical properties for better support in **right-to-left (RTL) languages**.

```css
div {
  margin-inline-start: 20px; /* Works for both LTR & RTL layouts */
}
```
Improves accessibility and flexibility in global projects.

##  `:is()` and `:where()` for Simplified Selectors
Reduces redundancy in CSS selectors.

### **Example**
```css
:is(h1, h2, h3) {
  color: blue;
}
```
Makes styling multiple elements more efficient.

