# HL7 Lithuania Registry — website

Source for **[hl7.lt](https://hl7.lt)** — the national hub for HL7® FHIR®
Implementation Guides, terminology resources, and community collaboration for Lithuania.

The site is generated from Markdown with **[mdbook](https://github.com/igorboss/mdbook)**
(a VitePress-based static-site generator) and published to GitHub Pages.

## Pages

Content lives under [`source/`](../source) (set via `source.root` in the config):

| File | Route | Purpose |
|---|---|---|
| `source/README.md` | `/` | Home |
| `source/build.md` | `/build` | FHIR Implementation Guide builds |
| `source/terminology.md` | `/terminology` | Code systems, value sets, concept maps |
| `source/community.md` | `/community` | Community & how to contribute |
| `source/lt/*.md` | `/lt/…` | Lithuanian translations |

Images live in `source/.gitbook/assets/`; site configuration (title, nav, footer,
theme, locales) is in [`.mdbook/config.yml`](../.mdbook/config.yml).

> **Note:** the site home (`/`) is `source/README.md` — mdbook's GitBook format uses the
> `README.md` at the source root as the landing page (the default locale lives at the
> root, other locales under `source/<lang>/`). *This* file (`.github/README.md`) is the
> repository's README and is **not** part of the published site.

## Local development

Requires Node ≥ 20.

```bash
# live-reload dev server
npx github:igorboss/mdbook dev --project .

# one-off build to .mdbook/dist
npx github:igorboss/mdbook build --project .
```

## Deployment

Every push to `main` runs [`.github/workflows/mdbook.yml`](workflows/mdbook.yml), which
builds the site and deploys it to GitHub Pages. The workflow pins a released mdbook
version (e.g. `igorboss/mdbook@v1.1.0`).

> ⚠️ **Do not add a `CNAME` file or set a Pages custom domain.**
> `hl7.lt` is served by a **reverse proxy** that pulls from the GitHub Pages origin
> (`hl7lt.github.io`). Setting a Pages custom domain makes the origin redirect to the
> proxy host, causing an `https`↔`http` redirect loop. Keep the Pages **custom domain
> empty** and the repo **without a `CNAME` file**.

## Editing content

Pages are plain Markdown with a few mdbook extras — card grids (`{.card-grid}`),
callout blockquotes (`> … {.is-info}`), and more. Add a page by creating its `.md` file
under `source/` and linking it from [`source/SUMMARY.md`](../source/SUMMARY.md); add its
Lithuanian version under `source/lt/`. See the
[mdbook documentation](https://github.com/igorboss/mdbook) for the full syntax.

## License

Licensed under the terms in [`LICENSE`](../LICENSE).
