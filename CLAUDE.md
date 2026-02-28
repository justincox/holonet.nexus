# Holonet.Nexus

A static landing page for [holonet.nexus](https://holonet.nexus) — Justin Cox's personal Holonet Channel Guide with a Star Wars sci-fi aesthetic.

## Project Structure

```
index.html   — Single-page app, all markup and JS inline
styles.css   — All styles (versioned via query string in HTML)
CNAME        — GitHub Pages custom domain
```

No build step, no dependencies, no package manager. Plain HTML/CSS/JS deployed via GitHub Pages.

## Architecture

**Static site** — everything lives in `index.html` and `styles.css`.

**Dispatches section** fetches posts from a Ghost CMS instance at `https://justincox.com` using the Content API:
- Latest post: excludes `reviews` and `write-now` primary tags
- Featured post: tagged `featured`, excludes the latest post to avoid duplication, randomly selected from the pool
- API key: `b498ed50fad70b488f50a1fca0` (public Content API key, read-only)
- All HTML built with manual DOM construction + `escapeHtml()` for XSS safety

**Randomized UI elements** on each page load:
- Node ID (e.g. `HN-4B2`, `HN-A-739`) — random alphanumeric format
- Sector name — random pick from Star Wars galaxy regions

**Translation effect** — most visible text uses a dual-span pattern:
```html
<span class="link-copy-source">Text</span>
<span class="link-copy-translation" aria-hidden="true">Text</span>
```
Both spans contain the same text; CSS animates between them for a "decoding" visual effect.

## Styles Versioning

When updating `styles.css`, bump the version query string in `index.html`:
```html
<link rel="stylesheet" href="styles.css?v=YYYYMMDD-N" />
```

## Deployment

Pushes to `main` deploy automatically via GitHub Pages.
