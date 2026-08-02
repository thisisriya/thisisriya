# Setup — 5 minutes

## 1. The repository has to be named exactly right

The profile README only renders on your page if the repo name **matches your username exactly**:

```
github.com/riya2204-coder/riya2204-coder
```

Create it, tick **"Add a README file"**, make it **Public**. GitHub will show a hint like *"you found a secret!"* — that's how you know the name is correct. Then paste in `README.md`.

> Using a different handle? Open `README.md` and find-and-replace every `riya2204-coder` with the correct username. **Every stats image will be blank until this matches a real account** — this is the single most common reason images don't show.

## 2. Turn on the snake animation

The snake image 404s until the workflow runs once. In your profile repo:

1. Create the folder path `.github/workflows/`
2. Upload `snake.yml` into it
3. Go to the **Actions** tab → *Generate Snake Animation* → **Run workflow**

After ~30 seconds it creates an `output` branch containing `snake.svg`, and the image in the README starts rendering. It refreshes itself daily after that.

## 3. If an image still doesn't load

| Symptom | Cause | Fix |
|---|---|---|
| Stats / streak / trophies blank | Username mismatch, or the free host is rate-limited | Confirm the username; wait a few minutes and hard-refresh |
| Contribution graph blank | `github-readme-activity-graph` has occasional downtime | Wait, or delete that one line — everything else stands on its own |
| Snake blank | Workflow hasn't run yet | Step 2 above |
| Everything blank on first push | GitHub's image proxy is still caching | Hard-refresh (`Ctrl/Cmd + Shift + R`) after a minute |

Nothing in this README depends on a private URL or an account you don't have — every image is generated from your public GitHub data.

## 4. Things to fill in later

- **Project repo buttons** — both currently point at your repositories tab. Swap them for the real repo URLs when SuryaShield and FindIt.AI go public. They're marked with HTML comments.
- **Portfolio / X** — the `#` placeholders in the header.
- **Coding profiles** — LeetCode, Codeforces, CodeChef, HackerRank, GeeksforGeeks are shown as dimmed, reserved badges. There's a commented block in the Coding Profiles section with ready-made stat cards; uncomment one and add your handle when a profile is worth showing.

## 5. Optional polish

Pin **SuryaShield** and **FindIt.AI** on your profile once they're public. A README that promises two projects and a profile with zero pinned repos is the one thing a recruiter will notice.
