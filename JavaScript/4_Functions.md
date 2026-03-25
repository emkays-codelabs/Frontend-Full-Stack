
---

# Functions — Complete JavaScript Tutorial

---

# 🧠 1. What is a Function?

A **function** is a reusable block of code used to perform a task.

```js
function greet(name) {
    return "Hello " + name;
}

console.log(greet("Mahesh"));
```

👉 Think: **Write once → reuse many times**

---

# 🔁 2. Function Declaration vs Function Expression (VERY IMPORTANT)

---

## ✅ 2.1 Function Declaration

### ✔ Definition

A function defined using `function` keyword with a name.

```js
function greet(name) {
    return "Hello " + name;
}
```

---

### 🔥 Hoisting (Key Concept)

You can call it **before defining**

```js
greet("Mahesh"); // ✅ Works

function greet(name) {
    return "Hello " + name;
}
```

👉 JavaScript moves it to the top internally.

---

## ✅ 2.2 Function Expression

### ✔ Definition

A function stored inside a variable.

```js
const greet = function(name) {
    return "Hello " + name;
};
```

---

### ❌ No Hoisting

```js
greet("Mahesh"); // ❌ Error

const greet = function(name) {
    return "Hello " + name;
};
```

👉 Only variable is hoisted, not the function value.

---

## 🧠 Internal Understanding

---

### Declaration (JS sees this)

```js
function greet() {}
```

👉 Already available everywhere

---

### Expression (JS sees this)

```js
const greet;   // hoisted but undefined
greet();       // ❌ error

greet = function() {};
```

---

## 🔹 Naming Difference

```js
// Declaration → name required
function greet() {}

// Expression → optional
const greet = function() {};         // anonymous
const greet2 = function sayHi() {};  // named
```

---

## 🎯 Final Comparison

| Feature                | Declaration | Expression |
| ---------------------- | ----------- | ---------- |
| Hoisting               | ✅ Yes       | ❌ No       |
| Call before definition | ✅           | ❌          |
| Naming                 | Required    | Optional   |
| Use case               | General     | Callbacks  |

---

# ⚡ 3. Arrow Functions

---

## 🔹 Syntax

```js
const add = (a, b) => a + b;
```

---

## 🔹 Examples

```js
const square = x => x * x;
const greet = () => "Hello";
```

---

## 🔥 Key Differences

| Feature | Regular Function | Arrow Function  |
| ------- | ---------------- | --------------- |
| `this`  | Dynamic          | Fixed (lexical) |
| Syntax  | Long             | Short           |

---

# 🌍 4. Scope (Where variables live)

---

## 🔹 Types

### 1. Global Scope

```js
let a = 10;
```

---

### 2. Function Scope

```js
function test() {
    let b = 20;
}
```

---

### 3. Block Scope

```js
if (true) {
    let x = 5;
}
```

---

## 🔥 Example

```js
let global = "I am global";

function demo() {
    let local = "I am local";
    console.log(global);
}
```

---

# 🔁 5. Callbacks

---

## 🔹 Definition

A function passed into another function.

---

## 🔹 Example

```js
function greet(name, callback) {
    console.log("Hi " + name);
    callback();
}

function sayBye() {
    console.log("Bye!");
}

greet("Mahesh", sayBye);
```

---

# 🚀 6. Higher-Order Functions (CORE CONCEPT)

---

## 🔹 Definition

A function that:

1. Takes another function as argument
2. OR returns a function

---

## 🔹 Example 1 (Function as argument)

```js
function operate(a, b, operation) {
    return operation(a, b);
}

const add = (x, y) => x + y;

console.log(operate(2, 3, add));
```

---

## 🔹 Example 2 (Returning function)

```js
function multiplier(factor) {
    return function(num) {
        return num * factor;
    };
}

const double = multiplier(2);
console.log(double(5));
```

---

# 🔥 7. Array Methods (Built-in Higher-Order Functions)

---

## 🔹 1. map() → Transform

```js
const nums = [1, 2, 3];
const doubled = nums.map(n => n * 2);
```

---

## 🔹 2. filter() → Select

```js
const nums = [1, 2, 3, 4];
const evens = nums.filter(n => n % 2 === 0);
```

---

## 🔹 3. reduce() → Combine

```js
const nums = [1, 2, 3, 4];
const sum = nums.reduce((acc, curr) => acc + curr, 0);
```

---

## 🔹 4. forEach() → Loop

```js
[1,2,3].forEach(n => console.log(n));
```

---

## 🔹 5. find() → First match

```js
const result = [10,20,30].find(n => n > 15);
```

---

## 🔹 6. some() → Any true?

```js
[1,2,3].some(n => n > 2); // true
```

---

## 🔹 7. every() → All true?

```js
[2,4,6].every(n => n % 2 === 0); // true
```

---

# 🔁 8. Callback vs Higher-Order Function

| Concept      | Meaning                 |
| ------------ | ----------------------- |
| Callback     | Function passed         |
| Higher-order | Function using callback |

---

# 🧪 9. Practice Problems

---

## 🔹 1. Square numbers

```js
[1,2,3].map(n => n * n);
```

---

## 🔹 2. Filter odds

```js
[1,2,3,4].filter(n => n % 2 !== 0);
```

---

## 🔹 3. Sum

```js
[1,2,3].reduce((a,b) => a + b, 0);
```

---

## 🔹 4. Custom HOF

```js
function apply(arr, fn) {
    return arr.map(fn);
}

apply([1,2,3], x => x * 10);
```

---

# 🌍 10. Real-World Example (E-commerce)

```js
const prices = [100, 200, 300];

// Add tax
const final = prices.map(p => p * 1.18);

// Filter expensive
const expensive = final.filter(p => p > 200);

// Total
const total = expensive.reduce((sum, p) => sum + p, 0);

console.log(total);
```

---

# 🧠 11. Final Summary (Memory Map)

---

### 🔹 Functions

* Declaration → hoisted
* Expression → not hoisted
* Arrow → short syntax

---

### 🔹 Core Concepts

* Scope → variable visibility
* Callback → function inside function
* Higher-order → function using function

---

### 🔹 Array Methods

* `map` → transform
* `filter` → select
* `reduce` → combine
* `forEach` → loop

---

# 🎯 Final Mental Model

👉 **Functions = Building Blocks**
👉 **Callbacks = Plug-ins**
👉 **Higher-order = Smart Controllers**
👉 **Array methods = Real-world tools**

---

