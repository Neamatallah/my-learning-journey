# HTML Notes

A practical reference covering HTML fundamentals, document structure, text, links, images, lists, tables, semantic HTML, media, forms, accessibility, and common HTML concepts.

## 1. HTML Fundamentals

### What is HTML?

**HTML** stands for **HyperText Markup Language**.

HTML is the standard markup language used to structure the content and meaning of web pages.

HTML describes **what content is and how it is structured**, while technologies such as CSS are used for presentation and styling.

---

## 2. HTML Elements and Tags

HTML documents are built using **elements**.

Example:

```html
<p>Hello World</p>
```

The structure contains:

* `<p>` → opening tag
* `Hello World` → content
* `</p>` → closing tag
* the complete structure → the HTML element

Some elements do not have closing tags. These are called **void elements**.

Examples:

```html
<meta>
<br>
<img>
<input>
```

---

## 3. `index.html`

`index.html` is commonly used as the **main/default HTML document** of a website.

Example:

```text
My Website/
└── index.html
```

When a server receives a request for a directory without a specific document, a default document such as `index.html` may be used.

---

## 4. The `.html` Extension

The `.html` extension identifies a file as an HTML document.

Examples:

```text
index.html
about.html
contact.html
```

---

# 5. HTML Document Structure

A basic HTML document is structured around:

```html
<!DOCTYPE html>
<html>
<head>
    ...
</head>
<body>
    ...
</body>
</html>
```

The main parts are:

```text
<!DOCTYPE html>
        ↓
<html>
 ├── <head>
 └── <body>
```

---

## `<!DOCTYPE html>`

### Meaning

`DOCTYPE` means **Document Type Declaration**.

### Purpose

The HTML5 declaration:

```html
<!DOCTYPE html>
```

tells the browser that the document is an HTML document and helps the browser use modern standards-based rendering.

### Important Note

`<!DOCTYPE html>` is a **declaration**, not a normal HTML element.

It does not have a closing tag.

---

## Standards Mode and Quirks Mode

Browsers can render documents using different compatibility modes.

### Standards Mode

The browser follows modern web standards.

### Almost Standards Mode

A mode between Standards Mode and Quirks Mode with limited compatibility behavior.

### Quirks Mode

A compatibility mode that reproduces some older browser behavior.

Using the correct HTML5 DOCTYPE ensures the document is rendered in **Standards Mode**.

---

# 6. `<html>`

### Meaning

`<html>` is the **root element** of the HTML document.

### Purpose

It contains the entire document, including:

* `<head>`
* `<body>`

Example:

```html
<html>
    <head>
        ...
    </head>

    <body>
        ...
    </body>
</html>
```

---

# 7. `<head>`

### Purpose

`<head>` contains information **about the document**, such as metadata and the document title.

Common elements placed inside it include:

```html
<title>
<meta>
```

The `<head>` is different from the `<body>` because it does not contain the normal visible page content.

---

# 8. `<body>`

### Purpose

`<body>` contains the main content of the webpage.

Examples include:

* headings
* paragraphs
* lists
* tables
* images
* links
* forms
* media
* other page content

Example:

```html
<body>
    <h1>My CV</h1>
    <p>Welcome to my page.</p>
</body>
```

---

# 9. `<title>`

### Meaning

`title` represents the **title of the document**.

### Purpose

Defines the document title used by the browser.

```html
<head>
    <title>My CV</title>
</head>
```

It can appear in places such as:

* the browser tab
* bookmarks
* browser interfaces

`<title>` belongs inside `<head>` and has a closing tag.

---

# 10. `<meta>`

### Meaning

`meta` refers to **metadata** — information about the document.

### Purpose

Provides information about the HTML document to browsers, search engines, and other systems.

Example:

```html
<meta charset="UTF-8">
```

`<meta>` is a **void element**, so it does not have a closing tag.

---

## `charset`

### Meaning

`charset` means **character set / character encoding**.

### Purpose

Specifies the character encoding used by the document.

Example:

```html
<meta charset="UTF-8">
```

### UTF-8

UTF-8 is a character encoding that supports a very large range of characters and languages.

It allows text such as Arabic and English to be interpreted correctly.

---

## `name`

With `<meta>`, `name` identifies the type/name of metadata being provided.

Example:

```html
<meta name="description" content="A personal CV page">
```

---

## `content`

`content` contains the actual value associated with the metadata.

Example:

```html
<meta name="description" content="A personal CV page">
```

Here:

```text
name    → description
content → A personal CV page
```

The content is metadata and does not appear as normal visible text inside the webpage.

---

# 11. HTML Comments

### Syntax

```html
<!-- This is a comment -->
```

### Purpose

Comments are notes written inside the HTML source.

They can be used to:

* explain code
* organize sections
* leave development notes

Comments are not displayed as normal page content.

---

# 12. Rendering

**Rendering** is the process in which the browser interprets the webpage and produces the visual result shown to the user.

Conceptually:

```text
HTML
  ↓
Browser
  ↓
Rendering
  ↓
Visible Webpage
```

---

# 13. Headings

HTML provides six heading levels:

```html
<h1>Heading 1</h1>
<h2>Heading 2</h2>
<h3>Heading 3</h3>
<h4>Heading 4</h4>
<h5>Heading 5</h5>
<h6>Heading 6</h6>
```

### Meaning

`h` stands for **heading**.

### Hierarchy

```text
<h1>
 ├── <h2>
 │    ├── <h3>
 │    └── <h3>
 └── <h2>
```

The heading level represents the **hierarchy and importance of the heading**, not simply its visual size.

* `<h1>` → highest/main heading level
* `<h2>` → subsection
* `<h3>` → lower-level subsection
* ...
* `<h6>` → lowest heading level

---

# 14. `<p>`

### Meaning

`p` stands for **paragraph**.

### Purpose

Represents a paragraph of text.

```html
<p>This is a paragraph.</p>
```

### Block-Level Element

`<p>` is a **block-level element**.

It normally starts on a new line and occupies the available width of its containing area.

---

