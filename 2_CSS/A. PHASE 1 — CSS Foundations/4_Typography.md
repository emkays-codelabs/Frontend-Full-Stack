---
# CSS Typography — Step-by-Step Guide (Beginner Friendly)

Typography in CSS means **styling text** — how it looks, how big it is, how it is spaced, and how it is aligned.

Let’s learn each property one by one with simple examples.

---

# ✅ 1️⃣ `font-family`

### 🔹 What it does:

Specifies which **font** the text should use.

### 🔹 Basic Syntax:

```css
p {
  font-family: Arial, Helvetica, sans-serif;
}
```

### 🔹 Important Rule:

Always provide **fallback fonts**.

Example:

```css
body {
  font-family: "Times New Roman", Times, serif;
}
```

If the first font is not available, the browser tries the next one.

### 🔹 Generic Font Families:

* `serif`
* `sans-serif`
* `monospace`
* `cursive`
* `fantasy`

---

# ✅ 2️⃣ `font-size`

### 🔹 What it does:

Controls the **size of the text**.

### 🔹 Units:

* `px` → pixels (fixed size)
* `em` → relative to parent
* `rem` → relative to root (recommended)
* `%`

### 🔹 Example:

```css
h1 {
  font-size: 32px;
}

p {
  font-size: 1rem;
}
```

### 🔹 Best Practice:

Use `rem` for better responsiveness.

---

# ✅ 3️⃣ `font-weight`

### 🔹 What it does:

Controls how **bold** the text is.

### 🔹 Values:

* `normal`
* `bold`
* `lighter`
* `bolder`
* 100 – 900

### 🔹 Example:

```css
h1 {
  font-weight: bold;
}

p {
  font-weight: 400;
}
```

400 = normal
700 = bold

---

# ✅ 4️⃣ `font-style`

### 🔹 What it does:

Makes text **italic** or normal.

### 🔹 Example:

```css
em {
  font-style: italic;
}
```

Values:

* `normal`
* `italic`
* `oblique`

---

# ✅ 5️⃣ `line-height`

### 🔹 What it does:

Controls the **space between lines**.

### 🔹 Example:

```css
p {
  line-height: 1.6;
}
```

👉 1.5 – 1.8 is good for readability.

---

# ✅ 6️⃣ `letter-spacing`

### 🔹 What it does:

Controls space **between letters**.

### 🔹 Example:

```css
h1 {
  letter-spacing: 2px;
}
```

---

# ✅ 7️⃣ `text-align`

### 🔹 What it does:

Aligns text horizontally.

### 🔹 Values:

* `left`
* `right`
* `center`
* `justify`

### 🔹 Example:

```css
p {
  text-align: center;
}
```

---

# ✅ 8️⃣ `text-decoration`

### 🔹 What it does:

Adds decoration like underline.

### 🔹 Example:

```css
a {
  text-decoration: none;
}
```

Values:

* `underline`
* `overline`
* `line-through`
* `none`

---

# ✅ 9️⃣ `text-transform`

### 🔹 What it does:

Changes text case.

### 🔹 Example:

```css
h2 {
  text-transform: uppercase;
}
```

Values:

* `uppercase`
* `lowercase`
* `capitalize`

---

# 🎯 Complete Beginner Example

### HTML

```html
<h1>Welcome to CSS Typography</h1>
<p>This is a simple paragraph example.</p>
```

### CSS

```css
body {
  font-family: Arial, sans-serif;
}

h1 {
  font-size: 2rem;
  font-weight: 700;
  letter-spacing: 1px;
  text-transform: uppercase;
  text-align: center;
}

p {
  font-size: 1rem;
  line-height: 1.6;
  text-align: justify;
}
```

---

# 🌐 Using Google Fonts (Step-by-Step)
 ### Method 1: Using Google Fonts (Easiest)
Step 1: Go to

👉 https://fonts.google.com

Search a font (Example: Poppins)

Step 2: Copy the <link> Tag

Example:

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
Step 3: Paste in <head>
<head>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;700&display=swap" rel="stylesheet">
</head>
Step 4: Use in CSS
body {
  font-family: 'Poppins', sans-serif;
}

✅ Done! Font is now embedded.

### Method 2: Using @font-face (Local Font File)

If you download a .ttf or .woff file:

### Step 1: Put Font File in Project
fonts/
   MyFont.woff
### Step 2: Add @font-face in CSS
@font-face {
  font-family: 'MyCustomFont';
  src: url('fonts/MyFont.woff') format('woff');
}
### Step 3: Use It
body {
  font-family: 'MyCustomFont', sans-serif;
}

Now it is embedded locally.

---

# 🧠 Quick Typography Cheat Sheet

| Property        | Purpose               |
| --------------- | --------------------- |
| font-family     | Choose font           |
| font-size       | Text size             |
| font-weight     | Boldness              |
| font-style      | Italic                |
| line-height     | Space between lines   |
| letter-spacing  | Space between letters |
| text-align      | Align text            |
| text-decoration | Underline etc         |
| text-transform  | Uppercase/lowercase   |

---

# 🧠 CSS Typography Mindmap

