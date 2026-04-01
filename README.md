# strudel phreak

browser-based live coding music playground. no server, no deps, just vibes.

built on [strudel](https://strudel.cc) — a JavaScript port of TidalCycles for algorithmic pattern music.

## what it does

write patterns, hit ctrl+enter, hear music. everything runs in the browser via Web Audio API.

- 4 presets: deep house, breakcore, acid, ambient
- live scope visualizer
- BPM control
- inline help (ctrl+/)

## presets

**deep house** — classic 4-on-the-floor with filtered bass, chord stabs, vocal chops

**breakcore** — amen break chaos, distorted bass, noise bursts

**acid** — 303-style resonant filter sweeps, kick + hihat groove

**ambient** — slow evolving pads, sparkle textures, deep tones

## keyboard shortcuts

- `ctrl+enter` evaluate code
- `ctrl+/` toggle help
- `ctrl+.` silence all

## extend it

write your own patterns in the editor. the strudel API is powerful:

```
// layer patterns with stack()
stack(
  s("bd ~ sd ~").gain(0.8),
  note("c2 eb2 g2 bb2").sound("sawtooth").lpf(800),
  s("~ hh ~ hh").pan("<-1 1>")
)
```

[full strudel docs](https://strudel.cc/learn/)

## run locally

just open `index.html` in a browser. no build step.

## license

do whatever you want
