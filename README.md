# Last Pixel

An original browser-first 2.5D top-down survival shooter prototype built around short,
readable matches, deterministic rules, and a dense small-town battlefield.

> **Current public build:** D6.3 Single-player Closeout
>
> The permanent Pages build has one local player and 12 Bot-Lite opponents. A separate
> owner-hosted early multiplayer alpha is also playable while the test PC is online.

## Play Online

**[Launch the D6.3 browser playtest](https://cyh29hao.github.io/last-pixel/)**

Desktop keyboard and mouse are required. This is a static single-player build: no login,
analytics, multiplayer server, cloud save, or account system is used.

The project adds no cookies or telemetry. GitHub Pages may process connection data under
GitHub's own policy; see the [playtest privacy note](https://cyh29hao.github.io/last-pixel/PRIVACY.txt).

## Try the Multiplayer Alpha

**[Open the home-hosted Online test](https://desktop-bsm6imq.taild233f6.ts.net:8443/?auth=play)**

No account creation or Tailscale installation is required. Open **Online**, choose
**Quick Guest Join**, then use `WASD`/arrow keys to move, the mouse to aim, left click or `Space`
to fire, `R` to reload, and `E` to pick up. Desktop Chrome or Edge is recommended.

This is a minimal authoritative combat test, not the complete D6.3 game: two or more guests can
share a room, move, collect starter weapons, fire, and take server-judged damage. It is available
only while the owner PC is powered, awake, online, connected to Tailscale, and running the home
stack. Players need only a normal internet connection; if the link is unavailable, use the
permanent single-player Pages build above.

## Current Game

Drop into an original `18,000 x 16,800` water-town, search interiors for equipment, fight
through a five-phase shrinking safe zone, use vehicles and grenades to break stalemates,
contest delayed air drops, and survive until one participant remains.

The current public loop includes:

- 13-participant local matches: one player and 12 active Bot-Lite opponents
- 180 visible buildings, 109 searchable interiors, connected commercial rows, alleys,
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

Fresh D6.3 closeout checks passed:

- the complete 62-test browser regression suite;
- the full repository typecheck, lint, test, and build gate;
- visual review and one-click browser smoke;
- the source-map/private-marker scan and fail-closed JavaScript gzip budget.

D6.3 inherits D6.1's passed hardening baseline: 100/100 deterministic same-page match
lifecycles, active-Bot full-zone statistics, regular/stress performance, and a strict 20-minute
Edge heap run with five restarts, zero runtime errors, and 1.6% measured heap growth. Those long
gates were not rerun specifically for D6.3.

The formal `v0.1-demo` tag still requires the owner's final three-match acceptance and explicit
tag decision. The Vite/Phaser large-chunk warning remains a known non-blocker.

## Development Status

Authoritative multiplayer engineering is active in the private development line. The shared
deterministic simulation and the first MP0b slices for loot, pickup arbitration, private
inventory, death boxes, doors, soft barriers, firearms, and matching ammunition have passed
local automated and real two-client WebSocket checks.

The zero-rental-cost owner-PC transport path now has public HTTPS, credentialed cross-origin
matchmaking, WebSocket transport, and a temporary signed guest path. A two-browser public verifier
observed one shared room, replicated movement, target health changing from 100 to 83, and no page
errors; the real-WebSocket server suite independently locks those decisions to the authority.
Full D6.3 parity,
throwables, vehicles, zones, air drops, Bots, complete equipment interaction, matchmaking, Bot
fill, prediction/reconciliation, real-human latency/reconnect testing, abuse controls, mobile
controls, and final UI remain open.

## Availability

The permanent single-player game is published as a scanned static artifact from the isolated
`gh-pages` branch. The early multiplayer alpha is served separately from the owner PC and is not
stored in this public repository.
The public `main` branch remains a fail-closed showcase containing only this README. No private
TypeScript source, source maps, internal documents, research corpus, downloadable package,
credentials, or multiplayer server are published.

The earlier D5.95 milestone remains available as a historical
[prerelease](https://github.com/Cyh29hao/last-pixel/releases/tag/d5.95-playtest).

## Next

- Finish MP0b migration until the authoritative simulation reaches complete D6.3 rule parity
- Add public/private rooms for 2-6 humans with Bot fill to 13 participants
- Validate real-human WAN latency/reconnects, abuse controls, and an always-on hosted authority
- Complete owner acceptance and make a separate decision on the formal `v0.1-demo` tag

The current public build remains an original graybox: production art/audio, final balance, full
Bot behavior, and a deployed multiplayer product are not included. Last Pixel is not an official
remake, port, or licensed continuation of any existing game.
