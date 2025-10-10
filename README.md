Lightweight Portfolio

This is a minimal, responsive portfolio built with pure HTML and CSS. It's intended for a backend-focused engineer with fullstack, game, and C++ experience.

Files

How to preview
Open `index.html` in your browser (double-click in Explorer or use a local HTTP server).

Customize

Hosting
This is a static site — deploy to GitHub Pages, Netlify, or any static host.

Lightweight Portfolio

This is a minimal, responsive portfolio built with pure HTML and CSS. It's intended for a backend-focused engineer with fullstack, game, and C++ experience.

Files
- `index.html` — the main page
- `css/styles.css` — styles

Images
- Place project screenshots under `assets/images/`.
- Default filenames referenced by the site:
	- `project-jobqueue.jpg`
	- `project-tooling.jpg`
	- `project-observability.jpg`

How to preview
Open `index.html` in your browser (double-click in Explorer or use a local HTTP server).

Customize
- Replace "Your Name" and contact information in `index.html`.
- Add or replace project images in `assets/images/` using the filenames above (or update the `src` attributes in `index.html`).
- Swap colors in `css/styles.css` under `:root`.

Hosting
This is a static site — deploy to GitHub Pages, Netlify, or any static host.

Notes
- We used a matcha-inspired color palette. We can add CDN image optimization later if you want.

Using jsDelivr (GitHub CDN)

This project can serve static assets through jsDelivr using the GitHub "gh" provider. That means you can reference files from this repository (or any public GitHub repo) with URLs like:

- https://cdn.jsdelivr.net/gh/<GITHUB_USER>/<REPO>@<BRANCH_OR_TAG>/path/to/file

Examples for this repo (replace `CamDHall`, `portfolio_2026`, and `main` if your repo or branch differ):

- CSS (styles):
	https://cdn.jsdelivr.net/gh/CamDHall/portfolio_2026@main/css/styles.css
- Project images:
	https://cdn.jsdelivr.net/gh/CamDHall/portfolio_2026@main/assets/images/project-jobqueue.svg
- Resume PDF:
	https://cdn.jsdelivr.net/gh/CamDHall/portfolio_2026@main/resume.pdf

Pin to a release or tag by using `@v1.2.3` instead of `@main` to ensure the CDN serves a fixed version. If you update files on `main` and want changes to propagate immediately, keep `@main` (jsDelivr caches content briefly, but will update when upstream changes).

Publishing notes

- Make sure the assets you reference are committed and pushed to the branch you use in the URL (e.g. `main`).
- For private repositories, jsDelivr cannot fetch files. Use a public GitHub repo or an alternative CDN.
- If you want to serve Google Fonts via jsDelivr, you can include a local copy of the font files and reference them from the repo, but in most cases loading fonts directly from Google Fonts (as this site does) is simplest and recommended.

If you'd like, I can also:
- Replace all image URLs in `index.html` with placeholder templated variables and add a small script to switch between local and CDN paths for local development vs production.
- Add a short deployment section showing how to tag a release and update links to a pinned version.

Local development

During development it's often easier to load assets from the local filesystem so you can iterate without pushing to GitHub. The files in this repo (for example `css/styles.css`, `assets/images/*`, and `resume.pdf`) will continue to work when you open `index.html` locally.

To switch between local and CDN paths you can:

1. Use the CDN URLs in `index.html` for production.
2. For local testing, change the CDN URLs back to local relative paths (for example, `css/styles.css` or `assets/images/project-jobqueue.svg`).

If you'd like, I can add a tiny build script that swaps these automatically (or uses a simple query-string flag to load local assets when present).
