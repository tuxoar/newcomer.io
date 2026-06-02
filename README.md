# newcomer.io

Personal site for Shaun Newcomer — Security Engineer. Single static `index.html`, no build step, no dependencies.

## Deploy to GitHub Pages

1. **Create a repo.** For a user site, name it exactly `tuxoar.github.io`. (Any repo name works too — Pages will just live at a sub-path until the custom domain is set.)
2. **Push these files** to the `main` branch:
   - `index.html`
   - `CNAME` (contains `newcomer.io` — tells Pages to serve the custom domain)
   - `.nojekyll` (skips Jekyll processing so files are served as-is)
   - `README.md`
3. **Enable Pages.** In the repo: **Settings → Pages → Build and deployment → Source: Deploy from a branch**, branch `main`, folder `/ (root)`. Save.
4. **Point your domain.** At your DNS provider for `newcomer.io`, add:
   - Four `A` records for the apex (`@`): `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - One `AAAA`/`CNAME` for `www` → `tuxoar.github.io` (optional but recommended)
5. **Enforce HTTPS.** Back in **Settings → Pages**, once the domain verifies, tick **Enforce HTTPS**.

DNS changes can take anywhere from a few minutes to a few hours to propagate.

## Editing

Everything is in `index.html` — content, styles, and a tiny scroll-reveal script, all inline. Edit the text directly; no tooling required.
