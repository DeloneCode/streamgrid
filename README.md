# StreamGrid — Multi-Stream Twitch Viewer

A single-file web app to watch multiple Twitch streams simultaneously in a smart auto-adjusting grid.

![StreamGrid Screenshot](screenshot.png)

---

## Features

- **Add streams** — paste a Twitch URL or just type a channel name
- **Smart grid layout** — auto-adjusts as you add streams (1=full, 2=side-by-side, 3=2+1, 4=2×2, 5=2+3, 6=3×2, etc.)
- **Persistence** — streams survive page refreshes (saved to `localStorage`)
- **Drag to reorder** — rearrange tiles by dragging
- **Layout lock** — pin the grid to a fixed column count instead of auto
- **Theater mode** — expand one stream to ~70% width with others stacked in a sidebar
- **Fullscreen** — per-tile fullscreen with one click
- **Hide/show header** — collapse the top bar to maximize screen real estate
- **Mute all** — one button to mute every stream simultaneously
- **Presets** — save and load named groups of streams (e.g. "Friday Night Squad")
- **Remove** — remove any stream individually

---

## Usage

1. Open `index.html` in your browser (or serve it locally)
2. Type a channel name or paste a Twitch URL into the input
3. Click **Add** or press **Enter**
4. Add as many streams as you want — the grid adjusts automatically

> **Note:** The Twitch embed requires `parent=localhost` when running locally. For other hostnames, update the `parent` parameter in `buildSrc()`.

---

## Stack

- Vanilla HTML / CSS / JS — zero dependencies, single file
- [Twitch Player Embed API](https://dev.twitch.tv/docs/embed/everything/)
- Google Fonts: Space Mono + Barlow Condensed
- CSS flexbox grid + CSS Grid for theater mode
- HTML5 Drag and Drop API
- `localStorage` for persistence

---

## Running Locally

```bash
# Any static server works, e.g.:
npx serve .
# or
python -m http.server 8080
```

Then open `http://localhost:8080`.

---

## Project Structure

```
twitchviewer/
└── index.html   # entire app — styles, markup, and logic
```

---

Made with Claude Code.
