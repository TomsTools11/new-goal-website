# GOAL — Client Resources Strategy Website

A static site presenting the GOAL Client Resources Website Section Strategy.

## Pages

| URL | File | Description |
| --- | --- | --- |
| `/` | `index.html` | Landing page linking to all resources |
| `/strategy` | `strategy.html` | Strategy & implementation plan |
| `/dashboard` | `dashboard.html` | Structured dashboard view |
| `/goal-client-resources-strategy.pdf` | PDF | Source PDF document |

This is a plain static site — no build step or dependencies. The pages are
self-contained HTML with inline CSS (fonts are loaded from Google Fonts).

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

[`vercel.json`](./vercel.json) enables `cleanUrls` so pages are served at
extension-less paths (e.g. `/strategy` instead of `/strategy.html`).
