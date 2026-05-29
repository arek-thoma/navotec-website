# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Static single-page portfolio website for Arkadius Thoma (IT Consultant & Software Developer). No build system, no dependencies to install, no compilation step.

## Local Development

Open `index.html` directly in a browser, or serve it with a local HTTP server to avoid CORS issues with external resources:

```powershell
python -m http.server 8000
# or
npx http-server .
```

## Architecture

Everything lives in `index.html` — HTML structure, embedded CSS, and no JavaScript. The `foto.jpg` and `Fotos/` directory contain profile images referenced by the HTML.

**External CDN dependencies (no local install needed):**
- Google Fonts: Playfair Display, Source Sans 3
- Tabler Icons via jsDelivr

**CSS design system (all embedded in `index.html`):**
- CSS custom properties defined in `:root` for the color/spacing system
- Primary accent: `--orange: #BA7517`
- Layout: single centered column, `max-width: 800px`
- Responsive breakpoint: `560px` (mobile)
- Dark mode: `prefers-color-scheme: dark` media query
- Animations: `fadeUp` keyframe with staggered `animation-delay` per section

**Page sections (in order):** nav → hero → about (`#ueber-mich`) → contact (`#kontakt`) → footer

## Known Gaps

- `impressum.html` and `datenschutz.html` are linked in the footer but do not exist yet.
