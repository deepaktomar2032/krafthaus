# Krafthaus

Single-page marketing site for Krafthaus LLC, a US e-commerce company. Built with SvelteKit
(`@sveltejs/adapter-static`) as a fully static site — no analytics, tracking, or backend.

## Before publishing

Two placeholders in [`src/lib/data/company.js`](src/lib/data/company.js) still need to be replaced with real values:

- `phone` — currently a placeholder US number
- `address` — currently a placeholder registered address

The site is configured for the custom domain in [`static/CNAME`](static/CNAME) (`krafthausgroup.com`). Point its DNS
at GitHub Pages — see the deployment PR/commit notes for the exact records.

## Development

```sh
npm install
npm run dev       # start local dev server
npm run build     # produce a static export in build/
npm run preview   # preview the production build locally
```

Deployment to GitHub Pages happens automatically via [`.github/workflows/deploy.yml`](.github/workflows/deploy.yml)
on every push to `master`.
