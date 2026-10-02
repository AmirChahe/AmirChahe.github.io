# CLAUDE.md

This repo is Amirhosein Chahe's personal website (<https://amirchahe.github.io>), created from the al-folio v1.2 template. See [README.md](README.md) for where each piece of content lives.

Differences from the upstream template that override what `AGENTS.md` and `docs/` say:

- `baseurl` is **blank** (user site at the domain root), not `/al-folio`. Build with plain `bundle exec jekyll build`; the dev server is at `http://localhost:4000/`.
- Local overrides of theme files are allowed here (this is a user site, not the template repo). Current override: `_includes/news.liquid` (dates as `%b %Y`).
- `test/` and all CI workflows except `.github/workflows/deploy.yml` were removed, so the template's integration tests, style-contract lint and visual tests do not apply.

`AGENTS.md`, `docs/ARCHITECTURE.md` and `docs/BOUNDARIES.md` still describe how the al-folio gems fit together.
