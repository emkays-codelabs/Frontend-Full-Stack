

---

# 1️⃣ Attribute Selectors

Attribute selectors target elements based on **HTML attributes** and their values.

## ✅ Basic Syntax

```css
element[attribute] { }
element[attribute="value"] { }
```

## 🔹 Types of Attribute Selectors

| Selector          | Meaning       | Example                 |
| ----------------- | ------------- | ----------------------- |
| `[attr]`          | Has attribute | `input[required]`       |
| `[attr="value"]`  | Exact match   | `input[type="text"]`    |
| `[attr^="value"]` | Starts with   | `a[href^="https"]`      |
| `[attr$="value"]` | Ends with     | `img[src$=".png"]`      |
| `[attr*="value"]` | Contains      | `div[class*="card"]`    |
| `[attr~="value"]` | Contains word | `p[class~="highlight"]` |

## 🔹 Example

```html
<input type="text">
<input type="password">
```

```css
input[type="text"] {
  border: 2px solid blue;
}
```

✔ Only the text input gets styled.

---

# 2️⃣ Pseudo-class Selectors

Pseudo-classes target elements based on **state, position, or interaction**.

## ✅ Syntax

```css
selector:pseudo-class { }
```

## 🔹 Common Pseudo-classes

| Pseudo-class    | Meaning                 |
| --------------- | ----------------------- |
| `:hover`        | When mouse is over      |
| `:focus`        | When element is focused |
| `:active`       | When clicked            |
| `:first-child`  | First child of parent   |
| `:last-child`   | Last child of parent    |
| `:nth-child(n)` | Specific child          |
| `:checked`      | Checked input           |
| `:disabled`     | Disabled input          |

## 🔹 Example

```css
button:hover {
  background-color: green;
}

li:first-child {
  color: red;
}
```

✔ Changes style based on interaction or position.

---

# 3️⃣ Pseudo-element Selectors

Pseudo-elements target **specific parts of an element**, not the whole element.

## ✅ Syntax

```css
selector::pseudo-element { }
```

> Modern CSS uses **double colon (::)**

## 🔹 Common Pseudo-elements

| Pseudo-element   | Purpose                       |
| ---------------- | ----------------------------- |
| `::before`       | Insert content before element |
| `::after`        | Insert content after element  |
| `::first-letter` | First letter                  |
| `::first-line`   | First line                    |
| `::selection`    | Selected text                 |

## 🔹 Example

```css
p::first-letter {
  font-size: 30px;
  color: red;
}

div::before {
  content: "🔥 ";
}
```

✔ Styles part of the element or inserts decorative content.

---

# 🔥 Quick Comparison

| Feature  | Attribute Selector   | Pseudo-class             | Pseudo-element      |
| -------- | -------------------- | ------------------------ | ------------------- |
| Targets  | Attribute values     | State/Position           | Part of element     |
| Uses     | `[]`                 | `:`                      | `::`                |
| Example  | `input[type="text"]` | `a:hover`                | `p::first-letter`   |
| Works on | HTML attributes      | Interaction/DOM position | Visual part/content |

---
Here are both a **visual diagram** and a **CSS mindmap** for quick understanding and revision.

---

# 📌 VISUAL DIAGRAM

```
CSS SELECTORS
│
├── 1️⃣ Attribute Selectors  [ ]
│     │
│     ├── [attr]
│     │     → input[required]
│     │
│     ├── [attr="value"]
│     │     → input[type="text"]
│     │
│     ├── [attr^="value"]  (starts with)
│     │     → a[href^="https"]
│     │
│     ├── [attr$="value"]  (ends with)
│     │     → img[src$=".png"]
│     │
│     └── [attr*="value"]  (contains)
│           → div[class*="card"]
│
│     🎯 Targets: HTML attributes
│
│
├── 2️⃣ Pseudo-class Selectors  :
│     │
│     ├── :hover
│     ├── :focus
│     ├── :active
│     ├── :first-child
│     ├── :last-child
│     ├── :nth-child(n)
│     ├── :checked
│     └── :disabled
│
│     🎯 Targets: State / Position / Interaction
│
│
└── 3️⃣ Pseudo-element Selectors  ::
      │
      ├── ::before
      ├── ::after
      ├── ::first-letter
      ├── ::first-line
      └── ::selection
       
      🎯 Targets: Part of an element
```

---

# 🧠 CSS MINDMAP (Concept Map)

```
                           CSS SELECTORS
                                  │
        ┌─────────────────────────┼─────────────────────────┐
        │                         │                         │
 Attribute Selectors        Pseudo-classes           Pseudo-elements
        │                         │                         │
  Target attributes          Target state             Target part
        │                         │                         │
  [type="text"]              :hover                   ::before
  [required]                 :focus                   ::after
  [href^="https"]            :first-child             ::first-letter
  [src$=".png"]              :nth-child()             ::first-line
  [class*="card"]            :checked                 ::selection
        │                         │                         │
  Works on HTML              Works on behavior        Works on visual
  properties                 & DOM position           portions
```

---

# 🔥 Ultra-Quick Summary

| Selector Type  | Symbol | Targets          | Example              |
| -------------- | ------ | ---------------- | -------------------- |
| Attribute      | `[ ]`  | HTML attributes  | `input[type="text"]` |
| Pseudo-class   | `:`    | State / position | `button:hover`       |
| Pseudo-element | `::`   | Part of element  | `p::first-letter`    |

---




