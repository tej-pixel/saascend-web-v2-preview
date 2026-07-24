# Brand & image assets — drop files here

Save brand/image files here with the exact filenames below and the site picks
them up. (Claude Code can't pull images pasted into chat onto disk — files must
exist on disk or be reachable by URL.)

## Logos → `public/brand/`  ✅ wired

| File | Used by | Notes |
|------|---------|-------|
| `saascend-logo-white.png` | Header, Footer | White-and-blue wordmark for dark navy backgrounds |
| `saascend-logo-dark.png`  | any light-bg use (`<Logo variant="dark" />`) | Full-color wordmark for light backgrounds |

These are already in place and rendering. To update the logo, just replace the
files (keep the names). `Logo.astro` references them directly — no env flag needed.

## Client logos → `public/brand/clients/`

Drop each client logo as an SVG/PNG named by slug, e.g. `northwind.svg`,
`atlas-industrial.svg`, `vellum.svg`. Then map them in
`src/components/LogoMarquee.astro` (`LOGOS` array: set `img: '/brand/clients/<file>'`).
Logos with a `href` link to that case study.

## Hero background → `public/images/`

| File | Used by |
|------|---------|
| `hero-summit.jpg` | Homepage hero background (the summit/mountaineering image) |

Recommended: ~2400×1400, optimized JPG/WebP, < 400 KB. The hero applies a navy
gradient overlay automatically for text contrast.
