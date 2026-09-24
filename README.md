# Last Pixel

Last Pixel is an original browser-first 2.5D survival shooter: one dense water town, short
readable matches, deterministic rules, and a final-circle finish.

> **Current public build:** M2.5 / M3.4 single-player midterm
>
> **Online status:** frozen for the current cycle; no public matchmaking URL is advertised.

## Play Now

**[Open the current browser game](https://cyh29hao.github.io/last-pixel/)**

The public Pages build runs a complete solo match with one local player and 12 Bot-Lite opponents.
It requires a desktop keyboard and mouse. No account, game server, cloud save, analytics, or
gameplay telemetry is used.

Controls: `WASD` move, mouse aim, left click fire, `F` interact, `Tab` inventory, and `M` tactical
map.

The game itself adds no cookies. GitHub Pages may process connection data under GitHub's own
policy; see the [playtest privacy note](https://cyh29hao.github.io/last-pixel/PRIVACY.txt).

## What Is in the Public Build

- One original `18,000 × 16,800` water-town map with 180 visible buildings and 109 searchable
  interiors
- 13-participant local matches: one player and 12 active Bot-Lite opponents
- Firearms and ammunition, healing, armor, backpacks, grenades, death boxes, destructible doors,
  soft barriers, indoor-weighted loot, and persistent air drops
- Five shrinking safe-zone phases, tactical map and minimap, announcements, inventory, and match
  settlement
- 20 drivable cars, pickups, and vans with seats, collision damage, run-over consequences, and
  wreck explosions
- Seeded simulation and placement for reproducible failures and varied normal starts
- Fair Bot openings with no hidden weapons/ammunition, real visible world pickup, searchable-area
  movement, existing-door use, bounded stuck recovery, and profile-specific local cover preference
- Denser deterministic indoor/high-value-area loot, real loaded/reserve ammunition in the combat
  HUD, and a larger desktop Tab loadout

## Current Development Boundary

The active cycle optimizes only the single-player match. Accounts, rooms, servers, WAN deployment
and multiplayer promotion are frozen. Historical Online code remains private and is not presented
as current product progress.

## Verification Snapshot

The current private workspace gate passes:

- research: 9 tests
- game core: 172 tests
- protocol: 11 tests
- client: 134 tests
- game server: 34 tests
- repository typecheck, lint, formatting, tests, and builds
- Pages artifact leak scan and JavaScript budget gate

The public Pages artifact matches the verified current single-player workspace checkpoint.

## Availability and Boundaries

The public `main` branch is a fail-closed showcase containing only this README. The isolated
`gh-pages` branch contains only the scanned compiled solo artifact. Private TypeScript source,
source maps, internal documents, research material, credentials, and the multiplayer server are
not published here.

The current public build is an original graybox. Production art/audio, final balance, complete
tactical Bot behavior, mobile controls, and Online features are not included. Last Pixel is not an
official remake, port, or licensed continuation of any existing game.

## Next Gates

1. Evidence-first M4.1 diagnosis of empty traversal, vehicle clearance, and key POI connectivity
2. Original in-match visual language, then an audited footsteps/fire/vehicle/proximity sound slice
3. Longer human matches and the remaining per-profile balance sample before final acceptance

The earlier D5.95 milestone remains available as a historical
[prerelease](https://github.com/Cyh29hao/last-pixel/releases/tag/d5.95-playtest).
