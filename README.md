# Garden City Tattoo — Lineup

Mobile-first landing page: an endlessly swipeable band photo with one stop per artist. The centred artist is in colour; everyone else is black-and-white and blurred. The artist's name repeats in the background, and the logo and contact speed dial take that artist's neon colour.

Single self-contained file: `index.html` (images are embedded). Works on GitHub Pages as-is, or deploy on [Railway](https://railway.com) with the included `package.json` static server.

**Demo:** [demo.gif](./demo.gif) — 9:16 letterboxed so the full page (including the bottom) shows when opened directly.

## Deploy on Railway

1. Push this repo to GitHub (see below).
2. In [Railway](https://railway.com/new): **New Project** → **Deploy from GitHub repo** → select `garden-city-lineup`.
3. Railway detects Node via `package.json` and runs `npm start`, which serves the site on `$PORT`.
4. Open **Settings → Networking → Generate Domain** for a public URL.

No build step or environment variables required.

## Editing
All settings live at the top of the `<script>` in `index.html`:

- `STEPS`: one entry per artist: stop position (`x`, in source-image pixels), `name`, `neon` colour, `ig`, `email`, `phone` (optional `sms`).
- `VIEW_W`, `DROP`: zoom level and how low the photo sits.
- `--bg-blur` (CSS): softness of out-of-focus people.

People outlines live in the `people-svg` block. Edit `people-trace.svg` (ids `p1`–`p7`, layer order = depth, last = front), delete the reference photo layer, and paste the SVG into that block.

Press **D** on desktop to show stop markers and outlines.

> Jake Mercer, Sam Holloway, Luis Ortega and Ben Carver are placeholder names. All emails and phone numbers are placeholders.
