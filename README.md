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

## Changelog

### 2026-02-28 | 1.3 | The Documentation Cleanup Edit
- Added the project README with the site overview, stack notes, and file inventory.
- Removed the repo-local `CLAUDE.md` so the project documentation lives in the standard README.

### 2026-02-11 | 1.2 | The Translation Interface Edit
- Added the decoding-style translation treatment for dispatch titles, excerpts, and outpost card copy.
- Updated supporting link copy for the website, book, newsletter, and social relays.
- Added reduced-motion handling for the translation effect and refreshed the stylesheet version stamp.

### 2026-02-06 | 1.1 | The Featured Dispatch and Randomization Edit
- Expanded the dispatch panel from a single latest post card to a latest-and-featured stack powered by the Ghost Content API.
- Added random featured-post selection from the `featured` tag archive.
- Refined the node and sector randomization logic plus related landing-page spacing and dispatch styling.

### 2026-02-03 | 1.0 | Initialization
- Launched the static Holonet landing page with custom Womprat and Aurebesh fonts, core layout styling, and GitHub Pages domain setup.
- Added the primary outpost and social relay card structure plus the original latest-dispatch feed integration.
- Added Mastodon verification metadata and the first pass of the Star Wars-themed landing-page presentation.
