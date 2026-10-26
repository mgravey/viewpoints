# viewpoints

Short, citable viewpoint papers on geoscience, data science, and research practice.

## URL

Published at: `https://www.mgravey.com/viewpoints/`

## Writing model

Each note is a single file in `_topics/`.
Use `_topics/_template.md` to start a new piece.

Required front matter fields:

- `title` (string)
- `slug` (string)
- `topic` (string)
- `summary` (string, 1-2 lines)
- `date` (date)
- `updated` (date, optional)
- `tags` (array of strings, optional)
- `status` (`draft` or `published`; default is `published`)
- `image` (string, optional): site-relative path of the article's first figure, e.g. `/assets/images/viewpoints/clearing-the-path.webp`. Used for `og:image`, the large Twitter card and the JSON-LD `image`.

Drafts are still rendered at their URL, but get `<meta name="robots" content="noindex">` and are left out of the homepage, `sitemap.xml`, `feed.xml`, `llms.txt` and `llms-full.txt`.

## Latest viewpoints

- [Why should we NOT get used to it?](_topics/why-should-we-not-get-used-to-it.md) — Why adapting to unresolved problems can reinforce them, including habitual uses of PCA and p-values.
- [Should a new idea already outperform the state of the art?](_topics/should-a-new-idea-already-outperform-the-state-of-the-art.md) — Why current performance alone is insufficient to reject a research direction or funding proposal.

Both articles are dated 2026-10-09 and marked `published`, so they appear automatically on the homepage and in the topic feed after deployment. Statistical references use DOI links; the PCA example is self-contained.

## Article illustrations

Each of these two articles includes its original painted illustration near the beginning and a schematic alongside the relevant argument. The four selected images were generated with OpenAI's built-in image tool and are stored in `assets/images/viewpoints/` as WebP assets. Paintings use quality 85 compression; schematics use lossless compression to preserve their lettering. No cropping is applied.

The shared `_includes/topic-figure.html` renders responsive images with descriptive alt text, captions, fixed intrinsic dimensions, and links to the full-size assets. Opening illustrations load eagerly; later figures load lazily. Use Jekyll's `relative_url` filter for asset links so they work under `/viewpoints/`.

Image concepts:

- `clearing-the-path.webp`: walkers follow a detour while one person removes the fallen branch.
- `pruning-new-directions.webp`: a gardener cuts young shoots while the main stem reaches a barrier.
- `cycle-of-acceptance.webp`: the problem–workaround–habit cycle and a route through improvement.
- `research-alternatives.webp`: early rejection of alternatives compared with keeping research directions open.

## Search engines and LLMs

All metadata is written by hand in Liquid (no SEO or sitemap gems); it is generated from `_topics/`, so new articles need no extra lists.

- `_includes/seo.html` (included in the `<head>` of `_layouts/default.html`) adds the canonical URL, Open Graph and Twitter tags, Google Scholar `citation_*` tags on articles, and JSON-LD: a `ScholarlyArticle` per article and a `CollectionPage` on the homepage. The author is referenced by `@id` (`https://www.mgravey.com/#person`), which the main site defines; author details live under `author:` in `_config.yml`.
- `sitemap.xml` lists the homepage and every published article. The main site's sitemap index at `https://www.mgravey.com/sitemap.xml` points to it.
- `feed.xml` is a hand-written Atom feed of published articles. It replaces the `jekyll-feed` output, which did not skip `status: draft` (the gem remains in the `Gemfile` but is no longer enabled in `_config.yml`).
- `llms.txt` follows the [llms.txt](https://llmstxt.org) convention: a short description, links to the main site's `llms.txt` and to `llms-full.txt`, and one line per article.
- `llms-full.txt` contains every published article as Markdown, newest first, with its metadata. Figure includes become `[Figure: alt text — caption]` lines (via `figure_format: text`), and the few inline HTML tags used in articles (math spans, `<sub>`, `<sup>`) are converted to plain text. Add a matching replacement there if an article starts using other inline HTML.

## Local preview and deployment

Install the gems with `bundle install`, then run `bundle exec jekyll serve` and open `http://localhost:4000/viewpoints/`.
Run `bundle exec jekyll build` to check the production output in `_site/`.

`Gemfile.lock` includes the `x86_64-linux-gnu` platform so the GitHub runner installs prebuilt `google-protobuf`, `sass-embedded` and `ffi` gems instead of compiling them (compiling `google-protobuf` fails on Ubuntu 26.04). After changing gems, run `bundle lock --add-platform x86_64-linux-gnu` and check that these `-x86_64-linux-gnu` entries are still in the lockfile.

The GitHub Pages workflow builds and deploys pushes to `master`. Adding an article locally does not deploy it.
Generated output, local caches, and the workflow-generated `_config_ci.yml` are ignored by Git.

## Citation and reuse

Please cite the original URL and author when reusing or adapting content.

Content is licensed under **CC BY-SA 4.0**.

- Human-readable summary: <https://creativecommons.org/licenses/by-sa/4.0/>
- Legal code: <https://creativecommons.org/licenses/by-sa/4.0/legalcode>
