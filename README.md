# konf. — landing page

The public landing page for **Konf** (konf.app / konf.run) — the batteries-included
platform for community tech conferences.

Static, dependency-free, single `index.html`. No build step: GitHub Pages serves the
repo root as-is (`.nojekyll` disables Jekyll processing).

## Deploy

GitHub Pages → **Settings → Pages → Deploy from a branch → `main` / `/ (root)`**.

Custom domain: once DNS is decided, add the domain under Settings → Pages (GitHub
writes the `CNAME` file) and point an `A`/`ALIAS`/`CNAME` record per
[GitHub's docs](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site).
Working assumption: `konf.app` is the front door (this page), `konf.run` is the tenant
runtime on the platform side.

## Before flipping public

- [ ] `hei@konf.app` must exist (the CTA mails it) — set up mail routing for konf.app first.
- [ ] Verify the live-conference links (currently `cloudnativebergen.no`).
- [ ] Repo → public, then enable Pages (Pages on a private repo requires a paid org plan).

## Brand

Polar-night ground `#0B1220` · ember accent `#E8823C` · aurora `#57C4A3` (terminal
success only) · name-badge mark · lowercase wordmark `konf.` · tagline
**"Run your conference."**
