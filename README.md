# Orbit Dash — Best Game 01 Bounty Entry

[![make.fun bounty](https://img.shields.io/badge/make.fun-bounty-blue)](https://make.fun/bounty/best-game-01)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Node 22](https://img.shields.io/badge/node-22-green)](https://nodejs.org)
[![Game](https://img.shields.io/badge/game-orbit%20dash-ff6b9d)](https://make.fun/bounty/best-game-01)

An original arcade game where you pilot a ship in orbit around a planet, dodging asteroids and collecting stars. Built for the [make.fun best-game-01 bounty](https://make.fun/bounty/best-game-01).

## Game

**Orbit Dash** is a 2D canvas arcade game. You control a ship orbiting a central planet. Rotate with **LEFT/RIGHT** or **A/D**, and **SPACE** to dash inward. Dodge incoming asteroids, collect golden stars for points, and survive escalating waves.

- **Goal**: Survive as long as possible, score points
- **Controls**: Arrow keys / WASD to rotate, SPACE to dash
- **Lives**: 3 — each asteroid hit costs one life and 50 points
- **Waves**: Difficulty increases every ~30 seconds
- **Scoring**: +5 per asteroid dodged, +100 per star collected

## Play

Serve the `game/` directory with any static file server:

```sh
node serve.ts   # serves game/ on http://localhost:8080
```

Or simply open `game/index.html` in a desktop browser. No network requests are made — everything is self-contained.

## Build

Requires Node.js 22:

```sh
npx tsx main.ts   # builds dossier.json into MAKEFUN_OUTPUT_DIR (default /output)
```

## Project Structure

```
main.ts                      # Node 22 entry point, builds the dossier
serve.ts                     # Local dev static server
game/index.html              # The complete game (HTML/CSS/JS inline, no deps)
screenshots/                 # 4 real renders of gameplay
  ├── 01-title.png           # Title screen
  ├── 02-playing.png         # Early gameplay
  ├── 03-action.png          # Mid-game action
  └── 04-later.png           # Later wave gameplay
vendor/makefun-game.ts       # make.fun game library (unchanged from kit)
LICENSE                      # MIT (SPDX)
.makefun/owner.json          # Wallet claim file
```

## License

MIT — see [LICENSE](LICENSE).
