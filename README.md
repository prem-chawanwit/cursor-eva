# cursor-eva

## Project Update Report

- Open the report from GitHub Pages/root URL via `index.html`
- Direct file: [`session_202_comparison_v1.html`](./session_202_comparison_v1.html)

## Public Deployment

### Option A: GitHub Pages

This repo publishes the static report to the `gh-pages` branch on every push to `main`.

- Public URL, if GitHub Pages is enabled: `https://prem-chawanwit.github.io/cursor-eva/`
- Workflow: [`.github/workflows/deploy-pages.yml`](./.github/workflows/deploy-pages.yml)

GitHub Pages requires this repo to be public, or a GitHub Enterprise plan that supports private Pages.

If the repo is public, enable GitHub Pages once:

1. Go to **Settings** → **Pages**
2. Set **Source** to **Deploy from a branch**
3. Select branch **gh-pages** and folder **/** (root)
4. Save, then wait for GitHub Pages to publish

### Option B: Netlify for private repositories

Use this option when the repository must stay private but the report should be public.

- Workflow: [`.github/workflows/deploy-netlify.yml`](./.github/workflows/deploy-netlify.yml)
- Trigger: manual run from **Actions** → **Deploy static report to Netlify**

Setup:

1. Create a Netlify site.
2. Copy the Netlify **Site ID**.
3. Create a Netlify personal access token.
4. Add GitHub Actions secrets:
   - `NETLIFY_SITE_ID`
   - `NETLIFY_AUTH_TOKEN`
5. Run the Netlify workflow manually.
