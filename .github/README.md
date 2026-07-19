# HL7 Lithuania Registry — website

Source for **[hl7.lt](https://hl7.lt)** — the national hub for HL7® FHIR®
Implementation Guides, terminology resources, and community collaboration for Lithuania.

The site is generated from Markdown with **[mdbook](https://github.com/helex-solutions/mdbook)**
(a VitePress-based static-site generator) and published to GitHub Pages.

## Content (TermX format)

The site uses mdbook's **TermX** layout under [`source/`](../source):

- [`source/space.json`](../source/space.json) — space metadata (names, languages, default lang, site URL).
- [`source/pages.json`](../source/pages.json) — the page tree; each page lists one `contents` entry per language (`name`, `slug`, `lang`).
- `source/pages/<slug>.md` — page markdown, **one file per language content** (each language has its own slug).
- `source/attachments/img/` — images, referenced as `/attachments/img/<file>`.

| Page | EN slug → route | LT slug → route |
|---|---|---|
| Home | `home` → `/` | `pradzia` → `/lt/` |
| Builds | `build` → `/build` | `versijos` → `/lt/versijos` |
| Terminology | `terminology` → `/terminology` | `terminologija` → `/lt/terminologija` |
| Community | `community` → `/community` | `bendruomene` → `/lt/bendruomene` |

Site configuration (title, nav, footer, theme, per-locale menu) is in
[`.mdbook/config.yml`](../.mdbook/config.yml).

> **Note:** TermX uses a distinct slug per language, so Lithuanian routes are localized
> (`/lt/versijos`, not `/lt/build`). Prose uses `breaks: true` (single newline → `<br>`),
> so keep each paragraph on one line. *This* file (`.github/README.md`) is the repository's
> README and is **not** part of the published site.

## Local development

Requires Node ≥ 20.

```bash
# live-reload dev server
npx github:helex-solutions/mdbook dev --project .

# one-off build to .mdbook/dist
npx github:helex-solutions/mdbook build --project .
```

## Deployment

Every push to `main` runs [`.github/workflows/mdbook.yml`](workflows/mdbook.yml), which
builds the site and deploys it to GitHub Pages. The workflow pins a released mdbook
version (e.g. `helex-solutions/mdbook@v1.1.0`).

> ⚠️ **Do not add a `CNAME` file or set a Pages custom domain.**
> `hl7.lt` is served by a **reverse proxy** that pulls from the GitHub Pages origin
> (`hl7lt.github.io`). Setting a Pages custom domain makes the origin redirect to the
> proxy host, causing an `https`↔`http` redirect loop. Keep the Pages **custom domain
> empty** and the repo **without a `CNAME` file**.

## Editing content

Pages are plain Markdown with a few mdbook extras — card grids (`{.card-grid}`),
callout blockquotes (`> … {.is-info}`), and more. To add a page: create
`source/pages/<slug>.md` for each language, add a node to
[`source/pages.json`](../source/pages.json) with its per-language `contents`, and (for a
new top-level menu entry) update `nav`/`locales` in the config. See the
[mdbook documentation](https://github.com/helex-solutions/mdbook) for the full syntax.

## License

Licensed under the terms in [`LICENSE`](../LICENSE).
