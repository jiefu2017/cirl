# CIRL — Control and Intelligent Robotics Lab

Website for the Control and Intelligent Robotics Lab, led by Dr. Jie Fu at the
University of Florida. Built with [Hugo](https://gohugo.io) and deployed to
GitHub Pages via GitHub Actions.

## Local development

```sh
brew install hugo   # if not already installed
hugo server -D
```

Visit http://localhost:1313/cirl/.

## Editing content

- **People**: edit `data/people.yaml`.
- **Publications**: edit `data/publications.yaml` (add new entries at the top of their year).
- **Research areas**: edit the Markdown files in `content/research/`.
- **News**: add a new Markdown file in `content/news/` (copy an existing one and update the date/title).
- **Contact info / site-wide settings**: edit the `[params]` section in `hugo.toml`.

## Deployment

Pushing to `main` triggers `.github/workflows/hugo.yml`, which builds the site
with Hugo and publishes it to GitHub Pages. Enable Pages in the repo settings
under **Settings → Pages → Source: GitHub Actions** (one-time setup).

The site is served at `https://jiefu2017.github.io/cirl/`. If you point a
custom domain at it instead, add a `static/CNAME` file with the domain and
update `baseURL` in `hugo.toml`.
