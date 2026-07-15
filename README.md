# Personal Portfolio

A static, single-page personal portfolio site. Plain HTML, Sass-compiled CSS, and vanilla JS — no framework or bundler.

## Getting started

```bash
npm install
npm start
```

`npm start` runs a live-reloading dev server alongside a Sass watcher.

## Scripts

- `npm run devserver` — serve the site locally with live-server (auto-reload on changes)
- `npm run watch:sass` — watch `sass/main.scss` and recompile to `css/style.css` on change
- `npm start` — run `devserver` and `watch:sass` together (typical dev loop)
- `npm run build:css` — full production CSS build: compile Sass → concat → autoprefix → compress

Before shipping a styling change, run `npm run build:css` so `css/style.css` (the file `index.html` links) is fully regenerated.

## Structure

- `index.html` — single-page markup, organized by `<section id="...">` blocks (`home`, `about`, `experience`, `works`, `contact`)
- `sass/` — Sass source (7-1-pattern-inspired), assembled via `sass/main.scss`
- `css/` — compiled CSS build artifacts (generated, not hand-edited)
- `script.js` — page behavior: loading screen, nav, scroll reveal, works pagination, contact form validation/send
- `img/` — screenshots and icons used across the site

## Sections

- **Home** — header/intro
- **About me**
- **Education & Experience**
- **Recent Works** — project showcase with "show more"/"show less" pagination
- **Contact me** — form that sends mail via [SmtpJS](https://smtpjs.com/)
