# Solar Shop — Homepage (Contest Build)

A pixel-faithful, single-file rebuild of **solarshop.co.nz**'s homepage with a fully
redesigned, upgraded hero section — built for the Freelancer.com contest
*"Solar Shop Hero Section Design"* and ready to deploy as a static site.

🔋 **Live-ready:** one `index.html`, zero dependencies, zero build step.
Every image, font (woff2), stylesheet and script is inlined — the page works
offline, on any static host, with **0 external requests**.

---

## What's inside

| File | Purpose |
|---|---|
| `index.html` | The complete website (full homepage replica + upgraded hero). Just serve it. |

## Highlights

- **100% homepage replica** — header + mega-menu, all 10 sections, footer,
  marquee, accreditation band, exact brand tokens (`--cream #FBF7EE`,
  `--deep #1F3D26`, `--sun #B89A4E`, Fraunces + Plus Jakarta Sans).
- **Upgraded hero (v29 lineage)**
  - 5-slide team-photo slider (Ken Burns, autoplay, hover-pause, swipe, keys)
  - Brand-gradient veil (hero only), gradient serif accent line
  - "Powered by Trilect" co-brand pill + rating trust-badge (pill shapes)
  - Editorial vertical brand rail on wide viewports (fluid, device-auto)
- **Solar-panel stats band** — the 5 KPIs rendered as a PV module:
  aluminium frame, blue cell glass, busbars, sunlight glare sweep,
  photon sparks, charge bar, cell charge pulses (7s loop).
- **Energy story vignettes** — EV charger (left) & battery (right) fed by
  animated gold beams; AI-generated house PNGs whose dark windows light up
  when the panel finishes charging.
- **Responsive** — desktop → mobile breakpoints verified at
  1280 / 1440 / 1600 / 2000 / 2560 / 390 px.
- **Accessible motion** — every animation honours `prefers-reduced-motion`.

## Deploy on Cloudflare Pages

### Option A — Git integration (recommended)

1. Push this folder to a GitHub repository (see commands below).
2. Cloudflare Dashboard → **Workers & Pages** → **Create** → **Pages** →
   **Connect to Git** → pick the repo.
3. Build settings:
   - *Framework preset:* `None`
   - *Build command:* *(leave empty)*
   - *Build output directory:* `/`  (repo root)
4. **Save and Deploy** — `index.html` at the root is served automatically.
   Every future `git push` re-deploys.

### Option B — Direct upload

Cloudflare Dashboard → **Workers & Pages** → **Create** → **Pages** →
**Upload assets** → drag `index.html` in → deploy.

### GitHub quick-start

```bash
cd github_repo
git init
git add .
git commit -m "Solar Shop homepage — contest build (single-file, Cloudflare-ready)"
git branch -M main
git remote add origin https://github.com/<your-user>/<your-repo>.git
git push -u origin main
```

## Notes

- No build tooling, no package.json, no CDN links — nothing to install.
- Page weight ≈ 6.5 MB (all photography + 6 woff2 faces embedded as data URIs);
  Cloudflare's CDN gzips/brotlis it automatically.
- Fonts, colours and spacing tokens are editable at the top of the embedded
  `<style>` block (see `:root` custom properties).
