# Last Pixel

An original lightweight 2.5D top-down survival shooter prototype.

## What Is This?

Last Pixel is an original browser-first game project focused on quick survival-shooter matches, readable combat, deterministic simulation, and a compact graybox development loop.

This public repository is currently a showcase only. Source code and internal development history are kept in a private development repository.

## Current Status

The project has reached the local D5.95 map-density and vehicle-comfort milestone:

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
- D5.7 map polish, spawn fairness, lake island military base, and denser town destinations complete
- D5.7H map playability, room cutaway, outdoor loot legality, and backpack quick-slot hardening complete
- D5.8/D5.8A expanded-map and cutaway iterations completed and owner-audited
- D5.9 original Map V2 implemented at the locked final graybox size with connected water, purposeful crossings, road hierarchy, residential variety, and civic/transit destinations
- D5.9 local survival loop implemented with 12 Bot-Lite opponents, shrinking safe zones, delayed air drops, throwable grenades, destructible soft barriers, and richer vehicles
- D5.9 product-shell pass completed for menu, loading, inventory, tactical map, and settlement
- D5.95 map-comfort pass completed with 173 buildings, 105 searchable interiors, real connected rows/internal doors, denser centered housing, 360 varied grass patches, 96 cover pieces, and 12 vehicle nodes
- D5.95 vehicle-comfort pass completed with smaller/tougher/faster vehicles, directional mass-scaled run-over damage, vehicle collisions, high-speed exits, lethal wreck explosions, and wider drive-through entrances
- D5.95 consistency/readability pass completed for indoor loot layers, Bot weapon/death-box identity, and clipped tactical-map circles

## Current Features

- Browser-playable local prototype
- Screen-relative movement
- Mouse aiming
- Original placeholder firearm tuning anchors
- Deterministic seeded core simulation
- Projectile collision and damage simulation
- Auto reload and reload progress UI
- Item-backed loot, ammo, healing, and inventory state
- Doors, interior visibility, death boxes, and active local Bot-Lite participants
- Legal randomized player/participant spawns and randomized loot
- Balanced car/pickup/van roles with four seats, acceleration, steering, braking, collision, projectile damage, run-over damage, high-speed exits, and lethal destruction
- Projectile- and vehicle-destructible soft guardrails/fences
- Backpack-backed throwable grenades with flight, bounce, fuse, line-of-sight, and radial damage
- Five-phase shrinking safe zone with current/next tactical-map rings and damage pressure
- Delayed deterministic air drops sampled inside the planned safe zone
- 12 active local Bot-Lite opponents with combat, stuck replanning, and safe-zone rotation
- Hide/reveal house cutaway behavior with interior props and cover
- Backpack item progression, right-click inventory handling, and equipment overflow behavior
- Large map overlay with a single player marker plus minimap readability improvements
- Client-side projected 2.5D graybox presentation
- Original graybox town with 173 visible buildings, 105 searchable interiors, 15 semantic zones, connected waterways, six purposeful crossings, east rail boundary, alleys, service roads, connected rows, and indoor-first loot
- Stronger map topology, accessibility, density, loot, spawn, and player-radius reachability checks
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

- Owner D5.95 map/vehicle feel playtest and bounded bug triage
- Performance caching, long-running match soak, and richer Bot behavior
- Harden the complete single-player Battle Royale loop
- Demo hardening and visual readability pass
- Server-readiness audit
- Local authoritative multiplayer vertical slice
- Multiplayer feature parity and 6-human Internet test

## Status

Active development.

This is not an official remake, port, or licensed continuation of any existing game.
