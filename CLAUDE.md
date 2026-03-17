# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

Personal academic portfolio website for Rom Himelstein, hosted on GitHub Pages (`wr0om.github.io`). Plain static site — no build process, no package manager, no framework, no JavaScript.

## Development

**To preview locally:** open `index.html` directly in a browser, or use any static file server:
```
python3 -m http.server 8000
```

**Deployment:** pushing to `main` automatically publishes via GitHub Pages. No build step needed.

## Architecture

Two files contain all the code:
- `index.html` — entire page structure and content
- `style.css` — all styling via CSS custom properties (dark theme, Inter font, 800px max-width)

Images live in `images/` (profile photo) and `images/papers/` (paper thumbnails named `paper1.png` through `paper6.jpg`).

## Page Structure

`index.html` is divided into five sections with matching nav anchor IDs:
1. `#hero` — name, profile photo, bio, social links
2. `#about` — research background and affiliations
3. `#publications` — paper cards (thumbnail + venue + title + authors + links)
4. `#talks` — talk/appearance entries
5. `#contact` — footer with social links

## Content Conventions

**Publication cards** follow this pattern: thumbnail image → venue badge → paper title → author list → arXiv/ACL Anthology links.

**Paper thumbnails** are named sequentially (`paper1.png`, `paper2.png`, ...) and should be added to `images/papers/`. Add `loading="lazy"` on `<img>` tags for thumbnails.

**Social/external links** used throughout: GitHub (`wr0om`), Google Scholar, LinkedIn, Email (`romhim@campus.technion.ac.il`), arXiv, ACL Anthology.