# 15. Attributes

### What is an Attribute?

An **attribute** provides additional information or configuration for an HTML element.

General syntax:

```html
<element attribute="value">
```

Example:

```html
<p class="intro">Hello</p>
```

Here:

```text
class → attribute
"intro" → attribute value
```

Attributes are generally written in the opening tag.

---

## Global Attributes

**Global attributes** can be used on many different HTML elements.

Examples include:

```text
class
id
title
hidden
```

Some attributes are instead associated with particular elements.

Examples:

```text
href
src
charset
```

---

## Attribute Values and Quotation Marks

These forms can work for a simple one-word value:

```html
<p class="intro">Hello</p>
```

```html
<p class='intro'>Hello</p>
```

```html
<p class=intro>Hello</p>
```

Quotation marks become important when a value contains spaces:

```html
<p class="my element">Hello</p>
```

Without quotation marks, the space can cause the value to be interpreted incorrectly.

---

## Boolean Attributes

A **boolean attribute** is enabled by its presence.

Example:

```html
<p hidden>Hidden content</p>
```

The attribute does not need a normal value.

---

# 16. `<hr>`

### Meaning

`hr` represents a **thematic break** or separation between sections of content.

Example:

```html
<p>Product One</p>

<hr>

<p>Product Two</p>
```

It is commonly rendered as a horizontal line by default.

---

# 17. Text and Inline Elements

## `<b>`

### Meaning

`b` is used to **bring attention** to text.

### Purpose

Used to draw attention to text without expressing strong semantic importance.

```html
<p>This is <b>important text</b>.</p>
```

---

## `<strong>`

### Purpose

Represents **strong importance**.

```html
<p><strong>Warning:</strong> Save your work.</p>
```

### Difference

```text
<strong> → strong importance
<b>      → attention/distinction
```

The visual appearance of `<strong>` may be bold, but its meaning is semantic importance rather than simply bold styling.

---

## `<i>`

### Purpose

Represents text that is stylistically or semantically distinct from the surrounding content.

```html
<p>The term <i>HTML</i> is commonly used in web development.</p>
```

---

## `<em>`

### Meaning

`em` represents **emphasis**.

### Purpose

Adds semantic emphasis to text.

```html
<p>This is <em>very</em> important.</p>
```

### Difference

```text
<i>   → text that is distinct from surrounding content
<em> → emphasis
```

Both may appear italic by default, but their meanings are different.

---

## `<mark>`

### Meaning

Mark / highlighted text.

### Purpose

Highlights text.

```html
<p>This is <mark>important</mark>.</p>
```

---

## `<u>`

### Purpose

Represents underlined text.

```html
<p><u>Underlined text</u></p>
```

---

## `<small>`

### Purpose

Represents smaller text or side information.

```html
<p><small>Additional information</small></p>
```

---

## `<s>`

### Purpose

Represents information that is no longer accurate, relevant, or current.

```html
<p><s>$100</s> $80</p>
```

### Difference from `<del>`

```text
<s>   → no longer accurate/relevant/current
<del> → content that has been deleted
```

---

## `<del>`

### Meaning

`del` represents **deleted content**.

### Purpose

Represents content that has been removed from the document.

```html
<p><del>Second Year</del> Third Year</p>
```

This can be useful when showing an old value that has been replaced.

---

## `<ins>`

### Meaning

`ins` represents **inserted content**.

### Purpose

Represents content that has been added.

```html
<p><ins>Third Year</ins></p>
```

---

## `<sub>`

### Meaning

Subscript.

### Purpose

Places content lower than the normal text line.

Useful for scientific and mathematical notation.

```html
H<sub>2</sub>O
```

---

## `<sup>`

### Meaning

Superscript.

### Purpose

Places content higher than the normal text line.

```html
x<sup>2</sup>
```

---

# 18. Links

## `<a>`

### Meaning

`a` stands for **Anchor**.

### Purpose

Creates a hyperlink to another location.

```html
<a href="https://example.com">Visit the website</a>
```

The clickable text is placed between the opening and closing tags.

`<a>` is inline by default.

---

## `href`

### Meaning

**href = Hypertext Reference**

### Purpose

Specifies the destination of a hyperlink.

```html
<a href="https://example.com">Visit</a>
```

---

## `target`

### Purpose

Specifies where the linked document or result should open.

```html
<a href="https://example.com" target="_blank">
    Open Website
</a>
```

### `_blank`

`target="_blank"` opens the destination in a new browsing context, commonly a new tab.

---

## `title` Attribute

The `title` attribute can provide additional information about a link.

```html
<a
    href="https://example.com"
    title="Open Example Website"
>
    Example
</a>
```

It can appear as a tooltip when hovering over the link.

---

## Internal Page Links

An element can be identified using `id`:

```html
<h2 id="about">About</h2>
```

A link can then point to it:

```html
<a href="#about">Go to About</a>
```

Relationship:

```text
id="about"
     ↑
href="#about"
```

The `#` indicates that the destination is an element identified by that ID.

---

## `mailto:`

Creates an email link.

```html
<a href="mailto:example@gmail.com">
    Send me an email
</a>
```

`mailto:` tells the browser that the link is intended to open an email application/composer.

---

# 19. Images

## `<img>`

### Meaning

`img` stands for **image**.

### Purpose

Embeds an image into the page.

```html
<img src="CV.png" alt="My CV">
```

`<img>` is a **void element**, so it does not have a closing tag.

---

## `src`

### Meaning

`src` stands for **source**.

### Purpose

Specifies the location/source of the image.

```html
<img src="CV.png" alt="CV">
```

Think:

```text
src → Where is the image?
```

---

## `alt`

### Meaning

`alt` stands for **alternative text**.

### Purpose

Provides alternative text describing the image.

```html
<img src="CV.png" alt="My CV">
```

It is useful when:

* the image cannot be displayed;
* assistive technologies need a textual description.

---

# 20. Relative Paths

A **relative path** describes a file location relative to the current HTML file.

Example:

```text
My Website/
├── index.html
└── CV.png
```

