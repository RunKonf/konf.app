# konf. — landing page

The public landing page for **Konf** (konf.app / konf.run) — the batteries-included
platform for community tech conferences.

Static, dependency-free, single `index.html`. No build step: GitHub Pages serves the
repo root as-is (`.nojekyll` disables Jekyll processing).

## Deploy

GitHub Pages → **Settings → Pages → Deploy from a branch → `main` / `/ (root)`**.

**Custom domains — both `konf.app` and `konf.run` serve this page.** GitHub Pages
accepts only ONE custom domain per repo: `konf.app` is this repo's Pages domain;
`konf.run` is served by a sibling redirect-shim repo (`RunKonf/konf.run`) with its
own Pages site + certificate, because both TLDs are **HSTS-preloaded** (browsers
force HTTPS, so plain-HTTP registrar forwarding cannot work).

The platform may later claim `*.konf.run` subdomains for tenant sites; the apex
redirect doesn't conflict with that.

## Launch sequence

1. [x] `hei@konf.app` mailbox/routing (registrar email forwarding, MX live).
2. [x] DNS: both apexes → GitHub Pages A records (185.199.108–111.153).
3. [x] Repo → **public** (2026-07-28).
4. [x] Pages enabled: `main` / root, custom domain `konf.app`.
5. [ ] Enforce HTTPS once the `konf.app` certificate is provisioned (Settings → Pages).
6. [ ] `konf.run` redirect shim repo published + its Pages domain set to `konf.run`.
7. [ ] Verify: `https://konf.app` serves, `konf.run` redirects, OG preview renders,
       live-conference links resolve (`cloudnativebergen.no`).

## Brand

Polar-night ground `#0B1220` · ember accent `#E8823C` · aurora `#57C4A3` (terminal
success only) · name-badge mark · lowercase wordmark `konf.` · tagline
**"Run your conference."**
