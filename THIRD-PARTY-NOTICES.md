# Third-Party Notices

This theme bundles the following third-party assets. Each is used under its own license.
Update this file whenever an asset is added or removed.

| Asset             | Type  | Source                                              | License | Notice / attribution                            |
| ----------------- | ----- | --------------------------------------------------- | ------- | ----------------------------------------------- |
| Spectral          | Font  | https://fonts.google.com/specimen/Spectral          | OFL 1.1 | Copyright The Spectral Project Authors          |
| Schibsted Grotesk | Font  | https://fonts.google.com/specimen/Schibsted+Grotesk | OFL 1.1 | Copyright The Schibsted Grotesk Project Authors |
| IBM Plex Mono     | Font  | https://fonts.google.com/specimen/IBM+Plex+Mono     | OFL 1.1 | Copyright IBM Corp.                             |
| Lucide            | Icons | https://lucide.dev                                  | ISC     | Copyright (c) Lucide Contributors               |

The three faces the theme is set in — Spectral, Schibsted Grotesk and IBM Plex Mono — are served by
the Astro fontsource provider at build time (`fonts:` in `astro.config.mjs`), latin subset. Nothing
is fetched from a CDN at runtime.

Sample content — the magazine, its desks, its articles, its contributors and its editor — is
fictional. The sample photographs are **not stock**: all twenty-five are drawn by
`scripts/make-sample-plates.mjs`, seeded by article slug, and carry no third-party terms. Replacing
them with photographs of your own is the expected first step, and the script stays in the repository
so you can draw a stand-in when one is missing.
