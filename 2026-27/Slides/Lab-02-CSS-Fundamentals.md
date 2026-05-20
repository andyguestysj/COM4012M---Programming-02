<script type="text/javascript" src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML"></script>
<script type="text/x-mathjax-config">
  MathJax.Hub.Config({ tex2jax: {inlineMath: [['$', '$']]}, messageStyle: "none" });
</script>

# Lab 02 — CSS Fundamentals & the Box Model

## Overview

In this lab you will add an external stylesheet to the personal bio site you built in Lab 01. By the end of the session your site should have a consistent visual style applied across all pages, using only CSS — no inline styles.

If you did not complete Lab 01, start by creating a basic `index.html` with a `<header>`, `<nav>`, `<main>`, and `<footer>` — you can style a minimal page.

---

## Setting Up

### Create your stylesheet

1. Open your `lab01` folder from last week (or create a fresh `lab02` folder with a copy of your HTML files).
2. Create a new file in the same folder called `style.css`.
3. Link the stylesheet from every HTML page by adding the following line inside the `<head>` element:

```html
<link rel="stylesheet" href="style.css">
```

Your `<head>` should now look something like this:

```html
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Your Name — Home</title>
  <link rel="stylesheet" href="style.css">
</head>
```

4. Open `style.css` in your editor. Add this at the very top — it makes the box model behave predictably (we will cover why in the lecture):

```css
*, *::before, *::after {
  box-sizing: border-box;
}
```

---

## Part 1 — Typography

### Exercise 1.1 — Set a base font

Add styles for the `body` element to establish a default font for the whole page:

```css
body {
  font-family: Arial, Helvetica, sans-serif;
  font-size: 16px;
  line-height: 1.6;
  color: #333333;
  background-color: #f5f5f5;
}
```

Save `style.css` and refresh your browser. Your text should now look noticeably different from the browser default.

### Exercise 1.2 — Style the headings

Add distinct styles for `h1` and `h2`:

```css
h1 {
  font-size: 2.5em;
  font-family: Georgia, "Times New Roman", serif;
  color: #1a1a2e;
  margin-bottom: 4px;
}

h2 {
  font-size: 1.4em;
  color: #16213e;
  border-bottom: 2px solid #e0e0e0;
  padding-bottom: 6px;
}
```

Notice that `h1` uses a different font family from the body — a classic typographic approach of pairing a serif display font with a sans-serif body font.

### Exercise 1.3 — Experiment with font properties

Try adjusting the following properties and observe the effect:

```css
p {
  font-size: 1em;
  line-height: 1.8;
  letter-spacing: 0.01em;
  color: #444444;
}
```

- Change `line-height` between `1.2` and `2.0` — notice how readability changes.
- Change `letter-spacing` to `0.1em` — notice how it affects the feel of the text.

---

## Part 2 — Colour Scheme

### Exercise 2.1 — Choose a colour scheme

Pick three colours to use throughout your site:

- A **background** colour (light, easy to read against)
- A **text** colour (dark, high contrast)
- An **accent** colour (for headings, borders, and highlights)

