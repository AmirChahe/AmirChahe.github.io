# amirhoseinch.github.io

Personal academic website of **Amirhosein Chahe**, Ph.D. student in Electrical Engineering at Drexel University.

Live at <https://amirhoseinch.github.io>. Built with Jekyll from the [al-folio](https://github.com/alshedivat/al-folio) template (v1.2).

## Updating the site

Every push to `main` runs the **Deploy site** GitHub Action, which builds the site and publishes it to the `gh-pages` branch (GitHub Pages serves from that branch).

| To change                       | Edit                                                                          |
| ------------------------------- | ----------------------------------------------------------------------------- |
| Bio, photo caption, home layout | `_pages/about.md`                                                             |
| Profile photo                   | `assets/img/prof_pic.jpg`                                                     |
| Publications                    | `_bibliography/papers.bib` (thumbnails in `assets/img/publication_preview/`)  |
| News on the home page           | add a file to `_news/` (copy an existing one and change `date` and the text)  |
| Web CV (`/cv/`)                 | `_data/cv.yml`                                                                |
| Downloadable CV PDF             | `assets/pdf/Amirhosein_Chahe_CV.pdf`                                          |
| Email / GitHub / Scholar icons  | `_data/socials.yml`                                                           |
| Venue badge colors              | `_data/venues.yml`                                                            |
| Site title, SEO, feature flags  | `_config.yml`                                                                 |

### Publication entries

Besides the usual BibTeX fields, `papers.bib` supports these al-folio fields:

- `abbr` – venue badge (colors in `_data/venues.yml`)
- `selected = {true}` – also show the paper on the home page
- `preview` – thumbnail file name in `assets/img/publication_preview/`
- `arxiv`, `pdf`, `html`, `code`, `website`, `video`, `poster`, `slides` – link buttons
- `abstract`, `bibtex_show = {true}` – expandable abstract and BibTeX
- `award`, `award_name` – award button

## Local preview (optional)

With Docker:

```bash
docker compose up
```

then open <http://localhost:8080>. Without Docker you need Ruby 3.3, Bundler, Node.js and ImageMagick (`bundle install && npm ci && bundle exec jekyll serve`). See [docs/INSTALL.md](docs/INSTALL.md).

## Local customizations

- `_includes/news.liquid` overrides the theme's news list to show dates as month and year.
- Template demo content, the al-folio maintainers' CI workflows, and the blog/projects/teaching pages were removed. To bring a feature back, copy it from the al-folio v1.2 template.

More customization docs: [docs/CUSTOMIZE.md](docs/CUSTOMIZE.md) and [docs/FAQ.md](docs/FAQ.md).
