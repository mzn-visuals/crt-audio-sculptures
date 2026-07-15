# Changelog
## [1.7] - 2026-07-15

### Added

* Full album art color adaptation — the entire UI now derives its palette from the current track's album art, including panel backgrounds, borders, buttons, seek bar, volume fill, search input, search results, queue items, status pills, section dividers, scrollbars, and the CRT frame glow.
* Retractable wings — playback controls (previous, play/pause, next) and the volume control now live in slide-out wings flanking the pill, revealed on hover with a short delay and smoothly retracted on mouse leave.
* Dynamic scanline tinting — the CRT scanline texture is preserved but its color adapts to the album art palette rather than staying neutral.
* Lyric glow color now updates automatically with the album art palette.

### Changed

* Complete UI overhaul: the player is now a morphing pill/card hybrid — collapsed it sits as a compact pill with album art, track info, and a settings cog; clicking the cog expands it into a full settings card with smooth cross-fade transitions.
* All UI surfaces (backgrounds, borders, fills, glows) are tinted with a deeply darkened version of the album art's dominant color as the base panel color, with accent colors applied on top.
* Settings panel sections (Playback & Search, Shape & Style, Colors, Audio Reactivity, Effects & CRT, Lyrics) are now displayed as collapsible groups inside the expanded card.
* Color adaptation now updates every UI element site-wide rather than only a subset of buttons and progress bars.

### Fixed

* Settings cog button was unclickable when the pill was collapsed due to the seek scrubber sitting on top of it — fixed by raising the pill content layer above the scrubber.
* Seek scrubber no longer covers the entire expanded settings card.
* Pill expand/collapse and wing slide transitions restored to their original timing and easing after being disrupted by color adaptation changes.

## [1.6] - 2026-06-27

### Added

* A Windows release of CRT // AUDIO SCULPTURES is now available for download and use. No "proxy.js" required, works right out of the box.
* Discord RPC (Rich Presence) - now works with the Windows release.

## [1.5] - 2026-06-25

### Fixed

* Search bar's active/focus border now matches the lavender tone of the rest of the controls, instead of standing out in cyan.

## [1.4] - 2026-06-23

### Added

* Live percentage readout on the volume button — appears when scrolling, clicking, or dragging the slider, then reverts to the mute/unmute icon.
* Volume level now persists across reloads.
* Collapsible tab sections (Playback & Search, Shape & Style, Colors, Audio Reactivity, Effects & CRT, Lyrics) now remember their open/closed state across reloads; first-time default is everything closed except the autoplay queue, on both desktop and mobile.
* Lyrics font, size, stretch X/Y, opacity, color, and glow color now persist across reloads.
* Browser tab title now shows the currently playing track's name and artist, reverting to "CRT // AUDIO SCULPTURES" when paused or idle.

### Changed

* Music controls now use the same lavender-to-cyan gradient as the search button across all backgrounds (transport buttons, play/pause, volume, seek bar), extended to every other matching cyan element site-wide (status dots, active search results, queue buttons).
* Top-left status dot and color-adapt indicator dot now blink in sync with the now-playing dot.
* Preset pill now shows only the random descriptor name, dropping the numeric stats suffix.
* Initial load status text changed from "ready" to "happy visualizing"; the brief status shown between track transitions is now blank instead of "ready".
* Queue collapse arrow enlarged for visibility.
* Page title changed to "CRT // AUDIO SCULPTURES".

### Fixed

* Clicking mute now visually drops the volume slider to 0 and restores it on unmute, instead of leaving the slider in place.
* Removed the small blinking dot that sat above the volume control.

## [1.3] - 2026-06-23

### Fixed

* Stop button removed from the player controls.
* Next track is now prewarmed the moment the current one starts playing, removing the loading delay on transition.
* Local file picker and the usage hint below it now span the full width of the panel instead of shrinking to content size.
* Queue panel now shows a live item count, can be minimized/expanded, and each track has its own play button to jump straight to it.
* Layout: search results now render directly under the search bar, with the player card below them; Previous/Play/Next are centered above the seek bar with volume pinned to the right edge.
* Searching and playing a new song now starts a fresh autoplay radio mix and clears the previous queue, but playing within the same list (next, previous, or jumping to a queued track) no longer resets it.

## [1.2] - 2026-06-22

### Added
- Previous/next track buttons.
- Queue feature, allowing users to queue songs one after another.
- Seekbar showing the current playback position and the song's total duration.
- Support for pasting and directly playing links from both YouTube and YouTube Music.
- Autoplay/radio mode that starts automatically once a song finishes, based on the played song (similar to YouTube Music).
- Volume button that mutes/unmutes on click and reveals a volume slider on hover; scrolling the slider adjusts volume in 10% increments.

### Fixed
- "Now playing" pill at the top of the GUI now displays the song's name instead of "playing file".
- Redesigned music controls and merged them with the now playing bar under the search bar, combining play/pause into a single button.

## [1.1] - 2026-06-21

### Fixed
- Parsing issue that occurred on the first search (no longer requires reloading the page)

Happy visualizing!
