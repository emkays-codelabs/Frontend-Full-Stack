
---

# 📘 1️⃣ Introduction to JavaScript

## 1.1 What is JavaScript?

JavaScript (JS) is a **high-level, interpreted programming language** mainly used to make websites interactive.

If:

* HTML = Structure 🏗
* CSS = Styling 🎨
* JavaScript = Brain 🧠 (Logic + Interactivity)

---

## 1.2 Where Does JavaScript Run?

1. Inside Browser (Chrome, Firefox)
2. Inside Server (Node.js)

When you use:

* `console.log()` → It prints inside browser console.

Open:

```
Right click → Inspect → Console
```

---

## 1.3 Why JavaScript is Important?

Because it allows:

* Button clicks
* Form validation
* API calls
* Dynamic content
* Real-time updates
* Full-stack development (Node.js)

---

# 📘 2️⃣ How JavaScript Executes Code

JavaScript runs **line by line** (single-threaded).

Example:

```js
console.log("A");
console.log("B");
```

Output:

```
A
B
```

It executes from top → bottom.

---

# 📘 3️⃣ Console Methods

Console is used for debugging.

---

## 3.1 `console.log()`

```js
console.log("Hello World!");
```

👉 Prints normal message.

---

## 3.2 `console.info()`

Used for informational messages.

---

## 3.3 `console.warn()`

Shows warning (yellow in browser).

---

## 3.4 `console.error()`

Shows error (red in browser).

---

# 📘 4️⃣ Variables

## 4.1 What is a Variable?

A variable is a **container that stores value**.

Think like:

```
Box → label (name) → inside value
```

---

## 4.2 Syntax

```
LHS = RHS
```

Example:

```js
let age = 25;
```

* LHS → age
* RHS → 25

---

# 📘 5️⃣ Types of Variable Declarations

There are 3:

1. var
2. let
3. const

---

# 📘 6️⃣ var (Old Way)

```js
var age = 29;
var age = "Ajay Sharma"; // allowed
```

### Characteristics:

1. Function Scoped
2. Can redeclare
3. Hoisted
4. Causes bugs

Example:

```js
{
  var x = 10;
}
console.log(x); // works
```

Because var ignores block scope.

---

# 📘 7️⃣ let (Modern Way)

```js
let name = "Ujjawal";
name = "Ajay";
```

### Characteristics:

1. Block scoped
2. Cannot redeclare
3. Can update

Example:

```js
{
  let x = 10;
}
console.log(x); // ❌ error
```

---

# 📘 8️⃣ const

```js
const PI = 3.14;
```

### Characteristics:

1. Block scoped
2. Cannot redeclare
3. Cannot update

Must assign immediately.

---

# 📘 9️⃣ Scope

Scope = Area where variable is accessible.

---

## 9.1 Global Scope

```js
let a = 10;
```

Accessible everywhere.

---

## 9.2 Block Scope

```js
{
  let x = 5;
}
```

Only inside `{}`.

---

## 9.3 Function Scope

```js
function test() {
  var x = 5;
}
```

Accessible only inside function.

---

# 📘 🔟 Data Types

Data type = Type of value stored.

---

## 10.1 Two Categories

### A. Primitive (Stores actual value)

* String
* Number
* Boolean
* Null
* Undefined

### B. Non-Primitive (Stores reference)

* Object
* Array

---

# 📘 11️⃣ Primitive Data Types

---

## 11.1 String

```js
let fullname = "Ajay Sharma";
```

Text value.

---

## 11.2 Number

```js
let age = 25;
```

Integer or decimal.

---

## 11.3 Boolean

```js
let isAbove18 = false;
```

True or false.

---

## 11.4 Null

```js
let value = null;
```

Means intentionally empty.

⚠️ `typeof null` → object (JS bug)

---

## 11.5 Undefined

```js
let test;
```

Declared but not assigned.

---

# 📘 12️⃣ Non-Primitive Types

---

## 12.1 Object

```js
let person = {
  username: "ajaysharma12",
  age: 29
};
```

Collection of key-value pairs.

---

## 12.2 Array

```js
let numbers = [1, 2, 3];
```

Stores multiple values.

---

# 📘 13️⃣ typeof Operator

Used to check data type.

```js
console.log(typeof age);
```

Returns:

* "string"
* "number"
* "boolean"
* "object"

---

# 📘 14️⃣ Operators

Operators perform operations.

---

# 14.1 Arithmetic Operators

```js
1 + 1
15 * 6
30 / 5
5 ** 5
```

| Symbol | Meaning     |
| ------ | ----------- |
| +      | Addition    |
| -      | Subtraction |
| *      | Multiply    |
| /      | Divide      |
| **     | Power       |

---

# 14.2 Unary Operators

Works on single value.

Example:

```js
let x = 5;
let result = x++;
```

### Postfix (`x++`)

1. Assign old value to result
2. Then increase x

Output:

```
result = 5
x = 6
```

---

### Prefix (`++x`)

```js
let result = ++x;
```

1. Increase x first
2. Then assign

Output:

```
result = 6
x = 6
```

---

# 14.3 Comparison Operators

```js
5 == "5"  // true
5 === "5" // false
```

| Operator | Meaning         |
| -------- | --------------- |
| ==       | Loose equality  |
| ===      | Strict equality |
| !=       | Not equal       |
| >        | Greater         |
| <        | Less            |

Always use `===`

---

# 14.4 Logical Operators

```js
true && false
true || false
!true
```

| Operator | Meaning |   |    |
| -------- | ------- | - | -- |
| &&       | AND     |   |    |
|          |         |   | OR |
| !        | NOT     |   |    |

---

# 📘 15️⃣ Hoisting

`var` is hoisted.

```js
console.log(a);
var a = 5;
```

Output:

```
undefined
```

JS moves declaration to top internally.

---

# 📘 16️⃣ Case Sensitivity

```js
const PI = 3.14;
console.log(pi); // error
```

JS is case-sensitive.

---

# 📘 17️⃣ Execution Example (Step-by-Step)

```js
let x = 5;
let result = x++;
console.log(result, x);
```

Step 1: x = 5
Step 2: result = 5
Step 3: x becomes 6
Step 4: Print → 5 6

---

# 📘 18️⃣ Final Concepts Covered

1. What is JavaScript
2. Where JS runs
3. How JS executes
4. Console methods
5. Variables
6. var
7. let
8. const
9. Scope
10. Primitive types
11. Non-Primitive types
12. typeof
13. Arithmetic operators
14. Unary operators
15. Comparison operators
16. Logical operators
17. Hoisting
18. Case sensitivity
