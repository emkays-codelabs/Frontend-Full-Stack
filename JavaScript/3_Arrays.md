

---

# 📦 JavaScript Arrays — Complete Master Guide

---

# 🔹 1. What is an Array?

An **array** is a collection of values stored in a single variable.

```js
let arr = [10, 20, 30];
```

✔ Stores multiple values
✔ Index-based (starts from 0)

---

# 🔹 2. Access & Modify

```js
let arr = ["a", "b", "c"];

console.log(arr[0]); // "a"

arr[1] = "x";
console.log(arr); // ["a", "x", "c"]
```

---

# 🔹 3. Array Length

```js
console.log(arr.length);
```

---

# 🔹 4. Add & Remove Elements

## ➤ Add to End → `push()`

```js
arr.push(40);
```

## ➤ Remove from End → `pop()`

```js
arr.pop();
```

---

## ➤ Add to Start → `unshift()`

```js
arr.unshift(5);
```

## ➤ Remove from Start → `shift()`

```js
arr.shift();
```

---

# 🔹 5. Convert & Merge

## ➤ `toString()`

```js
let arr = [1, 2, 3];

console.log(arr.toString()); // "1,2,3"
```

---

## ➤ `concat()` → Merge arrays

```js
let a = [1, 2];
let b = [3, 4];

let result = a.concat(b);

console.log(result); // [1,2,3,4]
```

---

# 🔹 6. Slice vs Splice (🔥 VERY IMPORTANT)

---

## ➤ `slice()` → Copy (Non-destructive)

### Syntax

```js
slice(startIdx, endIdx)
```

```js
let arr = [1, 2, 3, 4];

let result = arr.slice(1, 3);

console.log(result); // [2, 3]
console.log(arr);    // unchanged
```

---

## ➤ `splice()` → Modify Original

### Syntax

```js
splice(startIdx, delCount, newEl1...)
```

---

### Remove

```js
let arr = [1, 2, 3, 4];

arr.splice(1, 2);

console.log(arr); // [1, 4]
```

---

### Add

```js
let arr = [1, 4];

arr.splice(1, 0, 2, 3);

console.log(arr); // [1,2,3,4]
```

---

### Replace

```js
let arr = [1, 2, 3];

arr.splice(1, 1, 99);

console.log(arr); // [1,99,3]
```

---

# 🔹 7. Looping Through Arrays

## ➤ for loop

```js
for (let i = 0; i < arr.length; i++) {
  console.log(arr[i]);
}
```

---

## ➤ for...of

```js
for (let val of arr) {
  console.log(val);
}
```

---

# 🔹 8. Important Functional Methods

---

## ➤ `map()` → Transform

```js
let arr = [1, 2, 3];

let result = arr.map(x => x * 2);
```

---

## ➤ `filter()` → Select

```js
let result = arr.filter(x => x > 1);
```

---

## ➤ `reduce()` → Single value

```js
let sum = arr.reduce((acc, val) => acc + val, 0);
```

---

## ➤ `find()` → First match

```js
arr.find(x => x > 2);
```

---

## ➤ `some()` → Any match

```js
arr.some(x => x > 2);
```

---

## ➤ `every()` → All match

```js
arr.every(x => x > 0);
```

---

# 🔹 9. Search & Utility

## ➤ `includes()`

```js
arr.includes(2);
```

## ➤ `indexOf()`

```js
arr.indexOf(2);
```

---

# 🔹 10. Sorting & Reversing

## ➤ `sort()`

```js
arr.sort((a, b) => a - b);
```

## ➤ `reverse()`

```js
arr.reverse();
```

---

# 🔹 11. Chaining (🔥 Advanced)

```js
let result = [1, 2, 3, 4]
  .filter(x => x % 2 === 0)
  .map(x => x * 10);

console.log(result); // [20, 40]
```

---

# 🔹 12. Real-World Example

```js
let users = [
  { name: "A", age: 20 },
  { name: "B", age: 30 }
];

let result = users
  .filter(user => user.age > 20)
  .map(user => user.name);

console.log(result); // ["B"]
```

---

# 🧠 Final Cheat Sheet

| Action       | Method    |
| ------------ | --------- |
| Add end      | push()    |
| Remove end   | pop()     |
| Add start    | unshift() |
| Remove start | shift()   |
| Copy         | slice()   |
| Modify       | splice()  |
| Transform    | map()     |
| Filter       | filter()  |
| Aggregate    | reduce()  |

---

# 🚀 Interview-Level Insight

👉 Arrays are **objects with index keys**

```js
typeof []; // "object"
```

👉 Memory is contiguous (conceptually)

👉 Methods like `map/filter` return new arrays → **immutability (important in React)**

---

# ⚡ Final Practice Challenge

```js
// Input
let arr = [5, 10, 15, 20];

// Output: [100, 200]  (even numbers × 10)
```

✔ Try using chaining

---


