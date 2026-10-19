# THE LAST SIGNAL v2.0.0 — QA report

## Automated checks performed
- `node --check game.js`: passed.
- `manifest.webmanifest` JSON parse: passed.
- All SVG scene/icon assets parsed as XML; 192×192 and 512×512 PNG icons generated.
- Chromium interactive test (game files embedded into the test document because the environment blocks local-file and loopback navigation): passed with zero JavaScript page errors.
- Main progression tested through: marker → van → cabin → safe code `742` → fuse/generator → cellar mimic encounter → original recording → research annex → third relay core → tower code `417` → transmitter.
- Each of the three distinct ending choices was played and its expected title was verified.
- Save → return to title → Continue round-trip: passed using a localStorage test shim.
- 390 px mobile viewport, mobile navigation dock and scene width: passed.

## Not claimed as tested
- A live public GitHub Pages deployment was not created.
- PWA installation and offline service-worker behavior were not tested in a real HTTPS deployment. The manifest parses and the service worker precaches the shipped runtime assets.
- This is an illustrated 2D, point-and-click browser game, not a photorealistic 3D game. No SQL/backend is required; progress is stored locally in the player's browser.
