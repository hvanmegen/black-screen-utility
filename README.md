# Black Screen Utility  
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)

A minimal fullscreen black page designed to keep a secondary monitor dark and stable.  
The tool was **conceptually designed by Henry van Megen** and **implemented by ChatGPT 5.1** using the functional specification described in `PROMPT.md`.

The repository contains:

- `index.html`  
  The entire tool in one self-contained HTML file (HTML, CSS, JS).
- `nosleep.min.js`  
  Local NoSleep.js copy to optionally prevent the screen from sleeping.
- `PROMPT.md`  
  A system prompt describing the complete functional design.  
  This file exists so future regenerations of `index.html` can be done deterministically.
- `LICENSE`  
  MIT license.

---

## Features

### Clock overlay
Toggle via right-click menu:
- **Show Time**
  - **slide-transition** (59 s ease-in/ease-out positional movement)
  - **fade-transition** (fade-out at :59, fade-in at :00)
  - **show-seconds** (toggle HH:MM vs HH:MM:SS)

Active items are **bold**.  
Transition options appear only when the timer is enabled.

### Fullscreen
- Double-click anywhere  
- Right-click → Toggle Fullscreen  
- Or use F11  

Fullscreen is intentionally **not persisted**.

### Persistence
Settings saved in `localStorage`:
- Whether the timer is active  
- Current transition mode (`none`, `slide`, `fade`)  
- Whether seconds are shown  

Not saved:
- Fullscreen state

### NoSleep.js
The page loads `nosleep.min.js` from the local directory.  
This can prevent monitor sleep after the first user interaction if enabled.

---

## SEO
The `<head>` block includes:
- 100% black favicons in multiple resolutions as inline images
- description  
- keywords  
- canonical URL  
- OpenGraph metadata  
- viewport settings  

This allows the project to be indexed properly by search engines.

---

## Installation
Clone the repository and deploy the three files:

```
index.html
nosleep.min.js
PROMPT.md
LICENSE
```

Place these on any static web server.

---

## Notes
The tool is intentionally extremely dark and stable to avoid:
- brightness shifts  
- local dimming fluctuations  
- distracting motion  

Use **slide-transition** for LCD/backlit panels.  
Use **fade-transition** for OLED panels.

---

## License
MIT License — see `LICENSE` for details.

