# CSS Grid: The Basics

CSS Grid is a **powerful** layout system that makes it easy to create **responsive**, **two-dimensional** layouts. Unlike Flexbox (which works in one direction at a time), Grid allows you to design layouts that align elements both **horizontally** and **vertically**.

## What is CSS Grid?
CSS Grid is a layout method that divides a container into **rows** and **columns**, allowing elements to be placed within this structure.

To enable Grid, apply `display: grid;` to a container.

```css
.container {
  display: grid;
}
```

## Grid Container & Grid Items

CSS Grid consists of **two main parts**:
- **Grid container** → The parent element that holds grid items (`display: grid;`).
- **Grid items** → The direct children inside a grid container.

```html
<div class="container">
  <div class="item">1</div>
  <div class="item">2</div>
  <div class="item">3</div>
</div>
```
```css
.container {
  display: grid;
  background-color: lightgray;
}

.item {
  padding: 20px;
  background-color: steelblue;
  color: white;
  margin: 5px;
}
```

## Defining Rows & Columns

Use `grid-template-columns` and `grid-template-rows` to define the **structure** of the grid.

### **Example:**
```css
.container {
  display: grid;
  grid-template-columns: 100px 200px auto;
  grid-template-rows: 100px 150px;
}
```
- **Columns**: First is 100px, second is 200px, third adjusts automatically.
- **Rows**: First is 100px, second is 150px.

## Repeat & Fractional Units
Instead of hardcoding values, you can use:
- `repeat()` → Creates repeating columns/rows.
- `fr` (fractional unit) → Shares space proportionally.

```css
.container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
}
```
This creates **three equal columns**.

## Grid Gap (Spacing)
Use `gap` to add space **between** grid items.

```css
.container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 10px;
}
```
- `gap: 10px;` → Adds **10px** space between all grid items.

## Placing Items in the Grid
You can position items using `grid-column` and `grid-row`.

```css
.item {
  grid-column: 1 / 3; /* Spans from column 1 to 3 */
  grid-row: 1 / 2;    /* Spans row 1 */
}
```

## Justify & Align Items

| Property        | Description                |
| --------------- | -------------------------- |
| `justify-items` | Aligns items horizontally. |
| `align-items`   | Aligns items vertically.   |

```css
.container {
  display: grid;
  justify-items: center; /* Centers items horizontally */
  align-items: center;   /* Centers items vertically */
}
```

## Justify & Align Content
These properties align **the whole grid** inside its container.

| Property          | Description                  |
| ----------------- | ---------------------------- |
| `justify-content` | Moves the grid horizontally. |
| `align-content`   | Moves the grid vertically.   |

```css
.container {
  display: grid;
  justify-content: center;
  align-content: center;
}
```

## Grid Auto-Placement
By default, CSS Grid **automatically** places items in available spaces. Use `grid-auto-flow` to control placement.

| Value    | Description                       |
| -------- | --------------------------------- |
| `row`    | Default. Places items row-by-row. |
| `column` | Places items column-by-column.    |
| `dense`  | Fills gaps when possible.         |

```css
.container {
  display: grid;
  grid-auto-flow: column;
}
```

## Grid Areas (Named Layouts)
You can **name areas** and position items using `grid-area`.

```css
.container {
  display: grid;
  grid-template-areas:
    "header header"
    "sidebar main"
    "footer footer";
}

.header { grid-area: header; }
.sidebar { grid-area: sidebar; }
.main { grid-area: main; }
.footer { grid-area: footer; }
```

## Summary
`display: grid;` enables CSS Grid.  
`grid-template-columns` & `grid-template-rows` define the layout.  
`gap` controls spacing between items.  
`justify-items` & `align-items` align items inside the grid.  
`grid-area` allows named layouts.  

