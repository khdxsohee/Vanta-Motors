<div align="center">

# ⚡ VANTA MOTORS

### *Engineered in the Dark.*

**A premium, fully interactive automobile landing page — dark showroom aesthetics, live telemetry, a working build & price configurator, and zero frameworks.**

![HTML5](https://img.shields.io/badge/HTML5-Semantic-orange?style=for-the-badge&logo=html5)
![CSS3](https://img.shields.io/badge/CSS3-Custom%20Engineered-blue?style=for-the-badge&logo=css3)
![JavaScript](https://img.shields.io/badge/JavaScript-Vanilla%20ES6-yellow?style=for-the-badge&logo=javascript)
![Build](https://img.shields.io/badge/Dependencies-Zero-green?style=for-the-badge)
![Motion](https://img.shields.io/badge/Motion-Reduced--Motion%20Safe-purple?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-ff4a1f?style=for-the-badge)

[Live Demo](https://khdxsohee.web.app/projects/vanta-motors.html) · [Report Bug](https://github.com/khdxsohee/vanta-motors/issues) · [Request Feature](https://github.com/khdxsohee/vanta-motors/issues)

</div>

---

## 📋 Table of Contents

- [About the Project](#-about-the-project)
- [Features](#-features)
- [Interactive Modules](#-interactive-modules)
- [Design System](#-design-system)
- [Tech Stack](#-tech-stack)
- [Project Structure](#-project-structure)
- [Getting Started](#-getting-started)
- [Configuration & Customization](#-configuration--customization)
- [Browser Support](#-browser-support)
- [Accessibility & Performance](#-accessibility--performance)
- [Roadmap](#-roadmap)
- [Contributing](#-contributing)
- [License](#-license)
- [Contact](#-contact)
- [Acknowledgments](#-acknowledgments)

---

## 🏁 About the Project

**VANTA MOTORS** is a fictional high-performance automobile marque brought to life as a single-file web experience. It was built with one goal: to feel like a **real showroom**, not a template.

Every section is interactive and functional — from a revving tachometer in the hero, to a live build configurator that recalculates pricing in real time, to a validated test-drive booking flow with confirmation codes. No dead buttons. No lorem ipsum. No frameworks.

> *"The MK-IV doesn't accelerate — it deletes distance."* — Owner Stories, Section 04

---

## ✨ Features

### Core Experience

| Feature | Description |
|---|---|
| 🏎️ **Live Tachometer** | SVG-built RPM gauge with idle jitter, shift lights, and a rev button |
| 🔢 **Count-Up Specs** | Animated HP / 0–100 / top-speed counters triggered on scroll |
| 🎛️ **Build & Price Configurator** | Model, paint, wheels & packs — live price tweening |
| 🎨 **Dynamic Paint Preview** | Grayscale image re-tinted per paint via CSS filters |
| 📅 **Test Drive Booking** | Full form validation, time slots, reference codes |
| 🗂️ **Filterable Lineup** | 6 vehicles filterable by Electric / Performance / SUV / Limited |
| 💬 **Testimonial Carousel** | Auto-rotating quotes with dots, arrows & hover-pause |
| ❓ **FAQ Accordion** | Smooth height-animated, single-open behavior |
| 📌 **Sticky Engineering Section** | Sticky narrative column + scrolling system panels |
| 🔔 **Toast Notifications** | Non-intrusive feedback for every user action |

### Motion & Polish

- 🎬 Ignition intro sequence on page load
- 🔤 Scramble-decode headline animation
- 🌊 Ken Burns breathing effect on hero imagery
- 🎞️ Headlight beam sweep across the hero car
- 📜 Dual marquees (telemetry ticker + oversized type strip)
- 🧭 Scroll progress bar + active-section nav highlighting
- 🌑 Film-grain noise overlay for texture depth
- ♿ Full `prefers-reduced-motion` support — all motion degrades gracefully

---

## 🕹️ Interactive Modules

### 1. The Tachometer
Built from raw SVG — tick marks, redline zone, and needle are generated/rotated in JavaScript.

```text
Idle   → 900 RPM with natural jitter
Rev    → Needle sweeps to ~8,300 RPM, holds, then decays
Lights → 6 shift LEDs ignite progressively past 3,800 RPM
```

### 2. The Configurator
A state-driven module — every selection re-renders the build:

```js
state = { model, paint, wheel, packs:Set }
→ paint filter applied to stage image
→ spec readout updated (HP / 0–100 / top speed)
→ itemized bill + animated total price
→ "Reserve" pre-fills the booking form
```

### 3. The Booking Flow
```
Validate → Simulate submit (900ms) → Generate REF code → Success card
         ↳ Inline field errors + toast feedback on failure
```

---

## 🎨 Design System

### Typography

| Role | Font | Usage |
|---|---|---|
| Display | **Anton** | Headlines, prices, giant wordmark |
| Body | **Manrope** | Paragraphs, forms, UI |
| Data | **IBM Plex Mono** | Labels, telemetry, specs, buttons |

### Color Palette

| Token | Hex | Purpose |
|---|---|---|
| `--bg` | `#0b0b0d` | Page background |
| `--panel` | `#121216` | Cards & surfaces |
| `--ink` | `#f2efe6` | Primary text |
| `--mut` | `#9aa0a8` | Secondary text |
| `--ember` | `#ff4a1f` | 🔥 Brand accent |
| `--amber` | `#ffb000` | Shift lights / highlights |

### Principles

- **No rounded-2xl cards** — sharp 4px radii, hard technical edges
- **No gradient soup** — texture comes from grid lines, noise & borders
- **Corner brackets, serial numbers, coordinates** — motorsport detailing
- **Contrast in type** — 6rem condensed headlines vs. 0.62rem mono labels

---

## 🧰 Tech Stack

```text
HTML5       → Semantic structure, zero div-soup where it matters
CSS3        → Custom properties, keyframes, IntersectionObserver-driven reveals
JavaScript  → Vanilla ES6+, ~450 lines, zero dependencies
Fonts       → Google Fonts (Anton · Manrope · IBM Plex Mono)
Images      → picsum.photos seeded placeholders (swap for real assets)
```

> **Why vanilla?** The entire experience ships as one portable file — open it anywhere, host it anywhere, no build step, no lock-in.

---

## 📁 Project Structure

```text
vanta-motors/
├── index.html        # ← everything: markup + styles + scripts (single file)
├── README.md         # ← you are here
└── LICENSE           # MIT
```

**Inside `index.html`:**

```text
<style>   → Full design system, components, motion, responsive rules
<body>    → 11 sections: intro, ticker, nav, hero, marquee, lineup,
            engineering, configurator, stories, booking, FAQ, footer
<script>  → IIFE-wrapped modules: tacho, reveal, counters, lineup,
            configurator, booking, carousel, FAQ, toast system
```

---

## 🚀 Getting Started

### Prerequisites

None. Just a modern browser.

### Option 1 — Direct Open

```bash
# Clone
git clone https://github.com/khdxsohee/vanta-motors.git
cd vanta-motors

# Open
open index.html          # macOS
start index.html         # Windows
xdg-open index.html      # Linux
```

### Option 2 — Local Server (recommended)

```bash
# Python
python -m http.server 8000

# Node (npx)
npx serve .

# Then visit http://localhost:8000
```

### Option 3 — Deploy

Drag-and-drop onto **GitHub Pages**, **Netlify**, **Vercel**, or **Cloudflare Pages**. Zero configuration required.

---

## ⚙️ Configuration & Customization

All data lives in clearly labeled JavaScript arrays — edit them, save, refresh:

```js
const CARS   = [ /* lineup cards: name, specs, price, image seed */ ];
const MODELS = { /* configurator base models + stats */ };
const PAINTS = [ /* paint name, swatch color, CSS filter, price */ ];
const WHEELS = [ /* wheel options + pricing */ ];
const PACKS  = [ /* optional packs + pricing */ ];
const QUOTES = [ /* testimonial text, author, role */ ];
```

**Swap placeholder images:** replace `https://picsum.photos/seed/...` URLs with your own photography.

**Rebrand:** change colors in `:root` CSS variables and the `VANTA` wordmark appears everywhere via CSS — search-and-replace takes 10 seconds.

---

## 🌐 Browser Support

| Browser | Status |
|---|---|
| Chrome / Edge 90+ | ✅ Full |
| Firefox 90+ | ✅ Full |
| Safari 15+ | ✅ Full |
| Mobile Safari / Chrome | ✅ Responsive |
| `prefers-reduced-motion` | ✅ Respected everywhere |

---

## ♿ Accessibility & Performance

- ♿ Semantic landmarks, labeled inputs, `aria-label`s on icon buttons
- ♿ Keyboard-operable accordion, buttons & menu
- ♿ Reduced-motion users get instant, animation-free rendering
- ⚡ Single HTTP request for all markup/styles/scripts
- ⚡ No libraries — JS payload ≈ 15 KB
- ⚡ Animations GPU-friendly (`transform` / `opacity` only)
- ⚡ IntersectionObservers instead of scroll listeners

---

## 🗺️ Roadmap

- [ ] Split into multi-file architecture (optional branch)
- [ ] WebGL paint configurator with real 3D model
- [ ] Sound design for the rev interaction (opt-in)
- [ ] Dark/light garage-mode toggle
- [ ] Multi-language support (EN / UR / DE / JA)
- [ ] Lighthouse 100/100 optimization pass

See [open issues](https://github.com/khdxsohee/vanta-motors/issues) for the full list.

---

## 🤝 Contributing

Contributions are what make the open-source community great. Any contribution is **greatly appreciated**.

1. Fork the project
2. Create your feature branch — `git checkout -b feature/AmazingFeature`
3. Commit your changes — `git commit -m 'feat: add AmazingFeature'`
4. Push to the branch — `git push origin feature/AmazingFeature`
5. Open a Pull Request

---

## 📄 License

Distributed under the **MIT License**. See [`LICENSE`](https://github.com/khdxsohee/vanta-motors/blob/main/LICENSE) for more information.

```text
MIT License — Copyright (c) 2026 khdxsohee
```

---

## 📬 Contact

**khdxsohee** — *Developer & Designer*

- GitHub: [@khdxsohee](https://github.com/khdxsohee)
- Project Link: [github.com/khdxsohee/vanta-motors](https://github.com/khdxsohee/vanta-motors)

> If this project helped you, consider dropping a ⭐ on the repo — it fuels the engine.

---

## 🙏 Acknowledgments

- Typography by [Google Fonts](https://fonts.google.com)
- Placeholder imagery by [Lorem Picsum](https://picsum.photos)
- Built with nothing but `index.html` and stubbornness 🏁

---

<div align="center">

**VANTA MOTORS © 2026 — Engineered Obsession**


</div>