The image can be referenced as:

```html
<img src="CV.png" alt="CV">
```

For a subfolder:

```text
My Website/
├── index.html
└── Pictures/
    └── Shop.jpg
```

Use:

```html
<img src="Pictures/Shop.jpg" alt="Shop">
```

---

## Project-Relative Path vs Windows Path

A Windows filesystem path may look like:

```text
C:\Users\...\Pictures\Shop.jpg
```

This is a machine-specific filesystem path.

For resources inside a web project, use a project-relative path:

```text
index.html
Pictures/
└── Shop.jpg
```

```html
<img src="Pictures/Shop.jpg" alt="Shop">
```

Key idea:

```text
Windows absolute path
        ≠
Project-relative web path
```

---

# 21. Lists

HTML provides several types of lists:

```text
<ul> → unordered list
<ol> → ordered list
<dl> → description list
```

---

## `<ul>`

### Meaning

**UL = Unordered List**

### Purpose

Creates a list where the order of items is not important.

```html
<ul>
    <li>HTML</li>
    <li>CSS</li>
    <li>Git</li>
</ul>
```

The browser normally displays unordered-list items with bullets.

---

## `<ol>`

### Meaning

**OL = Ordered List**

### Purpose

Creates a list where order or sequence matters.

```html
<ol>
    <li>First</li>
    <li>Second</li>
    <li>Third</li>
</ol>
```

Result:

```text
1. First
2. Second
3. Third
```

---

## `<li>`

### Meaning

**LI = List Item**

### Purpose

Represents one individual item inside a list.

```html
<li>HTML</li>
```

---

## `reversed`

Reverses the numbering of an ordered list.

```html
<ol reversed>
    <li>First</li>
    <li>Second</li>
    <li>Third</li>
</ol>
```

Result:

```text
3. First
2. Second
1. Third
```

`reversed` is a boolean attribute: its presence activates the behavior.

---

## `start`

Specifies the starting number of an ordered list.

```html
<ol start="5">
    <li>First</li>
    <li>Second</li>
    <li>Third</li>
</ol>
```

Result:

```text
5. First
6. Second
7. Third
```

Think:

```text
start → What number should the list start from?
```

---

## `type`

Specifies the marker style of an ordered list.

| Value | Marker Style |
| ----- | ------------ |
| `1`   | 1, 2, 3      |
| `A`   | A, B, C      |
| `a`   | a, b, c      |
| `I`   | I, II, III   |
| `i`   | i, ii, iii   |

Example:

```html
<ol type="A">
    <li>HTML</li>
    <li>CSS</li>
    <li>JavaScript</li>
</ol>
```

---

## `<li value="">`

Specifies the numbering value of an individual list item in an ordered list.

```html
<ol>
    <li>HTML</li>
    <li value="5">CSS</li>
    <li>JavaScript</li>
</ol>
```

This can be used to control the numbering of a particular `<li>`.

---

# 22. Nested Lists

### Meaning

A **nested list** is a list placed inside another list.

The inner list is normally placed inside the relevant `<li>`.

```html
<ul>
    <li>
        Frontend
        <ul>
            <li>HTML</li>
            <li>CSS</li>
        </ul>
    </li>

    <li>
        Backend
        <ul>
            <li>Python</li>
            <li>SQL</li>
        </ul>
    </li>
</ul>
```

Structure:

```text
List
└── List Item
    └── Nested List
        ├── List Item
        └── List Item
```

Nested lists are useful for representing hierarchical or grouped information.

---

# 23. Description Lists

## `<dl>`

### Meaning

**DL = Description List**

### Purpose

Creates a list of terms and their associated descriptions/details.

```html
<dl>
    <dt>HTML</dt>
    <dd>HyperText Markup Language</dd>

    <dt>Git</dt>
    <dd>A version control system.</dd>
</dl>
```

---

## `<dt>`

### Meaning

**DT = Description Term**

Represents the term being described.

```html
<dt>HTML</dt>
```

---

## `<dd>`

### Meaning

**DD = Description Details**

Provides the description/details associated with the term.

```html
<dd>HyperText Markup Language</dd>
```

Mental model:

```text
<dl> → whole description list
<dt> → term
<dd> → description/details
```

---

# 24. Tables

Tables organize structured data into rows and columns.

Basic example:

```html
<table>
    <tr>
        <th>Name</th>
        <th>Age</th>
    </tr>

    <tr>
        <td>Neamatalla</td>
        <td>19</td>
    </tr>
</table>
```

---

## `<table>`

Represents the table.

---

## `<tr>`

### Meaning

**TR = Table Row**

Represents one row.

```html
<tr>
    ...
</tr>
```

A row contains table cells such as:

```text
<th> → header cell
<td> → data cell
```

---

## `<th>`

### Meaning

**TH = Table Header**

Represents a header cell.

```html
<th>Name</th>
```

A `<th>` is usually displayed in bold by default.

However:

> `<th>` does **not** mean "bold text".

Its semantic purpose is to identify a table header.

---

## `<td>`

### Meaning

**TD = Table Data**

Represents a normal data cell.

```html
<td>Neamatalla</td>
```

Mental model:

```text
<tr> → row
<th> → header cell
<td> → data cell
```

---

## `<thead>`

### Meaning

**Table Head / Table Header Section**

Groups the header rows of a table.

```html
<thead>
    <tr>
        <th>Name</th>
        <th>Age</th>
    </tr>
</thead>
```

---

## `<tbody>`

### Meaning

**Table Body**

Groups the main data rows.

```html
<tbody>
    <tr>
        <td>Neamatalla</td>
        <td>19</td>
    </tr>
</tbody>
```

---

## `<tfoot>`

### Meaning

**Table Foot / Table Footer**

Groups footer or concluding rows.

```html
<tfoot>
    <tr>
        <td>Total</td>
        <td>1</td>
    </tr>
</tfoot>
```

---

## `<caption>`

### Purpose

Provides a caption/title for the table itself.

```html
<table>
    <caption>Students Information</caption>
</table>
```

