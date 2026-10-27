# CIVITAS — Realms

A browser-based civilization sandbox. Start with a Keep, villagers and a scout, then turn a small frontier into a kingdom. The game is written as a single self-contained `index.html`; single-player does not require an external game engine or server.

## Core gameplay

- Build farms, lumber camps, quarries, iron mines, homesteads, markets, barracks, academies, watchtowers, walls and storehouses.
- Earn food, wood, stone, iron, gold and science from your buildings each season.
- Select a villager, choose **Gather resource**, then click a wood, stone, iron or food deposit. Villagers walk to it and gather until the deposit runs out.
- Research crop rotation, stone masonry, trade routes, scholarship, iron smelting and steel arms.
- Recruit guards, archers, scouts, cavalry and siege carts from your barracks.
- Command troops to move or attack rival units and structures. Rival AI realms build their own economies, recruit troops and launch attacks.
- Capture every rival Keep to unite the frontier. Defend your own Keep, upgrade and repair structures, and complete milestones.
- Save/load locally, pause the simulation, and adjust the game speed.

## Run locally

Double-click `index.html` to play single-player in a modern browser. No build step, installation or local server is required. The world is drawn with a custom isometric canvas, and buildings, units and terrain are drawn directly by the game. The welcome-menu actions use explicit click listeners and report an error if an action fails.

## Publish using GitHub Pages

1. Create a GitHub repository.
2. Upload `index.html` and `README.md` directly into the repository root.
3. Open **Settings → Pages**.
4. Under the deployment source, choose **Deploy from a branch**, select `main` and `/(root)`, then save.
5. Open the published URL from GitHub Pages.

## Multiplayer

From the menu, choose **Host a world for friends**. When the world opens, click **Invite**, copy the link and send it to your friends. A joiner can also use **Join a friend's world** and paste the full link or room ID. The host must keep their game open during the match. The optional PeerJS browser library is loaded only when you try to host or join, so it cannot block single-player startup. An internet connection is required for multiplayer, and some school/work networks may block peer connections.

## Controls

- Click a tile to inspect it and see valid construction options.
- Click one of your units to select it.
- Villager: choose **Gather resource**, then click a deposit.
- Military unit: choose **Attack target**, then click an enemy unit or building; or choose **Move unit**, then click land.
- Drag empty terrain to pan; use the mouse wheel to zoom.
- `Escape`: open/close settings. `Space`: pause/resume. `B`: build, `T`: tech, `A`: army.

## Settings

Settings include Liquid Glass UI, graphics quality, UI scaling, unit/building labels, resource icons, tile outlines, reduced motion, map size, AI difficulty and count, starting resources, autosave, simulation speed, screen effects, sound toggle and volume.

## Updating an existing GitHub Pages site

Replace the existing root `index.html` with the one from this ZIP, commit the change, and hard-refresh the published page (`Ctrl+F5` on Windows). A previously published or cached version will not receive the fix until the new file is uploaded and Pages redeploys.

## Notes

- Saves are stored in the current browser and device.
- Single-player is fully local and does not need the PeerJS library.
- Multiplayer uses PeerJS/WebRTC signalling and peer-to-peer state sharing; the host is the authority for the world simulation. Multiplayer needs a live internet connection and is subject to network restrictions.
