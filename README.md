# Last Pixel

An original browser-first 2.5D top-down survival shooter prototype built around short,
readable matches, deterministic rules, and a dense small-town battlefield.

> **Current online build:** D6 Demo Hardening Candidate
>
> Local single-player graybox with 12 Bot-Lite opponents. Multiplayer, production art,
> final UI/audio, attachments, and final balance are not included.

## Play Online

**[Launch the D6 browser playtest](https://cyh29hao.github.io/last-pixel/)**

Desktop keyboard and mouse are required. This is a static single-player build: no login,
analytics, multiplayer server, cloud save, or account system is used.

The project adds no cookies or telemetry. GitHub Pages may process connection data under
GitHub's own policy; see the [playtest privacy note](https://cyh29hao.github.io/last-pixel/PRIVACY.txt).

## Current Game

Drop into an original `18,000 x 16,800` water-town, search interiors for equipment, fight
through a five-phase shrinking safe zone, use vehicles and grenades to break stalemates,
contest delayed air drops, and survive until one participant remains.

The current loop includes:

- 13-participant local matches: one player and 12 active Bot-Lite opponents
- 173 visible buildings, 105 searchable interiors, connected commercial rows, alleys,
  bridges, rail boundary, hospital, hotel, restaurant, school sports fields, and civic POIs
- Item-backed weapons, matching ammunition, healing, armor, backpacks, death boxes, and
  indoor-weighted loot
- Projectile combat, grenades, destructible soft barriers, grass concealment, global kill
  feed, five-second death observation, and persistent empty containers
- Five-phase safe-zone pressure and hard-collision air drops constrained to the white circle
- Drivable cars, pickups, and vans with seats, swept movement, damage, collisions,
  run-over consequences, high-speed exits, and lethal wreck explosions
- Bot road/bridge routing, white-circle priority, finite weapons/ammo, consistent drops, and
  one cautious first-aid use that cancels for enemies or urgent zone movement
- Seeded simulation and map placement for reproducible tests and varied normal starts

## D5.96 Map and Balance Pass

- Connected and shortened water routes with purposeful crossings
- Three large searchable POIs plus football and basketball facilities
- Building-edge and roadside vegetation instead of large empty grass fields
- Streetlights, benches, road signs, connected-room buildings, and denser central housing
- Expanded weapon roster and loot rebalance, stronger S686/RPG roles, and gun/ammo pairing
- More responsive vehicles with 20% extra health and safer high-speed exit damage

## D6 Hardening

- Development-only diagnostics and runtime tuning are isolated behind explicit debug/test
  query capabilities and are absent from the ordinary public URL
- Static map rendering, camera culling, broad-phase projectile/collision queries, throttled
  debug publication, and change-driven redraw paths
- Atomic clean-match snapshots plus exact ammunition, item, consumable, and elimination
  accounting across repeated matches
- Deterministic soak coverage for 100 same-page match lifecycles, active 12-Bot full-zone
  simulations, and 15-Bot/200-projectile stress

## Verification Snapshot

- 100/100 deterministic same-page match lifecycles passed with zero clean-start transient
  leaks and zero page/console errors
- 10 full-zone seeds: 21/120 Bot safe-zone eliminations (17.5%, under the 20% budget)
- Regular 12-Bot performance: 59.8 average FPS and 17.3ms reported p95 frame time
- 15-Bot + 200-projectile stress: 50.3 median FPS, 62.6Hz simulation tick, 1.02x rule time
- First public-build readiness remains under 3 seconds; a long 100-match session reached a
  13.8-second later-match initialization outlier, retained as a known optimization risk

The strict 20-minute heap gate and the owner's final three-match acceptance are still
pending. The Vite/Phaser large-chunk warning remains visible rather than being hidden.

## Availability

The online build is published as a scanned static artifact from the isolated `gh-pages`
branch. The public `main` branch remains a fail-closed showcase containing only this README.
No private TypeScript source, source maps, internal documents, research corpus, downloadable
package, or online game server are published.

The earlier D5.95 milestone remains available as a historical
[prerelease](https://github.com/Cyh29hao/last-pixel/releases/tag/d5.95-playtest).

## Next

- Bounded map/minimap and vehicle-placement closeout from owner playtest feedback
- Bot collision safety and equipment/drop variety
- Weapon, ammunition, RPG, backpack, and attachment balance work
- Final demo acceptance, then server-readiness audit and authoritative multiplayer work

Last Pixel is an original project, not an official remake, port, or licensed continuation
of any existing game.
