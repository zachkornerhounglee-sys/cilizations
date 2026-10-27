# CIVITAS — Empires

A self-contained browser strategy game built with Three.js. It uses a procedural low-poly 3D hex world and custom mesh-built cities and units, so you do not need to download a separate models folder.

## Features

- Turn-based civilization gameplay on a generated hex map
- Four empires per match, with AI rivals
- Found cities, grow populations, train units, improve tiles, and discover technologies
- Fog of war, exploration, rival-unit combat, and capital capture
- Domination, scientific, and influence victory conditions
- Online friend matches through PeerJS/WebRTC; share a link from the host's Invite button
- Settings for liquid-glass UI, graphics preset, interface scale, camera sensitivity, map size, AI difficulty, victory rules, editable keybindings, map labels/yields, reduced motion, sound effects, and autosave
- Local browser save/load
- Responsive HUD for desktop and mobile

## Run locally

The easiest option is to open `index.html` in a browser with an internet connection. Since the Three.js modules are loaded from a CDN, some browser features may work better when served over HTTP. If you have Python installed, open a terminal in this folder and run:

```bash
python -m http.server 8000
```

Then open `http://localhost:8000`.

## Publish with GitHub Pages

1. Create a new GitHub repository.
2. Upload `index.html` and `README.md` to the repository root (not inside an extra nested folder).
3. Open **Settings → Pages** in the repository.
4. Under the build/deployment source, select **Deploy from a branch**, choose the `main` branch and `/ (root)`, then save.
5. Wait for GitHub Pages to publish the site, then open the URL GitHub provides.
6. To play with friends, open the published site, choose **Create an online game**, click **Invite**, and copy the link. Share it with your friends. They should open that link while the host keeps the game page open.

## Multiplayer notes

The game is statically hosted by GitHub Pages; multiplayer signalling uses PeerJS's public cloud service and gameplay state is sent directly between browsers using WebRTC data connections. No separate game server is included. Some school, workplace, or restricted networks may block the signalling service or peer-to-peer connections. Friends should use the same current published link, and the host must remain online for that session.

## Controls

- Click a unit, then click an adjacent land hex to move.
- Move adjacent to an enemy unit or rival city to attack.
- Select a Settler and choose **Found a city** to settle open land.
- Select a city to choose production.
- `Space`: end turn
- `N`: select the next unit with movement remaining
- `1` / `2` / `3` / `4`: Empire / Research / Cities / Diplomacy
- `Esc`: open or close settings
- Drag to orbit, right-drag to pan, scroll or pinch to zoom

## Dependencies

- Three.js 0.164.1 via jsDelivr CDN
- PeerJS 1.5.4 via unpkg CDN

An internet connection is needed to load these libraries. The project does not bundle third-party library code.
