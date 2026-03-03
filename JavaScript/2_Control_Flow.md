
---

# 📘 02_Control_Flow – JavaScript Tutorial

This module covers:

* Unary Operators
* Comparison Operators
* Logical Operators
* Conditional Statements
* Loops
* Type Conversion
* Type Coercion

---

# 🔹 1️⃣ Unary Operators

Unary operators work on **one operand (one variable/value)**.

There are two main types:

## ➤ Increment (`++`)

## ➤ Decrement (`--`)

They also work in two ways:

### 1. Prefix → `++x`

### 2. Postfix → `x++`

---

## 🔸 Prefix Increment

```js
let x = 5;
let result1 = ++x;

console.log(result1); // 6
console.log(x);       // 6
```

### Why?

* First increase value
* Then assign

Steps:

```
x = 5
++x → x becomes 6
result1 = 6
```

---

## 🔸 Postfix Decrement

```js
let y = 10;
let result2 = y--;

console.log(result2); // 10
console.log(y);       // 9
```

### Why?

* First assign value
* Then decrease

Steps:

```
y = 10
result2 = 10
y becomes 9
```

---

# 🔹 2️⃣ Comparison Operators

Used to compare values.

```js
const num1 = 5;
const num2 = "5";
```

---

## 🔸 Loose Equality (`==`)

```js
console.log(num1 == num2); // true
```

✔ Converts type before comparing.

---

## 🔸 Strict Equality (`===`)

```js
console.log(num1 === num2); // false
```

✔ Checks value AND type.

💡 Always prefer `===`

---

## Other Comparison Operators

```js
console.log(num1 > num2);  // false
console.log(num1 >= num2); // true
console.log(num1 < num2);  // false
console.log(num1 <= num2); // true
console.log(num1 != num2); // false
```

---

# 🔸 Comparing Objects

```js
const person = { name: "Sohan" };
const user = { name: "Sohan" };

console.log(person == user);  // false
console.log(person === user); // false
```

### Why?

Objects are compared by **reference (memory address)**, not value.

Even if data is same → they are different objects.

---

```js
console.log([] == []); // false
```

Same reason → different memory reference.

---

```js
console.log(null == null); // true
```

Because both are same primitive value.

---

# 🔹 3️⃣ Logical Operators

Used to combine conditions.

## ✔ AND (`&&`)

```js
true && false // false
```

Returns true only if BOTH are true.

---

## ✔ OR (`||`)

```js
true || false // true
```

Returns true if at least one is true.

---

## ✔ NOT (`!`)

```js
!true  // false
!false // true
```

Reverses boolean value.

---

# 🔹 4️⃣ Conditional Statements

---

## 1️⃣ if Statement

```js
const age = 20;

if (age >= 18) {
  console.log("Eligible to vote");
}
```

Runs only if condition is true.

---

## 2️⃣ if-else

```js
const marks = 45;

if (marks >= 50) {
  console.log("Pass");
} else {
  console.log("Fail");
}
```

---

## 3️⃣ if-else-if

```js
const score = 68;

if (score >= 85) {
  console.log("Grade A");
} else if (score >= 65) {
  console.log("Grade B");
} else {
  console.log("Fail");
}
```

JS checks from top → stops when condition becomes true.

---

## 4️⃣ switch Statement

Used when comparing one value against multiple cases.

```js
const day = 2;

switch (day) {
  case 1:
    console.log("Monday");
    break;
  case 2:
    console.log("Tuesday");
    break;
  default:
    console.log("Invalid day");
}
```

⚠ `break` is important.
Without break → fall-through happens.

---

# 🔹 5️⃣ Loops

Loops repeat code.

---

## 🔸 for Loop

```js
for (let i = 1; i <= 5; i++) {
  console.log(i);
}
```

Best when number of iterations is known.

---

## 🔸 while Loop

```js
let j = 1;

while (j <= 5) {
  console.log(j);
  j++;
}
```

