# AGENTS.md

## Cursor Cloud specific instructions

This repository is a **zero-dependency static HTML site** (a GULF "AI Assistant Evaluation"
project-update report). There is no package manager, build step, test suite, or lint tooling.

- Entry point: `index.html` performs a `<meta http-equiv="refresh">` redirect to the actual
  report `session_202_comparison_v1.html`. The report references `gulf-logo.svg`.
- Run it locally by serving the repo root with any static file server, e.g.
  `python3 -m http.server 8000`, then open `http://localhost:8000/` (root redirects to the report).
  Opening the HTML file directly via `file://` also works; a server is only needed for clean URLs.
- There are **no tests, no lint, and no build** to run. The report is plain static HTML/CSS with
  no JavaScript, so "running the app" means serving and viewing the rendered report.
- Deployment is handled by GitHub Actions: `.github/workflows/deploy-pages.yml` (publishes to the
  `gh-pages` branch on push to `main`) and `.github/workflows/deploy-netlify.yml` (manual). These
  only copy the static files; do not treat them as a local build.
