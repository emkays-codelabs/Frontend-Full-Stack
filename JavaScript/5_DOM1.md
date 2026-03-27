
---

# 🌐 JavaScript DOM – Complete Deep Tutorial (Beginner → Advanced)

---

# 🔹 1. What is the DOM?

**DOM = Document Object Model**

👉 Browser converts HTML into a **tree of objects** you can control using JavaScript.

### Example:

```html
<body>
  <div id="container">
    <h1>Hello</h1>
    <p>World</p>
  </div>
</body>
```

### Structure:

```
document
 └── body
      └── div (parent)
           ├── h1 (child)
           └── p (child)
```

👉 Every element = **Node (object)**
👉 You can **select, modify, delete, create**

---

# 🔹 2. Selecting Elements (VERY IMPORTANT)

---

## ✅ getElementById vs #id

### ✔️ HTML

```html
<h1 id="title">Hello</h1>
```

### ✔️ JavaScript (Method 1)

```js
const el = document.getElementById("title");
```

### ✔️ JavaScript (Method 2 - Modern)

```js
const el = document.querySelector("#title");
```

### 🔥 Difference:

| Method         | Syntax   | Returns        |
| -------------- | -------- | -------------- |
| getElementById | "title"  | Single element |
| querySelector  | "#title" | First match    |

👉 `#` is used in **CSS selector style**

---

## ✅ Class Selection

```js
document.getElementsByClassName("item");   // HTMLCollection
document.querySelectorAll(".item");        // NodeList (better)
```

---

## ✅ Tag Selection

```js
document.getElementsByTagName("p");
```

---

## 🔥 Best Practice:

👉 Always prefer:

```js
document.querySelector()
document.querySelectorAll()
```

---

# 🔹 3. Content Manipulation (VERY IMPORTANT)

---

## ✅ innerText

```js
el.innerText = "Hello";
```

👉 Shows **only visible text**
👉 Ignores hidden elements

---

## ✅ textContent

```js
el.textContent = "Hello";
```

👉 Shows **all text (even hidden)**
👉 Faster than innerText

---

## ✅ innerHTML

```js
el.innerHTML = "<b>Hello</b>";
```

👉 Can insert HTML
👉 ⚠️ Security risk (XSS)

---

## 🔥 Difference Table

| Property    | Includes HTML | Includes Hidden | Use Case     |
| ----------- | ------------- | --------------- | ------------ |
| innerText   | ❌             | ❌               | UI text      |
| textContent | ❌             | ✅               | raw text     |
| innerHTML   | ✅             | ✅               | dynamic HTML |

---

# 🔹 4. Parent, Child, Sibling (Core Concept)

---

## Example HTML:

```html
<div id="parent">
  <p id="child1">One</p>
  <p id="child2">Two</p>
</div>
```

---

## ✅ Parent

```js
const child = document.getElementById("child1");
console.log(child.parentElement);
```

👉 Output = `<div id="parent">`

---

## ✅ Children

```js
const parent = document.getElementById("parent");

console.log(parent.children);   // HTMLCollection
console.log(parent.children[0]); // first child
```

---

## ✅ First & Last Child

```js
parent.firstElementChild
parent.lastElementChild
```

---

## ✅ Siblings

```js
const el = document.getElementById("child1");

el.nextElementSibling
el.previousElementSibling
```

---

## 🔥 Summary

| Concept         | Meaning  |
| --------------- | -------- |
| parentElement   | go up    |
| children        | go down  |
| nextSibling     | next     |
| previousSibling | previous |

---

# 🔹 5. Looping Through Elements (IMPORTANT 🔥)

---

## Example:

```html
<div class="box"></div>
<div class="box"></div>
<div class="box"></div>
```

---

## ✅ Using querySelectorAll

```js
const boxes = document.querySelectorAll(".box");

for (let i = 0; i < boxes.length; i++) {
  boxes[i].textContent = "Box " + (i + 1);
}
```

---

## ✅ Using forEach (Modern)

```js
boxes.forEach((box, index) => {
  box.textContent = `Box ${index + 1}`;
});
```

---

## 🎯 Assign Unique Values to Divs

```js
const divs = document.querySelectorAll("div");

divs.forEach((div, i) => {
  div.id = "div-" + i;
});
```

👉 Output:

```
div-0
div-1
div-2
```

---

# 🔹 6. Styling Elements

```js
el.style.color = "red";
el.style.backgroundColor = "black";
```

---

## ✅ Better: classList

```js
el.classList.add("active");
el.classList.remove("active");
el.classList.toggle("active");
```

---

# 🔹 7. Attributes

```js
el.setAttribute("src", "img.png");
el.getAttribute("src");
el.removeAttribute("src");
```

---

# 🔹 8. Creating Elements

```js
const div = document.createElement("div");
div.textContent = "New Div";

document.body.appendChild(div);
```

---

## Insert Positions

```js
parent.appendChild(el);   // end
parent.prepend(el);       // start
```

---

# 🔹 9. Removing Elements

```js
el.remove();
```

---

# 🔹 10. Events

```js
btn.addEventListener("click", () => {
  alert("Clicked");
});
```

---

## Event Object

```js
btn.addEventListener("click", (e) => {
  console.log(e.target);
});
```

---

# 🔹 11. Form Handling

```js
form.addEventListener("submit", (e) => {
  e.preventDefault();
  console.log(input.value);
});
```

---

# 🔹 12. DOM Ready (Important)

```js
document.addEventListener("DOMContentLoaded", () => {
  console.log("DOM loaded");
});
```

---

# 🔹 13. Advanced – Event Delegation

```js
ul.addEventListener("click", (e) => {
  if (e.target.tagName === "LI") {
    console.log("Clicked LI");
  }
});
```

---

# 🔹 14. Real Example (Everything Combined)

```html
<div id="container">
  <button id="btn">Add</button>
</div>
```

```js
const btn = document.getElementById("btn");
const container = document.getElementById("container");

btn.addEventListener("click", () => {
  const div = document.createElement("div");
  div.textContent = "New Item";

  container.appendChild(div);
});
```

---

# 🔥 Final Summary (VERY IMPORTANT)

DOM lets you:

✔ Select elements
✔ Modify content
✔ Traverse (parent/child/sibling)
✔ Handle events
✔ Create dynamic UI

---
