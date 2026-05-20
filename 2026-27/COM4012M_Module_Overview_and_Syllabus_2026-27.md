# COM4012M — Programming for the Web
## Module Overview and Syllabus 2026–27

**York St John University — School of Science, Technology and Health**

---

## Module Details

| | |
|---|---|
| **Module code** | COM4012M |
| **Module title** | Programming for the Web |
| **Level** | 4 (first year undergraduate) |
| **Credits** | 20 |
| **Module leader** | Dr Andy Guest |
| **Contact** | a.guest@yorksj.ac.uk |
| **Prior knowledge assumed** | Introductory Python (COM4011M or equivalent) |
| **Assessment** | 100% portfolio |
| **Assessment deadline** | TBC (Semester 2, Week 12) |
| **Feedback date** | TBC |

---

## Module Description

COM4012M introduces students to the theory and practice of building for the web. The module covers the full client-to-server development stack — HTML, CSS, JavaScript, and PHP — alongside the principles of User Experience (UX) design that underpin effective web application development.

The module is structured around two parallel strands delivered in each weekly session:

- **Lectures** address the theoretical and design dimensions of web development, using Jesse James Garrett's five-plane UX framework as an organising structure, alongside topics in information design, usability, accessibility, and — new in 2026–27 — the critical use of AI coding tools.
- **Labs** develop practical web development skills progressively, from HTML and CSS fundamentals through to server-side PHP, database integration, asynchronous JavaScript, and modern CSS techniques.

Students are expected to use AI coding assistants (such as GitHub Copilot, Claude, or ChatGPT) as part of their professional workflow throughout the module. Critically evaluating and adapting AI-generated code is taught explicitly and assessed as a component of the portfolio.

---

## Learning Outcomes

On successful completion of this module, students will be able to:

| | |
|---|---|
| **LO1** | Demonstrate an understanding of essential design concepts, principles and approaches to software development |
| **LO2** | Deploy appropriate theory, practice and methods for the design, production, access, use and evaluation of software |
| **LO3** | Apply key software engineering practices and principles to multimedia software development |

*Note: Learning Outcomes are fixed at validation and unchanged from 2025–26. The introduction of AI tools content and assessment maps to LO2 (evaluating software tools and methods) and LO3 (applying software engineering practices) without requiring revalidation.*

---

## Module Structure

Sessions are held once per week. Each week comprises:

- **Lecture:** 1 hour — theory, design principles, and conceptual content
- **Lab:** 3 hours — practical web development with structured worksheets
- **Self-directed learning (SDL):** 1.5 hours — recommended (not timetabled)

---

## Lecture Programme

The lecture programme addresses UX design theory in the first half of the semester, then transitions to topics in visual design, usability, accessibility, and AI-assisted development. The sequence follows Garrett's five-plane model (strategy → scope → structure → skeleton → surface) before moving into evaluation and professional practice.

