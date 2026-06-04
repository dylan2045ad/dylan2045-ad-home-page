# Project Architecture — Dylan From 2045 Hub

## Overview

A zero-dependency, single-file static site. Everything lives in `index.html` with inline CSS.

## Key Files

- `index.html` — the entire site: markup + all styles inline
- `header.jpg` — header image (swap this file to change the hero photo)
- `netlify.toml` — tells Netlify to publish from the repo root

## Design Conventions

- Color palette: `#050a24` background, `#00eaff` cyan, `#ff2bd6` magenta, `#9d5bff` purple
- Neon glow via `text-shadow` and `box-shadow`; no external font or icon libraries
- Buttons: `.btn-m` (magenta), `.btn-c` (cyan), `.btn-p` (purple for book cards)
- All external links use `target="_blank" rel="noopener"`

## Non-obvious Decisions

- The hero `<img>` uses an `onerror` handler to fall back to a "header image" placeholder so the page looks fine before `header.jpg` is replaced.
- No build step — `netlify.toml` sets `publish = "."` so Netlify serves the repo root directly.