You can use a tool like [coolors.co](https://coolors.co) or [colorhunt.co](https://colorhunt.co) to find a combination you like.

Apply your colours to the body and headings. For example:

```css
body {
  background-color: #fafafa;
  color: #2c2c2c;
}

h1, h2 {
  color: #005f73;  /* your accent colour */
}
```

### Exercise 2.2 — Colour formats

CSS supports several colour formats. Try expressing the same colour in different ways — all of these are equivalent:

```css
/* Named colour */
color: steelblue;

/* Hex */
color: #4682b4;

/* RGB */
color: rgb(70, 130, 180);

/* HSL */
color: hsl(207, 44%, 49%);

/* RGBA — with 50% transparency */
background-color: rgba(70, 130, 180, 0.5);
```

---

## Part 3 — The Box Model

### Exercise 3.1 — Inspect the box model in DevTools

Before writing any CSS, use the browser to see the box model in action:

1. Open your page in Chrome or Firefox.
2. Right-click any paragraph and choose **Inspect**.
3. In the DevTools panel, select the **Computed** tab (Chrome) or scroll to the box model diagram.
4. Hover over the margin, padding, border, and content areas in the diagram — the browser highlights each region in the page.

Every element has these four layers, even if they are all zero.

### Exercise 3.2 — Margin and padding

Add spacing to your page layout:

```css
body {
  margin: 0;
  padding: 0;
}

header {
  padding: 24px 32px;
  background-color: #005f73;
  color: #ffffff;
}

header h1 {
  margin: 0;
  color: #ffffff;
}

main {
  padding: 32px;
  max-width: 900px;
  margin: 0 auto;  /* centres the content horizontally */
}

footer {
  padding: 16px 32px;
  background-color: #333333;
  color: #cccccc;
  font-size: 0.875em;
}
```

`margin: 0 auto` on a block element with a set `max-width` is the standard way to centre page content.

### Exercise 3.3 — Borders

Add a visible border to your `<aside>` element:

```css
aside {
  border: 2px solid #005f73;
  border-radius: 6px;
  padding: 16px 20px;
  background-color: #e9f5f8;
}
```

Try the following variations:

```css
border: 1px dashed #ccc;
border-left: 4px solid #005f73;  /* accent left border only */
border-radius: 12px;             /* more rounded corners */
```

---

## Part 4 — Selectors

### Exercise 4.1 — Class selectors

Class selectors let you apply a style to specific elements rather than all elements of a type.

Add a class to one of your paragraphs in `index.html`:

```html
<p class="intro">This is the introductory paragraph of my page.</p>
```

Then add a rule for that class in `style.css`:

```css
.intro {
  font-size: 1.15em;
  font-style: italic;
  color: #005f73;
  border-left: 3px solid #005f73;
  padding-left: 12px;
}
```

You can apply the same class to multiple elements — try adding `class="intro"` to a paragraph on another page and confirm that the style applies there too.

### Exercise 4.2 — ID selectors

An ID uniquely identifies a single element. Add an `id` to your `<header>` in the HTML:

```html
<header id="site-header">
```

Then style it by ID in your CSS:

```css
#site-header {
  background-color: #1a1a2e;
  color: #ffffff;
  text-align: center;
}
```

Notice that the `#site-header` rule takes priority over a general `header` rule if both exist — this is specificity in action.

### Exercise 4.3 — Styling navigation links

The `<nav>` element and its links probably look plain by default. Style them:

```css
nav {
  background-color: #16213e;
  padding: 10px 32px;
}

nav a {
  color: #ffffff;
  text-decoration: none;
  margin-right: 20px;
  font-weight: bold;
}

nav a:hover {
  color: #a8dadc;
}
```

`nav a` is a **descendant selector** — it only targets `<a>` elements that are inside a `<nav>`, leaving other links unstyled.

`:hover` is a **pseudo-class** — it applies styles when the user's mouse is over the element. Try it in your browser.

---

## Part 5 — Consistency Across Pages

### Exercise 5.1 — Apply the stylesheet to all pages

Make sure `<link rel="stylesheet" href="style.css">` appears in the `<head>` of every HTML file — `index.html`, `skills.html`, and `about.html`.

Open each page in the browser and confirm they all share the same visual style.

This is the key advantage of an external stylesheet: one file controls the appearance of the entire site.

---

## Part 6 — Validation

### Exercise 6.1 — Validate your CSS

1. Go to [jigsaw.w3.org/css-validator](https://jigsaw.w3.org/css-validator).
2. Choose the **File Upload** tab and upload `style.css`.
3. Fix any errors reported and re-validate until you have zero errors.

Also re-validate your HTML at [validator.w3.org](https://validator.w3.org) — adding a `<link>` element should not introduce errors, but it is worth checking.

### Add validation logos

Once both validators show no errors, add the official validation logos to your page footer:

```html
<footer>
  <p>Contact: <a href="mailto:you@example.com">you@example.com</a></p>
  <p>
    <a href="https://validator.w3.org/check?uri=referer">
      <img src="https://www.w3.org/Icons/valid-html401" alt="Valid HTML">
    </a>
    <a href="https://jigsaw.w3.org/css-validator/check/referer">
      <img src="https://jigsaw.w3.org/css-validator/images/vcss" alt="Valid CSS">
    </a>
  </p>
</footer>
```

These logos are a requirement of the Web Standards criterion in the portfolio assessment.

---

## Extension Tasks

If you finish the main exercises with time to spare:

1. **Google Fonts** — visit [fonts.google.com](https://fonts.google.com), choose a font pair (one for headings, one for body text), and use the `<link>` code they provide to load them in your `<head>`. Apply them in your CSS with `font-family`.

2. **Hover effects on the nav** — if you haven't already, add a `:hover` rule to your nav links. Also try adding a `transition` for a smooth colour change:
   ```css
   nav a {
     transition: color 0.2s ease;
   }
   ```

3. **Specificity experiment** — add `!important` to one property and observe that it overrides everything else. Then remove it and find a proper solution using a more specific selector instead. `!important` is rarely the right answer.

4. **Box model arithmetic** — without `box-sizing: border-box`, calculate the total rendered width of:
   - `width: 300px`, `padding: 20px`, `border: 3px solid black`
   Then add `box-sizing: border-box` and observe the difference in DevTools.

---

## Checklist

Before you finish, check that your site has:

- [ ] An external `style.css` file linked from every HTML page
- [ ] `box-sizing: border-box` applied globally at the top of the stylesheet
- [ ] A consistent colour scheme using at least three colours
- [ ] At least two different `font-family` values used
- [ ] Styled headings (`h1`, `h2`) with distinct sizes and colours
- [ ] Padding and margin applied to at least three different elements
- [ ] At least one visible border
- [ ] At least one class selector in use (in both CSS and HTML)
- [ ] At least one ID selector in use
- [ ] Navigation links styled (no underline, colour changed)
- [ ] `:hover` state on navigation links
- [ ] Zero CSS validation errors
- [ ] Zero HTML validation errors
- [ ] Validation logos in the footer
