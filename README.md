# mustafacaliskan-site

Personal academic website of Mustafa Enes Çalışkan, PhD candidate in Economics at the University of Delaware.

Built with [Hugo](https://gohugo.io/) and deployed to GitHub Pages via GitHub Actions.

## Structure

- `content/_index.md` — homepage bio
- `data/papers.yaml` — job market paper, working papers, work in progress
- `data/teaching.yaml` — teaching history
- `data/awards.yaml` — fellowships and awards
- `data/talks.yaml` — presentations, conference service, department service
- `data/news.yaml` — news feed
- `hugo.yaml` — site configuration (name, tagline, email, menu, social links)
- `assets/css/style.css` — all styles
- `static/files/` — PDFs
- `static/images/photo.jpg` — headshot

## How to update

See [UPDATING.md](UPDATING.md) — every change can be made in the GitHub web editor; the site auto-deploys on push to `main`.

## Local preview

Install [Hugo extended](https://gohugo.io/installation/), then:

```
hugo server
```

and open http://localhost:1313/mustafacaliskan-site/.

## Deployment

Push to `main`. The workflow in `.github/workflows/deploy.yml` builds the site and publishes it to GitHub Pages. In the repo settings, set **Settings → Pages → Source: GitHub Actions** (one-time step).
