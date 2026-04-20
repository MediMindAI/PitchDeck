# MediMind Pitch Deck

Self-contained 10-slide investor deck for the $200K round.

## Files

```
MediMind-Pitch/
├── MediMind-PitchDeck.html        ← open this in a browser
├── Market-Research-Backup.md      ← verified sources for every market number
├── assets/
│   ├── logo-horizontal-dark.svg   ← cover slide logo
│   ├── logo-horizontal-light.svg  ← for light backgrounds
│   ├── logo-icon-dark.svg         ← footer watermark
│   ├── logo-icon-light.svg        ← alt icon
│   ├── favicon.svg                ← browser tab
│   ├── apple-touch-icon.png       ← iOS/macOS share preview
│   └── og-image.png               ← Slack/LinkedIn/email preview
└── README.md                       ← this file
```

**Brand-aligned** with `/Users/toko/Desktop/medimind-brand/` (v1.0, 2026-04-18) — logos, tokens, and social assets are the authoritative brand files.

## How to view

Double-click `MediMind-PitchDeck.html` or open it in Chrome/Safari.

## Slide list (11 slides — matches your outline + Ask + Terms explainer)

| # | Slide |
|---|---|
| 1 | Cover |
| 2 | Hook — Practicing medicine without AI is malpractice |
| 3 | Crisis — When a patient with AI knows more than a doctor |
| 4 | Solution — AI-native medical ecosystem |
| 5 | Why AI-Native Wins — One unified system, tiny team |
| 6 | Team — Doctors building for doctors + Advisory |
| 7 | Market Opportunity — TAM / SAM / SOM (sourced) |
| 8 | Progress — 13-month timeline (incl. Feb 2026 Innovative Startup award) |
| 9 | Ambition — Georgia → Region → Global |
| 10 | The Ask — $200K milestone: 30 contracts, cover Georgia, start regional |
| 11 | What You're Investing In — SAFE/Convertible Note terms + plain English |

## Keyboard controls

- **Arrow keys** — next / previous slide
- **`F`** — fullscreen (use this when presenting)
- **`S`** — opens speaker-notes window (use on a second screen)
- **`ESC`** — overview grid of all slides
- **`?`** — keyboard shortcut help

## Export to PDF (for cold-sending)

1. Open this in Chrome: `file:///Users/toko/Desktop/MediMind-Pitch/MediMind-PitchDeck.html?print-pdf`
2. `Cmd+P` → Destination: Save as PDF
3. More settings → **Paper size: A4 Landscape**, **Margins: None**, **Background graphics: ON**
4. Save

## Things to customize before sending

Search the HTML for `[FILL IN` and replace:

- Line near Slide 6 (Team) — co-founder name, role, background
- Line near Slide 6 — your own background
- Cover slide footer — real email + website

## Swapping placeholder elements for real assets

**Team headshots (Slide 6):** Currently shows initials in gradient circles. To swap for real photos, find each `<div class="team-avatar">XX</div>` and replace with:
```html
<div class="team-avatar" style="background: url('assets/lasha.jpg') center/cover;"></div>
```
Drop images in the `assets/` folder first.

**MediMind logo:** Currently the wordmark is text-only in bold Inter. If you have a logo SVG, drop it in `assets/` and replace the `<h1>MediMind</h1>` in the Cover section with `<img src="assets/logo.svg" alt="MediMind" />`.

## Design system

Fully aligned with the MediMind brand book at `/Users/toko/Desktop/medimind-brand/`.

**Palette** (CSS variables, defined once in `:root`):
- Primary navy: `var(--emr-primary)` · `#1a365d`
- Secondary blue: `var(--emr-secondary)` · `#2b6cb0`
- Accent bright: `var(--emr-accent)` · `#3182ce`
- Light accent: `var(--emr-light-accent)` · `#bee3f8`
- Success green: `var(--emr-success)` · `#38a169`
- Warning orange: `var(--emr-warning)` · `#dd6b20`
- Error red: `var(--emr-error)` · `#e53e3e`
- Primary gradient: `var(--emr-gradient-primary)`

**Typography:** System font stack — zero CDN dependency, renders natively on macOS/iOS/Windows/Android, includes Noto Sans Georgian for Georgian text fallback.

**Logo:** Real brand SVG (not text). On cover: `assets/logo-horizontal-dark.svg`. Footer icon: `assets/logo-icon-dark.svg`.

## Offline mode

Only reveal.js (CSS + JS) loads from a CDN — fonts are now system-native. If presenting without internet:
1. Download [reveal.js 4.6.1](https://github.com/hakimel/reveal.js/archive/refs/tags/4.6.1.zip) → copy `dist/reveal.css` and `dist/reveal.js` into `assets/`
2. Update the 2 reveal.js CDN links in the HTML `<head>` to point at `assets/...`

System fonts (San Francisco / Segoe UI / Roboto) render instantly — no font-flash even offline.