Important distinction:

```text
<title>   → document/page title
<caption> → table caption
```

---

## Complete Table Structure

```html
<table>

    <caption>Students Information</caption>

    <thead>
        <tr>
            <th>Name</th>
            <th>Age</th>
        </tr>
    </thead>

    <tbody>
        <tr>
            <td>Neamatalla</td>
            <td>19</td>
        </tr>
    </tbody>

    <tfoot>
        <tr>
            <td>Total</td>
            <td>1 Student</td>
        </tr>
    </tfoot>

</table>
```

Hierarchy:

```text
<table>
├── <caption>
├── <thead>
│   └── <tr>
│       └── <th>
├── <tbody>
│   └── <tr>
│       └── <td>
└── <tfoot>
    └── <tr>
        └── <td>
```

---

## `colspan`

### Meaning

Column Span.

### Purpose

Allows a cell to span across multiple columns.

```html
<tr>
    <td colspan="2">Total</td>
</tr>
```

`colspan="2"` means the cell occupies the space of two columns.

---

## `rowspan`

### Meaning

Row Span.

### Purpose

Allows a cell to span multiple rows vertically.

```html
<tr>
    <td rowspan="2">Category</td>
    <td>Item One</td>
</tr>

<tr>
    <td>Item Two</td>
</tr>
```

`rowspan="2"` means the cell occupies the space of two rows.

---

## `border`

`border` can be used as a basic HTML table attribute to display a border.

Example:

```html
<table border="1">
```

It is useful for simple table experiments, while modern presentation and styling are normally handled with CSS.

---

## `cellpadding`

`cellpadding` controls the space between the cell content and the cell border in older HTML table usage.

Example:

```html
<table cellpadding="10">
```

Modern table presentation is normally handled with CSS.

---

# 25. `<span>`

### Meaning

`span` is a generic inline container.

### Purpose

Wraps a small piece of content, especially when that part needs to be targeted separately.

```html
<p>
    Hello <span>World</span>
</p>
```

`<span>` is **inline** by default.

---

# 26. `<div>`

### Meaning

`div` represents a generic **division/container**.

### Purpose

Groups elements together as a block-level container.

```html
<div class="product">
    <h2>Book</h2>
    <p>$20</p>
</div>
```

Mental model:

```text
<div>  → generic block container
<span> → generic inline container
```

A parent does not automatically pass every CSS property to its children. Some properties inherit, while others do not.

---

# 27. `<br>`

### Meaning

**BR = Line Break**

### Purpose

Creates a line break.

```html
Hello<br>
World
```

Result:

```text
Hello
World
```

`<br>` is a void element and has no closing tag.

Correct:

```html
<br>
```

Not:

```html
</br>
```

---

# 28. HTML Entities

HTML entities represent special characters that have special meanings in HTML or are difficult to type directly.

| Entity    | Displays |
| --------- | -------- |
| `&gt;`    | `>`      |
| `&lt;`    | `<`      |
| `&amp;`   | `&`      |
| `&asymp;` | `≈`      |
| `&copy;`  | `©`      |

Examples:

```html
<p>5 &lt; 10</p>
```

Displays:

```text
5 < 10
```

Another example:

```html
<p>Tom &amp; Jerry</p>
```

Displays:

```text
Tom & Jerry
```

---

# 29. Semantic HTML5

### What is Semantic HTML?

Semantic HTML uses elements whose names communicate the **meaning and role** of their content.

Instead of using only generic containers:

```html
<div id="header">
```

HTML5 provides meaningful elements:

```html
<header>
```

Semantic elements help developers, browsers, search engines, and assistive technologies understand the structure of a page.

They do not automatically provide visual styling.

---

## `<header>`

Represents introductory/header content for a page or section.

```html
<header>
    <h1>My Website</h1>
</header>
```

---

## `<nav>`

### Meaning

Navigation.

### Purpose

Represents a section containing navigation links.

```html
<nav>
    <a href="#home">Home</a>
    <a href="#about">About</a>
</nav>
```

---

## `<main>`

Represents the main content of the document.

```html
<main>
    <h1>My CV</h1>
</main>
```

---

## `<section>`

Represents a thematic section of content.

```html
<section>
    <h2>Education</h2>
    <p>Engineering Student</p>
</section>
```

---

## `<article>`

Represents a self-contained piece of content.

```html
<article>
    <h2>My Project</h2>
    <p>Project description...</p>
</article>
```

---

## `<aside>`

Represents content related to the surrounding content but separate from the main flow.

```html
<aside>
    <h2>Contact</h2>
    <p>Email: example@email.com</p>
</aside>
```

---

## `<footer>`

Represents footer content for a page or section.

```html
<footer>
    <p>Copyright 2026</p>
</footer>
```

---

# 30. Audio

## `<audio>`

### Purpose

Embeds audio content into a webpage.

```html
<audio controls>
    <source src="audio.mp3" type="audio/mpeg">
</audio>
```

---

# 31. `<source>`

### Meaning

`source` represents a **media source**.

### Purpose

Specifies a media file used by `<audio>` or `<video>`.

```html
<audio controls>
    <source src="song.mp3" type="audio/mpeg">
</audio>
```

Multiple sources can be provided when different formats are available:

```html
<audio controls>
    <source src="song.mp3" type="audio/mpeg">
    <source src="song.ogg" type="audio/ogg">
</audio>
```

---

## `src`

Specifies the location of the media source.

```html
<source src="song.mp3">
```

---

## `type`

Specifies the media type/MIME type.

```html
<source
    src="song.mp3"
    type="audio/mpeg"
>
```

---

## `controls`

Displays the browser's built-in media controls.

```html
<audio controls>
    ...
</audio>
```

---

---

## `Autoplay`

play automatically, without action from a user.

```html
<audio autoplay>
    ...
</audio>
```

---
## `loop`

Causes the media to repeat after it finishes.

```html
<audio controls loop>
    <source src="song.mp3" type="audio/mpeg">
</audio>
```

Conceptually:

```text
play → finish → play again
```

---

