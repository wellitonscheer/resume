# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

A static HTML resume/portfolio for Welliton Scheer. No build system, no package manager — just plain HTML and a LaTeX file for PDF generation.

## Running Locally

```bash
python -m http.server 8000
# Visit http://localhost:8000
```

Or open `index.html` directly in a browser.

## Architecture

- **`index.html`** — Dark, minimal resume website. Tailwind CSS (CDN), Font Awesome icons, Inter font. No JavaScript, no animations. Single-column layout on `bg-gray-950`.
- **`resume.tex`** — LaTeX resume for Overleaf/PDF compilation. Same content as the website. Uses standard packages (geometry, hyperref, titlesec, enumitem).
- **`icon.png`** — Favicon for the website.

## Key Conventions

- Styling in `index.html` uses Tailwind utility classes directly in HTML. No custom CSS classes beyond the font-family declaration.
- The LaTeX version is designed to compile cleanly on Overleaf with no special setup.
- Both files must be kept in sync when resume content changes (experience, projects, skills, education, open source contributions).
