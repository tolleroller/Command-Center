# Command Center

Personal life dashboard — a progressive web app (PWA) for iPhone and desktop.

**Live:** [tolleroller.github.io](https://tolleroller.github.io)

## What it is

A single-file personal command center with:

- **Home** — wealth snapshot, goals progress, today’s focus, project pulse, vision board
- **Finance** — holdings, savings rate, net worth, recommended next steps
- **News** — curated markets, SpaceX/Tesla, tech/AI, science, policy, UAP, trending
- **Entertainment** — movies, TV, music tailored to taste
- **Projects** — active work and personal project trackers
- **Goals** — cash buffer, emergency savings, homestead, remote PE consultancy
- **Health** — supplements, routines, nature / recovery
- **Lab** — innovation ideas, agents, experiments

Data persists in the browser (`localStorage`). No account required.

## How to use on iPhone

1. Open the live site in **Safari**
2. Share → **Add to Home Screen**
3. Launch from the home-screen icon (full-screen PWA)

Chrome on iOS does not support Add to Home Screen the same way — use Safari.

## Updating

Replace `index.html` in this repo (upload / commit). GitHub Pages redeploys automatically. Hard-refresh or re-open the home-screen app to see changes.

## Stack

- Single `index.html` (HTML + Tailwind CDN + vanilla JS)
- Optional embedded images (base64) for offline-friendly assets
- Chart.js where charts are used
- No backend; static hosting via GitHub Pages

## Privacy

Personal dashboard. No analytics, no third-party auth. Finance numbers are illustrative / manually maintained for now.

## Author

Built iteratively as a personal MVP — civil engineering / remote PE / autonomy focused.
