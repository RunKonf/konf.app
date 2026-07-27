# konf. — landing page

The public landing page for **Konf** (konf.app / konf.run) — the batteries-included
platform for community tech conferences.

Static, dependency-free, single `index.html`. No build step: GitHub Pages serves the
repo root as-is (`.nojekyll` disables Jekyll processing).

## Deploy

GitHub Pages → **Settings → Pages → Deploy from a branch → `main` / `/ (root)`**.

**Custom domains — both `konf.app` and `konf.run` serve this page.** GitHub Pages
accepts only ONE custom domain per repo, so the pattern is:

1. Set `konf.app` as the Pages custom domain (Settings → Pages; GitHub writes `CNAME`),
   DNS per [GitHub's docs](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site).
2. Redirect `konf.run/*` → `konf.app/*`. Both `.app` and `.run` are **HSTS-preloaded
   TLDs** (browsers force HTTPS), so plain-HTTP registrar forwarding will NOT work —
   use an HTTPS-capable redirect: Cloudflare free tier (proxy + redirect rule) or a
   registrar that does TLS forwarding.

The platform may later claim `*.konf.run` subdomains for tenant sites; the apex
redirect above doesn't conflict with that.

## Before flipping public

- [ ] `hei@konf.app` must exist (the CTA mails it) — set up mail routing for konf.app first.
- [ ] Verify the live-conference links (currently `cloudnativebergen.no`).
- [ ] Repo → public, then enable Pages (Pages on a private repo requires a paid org plan).

## Brand

Polar-night ground `#0B1220` · ember accent `#E8823C` · aurora `#57C4A3` (terminal
success only) · name-badge mark · lowercase wordmark `konf.` · tagline
**"Run your conference."**
