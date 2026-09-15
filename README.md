# 👑 Qin Shi Huang on a Polar Bear

秦始皇骑北极熊 — a crowned emperor riding a polar bear across an arctic night,
animated entirely from a single self-contained HTML file (inline SVG, SMIL +
CSS animations, **no JavaScript, no dependencies**).

## Features

- **Walk cycle solved, not eyeballed.** Each leg is a rigid rod pivoting on its
  hip. During stance the foot is pinned to the ground (an exact `asin` curve),
  so the paws never slide: measured world-space foot slip is **< 0.01 u** over
  a full 62.4 u stride.
- **Body bob derived from the same model.** The support legs reach ±18.34° at
  the extremes, so the hip rides 3.15 u low there and 0.49 u high when a leg
  passes vertical — a 0.3 s loop (four support events per gait cycle).
- **Ground scroll locked to the stride.** The detail band is exactly 100 u
  periodic and shifts at the bear's own speed (52.02 u/s), so standing paws and
  moving snow agree.
- **Four-phase walk** — each foot a quarter cycle apart, with paw lift from a
  scale-Y about the hip.
- **Rotation centres are explicit** (`animateTransform` values carry their own
  centres), so the scene stays pixel-perfect at any window size or zoom level.
- Flat vector scene: aurora ribbons, twinkling stars, flat cream moon,
  snow-capped peaks, drifting snowfall, and the emperor's 冕冠 crown with gold
  band and bead fringe, gold-trimmed black robe, red-and-gold saddle blanket.
- The caption is real HTML text, so a full-bleed crop can never eat it.
- `prefers-reduced-motion` stops the CSS-driven motion (ground scroll,
  snowfall, star twinkle, aurora, body bob). The limb swings are SMIL and
  continue — SMIL can't be switched off from CSS without scripting.

## Run it

Just open `index.html` in any modern browser — no build step, no server needed.

Or view the live page: **https://laiyewfai.github.io/qin-shihuang-polar-bear/**

## License

MIT
