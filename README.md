# Resume

Static HTML resume and LaTeX PDF for Welliton Scheer. No build system, no JavaScript — just plain HTML and a `.tex` file.

## Tech Stack

- HTML with [Tailwind CSS](https://tailwindcss.com/) (CDN)
- [Font Awesome](https://fontawesome.com/) icons
- [Inter](https://fonts.google.com/specimen/Inter) font (Google Fonts)
- LaTeX for PDF generation

## Project Structure

```
resume/
├── index.html   # Resume website (dark, single-column layout)
├── resume.tex   # LaTeX resume for PDF compilation
├── icon.png     # Favicon
└── README.md
```

## Running Locally

Open `index.html` directly in a browser, or serve it:

```bash
python -m http.server 8000
# Visit http://localhost:8000
```

## PDF Version

`resume.tex` compiles cleanly on [Overleaf](https://www.overleaf.com/) with no special setup. Uses standard LaTeX packages (geometry, hyperref, titlesec, enumitem).

## Keeping in Sync

Both `index.html` and `resume.tex` contain the same resume content. Update both when making changes to experience, projects, skills, education, or open source contributions.
