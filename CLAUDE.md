# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Static website for the Canarian writer Antolín Dávila, hosted on GitHub Pages. No build tools, bundlers, or JavaScript frameworks — just plain HTML and CSS.

## Architecture

Multi-page site. All content is in **Spanish** with UTF-8 encoding.

- **`index.html`** — Landing page with hero, biography summary, works grid, selected quotes, and contact. Uses Google Fonts (Cormorant Garamond + Manrope) and CSS custom properties for theming.
- **`styles.css`** — All styles in one file. CSS custom properties in `:root` control the palette. Responsive breakpoint at 860px. Inner-page classes: `.page-header`, `.breadcrumb`, `.prose`, `.book-detail`, `.quote-list`, `.nav-books`, `.pub-list`, `.attribution`.
- **`images/`** — All site images (lowercase filenames). Copied from the legacy archive.
- **Content pages:**
  - `biografia.html` — Full biography (merged intro + personal data)
  - `novelas.html` — Index of 9 novels, links to detail pages
  - `cuentos.html` — Index of story collections
  - `radio.html` — Radio programs
  - `frases.html` — 100+ author quotes
  - `esquela.html` — Poetic eulogy
- **Novel detail pages:** `orla.html`, `calle.html`, `cernicalo.html`, `roble.html`, `cabalga.html`, `rosa.html`
- **Story collection pages:** `caudillo.html`, `feria.html`
- **Presentation/review pages:** `presfer.html`, `rosaant.html`, `rosaosv.html`
- **`legacy/`** — Complete archive of the original FrontPage-era website (~2000s). Preserved as-is, not linked from the live site.
- **`.nojekyll`** — Ensures GitHub Pages serves all files without Jekyll processing.

## Deployment

Push to `main` branch. GitHub Pages deploys from root (`/`). No build step required.

## Key Conventions

- Every inner page shares the same nav bar and breadcrumb pattern. When adding a page, follow the template in any existing inner page (e.g., `biografia.html`).
- Novel detail pages include a `.nav-books` section at the bottom for cross-navigation between sibling novels.
- Images use lowercase filenames in `images/` (e.g., `orla.jpg` not `orla.JPG`).
