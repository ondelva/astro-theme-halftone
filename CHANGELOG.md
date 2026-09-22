# Changelog

All notable changes to this project are documented here. Format: [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

## [1.1.0] - 2026-09-22

The demo content is rebuilt around real photographs. The theme's code is unchanged apart from one
config default; what changed is what it is filled with.

### Changed

- **The sample photographs are real pictures of real places**, not drawings. Nineteen of them, under
  public-domain, CC0 or CC BY licences, credited on the plate in `heroCredit` and in full in
  `THIRD-PARTY-NOTICES.md`. Unsplash and similar libraries were ruled out: their terms do not cover
  redistributing the pictures inside a template.
- **The desks are Ports, Transit, Power and Land.** The free licences that allow redistribution are
  strongest on infrastructure, transport, energy and landscape, so the demo magazine was rebuilt on
  that axis rather than filled with weak pictures on the old one.
- **The nineteen articles are new**, written to the photographs. They describe real places, so they
  carry no invented statistics, quotes or officials — the register is observational rather than
  reported.
- `blog.postsPerPage` is `4` instead of `6`, so a five-piece desk still paginates.
- `scripts/make-sample-plates.mjs` now draws the six contributor portraits only. The contributors
  are fictional, and a real face does not belong under an invented byline.

## [1.0.0] - 2026-09-22

First release. The demo is live, and the Pro edition is on sale.

### Added

- The README links to the Pro edition's checkout, with its two prices.

### Changed

- The lead piece on the home cover carries a different sample photograph. The cover plate holds
  its scrim over the left of the frame, so only the band to the right of the type reads as a
  picture — and the old plate had an empty horizon there, which left the cover looking like a
  dark field rather than a photograph.
- The screenshots in `docs/screenshots/` were taken again against this build.

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
