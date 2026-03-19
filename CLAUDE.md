# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

A collection of standalone, single-file HTML tools ("vibed tools"). Each tool is a self-contained HTML file with all CSS, JS, and logic inlined — no build system, package manager, or server required. Open any `.html` file directly in a browser to use it.

## Architecture

- **index.html** — Landing page listing all available tools. Deployed via GitHub Pages (see `.github/workflows/pages.yml`). When adding a new tool, add a card entry here.
- **bird-guessing.html** — "Knowledge Tree": an interactive bird species guessing/learning game. Uses Google Fonts (DM Serif Display, DM Sans, JetBrains Mono). Dark-themed UI with CSS custom properties.
- **netcdf-viewer.html** — "NetCDF Climate Viewer": a climate data visualization tool. Depends on CDN-loaded libraries (Leaflet, Plotly.js, chroma-js) with an inlined NetCDF parser. Sidebar + map layout.

## Conventions

- Each tool is entirely self-contained in a single `.html` file — do not split into separate CSS/JS files.
- External dependencies are loaded via CDN `<script>`/`<link>` tags, not npm.
- All tools use a dark color scheme (`#0d1117` background family) with CSS custom properties (`:root` variables).
- No build step, test suite, or linter — test by opening the `.html` file in a browser.
- MIT licensed.

## Deployment

The `main` branch auto-deploys to GitHub Pages via `.github/workflows/pages.yml`. Every file in the repo root is served as-is.
