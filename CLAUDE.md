# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working in this repository.

## Project

The personal site for **Chidi Oparah, Fractional CTO** — live at **chidioparah.com** (see `CNAME`). Positioning centres on the 6E Method™ and a 25+ year enterprise track record. British English throughout.

## Architecture

- **Static HTML, no build step.** Each page is a self-contained `.html` file with inline `<style>` and `<script>` — there is no shared `menu.js`/`app.js` and no framework. Nav and styling are duplicated per page, so a global change (e.g. a nav link) must be applied to each page.
- **Pages:**
  - `index.html` — home / landing
  - `chidi-oparah.html` — about / bio
  - `contact.html` — contact
  - `rvelate-sample.html`, `rvelate-sample-purple.html` — design samples
- **Assets:** `chidi-photo.jpg`, `chidi photo gemini.png`, PDFs (CV, certificates) live in the root.
- **`bmad/`** is a separate sub-project with its own `bmad/claude.md` — do not mix its conventions with the main site.

## Running locally

No server strictly required (pages are self-contained), but to preview as deployed:

```bash
python3 -m http.server 8080
# then open http://localhost:8080
```

## Deployment

Pushes to `main` auto-deploy to GitHub Pages via `.github/workflows/static.yml`. The **entire repository root is published as-is**, so keep stray/working files out of root or expect them to ship.

## Conventions

- Use **British English** spelling (optimise, colour, behaviour, licence).
- Preserve trademark glyphs: 6E Method™, Rvelate™.
- Keep SEO/OG/Twitter meta tags in each page's `<head>` accurate and in sync with content.
- Match the existing inline style/structure of the page you're editing.

## Workflow

- When the user asks to add or update TODOs, edit `TODO.md`.
- Commit **and push** after completing changes (default branch is `main`, which auto-deploys).
