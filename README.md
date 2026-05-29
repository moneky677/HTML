# 📚 HTML Reference Guide

A complete reference guide covering everything you need to know about HTML.

---

## 🏗️ Document Skeleton

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>Page Title</title>
    <link rel="stylesheet" href="style.css">
  </head>
  <body>
    <!-- Content goes here -->

    <script src="script.js"></script>
  </body>
</html>
```

| Tag | Purpose |
|-----|---------|
| `<!DOCTYPE html>` | Tells browser this is HTML5 |
| `<html>` | Root element of the page |
| `<head>` | Behind the scenes info (title, links) |
| `<body>` | Everything visible on the page |

---

## 🔤 Headings

```html
<h1>Heading 1 (biggest)</h1>
<h2>Heading 2</h2>
<h3>Heading 3</h3>
<h4>Heading 4</h4>
<h5>Heading 5</h5>
<h6>Heading 6 (smallest)</h6>
```

---

## 📜 Text & Paragraphs

```html
<p>Regular paragraph text.</p>

<pre>
  Pre-formatted text
  preserves spaces and line breaks.
</pre>

<br>   <!-- line break (self-closing) -->
<hr>   <!-- horizontal line (self-closing) -->

<!-- Comment (not visible on page) -->
```

---

## ✍️ Text Formatting

| Tag | Effect |
|-----|--------|
| `<b>` / `<strong>` | **Bold** |
| `<i>` / `<em>` | *Italic* |
| `<u>` | Underline |
| `<del>` | ~~Strikethrough~~ |
| `<mark>` | Highlight |
| `<small>` | Smaller text |
| `<big>` | Bigger text |
| `<sub>` | Subscript (H₂O) |
| `<sup>` | Superscript (x²) |
| `<ins>` | Inserted/underlined text |
| `<tt>` | Monospace font |
| `<code>` | Inline code |

```html
<p>Water is H<sub>2</sub>O</p>
<p>x<sup>2</sup> + y<sup>2</sup> = z<sup>2</sup></p>
<mark style="background-color: lightgreen;">highlighted</mark>
```

---

## 🖼️ Images

```html
<img src="images/dog.jpg" alt="A cute dog" width="300" height="200">
```

| Attribute | Purpose |
|-----------|---------|
| `src` | File path or URL of the image |
| `alt` | Text shown if image fails to load |
| `width` | Width in pixels |
| `height` | Height in pixels |

> Tip: Set only width OR height to keep the aspect ratio

---

## 🔗 Links

```html
<!-- Basic link -->
<a href="https://www.google.com">Click here</a>

<!-- Open in new tab -->
<a href="https://www.google.com" target="_blank">Click here</a>

<!-- Tooltip on hover -->
<a href="https://www.google.com" title="Go to Google">Click here</a>

<!-- Clickable image -->
<a href="https://www.google.com">
    <img src="logo.png" alt="Logo" width="100">
</a>

<!-- Link to another page in same folder -->
<a href="about.html">About</a>
```

---

## 🎧 Audio

```html
<audio controls>
    <source src="music/song.mp3" type="audio/mpeg">
    <source src="music/song.wav" type="audio/wav">
    Your browser does not support audio.
</audio>
```

| Attribute | Effect |
|-----------|--------|
| `controls` | Shows play/pause buttons |
| `autoplay` | Starts automatically |
| `muted` | Starts muted |
| `loop` | Repeats when finished |

---

## 🎥 Video

```html
<video width="500" controls autoplay muted loop>
    <source src="videos/clip.mp4" type="video/mp4">
    Your browser does not support video.
</video>
```

---

## 🌐 Favicon

```html
<head>
    <link rel="icon" type="image/png" href="images/favicon.png">
</head>
```

---

## 📦 Containers

| Tag | Type | Use |
|-----|------|-----|
| `<div>` | Block | Groups sections, layout |
| `<span>` | Inline | Styles part of a sentence |

```html
<!-- div takes full width, starts new line -->
<div style="background-color: lightblue;">
    <h1>Hello</h1>
    <p>Inside the div</p>
</div>

<!-- span stays inline with text -->
<p>This is <span style="color: red;">red</span> text.</p>
```

---

## 📋 Lists

### Unordered List (bullets)
```html
<ul>
    <li>Milk</li>
    <li>Eggs</li>
    <li>Bread
        <ul>
            <li>White</li>
            <li>Brown</li>
        </ul>
    </li>
</ul>
```

### Ordered List (numbers)
```html
<ol>
    <li>Wake up</li>
    <li>Eat breakfast</li>
    <li>Go to school</li>
</ol>
```

### Description List
```html
<dl>
    <dt>Dragon</dt>
    <dd>A mythical fire-breathing creature.</dd>

    <dt>Phoenix</dt>
    <dd>An immortal bird from Greek mythology.</dd>
</dl>
```

---

## 📊 Tables

```html
<table border="1">
    <tr>
        <th>Name</th>
        <th>Age</th>
        <th>City</th>
    </tr>
    <tr>
        <td>SpongeBob</td>
        <td>30</td>
        <td>Bikini Bottom</td>
    </tr>
    <tr>
        <td>Patrick</td>
        <td>34</td>
        <td>Bikini Bottom</td>
    </tr>
