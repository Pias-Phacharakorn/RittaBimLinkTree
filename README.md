# RittaBimLinkTree

## Overview

A single-page "link tree" for **RITTA's Revit add-in** (Ritta pyRevit). It gathers the
links users need in one place, in collapsible sections:

- Installing Ritta pyRevit
- Requesting a Ritta pyRevit license
- Ritta pyRevit tools
- RITTA BQC – KPI Modeler
- Support through LINE Official Account

The page is in Thai and is published on GitHub Pages.

## Tech stack

- Plain **HTML + CSS + JavaScript** in one file, no build step
- **Inter** font from Google Fonts
- **GitHub Pages**, deployed by GitHub Actions

## Project tree

```text
RittaBimLinkTree/
├── index.html                       # The whole page: markup, styles and dropdown script
├── assets/
│   └── BimCenter.png                # Logo and favicon
├── .github/workflows/static.yml     # Deploys the repo to GitHub Pages
└── .claude/settings.json
```

## Running locally

Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
```

## Deploying

Every push to `main` runs `.github/workflows/static.yml`, which uploads the whole
repository to GitHub Pages. It can also be run by hand from the Actions tab
(`workflow_dispatch`).

## Developing

- Add or change links in `index.html`; each section is a dropdown with its own list.
- Keep image assets in `assets/`. Everything in the repo is published, so commit only files
  meant to be public.
