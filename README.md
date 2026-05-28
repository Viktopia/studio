# Viktopia Studio

Source for [studio.viktopia.io](https://studio.viktopia.io) — a one-page
portfolio for Viktopia Studio.

## Stack

- **[Hugo](https://gohugo.io/)** (extended) for static site generation and
  image processing (PNG → WebP via the asset pipeline).
- **[Tailwind CSS v4](https://tailwindcss.com/)** with a CSS-first token
  system (Catppuccin Latte palette + a custom editorial type scale).
- **[Bun](https://bun.sh/)** for JS dependency management.
- **GitHub Pages** for hosting (custom domain via `CNAME`).

## Local development

```sh
bun install
bun run dev          # hugo server on http://localhost:1313
```

## Build

```sh
bun install
bun run build        # output → ./public
```

## Deploy

Pushes to `master` are deployed by `.github/workflows/deploy.yml`
(GitHub Pages with `actions/deploy-pages`). The site is served on the
custom domain `studio.viktopia.io` (see `static/CNAME`).

## Adding a project

Create a new markdown file under `content/projects/` with frontmatter
matching the existing entries. Drop the logo into `assets/images/` —
Hugo will resize and convert it to WebP at build time.

## License

© Viktopia UK Ltd, DBA Viktopia Studio. All rights reserved.
