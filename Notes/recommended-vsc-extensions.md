# Recommended Visual Studio Code Extensions  
## COM4012M – Web Programming

Using :contentReference[oaicite:0]{index=0} for this module works very well because students can use the same environment across HTML, CSS, JavaScript, PHP, and introductory ASP.NET work.

These extensions help support first-year students by improving code quality, reducing setup issues, and making debugging easier.

---

# Essential Extensions

## Live Server

### Why

* Launches a local development server for HTML/CSS/JavaScript projects
* Automatically refreshes the browser when files are saved
* Makes testing much easier for beginners

### Useful For

* HTML
* CSS
* JavaScript
* Responsive design testing

---

## Prettier – Code Formatter

### Why

* Automatically formats code consistently
* Helps students learn clean code structure
* Reduces common syntax mistakes caused by poor formatting

### Useful For

* HTML
* CSS
* JavaScript
* JSON

---

## ESLint

### Why

* Identifies JavaScript mistakes early
* Highlights syntax errors and poor practices
* Encourages professional coding habits

### Useful For

* JavaScript
* DOM scripting
* Form validation work

---

## HTML CSS Support

### Why

* Better autocomplete for HTML and CSS
* Faster development
* Helps students discover valid properties and values

### Useful For

* HTML
* CSS

---

## Path Intellisense

### Why

* Autocompletes filenames and paths
* Helps avoid broken image and stylesheet links

### Useful For

* Linking CSS files
* Images
* JavaScript files
* Project organisation

---

# Useful Extensions

## Auto Rename Tag

### Why

* Automatically updates matching HTML tags
* Prevents frustrating beginner mistakes

### Useful For

* HTML development

---

## JavaScript (ES6) Code Snippets

### Why

* Provides common JavaScript templates
* Speeds up development
* Helps students learn syntax patterns

### Useful For

* JavaScript fundamentals

---

## GitLens

### Why

* Improves Git integration inside VS Code
* Helps students understand version control
* Useful when introducing GitHub issue tracking and debugging workflows

### Useful For

* Git and GitHub workflow

---

## Error Lens

### Why

* Makes errors and warnings much more visible
* Excellent for beginners who often miss small syntax errors

### Useful For

* All programming languages

---

# PHP Support

## PHP Intelephense

### Why

* Strong autocomplete and error checking for PHP
* Improves understanding of server-side scripting

### Useful For

* PHP
* Form processing
* Server-side validation

---

## PHP Server (Optional Alternative)

### Why

* Quick way to run local PHP projects

### Useful For

* PHP practical sessions

---

# Optional for ASP.NET Introduction

## C# Dev Kit

### Why

* Useful if students briefly explore ASP.NET concepts
* Provides strong support for C# and .NET development

### Useful For

* Introductory ASP.NET

---

# Strongly Recommended Student Setup

## Minimum Install Set

For Week 1 I would strongly recommend students install:

* Live Server
* Prettier
* ESLint
* Auto Rename Tag
* Path Intellisense
* PHP Intelephense
* Error Lens

This keeps setup simple while covering nearly all semester needs.

---

# Good Teaching Practice

## Suggest a Shared Settings File

Providing students with a `.vscode/settings.json` file helps standardise behaviour across the cohort.

Example:

```json
{
    "editor.formatOnSave": true,
    "files.autoSave": "afterDelay",
    "editor.wordWrap": "on",
    "liveServer.settings.donotShowInfoMsg": true
}