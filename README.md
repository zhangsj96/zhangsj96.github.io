# zhangsj96.github.io

Personal website of Shangjia Zhang, built with [al-folio](https://github.com/alshedivat/al-folio) v1 and deployed to
GitHub Pages by `.github/workflows/deploy.yml` on every push to `master`.

## Where things live

| Content | File |
| --- | --- |
| Home page (bio, research summary) | `_pages/about.md` |
| News items | `_news/*.md` (one file per item) |
| Research themes (cards + detail pages) | `_projects/*.md`, landing page `_pages/projects.md` |
| Figures / movies for research pages | `assets/img/research/`, `assets/video/` (web-compressed copies; full-res on figshare) |
| Publications | `_bibliography/papers.bib` (`selected={true}` → home page; `preview=` → thumbnail) |
| Talks, press, outreach | `_pages/talks.md` |
| Teaching & mentoring | `_pages/teaching.md` |
| CV | `assets/pdf/Shangjia_Zhang_CV.pdf` (copy from the LaTeX CV repo) |
| Social links | `_data/socials.yml` |

## Local preview

Uses a conda env named `website` (Ruby 3.3, Node 20, ImageMagick):

```bash
conda create -n website -c conda-forge ruby=3.3 nodejs=20 imagemagick compilers make   # once
bin/local bundle install && bin/local npm ci                                              # once
bin/local bundle exec jekyll serve --livereload                                           # http://localhost:4000
```
