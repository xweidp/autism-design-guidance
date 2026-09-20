# What the Literature Says About Design Guidance for Autistic Learners

An interactive view of a PRISMA-ScR scoping review of published design guidance
(2018 to 2026) for educational technology for autistic learners.

Rather than reducing the literature to a single checklist, the site is organised
around the **decisions a developer has to make**, and shows where included studies
point in different directions.

- 76 reports representing 73 studies
- 1,046 verbatim passages, coded as 1,101 analytic records, each verified against the source PDF
- 420 recommendations across 12 design areas
- 23 disagreements where the literature points two ways
- 193 recommendations (46 per cent) said by a single study

## Status

**Working prototype.** Domain assignment has not yet been through independent human review, so
boundaries may change. Study counts and quotations are verified against the source PDFs.

## What changed on 20 September 2026

The principle-family layer is gone. Amendment A16 retired the 414-principle, 145-family taxonomy
after a coder found the family level could not be applied: 145 categories carrying labels and no
definitions, with several plausible for most passages. The site no longer has a Topic filter and
no longer groups recommendations into design issues. It is organised by the twelve design areas,
which are not mutually exclusive, and by individual recommendations.

The Setting filter is also gone: the field it drew on is not reconstructible from the current
corpus. In its place is a **Who took part** filter, which selects on whether the studies behind a
recommendation involved autistic participants, adults acting as proxies, or no participants at all.
Given that half the advice in this review rests on work with no autistic participant, that is the
more useful facet.

## Contents

| File | What it is |
|---|---|
| `index.html` | The whole site. One self-contained file with the data inlined. |
| `404.html` | Not-found page. |
| `.nojekyll` | Tells GitHub Pages to serve files as-is. |
| `LICENSE` | **Choose one before publishing.** |

## Where the data comes from

Nothing is typed by hand and there is no spreadsheet behind the live site. The chain is:

```
09_final/A18/QUOTES_A18.csv        the charted passages, one row per record
09_final/STUDY_CHARACTERISTICS.csv what each report is and who took part
09_final/EVIDENCE_final.csv        source to study mapping (linked reports)
09_final/A15/CONTRADICTIONS_A15.csv the reported disagreements
02_screening/SCREENING_LOG_ALL_469.csv  DOIs, read through the corrections overlay
        |
        v  tools/build_site_data.py
_site_build/data.json
        |
        v  tools/build_site.py
_site_build/index.html  and  website/index.html   (data inlined, no fetch at runtime)
```

To refresh the site after any change to the corpus, run the two scripts in that order.

## Deploying

**Cloudflare Pages, direct upload.** Pages, then Create, then Upload assets, then drag this
folder in. No build command, no framework preset. It is static.

**Cloudflare Pages, from GitHub.** Connect the repository, leave the build command
empty and set the output directory to `/`.

**GitHub Pages.** Push this folder to a repository, then Settings, Pages, Deploy
from a branch, `main`, `/ (root)`.

**Locally.** Open `index.html` in a browser. No server needed.

## Offline use

The only external requests are the Google Fonts stylesheet and the DOI links on
citations. Remove the `<link rel="stylesheet" href="https://fonts.googleapis.com...">`
line to make the page fully self-contained; it falls back to Georgia and the
system sans.

## How to read the counts

Counts are **independent studies, not reports**: three pairs of papers report the same study each
and are counted once. A count shows how often a position recurs in this literature, not how strong
the evidence for it is. "Evidence of their own" means studies that generated data, as opposed to
reviews and conceptual papers.

A recommendation with one study behind it and no recorded counter-position usually means the
question has not been studied much, not that the field has settled it. Filter by **Said by one
study only** to see them.

## Citation

[PENDING, add the manuscript citation once the paper is submitted.]
