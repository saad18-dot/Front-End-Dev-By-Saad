# 01 — HTML5

Notes, exercises, and small practice snippets from learning HTML5 — semantic structure, forms, accessibility basics, and document fundamentals.

## Contents
- `notes.md` — my own summary notes, written in my own words )
- `exercises/` — small practice files 

## What I learned here
# HTML Complete Course Notes
*(Based on _"Apna College", "Free CodeCamp" and "MDN WEB DOCS"_ HTML Tutorial — I build this Notes to enhance my Skills*

---

## LEVEL 1: Basics of HTML

### What is HTML?
HTML (HyperText Markup Language) is a **markup language** — it defines the **structure and layout** of a webpage: what goes where (like a house blueprint — which room is where, what's inside each room).

### The Three Parts of Front-End Development
| Part | Role | Analogy |
|---|---|---|
| **HTML** | Structure/layout of the page | The rooms of a house |
| **CSS** | Styling — colors, sizes, shapes, fonts | Wall paint, furniture style |
| **JavaScript** | Functionality/logic (interactivity) | Switches that actually turn the fan/light on |

### Tools Needed
- **Text/Code Editors**: Notepad (basic), UltraEdit (professional, paid, 30-day trial, has FTP/SFTP integration, code highlighting), **VS Code** (free, by Microsoft — used throughout this course).
- **VS Code Setup**: Download from the official site → choose 32-bit/64-bit based on your system → install.
- **Live Server extension**: Lets you see changes in the browser instantly without manually refreshing.
- **Emmet**: A built-in VS Code toolkit — typing `!` and pressing the abbreviation option auto-generates the full HTML boilerplate code.

### Viewing Any Website's HTML
- **Right-click → View Page Source**: Shows the raw HTML code of a page.
- **Right-click → Inspect**: Shows a cleaner, structured view, and lets you see which HTML element occupies which portion of the page visually.
- Note: You can copy some HTML but can't fully recreate a site this way — websites also have back-end logic, not just front-end.

### Creating Your First File
- File name convention: **`index.html`** — servers treat this as the default/home page automatically. If you don't create `index.html`, you must manually tell the server which file is the home page.
- HTML is **not case-sensitive**: `<head>`, `<HEAD>`, `<Head>` are all treated the same (unlike case-sensitive languages like C, C++, Python, Java).

### HTML Tags — The Basics
- A **tag** is a **container** — like a box in your kitchen holding some content (sugar, salt, etc.).
- Format: `<p>content</p>`
  - `<p>` = **opening tag**
  - `</p>` = **closing tag** (has a `/`)
  - Together with the content in between = one **element**.
- VS Code auto-closes tags when you type the opening tag.
- Some tags have **no content and no closing tag** — called **empty tags**, e.g., `<br>` (line break).

### The Boilerplate Code Structure
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My First Page</title>
</head>
<body>
    <!-- visible content goes here -->
</body>
</html>
```
- `<!DOCTYPE html>` — declares this document uses HTML5.
- `<html>` — the **root element** of the document; everything else lives inside it.
- `<head>` — contains **meta information** (data about data) that is *not displayed* on the page but is useful to the browser/search engines (e.g., page title, viewport settings for responsiveness).
  - **Viewport meta tag**: Makes the website **responsive** — looks good on phones, tablets, and large screens alike.
- `<title>` — sets the tab title of the page.
- `<body>` — contains everything that **is displayed** on the actual webpage.

### Relationship Terms
- `<head>` and `<body>` are both **children** of `<html>` (their **parent**).
- `<head>` and `<body>` are **siblings** of each other.

### Comments in HTML
- Format: `<!-- your comment here -->`
- Comments are **not rendered/parsed** by the browser — they're only visible in the code, useful for explaining code to yourself or teammates.

### MDN Reference
- Ctrl+click on any tag name in VS Code opens the **MDN (Mozilla Developer Network)** documentation — a great free resource with browser compatibility info, examples, and usage details for every tag.

### 🔧 Project 1 (Part 1)
Create a folder called `portfolio`. Inside it, create `index.html` with boilerplate code, and simply print "Hello World" or "Portfolio".

---

## LEVEL 2: HTML Tags in Detail

### Attributes
- **Attributes add extra information to a tag.**
- Format: `attributeName="value"` (written inside the opening tag)
- Example: `<html lang="en">` — the `lang` attribute specifies the document's language.
- Values can be in **single or double quotes** — both valid; double quotes are the convention used in this course.

### Heading Tags — `<h1>` to `<h6>`
- `<h1>` = largest/most important, `<h6>` = smallest/least important.
- **Important rule**: Headings indicate **importance/hierarchy for SEO**, NOT just visual size. Don't use `<h1>` just because you want big text, or `<h6>` just because you want small text — use CSS `font-size` for that instead.
- Search engines use heading hierarchy to understand which content is more important when ranking pages.

### Paragraph Tag — `<p>`
- Adds paragraphs of text.
- **Word Wrap tip**: If a long paragraph causes horizontal scrolling in your editor, use Command Palette → "Toggle Word Wrap" to make it wrap within the visible area (purely a code-editor display feature, doesn't affect actual output).

### Anchor Tag — `<a>`
- Used to **add links to pages**.
- Syntax: `<a href="URL">Display Text</a>`
- **Absolute link**: Full link to another website (e.g., `https://google.com`) — points to an external site.
- **Relative link**: Points to another page **within your own website/project folder** (e.g., `hello.html`, or `folder/page.html`) — points to a local file relative to the current file's location.

### Image Tag — `<img>`
- Used to **add images to your page**.
- Syntax: `<img src="link" alt="description">`
- `src` — the image source; can be an absolute URL (from internet) or relative URL (local file).
- `alt` — alternative text shown if the image fails to load (also improves accessibility for screen readers).
- `height` and `width` attributes can resize the image — **but it's advisable to set only ONE of them at a time** (not both), otherwise the image's aspect ratio gets distorted. Ideally, size/dimension styling should be done via **CSS**, not HTML attributes.

### Line Break Tag — `<br>`
- Adds a line break / moves content to the next line.
- It's an **empty tag** — no content, no closing tag needed.

### Text Formatting Tags
| Tag | Effect |
|---|---|
| `<b>` | **Bold** text |
| `<i>` | *Italic* text |
| `<u>` | <u>Underline</u> text |
| `<big>` | Bigger font text |
| `<small>` | Smaller font text |

- Tags can be **nested** inside other tags — e.g., you can underline just one word inside a paragraph by wrapping only that word in `<u>...</u>` within the `<p>` tag.

### Horizontal Rule — `<hr>`
- Used to **visually separate content/sections** with a horizontal line and spacing.
- "Ruler" = scale; it divides the page into distinct visual sections.

### Subscript and Superscript
- `<sub>` — subscript (text appears slightly below the line) — used for chemical formulas: `H<sub>2</sub>O`
- `<sup>` — superscript (text appears slightly above the line) — used for math: `3<sup>2</sup> = 9`

### Preformatted Text — `<pre>`
- Displays text **exactly as written**, preserving all spaces and line breaks.
- By default, HTML **ignores** extra spaces and line breaks in regular text (e.g., inside `<p>`) — everything collapses to a single line/normal spacing.
- Use `<pre>` when you need to preserve exact formatting (e.g., code snippets, ASCII art).

### 🔧 Project 1 (Part 2)
Create 3 pages for your portfolio: Education, Experience, and Projects — link them all from the home page using anchor tags. Use proper headings, paragraphs, and formatting tags (sub/sup for percentages or CGPA, etc.).

---

## LEVEL 3: Page Layouts in HTML

### Semantic vs Non-Semantic Tags
- **Semantic tags**: Their name clearly indicates their purpose/content — e.g., `<header>`, `<footer>`, `<main>`, `<section>`, `<article>`, `<aside>`.
- **Non-semantic tags**: Name doesn't reveal what's inside — e.g., `<div>`, `<span>`.

**Benefits of using semantic tags:**
1. Code is more **readable and structured**.
2. Better **SEO** — improves search engine rankings.
3. Better **user experience**, including for accessibility tools/screen readers.

### Core Layout Tags

**`<header>`** — Contains the top section of the page (e.g., navigation menu, logo, main title).

**`<footer>`** — Contains the bottom section (e.g., contact info, copyright).

**`<main>`** — Contains the primary/central content of the page. Inside `<main>`, three major sub-tags are commonly used:

1. **`<section>`** — Divides the page into distinct thematic sections (e.g., an Education section, an Experience section).
2. **`<article>`** — Represents a self-contained, complete piece of content (e.g., "My Story," a blog post, a bio).
3. **`<aside>`** — Represents content **not part of the main content** — e.g., advertisements, sidebars, related-but-secondary info. Search engines/SEO don't weight this as main content.

### `<div>` — Generic Container
- A **container for other HTML elements** with **no special semantic meaning** of its own (hence "non-semantic").
- Its main job: **group/contain** other elements together so you can style or manipulate them collectively.
- **Default height is 0** when empty; expands to fit content once something is placed inside.
- `<div>` is a **block-level element** — it takes up the **full width** of its parent container, regardless of how much space the content actually needs.

### `<span>` — Inline Container
- Similar to `<div>` (also a generic container) but used differently.
- `<span>` is an **inline element** — it only takes up **as much width as its content needs**, not the full line.

### Block vs Inline Elements
| Block Elements (full width) | Inline Elements (only needed width) |
|---|---|
| `<div>`, `<header>`, `<footer>`, `<section>`, `<article>`, `<p>`, headings | `<span>`, `<a>`, `<img>`, `<br>`, `<b>`, `<i>`, `<sub>`, `<sup>` |

Use **Inspect Element** in the browser to visually confirm how much horizontal space any element occupies.

### 🔧 Project 1 (Part 3)
Add an image to your homepage (make it clickable, e.g., linking to your GitHub). Divide your `<main>` section into multiple `<section>` elements for better structure.

---

## LEVEL 4 (PRO LEVEL): Lists, Tables, and Forms

### Lists

**Unordered List** — bullet points, no specific sequence:
```html
<ul>
  <li>Apple</li>
  <li>Mango</li>
  <li>Litchi</li>
</ul>
```
- `<ul>` = **U**nordered **L**ist, `<li>` = **L**ist **I**tem
- Bullet shape (circle, square, disc, triangle) can be changed via CSS.

**Ordered List** — numbered/lettered sequence:
```html
<ol>
  <li>Apple</li>
  <li>Mango</li>
  <li>Litchi</li>
</ol>
```
- `<ol>` = **O**rdered **L**ist — items appear numbered (1, 2, 3...) or can be set to letters (a, b, c) or Roman numerals via attributes.

**Nested Lists**: You can place a `<ul>` or `<ol>` inside an `<li>` to create a sub-list (e.g., under "Apple" → Color: Red, Season: Winter).

### Tables

Three main tags:
| Tag | Purpose |
|---|---|
| `<tr>` | **T**able **R**ow — creates a row |
| `<td>` | **T**able **D**ata — holds the actual data in a cell |
| `<th>` | **T**able **H**eader — holds the header/column-title cell (bold, centered by default) |

```html
<table>
  <caption>Student Data</caption>
  <thead>
    <tr>
      <th>Name</th>
      <th>Roll Number</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Shraddha</td>
      <td>101</td>
    </tr>
  </tbody>
</table>
```
- **`<caption>`** — describes what the table is about (like a photo caption).
- **`<thead>`** — wraps the header row(s).
- **`<tbody>`** — wraps the actual data rows.
- **`colspan`** attribute (used on `<th>` or `<td>`) — makes a cell span across multiple columns (e.g., `<th colspan="2">Information</th>` merges two columns under one header, similar to merging cells in Excel).

### Forms

Forms **collect data from users** (login forms, sign-up forms, feedback forms, contact forms).

```html
<form action="action.php">
  ...form elements...
</form>
```
- `action` attribute — specifies where the submitted form data is sent (typically a back-end file like PHP, or a JS handler). Not required to understand deeply while just learning form *design*.

#### Input Types
```html
<input type="text" placeholder="Type something here">
<input type="password" placeholder="Enter password">
<input type="radio" name="class" value="11th" id="r1">
<input type="checkbox" name="subject" value="Math" id="c1">
```
- `type="text"` — plain visible text input.
- `type="password"` — input is masked with dots (hidden from view).
- `placeholder` — greyed-out hint text shown when the field is empty.

#### Radio Buttons
- Used when the user can select **only one option** from a group (e.g., choosing a class: 11th or 12th).
- Give all related radio buttons the **same `name`** attribute — this groups them so selecting one deselects the others.
- Each radio button needs a **different `id`**.
- The **`value`** attribute is what's actually sent to the back-end (not necessarily what's displayed to the user) — always keep the displayed label and value in sync to avoid confusion.

#### Checkboxes
- Used when the user can select **multiple options** (e.g., choosing favorite subjects).
- Structured similarly to radio buttons but allow multi-selection.

#### Labels
```html
<label for="r1">Class 11th</label>
<input type="radio" name="class" value="11th" id="r1">
```
- `<label>` connects descriptive text to a form input using the `for` attribute (which must match the input's `id`).
- **Two key benefits of labels:**
  1. **Accessibility** — screen readers announce the label so visually impaired users know what each field/button is for.
  2. **Usability** — clicking the *label text* (not just the tiny radio/checkbox itself) also selects the option, which is very helpful for users with limited vision or motor precision.

#### Class vs ID
- **`id`** — a **unique identifier** for a single element (like a student's roll number — one specific person).
- **`class`** — a **group identifier** shared across multiple elements (like a "House" in school — Green House, Red House, etc.), used to apply the same style/behavior to many elements at once.
- An element can have both a `class` and an `id` simultaneously.

#### Textarea
```html
<textarea name="feedback" id="101" placeholder="Please give your valuable feedback" rows="5" cols="30"></textarea>
```
- Provides a **multi-line text input box** — commonly used for feedback/comments.
- `rows` and `cols` control its visible size.

#### Select (Dropdown)
```html
<select name="city">
  <option>Delhi</option>
  <option>Bangalore</option>
  <option>Pune</option>
</select>
```
- Creates a **dropdown menu** of options (e.g., selecting a city or state).

#### Submit Button
```html
<input type="submit" value="Submit">
```
- Submits all the form data (to whatever the `action` attribute points to).

### 🔧 Project 1 (Part 4)
Add a "Contact Me" form to your portfolio (name, email, message/query).

### 🔧 Project 2 (Bonus Idea)
Build a resource website for college students: a sign-up form, links/`<iframe>`s to coding videos, and a table listing topics covered on the homepage.

---

## Bonus Tags

### `<iframe>` — Embed Another Website/Video Inside Yours
```html
<iframe src="https://en.wikipedia.org/wiki/HTML" width="600" height="400"></iframe>
```
- Displays another website or a video (e.g., an embedded YouTube video) inside your own page.
- Some websites (e.g., Google, MDN) **block being embedded** this way for security reasons (to prevent phishing-style attacks where someone mimics a trusted site). Others (like Wikipedia) allow it since their content is freely available.

### `<video>` — Embed a Video File
```html
<video src="myvideo.mp4" width="400" height="300" controls loop></video>
```
- `src` — path to the video file (relative or absolute).
- `controls` — shows play/pause/volume/fullscreen controls (without this, the video can't be played by the user).
- `loop` — video automatically restarts after finishing.
- `autoplay` — starts playing automatically on page load. **Generally not recommended** because:
  1. It can waste a user's mobile data/bandwidth.
  2. It can create a poor/annoying user experience (unexpected sound, etc.).
  - If you must autoplay, mute the sound (common practice for ads).

---

## What's Next?
After mastering HTML, the natural next steps are:
1. **CSS** (Cascading Style Sheets) — styling: colors, sizes, layout, fonts.
2. **JavaScript** — functionality/interactivity.
3. **Back-end development** — handling form data, databases, etc.


## Resources I used
- MDN Web Docs — https://developer.mozilla.org/en-US/docs/Learn
- freeCodeCamp — HTML Crash Course
- Apna College — https://www.youtube.com/watch?v=HcOc7P5BMi4&list=PLfqMhTWNBTe0PY9xunOzsP5kmYIz2Hu7i (Html Crash Course)

> Finished projects using HTML go in `/projects`, not here. This folder is for learning material only.
