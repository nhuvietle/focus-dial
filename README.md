# Focus Dial

A 60-minute visual focus timer. A red disk shows the time left and shrinks as it runs down. One HTML file, no dependencies, works offline, installs as a desktop app from Chrome or Edge.

## Use

| Action | How |
|---|---|
| Set time | Drag around the dial, pick a preset, or use `↑` `↓` (±1 min, `Shift` ±5) |
| Start / pause | `Space` or the Start button |
| Reset | `R` |
| Presets | 25 / 45 / 60 / 90 min, or `1`–`4`. Over 60 min, an outer ring shows the second lap. |
| Floating window | `P` or **Float on top**. A small dial that stays above other apps. Chrome/Edge only, not Safari. |
| End of session | Optional soft chime and system notification. No ticking while it runs. |
| Today's log | Top right: completed sessions and focused minutes. Resets each day, stored per machine. |

## Publish on GitHub Pages (one time)

1. Create an empty GitHub repo, e.g. `focus-dial`.
2. Push this folder:
   ```bash
   git add . && git commit -m "Focus Dial v1"
   git branch -M main
   git remote add origin https://github.com/<you>/focus-dial.git
   git push -u origin main
   ```
3. On GitHub: **Settings → Pages → Build and deployment → Deploy from a branch → `main` / `(root)` → Save**.
4. After a minute the app is live at `https://<you>.github.io/focus-dial/`.

## Install on each machine

- **Chrome (Mac or Windows):** open the URL → click the install icon in the address bar (or the **Install app** button on the page). On Mac it appears in Launchpad/Spotlight and can be kept in the Dock.
- **Edge (Windows):** open the URL → **⋯ → Apps → Install this site as an app**. Pin it to the taskbar.

Updates: edit `index.html`, push, and the next launch on each machine picks up the change.

## Run locally

```bash
python3 -m http.server 5178 --directory .
```

Then open http://localhost:5178. Offline caching and install need `http://localhost` or `https://`. Opening the file directly (`file://`) still runs the timer.
