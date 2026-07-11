# Last Pixel

An original lightweight 2.5D top-down survival shooter prototype.

## What Is This?

Last Pixel is an original browser-first game project focused on quick survival-shooter matches, readable combat, deterministic simulation, and a compact graybox development loop.

This public repository is currently a showcase only. Source code and internal development history are kept in a private development repository.

## Current Status

The project has completed local gates through D5.6:

- Research gate complete
- D1 movement graybox complete
- D2 combat baseline complete
- D2.5 projected 2.5D presentation complete
- D3A generic item / inventory foundation complete
- D3B playable loot spine complete
- D3C first item-backed combat slice complete
- D3D scaled world, inventory UI, death boxes, and match shell complete
- D5 world skeleton with map invariants, legal spawn/loot, static vehicles, and alive count complete
- D5.1 map legality, town detail, backpack/equipment, armor pickup, grenade loot, and ammo stack patch complete
- D5.5 materials skeleton, drivable placeholder vehicles, minimap, and richer menu/settlement shell complete
- D5.6 house rendering, map reachability, inventory usability, backpack capacity, and map marker polish complete

## Current Features

- Browser-playable local prototype
- Screen-relative movement
- Mouse aiming
- Original placeholder firearm tuning anchors
- Deterministic seeded core simulation
- Projectile collision and damage simulation
- Auto reload and reload progress UI
- Item-backed loot, ammo, healing, and inventory state
- Doors, interior visibility, death boxes, and static dummy participants
- Legal randomized player/participant spawns and randomized loot
- Static concept vehicles with four seats and health display
- Placeholder vehicles can be entered and driven by the driver seat in the local prototype
- Hide/reveal house cutaway behavior with interior props and cover
- Backpack item progression, right-click inventory handling, and equipment overflow behavior
- Large map overlay with a single player marker plus minimap readability improvements
- Client-side projected 2.5D graybox presentation
- Original graybox town map with collision-backed blockers, trees, rivers, bridges, and interiors
- One-click local playtest workflow in the private development tree

## Technical Highlights

- TypeScript
- Phaser
- Pure game-core package separated from rendering
- Deterministic seeded simulation
- Client-owned 2.5D projection adapter
- Automated unit, lint, typecheck, build, and browser smoke checks

## Play

No public playable build is released yet.

There is no GitHub Pages deployment, no downloadable release, and no online server for this project at the current stage.

## Roadmap

- Owner D5.6 playtest and bug triage
- Bot / AI only after D5.6 is accepted
- Complete single-player Battle Royale loop
- Demo hardening and visual readability pass
- Server-readiness audit
- Local authoritative multiplayer vertical slice
- Multiplayer feature parity and 6-human Internet test

## Status

Active development.

This is not an official remake, port, or licensed continuation of any existing game.
