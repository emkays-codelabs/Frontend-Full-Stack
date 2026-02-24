
---


# ✅ Complete HTML Example With All Mentioned Tags

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <!-- Base URL for relative links -->
    <base href="https://example.com/" target="_blank">

    <!-- Metadata -->
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="HTML Elements Demonstration">

    <!-- Title of page -->
    <title>Complete HTML Elements Demo</title>

    <!-- Internal CSS -->
    <style>
        body {
            font-family: Arial, sans-serif;
        }
        header, footer {
            background: #f2f2f2;
            padding: 10px;
        }
        nav a {
            margin-right: 10px;
        }
        .highlight {
            color: red;
        }
    </style>

    <!-- External CSS file -->
    <link rel="stylesheet" href="styles.css">

    <!-- JavaScript -->
    <script>
        console.log("Page Loaded");
    </script>
</head>

<body>

    <!-- HEADER -->
    <header>
        <h1>Main Website Title</h1>
        <p>This is the introductory content.</p>
    </header>

    <!-- NAVIGATION -->
    <nav>
        <a href="#section1">Section 1</a>
        <a href="#article">Article</a>
        <a href="https://google.com">Google</a>
    </nav>

    <!-- MAIN CONTENT -->
    <main>

        <!-- SECTION -->
        <section id="section1">
            <h2>Section Example</h2>
            <p>This is a paragraph inside a section.</p>
            <hr>
        </section>

        <!-- ARTICLE -->
        <article id="article">
            <h2>Article Example</h2>
            <p>
                This article is self-contained content.
                <span class="highlight">This text is highlighted using span.</span>
            </p>
        </article>

        <!-- ASIDE -->
        <aside>
            <h3>Related Info</h3>
            <p>This is additional related information.</p>
        </aside>

        <!-- DIV -->
        <div>
            <h3>Generic Div Container</h3>
            <p>Div has no semantic meaning. Used for layout.</p>
        </div>

        <!-- BLOCKQUOTE -->
        <blockquote cite="https://example.com">
            "This is an extended quotation example."
        </blockquote>

        <!-- FIGURE -->
        <figure>
            <img src="image.jpg" alt="Sample Image" width="150">
            <figcaption>This is the image caption.</figcaption>
        </figure>

        <!-- PRE -->
        <pre>
Line 1
    Line 2
        Line 3
        </pre>

        <!-- ORDERED LIST -->
        <h3>Ordered List</h3>
        <ol type="A" start="3">
            <li>Car</li>
            <li>Bike</li>
            <li>Bus</li>
        </ol>

        <!-- UNORDERED LIST -->
        <h3>Unordered List</h3>
        <ul>
            <li>Apple</li>
            <li>Banana</li>
            <li>Orange</li>
        </ul>

        <!-- DESCRIPTION LIST -->
        <h3>Description List</h3>
        <dl>
            <dt>HTML</dt>
            <dd>HyperText Markup Language</dd>

            <dt>CSS</dt>
            <dd>Cascading Style Sheets</dd>
        </dl>

        <!-- ADDRESS -->
        <address>
            Written by Mahesh Kumar <br>
            Nellore, India
        </address>

    </main>

    <!-- FOOTER -->
    <footer>
        <p>&copy; 2026 My Website</p>
    </footer>

</body>

</html>
```

---

# 📘 Explanation of Important Concepts

---

# ✅ Block-Level Elements

Block elements:

* Start on a new line
* Take full width
* Stack vertically

Examples:

```
<header>
<nav>
<main>
<section>
<article>
<aside>
<div>
<p>
<h1>–<h6>
<ol>, <ul>, <li>
<dl>, <dt>, <dd>
<blockquote>
<figure>
<pre>
<footer>
<hr>
```

---

# ✅ Inline Elements

Inline elements:

* Do NOT start on new line
* Take only required width
* Flow inside text

Examples:

```
<a>
<span>
<img>
<strong>
<em>
<b>
<i>
<u>
```

---

# ✅ What is `<span>`?

`<span>` is:

* Inline element
* No semantic meaning
* Used to style small portion of text

Example:

```html
<p>This is <span style="color:red;">important</span> text.</p>
```

Use `<div>` for block.
Use `<span>` for inline.

---

# ✅ Head Elements Explained

| Tag        | Purpose                                   |
| ---------- | ----------------------------------------- |
| `<base>`   | Sets base URL for all relative links      |
| `<meta>`   | Metadata (charset, viewport, description) |
| `<title>`  | Browser tab title                         |
| `<link>`   | External CSS file                         |
| `<style>`  | Internal CSS                              |
| `<script>` | JavaScript                                |

---

# ✅ List Types

### Ordered List `<ol>`

Numbered / Lettered list

### Unordered List `<ul>`

Bullet list

### Description List `<dl>`

Term + Description pair

---

# ✅ Figure Elements

`<figure>` → self-contained media
`<figcaption>` → caption for that media

---

# 🏆 Final Layout Structure

```
html
 ├── head
 │    ├── base
 │    ├── meta
 │    ├── title
 │    ├── style
 │    ├── link
 │    └── script
 │
 └── body
      ├── header
      ├── nav
      ├── main
      │    ├── section
      │    ├── article
      │    ├── aside
      │    ├── div
      │    ├── lists
      │    ├── figure
      │    └── address
      └── footer
```

---
