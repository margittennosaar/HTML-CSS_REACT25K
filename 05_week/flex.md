# CSS Flexbox: The Basics

Flexbox (Flexible Box Layout) is a powerful CSS layout system that makes it easier to design **responsive**, **dynamic**, and **aligned** layouts. It helps distribute space efficiently across elements, even when their sizes are unknown.

## What is Flexbox?
Flexbox allows you to align items horizontally and vertically with minimal CSS. It is particularly useful for:
- Centering elements
- Creating dynamic layouts
- Building responsive navigation bars
- Handling equal-height columns

To use Flexbox, apply `display: flex;` to a parent container.

```css
.container {
  display: flex;
}
```

## Flex Container & Flex Items

Flexbox consists of **two main parts**:
- **Flex container** → The parent element that holds flex items (`display: flex;`).
- **Flex items** → The direct children inside a flex container.

```html
<div class="container">
  <div class="item">1</div>
  <div class="item">2</div>
  <div class="item">3</div>
</div>
```
```css
.container {
  display: flex;
  background-color: lightgray;
}

.item {
  padding: 20px;
  background-color: steelblue;
  color: white;
  margin: 5px;
}
```

## Main Axis & Cross Axis

Understanding the two axes in Flexbox is key:
- **Main Axis** → Defined by `flex-direction` (`row` or `column`).
- **Cross Axis** → Perpendicular to the main axis.

### **Example:**
```css
.container {
  display: flex;
  flex-direction: row; /* Main axis: left to right */
}
```

## Flex Direction

Defines how flex items are arranged.

| Value            | Description                              |
| ---------------- | ---------------------------------------- |
| `row`            | Default. Items are placed left to right. |
| `row-reverse`    | Items are placed right to left.          |
| `column`         | Items are placed top to bottom.          |
| `column-reverse` | Items are placed bottom to top.          |

```css
.container {
  display: flex;
  flex-direction: column;
}
```

## Justify Content (Align on Main Axis)
Controls the alignment of items along the **main axis**.

| Value           | Description                         |
| --------------- | ----------------------------------- |
| `flex-start`    | Items align to the start (default). |
| `flex-end`      | Items align to the end.             |
| `center`        | Items are centered.                 |
| `space-between` | Space between items.                |
| `space-around`  | Space around items.                 |
| `space-evenly`  | Equal spacing around all items.     |


```css
.container {
  display: flex;
  justify-content: center; /* Centers items */
}
```

## Align Items (Align on Cross Axis)
Controls how items align on the **cross axis**.

| Value        | Description                               |
| ------------ | ----------------------------------------- |
| `stretch`    | Default. Items stretch to fill container. |
| `flex-start` | Items align at the top.                   |
| `flex-end`   | Items align at the bottom.                |
| `center`     | Items align at the middle.                |
| `baseline`   | Items align by their text baselines.      |

```css
.container {
  display: flex;
  align-items: center; /* Aligns items in the center */
}
```

## Flex Wrap

By default, items try to fit in one row. Use `flex-wrap` to allow wrapping.

| Value          | Description                            |
| -------------- | -------------------------------------- |
| `nowrap`       | Default. Items stay in a single line.  |
| `wrap`         | Items wrap to the next line if needed. |
| `wrap-reverse` | Items wrap in reverse order.           |

```css
.container {
  display: flex;
  flex-wrap: wrap;
}
```

## Flex Grow, Shrink, and Basis

These properties control how flex items behave inside a flex container.

### Flex Grow (Expands items to fill space)

```css
.item {
  flex-grow: 1; /* Each item takes equal space */
}
```

### Flex Shrink (Controls shrinking)
```css
.item {
  flex-shrink: 0; /* Prevents shrinking */
}
```

### Flex Basis (Sets initial size)
```css
.item {
  flex-basis: 200px; /* Items start at 200px width */
}
```

**Shorthand**
```css
.item {
  flex: 1 1 200px; /* Grow, shrink, and basis in one line */
}
```

## Align Content (Multiple Rows)
Controls spacing of **wrapped rows**.

| Value           | Description                     |
| --------------- | ------------------------------- |
| `flex-start`    | Rows align at the top.          |
| `flex-end`      | Rows align at the bottom.       |
| `center`        | Rows align in the middle.       |
| `space-between` | Space between rows.             |
| `space-around`  | Space around rows.              |
| `stretch`       | Rows stretch to fill container. |

```css
.container {
  display: flex;
  flex-wrap: wrap;
  align-content: center; 
}
```

## Summary
`display: flex;` enables flexbox.  
`flex-direction` controls row/column layout.  
`justify-content` aligns on the main axis.  
`align-items` aligns on the cross axis.  
`flex-wrap` controls item wrapping.  
`flex-grow`, `flex-shrink`, and `flex-basis` control item sizing.