Runs while condition is true.

---

## 🔸 do-while Loop

```js
let k = 1;

do {
  console.log(k);
  k++;
} while (k <= 5);
```

Runs at least once even if condition is false.

---

# 🔹 6️⃣ Type Conversion (Manual)

Explicit conversion.

---

## Convert Number → String

```js
let numberValue = 123;
let numberString = String(numberValue);

console.log(typeof numberValue);  // number
console.log(typeof numberString); // string
```

---

## Convert String → Number

```js
let numberString = "123";
let numberValue = Number(numberString);

console.log(typeof numberValue); // number
```

---

## Convert String → Boolean

```js
let booleanStringValue = "false";
let booleanValue = Boolean(booleanStringValue);

console.log(booleanValue); // true
```

⚠ Important:

Any non-empty string = true

---

# 🔹 7️⃣ Type Coercion (Automatic Conversion)

JS automatically converts types.

---

```js
let number1 = 5;
let number2 = "10";

console.log(number1 + number2); // "510"
```

`+` with string → converts number to string.

---

```js
console.log(number1 - number2); // -5
console.log(number1 * number2); // 50
console.log(number1 / number2); // 0.5
```

Other operators force numeric conversion.

---

# 🔸 Special Cases

```js
console.log(true + 1);      // 2
console.log(false + 1);     // 1
console.log(null + 1);      // 1
console.log(undefined + 1); // NaN
```

Why?

* true → 1
* false → 0
* null → 0
* undefined → NaN

---

# 🧠 Interview Important Points

✔ Always use `===`
✔ Objects compare by reference
✔ `+` behaves differently with strings
✔ Understand falsy values:

```
false
0
""
null
undefined
NaN
```

---

# 📦 Final Summary

This module taught you:

* Unary operators (prefix vs postfix)
* Comparison operators
* Logical operators
* Conditional statements
* Loops
* Type conversion
* Type coercion

---
Perfect 💪
Now we move from **learning ➜ practicing**.

Below are structured exercises for your:

```
02_Control_Flow/
```

I divided them into:

* 🟢 Beginner
* 🟡 Intermediate
* 🔴 Advanced (Interview Level)
* 🚀 Mini Challenges

---

# 🟢 Level 1 – Beginner Exercises

---

## 1️⃣ Prefix vs Postfix

Predict the output before running:

```js
let a = 3;
let b = a++;
let c = ++a;

console.log(a);
console.log(b);
console.log(c);
```

👉 Explain why each value is what it is.

---

## 2️⃣ Comparison Practice

What will be the output?

```js
console.log(10 == "10");
console.log(10 === "10");
console.log(null == undefined);
console.log(null === undefined);
console.log("5" > 3);
```

👉 Explain each line.

---

## 3️⃣ Logical Operator

What will this print?

```js
console.log(true && false);
console.log(true || false);
console.log(!false);
console.log(5 > 3 && 10 < 5);
```

---

## 4️⃣ Simple if-else

Write a program:

If age is:

* Less than 13 → "Child"
* 13 to 19 → "Teen"
* 20+ → "Adult"

---

## 5️⃣ Even or Odd

Write a program to check if a number is even or odd.

---

# 🟡 Level 2 – Intermediate

---

## 6️⃣ Grade System

Create grading logic:

* 90+ → A
* 75–89 → B
* 60–74 → C
* 40–59 → D
* Below 40 → Fail

Use:

* First with if-else
* Then rewrite using switch (if possible)

---

## 7️⃣ Loop Sum

Find sum of numbers from 1 to 100 using:

* for loop
* while loop

Expected output:

```
5050
```

---

## 8️⃣ Multiplication Table

Print multiplication table of 5:

```
5 x 1 = 5
5 x 2 = 10
...
5 x 10 = 50
```

---

## 9️⃣ Break & Continue

Print numbers from 1 to 20:

* Skip multiples of 3
* Stop when number reaches 17

---

