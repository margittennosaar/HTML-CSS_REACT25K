# CSS Units: Absolute and Relative

CSS units define the size of elements, text, and spacing on a webpage. There are two main types of units:

**Absolute units** – Fixed sizes that do not change.  
**Relative units** – Sizes that adapt based on the parent element or viewport.


## Absolute Units
Absolute units have a fixed size and do not scale based on the screen or parent element.

| Unit             | Description                                        |
| ---------------- | -------------------------------------------------- |
| `px` (pixels)    | The most common unit for web design. Fixed size.   |
| `cm`, `mm`, `in` | Centimeters, millimeters, inches – used for print. |
| `pt`, `pc`       | Points and picas – mainly for print design.        |


```css
h1 {
  font-size: 24px; /* Fixed size, does not change */
}
```

Use absolute units when you need precise sizing that won’t change, like borders or print styling.

## Relative Units
Relative units are flexible and adjust based on the screen size or parent element.

| Unit           | Description                                                          |
| -------------- | -------------------------------------------------------------------- |
| `%`            | Percentage of the parent element's size.                             |
| `em`           | Relative to the font size of the parent.                             |
| `rem`          | Relative to the font size of the root (`<html>`).                    |
| `vw`, `vh`     | Viewport width and height (1vw = 1% of screen width).                |
| `vmin`, `vmax` | Based on the smaller (`vmin`) or larger (`vmax`) viewport dimension. |
| `ch`           | Width of the `0` character in the chosen font.                       |
| `ex`           | Height of the lowercase `x` in the font.                             |

```css
.container {
  width: 80%; /* Takes 80% of its parent */
}

h1 {
  font-size: 2rem; /* 2x the root font size */
}

.box {
  height: 50vh; /* 50% of the viewport height */
}
```

Use relative units for scalable and responsive layouts.

---

## Choosing the Right Unit
| Use Case                   | Recommended Units                 |
| -------------------------- | --------------------------------- |
| Font sizes                 | `rem` (scales with user settings) |
| Spacing (padding, margins) | `em`, `rem`, `%`                  |
| Responsive layouts         | `%`, `vw`, `vh`                   |
| Borders                    | `px` (fixed size)                 |

---

## Key differences between `em` and `rem`

| Unit  | Relative To                         |
| ----- | ----------------------------------- |
| `em`  | The **parent** element's font size. |
| `rem` | The **root (`html`)** font size.    |

```css
html {
  font-size: 16px;
}

.parent {
  font-size: 20px;
}

.child {
  font-size: 1.5em; /* 1.5 x 20px = 30px */
}

.another-child {
  font-size: 1.5rem; /* 1.5 x 16px = 24px */
}
```
Use `rem` for consistent scaling across the entire website.


## Viewport Units for Full-Screen Layouts
Viewport-based units (`vw`, `vh`, `vmin`, `vmax`) are useful for making full-screen elements.

```css
.hero {
  width: 100vw; /* Full screen width */
  height: 100vh; /* Full screen height */
}
```
Use viewport units when designing full-screen sections and dynamic layouts.

## Summary
- Absolute units (`px`, `cm`, `pt`) – Best for fixed sizes.  
- Relative units (`%`, `em`, `rem`, `vw`, `vh`) – Best for responsive designs.  
- Use `rem` for font sizes, `%` for fluid layouts, and `vh`/`vw` for fullscreen elements.


