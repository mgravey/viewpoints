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

## Latest viewpoints

- [Why should we NOT get used to it?](_topics/why-should-we-not-get-used-to-it.md) — Why adapting to unresolved problems can reinforce them, including habitual uses of PCA and p-values.
- [Should a new idea already outperform the state of the art?](_topics/should-a-new-idea-already-outperform-the-state-of-the-art.md) — Why current performance alone is insufficient to reject a research direction or funding proposal.

Both articles are dated 2026-10-09 and marked `published`, so they appear automatically on the homepage and in the topic feed after deployment. Statistical references use DOI links; the PCA example is self-contained.

## Local preview and deployment

Install the gems with `bundle install`, then run `bundle exec jekyll serve` and open `http://localhost:4000/viewpoints/`.
Run `bundle exec jekyll build` to check the production output in `_site/`.

The GitHub Pages workflow builds and deploys pushes to `master`. Adding an article locally does not deploy it.
Generated output, local caches, and the workflow-generated `_config_ci.yml` are ignored by Git.

## Citation and reuse

Please cite the original URL and author when reusing or adapting content.

Content is licensed under **CC BY-SA 4.0**.

- Human-readable summary: <https://creativecommons.org/licenses/by-sa/4.0/>
- Legal code: <https://creativecommons.org/licenses/by-sa/4.0/legalcode>