```
                         CSS TYPOGRAPHY
                               │
 ──────────────────────────────┼──────────────────────────────
                               │
        ┌─────────────── Font Properties ────────────────┐
        │                                                 │
   font-family                                      font-size
   │                                                 │
   ├─ serif                                          ├─ px
   ├─ sans-serif                                     ├─ rem (recommended)
   ├─ monospace                                      ├─ em
   └─ custom fonts (Google Fonts)                    └─ %

        │                                                 │
   font-weight                                     font-style
   │                                                 │
   ├─ normal (400)                                   ├─ normal
   ├─ bold (700)                                     ├─ italic
   └─ 100–900                                        └─ oblique

 ───────────────────────────────────────────────────────────────

        ┌────────────── Text Spacing ───────────────┐
        │                                           │
   line-height                                letter-spacing
   │                                           │
   ├─ 1.5 – 1.8 (good readability)            ├─ 1px
   └─ unitless preferred                      └─ 2px+

 ───────────────────────────────────────────────────────────────

        ┌────────────── Text Formatting ───────────────┐
        │                                               │
   text-align                                   text-decoration
   │                                               │
   ├─ left                                        ├─ underline
   ├─ right                                       ├─ line-through
   ├─ center                                      └─ none
   └─ justify

                 │
          text-transform
                 │
          ├─ uppercase
          ├─ lowercase
          └─ capitalize
```

---

# 📌 Visual Diagram (Beginner-Friendly Layout)

```
+--------------------------------------------------+
|                  CSS TYPOGRAPHY                  |
+--------------------------------------------------+

[ FONT CONTROL ]
----------------------------------------------------
font-family    → Choose font
font-size      → Size of text
font-weight    → Boldness
font-style     → Italic or normal


[ SPACING CONTROL ]
----------------------------------------------------
line-height    → Space between lines
letter-spacing → Space between letters


[ TEXT FORMAT CONTROL ]
----------------------------------------------------
text-align     → left | center | right | justify
text-decoration→ underline | none | line-through
text-transform → uppercase | lowercase | capitalize
```

---

# 🎯 How Everything Works Together (Example)

```css
body {
  font-family: 'Roboto', sans-serif;
  font-size: 1rem;
  line-height: 1.6;
}

h1 {
  font-weight: 700;
  letter-spacing: 1px;
  text-transform: uppercase;
  text-align: center;
}
```
---
# 🧠 Typography Visual Mindmap

```
                           CSS TYPOGRAPHY
                                 │
     ────────────────────────────┼───────────────────────────
                                 │
                         1️⃣ FONT SIZE
                                 │
        ┌───────────────┬───────────────┬───────────────┐
        │               │               │               │
     Keywords          px              rem             em
        │               │               │               │
  small, large      14px, 16px      1rem, 2rem      1.2em, 1.5em
  x-large etc       30px etc        (best practice)  (relative to parent)

                                 │
                         2️⃣ FONT WEIGHT
                                 │
        100 200 300 400 500 600 700 800 900
             │           │
           Light       Normal(400)
                         Bold(700)

                                 │
                         3️⃣ FONT STYLE
                                 │
                    normal | italic | oblique

                                 │
                         4️⃣ FONT FAMILY
                                 │
        ┌───────────────┬────────────────┬─────────────────┐
        │               │                │
     Web Safe       Google Fonts       @font-face
        │               │                │
   Arial            Poppins           Local font file
   Verdana          Roboto            .woff / .ttf
   Georgia          Open Sans

                                 │
                         5️⃣ TEXT CONTROL
                                 │
        ┌───────────────┬───────────────┬───────────────┐
        │               │               │
    line-height     letter-spacing   text-transform
    (1.5–1.8)       (1px, 2px)       uppercase
                                      lowercase
                                      capitalize
```

---

# 📄 Printable Typography Cheat Sheet

You can print this section 📌

---

# 🎨 CSS TYPOGRAPHY QUICK REFERENCE

---

## ✅ FONT SIZE

| Type       | Example              |
| ---------- | -------------------- |
| Keyword    | small, medium, large |
| Pixels     | 14px, 16px, 30px     |
| rem (Best) | 1rem, 2rem           |
| em         | 1.2em                |
| %          | 120%                 |

👉 `1rem = 16px (default)`

---

## ✅ FONT WEIGHT

| Value | Meaning    |
| ----- | ---------- |
| 100   | Thin       |
| 300   | Light      |
| 400   | Normal     |
| 600   | Semi Bold  |
| 700   | Bold       |
| 900   | Extra Bold |

---

## ✅ FONT STYLE

```
normal
italic
oblique
```

---

## ✅ FONT FAMILY

### Web Safe Example:

```css
font-family: Arial, sans-serif;
```

### Google Fonts Example:

```html
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;700&display=swap" rel="stylesheet">
```

```css
body {
  font-family: 'Poppins', sans-serif;
}
```

### Local Font Example:

```css
@font-face {
  font-family: 'MyFont';
  src: url('fonts/MyFont.woff');
}
```

---

## ✅ TEXT SPACING

```css
line-height: 1.6;
letter-spacing: 1px;
```

---

## ✅ TEXT TRANSFORM

```css
text-transform: uppercase;
text-transform: lowercase;
text-transform: capitalize;
```

---

# 🧠 Complete Example (Professional Setup)

```css
html {
  font-size: 16px;
}

body {
  font-family: 'Poppins', sans-serif;
  font-size: 1rem;
  font-weight: 400;
  line-height: 1.6;
}

h1 {
  font-size: 2rem;
  font-weight: 700;
  letter-spacing: 1px;
  text-transform: uppercase;
}
```

---

# 🎯 Beginner Recommended Defaults

✔ Base font size → `16px`
✔ Body text → `1rem`
✔ Headings → `2rem+`
✔ Line height → `1.5–1.8`
✔ Normal weight → `400`
✔ Bold → `700`

---


