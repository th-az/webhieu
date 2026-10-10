# HU Culinary

React, Vite, and Tailwind CSS single-page website.

## Local development

Use Node.js 22.12.0 or later (see `.nvmrc`), then run:

```sh
npm ci
npm run dev
```

## Build

```sh
npm run build
```

The production site is generated in `dist`.

## Deploy to Cloudflare Pages

Connect the `th-az/webhieu` GitHub repository to Cloudflare Pages and use:

- **Production branch:** `main`
- **Build command:** `npm run build`
- **Build output directory:** `dist`
- **Root directory:** `/` (the repository root)
- **Node.js version:** `22.12.0` or later

Cloudflare Pages automatically serves the root `index.html` for single-page application routes
(such as `/about`, `/products`, `/products/classic-hu`), so direct links and page refreshes work out of the box.
Public images and build assets use root-relative URLs.

No Cloudflare Worker, database, or Netlify-specific configuration is required.
