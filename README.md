# GOAL — Website SEO & Content Strategy

A static site presenting the GOAL website redesign workstream: two SEO audits
and the content strategy for the on-domain Resources Hub.

## Pages

| URL | File | Description |
| --- | --- | --- |
| `/` | `index.html` | Overview / hub — links the three reports + OKR context |
| `/seo-audit-current` | `seo-audit-current.html` | **Report 01** — full SEO audit of the current site (checkoutgoal.com) |
| `/seo-audit-redesign` | `seo-audit-redesign.html` | **Report 02** — pre-launch SEO audit of the redesigned site |
| `/content-strategy` | `content-strategy.html` | **Report 03** — strategic case, IA, copy playbook & content roadmap |
| `/goal-client-resources-strategy.pdf` | PDF | Source strategy document (archive) |

All pages share a single design system in [`assets/`](./assets):

- `assets/report.css` — the brand stylesheet (Inter, blue/navy palette, mint accent)
- `assets/goal-logo.png` — the GOAL logo

The reports carry `<meta name="robots" content="noindex">` — they are internal
strategy documents, not public marketing pages.

This is a plain static site — no build step or dependencies (fonts load from
Google Fonts). Cross-page links are extensionless to match Vercel `cleanUrls`.

## Deploying to Vercel

The repo is ready to deploy as-is.

### Option A — Vercel dashboard
1. Push this repo to GitHub (already done if you're reading this on GitHub).
2. Go to [vercel.com/new](https://vercel.com/new) and import the repository.
3. Leave **Framework Preset** as **Other**, with no build command and no output
   directory (the root is served directly).
4. Click **Deploy**.

### Option B — Vercel CLI
```bash
npm i -g vercel
vercel        # preview deployment
vercel --prod # production deployment
```

## Configuration

[`vercel.json`](./vercel.json) enables `cleanUrls` so pages are served without
their `.html` extension, with `trailingSlash` disabled.
