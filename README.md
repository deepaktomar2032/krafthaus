# Krafthaus

Single-page marketing site for Krafthaus LLC, a US e-commerce company. Built with SvelteKit
(`@sveltejs/adapter-static`) as a fully static site — no analytics, tracking, or backend.

## Publishing

The site is live at the custom domain in [`static/CNAME`](static/CNAME) (`krafthausgroup.com`), deployed via GitHub
Pages.

## Development

```sh
npm install
npm run dev       # start local dev server
npm run build     # produce a static export in build/
npm run preview   # preview the production build locally
```

Deployment to GitHub Pages happens automatically via [`.github/workflows/deploy.yml`](.github/workflows/deploy.yml)
on every push to `master`.