| Week | Title | Key Content |
|------|-------|-------------|
| 1 | How the Web Works & HTML Foundations | Client-server model; HTTP request/response cycle; role of HTML, CSS, JS, and PHP; brief history of the web; introduction to UX as the module's design framework |
| 2 | CSS Fundamentals & the Box Model | Separation of content and presentation; inline, internal, and external CSS; the box model; typography, colour, and spacing; CSS specificity and the cascade |
| 3 | Responsive Layouts & Accessibility | Responsive web design; viewport and media queries; fluid grids; introduction to WCAG; semantic HTML and its role in accessibility; screen readers and assistive technologies |
| 4 | AI Tools for Web Development | What AI coding assistants are and how they work; effective prompting for web development tasks; critical evaluation of AI-generated code; academic integrity and disclosure requirements; known limitations (outdated APIs, accessibility gaps, security anti-patterns) |
| 5 | JavaScript Basics + DOM & Event-driven Programming | From Python to the browser: JS syntax for Python developers; variables, types, functions; the Document Object Model; event listeners and handlers; selecting and manipulating DOM elements |
| 6 | Arrays, Objects & Functional Patterns | JS arrays and array methods; objects and object literals; introduction to functional programming patterns (map, filter, reduce); JSON as a data format |
| 7 | Asynchronous JS & APIs | The event loop and asynchronous execution; callbacks, promises, and async/await; fetch() and REST APIs; handling JSON responses; practical API integration |
| 8 | Introduction to PHP & Server-side Concepts | Why server-side programming is needed; PHP syntax and structure; variables, data types, control flow; echo and output; running PHP on ysjcs.net; comparison with client-side JS |
| 9 | Forms, PHP & Database Interaction | HTML forms and HTTP methods (GET vs POST); PHP form handling; introduction to MySQL; connecting to a database with mysqli; SELECT, INSERT, UPDATE, DELETE; phpMyAdmin |
| 10 | Introduction to ASP.NET & the MVC Pattern *(conceptual overview)* | Server-side development beyond PHP; the MVC architectural pattern; ASP.NET as a contrast to PHP; when and why different server-side technologies are chosen; this topic is not assessable but provides important professional breadth |
| 11 | Web Security Fundamentals | Common web vulnerabilities (XSS, SQL injection, CSRF); input validation and sanitisation; HTTPS and secure cookies; responsible disclosure; security considerations when using AI-generated code |
| 12 | Evaluation, Employability & Next Steps | Usability evaluation methods; heuristic evaluation (Nielsen's 10 heuristics); accessibility auditing (WAVE, Lighthouse); the web development job market; portfolio building; frameworks and technologies to explore next |

### Notes on Changes from 2025–26

**Week 4 (new):** A dedicated AI Tools lecture has been introduced before students encounter the more complex JavaScript and PHP content. Students need a critical framework for AI use before they begin relying on AI assistance in labs. This replaces the standalone JavaScript Basics lecture from the previous year.

**Week 5 (merged):** JavaScript fundamentals (variables, types, functions, the Python comparison) are condensed into the opening section of the DOM lecture. Students entering with Python experience pick up JS syntax quickly; a full standalone lecture is no longer required.

**Week 10 (reduced):** ASP.NET is retained as a conceptual contrast to PHP — students should understand that server-side development is not limited to one language or framework — but is no longer treated as an assessable technology. The session is a comparative discussion rather than a technical tutorial.

---

## Lab Programme

Labs run for three hours each week and are structured around practical worksheets. Students work independently with tutor support. Each lab builds directly on the preceding week's lecture content.

The web server used throughout is **ysjcs.net** (SSH on port 2222; file transfer via SCP or SFTP; phpMyAdmin at www.ysjcs.net/phpmyadmin).

---

### Week 1 — HTML Foundations

**Topic:** Structuring content with HTML

Students will be able to:
- Write valid HTML5 documents with correct DOCTYPE, head, and body structure
- Use semantic elements including headings, paragraphs, lists, links, images, and tables
- Create internal and external hyperlinks, including bookmark anchors
- Understand file and folder organisation for a multi-page website

---

### Week 2 — CSS Fundamentals

**Topic:** Styling web pages with CSS

Students will be able to:
- Apply styles using inline, internal, and external stylesheets
- Use CSS properties to control typography, colour, borders, margins, and padding
- Understand and apply the CSS box model
- Use CSS selectors including element, class, and ID selectors

---

### Week 3 — Semantic HTML & CSS Positioning

**Topic:** Page layout and HTML5 semantic structure

Students will be able to:
- Use HTML5 semantic elements (header, footer, nav, section, article, aside) appropriately
- Apply CSS positioning (static, relative, absolute, fixed, sticky) to control element placement
- Use floats and the basics of flexbox for layout
- Understand how semantic structure supports accessibility

---

### Week 4 — JavaScript Part 1

**Topic:** JavaScript syntax and the browser environment

Students will be able to:
- Write basic JavaScript including variables (var, let, const), functions, and conditionals
- Use document.write(), alert(), and prompt() for basic output and input
- Attach JavaScript to HTML pages internally and externally
- Recognise the parallels and differences between JavaScript and Python

---

### Week 5 — HTML5, CSS3 & Responsive Design

**Topic:** Modern HTML and CSS features; responsive web design

Students will be able to:
- Use HTML5 multimedia elements (audio, video) and graphical elements (canvas, SVG)
- Apply CSS3 features including transitions, animations, and multi-column layouts
- Implement a responsive grid layout using CSS and media queries
- Use the viewport meta tag correctly for mobile display

---

### Week 6 — PHP Part 1

**Topic:** Introduction to server-side programming with PHP

Students will be able to:
- Write basic PHP scripts using variables, data types, echo, and comments
- Use control structures: if/else, switch, for loops, and while loops
- Transfer files to ysjcs.net via SSH/SCP and run PHP scripts from the server
- Understand the difference between client-side and server-side execution

---

### Week 7 — PHP Part 2 & SQL

**Topic:** PHP with database interaction

Students will be able to:
- Connect to a MySQL database using mysqli_connect()
- Execute SQL queries (SELECT, INSERT, UPDATE, DELETE) from PHP
- Display database records in an HTML page
- Use phpMyAdmin to create and manage databases and tables

---

### Week 8 — PHP & Cookies

**Topic:** State management with cookies

Students will be able to:
- Create, read, and delete cookies using PHP (setcookie()) and JavaScript (document.cookie)
- Distinguish between session cookies and persistent cookies
- Understand the limitations and security implications of cookie-based state
- Apply cookies to a simple practical use case (e.g. remembering a user preference)

---

### Week 9 — Session Variables

**Topic:** Server-side session management

Students will be able to:
- Start a PHP session with session_start() and store data in $_SESSION
- Read, modify, and destroy session variables across multiple pages
- Distinguish between cookies and session variables and know when to use each
- Use server variables ($_SERVER) to access request and client information

---

### Week 10 — Shopping Carts & Database Integration

**Topic:** Combining sessions and databases in a multi-page application

Students will be able to:
- Build a multi-page application using sessions to maintain state across pages
- Integrate form input, database lookup, session storage, and output in a complete workflow
- Use INSERT and UPDATE statements to modify database records from a form
- Understand the architecture of a simple e-commerce flow

---

### Week 11 — JSON & Asynchronous JavaScript

**Topic:** Data interchange formats and asynchronous requests

Students will be able to:
- Parse and construct JSON data structures in JavaScript
- Use XMLHttpRequest or fetch() to make asynchronous requests to a server
- Send and receive JSON data between a PHP backend and a JavaScript frontend
- Use jQuery to simplify DOM manipulation and event handling

---

## Assessment

### Overview

The module is assessed by a single portfolio component worth 100% of the module mark.

Students design and develop a fully functioning website of their own choosing, hosted live on ysjcs.net. The site must demonstrate competency across the full stack taught in the module (HTML5, CSS, JavaScript, PHP) and should address all five planes of the UX design framework.

**Minimum scope:** 5–6 pages. Most submissions achieving strong marks will exceed this.

**Submission deadline:** TBC — Semester 2, Week 12

---

### Submission Requirements

Students submit three components:

**1. Website on ysjcs.net**
The live, functional website is the primary submission. This is the version that is marked.

**2. ReadMe Document** (Word or equivalent)
A structured document containing:
- Introduction to the website (100–250 words)
- User login details (if applicable)
- URL to the index page on ysjcs.net
- phpMyAdmin username and database details
- Outline of notable features, technologies, or innovations
- Testing results with clearly identified tests
- References for any adapted code, with sources and brief explanation of adaptations
- Full reference list
- AI Disclosure Statement (brief, not in word count)

**3. AI Development Log** (separate document, 300–500 words — required)
A structured critical reflection on AI tool use, containing:
- Which AI tools were used and at which stages
- Two or three specific worked examples, each covering: the prompt given; the output produced; what was wrong, incomplete, or unsuitable; and what changes were made and why
- A reflection (100–150 words) on how AI tools affected the workflow and what was learned about their limitations

A zip file of all website source files is also submitted to Moodle for archival and integrity purposes.

---

### Marking Criteria

| Criterion | Weighting | What is assessed |
|-----------|-----------|-----------------|
| **Content** | 20% | Quality, depth, and relevance of site content; multimedia integration; user interaction; application of the inverted pyramid principle; originality |
| **Use of Technology** (incl. AI tool use) | 25% | Appropriate and effective use of HTML5, CSS, JavaScript, PHP, and any additional technologies; quality of AI Development Log including sophistication of prompting, critical evaluation of output, and evidence of adaptation and understanding |
| **User Experience Design** | 20% | Graphic design quality and consistency; navigation clarity; accessibility compliance (WCAG); responsiveness across screen sizes; application of UX design principles |
| **Web Standards** | 15% | HTML5 and CSS validation; semantic markup; code structure and quality; display of validation logos |
| **Professionalism & Presentation** (incl. AI Development Log) | 20% | Site functions correctly on ysjcs.net; error handling; referencing of borrowed code; quality and completeness of ReadMe; quality and critical depth of AI Development Log |

Marking follows the University's Generic Assessment Descriptors across grade bands: Fail (0–29), Borderline Fail (30–39), Third (40–49), 2:2 (50–59), 2:1 (60–69), First (70–84), High First (85–100). Full band descriptors for each criterion are provided in the Assignment Brief.

---

### AI Assessment Policy

The use of AI coding assistants is **expected and encouraged** throughout this module. The AI Development Log ensures that use is transparent, critically engaged, and demonstrably understood.

| | Policy |
|---|---|
| **Permitted** | All stages of development — planning, coding, debugging, content drafting |
| **Prohibited** | Submitting AI output without critical evaluation or disclosure; using AI to generate the AI Development Log itself |
| **Assessed via** | AI Development Log (contributes to Use of Technology and Professionalism & Presentation criteria) |
| **Rewarded** | Sophisticated, critical AI use is explicitly rewarded at First and High First grade bands |
| **Penalised** | Undisclosed AI use, or AI output submitted without evidence of understanding, will score poorly regardless of apparent sophistication |

The key principle is **authorship and understanding**. A student who uses AI to generate code, identifies a flaw in the output, corrects it, and explains their reasoning is demonstrating exactly the professional competency this module aims to develop.

---

### Changes to Assessment from 2025–26

| Area | 2025–26 | 2026–27 | Rationale |
|------|---------|---------|-----------|
| AI Development Log | Not required (brief statement only) | Required separate document (300–500 words) | Makes AI use transparent, assessable, and pedagogically meaningful |
| Use of Technology weighting | 20% | 25% | Absorbs AI assessment; reflects that critical technology use is the key differentiator |
| Web Standards weighting | 20% | 15% | Validation is increasingly automated; reduced weight reflects this |
| AI policy | Restrictive (syntax lookup only) | Professional (all stages; documented) | Previous policy was unenforceable and inconsistent with teaching AI as a topic |

---

## Reading and Resources

### Core References

- Garrett, J. J. (2011) *The Elements of User Experience: User-Centered Design for the Web and Beyond.* 2nd ed. New Riders.
- Nielsen, J. (1993) *Usability Engineering.* Morgan Kaufmann.
- Duckett, J. (2014) *HTML & CSS: Design and Build Websites.* Wiley.
- Duckett, J. (2014) *JavaScript & jQuery: Interactive Front-End Web Development.* Wiley.

### Key Online Resources

- W3Schools: [www.w3schools.com](https://www.w3schools.com) — primary practical reference for HTML, CSS, JS, and PHP
- MDN Web Docs: [developer.mozilla.org](https://developer.mozilla.org) — authoritative reference documentation
- W3C HTML Validator: [validator.w3.org](https://validator.w3.org)
- W3C CSS Validator: [jigsaw.w3.org/css-validator](https://jigsaw.w3.org/css-validator)
- WAVE Accessibility Tool: [wave.webaim.org](https://wave.webaim.org)
- Nielsen Norman Group: [www.nngroup.com](https://www.nngroup.com) — usability and UX research
- W3C Web Accessibility Initiative: [www.w3.org/WAI](https://www.w3.org/WAI)

---

## Key Policies

### Academic Integrity

Students are referred to the University's Academic Misconduct Policy. Penalties for academic misconduct, including misrepresentation of AI use, may include mark reduction or termination of programme.

### Late Submission

A penalty may be applied for late or non-submission of work by the published deadline. Where a reassessment opportunity exists, late or non-submission receives a mark of zero and is not eligible for a capped mark.

### Exceptional Circumstances

Extensions to the published deadline may be granted where a student meets the eligibility criteria for Exceptional Circumstances. Students should approach the module leader or Student Services in advance of the deadline.

### Anonymous Marking

This assessment is exempt from anonymous marking (portfolio format with live website component).

---

*COM4012M · York St John University · School of Science, Technology and Health · 2026–27*
