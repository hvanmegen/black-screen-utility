# Black Screen Utility  
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)

A minimal fullscreen black page designed for secondary monitors, dark rooms, and distraction-free use.

This utility runs on **https://black.qmp-media.nl/** and includes:
- A clock overlay (optional)
- Three movement modes:
  - **none** – instant jump every minute
  - **slide-transition** – 59s ease-in / ease-out movement, no brightness changes
  - **fade-transition** – fade-out at :59 and fade-in at :00 (OLED-friendly)
- A **show-seconds** toggle
- Full persistence via `localStorage` (except fullscreen state)
- Optional **NoSleep.js** to prevent the display from sleeping

Everything is intentionally minimal so the monitor stays as dark as possible.

---

## Features

### Clock overlay
Toggle via right-click menu:
- Show Time
  - slide-transition  
  - fade-transition  
  - show-seconds  

All active states appear **bold**.

### Fullscreen
Three ways:
- Doubleclick anywhere  
- Right-click → Toggle Fullscreen  
- Press **F11**

Fullscreen is not saved because browsers do not expose fullscreen exit events consistently and users often toggle it manually.

### Persistence
Saved in `localStorage`:
- `timerActive`
- `transitionMode`
- `showSeconds`

Not saved:
- fullscreen mode

---

## NoSleep.js
A local copy (`nosleep.min.js`) is loaded from the project root.  
This prevents the machine from turning off the screen while the tool is open.

---

## SEO
The `<head>` section includes:
- meta description  
- keywords  
- canonical URL  
- OpenGraph metadata  
- responsive viewport  

This allows Google to index the page.

---

## Installation
Clone the repo and deploy to your webserver:

```
index.html
nosleep.min.js
README.md
LICENSE
```

Ensure correct MIME types for `.html` and `.js`.

---

## Notes
The page is designed to be extremely dark and stable, avoiding:
- local-dimming pulses  
- OLED brightness pumping  
- distracting UI changes  

**slide-transition** is best for LCD backlit panels.  
**fade-transition** is acceptable for OLED panels.

---

## License
This project is licensed under the MIT License.  
See the `LICENSE` file for full text.
