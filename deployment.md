# Deployment

This site is intended to be deployed from GitHub to Cloudflare Pages.

## Cloudflare Pages settings

- Production branch: `main`
- Build command: `mkdocs build`
- Build output directory: `site`

## Notes

- Python dependencies are declared in `requirements.txt`.
- The repository pins Python with `.python-version`.
- Each push to the connected GitHub branch should trigger a new Pages deployment.
