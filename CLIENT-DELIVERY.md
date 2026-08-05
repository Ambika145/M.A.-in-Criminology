# Client Delivery Format Checklist

## Requirements alignment

| # | Requirement | Status |
|---|-------------|--------|
| 1 | File type `.html` | Yes — `index.html` |
| 2 | Bootstrap 3 or 4 | Yes — **Bootstrap 4.6.2** |
| 3 | Maximum 5 CSS files | Yes — **2 CSS files**: Bootstrap 4 + `css/style.css` |
| 4 | Maximum 10 JS files | Yes — jQuery, Bootstrap 4, `js/main.js`, NPF scripts, analytics |
| 5 | Remove unwanted JS/CSS (avoid form conflicts) | Yes — removed OwlCarousel, Bootstrap 5, Bootstrap Icons, dead inline JS; page JS does not touch form fields |
| 6 | Image folder ≤ 5 MB | Yes — `images/` (~0.9 MB) |
| 7 | Font folder if specific font required | Yes — `fonts/` (Montserrat woff2) |
| 8 | Banner image 1366 × 768 | Yes — `images/banner.jpg` |

## What to share with the client

Ship these folders/files only:

```
index.html
css/style.css
js/main.js
fonts/
images/
```

Do **not** ship for client upload: `assets/` (uncompressed originals), `node_modules/`, `style.css` / `responsive.css` at root (merged into `css/style.css`), or `scripts/`.

## CSS files (2 / max 5)

1. Bootstrap 4.6.2 (CDN)
2. `css/style.css` (site styles + responsive + local fonts)

## JS files (within max 10)

1. jQuery 3.6.0
2. Bootstrap 4.6.2 bundle
3. `js/main.js` (sliders/tabs only — no form field logic)
4. NPF `emwgts.js` (enquiry widgets)
5. NPF `npfwpopup.js`
6. NPF chatbot loader
7. GTM / Facebook Pixel (analytics)

## Notes

- Registration forms are NPF widgets only — do not add custom form JS.
- FAQ uses Bootstrap 4 collapse (`data-toggle` / `data-target` / `data-parent`).
