# Holonet.Nexus

Personal landing page for [holonet.nexus](https://holonet.nexus) — a Star Wars-themed Holonet Channel Guide for Justin Cox.

## What it does

- Displays the latest and a randomly selected featured post fetched from [JustinCox.com](https://justincox.com) via the Ghost Content API
- Links to primary outposts (website, book, newsletter) and social relays (Mastodon, Instagram, LinkedIn)
- Randomizes a node ID and galaxy sector on each page load
- Animates visible text through a "decoding" translation effect

## Stack

Plain HTML, CSS, and vanilla JS. No build step, no dependencies. Deployed via GitHub Pages on push to `main`.

## Files

| File | Purpose |
|------|---------|
| `index.html` | All markup, inline scripts, and Ghost API logic |
| `styles.css` | All styles (versioned via query string) |
| `CNAME` | Custom domain for GitHub Pages |
