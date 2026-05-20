<script type="text/javascript" src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML"></script>
<script type="text/x-mathjax-config">
  MathJax.Hub.Config({ tex2jax: {inlineMath: [['$', '$']]}, messageStyle: "none" });
</script>

# Lab 01 — HTML Foundations

## Overview

In this lab you will write your first HTML pages from scratch. By the end of the session you should have a valid, multi-page personal bio site hosted on your own machine and ready to upload to the module web server.

There is no CSS in this lab — focus entirely on **structure and semantics**. Presentation comes next week.

---

## Setting Up

### Tools you will need

You will be writing HTML as plain text. Use whichever code editor you prefer:

- **VS Code** — recommended. Available from [code.visualstudio.com](https://code.visualstudio.com) or via AppsAnywhere.
- **Notepad++** — lightweight alternative on Windows.
- Do **not** use Microsoft Word or any word processor — these add hidden formatting that breaks HTML.

### Create your project folder

1. Create a new folder somewhere on your computer — name it `com4012` or similar.
2. Inside it, create a subfolder called `lab01`.
3. All files for this lab go inside `lab01`.

### View your pages in a browser

1. Open your HTML file in a browser by dragging it into the browser window, or right-clicking the file and selecting **Open with > your browser**.
2. Each time you save changes in your editor, refresh the browser (`F5` or `Ctrl+R`) to see the result.

---

## Part 1 — The HTML Skeleton

Every valid HTML5 page starts with the same basic structure.

### Exercise 1.1 — Create your first page

1. In your `lab01` folder, create a new file called `index.html`.
2. Type (don't copy-paste) the following skeleton exactly:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Your Name — Home</title>
  </head>
  <body>

    <h1>Your Name</h1>
    <p>Welcome to my personal page.</p>

  </body>
</html>
```

3. Replace `Your Name` with your actual name in both places.
4. Save the file and open it in your browser.

You should see your name as a large heading and the welcome text below it.

### What each part does

- `<!DOCTYPE html>` — tells the browser this is an HTML5 document. Always the first line.
- `<html lang="en">` — the root element. `lang="en"` tells screen readers the language.
- `<head>` — contains metadata about the page. Nothing here is visible to the user.
- `<meta charset="UTF-8">` — sets the character encoding. Required for special characters to display correctly.
- `<meta name="viewport" ...>` — makes the page behave correctly on mobile screens.
- `<title>` — the text shown in the browser tab and bookmarks.
- `<body>` — everything visible to the user goes here.

---

## Part 2 — Common HTML Elements

### Exercise 2.1 — Headings and paragraphs

HTML has six levels of heading, `<h1>` through `<h6>`. Use them to create a logical outline — `<h1>` is the page title, `<h2>` for major sections, `<h3>` for subsections, and so on.

Add the following to your `<body>`, replacing the placeholder content:

```html
<h1>Your Name</h1>

<h2>About Me</h2>
<p>Write two or three sentences about yourself here.</p>
<p>Add a second paragraph with something else about you.</p>

<h2>My Studies</h2>
<p>Describe your course and what you are studying.</p>

<h2>Hobbies and Interests</h2>
<p>Write about your interests here.</p>
```

Save and refresh your browser. Notice how the browser applies default sizes to each heading level automatically.

### Exercise 2.2 — Lists

HTML supports ordered lists (`<ol>`) and unordered lists (`<ul>`). Each item is wrapped in `<li>`.

Add a list of your interests inside your Hobbies section:

```html
<h2>Hobbies and Interests</h2>
<p>Some things I enjoy:</p>

<ul>
  <li>Interest one</li>
  <li>Interest two</li>
  <li>Interest three</li>
</ul>
```

Try changing `<ul>` to `<ol>` and observe the difference.

### Exercise 2.3 — Inline text elements

Add emphasis and importance to text using inline elements:

```html
<p>
  My name is <strong>Your Name</strong> and I am studying
  <em>Computing</em> at York St John University.
</p>
```

- `<strong>` — important text (typically bold)
- `<em>` — emphasised text (typically italic)

---

## Part 3 — Links and Images

### Exercise 3.1 — Hyperlinks

The `<a>` element creates a hyperlink. The `href` attribute specifies the destination.

Add a link to an external site:

```html
<h2>Useful Links</h2>
<ul>
  <li><a href="https://developer.mozilla.org">MDN Web Docs</a></li>
  <li><a href="https://www.w3schools.com">W3Schools</a></li>
</ul>
```

To open a link in a new tab, add `target="_blank"` and `rel="noopener noreferrer"`:

```html
<a href="https://developer.mozilla.org" target="_blank" rel="noopener noreferrer">
  MDN Web Docs (opens in new tab)
</a>
```

### Exercise 3.2 — Images

The `<img>` element is a **void element** — it has no closing tag.

1. Find any image file (a photo of yourself, or any image you have saved) and copy it into your `lab01` folder. Rename it `photo.jpg`.
2. Add the image to your page:

```html
<img src="photo.jpg" alt="A photo of Your Name" width="200">
```

Key attributes:
- `src` — the path to the image file
- `alt` — a text description (required — used by screen readers and if the image fails to load)
- `width` — optional display width in pixels

**Never omit the `alt` attribute.** An empty `alt=""` is acceptable for purely decorative images, but a meaningful description is always better.

---

## Part 4 — Semantic Structure

HTML5 introduced **semantic elements** that describe the role of content, not just its appearance. Use these instead of generic `<div>` elements wherever possible.

### Exercise 4.1 — Restructure your page with semantic elements

Reorganise your `index.html` to use semantic structure:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Your Name — Home</title>
  </head>
  <body>

    <header>
      <h1>Your Name</h1>
      <p>Computing Student, York St John University</p>
    </header>

    <nav>
      <a href="index.html">Home</a>
      <a href="skills.html">Skills</a>
      <a href="about.html">About</a>
    </nav>

    <main>
      <article>
        <h2>About Me</h2>
        <p>Write your bio here.</p>
        <img src="photo.jpg" alt="A photo of Your Name" width="200">
      </article>

      <aside>
        <h2>Interests</h2>
        <ul>
          <li>Interest one</li>
          <li>Interest two</li>
          <li>Interest three</li>
        </ul>
      </aside>
    </main>

    <footer>
      <p>Contact: <a href="mailto:youremail@example.com">youremail@example.com</a></p>
    </footer>

  </body>
</html>
```

The semantic elements and their roles:

| Element | Purpose |
|---------|---------|
| `<header>` | Site or section header — logo, title, tagline |
| `<nav>` | Navigation links |
| `<main>` | The primary content of the page |
| `<article>` | Self-contained content that could stand alone |
| `<aside>` | Supplementary content related to the main content |
| `<footer>` | Footer — contact info, copyright, credits |

---

## Part 5 — Multiple Pages

### Exercise 5.1 — Create a second page

1. Create a new file in your `lab01` folder called `skills.html`.
2. Give it the same skeleton structure as `index.html`.
3. Change the `<title>` to `Your Name — Skills`.
4. Add a heading `<h2>Technical Skills</h2>` and an unordered list of computing skills you have or are developing.
5. Copy the `<nav>` block from `index.html` into this page so users can navigate between pages.

### Exercise 5.2 — Create a third page

1. Create `about.html` with the same skeleton and nav.
2. Add a heading `<h2>About This Site</h2>` and a short paragraph explaining what the site is.

### Exercise 5.3 — Test your navigation

1. Open `index.html` in your browser.
2. Click each link in the nav bar — you should move between all three pages.
3. Confirm that the nav links work correctly on all three pages.

---

## Part 6 — Validation

HTML validation checks your code against the W3C standard and catches errors you might not notice visually.

### Exercise 6.1 — Validate your HTML

1. Go to [validator.w3.org](https://validator.w3.org).
2. Choose the **File Upload** tab.
3. Upload your `index.html`.
4. Read the results. Fix any errors shown and re-validate until you have zero errors.
5. Repeat for `skills.html` and `about.html`.

Common errors to look out for:
- Missing `alt` attribute on `<img>`
- Missing `lang` attribute on `<html>`
- Unclosed tags
- Incorrectly nested elements

---

## Extension Tasks

If you finish the main exercises with time to spare:

1. **Bookmark anchors** — add an `id` attribute to one of your headings (e.g. `<h2 id="skills">`) and create a link that jumps directly to it: `<a href="#skills">Jump to Skills</a>`.

2. **Browser DevTools** — open Chrome or Firefox DevTools (`F12`) and use the Elements panel to inspect the DOM of your page. Try editing an element directly in the DevTools panel and see the live effect.

3. **Inspect a real site** — visit any website you use regularly and inspect its HTML structure. Can you identify the `<header>`, `<nav>`, `<main>`, and `<footer>`? Are semantic elements being used, or is it mostly `<div>`?

---

## Checklist

Before you finish, check that your site has:

- [ ] Valid HTML5 skeleton on all pages (`DOCTYPE`, `html`, `head`, `body`)
- [ ] `lang` attribute on `<html>` element
- [ ] Meaningful `<title>` on every page
- [ ] `<header>`, `<nav>`, `<main>`, and `<footer>` used appropriately
- [ ] At least one image with a descriptive `alt` attribute
- [ ] At least one `<article>` and one `<aside>`
- [ ] Navigation links working between all three pages
- [ ] Zero validation errors at validator.w3.org
