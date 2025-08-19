# Alloy Brand Assets

Centralized, source‑of‑truth assets for Alloy’s visual identity.

Contents
- `logo-mark.svg`: Primary logo mark (stylized “A”, blue→aqua gradient)
- `favicon.svg`: Favicon using the same mark
- `og.svg`: Open Graph banner (SVG), copied from the apex site
- `brand.css`: CSS custom properties (colors + font stacks)
- `colors.json`: Color tokens for programmatic use

Usage
- Docs (MkDocs):
  - Copy `logo-mark.svg` to `docs/assets/logo.svg` and `favicon.svg` to `docs/assets/favicon.svg` (already done).
  - Or reference them directly if hosting these under a shared domain.
- Main site (Vercel):
  - Use `logo-mark.svg` inline as in `alloy-www/index.html` or link to it as a file.
  - `og.svg` can be exported to PNG for social cards.

PNG exports
- Inkscape: `inkscape --export-type=png --export-width=1200 --export-filename=og.png og.svg`
- rsvg: `rsvg-convert -w 1200 -h 630 og.svg > og.png`
- macOS Preview: open and export as PNG.

Colors (from apex site)
- Brand: `#7aa2ff`
- Accent: `#54f0d1`
- Text: `#e8eaf6`
- Muted: `#a9b0c9`
- Bg 1: `#0b0f22`
- Bg 2: `#121637`
- Border: `rgba(255,255,255,0.12)`
- Card: `rgba(255,255,255,0.06)`

Fonts
- Sans: `ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, Helvetica, Arial, "Apple Color Emoji", "Segoe UI Emoji"`
- Mono: `ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, "Liberation Mono", monospace`

Notes
- This folder is intended to be its own repo (`alloy-brand`). You can git init here and set a remote.
- Update both `alloy-www` and `alloy-py` when brand assets evolve; these files are the canonical versions.
