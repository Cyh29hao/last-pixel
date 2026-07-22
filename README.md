# Last Pixel

An original browser-first 2.5D top-down survival shooter prototype built around short,
readable matches, deterministic rules, and a dense small-town battlefield.

> **Current public build:** D6.3 Single-player Closeout
>
> One local player and 12 Bot-Lite opponents. No multiplayer service is deployed.

## Play Online

**[Launch the D6.3 browser playtest](https://cyh29hao.github.io/last-pixel/)**

Desktop keyboard and mouse are required. This is a static single-player build: no login,
analytics, multiplayer server, cloud save, or account system is used.

The project adds no cookies or telemetry. GitHub Pages may process connection data under
GitHub's own policy; see the [playtest privacy note](https://cyh29hao.github.io/last-pixel/PRIVACY.txt).

## Current Game

Drop into an original `18,000 x 16,800` water-town, search interiors for equipment, fight
through a five-phase shrinking safe zone, use vehicles and grenades to break stalemates,
contest delayed air drops, and survive until one participant remains.

The current public loop includes:

- 13-participant local matches: one player and 12 active Bot-Lite opponents
- 176 visible buildings, 108 searchable interiors, connected commercial rows, alleys,
  bridges, rail boundary, hospital, hotel, restaurant, sports fields, and civic POIs
- Item-backed weapons and matching ammunition, healing, armor, backpacks, grenades, death
  boxes, destructible doors/soft barriers, and indoor-weighted loot
- Five-phase safe-zone pressure and persistent hard-collision air drops constrained to the
  active white circle
- 20 drivable cars, pickups, and vans with seats, collision damage, run-over consequences,
  high-speed exits, and lethal wreck explosions
- Bot road/bridge routing, white-circle priority, finite weapons/ammo, consistent drops, and
  one cautious first-aid use
- Full lobby, how-to-play and equipment guide, tactical map/minimap, compact HUD,
  announcements, combined loot/death-box inventory view, and match settlement
- Seeded simulation and placement for reproducible tests and varied normal starts

## Verification Snapshot

The published D6.3 closeout passed:

- the complete 62-test browser regression suite;
- 100/100 deterministic same-page match lifecycles;
- active-Bot full-zone statistics and regular/stress performance gates;
- a strict 20-minute Edge heap run with five restarts, zero runtime errors, and 1.6% measured
  heap growth;
- the source-map/private-marker scan and fail-closed JavaScript gzip budget.

The formal `v0.1-demo` tag still requires the owner's final three-match acceptance and explicit
tag decision. The Vite/Phaser large-chunk warning remains a known non-blocker.

## Development Status

Authoritative multiplayer engineering is active in the private development line. The shared
deterministic simulation and the first MP0b slices for loot, pickup arbitration, private
inventory, death boxes, doors, soft barriers, firearms, and matching ammunition have passed
local automated and real two-client WebSocket checks.

That engineering checkpoint is not a deployed multiplayer game and does not yet have full D6.3
feature parity. Throwables, vehicles, zones, air drops, Bots, complete equipment interaction,
matchmaking, Bot fill, prediction/reconciliation, hosted-provider testing, and production
identity configuration remain open.

## Availability

The online game is published as a scanned static artifact from the isolated `gh-pages` branch.
The public `main` branch remains a fail-closed showcase containing only this README. No private
TypeScript source, source maps, internal documents, research corpus, downloadable package,
credentials, or multiplayer server are published.

The earlier D5.95 milestone remains available as a historical
[prerelease](https://github.com/Cyh29hao/last-pixel/releases/tag/d5.95-playtest).

## Next

- Finish MP0b migration until the authoritative simulation reaches complete D6.3 rule parity
- Add public/private rooms for 2-6 humans with Bot fill to 13 participants
- Validate hosted authority, production identity boundaries, and real multi-human WAN play
- Complete owner acceptance and make a separate decision on the formal `v0.1-demo` tag

The current public build remains an original graybox: production art/audio, final balance, full
Bot behavior, and a deployed multiplayer product are not included. Last Pixel is not an official
remake, port, or licensed continuation of any existing game.
