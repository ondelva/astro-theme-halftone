# Changelog

All notable changes to this project are documented here. Format: [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

## [0.9.0] - 2026-09-22

First snapshot of the free edition, cut from Halftone Pro. The live demo and the screenshots
follow in 1.0.0.

### Added

- The home cover plate, desk fronts with pagination, the article, the colophon, 404, the feed,
  `robots.txt` and the sitemap.
- Cover lines: the labelled teasers set on a cover plate, on the home cover and every desk front.
- The article rail: figures blocks and what else the desk has filed. The layout branches on
  `format` — report, brief, photo essay — and on nothing else.
- Contributor bios, related reading, reading time, dark mode.
- Share cards: an article's own photograph, cropped and baked at build.
- Analytics (Plausible, GA4, Umami), off until a provider is named.
- UI strings in `src/i18n/`, English and Korean, checked against each other by the type.
- Twenty-five sample photographs, drawn by `scripts/make-sample-plates.mjs` and seeded by slug, so
  the theme carries no stock-photo redistribution terms.
- `README.md`, `docs/customization.md`, `docs/content.md`, `docs/components.md`, `docs/deploy.md`
  and `AGENTS.md`.
