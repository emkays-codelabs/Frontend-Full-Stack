
---

# 1️⃣ Types of Basic CSS Selectors

## 1. Universal Selector (`*`)

* Selects **all elements**
* Used to apply global styles

```css
* {
  margin: 0;
}
```

---

## 2. Element Selector (`tagname`)

* Selects all elements of that type

```css
p {
  color: blue;
}
```

---

## 3. Class Selector (`.classname`)

* Selects elements with a specific class
* Can be reused on multiple elements

```css
.highlight {
  background-color: yellow;
}
```

---

## 4. ID Selector (`#idname`)

* Selects one unique element
* IDs should not repeat

```css
#mainTitle {
  color: red;
}
```

---

# 2️⃣ Combinator Selectors

Combinators define relationships between elements.

---

## 1. Descendant Selector (`A B`)

Selects **B inside A** (at any level).

```css
div p {
  color: green;
}
```

Meaning: All `<p>` inside `<div>` (even nested deep).

---

## 2. Child Selector (`A > B`)

Selects **direct child B of A only**.

```css
div > p {
  color: purple;
}
```

---

## 3. Adjacent Sibling Selector (`A + B`)

Selects the **immediately next sibling**.

```css
h2 + p {
  color: orange;
}
```

---

## 4. General Sibling Selector (`A ~ B`)

Selects **all siblings after A**.

```css
h2 ~ p {
  color: brown;
}
```

---

# 🔥 Complete Working Example (Step-by-Step Sample Page)

Copy this into a `.html` file and run in browser:

```html
<!DOCTYPE html>
<html>
<head>
    <title>CSS Selectors Demo</title>

    <style>
        /* 1. Universal Selector */
        * {
            font-family: Arial;
        }

        /* 2. Element Selector */
        p {
            color: blue;
        }

        /* 3. Class Selector */
        .highlight {
            background-color: yellow;
        }

        /* 4. ID Selector */
        #mainTitle {
            color: red;
        }

        /* 5. Descendant Selector */
        div p {
            color: green;
        }

        /* 6. Child Selector */
        div > span {
            color: purple;
        }

        /* 7. Adjacent Sibling Selector */
        h2 + p {
            color: orange;
        }

        /* 8. General Sibling Selector */
        h3 ~ p {
            color: brown;
        }
    </style>
</head>
<body>

    <h1 id="mainTitle">CSS Selectors Explained</h1>

    <p>This is normal paragraph (Element selector applied)</p>

    <p class="highlight">This paragraph uses class selector</p>

    <div>
        <p>This paragraph is inside div (Descendant selector applied)</p>
        <span>This is direct child span of div (Child selector applied)</span>

        <div>
            <p>This paragraph is nested inside div (Descendant works)</p>
        </div>
    </div>

    <h2>Adjacent Sibling Example</h2>
    <p>This paragraph is immediately after h2 (Adjacent sibling)</p>
    <p>This paragraph is NOT adjacent to h2</p>

    <h3>General Sibling Example</h3>
    <p>This paragraph comes after h3 (General sibling)</p>
    <p>This paragraph also comes after h3 (General sibling)</p>

</body>
</html>
```

---

# 🧠 Visual Understanding Summary

| Selector         | Symbol   | Meaning                     |
| ---------------- | -------- | --------------------------- |
| Universal        | `*`      | Selects all elements        |
| Element          | `p`      | Selects all `<p>`           |
| Class            | `.class` | Selects elements with class |
| ID               | `#id`    | Selects unique element      |
| Descendant       | `A B`    | B inside A                  |
| Child            | `A > B`  | Direct child only           |
| Adjacent Sibling | `A + B`  | Immediately next            |
| General Sibling  | `A ~ B`  | All siblings after          |

---

