# Setup &amp; Troubleshooting

## What was broken

| Image | Why it failed | Status |
|---|---|---|
| Hero banner | `capsule-render.vercel.app` was offline — free Vercel instance, goes down often | **Removed.** Header is now HTML + typing SVG |
| GitHub Stats, Top Languages | Pointed at `riya2204-coder`, which isn't your account | **Fixed** → `thisisriya` |
| Streak, Trophies | Same wrong username | **Fixed** → `thisisriya` |
| Typing SVG text cut off | Line was wider than the 600px canvas | **Fixed** — 620px canvas, 18px type |
| Snake | Workflow hasn't run yet | See step 2 |
| Contribution graph | Nothing — it was already working | Untouched |

Everything now uses only hosts that rendered correctly in your screenshots: **shields.io**, **komarev**, **readme-typing-svg.demolab.com**, **github-readme-activity-graph**, plus the three GitHub stat services with the corrected handle.

## 1. Replace the README

Your repo `thisisriya/thisisriya` already exists and renders — just replace the contents of `README.md`. Then **hard-refresh** (`Cmd/Ctrl + Shift + R`).

> GitHub's image proxy caches failures. If a stat card still looks broken for a few minutes after the fix, that's the old 404 being served from cache — it clears on its own.

## 2. Turn on the snake

1. In `thisisriya/thisisriya`, create the path `.github/workflows/snake.yml` and paste in the `snake.yml` file
2. **Actions** tab → *Generate Snake Animation* → **Run workflow**
3. Wait ~30 seconds — it creates an `output` branch with `snake.svg`, and the image starts rendering

It re-runs daily on its own after that.

## 3. If a stat card is still blank

`github-readme-stats.vercel.app` and `github-profile-trophy.vercel.app` are free shared instances that rate-limit under load. A blank card there is temporary, not a config error — it usually returns within an hour.

If one is persistently down, delete that single `<img>` line. Nothing in the layout depends on any other image being present.

## 4. Still to fill in

- **Project buttons** — both point at your repositories tab. Swap in the real URLs when SuryaShield and FindIt.AI are public (marked with HTML comments).
- **Portfolio / X** — the `#` placeholders in the header.
- **Coding profiles** — dimmed reserved badges for now. There's a commented block with ready-made stat cards in that section.

## 5. The thing that matters most

Pin **SuryaShield** and **FindIt.AI** once they're public. A README that describes two strong projects sitting above an empty pinned-repos row is the gap a recruiter will notice first — and right now your contribution graph reads zero, which is the one number the README can't talk its way around.
