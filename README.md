**Real-time JJK cursed technique simulator using hand gesture recognition. Uses MediaPipe Hands to track finger positions via webcam and maps gestures to 8 techniques, each rendered as a unique 20,000-particle 3D formation with bloom post-processing and camera shake. Built with Three.js + WebGL. No backend, single HTML file.**

**How it works:** MediaPipe reads 21 hand landmarks per frame. Finger state (up/down) is determined by comparing tip Y-coordinate vs knuckle Y-coordinate. Each unique finger combination maps to a technique — particles lerp smoothly between formations every state change.

---

### Techniques

| Gesture | Technique | Effect |
|---|---|---|
| ☝️ Index only | Reverse Cursed Technique: Red | 3-arm red spiral expanding outward |
| ✌️ Index + Middle | Domain Expansion: Infinite Void | White ring + scattered blue particle sphere |
| 🤌 Pinch | Secret Technique: Hollow Purple | Dense purple sphere explosion, max bloom |
| 🖐️ All fingers | Domain Expansion: Malevolent Shrine | Ground plane + pillars + curved ceiling, locked upright |
| 🤙 Ring + Pinky | Limitless: Blue | Reverse of Red — 3 arms spiraling *inward* to a blazing blue core |
| 🤘 Index + Pinky | Ten Shadows Technique | 3 dark elongated shadow beast blobs + wispy purple tendrils |
| 🖕 Middle only | Idle Transfiguration | 5 sine-wave distorted humanoid soul figures, pink/flesh colored |
| ✊ Fist | Black Flash | 5 concentric shockwave rings, dark core → orange/gold outward, flickering bloom |

---

**Stack:** Three.js · MediaPipe Hands · UnrealBloomPass · Vanilla JS · No dependencies beyond CDN