</table>
```

| Tag | Purpose |
|-----|---------|
| `<table>` | Creates the table |
| `<tr>` | Table row |
| `<th>` | Table header (bold by default) |
| `<td>` | Table data cell |

> Place content under a specific column by adding empty `<td>` tags to skip columns

---

## 📝 Forms

```html
<form action="submit.php" method="post">

    <!-- Text input -->
    <label for="username">Username:</label>
    <input type="text" id="username" name="username" placeholder="Enter name" required>
    <br>

    <!-- Password -->
    <label for="pwd">Password:</label>
    <input type="password" id="pwd" name="pwd" minlength="6" required>
    <br>

    <!-- Email -->
    <label for="email">Email:</label>
    <input type="email" id="email" name="email" required>
    <br>

    <!-- Number -->
    <label for="qty">Quantity:</label>
    <input type="number" id="qty" name="qty" min="0" max="99" value="1">
    <br>

    <!-- Date -->
    <label for="bday">Birthday:</label>
    <input type="date" id="bday" name="bday">
    <br>

    <!-- Radio buttons (same name = same group) -->
    <p>Title:</p>
    <input type="radio" id="mr" name="title" value="Mr">
    <label for="mr">Mr</label>
    <input type="radio" id="miss" name="title" value="Miss">
    <label for="miss">Miss</label>
    <br>

    <!-- Dropdown -->
    <label for="payment">Payment:</label>
    <select id="payment" name="payment">
        <option value="visa">Visa</option>
        <option value="mastercard">MasterCard</option>
    </select>
    <br>

    <!-- Checkbox -->
    <label for="subscribe">Subscribe:</label>
    <input type="checkbox" id="subscribe" name="subscribe">
    <br>

    <!-- Textarea -->
    <label for="comment">Comment:</label>
    <textarea id="comment" name="comment" rows="3" cols="25"></textarea>
    <br>

    <!-- File upload -->
    <label for="file">Upload:</label>
    <input type="file" id="file" accept="image/png, image/jpeg">
    <br>

    <!-- Buttons -->
    <input type="submit" value="Submit">
    <input type="reset" value="Clear">

</form>
```

### Form Attributes

| Attribute | Purpose |
|-----------|---------|
| `required` | Field must be filled |
| `placeholder` | Hint text inside field |
| `minlength` / `maxlength` | Min/max characters |
| `min` / `max` | Min/max value for numbers |
| `pattern` | Regex the input must match |

---

## 🏷️ Semantic Tags

These tags work like `<div>` but describe their purpose:

```html
<header>
    <h1>My Website</h1>
    <nav>
        <a href="index.html">Home</a>
        <a href="about.html">About</a>
    </nav>
</header>

<main>
    <section>
        <h2>Section Title</h2>
        <p>Section content...</p>
    </section>

    <article>
        <h2>Blog Post Title</h2>
        <p>Article content...</p>
    </article>

    <aside>
        <h2>Related Links</h2>
    </aside>
</main>

<footer>
    <p>&copy; 2024 My Website</p>
</footer>
```

| Tag | Use |
|-----|-----|
| `<header>` | Top of page — logo, title, nav |
| `<nav>` | Navigation links |
| `<main>` | Main page content (one per page) |
| `<section>` | Grouped related content |
| `<article>` | Self-contained content (blog, news) |
| `<aside>` | Sidebar, related content |
| `<footer>` | Bottom of page — copyright, contact |

---

## 🎨 Applying CSS

```html
<!-- Inline (on the element) -->
<h1 style="color: red; font-size: 2em;">Hello</h1>

<!-- Internal (in <head>) -->
<head>
    <style>
        h1 { color: red; }
    </style>
</head>

<!-- External (separate file) -->
<head>
    <link rel="stylesheet" href="style.css">
</head>
```

---

## 🔗 Linking Files

```html
<head>
    <!-- CSS -->
    <link rel="stylesheet" href="style.css">

    <!-- Favicon -->
    <link rel="icon" href="favicon.png">

    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Roboto&display=swap" rel="stylesheet">
</head>

<body>
    <!-- JavaScript (place before </body>) -->
    <script src="script.js"></script>
</body>
```

---

## 🔘 Buttons

```html
<!-- Basic button -->
<button>Click Me</button>

<!-- Linked button -->
<a href="https://www.google.com">
    <button>Go to Google</button>
</a>

<!-- Button with JavaScript -->
<button onclick="alert('Hello!')">Click Me</button>
```

---

## 🌍 Special Characters (HTML Entities)

| Entity | Output |
|--------|--------|
| `&lt;` | `<` |
| `&gt;` | `>` |
| `&amp;` | `&` |
| `&copy;` | © |
| `&trade;` | ™ |
| `&nbsp;` | (non-breaking space) |
| `&laquo;` | « |
| `&raquo;` | » |

```html
<!-- Display code as text -->
<pre>
    &lt;h1&gt;Hello World&lt;/h1&gt;
</pre>
```

---

## 🏷️ Common Attributes

| Attribute | Use |
|-----------|-----|
| `id` | Unique identifier for one element |
| `class` | Reusable style group (can have multiple) |
| `style` | Inline CSS styling |
| `title` | Tooltip on hover |
| `href` | Link destination |
| `src` | File path for images/scripts |
| `alt` | Alternative text for images |
| `width` / `height` | Size in pixels |
| `target="_blank"` | Open link in new tab |

```html
<!-- Multiple classes separated by space -->
<p class="red bold large">Hello</p>

<!-- id targets one specific element -->
<p id="intro">Introduction paragraph</p>
```

---

## 🧠 Tips

- Always close your tags
- `<head>` is for behind the scenes info, `<body>` is for visible content
- `id` = unique (use once), `class` = reusable (use many times)
- Images inside tables must be in `<td>` tags
- `<br>` and `<img>` are self-closing (no end tag needed)
- Put `<script>` at the bottom of `<body>` so HTML loads first
- Use semantic tags (`<header>`, `<nav>`, etc.) instead of just `<div>` where possible

---

*Notes based on the HTML & CSS Full Course by Bro Code.*
