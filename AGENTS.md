# AGENTS.md

## Cursor Cloud specific instructions

This repository (`cursor-eva`) is a **static HTML report site** — there is no
package manager, build system, dependencies, tests, or linter. The "application"
is the static report `session_202_comparison_v1.html`, with `index.html` acting
as a redirect landing page.

### Running it (development mode)

Serve the repo root with any static file server, e.g.:

```bash
python3 -m http.server 8000
```

Then open `http://localhost:8000/` (redirects to the report) or
`http://localhost:8000/session_202_comparison_v1.html` directly. No build step is
required — edits to the HTML are reflected on page reload.

### "Build" / deploy

There is no local build. The closest equivalent is the GitHub Actions deploy
workflows (`.github/workflows/deploy-pages.yml`, `deploy-netlify.yml`), which
just copy `index.html`, `session_202_comparison_v1.html`, and `README.md` into a
`public/` folder and publish it. If you replicate that locally, treat `public/`
as a throwaway build artifact (do not commit it).

### Lint / test

None exist. There is nothing to lint, test, or compile.
