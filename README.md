# CRT // AUDIO SCULPTURES

A music visualizer that lives in a single HTML file. Search any track, hit play, and watch a 3D audio-reactive sculpture render itself in real time — complete with synced lyrics, a CRT phosphor shader stack, and adaptive colors pulled from album art.

Built by [mzn.visuals](https://www.tiktok.com/@mzn.visuals).

---

## What it looks like

- 3D WebGL scene powered by Three.js
- Bloom, afterimage, and CRT scanline post-processing
- Audio-reactive geometry that moves with the beat
- Synced lyrics floating in 3D space (auto-fetched from lrclib.net)
- Album art colors that bleed into the whole scene

---

## How to use it

### Option 1 — Just open the file
Download `index.html`, open it in your browser. You can load local audio files right away.

For YouTube search to work, you'll need the local proxy running (see below).

### Option 2 — With the local proxy (full experience)

The proxy handles YouTube search and stream resolution so everything works without CORS issues.

**Requirements:**
- [Node.js 18+](https://nodejs.org)
- [yt-dlp](https://github.com/yt-dlp/yt-dlp)

**Run it:**
```bash
node proxy.js
```

Then open `index.html` in your browser. The app detects the proxy automatically.

---

## Features

- **YouTube search** — search by track name, results pull from YouTube Music
- **Local file support** — drag in any audio file, works offline
- **Synced lyrics** — auto-fetched and animated in 3D, beat-reactive
- **CRT shader** — scanlines, phosphor glow, screen curvature
- **Adaptive color** — scene colors extracted from album art in real time
- **RGB mode** — override colors manually
- **Fully offline-capable** for local files (no proxy needed)

---

## Stack

- [Three.js](https://threejs.org) — 3D rendering
- [Web Audio API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Audio_API) — audio analysis
- [lrclib.net](https://lrclib.net) — synced lyrics
- [yt-dlp](https://github.com/yt-dlp/yt-dlp) — stream resolution via local proxy

---

## Project structure

```
crt-audio-sculptures/
├── index.html    — the entire app
└── proxy.js      — local CORS proxy (optional but recommended)
```

---

## License

Personal / non-commercial. Don't redistribute without credit.
