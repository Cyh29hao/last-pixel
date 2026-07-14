# Last Pixel

An original browser-first 2.5D top-down survival shooter prototype built around short,
readable matches, deterministic rules, and a dense small-town battlefield.

> **Current milestone:** [D5.95 — Map & Vehicle Comfort Playtest](https://github.com/Cyh29hao/last-pixel/releases/tag/d5.95-playtest)
>
> Local single-player graybox with 12 Bot-Lite opponents. Multiplayer, production art,
> public binaries, and online hosting are not part of this release.

## The Game Today

Drop into an original `18,000 x 16,800` town, search interiors for equipment, fight through
a five-phase shrinking safe zone, use vehicles and grenades to break stalemates, contest
delayed air drops, and survive until one participant remains.

The current playable loop includes:

- 13-participant local matches: one player and 12 active Bot-Lite opponents
- Item-backed weapons, ammunition, healing, armor, backpacks, death boxes, and indoor loot
- Projectile combat, auto reload, throwable grenades, soft barriers, and grass concealment
- Five-phase safe-zone pressure, delayed deterministic air drops, and victory/defeat flow
- Drivable cars, pickups, and vans with seats, damage, collisions, run-over consequences,
  high-speed exits, and lethal wreck explosions
- Seeded simulation and map placement for reproducible tests and varied normal starts

## D5.95 World Pass

D5.95 focuses on making the locked-size map feel intentional instead of merely large:

- 173 visible buildings across 15 semantic zones
- 105 searchable interiors and 68 intentionally closed structures
- Connected commercial and residential rows with shared-wall passages and internal doors
- Center-weighted housing, alleys, service roads, connected waterways, six purposeful
  crossings, a rail boundary, civic/transit destinations, and indoor-first loot placement
- 360 varied seeded grass/brush patches, 96 urban cover pieces, and 12 vehicle nodes
- Brighter interior cutaways that keep loot and actors readable
- Wider entrance hierarchy so cars can enter common buildings and larger vehicles can use
  selected flagship entrances

## D5.95 Vehicle Pass

Vehicle roles are smaller, tougher, faster, and more responsive while retaining distinct
car, pickup, and van handling. The rules now account for:

- Run-over damage based on collision-normal relative speed and vehicle mass
- Vehicle-to-vehicle impulse, velocity response, and mutual damage
- High-speed exit damage and safe-exit validation
- Occupant death and a small falloff blast when a vehicle is destroyed
- Projectile- and vehicle-destructible soft guardrails and fences

## Quality Snapshot

The D5.95 checkpoint passed the private development repository's full local gate:

- TypeScript typecheck, ESLint, Prettier, package builds, and production client build
- 123 unit tests: 9 research, 82 game-core, and 32 client
- 40/40 Playwright browser tests with one supported heavyweight game client
- One-click local cold-start smoke at HTTP 200 with the D5.95 label
- Seeded spawn/loot sampling and a 91/100 visual QA verdict

The production build retains a known non-blocking Phaser/Vite large-chunk warning. Extreme
vehicle motion is not yet swept-collision based, and Bot looting, healing, doors, throwables,
driving, and full pathfinding remain future work.

## Architecture

- TypeScript, Phaser, Vite, Vitest, and Playwright
- Pure deterministic `game-core` rules separated from Phaser rendering and browser globals
- Client-owned projected 2.5D presentation
- Regression-tested map topology, accessibility, density, spawn, loot, and vehicle contracts
- One-click local play/stop workflow in the private development tree

## Availability

D5.95 is a **release-notes-only GitHub prerelease**. This public repository remains a
fail-closed showcase containing only this README. It does not publish the private source
tree, a downloadable game build, GitHub Pages, or an online server.

## Next

- Owner feel review and bounded comfort/balance fixes
- Static world-render caching and long-running multi-match soak coverage
- Single-player demo hardening and original production visual work
- Server-readiness audit, then a local authoritative multiplayer vertical slice
- Multiplayer parity and a six-human Internet test

## Project Status

Active development. Last Pixel is an original project, not an official remake, port, or
licensed continuation of any existing game.
