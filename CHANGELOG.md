# Changelog
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
