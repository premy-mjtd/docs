# MkDocs on Cloudflare Pages

This repository is set up as a static documentation site using MkDocs.

## Local development

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
mkdocs serve
```

Your local preview will be available at `http://127.0.0.1:8000`.

## Build locally

```bash
mkdocs build
```

The generated static site is written to `site/`.

## Deploy on Cloudflare Pages

Connect this GitHub repository to Cloudflare Pages and use these settings:

- Production branch: `main`
- Build command: `mkdocs build`
- Build output directory: `site`

This repo includes a `.python-version` file pinned to `3.13`, which Cloudflare Pages can use to select the Python version in the current build system.

If you disable automatic dependency installation in Pages, change the build command to:

```bash
pip install -r requirements.txt && mkdocs build
```