## `muted`

Starts the media without sound.

```html
<video controls muted>
    ...
</video>
```

---

# 32. Video

## `<video>`

### Purpose

Embeds video content into a webpage.

```html
<video controls>
    <source src="video.mp4" type="video/mp4">
</video>
```

The general media structure is similar to `<audio>`.

---

## `width`

Specifies the displayed width of the video.

```html
<video controls width="600">
    ...
</video>
```

---

## `height`

Specifies the displayed height of the video.

```html
<video controls height="400">
    ...
</video>
```

---

## `poster`

Specifies an image displayed before the video is played.

```html
<video
    controls
    poster="thumbnail.jpg"
>
    <source src="video.mp4" type="video/mp4">
</video>
```

Think:

```text
poster → preview image for the video
```

---

# 33. Text Tracks

## `<track>`

Provides timed text tracks for media, such as subtitles or captions.

Example:

```html
<video controls>
    <source src="video.mp4" type="video/mp4">

    <track
        src="subtitles-en.vtt"
        kind="subtitles"
        srclang="en"
        label="English"
    >
</video>
```

`.vtt` is the text-track file format used for timed text.

---

## `kind`

Specifies the type/purpose of the text track.

Example:

```html
<track
    src="subtitles-en.vtt"
    kind="subtitles"
>
```

Common purposes include subtitles, captions, descriptions, chapters, and metadata.

---

## `srclang`

### Meaning

**Source Language**

### Purpose

Specifies the language of the text track.

```html
srclang="en"
```

---

## `label`

Provides a human-readable name for the track.

```html
label="English"
```

Difference:

```text
srclang → language code
label   → readable name
```

---

# 34. Forms

## `<form>`

### Purpose

Defines a form used to collect and submit user input.

```html
<form>
    ...
</form>
```

---

## `action`

### Purpose

Specifies where the submitted form data is sent.

```html
<form action="/submit">
    ...
</form>
```

Think:

```text
action → Where does the submitted data go?
```

---

## `method`

### Purpose

Specifies the method used to submit the form.

Common methods:

```text
GET
POST
```

Example:

```html
<form
    action="/submit"
    method="post"
>
    ...
</form>
```

---

# 35. GET vs POST

## GET

```html
<form method="GET">
```

During testing, submitted form data appeared in the URL.

Conceptually:

```text
Form
 ↓
GET
 ↓
Data appears in URL
```

---

## POST

```html
<form method="POST">
```

Submitted values are sent in the request body rather than being included in the URL in the same way as GET.

Conceptually:

```text
Form
 ↓
POST
 ↓
Data sent in the request body
```

The practical distinction to remember:

```text
GET  → data visible in URL
POST → data sent in request body
```

---

# 36. `<label>`

### Purpose

Provides a descriptive label for a form control.

```html
<label for="email">Email</label>
```

It tells the user what a form field is for.

---

## Connecting `<label>` to an Input

Use:

```text
label for
input id
```

Example:

```html
<label for="email">Email</label>

<input
    id="email"
    type="email"
>
```

Relationship:

```text
<label for="email">
          ↓
<input id="email">
```

The `for` value must match the input's `id`.

---

# 37. `<input>`

### Purpose

Creates an input control for collecting user data.

`<input>` is a **void element**.

The `type` attribute determines the kind of input.

---

# 38. Input Types

## `text`

Ordinary text input.

```html
<input type="text">
```

---

## `password`

Password input.

```html
<input type="password">
```

---

## `email`

Email input.

```html
<input type="email">
```

The browser performs email-style validation during normal form validation.

---

## `number`

Numeric input.

```html
<input type="number">
```

Can be combined with:

```html
<input
    type="number"
    min="1"
    max="100"
>
```

---

## `search`

Search-oriented input.

```html
<input type="search">
```

---

## `url`

URL input.

```html
<input type="url">
```

---

## `date`

Date input.

```html
<input type="date">
```

---

## `month`

Month/year input.

```html
<input type="month">
```

---

## `time`

Time input.

```html
<input type="time">
```

---

## `file`

Allows the user to select a file.

```html
<input type="file">
```

---

## `color`

Provides a color picker.

```html
<input type="color">
```

---

## `range`

Creates a range slider.

```html
<input type="range">
```

Example:

```html
<input
    type="range"
    min="0"
    max="100"
    step="10"
    value="50"
>
```

---

## `hidden`

Creates an input that is not displayed as a normal visible form control.

```html
<input
    type="hidden"
    name="user_id"
    value="123"
>
```

The value can still be submitted with the form.

A hidden input should not be treated as a security mechanism.

---

## `submit`

Creates a submit control.

```html
<input
    type="submit"
    value="Submit"
>
```

---

## `reset`

Creates a reset control.

```html
<input
    type="reset"
    value="Reset"
>
```

Resets form controls to their initial values/state.

---

## `radio`

### Meaning

`radio` creates a **radio button**.

### Purpose

Radio buttons are used when the user should choose **one option from a group of related options**.

Example:

```html
<input type="radio" name="gender" value="male">
<input type="radio" name="gender" value="female">
```

### Grouping Radio Buttons

Radio buttons are commonly grouped using the same `name` attribute.

```html
<input
    type="radio"
    name="gender"
    value="male"
>

<input
    type="radio"
    name="gender"
    value="female"
>
```

Because both inputs have:

```text
name="gender"
```

they belong to the same group, so the user can select one option from that group.

Mental model:

```text
same name
     ↓
same radio group
     ↓
one option can be selected
```

### `value` with Radio Buttons

The `value` attribute represents the value associated with the selected option when the form is submitted.

Example:

```html
<input
    type="radio"
    name="gender"
    value="male"
>
```

If this option is selected, the submitted data can be represented as:

```text
gender=male
```

### Connecting a Radio Button to a `<label>`

A radio button can be connected to a `<label>` using:

```text
label for
input id
```

Example:

```html
<input
    type="radio"
    id="male"
    name="gender"
    value="male"
>

<label for="male">Male</label>
```

The relationship is:

