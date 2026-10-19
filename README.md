# THE LAST SIGNAL — Horror Survival v2.0.0

A self-contained, responsive, point-and-click horror mystery for mobile and desktop browsers. No backend or SQL database is required: progress is saved locally in the browser (`localStorage`). The save belongs to that browser/device.

## Included
- Seven illustrated locations: forest, cabin, generator yard, cellar, research annex, radio tower, transmitter chamber.
- Interactive hotspot buttons and action cards; tap-first mobile controls plus keyboard shortcuts (`1–9`, `J` journal, `M` map, `I` inventory, `Esc` pause).
- Inventory with usable battery packs and medkit, field notes/journal, tactical map, condition/fear/battery status.
- Cabin safe puzzle (742), tower cipher (417), a survival encounter, generator power gate, relay-core progression, autosave/continue.
- Three endings: The Truth, The Escape, The Unknown.
- Installable PWA manifest and offline service worker for HTTPS hosting.
- No paid assets, external game libraries, login, server, or database required. Typography gracefully falls back when offline.

## Play locally
Open `index.html` in a modern browser. Most gameplay works from a file URL; service-worker offline installation requires an HTTPS site or `localhost`.

Optional local server:
```bash
python -m http.server 8000
```
Then open `http://localhost:8000` in the folder containing `index.html`.

## GitHub Pages hosting (free)
1. Create a GitHub repository named `the-last-signal` and set it public.
2. Upload the *contents* of this folder to the repository root. `index.html` must be in the root beside `game.js`, `style.css`, `manifest.webmanifest`, `sw.js`, `scenes/`, and `icons/`.
3. In **Settings → Pages**, choose **Deploy from a branch**, select `main` and `/(root)`, and Save.
4. Wait for the Pages deployment, then open `https://YOUR-USERNAME.github.io/the-last-signal/`.
5. On mobile Chrome, use the browser menu → **Add to Home screen**. The service worker caches game files after first load; first load needs internet.

## Controls
- Tap any action card or highlighted scene hotspot to investigate/travel.
- Keyboard: `1`–`9` selects an available action; `J` journal; `M` map; `I` inventory; `Esc` pause.
- Puzzle keypad works by touch or keyboard input.

## Walkthrough (spoilers)
1. Forest: inspect marker, search van, follow cabin trail.
2. Cabin: read desk note, open safe with `742` to obtain relay core 1, fuse, cellar key.
3. Generator yard: restore power using the fuse for relay core 2.
4. Cellar: survive the mimic encounter, recover the final recording, enter annex.
5. Research annex: collect relay core 3 and recover the research file with tower cipher `417`.
6. Radio tower: enter `417` at the uplink panel to unlock transmitter chamber.
7. Transmitter chamber: choose an ending. Recover the original transmission fragment for **The Truth**; a voice recording unlocks **The Unknown**; **The Escape** is always available after reaching the final console.

## Save / privacy
Saves are local to the browser and do not sync across devices. Clearing site data removes the save. There is no account, analytics, SQL database, or remote server in this package.
