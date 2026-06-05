<div align="center">
# 🍄 Super IUBI Bros

### A pixel-perfect, NES-style 2D platformer that runs in your browser

**No engine. No frameworks. No build step. One single HTML file.**

[![Play](file:///Users/jongurakuqi/Library/Mobile%20Documents/com~apple~CloudDocs/index.html).
[![License](https://img.shields.io/badge/License-MIT-fac000?style=for-the-badge)](LICENSE)
[![Made with JavaScript](https://img.shields.io/badge/Made_with-Vanilla_JS-5c94fc?style=for-the-badge&logo=javascript&logoColor=white)](#)
[![HTML5 Canvas](https://img.shields.io/badge/HTML5-Canvas-00a800?style=for-the-badge&logo=html5&logoColor=white)](#)

</div>

---

## ▶️ Watch the Live Demo

> ### 👉 **[CLICK HERE TO PLAY IN YOUR BROWSER](https://jongurakuqi.github.io/Super-Mario-Game-IUBI/)** 👈

No download, no install - the full game runs instantly on desktop and mobile.

> **Heads up:** the live link above assumes GitHub Pages is enabled for this repo. See the [Deploy Your Own Live Demo](#-deploy-your-own-live-demo) section below to switch it on in two clicks.

<div align="center">

<!-- Replace gameplay.gif with a real screen-recording of the game -->
<img src="gameplay.gif" alt="Super IUBI Bros gameplay" width="640">

*Drop a screen-recording named `gameplay.gif` in the repo root and it shows up right here.*

</div>

---

## ✨ Features

Frankly, this is a love letter to the original Super Mario Bros, constructed pixel-by-pixel.

- **Authentic NES rendering** - 256x224 virtual resolution scaled up with crisp pixelated edges (no blur), using the original Super Mario Bros color palette
- **Hand-drawn pixel sprites** - Mario with run, jump, and stand poses; Goombas with the classic angry-brow look
- **Classic set pieces** - glowing `?` blocks, breakable bricks, green warp pipes, spinning coins, hills, bushes, and parallax clouds
- **Real platformer physics** - momentum, gravity, variable jump, block bumps, and stomp mechanics
- **Full game loop** - score, coin counter, lives, countdown timer, win screen, and game-over screen
- **🎓 IUBI Edition** - collect the four glowing **I-U-B-I** letter badges scattered across the course, fly the IUBI banner at the flagpole and castle, and read IUBI facts on the win/lose screens
- **Chiptune sound** - jump, coin, stomp, and victory sound effects generated live with the WebAudio API (zero audio files)
- **Cross-platform controls** - keyboard plus on-screen touch buttons for mobile

---

## 🎮 Controls

| Action | Keyboard | Touch |
|--------|----------|-------|
| Move left | `←` or `A` | ◀ button |
| Move right | `→` or `D` | ▶ button |
| Jump | `Space`, `↑`, or `W` | A button |

**Goal:** Stomp the Goombas, grab the coins, collect all four **IUBI** letters, beat the clock, and reach the flagpole.

---

## 🚀 Getting Started

No installation required. You only need a modern web browser.

### Option 1 - Just open it
```bash
git clone https://github.com/JonGurakuqi/Super-Mario-Game-IUBI.git
cd Super-Mario-Game-IUBI
```
Then double-click `index.html`.

### Option 2 - Run a local server (recomended)
A local server avoids any browser security quirks:
```bash
# Python 3
python -m http.server 8000

# or Node
npx serve
```
Then visit `http://localhost:8000` in your browser.

---

## 🌐 Deploy Your Own Live Demo

Hosting this on GitHub Pages is free and takes about a minute:

1. Push the project to a GitHub repository.
2. Go to **Settings → Pages**.
3. Under **Source**, select your default branch (`main`) and the `/ (root)` folder.
4. Click **Save**. Your game goes live at:
   ```
   https://jongurakuqi.github.io/Super-Mario-Game-IUBI/
   ```
5. The game already lives in `index.html`, so it loads automatically at the root URL.

Henceforth, anyone with the link can play - no setup on their end.

---

## 🧱 Tech Stack

- **HTML5 Canvas** - all rendering
- **Vanilla JavaScript** - game loop, physics, collision, input
- **CSS** - HUD overlay, menus, and touch controls

Zero dependencies. The whole game is a single self-contained file.

---

## 📂 Project Structure

```
Super-Mario-Game-IUBI/
├── index.html      # The entire game (HTML + CSS + JS)
├── gameplay.gif    # Demo recording shown in this README
├── README.md       # You are here
└── LICENSE         # MIT License
```

---

## 🏗️ How It Works

The game runs on a single `requestAnimationFrame` loop that does four things each frame: update Mario, update enemies, update coins, and update particles - then renders the whole scene. The world is drawn in virtual NES coordinates and scaled up, so every sprite stays sharp.

Collision is constructed from simple axis-aligned bounding-box checks against three solid types: the ground segments, the floating blocks, and the pipes. Stomping is detected by checking Mario's downward velocity and his position relative to a Goomba's head.

---

## 🗺️ Roadmap

- [ ] Power-ups (Super Mushroom, Fire Flower)
- [x] Sound effects (WebAudio chiptune SFX) — background music still to come
- [x] Collectible IUBI letter badges
- [ ] Multiple levels / world map
- [ ] Local high-score saving
- [ ] Underground and castle themes

---

## 🙏 Acknowledgements

Built with gratitude as a tribute to the original **Super Mario Bros** (Nintendo, 1985). This is a non-commercial, educational fan project. Mario and all related characters are trademarks of Nintendo - this project is not affiliated with or endorsed by Nintendo.

---

## 📜 License

Released under the MIT License. See [`LICENSE`](LICENSE) for details.

---

<div align="center">

*Built by Jon Gurakuqi. Henceforth, may your jumps always clear the gaps.*

</div>
