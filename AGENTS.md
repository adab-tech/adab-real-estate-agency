# AGENTS.md

## Cursor Cloud specific instructions

This repo is a fully static brand-kit/website for **Adab Real Estate Agency**. There is
**no package manager, build step, lint config, or test suite** — it is plain HTML/CSS/SVG/PNG
plus one vanilla-JS config file (`assets/brand/site-config.js`).

- **Run (dev):** serve the repo root over HTTP so relative asset paths resolve, e.g.
  `python3 -m http.server 8000` from `/workspace`, then open `http://localhost:8000/`.
  Opening `index.html` via `file://` also works but HTTP is preferred.
- **Build:** none. Nothing to compile or bundle.
- **Lint / Test:** none configured. There are no automated checks to run.
- **Core functionality:** `index.html` is the brand hub linking to print templates in
  `assets/templates/` (business card, letterhead). Those templates pull contact details at
  runtime from `assets/brand/site-config.js` (`window.ADAB_SITE`), so editing that file is the
  intended way to change phone/email/website everywhere. Templates are designed to be printed
  to PDF (Ctrl/Cmd+P → Save as PDF).
- **External dependency:** Google Fonts CDN is loaded for display fonts; it is cosmetic only and
  the pages fall back to system fonts when offline.
