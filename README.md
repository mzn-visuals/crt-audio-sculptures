# CRT // AUDIO SCULPTURES

A music visualizer that lives in a single HTML file. Search any track, hit play, and watch a 3D audio-reactive sculpture render itself in real time — complete with synced lyrics, a CRT phosphor shader stack, and adaptive colors pulled from album art.

Built by [mzn.visuals](https://www.tiktok.com/@mzn.visuals).

**[Try it live →](https://mzn-visuals.github.io/crt-audio-sculptures/)**

---

## What it looks like

- 3D WebGL scene powered by Three.js
- Bloom, afterimage, and CRT scanline post-processing
- Audio-reactive geometry that moves with the beat
- Synced lyrics floating in 3D space
- Album art colors that bleed into the whole scene
- Discord Rich Presence — shows what you're listening to right from Discord (Windows app)

---

## How to use it

There are two fully-working, out-of-the-box ways to use it — Windows app and live site — plus a local/dev option if you want to run or edit the source yourself.

### Option 1 — Windows app

Download the latest `.exe` installer from [Releases](../../releases). Native Windows app, works right out of the box, and includes Discord Rich Presence.

### Option 2 — Live site

Open the [live version](https://mzn-visuals.github.io/crt-audio-sculptures/) in your browser. Works exactly the same as the Windows app — full YouTube search and streaming, no setup — just without Discord Rich Presence, since that needs native access to Discord that a browser tab can't get.

### Option 3 — Local / dev (HTML + proxy)

For running it locally or editing the code. The `index.html` and `proxy.js` files are bundled together in the [Releases](../../releases) as well. The proxy handles YouTube search and stream resolution so everything works without CORS issues.

**Requirements:**
- [Node.js 18+](https://nodejs.org)
- [yt-dlp](https://github.com/yt-dlp/yt-dlp)

**Run it:**
```bash
node proxy.js
```

Then open `index.html` in your browser. The app detects the local proxy automatically.

---

## Features

**Playback & search**
- YouTube search — search by track name, results pull from YouTube Music
- Paste-and-play support for YouTube and YouTube Music links
- Local file support — drag in any audio file, works fully offline
- Previous/next track controls, with the next track prewarmed the instant the current one starts, so there's no loading delay on transition
- Seek bar showing playback position and total duration
- Autoplay radio mode — keeps the music going after a track ends, picking similar songs the way YouTube Music does
- Queue — line up tracks, see a live item count, jump to any queued track directly, minimize/expand the panel
- Volume control — click to mute/unmute, scroll or drag to adjust, with a live percentage readout while adjusting; level persists across reloads

**Visuals & shader**
- CRT shader stack — scanlines, phosphor glow, screen curvature
- Adaptive color — scene colors extracted from album art in real time
- RGB mode — override colors manually
- F11 fullscreen toggle
- Lavender-to-cyan gradient theme across all controls, transport buttons, the seek bar, and status indicators

**Lyrics**
- Synced lyrics, auto-fetched and animated in 3D, beat-reactive
- Font, size, stretch X/Y, opacity, color, and glow color are all customizable and persist across reloads

**Quality of life**
- Collapsible control sections (Playback & Search, Shape & Style, Colors, Audio Reactivity, Effects & CRT, Lyrics), each remembering its open/closed state across reloads
- Browser tab title shows the currently playing track and artist
- Discord Rich Presence — broadcasts what's currently playing (Windows app only)
- Settings persist across reloads for every control on the panel

---

## Stack

- [Three.js](https://threejs.org) — 3D rendering
- [Web Audio API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Audio_API) — audio analysis
- [lrclib.net](https://lrclib.net) — synced lyrics
- [yt-dlp](https://github.com/yt-dlp/yt-dlp) — stream resolution via local proxy
- [Tauri](https://tauri.app) — native Windows packaging, with Discord Rich Presence wired in directly via Discord's native IPC

---

## Project structure

```
crt-audio-sculptures/
├── index.html    — the entire app
└── proxy.js      — local CORS proxy (only needed for local dev / editing the code)
```

---

## Star history

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/svg?repos=mzn-visuals/crt-audio-sculptures&type=Date&theme=dark" />
  <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/svg?repos=mzn-visuals/crt-audio-sculptures&type=Date" />
  <img alt="Star History Chart" src="https://api.star-history.com/svg?repos=mzn-visuals/crt-audio-sculptures&type=Date" />
</picture>

---

## License

Personal / non-commercial. Don't redistribute without credit.