```text
<label for="male">
          ↓
<input id="male">
```

The value of `for` must match the `id` of the corresponding input.

Clicking the label can then activate/select the associated radio button.

A complete group can look like:

```html
<input
    type="radio"
    id="male"
    name="gender"
    value="male"
>

<label for="male">Male</label>

<input
    type="radio"
    id="female"
    name="gender"
    value="female"
>

<label for="female">Female</label>
```

Here:

```text
id="male"
      ↕
for="male"

id="female"
      ↕
for="female"
```

The `id` values must be unique within the document, while the related radio buttons use the same `name` to form one group.

---

## `checkbox`

### Meaning

`checkbox` creates a **checkbox input**.

### Purpose

Checkboxes are used for options that can be selected **independently**.

Example:

```html
<input type="checkbox">
```

Unlike radio buttons, multiple checkboxes can be selected at the same time.

Example:

```html
<input type="checkbox" name="skill" value="html">
<input type="checkbox" name="skill" value="css">
<input type="checkbox" name="skill" value="git">
```

The user can select:

```text
HTML
CSS
Git
```

at the same time.

### `value` with Checkboxes

The `value` attribute represents the value associated with the checkbox when it is selected and submitted.

Example:

```html
<input
    type="checkbox"
    name="skill"
    value="html"
>
```

If the checkbox is selected, the submitted data can include:

```text
skill=html
```

### Connecting a Checkbox to a `<label>`

A checkbox can be connected to a `<label>` using the same:

```text
label for
input id
```

relationship.

Example:

```html
<input
    type="checkbox"
    id="terms"
    name="terms"
    value="accepted"
>

<label for="terms">
    I accept the terms
</label>
```

Relationship:

```text
<label for="terms">
          ↓
<input id="terms">
```

The `for` value must match the checkbox's `id`.

Clicking the label can then check or uncheck the associated checkbox.

### `checked`

The `checked` attribute can make a checkbox initially selected.

```html
<input
    type="checkbox"
    id="terms"
    name="terms"
    value="accepted"
    checked
>

<label for="terms">
    I accept the terms
</label>
```

`checked` is a **boolean attribute**.

Its presence means the checkbox starts in the checked state.

---

## Radio vs Checkbox

```text
radio
→ used when choosing one option from a group
→ related radio buttons normally share the same name
→ only one option in the group can be selected

checkbox
→ used for independently selectable options
→ multiple checkboxes can be selected
```

### Example

Radio:

```html
<input
    type="radio"
    id="male"
    name="gender"
    value="male"
>

<label for="male">Male</label>

<input
    type="radio"
    id="female"
    name="gender"
    value="female"
>

<label for="female">Female</label>
```

Checkbox:

```html
<input
    type="checkbox"
    id="html"
    name="skill"
    value="html"
>

<label for="html">HTML</label>

<input
    type="checkbox"
    id="css"
    name="skill"
    value="css"
>

<label for="css">CSS</label>
```

Mental model:

```text
Radio
→ choose ONE from a group

Checkbox
→ choose ZERO, ONE, or MORE independently
```

### `for` + `id` Relationship

For both radio buttons and checkboxes:

```text
<label for="...">
        ↓
<input id="...">
```

Example:

```html
<label for="html">HTML</label>

<input
    id="html"
    type="checkbox"
    name="skill"
    value="html"
>
```

The `for` attribute identifies which input the label belongs to, while the input's `id` provides the matching identifier.

---

# 39. Input Attributes

## `name`

### Purpose

Provides the name associated with the form control when its data is submitted.

```html
<input
    type="text"
    name="username"
>
```

The backend can use the name to identify what the submitted value represents.

---

## `value`

### Purpose

Specifies the value associated with an input.

```html
<input
    type="text"
    value="Neamatalla"
>
```

---

## `placeholder`

### Purpose

Displays a temporary hint inside an empty input.

```html
<input
    type="email"
    placeholder="Enter your email"
>
```

A placeholder is a hint about what to enter; it is not the actual submitted value.

---

## `required`

Makes the control required before normal browser form submission.

```html
<input
    type="email"
    required
>
```

The browser's built-in validation can prevent submission if the required field is invalid or empty.

---

## `readonly`

### Meaning

Read only.

### Purpose

Prevents the user from editing the value while keeping the control active.

```html
<input
    type="text"
    value="Neamatalla"
    readonly
>
```

The value is still submitted with the form.

---

## `disabled`

### Purpose

Disables the form control.

```html
<input
    type="text"
    value="Neamatalla"
    disabled
>
```

A disabled form control is not submitted with the form.

---

## `readonly` vs `disabled`

```text
readonly
→ cannot edit
→ value is submitted

disabled
→ disabled/inactive
→ value is not submitted
```

---

## `autofocus`

Requests that the input automatically receive focus when the page loads.

```html
<input
    type="text"
    autofocus
>
```

---

## `maxlength`

Sets the maximum number of characters allowed.

```html
<input
    type="text"
    maxlength="20"
>
```

---

## `minlength`

Sets the minimum number of characters expected/required.

```html
<input
    type="text"
    minlength="5"
>
```

---

## `min`

Sets the minimum permitted value for applicable inputs.

```html
<input
    type="number"
    min="1"
>
```

---

## `max`

Sets the maximum permitted value.

```html
<input
    type="number"
    max="100"
>
```

---

## `step`

Specifies the permitted stepping interval for applicable numeric inputs.

```html
<input
    type="number"
    min="0"
    max="100"
    step="5"
>
```

---

## `checked`

Makes a checkbox or radio input initially selected.

```html
<input
    type="checkbox"
    checked
>
```

---

# 40. `<select>`

Creates a dropdown/select control.

```html
<select name="country">
    ...
</select>
```

---

## `<option>`

Represents an option inside `<select>`.

```html
<select name="country">
    <option value="eg">Egypt</option>
    <option value="sa">Saudi Arabia</option>
</select>
```

An option has:

```text
value        → submitted value
visible text → what the user sees
```

For example:

```html
<option value="eg">Egypt</option>
```

