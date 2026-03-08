# Changelog

All notable changes to this portfolio are documented here.
This file serves as a public record of authorship and originality.

Format follows [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).

---

## [2.0.0] — 2025-03-08 — Full Redesign

### Concept
Complete ground-up redesign. Abandoned conventional vertical-scroll
portfolio in favour of a horizontal-scrolling editorial broadsheet.
No framework. No template. Built entirely from scratch.

### Added
- Horizontal scroll engine with physics-based lerp (factor 0.09)
- Panel snap with Web Audio API paper-rustle click sound
- Bebas Neue + Fraunces + IBM Plex Mono three-font editorial system
- Newspaper masthead: Vol. I · Issue 01 · Nagpur, India · 2025
- 7 horizontal panels: Hero, Experience, Skills, Projects, Research, Education, Contact
- Custom red-dot cursor with mix-blend-mode:multiply
- Ghost watermark section numbers in panel backgrounds
- Red bottom progress bar tracking scroll position
- Floating command nav (top-right pill buttons)
- Snap dot navigation (7 dots, bottom center)
- Dark / Light mode with CSS token system and 0.45s transitions
- Typewriter effect cycling 5 phrases with asymmetric timing
- Count-up project metrics triggered on panel entry
- Proficiency bars animated on scroll entry
- Keyboard navigation (0–6 keys, arrow keys)
- Drag, wheel, touch input all supported
- Deep navy panel (#003566) for Research section
- SVG grain texture overlay
- "Currently Building" live status badge with spinning icon
- GitHub source links on every project card
- Formspree-powered contact form (zero backend)
- Full Open Graph + Twitter Card meta tags
- Resume download (generates formatted .txt file client-side)
- Mobile fallback: converts to vertical scroll layout
- CC BY-NC-ND 4.0 license embedded in source code comments

### Design decisions
- Paper palette (#F2EDE4) chosen to evoke aged broadsheet newsprint
- Red (#C1121F) is Pantone 186 C — editorial authority
- Navy (#003566) for Research panel creates tonal drama mid-scroll
- No CSS framework: every rule written by hand for full control
- Single-file architecture: zero build step, instant deploy anywhere

---

## [1.0.0] — 2024-09-01 — Initial Portfolio

### Added
- Dark-theme single-page portfolio
- Cyan accent (#00e5ff) on dark navy background
- Syne + Space Mono + Outfit font stack
- Floating orbs, neural canvas, scan grid animations
- Sections: Hero, About, Experience, Skills, Projects, Research,
  Certifications, Achievements, Education, Leadership, Contact
- Wave bar animations on skills
- Cursor glow effect
- Scroll-reveal animations throughout

---

*© 2025 Harshal Naresh Donarkar. All rights reserved.*
*This changelog is a timestamped record of original authorship.*