# Dong Lab — Website

Source for the Dong Lab website. Pure static HTML / CSS / JS, no build step, hosted via GitHub Pages.

PI: **Yating Dong**, Professor, School of Life Sciences, Zhejiang Chinese Medical University.

## Page structure

```
├── index.html          # Home — hero + research preview + recent highlights
├── research.html       # Three research themes + approaches/methods
├── publications.html   # Year-grouped publication list (2026 → 2020 and earlier)
├── people.html         # PI bio + lab members + recruitment note
├── gallery.html        # Placeholder ( ｡◕ ‿ ◕ ｡) — fill in later
├── contact.html        # Address, email, joining-the-lab guide
├── assets/
│   ├── css/style.css   # Single stylesheet, theme tokens at the top
│   ├── js/main.js      # Mobile nav toggle
│   └── images/         # Drop photos and figures here
└── README.md
```

## Deploy to GitHub Pages

1. Create a new repo on GitHub.
   - For the lab's main site, use the repo name `<username>.github.io` → served at `https://<username>.github.io`
   - Or any name (e.g. `dong-lab`) → served at `https://<username>.github.io/dong-lab/`
2. Push all files in this folder to the `main` branch.
3. Repo Settings → Pages → Source: `Deploy from a branch`, branch `main`, folder `/ (root)`.
4. Wait 1–2 minutes. Pages will show the live URL.

## Custom domain (recommended)

1. Buy a domain, e.g. `donglab.org` (~ $10–15 / year).
2. Create a `CNAME` file in the repo root containing one line: `donglab.org`
3. At your DNS provider, add:
   - `A` records pointing to GitHub Pages IPs: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - Or a `CNAME` record pointing to `<username>.github.io`
4. Repo Settings → Pages → enable HTTPS.

## Placeholders to fill in

All editable spots are marked with square brackets `[ ]`. Open any HTML file and search for `[` to find them. The critical ones across all pages:

- `[your-email]@zcmu.edu.cn` — your institutional email
- `[id]` (Google Scholar) and `[your-id]` (ORCID) — IDs in profile URLs
- `[hobbies — ...]` in `people.html` — a sentence or two about you outside the lab
- Publications: replace placeholder entries with real ones
- People: replace `[Name]`, `[Year joined]`, etc. as the lab grows
- Hero news mentions the NSFC Excellent Young Scientists Fund (Overseas) — edit or remove as you prefer

## Adding content over time

### A new publication
In `publications.html`, copy one `<li class="pub-item">…</li>` block inside the right year. Use `†` for co-first authorship and `*` for corresponding author; the layout already supports them.

### A new lab member
In `people.html`, copy one `<div class="person-card">…</div>` block under the right role heading. Save a square portrait (e.g. 400×400) as `assets/images/firstname-lastname.jpg`, then replace `<div class="photo-placeholder small">…</div>` with `<img src="assets/images/firstname-lastname.jpg" alt="Name">`.

### Gallery photos
When you're ready to populate `gallery.html`, replace the empty-state block with gallery blocks. The CSS already supports a 4-column grid with three figure sizes (default, `tall`, `wide`). See `assets/css/style.css` → `.gallery-*` rules.

## Design tokens

Color, font, and spacing variables are at the top of `assets/css/style.css` under `:root`. To change the accent color globally, edit `--accent`. Current palette:

- Background `#0e1726` (deep navy)
- Surface `#1a2438`
- Accent `#5eead4` (teal)
- Display font: Fraunces (variable serif)
- Body font: Inter Tight

## License

Free to use, modify, and adapt.
