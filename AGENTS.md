# AGENTS.md

## What this repo is

Static HTML knowledge base (startup/growth notes in Italian). Deployed to GitHub Pages with **no build step** — HTML files are served directly.

## Structure

- `index.html` — main index linking into `docs/`
- `docs/` — content HTML pages (`startup-notes.html`, `notes.html`)
- `raw/`, `sidebusiness/`, `startup/` — source material, **all gitignored** (exist locally only, never committed)

## Tech stack

- Static HTML + Tailwind CSS loaded via `<script src="https://cdn.tailwindcss.com">` (CDN, no compilation)
- Google Fonts (Inter, Playfair Display) loaded externally
- No package.json, no bundler, no linting, no tests

## Deployment

- Push to `main` triggers `.github/workflows/static.yml`
- GitHub Pages serves the repo root as-is — no build artifact, no Jekyll
- Any HTML change merged to `main` goes live immediately

## Editing conventions

- All content is in Italian
- New documents: add HTML file to `docs/`, then add a card link in `index.html` following the existing `.doc-card` pattern
- Styling: use Tailwind utility classes inline (custom theme config is in `index.html` `<script>` block)
- Color palette: `stone-*` neutrals, `brand-accent` (#d97706 amber), `brand-light` (#fef3c7)
- License: CC BY-NC-SA 4.0