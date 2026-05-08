# InfinixLeverage

AI-powered customer support platform. Never miss another call, never lose another customer.

## Pages

| File | URL | Description |
|------|-----|-------------|
| `index.html` | `/` | Main landing page — hero, inbound/outbound call demos, CTA |
| `ai-support-website.html` | `/ai-support-website` | Meta-refresh redirect to `index.html` |
| `hero.html` | `/hero` | Kalalou Hero section |
| `teams.html` | `/teams` | Team page |
| `questionnaire.html` | `/questionnaire` | AI system questionnaire for Kalalou |
| `kalalou-presentation.html` | `/kalalou-presentation` | Kalalou AI Leverage presentation |
| `kalalou-presentation-page.html` | `/kalalou-presentation-page` | Kalalou presentation page view |

## Local Development

No build step needed. Serve the root directory with any static server:

```bash
npx serve .
# or
python -m http.server 8000
```

Then open `http://localhost:8000`.

## Deployment

Deployed on Vercel as a static site. Files in the repo root are served directly — no build process runs. `vercel.json` handles routing and clean URLs.

Push to `main` to deploy.

## Mobile Notes

- iPhone mockup uses `aspect-ratio: 1/2` + `max-width: 360px` — scales fluidly on all screen sizes without fixed pixel heights.
- Slide-to-call handlers use the Pointer Events API (`pointerdown` / `pointermove` / `pointerup`) for unified mouse and touch support. `touch-action: none` prevents scroll conflicts.
- Outbound call screen animates a "ringing..." pulse state once the user submits their number.
- All CSS is mobile-first (base styles target mobile; `min-width` breakpoints scale up to tablet/desktop).

## Branding

- **Favicon** (`favicon.svg`): Black rounded-rect background, white infinity stroke — renders at any size including browser tab and iOS home screen.
- **Nav logo** (`images/logo.svg`): Same infinity path with a white-to-grey gradient, transparent background — used as `<img>` in the nav bar.
- **Color palette**: `#000` / `#0a0a0a` backgrounds, `#fff` primary text, `#888` secondary text. Full light-mode support via CSS custom properties.

## Tech Stack

- Pure HTML / CSS / JavaScript — no framework, no build step
- [Three.js](https://threejs.org/) (CDN) — animated wave background on the hero
- Vercel — static hosting with `vercel.json` routing
