# Vividflar — Illustration Portfolio

A redesigned single-page portfolio site for **Vividflar** (Paul Nhlanhla Sikhakhane), built to replace the original Wix template with a custom layout, a real caption system, and a consistent visual identity.

**[Live preview →](#)** *(add your deployed URL here once hosted)*

---

## About this redesign

The original site was a flat image grid with no captions, mismatched crop ratios, and default Wix branding still showing. This version addresses that directly:

- **Grouped collections** — work is organized into *Character Studies*, *Fan Art & Pop Culture*, and *Texture & Concept Studies* instead of one undifferentiated feed
- **Gallery-label captions** — every piece gets a consistent title / medium / year tag, styled like a museum wall label, in place of blank or filename-based alt text
- **Unified image treatment** — every thumbnail is served at the same crop ratio and compression setting so the grid reads as one coherent body of work
- **Custom visual identity** — a dark ink palette with coral/marigold/teal accents, Fraunces for display type, Inter for body text, and IBM Plex Mono for captions and labels
- **Fully responsive** — 3-column grid on desktop, collapsing to 2 columns on tablet and mobile, with a slide-out mobile nav
- **No page-builder cruft** — no platform branding, no unused nav items, no stale copyright year

## Tech stack

Plain HTML, CSS, and vanilla JavaScript — no framework, no build step, no dependencies beyond Google Fonts.

- `index.html` — page structure and content
- `vividflar-styles.css` — all layout, color, typography, and responsive rules
- Google Fonts (Fraunces, Inter, IBM Plex Mono) loaded via CDN link

## File structure

```
.
├── index.html            # Main site markup
├── vividflar-styles.css  # All styling
└── README.md
```

> Keep `index.html` and `vividflar-styles.css` in the same folder — the stylesheet is linked with a relative path.

## Running locally

No build tools required. Either:

- Open `index.html` directly in a browser, or
- Serve it locally for a closer-to-production feel:
  ```bash
  python3 -m http.server 8000
  ```
  then visit `http://localhost:8000`

## Deploying

This is static HTML/CSS/JS, so it can go anywhere that serves static files:

- **GitHub Pages** — enable Pages on this repo (Settings → Pages → deploy from `main` branch)
- **Netlify / Vercel** — drag-and-drop the folder or connect the repo for auto-deploys
- **Wix** — paste the HTML into a Wix "Embed → HTML iframe" element if you want to keep it inside your existing Wix site

## Customizing

The portfolio grid ships with placeholder captions so the layout can be previewed immediately. Before publishing, search `index.html` for:

- `[Add title]` — replace with each piece's real title
- `[medium]` — replace with the actual medium (e.g. "Procreate", "Photoshop", "Traditional ink")
- `[year]` — replace with the year completed
- `[add title — name the source]` (fan art pieces) — name the source character/franchise explicitly

To add new pieces, duplicate a `.piece` block inside the relevant `.grid` container and swap the image URL, `alt` text, and label.

To adjust the palette or type scale, edit the CSS custom properties at the top of `vividflar-styles.css`:

```css
:root{
  --ink: #14121A;
  --paper: #EDE7E0;
  --coral: #FF5A54;
  --marigold: #F2A93B;
  --teal: #3FA79B;
  --text-soft: #C9C2D6;
}
```

## Credits

- Illustration work by **Vividflar** (Paul Nhlanhla Sikhakhane)
- Fonts: [Fraunces](https://fonts.google.com/specimen/Fraunces), [Inter](https://fonts.google.com/specimen/Inter), [IBM Plex Mono](https://fonts.google.com/specimen/IBM+Plex+Mono) via Google Fonts

## License

Site code is free to reuse and adapt. Illustration artwork remains © Vividflar — do not reuse the artwork itself without permission.
