# CSS Transitions

CSS **Transitions** allow properties to change smoothly over a period of time, instead of instantly. They are ideal for **hover effects, color changes, and simple UI animations**.

```css
.element {
  transition: property duration timing-function delay;
}
```
- **Property** → The CSS property to animate (e.g., `opacity`, `transform`).
- **Duration** → The time (e.g., `0.5s` or `300ms`).
- **Timing-function** → Defines speed changes (`ease`, `linear`, `ease-in-out`).
- **Delay** *(optional)* → Delay before the transition starts.


```css
.button {
  background-color: blue;
  transition: background-color 0.3s ease;
}

.button:hover {
  background-color: red;
}
```

**Effect**: The button smoothly changes from **blue to red** when hovered.

## Transitioning multiple properties

You can transition **multiple properties** at once:

```css
.box {
  width: 100px;
  height: 100px;
  background-color: green;
  transition: width 0.5s ease, height 0.5s ease;
}

.box:hover {
  width: 200px;
  height: 200px;
}
```

**Effect**: The box **grows** when hovered.

## Using `all` for multiple transitions

Instead of listing individual properties, you can use `all` to transition **all** properties.

```css
.card {
  transition: all 0.5s ease;
}

.card:hover {
  transform: scale(1.1);
  background-color: lightblue;
}
```
**Effect**: The card **scales up and changes color** on hover.

## Modern transitions examples

### Smooth dropdown menu

```css
.menu {
  max-height: 0;
  overflow: hidden;
  transition: max-height 0.5s ease-in-out;
}

.menu.open {
  max-height: 300px;
}
```

**Effect**: The dropdown menu smoothly opens and closes.


### Smooth button press effect

```css
.button {
  transition: transform 0.2s ease;
}

.button:active {
  transform: scale(0.95);
}
```
**Effect**: The button appears to press down slightly when clicked.


### Image hover zoom effect

```css
.image-container img {
  transition: transform 0.3s ease-in-out;
}

.image-container:hover img {
  transform: scale(1.1);
}
```
**Effect**: The image zooms in slightly when hovered.

### Text hover underline animation

```css
.link {
  display: inline-block;
  position: relative;
  text-decoration: none;
  color: #333;
}

.link::after {
  content: "";
  position: absolute;
  width: 100%;
  height: 2px;
  bottom: 0;
  left: 0;
  background-color: #007bff;
  transform: scaleX(0);
  transition: transform 0.3s ease-in-out;
}

.link:hover::after {
  transform: scaleX(1);
}
```
**Effect**: The underline smoothly expands when hovering over the text.

### Fade-In effect on scroll

```css
.fade-in {
  opacity: 0;
  transform: translateY(20px);
  transition: opacity 0.6s ease-out, transform 0.6s ease-out;
}

.fade-in.visible {
  opacity: 1;
  transform: translateY(0);
}
```
**Effect**: Elements smoothly appear when scrolled into view (requires JavaScript to add `.visible`).

## Transition delays & custom timing functions

You can add a delay and use different speed curves:

```css
.element {
  transition: opacity 0.5s ease-in-out 0.2s;
}
```

**Effect**: The transition starts after **0.2s** and has a smooth **ease-in-out** effect.

| Timing Function | Effect                                  |
| --------------- | --------------------------------------- |
| `linear`        | Same speed throughout                   |
| `ease`          | Slow start & end, fast middle (default) |
| `ease-in`       | Slow start, then fast                   |
| `ease-out`      | Fast start, then slow                   |
| `ease-in-out`   | Slow start & end                        |

## Transitioning transforms

You can animate **position, rotation, and scaling**.

```css
.image {
  transform: scale(1);
  transition: transform 0.3s ease;
}

.image:hover {
  transform: scale(1.2);
}
```
**Effect**: The image **zooms in** smoothly.

## Best Practices for CSS transitions
- Use **shorter durations** for fast interactions.
- Use **ease-in-out** for a more natural feel.
- **Test on different devices** to ensure smooth performance.

