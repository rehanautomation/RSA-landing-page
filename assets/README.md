# Assets

| File | Used in | Displayed width | Rendered height |
|---|---|---|---|
| `logo.png` | Header (Section 1) and Footer (Section 10) | 180px header, 120px on mobile, 160px footer | 50px / 33px / 45px |

Source file is 506 × 141px, RGBA with a transparent background.

## The footer logo is filtered white

The wordmark "ROCK SOLID" and the "POWERED BY ROCK SOLID AI" strapline are
dark navy. On the navy footer band they disappear completely, leaving only the
mountain and the word "Automation" floating on their own.

The footer therefore renders the same file as solid white using a CSS filter:

```css
.footer__logo{ filter: brightness(0) invert(1); }
```

That is legible and clean, but it flattens the blue mountain accent to white.
If a proper reversed logo is supplied, save it as `logo-reversed.png`, point
the footer `<img>` at it, and delete the filter rule from `.footer__logo`.

In GoHighLevel, upload a white version to the media library rather than
relying on a filter.

## Replacing the logo

Overwrite `logo.png`, keeping the filename, and update the `width` and
`height` attributes on both `<img>` tags in `index.html` to the new file's
real pixel dimensions. Those attributes only reserve the correct space while
the image loads; displayed size is set in CSS and height stays automatic, so
a different aspect ratio will not be squashed.

The header band is 80px tall. At 180px wide the current logo renders 50px
tall, which fits with room to spare. A much taller logo would crowd it.

SVG is preferred over PNG if a vector version exists — it stays sharp on
high-density screens at any size. If switching to SVG, update the `src`
extension in both places and drop the `width`/`height` attributes.
