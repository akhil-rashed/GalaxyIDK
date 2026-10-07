# 🌌 COSMOS — Interstellar Particle Observatory

> A cinematic, interactive 3D cosmic particle experience built with Three.js, WebGL, and GLSL shaders. Experience a procedurally generated galaxy with 150,000+ particles, dynamic nebulae, energy rings, and real-time audio reactivity — all running in your browser.

![Three.js](https://img.shields.io/badge/Three.js-r160-black?style=flat-square&logo=three.js)
![WebGL](https://img.shields.io/badge/WebGL-2.0-red?style=flat-square&logo=webgl)
![GLSL](https://img.shields.io/badge/GLSL-Shaders-blue?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)
![No Dependencies](https://img.shields.io/badge/Dependencies-None-brightgreen?style=flat-square)

---

## ✨ Overview

**COSMOS** transforms a simple Three.js particle demo into a **premium, cinematic WebGL experience** that feels like a hybrid between Interstellar, a modern art installation, and a deep-space observatory. The entire experience is contained in a **single self-contained HTML file** — no build tools, no frameworks, no external assets.

The scene features a multi-layered cosmic structure: a dense glowing core, spiral galactic arms, a sparse outer halo, procedural nebulae, distant galaxies, orbiting energy rings, drifting cosmic dust, and thousands of twinkling background stars — all powered by custom GLSL shaders and GPU-friendly instancing.

---

## 🎬 Features

### 🌠 Multi-Layered Galaxy System

- **150,000+ particles** across three distinct layers (core, disk, halo)
- **Spiral arm generation** with 4 arms, differential rotation, and density zones
- **Inter-arm field** for organic non-mathematical appearance
- **Vertical density waves** creating ripples through the galactic disk
- **Keplerian-style rotation** — inner particles orbit faster than outer ones
- **Adaptive particle counts** based on device capability

### 🎨 Advanced Shader-Based Rendering

- **6-stop cosmic color palette** (white → gold → magenta → violet → blue → cyan)
- **Distance, height, velocity, and time-based color interpolation**
- **Soft radial glow + bright star cores** per particle via `gl_PointCoord`
- **Velocity-based particle stretching** during warp mode
- **Fake depth-of-field** via distance-based size and alpha variation
- **Additive blending** throughout for authentic cosmic luminosity

### 💫 Central Energy Core

- **3 layered Fresnel shader shells** with procedural noise displacement
- **Pulsing scale animation** reacting to time, bursts, and audio
- **Billboarded bloom halo** that always faces the camera
- **Rotating ring orientations** at different speeds

### 🪐 Orbiting Energy Rings

- **4–5 thin torus rings** with unique orientations
- **Flow animation** along ring circumference
- **"Shy" rings** that only appear when the camera moves
- **Ring travellers** — tiny particles orbiting along each ring's path
- **Expands dynamically during energy bursts**

### 🌫️ Procedural Nebula

- **Shader-based fBm noise** with 3–5 octaves (quality-dependent)
- **Volumetric cloud appearance** on an inverted sphere
- **Multi-color blending** (deep blue → purple → warm orange highlights)
- **Galactic plane concentration** for realistic density falloff
- **Zero texture assets** — fully procedural

### ⭐ Deep-Space Star Field

- **Up to 9,000 background stars** at multiple depths
- **Twinkling animation** with per-star frequency variation
- **Color variation** (white → cool blue → warm yellow)
- **Smooth parallax** separate from the galaxy
- **Streaking** during warp mode

### 🌌 Distant Galaxies

- **Procedurally generated spiral galaxies** rendered on billboarded planes
- **Pure shader implementation** — no textures required
- **Always face the camera** for proper billboard behavior
- **Subtle presence** that adds depth without stealing focus

### 🪨 Floating Cosmic Fragments

- **GPU-instanced icosahedron fragments** drifting around the galaxy
- **Fresnel rim lighting** for crystalline appearance
- **Low-opacity presence** adds foreground depth

### ✨ Cosmic Dust

- **Independent drifting particles** with curved trajectories
- **Volumetric soft glow** rendering
- **Reactive to mouse and bursts**

---

## 🎮 Interactive Features

### 🖱️ Mouse & Touch Controls

- **OrbitControls** with smooth damping
- **Pointer parallax** — camera subtly tilts with cursor movement
- **Particle attraction/repulsion** near the cursor
- **Pinch-to-zoom** on mobile
- **Double-tap** for energy burst on touch devices
- **Double-click** triggers energy burst on desktop

### ⚡ Warp / Speed Mode

- Hold **Spacebar** or click **Warp** button
- Particles stretch into light-like streaks
- Rotation and movement accelerate
- Camera slowly moves forward
- Smooth bidirectional transitions

### 💥 Energy Burst

- **Double-click** anywhere to trigger
- Expanding shockwave propagates from the core
- Particles accelerate outward along the wavefront
- Core brightens dramatically
- Rings expand and intensify
- Subtle screen flash
- Smooth 1.8s return to normal

### 📷 Cinematic Auto-Camera

- Activates after **5 seconds of inactivity**
- Smooth cinematic orbit around the galaxy
- Instantly pauses on user interaction
- Optional dedicated **Cinematic Mode** with breathing camera motion

### 🎵 Audio-Reactive Mode

- **Microphone-based** real-time audio analysis
- **Bass frequencies** drive particle size and core pulsing
- **Overall volume** affects brightness and rotation
- **Requires explicit user permission** — never auto-requests
- Toggle via settings panel

---

## ⌨️ Keyboard Shortcuts

| Key | Action |
|-----|--------|
| **Space** (hold) | Activate warp mode |
| **G** | Toggle galaxy mode (spiral ⇄ cosmic vortex) |
| **N** | Toggle nebula visibility |
| **S** | Toggle star field |
| **C** | Toggle cinematic camera |
| **H** | Hide / show UI |
| **B** | Trigger energy burst |
| **Double-click** | Trigger energy burst |

---

## 🎛️ Settings Panel

Access via the **Settings** button (bottom-right).

### Rendering
- **Quality** — Auto / Low / Medium / High
- **Density** — Particle count multiplier (0.3× – 1.4×)
- **Performance Mode** — Reduces pixel ratio and disables heavy effects

### Visuals
- **Glow** — Overall luminosity (0.3× – 2.0×)
- **Color** — Color saturation vs grayscale (0 – 1.6)
- **Star field** — Background stars toggle
- **Nebula** — Procedural nebula toggle
- **Cosmic dust** — Drifting dust layer toggle
- **Energy rings** — Orbiting rings toggle

### Motion
- **Speed** — Time flow multiplier (0.1× – 2.5×)
- **Rotation** — Galactic rotation speed (0 – 2.5×)
- **Auto camera** — Cinematic orbit on inactivity
- **Cinematic** — Dedicated cinematic camera mode

### System
- **Audio reactive** — Microphone-based reactivity
- **Show stats** — FPS, particle count, render mode

---

## 📊 Quality Presets

| Preset | Particles | Stars | Pixel Ratio | Nebula Octaves |
|--------|-----------|-------|-------------|----------------|
| **Low** | 48,000 | 2,600 | 1.25× | 3 (disabled) |
| **Medium** | 105,000 | 5,200 | 1.6× | 4 |
| **High** | 155,000 | 9,000 | 2.0× | 5 |

Quality is **auto-detected** based on:
- CPU core count (`navigator.hardwareConcurrency`)
- Device memory (`navigator.deviceMemory`)
- Mobile vs desktop detection

**Adaptive degradation** kicks in automatically if FPS drops below 38 for extended periods, progressively:
1. Lowering pixel ratio
2. Disabling nebula and dust
3. Reducing particle density

---

## 🚀 Quick Start

### Option 1 — Direct Open

1. **Download** `index.html`
2. **Double-click** to open in a modern browser
3. Done. That's it.

### Option 2 — Local Server (recommended)

```bash
# Clone the repo
git clone https://github.com/yourusername/cosmos.git
cd cosmos

# Serve with any static server
python -m http.server 8000
# or
npx serve .
# or
php -S localhost:8000
```

Then open `http://localhost:8000`.

### Option 3 — Deploy

Drop `index.html` onto any static host:
- **GitHub Pages**
- **Netlify** (drag & drop)
- **Vercel**
- **Cloudflare Pages**
- **Surge.sh**

---

## 🧪 Browser Support

| Browser | Status |
|---------|--------|
| Chrome 90+ | ✅ Full support |
| Firefox 88+ | ✅ Full support |
| Safari 15+ | ✅ Full support |
| Edge 90+ | ✅ Full support |
| iOS Safari 15+ | ✅ Optimized |
| Android Chrome | ✅ Optimized |

**Requirements:**
- WebGL 1.0 (WebGL 2.0 preferred)
- ES Modules support
- Modern JavaScript (ES2020+)

If WebGL is unavailable, a clean fallback message is displayed.

---

## ⚙️ Performance Targets

| Device Class | Target FPS | Particle Count |
|--------------|-----------|----------------|
| High-end desktop | 60 FPS | ~155,000 |
| Mid-range desktop | 60 FPS | ~105,000 |
| Modern laptop | 55–60 FPS | ~105,000 |
| High-end mobile | 45–60 FPS | ~70,000 |
| Mid-range mobile | 30–45 FPS | ~48,000 |

Performance mode and auto-degradation ensure smooth experience across all devices.

---

## 🏗️ Architecture

The entire experience lives in **one HTML file**, organized into 18 clearly labeled sections:

```
1.  Configuration       — Quality presets, device detection, settings
2.  Renderer            — WebGL setup, pixel ratio, fallback detection
3.  Scene               — Scene hierarchy, groups (world, galaxy, stars, deep)
4.  Camera              — Perspective camera, FOV, initial position
5.  Controls            — OrbitControls with damping, touch support
6.  Shared Uniforms     — Global shader uniforms (time, mouse, warp, etc.)
7.  Shader Library      — All GLSL vertex & fragment shaders
8.  Galaxy              — Particle generation (core, disk, halo)
9.  Star Field          — Background star generation
10. Nebula + Distant    — Procedural nebula sphere, distant galaxies
11. Central Core        — Multi-shell Fresnel core, billboard glow
12. Energy Rings        — Torus rings with particle travellers
13. Interaction         — Mouse, touch, keyboard, audio input
14. UI                  — Settings panel, sliders, switches, toasts
15. Performance Monitor — FPS tracking, adaptive quality degradation
16. Animation Loop      — Main render loop with eased state updates
17. Resize Handling     — Debounced resize, orientation changes
18. Initialization      — Staged boot sequence with loader
```

---

## 🎨 Visual Design Philosophy

- **The galaxy is the hero** — nothing overpowers it
- **Depth through layers** — foreground dust, mid-ground galaxy, background stars
- **Cinematic color grading** — subtle vignette, screen-blended gradients
- **Glassmorphism UI** — backdrop-filtered panels, soft borders
- **Monospace typography** with wide letter-spacing for futuristic feel
- **No neon excess** — premium, mysterious, deep-space aesthetic
- **UI auto-hides** when inactive for immersive viewing

---

## 🔧 Technical Highlights

### Shader-Driven Everything
Every expensive calculation lives in GPU shaders:
- Particle motion, color, size, alpha
- Fresnel core shells
- Nebula fBm noise
- Ring flow and visibility
- Procedural distant galaxies

### Memory & Performance
- **Typed arrays** (`Float32Array`) for all geometry attributes
- **Reusable Vector3 objects** inside the animation loop
- **Debounced resize** events
- **Visibility API** pauses rendering when tab is hidden
- **Proper disposal** of geometries and materials on rebuild
- **InstancedMesh** for cosmic fragments

### No Dependencies
- No React, Vue, Angular
- No Tailwind, Bootstrap
- No jQuery
- Only Three.js (loaded via CDN import map)
- Pure vanilla JavaScript + CSS

---

## 🎁 Easter Eggs

- **Double-click the core** → energy burst with screen flash
- **Hold Space** → warp mode with particle streaking
- **"Shy" rings** only reveal themselves when you move the camera
- **Cosmic vortex mode** (G key) morphs the entire galaxy into a swirling tornado
- **Audio mode** turns the galaxy into a visualizer

---

## 📱 Mobile Optimizations

- Touch gestures (one-finger rotate, pinch-zoom)
- Double-tap for energy burst
- Automatic quality downgrade on low-end devices
- Capped pixel ratio to preserve performance
- Larger FOV in portrait orientation
- Touch-friendly UI with larger hit targets

---

## 🛠️ Customization

Want to tweak the experience? All key parameters live in the `settings` object and `QUALITY` presets at the top of the `<script type="module">` block:

```js
const QUALITY = {
    high: {
        galaxy: 155000,   // Main particle count
        dust: 16000,      // Cosmic dust particles
        stars: 9000,      // Background stars
        halo: 0.14,       // Halo ratio (0-1)
        nebula: true,     // Enable nebula
        octaves: 5,       // Noise octaves
        pixelRatio: 2.0,  // Max pixel ratio
        rings: 5,         // Energy ring count
        fragments: 48,    // Floating fragments
        distant: 7        // Distant galaxies
    }
};
```

Color palettes live in the `cosmicPalette()` GLSL function inside `GLSL_COMMON`.

---

## 📜 License

MIT License — free to use, modify, and distribute. Attribution appreciated but not required.

---

## 🙏 Credits

- **Three.js** — [threejs.org](https://threejs.org/)
- **Inspiration** — The original particle galaxy concept, Interstellar, cosmic photography from Hubble & JWST
- **No AI-generated textures or assets** — everything is procedural

---

## 🌟 Showcase

If you build something cool with this, open an issue or PR — I'd love to see it featured here.

---

<div align="center">

**Built with ❤️ by Akhil Rashed**

*"We are made of star-stuff. We are a way for the universe to know itself." — Carl Sagan*

</div>
