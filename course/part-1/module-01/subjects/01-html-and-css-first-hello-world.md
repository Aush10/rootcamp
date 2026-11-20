# P1M1S01 — HTML and CSS: first Hello World

**Module:** 1.1 — Hello World: Desktop, Web, SQL, and Common Tools  
**Status:** READY FOR FIRST SESSION (reading links pending live verification)  
**Time target:** approximately 35–50 minutes of the 6–8-hour module  
**Pre-AI coding policy:** write the HTML and CSS yourself; the instructor can explain concepts, troubleshoot questions, and review finished evidence, but must not supply finished code or patches.

## Why this matters to Rootcamp

Every later storefront, defensive browser extension, and Android-facing interface has a visible layer. HTML identifies a page's structure and content. CSS controls how that structure looks. Neither, by itself, proves a page has a secure server, encrypted connection, or trustworthy data source. Distinguishing those layers is the first step toward understanding what a later agent can see, modify, or accidentally expose.

## Required reading — human authority

**Shay Howe, “Building Your First Web Page,” *Learn to Code HTML & CSS*.**  
Read the portions that introduce an HTML document, basic elements, and the connection to a stylesheet; skip exhaustive syntax and optional design polish. **Target: 10–15 minutes.**

- Source: https://learn.shayhowe.com/html-css/building-your-first-web-page/
- Why this author: Howe is a named web developer and educator whose tutorial introduces actual markup and browser behavior.
- Verification: link and page title are provided from reference knowledge; **not checked live** in this session.

## Recommended reading — pick at most one now

1. **Bert Bos, “Starting with HTML + CSS,” W3C.** A short creator-authored walk-through of attaching CSS to an HTML page. https://www.w3.org/Style/Examples/011/firstcss.en.html (link not checked live)
2. **Eric A. Meyer and Estelle Weyl, *CSS: The Definitive Guide*, 4th ed.** Introductory section on rules, declarations and selectors. Use library/legitimate preview if available; the full book is not required.
3. **Rachel Andrew and other named instructors, *Learn CSS* (web.dev).** Browse the opening course path as optional perspective. https://web.dev/learn/css/ (individual chapter attribution to be verified).

## AI overview (conceptual only; no solution code)

The browser reads a local HTML file and builds a **document object model (DOM)**: a tree-like representation of the page's elements. A heading, paragraph, list, and link are not just visual things; they have meanings, and those meanings help browsers, assistive technologies, and later programmatic tools understand content. CSS matches elements through **selectors** and applies visual declarations such as color, spacing, and alignment.

A `Hello World` file can be opened locally without a web server. Later, the same page may be served by Node, a container, a cloud host, or an Android interface. The visible page can look identical while the underlying security boundary changes dramatically: local file access is not the same as an HTTPS page backed by server processes and databases.

**Rootcamp connection:** A future agent or browser extension should not assume that changing what a page *looks like* changes what the underlying service can *do*. This distinction matters for permission prompts, fake security indicators, and reviews of untrusted UI code.

**Deliberate limit:** Learn only enough selectors, properties and document structure to recognize and modify a simple page. Responsive design, build pipelines, JavaScript frameworks and web application security arrive later.

## Ungraded assignment — “Change one thing, trace one thing”

1. Create a new **local** `hello-world` folder under your own `Projects/rootcamp` workspace.
2. Without generated code, create a plain HTML page with a heading, a paragraph, and one link.
3. Put a small style rule in a separate CSS file and connect it to the HTML page.
4. Open the page in a browser and inspect the heading using the browser's developer tools.
5. Change **one** style property, refresh, and describe what changed and what did not.
6. Make a deliberate mistake in a selector or CSS filename, observe the effect, fix it, and record the cause.
7. Write two sentences on why this file is not yet a remotely hosted web application and does not have a TLS handshake.

**No grade on this assignment.** Its purpose is to feel the difference between structure, styling, browser interpretation, and hosting.

## What to save

- `index.html` and one `.css` file **written by the learner**
- A browser screenshot with no secrets, personal tabs or local private paths exposed
- `notes.md` with:
  - The distinction among HTML, CSS and the DOM
  - What broke and how it was restored
  - One future use in a storefront or security interface
- A brief source citation to Shay Howe; cite a section, not an unattributed AI summary.

## Links to next subjects

- P1M1S02 — SQLite: a table and a query (content versus presentation)
- P1M1S05 — HTTPS handshakes, certificates, and thumbprints (local file versus protected network connection)
- P1M4S01 — Browser JavaScript and the DOM (behavior added to the page)

## Optional rabbit holes

- CSS specificity
- Accessibility tree
- Browser rendering pipeline

Do not expand these yet unless a basic misunderstanding blocks the exercise.
