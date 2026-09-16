# How to Update Your Website

You can make every change described here directly on GitHub in your browser — no software to install. Open the file, click the pencil icon to edit, then click "Commit changes." The site rebuilds and goes live automatically within about 2 minutes.

## Add a new paper

1. Open `data/papers.yaml` and add a new entry at the top, copying this template:

```yaml
- title: "Your Paper Title"
  authors: ["Mustafa Enes Caliskan"]
  year: 2026
  status: "working paper"   # or: published, accepted, revise and resubmit, under review, work in progress
  venue: ""                 # journal name, if published or R&R
  pdf: "files/paper-name.pdf"   # or a full https:// link
  link: ""
  abstract: ""
  job_market_paper: false
```

2. If hosting the PDF on the site, upload it to `static/files/` (on GitHub: open the folder, "Add file" → "Upload files").

## Mark a paper as published

In `data/papers.yaml`, change its `status` to `"published"` and fill in `venue` with the journal name.

## Change your job market paper

Set `job_market_paper: true` on the new paper and `false` on the old one.

## Update your bio

Edit the paragraphs in `content/_index.md`. The tagline under your name in the hero section is in `hugo.yaml` under `params.tagline`.

## Add a teaching entry

Add an entry to `data/teaching.yaml`:

```yaml
- course: "Course Name"
  role: "Teaching Assistant"
  institution: "University of Delaware, Department of Economics"
  term: "Fall 2026"
  instructor: "Dr. Name"   # optional
```

## Add a news item

Add an entry to the top of `data/news.yaml`:

```yaml
- date: "August 2026"
  text: "What happened."
```

The homepage shows the 8 most recent items.

## Add an award, talk, or service role

- Awards: `data/awards.yaml`
- Conference presentations and service, department service: `data/talks.yaml`

## Update your CV

Right now the "CV" button links to your Google Drive PDF. To host it on the site instead:

1. Upload the PDF to `static/files/` as `cv.pdf`.
2. In `hugo.yaml`, change `params.cv` and the CV menu URL to `/files/cv.pdf`.

To keep using Google Drive, just replace the file inside Drive — the link stays the same.

## Change your photo

Replace `static/images/photo.jpg` with your headshot (keep the exact filename `photo.jpg`). A square image around 600×600 pixels looks best. **The current file is a placeholder with your initials — replace it before sharing the site.**

## Footer credit and directory marker

- Turn the "Created using GaryKing.org/mysite" footer line on/off: set `params.mysite.credit` in `hugo.yaml` to `true` or `false`.
- Turn the invisible directory marker on/off: set `params.mysite.discovery` to `true` or `false`.

## Changing colors

All colors are defined at the top of `assets/css/style.css` in the `:root` block. `--color-accent` controls links, buttons, and highlights.
