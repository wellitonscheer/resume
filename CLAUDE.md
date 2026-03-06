# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

A Svelte 5 carousel resume/portfolio for Welliton Scheer. Built with Vite, Tailwind CSS v4, and deployed on Cloudflare Pages.

## Commands

```bash
npm run dev      # Start dev server
npm run build    # Build to dist/
npm run preview  # Preview production build
```

## Architecture

- **Svelte 5 + Vite** — Plain Svelte (not SvelteKit), single-page static site
- **Tailwind CSS v4** — Installed via npm with `@tailwindcss/vite` plugin
- **Carousel UI** — 6 slides navigated with arrows, keyboard, touch swipe, and dot indicators. Horizontal on desktop, vertical on mobile. Infinite loop.
- **`src/App.svelte`** — Root component, dark bg, mounts Carousel
- **`src/lib/Carousel.svelte`** — Core carousel logic: transforms, arrows, dots, swipe, keyboard nav
- **`src/lib/slides/*.svelte`** — 6 pure presentational slide components (HeaderAbout, Experience, OpenSource, Projects, Technologies, Education)
- **`resume.tex`** — LaTeX resume for Overleaf/PDF compilation. Same content as the website.
- **`public/icon.png`** — Favicon

## Key Conventions

- Svelte 5 runes (`$state`, `$derived`, `$props`) — no legacy reactive syntax
- Styling uses Tailwind utility classes directly in markup
- The LaTeX version must be kept in sync when resume content changes
- Cloudflare Pages: build command `npm run build`, output directory `dist`
