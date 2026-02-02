# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Static HTML/CSS website for Anarchy Incubator — an open-source community building platforms for food sovereignty, mutual aid, and disaster relief. No JavaScript, no build tools, no dependencies.

## Development

Serve locally with any static file server:
```
python3 -m http.server 8000
```

No build step, linting, or tests exist. Changes to HTML/CSS files take effect immediately on reload.

## Architecture

- **index.html** — Home/philosophy page (hero, mission, approach, project previews, join CTA)
- **projects.html** — Detailed project showcases (Eggslist, Hatchtrack)
- **seeking.html** — Open roles and recruitment (engineers, designers, marketers)
- **main.css** — Single stylesheet (~1600 lines) containing the full design system, all components, and animations

## Design System (in main.css)

- **Color palette**: Dark purple (`#9B5FCC`) and gold (`#F0C040`) defined as CSS custom properties in `:root`
- **Fonts**: Space Grotesk (headings, WOFF2) and Tomorrow (body, TTF) served from `assets/fonts/`
- **Layout**: CSS Grid and Flexbox, responsive with `clamp()` fluid typography
- **Visual effects**: Solarpunk/space-punk atmospheric CSS — starfield drift, scanline flicker, nebula gradients, dot grid overlays, glitch effects, blob morphing animations
- **Wave dividers**: SVG-based section separators with color variants (warm, cream, moss, charcoal)
- **Organic shapes**: Border-radius values in 30-70% ranges for blob-like card shapes

## Pages share a consistent sticky header with pill-navigation and a footer with GitHub/Discord links.
