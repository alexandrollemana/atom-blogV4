# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this is

Hugo static site for the "Atom" cybersecurity blog (`at0m.space`). Theme is **PaperMod**, vendored in-tree under `themes/PaperMod/` (not a git submodule — edit/update it directly if needed). Site is deployed to GitHub Pages automatically by `.github/workflows/deploy.yml` on every push to `main`, using Hugo **extended** version pinned to `0.134.2`.

## Common commands

```bash
hugo server -D              # local dev server (includes drafts), http://localhost:1313
hugo                        # build to ./public/
hugo --gc --minify          # production-style build (matches CI)
hugo new blogs/<slug>.md    # new post using archetypes/posts.md template
hugo new <path>.md          # new content using archetypes/default.md
```

There is no test suite, lint step, or `package.json`. CI only runs `hugo --gc --minify --baseURL …`.

## Repository layout (non-obvious bits)

- `config.yml` — site config in YAML (not the more common `hugo.toml`). All site-wide params (profile mode, menu, social icons, fuse.js search options, PaperMod params) live here.
- `content/blogs/` — blog posts. The single existing post is in French; filenames may contain unicode (e.g. `de-zéro-à-la-BSCP-:-mon-parcours-et-mes-astuces.md`).
- `content/about/index.md` — about page (page bundle).
- `archetypes/posts.md` — template applied when creating files under `content/posts/` or via `hugo new posts/...`; defines the standard front matter (slug, category, cover image, showtoc, draft). Note that posts live under `blogs/`, not `posts/`, so the archetype is invoked explicitly via `hugo new blogs/<name>.md` only if you ask for it — otherwise `archetypes/default.md` is used.
- `static/images/`, `static/covers/` — served at site root (`/images/...`).
- `public/` — Hugo build output. Tracked in git in this repo; CI rebuilds and uploads `./public` as the Pages artifact, so committed contents under `public/` are overwritten on deploy.

## Layout override pattern

The root `layouts/` directory shadows `themes/PaperMod/layouts/` file-by-file — Hugo picks the project-root version first. When customizing the theme:

- Prefer adding/overriding a file in `layouts/` (e.g. `layouts/partials/extend_head.html`, `layouts/partials/footer.html`) instead of editing `themes/PaperMod/`.
- `config.yml` enables `markup.goldmark.renderer.unsafe: true`, so raw HTML in Markdown posts is rendered as-is (the existing BSCP post relies on this for inline `<img style=…>`).

## Front matter expectations

Posts use the front matter shape from `archetypes/posts.md`: `title`, `slug`, `category`, `summary`, `description`, `cover.{image,alt,caption,relative}`, `showtoc`, `draft`. PaperMod-specific fields used in `content/Page.md` (TocOpen, hidemeta, disableShare, ShowBreadCrumbs, searchHidden, editPost, etc.) are documented inline in that file and serve as the reference for per-page tweaks.

## Deployment

`.github/workflows/deploy.yml` installs Hugo extended 0.134.2 + Dart Sass, runs `hugo --gc --minify --baseURL <pages-url>/`, and publishes `./public` via `actions/deploy-pages`. Changes only go live after pushing to `main`. Site `baseURL` in `config.yml` is `//at0m.space/`; CI overrides it with the Pages URL at build time.
