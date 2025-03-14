# CSS Animations

CSS **Animations** allow elements to move, fade, grow, or change in a more complex way than transitions. Unlike transitions, animations can have multiple steps and loop indefinitely.

```css
@keyframes animation-name {
  0% { property: value; }
  100% { property: value; }
}

.element {
  animation: animation-name duration timing-function delay iteration-count direction;
}
```

- **`@keyframes`** → Defines animation steps.
- **`animation-name`** → The name of the keyframe.
- **`duration`** → The time the animation runs.
- **`iteration-count`** → How many times it repeats (`infinite` for looping).
- **`direction`** → `normal`, `reverse`, `alternate`, etc.

```css
@keyframes bounce {
  0% { transform: translateY(0); }
  50% { transform: translateY(-20px); }
  100% { transform: translateY(0); }
}

.box {
  width: 100px;
  height: 100px;
  background-color: orange;
  animation: bounce 0.5s ease infinite;
}
```
**Effect**: The box **bounces up and down**.

## Using multiple keyframes
```css
@keyframes colorChange {
  0% { background-color: red; }
  50% { background-color: blue; }
  100% { background-color: green; }
}

.box {
  animation: colorChange 3s ease infinite;
}
```
**Effect**: The box **cycles through red, blue, and green**.

## Controlling animation speed & repeats
| Property                    | Effect                                 |
| --------------------------- | -------------------------------------- |
| `animation-duration`        | Time for one cycle (e.g., `2s`)        |
| `animation-delay`           | Wait before starting (e.g., `1s`)      |
| `animation-iteration-count` | Number of loops (`1`, `3`, `infinite`) |
| `animation-direction`       | `normal`, `reverse`, `alternate`, etc. |

Example:
```css
.element {
  animation: spin 2s linear 1s infinite alternate;
}
```
**Effect**: The element spins endlessly, switching direction each time.

## Hover-Based animations
Animations can be triggered on hover without JavaScript.
```css
@keyframes rotate {
  from { transform: rotate(0deg); }
  to { transform: rotate(360deg); }
}

.circle {
  animation: none;
}

.circle:hover {
  animation: rotate 1s linear;
}
```

**Effect**: The circle **rotates only when hovered**.

## Best Practices for CSS animations

- Use `@keyframes` for **complex movements**.
- Avoid excessive animations for **better performance**.
- Use **GPU-accelerated properties** (`transform` and `opacity`).


