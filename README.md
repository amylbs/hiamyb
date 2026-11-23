# hiamyb.com

Portfolio site for Amy Brumet, Product Designer.

A single static page: no build step and no dependencies. Fonts load from Google Fonts.

## Structure

```
index.html   page, styles and script, including all case study copy
img/         images, videos, logos and favicon
```

Case studies are routed by URL hash, e.g. `/#whimsical`, `/#hestan-cue`.

## Editing content

Everything lives in `index.html`:

- **Case studies:** the `CS` array near the top of the `<script>`. Each entry has `title`, `lede`, `meta`, `problem`, `steps`, `outcome`, plus optional `gallery` (images after the outcome, `[src, alt, caption]`) and `afterSteps`. A step can carry media as a third item: `{img|video, label, caption}`.
- **Experience:** the `EXP` array. Company links live in `LINKS`.
- **Work collage layout:** `POS` (desktop) and `POS_M` (narrow screens). Each entry is `[left, top, rotation, z-index]`.

## Run locally

```
python3 -m http.server 8000
```

Then open http://localhost:8000.

## Deploy on GitHub Pages

1. Push this folder to a repository, with `index.html` at the root.
2. In the repository, go to Settings → Pages, choose "Deploy from a branch", then select `main` and `/ (root)`.
3. For a custom domain, add it under Settings → Pages. GitHub creates a `CNAME` file. Then point your DNS at GitHub Pages.
