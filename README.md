# 呪術廻戦 — Cursed Technique Simulator

> **Real-time hand gesture recognition × particle physics × JJK lore**  
> Activate cursed techniques with your bare hands through your webcam.

---

![Banner](https://i.imgur.com/placeholder-banner.gif)

## ✦ Demo

| Gesture | Technique | Preview |
|--------|-----------|---------|
| ☝️ Index finger up | **Reverse Cursed Technique: Red** | ![Red](https://i.imgur.com/placeholder-red.gif) |
| ✌️ Index + Middle up | **Domain Expansion: Infinite Void** | ![Void](https://i.imgur.com/placeholder-void.gif) |
| 🖐️ All fingers up | **Domain Expansion: Malevolent Shrine** | ![Shrine](https://i.imgur.com/placeholder-shrine.gif) |
| 🤌 Pinch (index + thumb) | **Secret Technique: Hollow Purple** | ![Purple](https://i.imgur.com/placeholder-purple.gif) |

> 📸 *Record your screen with [ScreenToGif](https://www.screentogif.com/) or [LICEcap](https://www.cockos.com/licecap/) and drop the GIFs into the table above.*

---

## ⚡ Features

- **Zero setup** — pure HTML/CSS/JS, runs directly in any modern browser
- **Live webcam hand tracking** via [MediaPipe Hands](https://google.github.io/mediapipe/solutions/hands.html)
- **20,000-particle system** built on [Three.js](https://threejs.org/) with GPU-accelerated rendering
- **Bloom post-processing** via `UnrealBloomPass` for that cursed energy glow
- **4 unique particle formations** — each technique has a distinct shape, color, and rotation behavior
- **Screen shake** on technique activation
- **Mirrored camera feed** with skeleton overlay drawn in real time

---

## 🚀 Getting Started

No installs, no bundlers. Just open it.

```bash
# Clone the repo
git clone https://github.com/YOUR_USERNAME/cursed-technique-simulator.git

# Open in browser
cd cursed-technique-simulator
open index1.html        # macOS
start index1.html       # Windows
xdg-open index1.html   # Linux
```

> ⚠️ **Important:** The app uses your webcam. Allow camera access when prompted.  
> Some browsers (especially Chrome) may block webcam access on `file://` — if that happens, serve it locally:

```bash
# Quick local server (Python)
python -m http.server 8080
# Then visit: http://localhost:8080
```

---

## 🤙 Gesture Guide

| Hand Shape | Technique Activated |
|---|---|
| Index finger raised, others curled | 🔴 **Red** — spiral particle arms spin outward |
| Index + Middle raised, ring curled | 🔵 **Infinite Void** — ring of white light + blue particle cloud |
| All four fingers raised | ⛩️ **Malevolent Shrine** — particles form a dark ground plane with a cursed arch |
| Index tip pinched to thumb tip | 🟣 **Hollow Purple** — dense glowing sphere + scattered debris |
| No hand / fist | ⚪ **Neutral** — dim ambient scatter |

---

## 🛠️ Tech Stack

| Layer | Library |
|---|---|
| 3D Rendering | [Three.js r160](https://threejs.org/) |
| Post-processing | `EffectComposer` + `UnrealBloomPass` |
| Hand Tracking | [MediaPipe Hands](https://google.github.io/mediapipe/solutions/hands.html) |
| Camera Utilities | `@mediapipe/camera_utils` |
| Skeleton Drawing | `@mediapipe/drawing_utils` |

All libraries are loaded via CDN — no `package.json` needed.

---

## 📁 Project Structure

```
cursed-technique-simulator/
└── index1.html        # Everything — scene, shaders, hand tracking, UI
```

Single-file architecture. The entire simulator lives in one HTML file.

---

## 🎨 Customization

Want to tweak things? Everything's in `index1.html`:

```js
const COUNT = 20000;         // Particle count (lower = better perf)
bloomPass.strength = 2.5;   // Glow intensity per technique
shakeIntensity = 0.4;       // Screen shake on technique activation
```

To add a new technique, define a `getYourTechnique(i)` function following the same `{x, y, z, r, g, b, s}` return pattern, then register it in `updateState()`.

---

## 🙏 Credits

- Inspired by **Jujutsu Kaisen** by Gege Akutami / MAPPA
- Particle system design inspired by cursed energy visual language from the anime
- Hand landmark detection powered by Google's MediaPipe

---

## 📜 License

MIT — do whatever you want, just don't claim you invented Hollow Purple.

---

<div align="center">
  <sub>Built for fun. No cursed spirits were harmed in the making of this project.</sub>
</div>
