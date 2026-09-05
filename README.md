# SAHAS Tourism

Website for an adventure tour operator based in Rajkot, Gujarat.

One HTML file. No framework, no build step, no dependencies to install — open it and it
runs. The only third-party code is a vendored copy of Three.js.

## The constraint

The site is mostly viewed on mid-range Android phones on Indian mobile data. That ruled
out a framework bundle before anything else was decided. Everything is inlined into a
single ~790-line document so the page is usable after one request, and the heavy assets
(the 3D model, the photography) load after the text is already readable.

## What's in it

- **A 3D Indian Roller** — the state bird of Gujarat — rendered on a full-viewport canvas
  with Three.js, loaded as a compressed GLTF via meshopt.
- **Letter-reveal headlines**, where particles resolve into type as each section enters.
- **Real photography only.** No stock imagery and no AI-generated images anywhere on the
  site; every photo is from an actual trip the operator ran.
- **A reduced-motion path** that disables the canvas and animation entirely for users who
  ask for it at the OS level.

## Stack

Vanilla HTML, CSS and JavaScript · Three.js r161 · GLTF + meshopt · Canvas 2D

## Running it

```bash
python3 -m http.server 8899
```

Then open `http://localhost:8899`. That's the whole toolchain.

## Layout

```
index.html        markup, styles and behaviour, inlined
assets/models/    compressed GLTF bird
assets/img/       trip photography
vendor/           Three.js r161 + loaders
```
