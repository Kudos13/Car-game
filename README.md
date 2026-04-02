# 🚗 Infinite Drive — Lamborghini SVJ

A browser-based infinite driving game built with Three.js. No server, no install — just open `index.html` and drive.

## 🎮 Play Online (GitHub Pages)

1. **Fork this repo** or push `index.html` to any GitHub repository
2. Go to **Settings → Pages**
3. Under *Source*, select **Deploy from a branch**
4. Choose `main` branch, `/ (root)` folder → click **Save**
5. Wait ~60 seconds, then visit:
   ```
   https://<your-username>.github.io/<repo-name>/
   ```

That's it — no build step, no dependencies to install.

---

## 🕹️ Controls

| Input | Gas | Brake | Steer |
|-------|-----|-------|-------|
| **Keyboard** | `W` / `↑` | `S` / `↓` | `A` `D` / `←` `→` |
| **Controller** | Right Trigger (RT) | Left Trigger (LT) | Left Stick |
| **Mobile** | Touch upper-right | Touch lower-right | Drag left half |

---

## ✨ Features

- **Infinite procedural road** — smooth curves, gentle hills, never repeats
- **Lamborghini SVJ** — orange low-poly model with rear wing, Y-headlights, quad exhausts, yellow brake calipers
- **200 MPH top speed** — 7-speed gearbox, RPM bar
- **Sunset sky dome** — gradient shader, atmospheric fog
- **Low-poly terrain** — rolling grass hills with flat shading
- **Instanced trees** — 450 trees (250 on mobile), zero performance hit
- **Mobile-first** — touch zones, auto-detects device, reduced pixel ratio
- **Gamepad API** — plug in any controller and go
- **GitHub Pages ready** — single HTML file, CDN-hosted Three.js

---

## 🛠️ Tech Stack

- [Three.js r128](https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js) (CDN)
- Vanilla JS, no build tools
- Custom GLSL sky shader
- `THREE.InstancedMesh` for trees
- Gamepad API for controller support

---

## 📁 Files

```
index.html   ← entire game, deploy this
README.md    ← this file
```

---

## 🔧 Tweaking

Open `index.html` and look for the constants block near the top of the `<script>`:

```js
const TOP_MPH    = 200;   // change top speed
const ROAD_W     = 12;    // road width in meters
const TREE_N     = 450;   // number of trees
const GEN_AHEAD  = 300;   // road samples generated ahead
```
