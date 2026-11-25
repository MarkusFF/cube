# CUBE

**Defender of the polyverse.** In development for over a decade.

A playable take on the 2006 parody game ad *Cube*. Roll a white cube one tile at a time, collect the diamonds, reach the goal, and every goal leads to a new colour level: Blue, Green, Orange, and finally Red, where you face the dreaded Cone.

Rendered at 320×240 and pushed through JPEG compression twice per frame, at roughly 20 fps. Cutting edge 3d graphics.

**Play:** open `index.html` in a browser (or the GitHub Pages site for this repo).

## Controls

| Key | Action |
| --- | --- |
| Arrows / WASD | Roll Cube |
| Any key | Continue |
| M | Mute |
| R, R | Back to title |
| Z (title screen) | Zen mode: endless floor, no enemies, Esc to leave |
| C (title screen) | Cheat mode: 1–4 jump to a level, K collect all diamonds, B big head, N next level |

On touch screens: swipe or use the on-screen pad.

## Music

`music/` holds the soundtrack, composed for the game and rendered from the same synth code it plays live:

- `cube-01-title-theme.mp3`
- `cube-02-level-theme.mp3` / `.wav` (seamless loop)
- `cube-03-the-cone.mp3` / `.wav` (seamless loop)

`music/render-soundtrack.html` re-renders the tracks (it uses an `OfflineAudioContext`; call `render('title' | 'level' | 'cone')` from the console to get a base64 WAV).

## Tech

One HTML file, [three.js r128](https://threejs.org/) from cdnjs, Web Audio for music and sound, and the browser's speech synthesis for the narrator.
