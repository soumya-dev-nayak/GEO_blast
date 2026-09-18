# GeoBlast

**A browser-based Geometry Dash-style game that runs fully offline from a single HTML file — no installation, no internet, no blocked websites.**

Built with vanilla HTML5 Canvas and JavaScript. Zero dependencies.

---

## Table of Contents

- [Overview](#overview)
- [Screenshots](#screenshots)
- [Video Demo](#video-demo)
- [How to Download and Play](#how-to-download-and-play)
- [How to Share](#how-to-share)
- [Game Mechanics](#game-mechanics)
- [Portals](#portals)
- [Controls](#controls)
- [File Structure](#file-structure)
- [Technical Notes](#technical-notes)
- [License](#license)

---

## Overview

GeoBlast is a locally runnable, browser-based clone of Geometry Dash. The entire game lives inside a single `.html` file — open it in any modern browser and play instantly. No server, no framework, no install required.

The level is procedurally generated on every run, so each attempt plays differently. The game includes a start menu, best-run tracker, practice mode, multiple obstacle types, and GD-style portals that change gravity, speed, and player mode mid-run.

---

## Screenshots

<p align="center">
  <img src="https://raw.githubusercontent.com/soumya-dev-nayak/GEO_blast/main/Pics/Fig-1%20GeoBlast%20Starting%20Page.png" width="650">
  <br>
  <b>Figure 1: GeoBlast Starting Page — Main Menu</b>
</p>

<br>

<p align="center">
  <img src="https://raw.githubusercontent.com/soumya-dev-nayak/GEO_blast/main/Pics/Fig-2%20Game%20Initialisation.png" width="650">
  <br>
  <b>Figure 2: Game Initialisation — Cube Mode in Action</b>
</p>

<br>

<p align="center">
  <img src="https://raw.githubusercontent.com/soumya-dev-nayak/GEO_blast/main/Pics/Fig-3%20Player%20Died.png" width="650">
  <br>
  <b>Figure 3: Player Died — Death Screen with Percentage Reached</b>
</p>

<br>

<p align="center">
  <img src="https://raw.githubusercontent.com/soumya-dev-nayak/GEO_blast/main/Pics/Fig-4%20Game%20Restart.png" width="650">
  <br>
  <b>Figure 4: Game Restart — Attempt Counter and Best Run Tracker</b>
</p>

---

## Video Demo

GitHub renders `.mp4` files with a built-in player when you open the file directly. Click the thumbnail below to watch the gameplay demo.

<p align="center">
  <a href="https://github.com/soumya-dev-nayak/GEO_blast/blob/main/Pics/GeoBlast_Gameplay.mp4">
    <img src="https://raw.githubusercontent.com/soumya-dev-nayak/GEO_blast/main/Pics/Fig-2%20Game%20Initialisation.png" width="650" alt="Click to watch GeoBlast gameplay demo">
  </a>
  <br>
  <b>Gameplay Demo — click the image to open the video on GitHub</b>
</p>

---

## How to Download and Play

No build tools, no package manager, no runtime required.

**Step 1 — Download the HTML file**

Click on [`GeoBlast — upgraded geometry dash 1.html`](https://github.com/soumya-dev-nayak/GEO_blast/blob/main/GeoBlast%20%E2%80%94%20upgraded%20geometry%20dash%201.html) in the file list, then click the **Download raw file** button at the top-right of the file view.

Alternatively, clone the repository:

```bash
git clone https://github.com/soumya-dev-nayak/GEO_blast.git
```

**Step 2 — Open it in a browser**

Double-click the downloaded `.html` file. It opens directly in Chrome, Firefox, or Edge with no setup needed.

The game starts immediately on the menu screen.

---

## How to Share

Because the entire game is a single self-contained `.html` file, sharing is as simple as sending the file. The recipient opens it in any browser — no internet connection is needed during play.

Ways to share:
- Attach it to an email
- Drop it in a shared drive or on a USB drive
- Copy it directly to a colleague's machine

---

## Game Mechanics

| Element | Description |
|---|---|
| **Cube** | Default player mode. Jumps on ground contact and rotates while airborne. |
| **Ship** | Activated by the Ship portal. Hold jump to thrust upward; release to fall. |
| **Spike** | Triangular ground hazard. Instant death on contact. |
| **Ceiling Spike** | Spike mounted on the ceiling. Active during gravity-flip segments. |
| **Block** | Solid platform. Can be landed on top; hitting the side kills the player. |
| **Elevated Block** | Block placed above ground level. Requires a timed jump to land on top. |
| **Sawblade** | Spinning circular blade that rotates in real-time. Instant death on contact. |
| **Jump Orb** | Yellow floating orb. Triggers a forced boost jump when the player makes contact. |

---

## Portals

Portals are vertical gate objects placed mid-level. Passing through one changes a property of the player. The active mode and modifiers are shown as a badge in the top-left corner of the canvas.

| Portal | Color | Effect |
|---|---|---|
| **Gravity Flip** | Purple | Flips gravity — the player falls toward the ceiling. Pass through again to revert. |
| **Speed Boost** | Orange | Increases movement speed by 1.5x. Pass through again to return to normal. |
| **Ship** | Cyan | Switches the player between Cube and Ship mode. |

---

## Controls

| Input | Action |
|---|---|
| `Space` | Jump (Cube mode) / Thrust upward (Ship mode) |
| `Click` or `Tap` | Same as Space |
| Double-press `Space` | Double jump — usable once while airborne in Cube mode |

Additional features:

- **Practice Mode** — the attempt counter does not increment; useful for learning obstacle placement before a serious run
- **Best Run Tracker** — the highest percentage reached across all attempts is saved and shown in the HUD and on the main menu
- **Procedural Level Generation** — the level layout is randomly generated each time Play is pressed, so no two runs are identical

---

## File Structure

```
GEO_blast/
├── GeoBlast — upgraded geometry dash 1.html   # The complete game (single file)
├── Pics/
│   ├── Fig-1 GeoBlast Starting Page.png
│   ├── Fig-2 Game Initialisation.png
│   ├── Fig-3 Player Died.png
│   ├── Fig-4 Game Restart.png
│   └── GeoBlast_Gameplay.mp4
├── LICENSE
└── README.md
```

---

## Technical Notes

- Built entirely with the **HTML5 Canvas API** and vanilla JavaScript
- No external libraries, no CDN dependencies, no build step
- Runs in any modern browser: Chrome, Firefox, Edge, Safari
- Compatible with Windows, Linux, and macOS
- Level generation uses a randomised pattern system to place obstacles, orbs, sawblades, and portals
- Smooth animation handled via `requestAnimationFrame` with delta-time correction
- Particle effects, parallax star fields, and animated portal gates are rendered per-frame on canvas

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

<p align="center">
  Made with HTML5 Canvas &nbsp;|&nbsp; No dependencies &nbsp;|&nbsp; Works offline
</p>
