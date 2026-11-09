# The Life of the Sun ☀️

> *"Ten billion years of stellar evolution, thrown into motion by your fingertips."*

An ultra-minimalist, single-file interactive hero experience recreating the complete lifecycle of our Sun—from a cold collapsing molecular cloud to a glowing ember of degenerate matter.

Everything you see on screen is computed live in a **single raw WebGL fragment shader**. No Three.js, no textures, no videos, no external libraries. Just pure mathematics, procedural raymarching, and physical momentum.

---

## What You're Experiencing

Grab the timeline or flick your cursor. You aren't just scrolling through a slide deck—**you are physically throwing the Sun**.

- **The Ball Never Changes Size**: Every evolutionary stage is a dynamic surface mapped onto the exact same celestial sphere.
- **Physical Throw & Whip**: Every scrub injects angular velocity (`ω`). As the Sun whips round, its convective granules and coronal flares smear horizontally into realistic motion bands before settling into the next epoch.
- **Deep Void Isolation**: The halo analytically decays to absolute zero (`#000000`) within a tight radius. No artificial box boundaries or background gradients—only pristine void and twinkling background stars that streak during high-speed rotation.
- **Sub-Millisecond Responsiveness**: Every wheel tick, touch drag, and track hover recalculates physics and shader uniforms on that exact frame.

---

## The Ten Epochs

| # | Epoch | Timeframe | What's Happening |
|:-:|:---|:---|:---|
| **0** | **Solar Nebula** | 4.6 billion years ago | A cold, diffuse interstellar cloud collapses inward under gravity |
| **1** | **Protostar** | 4.57 billion years ago | Gravitational pressure heats an infant core surrounded by dust |
| **2** | **Ignition** | 4.5 billion years ago | Core temperatures trigger thermonuclear hydrogen fusion |
| **3** | **The Sun** *(Today)* | Present day | In stable hydrostatic equilibrium halfway through its lifespan |
| **4** | **Brighter Sun** | 1 billion years from now | Increasing solar luminosity heats Earth, boiling the planetary oceans |
| **5** | **Subgiant** | 5 billion years from now | Hydrogen in the core is exhausted; shell fusion begins to swell the star |
| **6** | **Red Giant** | 7.6 billion years from now | Massive expansion swallows Mercury and roasts the inner solar system |
| **7** | **Helium Flash** | 7.7 billion years from now | Explosive ignition of degenerate helium in the core |
| **8** | **Planetary Nebula** | 7.8 billion years from now | Outer stellar envelopes detach, leaving a glowing teal gas shell |
| **9** | **White Dwarf** | 8 billion years from now | A dense, slowly cooling carbon-oxygen ember the size of Earth |

---

## Interactive Controls

| Input | Platform | Action |
|:---|:---|:---|
| **Hover Track** | Desktop | Hover along the bottom tick mark timeline to preview stages with an interactive Gaussian bell indicator. |
| **Click / Drag Track** | All | Instantly jump or drag the timeline to any point between Nebula and White Dwarf. |
| **Screen Drag** | All | Click or tap anywhere in the void to throw the timeline with proportional gesture drag. |
| **Mouse Wheel / Trackpad** | Desktop / Laptop | Scroll vertically or horizontally to throw the star with momentum. |
| **Arrow Keys** | Keyboard | <kbd>←</kbd> / <kbd>→</kbd> or <kbd>↑</kbd> / <kbd>↓</kbd> step backward or forward by exactly one stage. |
| **Home / End** | Keyboard | Jump instantly to **Solar Nebula** (<kbd>Home</kbd>) or **White Dwarf** (<kbd>End</kbd>). |
| **Idle Autoplay** | All | If left untouched for 5 seconds, time starts advancing automatically every 2.6 seconds. |

---

## Architecture & Math

- **Full-Screen Quad**: One oversized triangle (`[-1,-1, 3,-1, -1,3]`) drawn across the viewport.
- **Procedural 3D Texturing**: 5-octave Fractal Brownian Motion (FBM) with continuous time-domain turbulence (`evo`) and coordinate domain warping.
- **Physical Blur**: Angular velocity `ω` dynamically stretches sampling coordinates along the rotation axis (`1.0 / (1.0 + blur * 3.2)`), creating true optical streak smearing.
- **Volumetric Nebula Shell**: Planetary nebula mode renders an internal degenerate core surrounded by an illuminated dual-layer filament cavity.
- **Zero Dependencies**: Pure HTML5, CSS3, and raw WebGL 1.0 in a standalone file.

---

## Running Locally

Clone this repository and open `index.html` in any modern web browser:

```bash
git clone https://github.com/Hix-001/Sun_Timeline_Site.git
cd Sun_Timeline_Site
# Open directly in your browser:
start index.html
# Or serve with any lightweight static server:
python -m http.server 8080
```

---

## License

Distributed under the [MIT License](LICENSE).

---

<p align="center">
  Built with ❤️ by <a href="https://github.com/Hix-001"><b>hix-001</b></a>
</p>
