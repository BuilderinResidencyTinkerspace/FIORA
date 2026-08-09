# Builder-in-Residence — Project Template

Template repo for BIR projects. Click **Use this template** to start your own copy.

## What goes where

- `docs/` — project overview and weekly logs. This folder becomes your website.
- `code/` — firmware, scripts, anything runnable.
- `cad/` — 3D models and design files (STL, STEP, F3D, 3MF).

## Preview the docs locally

    pip install mkdocs-material
    mkdocs serve

Open http://127.0.0.1:8000 and edit files under `docs/` — the preview reloads as you save.

## Publishing (GitHub Pages)

Every push to `main` rebuilds and publishes the site automatically (see `.github/workflows/deploy.yml`).

First-time setup:

1. Push once and let the Action finish. It creates a `gh-pages` branch.
2. Settings → Pages → Source: **Deploy from a branch** → `gh-pages` / `root`.

Your site will be live at `https://<org-or-user>.github.io/<repo>/`.


## Weekly logs

Fill in `docs/week-01.md` through `docs/week-09.md` as you go. Keep them short: what you did, what's blocking you, what's next.
