---
marp: true
math: mathjax
title: COM4012M 01 - How the Web Works & HTML Foundations
theme: beam
paginate: true
header: 'COM4012M - Programming for the Web'
footer: 'Dr Andy Guest, York St John University'
---

<!-- _class: title -->
## COM4012M - Programming for the Web

# Lecture 01 - How the Web Works
# & HTML Foundations
# Dr Andy Guest

---

## Lecture Overview

<div class="columns"><div>

• The Internet vs the Web  
• Clients and servers  
• HTTP request/response cycle  
• URLs and how they resolve  
• What a browser actually does  

</div><div>

• HTML document structure  
• Semantic elements  
• From Python to HTML  
• Declarative vs procedural thinking  
• Lab: personal bio page  

</div></div>

---

<!-- _class: title -->
## How the Web Works

# The Internet & the Web

---

## The Internet vs the Web

These are not the same thing.

<div class="columns"><div>

**The Internet**

A global network of interconnected computers communicating via standardised protocols (TCP/IP).

Exists since the 1960s (ARPANET).

Carries many services:

• Email (SMTP)  
• File transfer (FTP)  
• The Web (HTTP/HTTPS)  

</div><div>

**The Web (World Wide Web)**

A system of interlinked documents and resources accessible over the Internet.

Invented by Tim Berners-Lee, 1989.

Built on three core technologies:

• HTML — structure  
• HTTP — transfer protocol  
• URLs — addressing  

</div></div>

---

## Clients and Servers

<div class="columns"><div>

**Client**

A device or application that *requests* resources.

Examples:

• Web browser (Chrome, Firefox)  
• Mobile app  
• `curl` on the command line  

The client initiates every communication.

</div><div>

**Server**

A computer that *responds* to requests by serving resources.

Examples:

• Apache / Nginx web servers  
• Node.js application server  
• PHP server  

Servers listen; clients speak first.

</div></div>

---

## The HTTP Request/Response Cycle

Every web page load follows this pattern:

<div class="columns"><div>

1. User enters URL in browser  
2. Browser resolves domain via DNS  
3. Browser sends **HTTP Request** to server  
4. Server processes request  
5. Server sends **HTTP Response**  
6. Browser renders received content  

This cycle repeats for every resource:  
HTML, CSS, images, scripts.

</div><div>

**HTTP Request contains:**

• Method (`GET`, `POST`, `PUT`, `DELETE`)  
• URL / path  
• Headers (browser info, accepted formats)  
• Optional body (for `POST`)  

**HTTP Response contains:**

• Status code (`200`, `404`, `500`...)  
• Headers (content type, caching...)  
• Body (the HTML, image, data...)  

</div></div>

---

## HTTP Status Codes

<div class="columns"><div>

| Code | Meaning |
|------|---------|
| `200` | OK — success |
| `301` | Moved permanently |
| `400` | Bad request |
| `403` | Forbidden |
| `404` | Not found |
| `500` | Internal server error |

</div><div>

Grouped by first digit:

• `1xx` → Informational  
• `2xx` → Success  
• `3xx` → Redirection  
• `4xx` → Client error  
• `5xx` → Server error  

A working page returns `200 OK`.

</div></div>

---

## URLs

**Uniform Resource Locator** — the address of a resource on the Web.

```
https://www.example.com:443/about/index.html?name=andy#contact
  │         │              │       │              │         │
scheme    host            port    path          query   fragment
```

<div class="columns"><div>

• **Scheme** — protocol (`http`, `https`)  
• **Host** — domain name or IP address  
• **Port** — optional; defaults to `80` (HTTP), `443` (HTTPS)  
• **Path** — resource location on the server  

</div><div>

• **Query string** — key/value parameters after `?`  
• **Fragment** — in-page anchor after `#`  

DNS resolves the hostname to an IP address before the request is sent.

</div></div>

---

## What a Browser Actually Does

A browser is more than a document viewer.

<div class="columns"><div>

After receiving an HTTP response, the browser:

1. Parses HTML → builds the **DOM**  
2. Parses CSS → builds the **CSSOM**  
3. Combines both → **Render Tree**  
4. Calculates layout (positions, sizes)  
5. Paints pixels to screen  
6. Executes JavaScript  

</div><div>

**DOM** — Document Object Model  

A tree structure representing every element in the HTML document.

