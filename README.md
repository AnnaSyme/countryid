# Country ID — "What country is it?"

A single-file, faceted GeoGuessr / OpenGuessr country finder. You observe a clue
(script, road lines, driving side, bollard, camera car, region, landscape,
hemisphere), the tool narrows the candidate countries, and you drill down to an
answer with per-country tells.

Live: **annasyme.com/countryid**

## What's in this repo

- `index.html` — the entire app. Self-contained: all HTML, CSS, JS, the icon set,
  and the country data are inline. **This is the only file you need to host.**
- `README.md` — this file.
- `LICENSE` — MIT.

There are **no build steps and no local assets**. The one external dependency is
Google Fonts (loaded from `fonts.googleapis.com` at runtime, for non-Latin scripts
like Khmer, Thai, Tibetan, etc.).

## Hosting

Published with GitHub Pages from the `main` branch (root). Because `annasyme.com`
is the custom domain on the `AnnaSyme.github.io` user site, this project repo is
served under it at **annasyme.com/countryid**.

To update the live site, edit `index.html` and:

    git add index.html
    git commit -m "Update country finder"
    git push

Pages rebuilds in ~1 minute.

## Editing later

Everything lives in `index.html`. The data lives in three inline JS consts near
the top of the `<script>` block:

- `ICONS` — inline SVG icon library.
- `CO` — per-country detail pages (name, flag, links, signature tells).
- `ATTR` — per-country structured attributes used to narrow candidates (script,
  drive side, road-line colour, region, hemisphere, terrain, bollard, car).

The Feedback button (`id="fbBtn"`) opens an email to a masked Fastmail address.
