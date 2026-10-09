# CompactSplat project website

A static academic project page, following SurfSplat's title/authors/resources → teaser → abstract → overview → results → citation structure. The page uses original CompactSplat manuscript figures, with keyboard-accessible resolution switching and citation copying. No build or external JavaScript dependencies are needed.

## Run locally

From the repository root:

```bash
python3 -m http.server 8765 --bind 127.0.0.1 --directory .
```

Open [the local page](http://127.0.0.1:8765/). Files are served only on the local machine.

## Edit

- `index.html`: content, author metadata, native-resolution result table and citation.
- `styles.css`: responsive academic layout.
- `script.js`: resolution-specific manuscript values and copy interaction.
- `assets/`: manuscript figure renderings; provenance is in [SOURCES.md](assets/SOURCES.md).

The native-resolution table in HTML remains readable with JavaScript disabled. When changing the results, keep its values synchronized with `script.js`; retain protocol and provenance notes. Bold values are computed among the displayed rows, including ties.

The result tables report paper values. See the [reproducibility notes](https://github.com/hebing-sjtu/CompactSplat/blob/main/docs/REPRODUCIBILITY.md) for implementation differences and the [model status](https://github.com/hebing-sjtu/CompactSplat/blob/main/MODEL_ZOO.md) for checkpoint availability.

## GitHub Pages

Website repository: https://github.com/hebing-sjtu/CompactSplat-website

Planned website URL: https://hebing-sjtu.github.io/CompactSplat-website/

This repository contains the static website only. The training and evaluation code is maintained in [CompactSplat](https://github.com/hebing-sjtu/CompactSplat).

To publish after approval, enable GitHub Pages with **Deploy from a branch**, branch **main**, folder **/(root)**. The `.nojekyll` file serves these static files directly. No build step, external hosting service, or deployment credential is needed.

GitHub Pages for personal accounts serves a public website, including when a supported plan allows the source repository to remain private. Keep Pages disabled until public website access is approved. The included `noindex` metadata and `robots.txt` discourage indexing; they do not restrict visitors.