JavaScript can read and modify the DOM.

We will return to this in Lecture 05.

</div></div>

---

<!-- _class: title -->
## HTML Foundations

# Structure & Syntax

---

## What is HTML?

**HyperText Markup Language**

HTML describes the *structure* and *meaning* of web content.

<div class="columns"><div>

It is **not** a programming language.

There are no:

• Variables  
• Loops  
• Functions  
• Logic  

It is a **declarative** markup language.

You describe *what* things are, not *how* to produce them.

</div><div>

**Key concepts:**

• Elements — building blocks  
• Tags — mark the start and end of elements  
• Attributes — provide additional information  
• Nesting — elements can contain elements  

</div></div>

---

## From Python to HTML — A Shift in Thinking

You already know Python — an *imperative* language.

<div class="columns"><div>

**Python (imperative)**

```python
name = "Andy"
print(f"<h1>{name}</h1>")
```

You tell the computer *how* to produce output, step by step.

Execution follows your instructions in sequence.

</div><div>

**HTML (declarative)**

```html
<h1>Andy</h1>
```

You describe *what* the content is.

The browser decides how to render it.

No steps. No sequence. Just structure.

</div></div>

This distinction matters. HTML is not a program — it is a document.

---

## HTML Syntax

An HTML **element** consists of:

```html
<tagname attribute="value">Content goes here</tagname>
```

<div class="columns"><div>

**Opening tag** — marks the start  
**Content** — text or nested elements  
**Closing tag** — marks the end (`/`)  

Some elements are **void** (self-closing):

```html
<img src="photo.jpg" alt="A photo">
<br>
<hr>
<input type="text">
```

</div><div>

**Attributes** provide extra information:

```html
<a href="https://example.com">Link</a>
<img src="logo.png" alt="Logo">
<p class="intro">Hello</p>
<div id="main">...</div>
```

• `href` — hyperlink destination  
• `src` — file source  
• `alt` — alternative text  
• `class` / `id` — for CSS and JS  

</div></div>

---

## The HTML Document Structure

Every valid HTML page follows this skeleton:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Page Title</title>
    <link rel="stylesheet" href="style.css">
  </head>
  <body>
    <!-- Visible content goes here -->
  </body>
</html>
```

<div class="columns"><div>

**`<!DOCTYPE html>`** — tells the browser this is HTML5  
**`<html>`** — root element of the page  
**`<head>`** — metadata (not visible)  

</div><div>

**`<meta charset>`** — character encoding  
**`<title>`** — tab/window title  
**`<body>`** — all visible content  

</div></div>

---

## Semantic HTML

HTML5 introduced **semantic elements** — tags that describe the *meaning* of content, not just its appearance.

<div class="columns"><div>

**Structural semantics:**

```html
<header>   Site header / logo / nav   </header>
<nav>      Navigation links           </nav>
<main>     Primary page content       </main>
<article>  Self-contained content     </article>
<section>  Thematic grouping          </section>
<aside>    Sidebar / supplementary    </aside>
<footer>   Footer information         </footer>
```

</div><div>

**Why semantics matter:**

• Accessibility — screen readers use them  
• SEO — search engines understand structure  
• Maintainability — code is easier to read  
• Standards compliance  

Avoid overusing `<div>` and `<span>` where a semantic element exists.

</div></div>

---

## Text & Inline Elements

<div class="columns"><div>

**Headings** (h1–h6):

```html
<h1>Page title</h1>
<h2>Section heading</h2>
<h3>Subsection</h3>
```

Use headings to create a logical outline.  
`<h1>` once per page.

**Paragraph:**

```html
<p>This is a paragraph of text.</p>
```

</div><div>

**Inline text elements:**

```html
<strong>Bold / important</strong>
<em>Italic / emphasis</em>
<a href="url">Hyperlink</a>
<span>Generic inline wrapper</span>
<code>Inline code</code>
```

**Lists:**

```html
<ul>                  <!-- unordered -->
  <li>Item one</li>
  <li>Item two</li>
</ul>

<ol>                  <!-- ordered -->
  <li>First step</li>
  <li>Second step</li>
</ol>
```

</div></div>

---

## Images & Links

<div class="columns"><div>

**Images:**

```html
<img src="photo.jpg" alt="A landscape photo">
```

• `src` — path to the image file  
• `alt` — required; describes the image  
  (used by screen readers and if image fails)  
• Always include `alt` text  

**Relative vs absolute paths:**

```html
<!-- Relative (same server) -->
<img src="images/logo.png">