When selected, the submitted data can be:

```text
country=eg
```

---

## `selected`

Makes an option selected by default.

```html
<option selected>Egypt</option>
```

---

## `<optgroup>`

### Meaning

Option Group.

### Purpose

Groups related options inside a `<select>`.

```html
<select name="car">

    <optgroup label="German Cars">
        <option value="bmw">BMW</option>
        <option value="mercedes">Mercedes</option>
    </optgroup>

</select>
```

---

## `multiple`

Allows multiple options to be selected where supported.

```html
<select multiple>
    <option>HTML</option>
    <option>CSS</option>
    <option>Git</option>
</select>
```

---

# 41. `<textarea>`

Creates a multi-line text input.

```html
<textarea>
Write your message here.
</textarea>
```

It is useful for larger amounts of user-entered text.

---

# 42. `<button>`

Creates a clickable button.

```html
<button>Submit</button>
```

Buttons can be used for actions such as submitting forms or triggering interactions.

The HTML element itself creates the button; additional behavior can be provided by other technologies such as JavaScript.

---

# 43. `novalidate`

Used on `<form>`.

```html
<form novalidate>
    ...
</form>
```

### Purpose

Prevents the browser from performing its normal built-in form validation when the form is submitted.

It can be useful during testing.

---

# 44. `target` on Forms

Controls where the result of a form submission opens.

Example:

```html
<form
    action="result.html"
    target="_blank"
>
    ...
</form>
```

### `_blank`

Opens the submission result in a new browsing context, commonly a new tab.

Important:

```text
target="_blank"
→ controls where the submission result opens
```

It does **not** itself preserve form data.

---

# 45. `<datalist>`

### Purpose

Provides predefined suggestions for an input while still allowing the user to type a custom value.

Example:

```html
<input list="languages">

<datalist id="languages">
    <option value="HTML">
    <option value="CSS">
    <option value="Python">
</datalist>
```

The connection is:

```text
<input list="languages">
          ↓
<datalist id="languages">
```

The input's `list` attribute must match the `<datalist>`'s `id`.

---

## `<select>` vs `<datalist>`

```text
<select>
→ user selects from available options

<datalist>
→ provides suggestions
→ user can still type another value
```

---

# 46. `<q>`

### Purpose

Represents a short inline quotation.

```html
<p>
    She said <q>Keep learning.</q>
</p>
```

The browser may display quotation marks around the content.

---

# 47. `<blockquote>`

### Purpose

Represents a longer or standalone quotation.

```html
<blockquote>
    Learning never stops.
</blockquote>
```

Difference:

```text
<q>
→ short inline quotation

<blockquote>
→ longer/standalone quotation
```

---

# 48. `<code>`

### Purpose

Represents a short piece of computer code.

```html
<p>
    Use <code>&lt;p&gt;</code> for a paragraph.
</p>
```

---

# 49. `<pre>`

### Meaning

`pre` stands for **preformatted text**.

### Purpose

Preserves whitespace and line breaks in the displayed text.

```html
<pre>
Line 1
    Line 2
        Line 3
</pre>
```

The browser preserves the written spacing and line structure.

---

# 50. `<wbr>`

### Meaning

**WBR = Word Break Opportunity**

### Purpose

Provides a possible line-break position inside a long word or string.

```html
<p>
    verylongword<wbr>example
</p>
```

Important:

```text
<wbr>
→ possible line break

<br>
→ actual line break
```

`<wbr>` does not force a line break.

---

# 51. `<bdi>`

### Meaning

**BDI = Bidirectional Isolation**

### Purpose

Isolates the direction of text from the surrounding bidirectional text.

This is useful when text may contain languages with different writing directions.

Example:

```html
<p>
    User: <bdi>اسم المستخدم</bdi>
</p>
```

The isolated content can have a different text direction without interfering with the surrounding text.

---

# 52. `<iframe>`

### Meaning

**IFRAME = Inline Frame**

### Purpose

Embeds another document or external content inside the current page.

Example:

```html
<iframe src="https://example.com"></iframe>
```

---

# 53. Accessibility

Accessibility means making web content usable by as many people as possible, including people who use assistive technologies such as **Screen Readers**.

Important HTML accessibility concepts include:

```text
lang
Screen Readers
ARIA
role
aria-label
aria-labelledby
aria-hidden
aria-checked
tabindex
```

---

# 54. `lang`

### Meaning

`lang` specifies the **language** of the document or an element.

Example:

```html
<html lang="en">
```

This tells browsers and assistive technologies what language the content uses.

It may not create a visible change, but it can affect how assistive technologies interpret and pronounce content.

For example:

```html
<html lang="en">
```

indicates English.

---

# 55. Screen Readers

A **Screen Reader** is assistive software that interprets webpage content and communicates information to the user.

It can communicate information such as:

* text
* headings
* buttons
* form fields
* element states
* interactive elements

Conceptually:

```text
Webpage
   ↓
Screen Reader
   ↓
Information communicated to user
```

---

# 56. ARIA

### Meaning

**ARIA = Accessible Rich Internet Applications**

ARIA provides additional accessibility information to assistive technologies.

ARIA attributes commonly begin with:

```text
aria-
```

ARIA is especially useful when custom elements need accessibility information that native HTML does not already provide.

---

## Native HTML vs ARIA

When native HTML already provides the required semantics, prefer the native element.

For example:

```html
<button>Submit</button>
```

is preferable to unnecessarily creating:

```html
<div role="button">
    Submit
</div>
```

Native HTML already provides the appropriate button semantics.

---

# 57. `role`

### Purpose

Defines the semantic role that an element should communicate to assistive technologies.

Example:

```html
<div role="checkbox">
    Accept
</div>
```

Here:

```text
role="checkbox"
→ the element is communicated as a checkbox
```

This is useful for custom interactive elements.

---

# 58. `aria-checked`

### Purpose

Communicates the checked state of an ARIA checkbox.

```html
<div
    role="checkbox"
    aria-checked="true"
>
    Accept
</div>
```

