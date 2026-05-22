---
name: artifact
description: Create standalone, self-contained HTML pages in /tmp to visualize and communicate various types of information.
---

Artifacts should *always*...
- Use this drop-in, fully classless CSS file for styling:
  ```html
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/amanvirparhar/tufte-y@0.2.6/tufte-y.css"/>
  ```
- Use `d3` to visualize any kind of data; it can be loaded from a CDN like so:
  ```html
  <script src="https://cdn.jsdelivr.net/npm/d3@7"></script>
  ```
- `open` the HTML file after it has been written to disk

Abide by the following CSS guidelines:
- Heavily avoid `<style>` blocks and custom CSS declarations
- Every page must be wrapped in `<article>` and the "main" content (everything but the title and subtitle) should be wrapped in a single `<section>` block
- Never use `<div>` or `<span>` for layout, as the CSS handles structure through semantic elements
- Tables should be clean/unadorned, as the CSS file already provides all of the styling necessary
- Always read on this reference when creating charts/tables with d3: `https://raw.githubusercontent.com/chrisvoncsefalvay/claude-d3js-skill/refs/heads/main/SKILL.md`
- Charts should...
  - Be wrapped in `<figure>`
  - Never use data labels; instead, always use tooltips to show data values on hover 
  - Use earthy HSL tones for chart colors, and avoid neon, "Bootstrap-y" hex colors, and pure black
  - Have margins set based on their longest axis label: measure the string length of tick labels and multiply by ~10px per character to compute the needed left/bottom margin, rather than blindly hardcoding
  - Not have `<figcaption>` elements - the section heading and surrounding prose already explain what the reader is looking at; only add a `<figcaption>` when the chart would be genuinely confusing without one
- The main title should, of course, be an `<h1>`, and it should always be short (less than 30 characters long)
- The first `<p>` after an `<h1>` is styled as a subtitle, which means that it should be never be more than 20-30 characters long

Think of each artifact as an essay with supporting evidence, not a dashboard. The prose should tell the main story, and charts/tables should present data to illustrate specific points. Make sure to not unnecessarily repeat the same information or rehash the same point, and make everything flow in a single column at reading width.
