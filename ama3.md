# AMA Session 3

## 1) Explain `z-index`

`z-index` decides **which element appears on top** when elements overlap.

`z-index` works on elements that are positioned, such as:
- `position: relative`
- `position: absolute`
- `position: fixed`
- `position: sticky`

### Example
```css
.box1 {
  position: relative;
  z-index: 1;
}

.box2 {
  position: relative;
  z-index: 5;
}
```

Here, `box2` will appear above `box1` because `5` is greater than `1`.

- Bigger `z-index` = appears above smaller one.
- If `z-index` is not working, often the element is not positioned.
- `z-index` also depends on stacking context.

---

## 2) Create branch and switch in Git

```bash
git checkout -b branch_name
```
---

## 3) How to initialize Git

To start Git in a project folder:

```bash
git init
```

It creates a hidden `.git` folder which allows Git to track changes.

```bash
mkdir my_project
cd my_project
git init
```

After that, Git starts tracking the repository.


---

## 4) Explain `&nbsp;`

`&nbsp;` means **non-breaking space** in HTML.

Normally, HTML collapses multiple spaces into one.  
If you want an extra space that should stay visible, you can use `&nbsp;`.

### Example
```html
Hello&nbsp;&nbsp;World
```

This adds spaces between `Hello` and `World`.

### Why it is called non-breaking
The browser tries not to break the line at that space.

---

## 5) `hr` vs `br`

## `<hr>`
`<hr>` means **horizontal line**.  
It creates a horizontal line.

### Example
```html
<p>Section 1</p>
<hr>
<p>Section 2</p>
```

It visually separates sections.

## `<br>`
`<br>` means **line break**.  
It moves content to the next line.

### Example
```html
Hello<br>World
```

Output:
Hello  
World

---

## 6) How to see previous commit in Git

### Show commit history
```bash
git log
```
---

## 7) Aggregate functions in SQL

Aggregate functions perform calculations on **multiple rows** and return **one result**.

### Common aggregate functions

#### `COUNT()`
Counts rows.

```sql
SELECT COUNT(*) FROM employees;
```

#### `SUM()`
Adds values.

```sql
SELECT SUM(salary) FROM employees;
```

#### `AVG()`
Finds average value.

```sql
SELECT AVG(salary) FROM employees;
```

#### `MIN()`
Finds smallest value.

```sql
SELECT MIN(salary) FROM employees;
```

#### `MAX()`
Finds largest value.

```sql
SELECT MAX(salary) FROM employees;
```
---

## 8) Why we use media queries

Media queries are used to make a website **responsive**.

That means the layout can change depending on:
- screen width
- device type
- orientation

A design that looks good on laptop may look bad on mobile.  
Media queries help adjust styles for different screen sizes.

### Example
```css
body {
  font-size: 18px;
}

@media (max-width: 600px) {
  body {
    font-size: 14px;
  }
}
```

---

## 9) Explain `position: fixed`

`position: fixed` places an element relative to the **browser window (viewport)**.

It stays in the same place even when the page scrolls.

### Example
```css
button {
  position: fixed;
  bottom: 20px;
  right: 20px;
}
```
This keeps the button at the bottom-right corner of the screen.

---

## 10) How to import online CSS

## Using `<link>` in HTML
```html
<link rel="stylesheet" href="https://example.com/style.css">
```
---

## 11) Converting CSV to table in PostgreSQL
Using `\copy` in `psql`:

```sql
\copy table/relation FROM '/path/to/csvfile' DELIMITER ',' CSV HEADER;
```

---

## 12) Which thing is affected by `color` property

The CSS `color` property changes the **text color** of an element.

### Example
```css
p {
  color: red;
}
```

This makes paragraph text red.

### Affects
- normal text
- inline text
- list item text
- text inside elements

---

## 13) What is `gap`

`gap` is used to create space **between items** in:
- flex containers
- grid containers

### Example with flex
```css
.container {
  display: flex;
  gap: 20px;
}
```

This creates `20px` space between flex items.

### Example with grid
```css
.container {
  display: grid;
  gap: 15px;
}
```

### Types
You can also use:
- `row-gap`
- `column-gap`

Example:
```css
.container {
  display: grid;
  row-gap: 10px;
  column-gap: 20px;
}
```

---

## 14) Use of `CSV HEADER` while converting CSV to table

When importing CSV in PostgreSQL, `HEADER` tells PostgreSQL:
**the first row of the CSV file contains column names, not actual data**

### Example CSV
```csv
id,name,age
1,Asha,21
2,Ravi,22
```
- first row = column names
- actual data starts from second row
