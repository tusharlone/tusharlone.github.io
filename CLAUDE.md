# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This is a static personal academic website for Tushar Lone, hosted via GitHub Pages at tusharlone.github.io. There is no build system, bundler, or framework — it is plain HTML/CSS served directly.

## Development

No build, test, or lint commands. Open any `.html` file directly in a browser to preview. The site is deployed automatically by GitHub Pages from the `main` branch.

## Architecture

- **Layout**: Bootstrap 5.3 grid (`container` > `row` > `col-md-1` sidebar + `col-md-11` content). Every page repeats this structure with a fixed left sidebar navigation.
- **Styling**: `styles.css` is the single shared stylesheet, loaded after Bootstrap. The `Inter` font is loaded from Google Fonts. The sidebar uses a gradient highlight (`linear-gradient`) for the active page via the `class="current"` marker.
- **Responsive behavior**: The sidebar collapses to a horizontal top bar at `<=700px` and stacks vertically at `<=400px` (media queries in `styles.css`).
- **Navigation**: Each HTML page has its own copy of the sidebar nav. The `class="current"` attribute must be set on the correct `<a>` tag in each page. When adding a new page, update the sidebar in **all** existing pages.
- **Assets**: `img/` for photos and social logos, `ico/` for skill/tool icons and the favicon.
- **External links** use `target="_blank"` throughout.

## Pages

- `index.html` — Home (intro, profile photo, contact, social links)
- `bio.html` — Education, employment history, workshops, awards
- `publications.html` — Conference and journal papers
- `projects.html` — Research projects (InventOpt, SupplyNetPy)
- `teaching.html` — TA history at IIT Goa and teaching at prior institutions
