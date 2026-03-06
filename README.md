# Resume

Svelte 5 carousel resume and portfolio for Welliton Scheer. Built with Vite, Tailwind CSS v4, and deployed on Cloudflare Pages.

## Tech Stack

- [Svelte 5](https://svelte.dev/) + [Vite](https://vitejs.dev/) (single-page static site)
- [Tailwind CSS v4](https://tailwindcss.com/) via `@tailwindcss/vite`
- [Font Awesome](https://fontawesome.com/) icons
- [Inter](https://fonts.google.com/specimen/Inter) font (Google Fonts)
- LaTeX for PDF generation

## Project Structure

```
resume/
├── src/
│   ├── App.svelte                  # Root component
│   └── lib/
│       ├── Carousel.svelte         # Carousel logic (arrows, dots, swipe, keyboard)
│       └── slides/
│           ├── HeaderAbout.svelte
│           ├── Experience.svelte
│           ├── OpenSource.svelte
│           ├── Projects.svelte
│           ├── Technologies.svelte
│           └── Education.svelte
├── public/
│   └── icon.png                    # Favicon
├── resume.tex                      # LaTeX resume for PDF compilation
├── index.html
├── vite.config.js
└── package.json
```

## Running Locally

```bash
npm install
npm run dev       # Start dev server
npm run build     # Build to dist/
npm run preview   # Preview production build
```

## Deployment

Hosted on [Cloudflare Pages](https://pages.cloudflare.com/). Build command: `npm run build`, output directory: `dist`.

## PDF Version

`resume.tex` compiles cleanly on [Overleaf](https://www.overleaf.com/) with no special setup. Uses standard LaTeX packages (geometry, hyperref, titlesec, enumitem).

## Keeping in Sync

The Svelte slide components (`src/lib/slides/`) and `resume.tex` contain the same resume content. Update both when making changes to experience, projects, skills, education, or open source contributions.
