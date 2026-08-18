# webgl-glass-sticker

A WebGL demo: a liquid-glass "glass-object" effect layered over a falling-sticker scene, built with **Three.js** and a **lil-gui** live debug panel.

## What's inside

- `glass-sticker-debug.html` — the single-file demo. No build step.
  - Stickers fall continuously via an `InstancedMesh` driven by a custom shader atlas (size & count are tunable).
  - Mouse movement drives a sine-distortion post-process that follows the cursor.
  - Click anywhere to burst a cluster of stickers.
  - Glass material uses `MeshPhysicalMaterial` with transmission + dispersion (canvasui.dev `glass-object` style).

## Run

No bundler needed:

```bash
# 方式一：直接双击打开 glass-sticker-debug.html
# 方式二：本地静态服务（推荐，避免某些 CDN/CORS 限制）
python3 -m http.server
# 然后浏览器访问 http://localhost:8000/glass-sticker-debug.html
```

## Tech stack

- Three.js r0.169 (loaded via CDN import map)
- lil-gui 0.19 for the debug panel