<!-- Absolute (external URL) -->
<img src="https://example.com/img.png">
```

</div><div>

**Links:**

```html
<!-- External link -->
<a href="https://example.com">Visit site</a>

<!-- Internal link -->
<a href="about.html">About us</a>

<!-- Open in new tab -->
<a href="https://example.com" target="_blank"
   rel="noopener noreferrer">External</a>

<!-- Email link -->
<a href="mailto:hello@example.com">Email</a>

<!-- In-page anchor -->
<a href="#contact">Jump to contact</a>
```

</div></div>

---

## Nesting & Document Hierarchy

HTML elements nest to form a **tree structure** — the DOM.

```html
<main>
  <article>
    <header>
      <h2>My First Blog Post</h2>
    </header>
    <p>This is the first paragraph.</p>
    <p>This is the second paragraph with a <a href="#">link</a>.</p>
  </article>
</main>
```

<div class="columns"><div>

Rules:

• Elements must be properly nested  
• Every opened tag must be closed  
• Siblings sit at the same level  
• Children are indented for readability  

</div><div>

Bad nesting (invalid):

```html
<!-- Wrong -->
<p>Hello <strong>world</p></strong>

<!-- Correct -->
<p>Hello <strong>world</strong></p>
```

</div></div>

---

## Inspecting HTML in the Browser

Every browser includes **Developer Tools**.

<div class="columns"><div>

Open with:

• `F12` (Windows / Linux)  
• `Cmd + Option + I` (macOS)  
• Right-click → *Inspect*  

The **Elements** panel shows:

• The live DOM tree  
• Applied styles  
• Element properties  

</div><div>

Use DevTools to:

• Inspect the structure of any webpage  
• Understand how HTML is organised in the wild  
• Debug your own pages  
• Experiment by editing elements live  

**Get into the habit of inspecting pages you use every day.**

</div></div>

---

## Critical Perspective

HTML is simple to learn but easy to use poorly.

<div class="columns"><div>

**Common mistakes:**

• Using `<div>` for everything (div soup)  
• Skipping `alt` attributes on images  
• Incorrect heading hierarchy (h1 → h3)  
• Missing `lang` attribute on `<html>`  
• Inline styles instead of CSS  

</div><div>

**Good practice:**

• Write HTML for meaning, not appearance  
• Validate at [validator.w3.org](https://validator.w3.org)  
• Test with a screen reader  
• Use semantic elements wherever possible  
• Separate content (HTML) from presentation (CSS)  

</div></div>

Presentation and behaviour are handled by CSS and JavaScript — HTML's only job is structure.

---

## Key Takeaways

• The Web runs on the HTTP request/response cycle — client requests, server responds  
• A URL uniquely identifies every resource on the Web  
• HTML is *declarative* — you describe structure, the browser renders it  
• Every page follows the same skeleton: `DOCTYPE` → `html` → `head` + `body`  
• Semantic elements communicate meaning to browsers, search engines and assistive technology  
• Think of HTML as a document, not a program  

---

## References

Berners-Lee, T., Fielding, R. and Masinter, L. (2005) *Uniform Resource Identifier (URI): Generic syntax*. RFC 3986. Fremont: IETF. Available at: https://www.rfc-editor.org/rfc/rfc3986 (Accessed: [date]).

Fielding, R. and Reschke, J. (2014) *Hypertext Transfer Protocol (HTTP/1.1): Semantics and content*. RFC 7231. Fremont: IETF. Available at: https://www.rfc-editor.org/rfc/rfc7231 (Accessed: [date]).

MDN Web Docs (2024) *HTML: HyperText Markup Language*. Mozilla. Available at: https://developer.mozilla.org/en-US/docs/Web/HTML (Accessed: [date]).

W3C (2023) *HTML Living Standard*. WHATWG. Available at: https://html.spec.whatwg.org (Accessed: [date]).

---

## References

Duckett, J. (2011) *HTML & CSS: Design and build websites*. Indianapolis: John Wiley & Sons.

Robbins, J.N. (2018) *Learning web design: A beginner's guide to HTML, CSS, JavaScript and web graphics*. 5th edn. Sebastopol: O'Reilly Media.
