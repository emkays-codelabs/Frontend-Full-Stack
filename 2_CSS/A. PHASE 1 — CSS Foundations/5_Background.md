# 🎨 CSS Background Properties — Beginner Step-by-Step Guide

Background properties control what appears **behind** your content (color, images, effects).

---

# ✅ 1️⃣ `background-color`

### 🔹 What it does:

Sets the **background color** of an element.

### 🔹 Example:

```css
div {
  background-color: lightblue;
}
```

You can use:

* Color name → `red`
* Hex → `#ff0000`
* RGB → `rgb(255,0,0)`
* HSL → `hsl(0, 100%, 50%)`

---

# ✅ 2️⃣ `background-image`

### 🔹 What it does:

Sets an **image** as background.

### 🔹 Example:

```css
div {
  background-image: url("image.jpg");
}
```

👉 The image is placed behind the content.

---

# ✅ 3️⃣ `background-repeat`

### 🔹 What it does:

Controls how the background image repeats.

### 🔹 Values:

* `repeat` (default)
* `no-repeat`
* `repeat-x`
* `repeat-y`

### 🔹 Example:

```css
div {
  background-image: url("pattern.png");
  background-repeat: no-repeat;
}
```

---

# ✅ 4️⃣ `background-position`

### 🔹 What it does:

Controls **where** the image appears.

### 🔹 Values:

* `left`, `right`, `center`
* `top`, `bottom`
* or custom values like `50% 50%`

### 🔹 Example:

```css
div {
  background-image: url("image.jpg");
  background-position: center;
}
```

---

# ✅ 5️⃣ `background-size`

### 🔹 What it does:

Controls the **size** of the background image.

### 🔹 Important Values:

* `auto`
* `cover` ✅ (recommended for full sections)
* `contain`
* Custom size: `300px 200px`

### 🔹 Example:

```css
div {
  background-image: url("image.jpg");
  background-size: cover;
}
```

### 🔹 Difference:

| Value   | Meaning                                  |
| ------- | ---------------------------------------- |
| cover   | Fills entire container (may crop image)  |
| contain | Shows full image (may leave empty space) |

---

# ✅ 6️⃣ `background-attachment`

### 🔹 What it does:

Controls whether background scrolls with page.

### 🔹 Values:

* `scroll` (default)
* `fixed`
* `local`

### 🔹 Example:

```css
div {
  background-attachment: fixed;
}
```

---

# 🌄 Parallax Effect (Beginner Explanation)

## 🔹 What is Parallax?

Parallax means:

> Background moves slower than content while scrolling.

It creates a **3D depth effect**.

---

## ✅ Simple Parallax Example

### HTML

```html
<section class="parallax">
  <h1>Welcome</h1>
</section>
```

### CSS

```css
.parallax {
  height: 400px;
  background-image: url("mountain.jpg");
  background-size: cover;
  background-position: center;
  background-attachment: fixed;
}
```

### 🔥 What Happens?

* Text scrolls
* Background stays fixed
* Creates parallax illusion

---

# 🎯 Complete Background Example

```css
body {
  margin: 0;
}

.hero {
  height: 100vh;
  background-color: #222;
  background-image: url("hero.jpg");
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
  background-attachment: fixed;
  color: white;
}
```

---

# 🧠 Background Properties Mindmap

```
                   CSS BACKGROUND
                         │
 ────────────────────────┼────────────────────────
                         │
    background-color     → Sets color
    background-image     → Adds image
    background-repeat    → Repeat control
    background-position  → Image position
    background-size      → Image size
    background-attachment→ Scroll or fixed
```

---

# 📌 Quick Cheat Sheet

| Property              | Purpose          |
| --------------------- | ---------------- |
| background-color      | Background color |
| background-image      | Add image        |
| background-repeat     | Control repeat   |
| background-position   | Position image   |
| background-size       | Resize image     |
| background-attachment | Scroll behavior  |

---

# 🧠 CSS Background + Typography Combined Mindmap

```
                         CSS STYLING
                             │
        ─────────────────────┼─────────────────────
                             │
                     1️⃣ TYPOGRAPHY
                             │
     ┌───────────────────────┼───────────────────────┐
     │                       │                       │
  Font Control           Spacing                Text Formatting
     │                       │                       │
 font-family           line-height              text-align
 font-size             letter-spacing           text-decoration
 font-weight                                      text-transform
 font-style

──────────────────────────────────────────────────────────────

                     2️⃣ BACKGROUND
                             │
     ┌───────────────────────┼───────────────────────┐
     │                       │                       │
   Colors                Images                  Effects
     │                       │                       │
 background-color     background-image       background-attachment
                      background-repeat       (scroll / fixed)
                      background-position
                      background-size
```

---

# 📌 Visual Diagram (Beginner-Friendly Layout)

```
+------------------------------------------------------+
|                     CSS DESIGN                       |
+------------------------------------------------------+

[ TYPOGRAPHY — TEXT DESIGN ]
--------------------------------------------------------
font-family      → Choose font
font-size        → Text size
font-weight      → Boldness
font-style       → Italic style
line-height      → Space between lines
letter-spacing   → Space between letters
text-align       → Alignment
text-decoration  → Underline / line-through
text-transform   → Uppercase / lowercase


[ BACKGROUND — AREA DESIGN ]
--------------------------------------------------------
background-color     → Background color
background-image     → Add image
background-repeat    → Control repetition
background-position  → Image position
background-size      → contain | cover
background-attachment→ scroll | fixed (parallax)
```

---

# 🎯 How They Work Together (Real Example)

```
+--------------------------------------------------+
|                HERO SECTION                      |
|  (Background Image + Styled Typography)         |
|                                                  |
|        WELCOME TO MY WEBSITE                    |
|        Modern Web Design                        |
+--------------------------------------------------+
```

### Example Code

```css
.hero {
  height: 100vh;
  background-image: url("hero.jpg");
  background-size: cover;
  background-position: center;
  background-attachment: fixed;
  color: white;
  text-align: center;
}

.hero h1 {
  font-size: 3rem;
  font-weight: 700;
  letter-spacing: 2px;
  text-transform: uppercase;
}

.hero p {
  font-size: 1.2rem;
  line-height: 1.6;
}
```

---

# 🧩 Concept Understanding (Very Important)

### Typography = Controls TEXT

### Background = Controls AREA behind text

Together they create:

✔ Hero sections
✔ Landing pages
✔ Banners
✔ Cards
✔ Parallax websites

---

