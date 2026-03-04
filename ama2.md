# AMA SESSION
## 1. Grid Template Areas 
Grid template areas allow you to visually design layouts.
### Example:
``` css
.container {
  display: grid;
  grid-template-areas:
    "header header"
    "sidebar main"
    "footer footer";
}
```
Assign areas to elements:
``` css
.header { grid-area: header; }
.sidebar { grid-area: sidebar; }
.main { grid-area: main; }
.footer { grid-area: footer; }
```
Each quoted line represents a row. Repeated names mean spanning.

------------------------------------------------------------------------
## 2. Flexbox in CSS
- Flexbox is used for 1-dimensional layouts (row OR column).
- We use properties like :
```css
display: flex / inline-flex
flex-direction
flex-wrap
flex-flow
justify-content
align-items
align-content
gap (row-gap, column-gap)
```
------------------------------------------------------------------------
## 3. Locking Mechanism in SQL
Locks prevent multiple users from modifying data at the same time.

Types: 
- Shared Lock → Read only 
- Exclusive Lock → Write/Update 

Prevents: - Dirty reads - Lost updates - Data inconsistency

------------------------------------------------------------------------
## 4. Flex vs Grid
  Flexbox        |       Grid
  --------------------- | -----------------------
  1D layout     |        2D layout
  Row OR column    |     Rows AND columns

Use Flex for alignment. Use Grid for page structure.

------------------------------------------------------------------------
## 5. Switching Branches in Git

``` bash
git branch
git switch branchName
```
OR
``` bash
git checkout branchName
```
------------------------------------------------------------------------
## 6. Types of Positions in CSS
-   static → default
-   relative → relative to itself
-   absolute → relative to positioned parent
-   fixed → fixed to viewport
-   sticky → sticks while scrolling
------------------------------------------------------------------------
## 7. Changing Height & Width of Inner Elements
- Either we can use inline styling or follow specificity score accordingly.
``` html
<div style="width: 300px; height: 200px; background-color: lightblue;">
  Inner Content
</div>
```
------------------------------------------------------------------------
## 8. Normalization in SQL
- Organizing database tables to reduce redundancy.
- Normal Forms: 
- 1NF → No repeating groups 
- 2NF → No partial dependency 
- 3NF → No transitive dependency 
- BCNF → Stronger 3NF
- Removes duplication - Maintain data integrity
------------------------------------------------------------------------
## 9. Flex Attributes in CSS
Container properties: 
- flex-direction 
- justify-content 
- align-items 
- flex-wrap 
- align-content

Item properties: 
- flex 
- flex-grow 
- flex-shrink 
- flex-basis 
- align-self
------------------------------------------------------------------------
## 10. Components of Box Model

1.  Content
2.  Padding
3.  Border
4.  Margin

`box-sizing: border-box;` includes padding and border in width.

------------------------------------------------------------------------
## 11. Comments in CSS
``` css
/* This is a comment */
```
------------------------------------------------------------------------
## 12. Table Tag in HTML
``` html
<table>
  <tr>
    <th>Name</th>
    <th>Age</th>
  </tr>
  <tr>
    <td>Meghana</td>
    <td>21</td>
  </tr>
</table>
```
Tags: 
- table → table container 
- tr → row 
- th → header cell 
- td → data cell
-----------------------------------------------------------------------
## 13. What is `<title>` in HTML?
Appears in: - Browser tab - Search engine results
Defined inside `<head>`:
``` html
<title>My Website</title>
```
------------------------------------------------------------------------
## 14. Tags Inside `<head>`
Common tags: - title - meta - link - style - script - base
```html
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="Website description">
  <title>My Website</title>
  <link rel="icon" href="favicon.ico">
</head>
```
------------------------------------------------------------------------
## 15. Padding vs Margin
  Padding           |         Margin
  -------------------------- | -----------------------
  Space inside element    |   Space outside element
  Affects background       |  Transparent
  Between content & border  | Between elements
------------------------------------------------------------------------
## 16. What is `<br>` Tag?
- Line break tag.
- It is a Self-closing tag.
``` html
Hello<br>World
```
Output: Hello\
World
