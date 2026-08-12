# Assets

Drop the logo files in here using the exact filenames below. The page already
points at these paths, so nothing in `index.html` needs editing — overwrite the
placeholder and refresh.

| Filename | Where it appears | Displayed width | Needs to read against |
|---|---|---|---|
| `logo.svg` | Header (Section 1) | 180px, 120px on mobile | White |
| `logo-reversed.svg` | Footer (Section 10) | 160px | Navy `#002C46` |

## Why two files

The footer sits on a navy band. A dark logo disappears against it, so the
footer needs a reversed (white or light) version. If your logo is already
light, or has a version that works on both, copy the same file to both names.

## Format

SVG is preferred — it stays sharp at any size and on any screen. PNG at 2×
the displayed width works too (360px wide for the header, 320px for the
footer), on a transparent background.

If you supply PNG or JPG instead of SVG, update the two `src` attributes in
`index.html` to match the new extension. Search for `assets/logo` to find them.

## Height

Height is set automatically from your file's own proportions, so a taller or
shorter logo will not be squashed. Only the width is fixed. The header band is
80px tall, so keep the header logo under roughly 48px of visual height at
180px wide, or it will crowd the band.
