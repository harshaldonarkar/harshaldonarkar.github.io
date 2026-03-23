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

Powered by **Web3Forms** (`https://api.web3forms.com/submit`). The hidden `access_key` input in `index.html` must contain a valid Web3Forms access key. Form submission is handled by `handleForm(event)` in the script block.

### PWA

`manifest.json` and `sw.js` make the site installable. The service worker uses stale-while-revalidate for assets and network-first for API calls (web3forms, workers.dev). The cache name is `hd-portfolio-v1` — bump this in `sw.js` to force cache invalidation after significant updates.

## Deployment

The site is deployed on Vercel. `vercel.json` sets security headers (HSTS, X-Frame-Options, X-Content-Type-Options, Permissions-Policy, etc.). No build configuration is needed — Vercel serves `index.html` directly.

GitHub Pages also works by enabling Pages from the `main` branch.

## License

CC BY-NC-ND 4.0 — this code is not a template and may not be copied or redistributed.