## 🔟 Reverse Counting

Print numbers from 10 to 1 using loop.

---

# 🔴 Level 3 – Advanced (Interview Style)

---

## 1️⃣ Tricky Type Coercion

Predict output:

```js
console.log([] + []);
console.log([] + {});
console.log({} + []);
console.log(true + true);
console.log(false == "0");
console.log(false === "0");
```

Explain WHY.

---

## 2️⃣ Falsy Check

Create a function:

```js
function checkValue(value) {
  // print "Falsy" or "Truthy"
}
```

Test with:

```
0
""
[]
{}
null
undefined
NaN
```

---

## 3️⃣ Nested Loop Pattern

Print:

```
*
**
***
****
*****
```

---

## 4️⃣ Prime Number Check

Write program to check if number is prime.

---

## 5️⃣ Infinite Loop Debug

What is wrong?

```js
let i = 0;
while (i < 5) {
  console.log(i);
}
```

Fix it.

---

# 🚀 Mini Challenges (Real Logic Thinking)

---

## Challenge 1 – ATM System

Create simple ATM logic:

* If balance >= withdrawal → allow
* Else → insufficient balance

---

## Challenge 2 – Login System

```js
const username = "admin";
const password = "1234";
```

Check if input matches both using logical operator.

---

## Challenge 3 – Number Guess Game

Create number guess:

* If guess > secret → "Too High"
* If guess < secret → "Too Low"
* If equal → "Correct!"

---

## Challenge 4 – FizzBuzz (Classic)

From 1 to 50:

* Divisible by 3 → Fizz
* Divisible by 5 → Buzz
* Divisible by both → FizzBuzz
* Else → number

---

# 🎯 Bonus – Real Developer Thinking

Answer without running:

```js
console.log(1 + "2" + 3);
console.log(1 + 2 + "3");
```

Why different outputs?

---

Perfect 🔥
Here is your **Answer Sheet – 02_Control_Flow Practice**

Read slowly. Understand the *why*, not just the output.

---

# 🟢 Level 1 – Beginner Answers

---

## 1️⃣ Prefix vs Postfix

```js
let a = 3;
let b = a++;
let c = ++a;

console.log(a);
console.log(b);
console.log(c);
```

### Step-by-step:

* `a = 3`
* `b = a++` → Postfix → assign first, then increment
  → `b = 3`, `a = 4`
* `c = ++a` → Prefix → increment first, then assign
  → `a = 5`, `c = 5`

### Final Output:

```
a = 5
b = 3
c = 5
```

---

## 2️⃣ Comparison Practice

```js
console.log(10 == "10");      // true
console.log(10 === "10");     // false
console.log(null == undefined); // true
console.log(null === undefined); // false
console.log("5" > 3);         // true
```

### Why?

* `==` converts types
* `===` does not
* `null == undefined` is special case → true
* `"5"` becomes 5 in numeric comparison

---

## 3️⃣ Logical Operators

```js
console.log(true && false); // false
console.log(true || false); // true
console.log(!false);        // true
console.log(5 > 3 && 10 < 5); // false
```

---

## 4️⃣ Age Category

```js
const age = 16;

if (age < 13) {
  console.log("Child");
} else if (age <= 19) {
  console.log("Teen");
} else {
  console.log("Adult");
}
```

---

## 5️⃣ Even or Odd

```js
let num = 7;

if (num % 2 === 0) {
  console.log("Even");
} else {
  console.log("Odd");
}
```

---

# 🟡 Level 2 – Intermediate Answers

---

## 6️⃣ Grade System

### if-else version

```js
let marks = 78;

if (marks >= 90) {
  console.log("A");
} else if (marks >= 75) {
  console.log("B");
} else if (marks >= 60) {
  console.log("C");
} else if (marks >= 40) {
  console.log("D");
} else {
  console.log("Fail");
}
```

Switch is not ideal here because switch checks exact values.

---