The values include:

```text
true  → checked
false → not checked
```

---

# 59. `tabindex`

### Purpose

Controls whether an element can receive keyboard focus and participate in keyboard navigation.

Example:

```html
<div
    role="checkbox"
    tabindex="0"
>
    Accept
</div>
```

`tabindex="0"` allows the element to participate in normal Tab navigation.

---

# 60. `aria-labelledby`

### Purpose

Associates an element with another element that provides its accessible name.

Example:

```html
<h2 id="profile-title">Profile</h2>

<section aria-labelledby="profile-title">
    ...
</section>
```

Relationship:

```text
aria-labelledby="profile-title"
              ↓
       id="profile-title"
```

---

# 61. `aria-label`

### Purpose

Provides an accessible name directly.

Example:

```html
<button aria-label="Close">
    X
</button>
```

The visible content is:

```text
X
```

while the accessible name can be:

```text
Close
```

---

# 62. `aria-hidden`

### Purpose

Indicates that an element should be hidden from the accessibility tree.

Example:

```html
<span aria-hidden="true">★</span>
```

This can be useful for decorative content that does not need to be announced.

---

# 63. Custom ARIA Checkbox Example

A custom checkbox can combine several accessibility concepts:

```html
<div
    role="checkbox"
    aria-checked="true"
    tabindex="0"
    aria-labelledby="plan1"
>
    Plan One
</div>

<label id="plan1">
    Plan One
</label>
```

Meaning:

```text
role="checkbox"
→ communicates the checkbox role

aria-checked="true"
→ communicates the checked state

tabindex="0"
→ allows keyboard focus

aria-labelledby="plan1"
→ obtains the accessible name from id="plan1"
```

A native checkbox already provides much of this semantic information:

```html
<label for="plan1">Plan One</label>

<input
    id="plan1"
    type="checkbox"
    checked
>
```

Therefore, ARIA should not be used simply to recreate semantics that native HTML already provides.

---

# 64. Semantic HTML and Accessibility

Semantic HTML and accessibility are closely related.

Using meaningful elements such as:

```html
<button>
<nav>
<main>
<header>
<footer>
```

gives browsers and assistive technologies useful information about the structure and purpose of content.

A good general principle is:

```text
Use the correct native HTML element first.
Add ARIA when additional accessibility information is actually needed.
```

---

# 65. Browser Tools

## View Page Source

**View Page Source** displays the HTML source of a webpage.

It is useful for examining the original/source HTML document.

---

## Inspect / Developer Tools

**Inspect** opens the browser's developer tools and allows you to examine the current document and its elements.

It is useful for:

* examining HTML structure;
* inspecting elements;
* seeing how the browser represents the document;
* testing and debugging webpages.

---

## View Page Source vs Inspect

```text
View Page Source
→ shows the page's source HTML

Inspect
→ shows the document as represented in the browser's developer tools
```

---


# 66. Important Conceptual Differences

## `<title>` vs `<caption>`

```text
<title>
→ document/page title

<caption>
→ table caption
```

---

## `<strong>` vs `<b>`

```text
<strong>
→ strong importance

<b>
→ attention/distinction
```

---

## `<s>` vs `<del>`

```text
<s>
→ no longer accurate/relevant/current

<del>
→ deleted content
```

---

## `<i>` vs `<em>`

```text
<i>
→ distinct text

<em>
→ emphasis
```

---

## `<q>` vs `<blockquote>`

```text
<q>
→ short inline quotation

<blockquote>
→ longer/standalone quotation
```

---

## `<span>` vs `<div>`

```text
<span>
→ inline container

<div>
→ block-level container
```

---

## `<p>` vs `<br>`

```text
<p>
→ paragraph

<br>
→ line break
```

---

## `<wbr>` vs `<br>`

```text
<wbr>
→ possible line-break opportunity

<br>
→ actual line break
```

---

## `<ul>` vs `<ol>`

```text
<ul>
→ unordered list

<ol>
→ ordered list
```

---

## `<th>` vs `<td>`

```text
<th>
→ table header

<td>
→ table data
```

---

## `<select>` vs `<datalist>`

```text
<select>
→ choose from available options

<datalist>
→ suggestions while allowing custom input
```

---

## `readonly` vs `disabled`

```text
readonly
→ cannot edit
→ value is submitted

disabled
→ disabled/inactive
→ value is not submitted
```

---

## GET vs POST

```text
GET
→ submitted data appears in the URL

POST
→ submitted data is sent in the request body
```

---

## Native Checkbox vs ARIA Checkbox

```text
Native checkbox
→ native checkbox semantics

Custom ARIA checkbox
→ requires additional semantic/accessibility information
```

---

## Radio vs Checkbox

```text
radio
→ choose one option from a group
→ related radio buttons normally share the same name

checkbox
→ independently selectable option
→ multiple checkboxes can be selected
```

---

## `label` + `for` vs `input` + `id`

```text
<label for="email">
          ↓
<input id="email">
```

The `for` attribute connects the label to the input whose `id` has the same value.

This relationship can be used with different input controls, including:

```html
<input type="radio">
<input type="checkbox">
<input type="text">
<input type="email">
```

Example:

```html
<label for="email">Email</label>

<input
    id="email"
    type="email"
    name="email"
>
```

The important relationship is:

```text
for="email"
     ↕
id="email"
```

# 67. Useful Resources

## HTML Reference

[HTML Reference — htmlreference.io](https://htmlreference.io/)

A quick reference for HTML elements and their usage.

## MDN HTML Reference

[MDN — HTML Reference](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference)

A detailed reference for HTML elements, attributes, and browser behavior.

## HTML Symbols Reference

[Toptal — HTML Symbols Reference](https://www.toptal.com/designers/htmlarrows/symbols/)

Useful for looking up HTML symbols and special characters.

## HTML Entities

[Complete List of HTML Entities — Scribd](https://www.scribd.com/document/711944543/Complete-list-of-HTML-entities-FreeFormatter-com)

Reference for HTML entities and their corresponding characters.

---
 
