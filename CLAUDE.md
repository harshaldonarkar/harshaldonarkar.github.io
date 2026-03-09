# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a **single-file** editorial portfolio for Harshal Donarkar — an AI Engineer. The entire site lives in `index.html`. There are no build tools, no npm, no frameworks, no dependencies, and no build step.

## Running Locally

```bash
# Open directly
open index.html

# Or serve with Python
python3 -m http.server 8080

# Or with Node
npx serve .
```

Visit `http://localhost:8080`. There is no compilation or installation required.

## Architecture

Everything is contained in a single `index.html`:

- **`<style>` block in `<head>`** — all CSS, including custom properties, animations, and responsive rules
- **`<body>`** — all HTML markup
- **`<script>` at end of `<body>`** — all JavaScript (vanilla ES6+)

### Panels

The site uses a horizontal-scrolling layout. `#stage` is a `display: flex` container holding 9 full-viewport panels:

| ID  | Section    |
|-----|------------|
| p0  | Hero       |
| p1  | Experience |
| p2  | Skills     |
| p3  | Projects   |
| p4  | Live AI Demo |
| p5  | Writing    |
| p6  | Research   |
| p7  | Education  |
| p8  | Contact    |

### CSS Token System

All colours are defined as custom properties at `:root` (light theme) and `[data-theme="dark"]` (dark theme):

```css
:root {
  --red: #C1121F;    /* accent */
  --blue: #003566;   /* research panel */
  --paper: #F2EDE4;  /* background */
  --ink: #0D0D0D;    /* text */
  --tan: #C9B99A;
}
```

Three-font system via Google Fonts:
```css
--f-display: 'Bebas Neue', sans-serif;
--f-serif: 'Fraunces', serif;
--f-mono: 'IBM Plex Mono', monospace;
```

### Key JavaScript Features

- **Custom cursor** — `#cursor` div with trail elements; grows on hover over interactive elements
- **Web Audio API** — generates a paper-rustle click sound on each panel snap
- **Typewriter hero** — cycles through 5 phrases with asymmetric type/delete timing
- **Count-up metrics** — numbers animate from 0 with cubic ease-out on scroll entry (IntersectionObserver)
- **Dark/light toggle** — switches `data-theme` on `<html>`, 0.45s CSS transition
- **Snap dot navigation** — 9-dot positional indicator; panel navigation via `scrollBy`
- **Dynamic favicon** — dims and changes title when tab is hidden (Page Visibility API)

### Contact Form

Powered by Formspree (zero backend). The form action URL in `index.html` needs `YOUR_FORM_ID` replaced with a real Formspree form ID.

## Deployment

The site is deployed on Vercel. `vercel.json` sets security headers (CSP-adjacent, HSTS, X-Frame-Options, etc.). No build configuration is needed — Vercel serves `index.html` directly.

GitHub Pages also works by enabling Pages from the `main` branch.

## License

CC BY-NC-ND 4.0 — this code is not a template and may not be copied or redistributed.
