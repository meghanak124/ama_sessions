# AMA Session 

## 1. Closures

A closure is when a function remembers variables from its outer scope
even after the outer function is finished.

``` js
function outer() {
  let count = 0;
  return function inner() {
    count++;
    console.log(count);
  };
}
```

------------------------------------------------------------------------

## 2. Immutable Methods

### Arrays:

-   concat()
-   slice()
-   map()
-   filter()
-   reduce()
-   spread operator

### Strings:

-   toUpperCase()
-   toLowerCase()
-   trim()
-   slice()
-   replace()

------------------------------------------------------------------------

## 3. Access HTML Elements

``` js
document.getElementById("id")
document.querySelector(".class")
document.querySelectorAll("div")
```

------------------------------------------------------------------------

## 4. sessionStorage vs localStorage


  | Feature  | localStorage  | sessionStorage|
  |--------- |---------|---------|
  | Lifetime |  Forever/till Manually removed  |      Till tab closes|
  | Scope    |     All tabs  |     Only current tab|

------------------------------------------------------------------------

## 5. HTML Entities
- HTML entities are special codes used to display reserved or special characters in HTML.
- Because some characters are already used by HTML itself.
```html
<p>5 < 10</p>
<p>5 &lt; 10</p>

<p>This is &lt;b&gt;bold&lt;/b&gt; text</p>
This is <b>bold</b> text
```

Entity	|Symbol|	Meaning|
 |--------- |---------|---------|
`&lt;`|	<	|less than
`&gt;`|	>	|greater than
`&amp;`	|&|	ampersand
`&quot;`|	"	|double quote
`&apos;`|	'	|single quote|
`&nbsp;`|` `&nbsp;&nbsp;(space)	|non-breaking space

------------------------------------------------------------------------

## 6. Promise.race()

- Promise.race() runs multiple promises at the same time
- It returns the result of the FIRST promise that settles
```js
const p1 = new Promise(resolve => {
  setTimeout(() => resolve("P1 done"), 2000);
});

const p2 = new Promise(resolve => {
  setTimeout(() => resolve("P2 done"), 1000);
});

const p3 = new Promise((resolve, reject) => {
  setTimeout(() => reject("Error in P3"), 500);
});

Promise.race([p1, p2])
  .then(result => console.log(result));
// output : P2 done

Promise.race([p1, p2, p3])
  .then(result => console.log(result));
// output : Error in P3
  ```

------------------------------------------------------------------------

## 7. throw

- a keyword to handle errors
- use whenever there is a chance of an error
- we may return a string or an error class object using throw
- error object allows us to use error class properties like err.message, err.stack etc.

``` js
if (age < 18) {
  throw new Error("Not allowed");
}

if (age < 18) {
  throw "Not allowed";
}
```

------------------------------------------------------------------------

## 8. explain fetch and what it returns

- fetch is used to make API calls (get data from server)
- It returns a promise
- When the promise resolves, We get a Response object
- It is in raw stream format (not usable directly)
- The data coming from server is in JSON format (string)

``` js
fetch("https://api.com/data")
  .then(res => res.json())
  .then(data => console.log(data));
```

```js
// raw stream format
response.body → " { name: 'Meghana' } "
// converted to JSON
data → { name: "Meghana" }
```
------------------------------------------------------------------------

## 9. Runtime vs Compile-time Error

-   Compile-time: Syntax error
-   Runtime: Logical errors

```js
// Compile error
console.log("hello"

// Runtime error
console.log(x);
```

------------------------------------------------------------------------

## 10. Microtasks vs Macrotasks

**Order:** Call stack → Microtasks → Macrotasks

**Microtasks (high priority)**
- Promise.then
- queueMicrotask

**Macrotasks**
- setTimeout
- setInterval
- setImmediate



------------------------------------------------------------------------

## 11. Promisification

Convert callback → Promise

```js
// Callback
fs.readFile("file", (err, data) => {})

// Promisified
const fs = require("fs").promises;
fs.readFile("file").then(...)
```

------------------------------------------------------------------------

## 12. Lexical Scoping

- Scope depends on where function is written
```js
function outer() {
  let x = 10;

  function inner() {
    console.log(x);
  }

  inner();
}
```
- inner can access x , because of lexical scope

------------------------------------------------------------------------

## 13. Function vs Method

-   Function: Independent
-   Method: Inside object
```js
function greet() {} // function

const obj = {
  sayHi() {} // method
};
```
------------------------------------------------------------------------

## 14. Higher Order Functions

Functions that take/return functions.
```js
function greet(fn) {
  fn();
}

greet(() => console.log("Hello"));
```

------------------------------------------------------------------------

## 15. DOM

- DOM is a tree representation of HTML.
```html
<body>
  <h1>Hello</h1>
</body>
```
JS can:
- read
- update
- delete elements
 
```js
document.querySelector("h1").textContent = "Hi";
```