# What the Literature Says About Design Guidance for Autistic Learners

An interactive view of a PRISMA-ScR scoping review of published design guidance
(2018–2026) for educational technology for autistic learners.

Rather than reducing the literature to a single checklist, the site is organised
around the **decisions a developer has to make**, and shows where included studies
point in different directions.

- 75 reports representing 73 studies
- 1,077 quoted recommendations, each verified against the source PDF
- 414 design principles grouped into 145 design issues
- 14 contested decisions where the literature disagrees
- 29 design issues resting on fewer than three studies

## Status

**Working prototype.** The grouping of principles into design issues has not yet
been through independent human review, so labels and boundaries may change. Study
counts and quotations are verified against the source PDFs.

## Contents

| File | What it is |
|---|---|
| `index.html` | The whole site. One self-contained file with the data inlined. |
| `404.html` | Not-found page. |
| `.nojekyll` | Tells GitHub Pages to serve files as-is. |
| `LICENSE` | **Choose one before publishing.** |

## Deploying

**Cloudflare Pages, direct upload.** Pages → Create → Upload assets → drag this
folder in. No build command, no framework preset. It is static.

**Cloudflare Pages, from GitHub.** Connect the repository, leave the build command
empty and set the output directory to `/`.

**GitHub Pages.** Push this folder to a repository, then Settings → Pages → Deploy
from a branch → `main` → `/ (root)`.

**Locally.** Open `index.html` in a browser. No server needed.

## Offline use

The only external requests are the Google Fonts stylesheet and the DOI links on
citations. Remove the `<link rel="stylesheet" href="https://fonts.googleapis.com...">`
line to make the page fully self-contained; it falls back to Georgia and the
system sans.

## How to read the counts

Counts are **independent studies, not reports**: two pairs of papers report the
same study and are counted once. A count shows how often a position recurs in this
literature, not how strong the evidence for it is. "Direct" means studies that
generated evidence of their own, as opposed to reviews and conceptual papers.

A topic with one recommendation and no recorded counter-position usually means the
question has not been studied much, not that the field has settled it. The
**Thin evidence** tab lists the topics where that applies.

## Citation

[PENDING — add the manuscript citation once the paper is submitted.]