## 7️⃣ Sum 1–100

### for loop

```js
let sum = 0;

for (let i = 1; i <= 100; i++) {
  sum += i;
}

console.log(sum); // 5050
```

---

## 8️⃣ Multiplication Table

```js
for (let i = 1; i <= 10; i++) {
  console.log(`5 x ${i} = ${5 * i}`);
}
```

---

## 9️⃣ Break & Continue

```js
for (let i = 1; i <= 20; i++) {

  if (i % 3 === 0) {
    continue; // skip multiples of 3
  }

  if (i === 17) {
    break; // stop loop
  }

  console.log(i);
}
```

---

## 🔟 Reverse Counting

```js
for (let i = 10; i >= 1; i--) {
  console.log(i);
}
```

---

# 🔴 Level 3 – Advanced Answers

---

## 1️⃣ Tricky Type Coercion

```js
console.log([] + []);        // ""
console.log([] + {});        // "[object Object]"
console.log({} + []);        // 0 (depends on environment)
console.log(true + true);    // 2
console.log(false == "0");   // true
console.log(false === "0");  // false
```

### Why?

* `[]` converts to ""
* `{}` converts to "[object Object]"
* true = 1
* false = 0
* `"0"` becomes 0 in loose comparison

---

## 2️⃣ Falsy Check Function

```js
function checkValue(value) {
  if (value) {
    console.log("Truthy");
  } else {
    console.log("Falsy");
  }
}
```

Falsy values:

```
0
""
null
undefined
NaN
false
```

Note:

```
[] → Truthy
{} → Truthy
```

---

## 3️⃣ Pattern

```js
for (let i = 1; i <= 5; i++) {
  console.log("*".repeat(i));
}
```

---

## 4️⃣ Prime Check

```js
let num = 7;
let isPrime = true;

if (num <= 1) {
  isPrime = false;
}

for (let i = 2; i < num; i++) {
  if (num % i === 0) {
    isPrime = false;
    break;
  }
}

console.log(isPrime ? "Prime" : "Not Prime");
```

---

## 5️⃣ Infinite Loop Fix

Wrong code:

```js
let i = 0;
while (i < 5) {
  console.log(i);
}
```

Problem:
`i` never increases → infinite loop

Fix:

```js
let i = 0;
while (i < 5) {
  console.log(i);
  i++;
}
```

---

# 🚀 Mini Challenge Answers

---

## ATM

```js
let balance = 1000;
let withdraw = 700;

if (withdraw <= balance) {
  console.log("Transaction Successful");
} else {
  console.log("Insufficient Balance");
}
```

---

## Login System

```js
const username = "admin";
const password = "1234";

let inputUser = "admin";
let inputPass = "1234";

if (inputUser === username && inputPass === password) {
  console.log("Login Success");
} else {
  console.log("Invalid Credentials");
}
```

---

## Guess Game

```js
let secret = 10;
let guess = 7;

if (guess > secret) {
  console.log("Too High");
} else if (guess < secret) {
  console.log("Too Low");
} else {
  console.log("Correct");
}
```

---

## FizzBuzz

```js
for (let i = 1; i <= 50; i++) {

  if (i % 3 === 0 && i % 5 === 0) {
    console.log("FizzBuzz");
  } else if (i % 3 === 0) {
    console.log("Fizz");
  } else if (i % 5 === 0) {
    console.log("Buzz");
  } else {
    console.log(i);
  }
}
```

---

# 🎯 Final Bonus

```js
console.log(1 + "2" + 3); // "123"
console.log(1 + 2 + "3"); // "33"
```

### Why?

First case:

```
1 + "2" = "12"
"12" + 3 = "123"
```

Second case:

```
1 + 2 = 3
3 + "3" = "33"
```

---

# 🏆 You Have Now Mastered

✔ Operators
✔ Comparison
✔ Logical
✔ Control Flow
✔ Loops
✔ Type Conversion
✔ Type Coercion

---



