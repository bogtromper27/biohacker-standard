# Biohacker Standard — Website

Multi-page marketing + content site for **biohackerstandard.com** — an independent research and education brand covering peptides, longevity, and human performance.

## Pages

| File | Purpose |
| --- | --- |
| `index.html` | Home — lead-capture hero (COA Literacy Guide opt-in), social follows (Instagram / Discord / X / TikTok), "who we are", blog teasers |
| `blog.html` | Blog index — featured post, category + sort filters, article grid, newsletter signup |
| `directory.html` | Vetted directory — search, category filters, verified brand/expert cards |
| `styles.css` | Shared design system (see below) |

## Design system — "Standard Bearer" colorway

- **Neutrals:** graphite ink `#15191B` on warm lab-paper `#F3F2EC`
- **Primary:** deep pine `#1D5A43`
- **Secondary:** brass `#AE8B4E` (warm contrast accent)
- **Type:** Archivo (display) · Hanken Grotesk (body) · IBM Plex Mono (labels/data), via Google Fonts

Accent CSS variables keep legacy `--blue*` / `--gold*` names for compatibility: `--blue` = pine, `--gold` = brass.

## Status

Static site, no build step. The email capture form currently shows a **mock success state** — it is not yet wired to FluentCRM. Wiring target: `POST /wp-json/fluent-crm/v2/public/forms/{ID}/submit`. The dark molecular panels are **image slots** ready to be replaced with photography.

## Local preview

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000 — or just open `index.html` directly in a browser.

## Deploying

This repo is **private**. GitHub Pages for a private repo requires a paid GitHub plan (Pro/Team/Enterprise); on a free plan the repo must be public for Pages to serve. The eventual production home is WordPress on biohackerstandard.com; GitHub is the source of truth for the design/code.
