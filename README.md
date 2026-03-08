# Harshal Donarkar — Portfolio

<div align="center">

![Portfolio Banner](https://img.shields.io/badge/Harshal%20Donarkar-AI%20Engineer-C1121F?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI+PHBhdGggZmlsbD0id2hpdGUiIGQ9Ik0xMiAyQTEwIDEwIDAgMCAwIDIgMTJhMTAgMTAgMCAwIDAgMTAgMTAgMTAgMTAgMCAwIDAgMTAtMTBBMTAgMTAgMCAwIDAgMTIgMnptMCAxOGE4IDggMCAwIDEtOC04IDggOCAwIDAgMSA4LTggOCA4IDAgMCAxIDggOCA4IDggMCAwIDEtOCA4eiIvPjwvc3ZnPg==)

[![License: CC BY-NC-ND 4.0](https://img.shields.io/badge/License-CC%20BY--NC--ND%204.0-lightgrey.svg?style=flat-square)](https://creativecommons.org/licenses/by-nc-nd/4.0/)
[![Built with](https://img.shields.io/badge/Built%20with-Vanilla%20HTML%2FCSS%2FJS-F2EDE4?style=flat-square&labelColor=0D0D0D)](https://github.com/harshaldonarkar/portfolio)
[![Status](https://img.shields.io/badge/Status-Live-16a34a?style=flat-square)](https://harshaldonarkar.dev)
[![PRs](https://img.shields.io/badge/PRs-Not%20Accepted-C1121F?style=flat-square)](./CONTRIBUTING.md)

**A one-of-a-kind horizontal-scrolling editorial portfolio for Harshal Naresh Donarkar.**

[View Live](https://harshaldonarkar.dev) · [Report a Bug](https://github.com/harshaldonarkar/portfolio/issues) · [Contact Me](mailto:harshaldonarkar@gmail.com)

</div>

---

## ⚠️ COPYRIGHT NOTICE — READ BEFORE USING

> **This portfolio and all its source code, design, layout, typography choices, animations, colour schemes, and written content are the exclusive intellectual property of Harshal Naresh Donarkar.**
>
> This work is licensed under [Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International (CC BY-NC-ND 4.0)](./LICENSE).
>
> **You may NOT:**
> - Copy, clone, or reproduce this design for personal or commercial use
> - Use this code as a template or boilerplate for another portfolio
> - Deploy a modified or unmodified version of this project
> - Redistribute or sublicense this work in any form
>
> **If you were inspired by this work** and wish to credit it, you must clearly state:
> *"Design inspired by [Harshal Donarkar](https://harshaldonarkar.dev)"*
> in a visible location on your project.
>
> Violations will be pursued under the DMCA and applicable copyright law.

---

## 🗞️ About This Portfolio

This is not a template. Every pixel, interaction, and line of code was deliberately crafted for **Harshal Donarkar** — an AI Engineer specialising in Deep Learning, Computer Vision, and Production ML Systems.

### What makes it unique

| Feature | Description |
|---|---|
| **Horizontal Broadsheet Layout** | Scrolls sideways like unrolling a newspaper — no framework, pure CSS |
| **Editorial Typography** | Bebas Neue + Fraunces + IBM Plex Mono — three-font system with intentional tension |
| **Panel Snap with Sound** | Web Audio API generates a paper-rustle click on each panel snap |
| **Typewriter Hero** | Cycles through 5 phrases with asymmetric type/delete timing |
| **Count-Up Metrics** | Project numbers animate from 0 with cubic ease-out on scroll entry |
| **Dark / Light Mode** | Full CSS token system with 0.45s theme transitions |
| **Contact Form** | Formspree-powered, zero backend required |
| **Open Graph Ready** | Full OG + Twitter Card meta tags for rich social previews |
| **Snap Dot Navigation** | 7-dot positional indicator + floating command nav |

---

## 🚀 Running Locally

This is a **single-file** portfolio. No build tools, no npm, no dependencies.

```bash
# Clone the repo
git clone https://github.com/harshaldonarkar/portfolio.git

# Open directly — that's it
open index.html
```

Or serve locally with any static server:

```bash
# Python
python3 -m http.server 8080

# Node (npx)
npx serve .
```

Then visit `http://localhost:8080`.

---

## 🌐 Deploying

### Netlify (recommended — free)
1. Go to [netlify.com](https://netlify.com)
2. Drag the `index.html` file onto the deploy zone
3. Your site is live in seconds

### GitHub Pages
1. Push to a `gh-pages` branch or enable Pages from `main`
2. Your site is live at `https://harshaldonarkar.github.io/portfolio`

### Vercel
```bash
npx vercel --prod
```

---

## ✉️ Activating the Contact Form

1. Create a free account at [formspree.io](https://formspree.io)
2. Create a new form and copy your Form ID (looks like `xpzgkrbd`)
3. In `index.html`, find this line:
   ```html
   <form action="https://formspree.io/f/YOUR_FORM_ID"
   ```
4. Replace `YOUR_FORM_ID` with your actual ID
5. Done — no backend, no server needed

---

## 🔗 Updating GitHub Links

Each project card has a `"View Code"` link. To update:

```html
<!-- Find each pj-gh anchor and update href -->
<a href="https://github.com/harshaldonarkar/YOUR-REPO" class="pj-gh">
```

---

## 🎨 Customisation Guide (for the author only)

### Changing the "Currently Building" badge
```html
<div class="building-badge">
  <span class="building-icon">⚙</span>
  Currently building: YOUR TEXT HERE
</div>
```

### Updating colour tokens
All colours live in `:root` and `[data-theme="dark"]` at the top of the `<style>` block:
```css
:root {
  --red: #C1121F;    /* accent colour */
  --blue: #003566;   /* research panel */
  --paper: #F2EDE4;  /* background */
  --ink: #0D0D0D;    /* text */
}
```

### Swapping fonts
Replace the Google Fonts `<link>` in `<head>` and update:
```css
--f-display: 'Bebas Neue', sans-serif;
--f-serif: 'Fraunces', serif;
--f-mono: 'IBM Plex Mono', monospace;
```

---

## 📁 File Structure

```
portfolio/
├── index.html          ← Entire portfolio (single file)
├── README.md           ← This file
├── LICENSE             ← CC BY-NC-ND 4.0
├── CONTRIBUTING.md     ← Contribution policy
├── SECURITY.md         ← Security & DMCA policy
├── .htaccess           ← Hotlink protection & headers
└── .github/
    └── ISSUE_TEMPLATE/
        └── bug_report.md
```

---

## 📊 Tech Stack

| Layer | Technology |
|---|---|
| Markup | HTML5 (semantic) |
| Styling | CSS3 (custom properties, grid, flexbox, animations) |
| Scripting | Vanilla JavaScript (ES6+) |
| Fonts | Google Fonts (Bebas Neue, Fraunces, IBM Plex Mono) |
| Sound | Web Audio API |
| Form | Formspree (free tier) |
| Hosting | Netlify / GitHub Pages / Vercel |

Zero dependencies. Zero frameworks. Zero build step.

---

## 📬 Contact

**Harshal Naresh Donarkar**
AI Engineer · Deep Learning · Computer Vision

- 📧 [harshaldonarkar@gmail.com](mailto:harshaldonarkar@gmail.com)
- 💼 [linkedin.com/in/harshal-donarkar](https://linkedin.com/in/harshal-donarkar)
- 🐙 [github.com/harshaldonarkar](https://github.com/harshaldonarkar)
- 🌐 [harshaldonarkar.dev](https://harshaldonarkar.dev)

---

<div align="center">

**© 2025 Harshal Naresh Donarkar. All rights reserved.**

*Designed & built from scratch. Not a template. Not for redistribution.*

</div>