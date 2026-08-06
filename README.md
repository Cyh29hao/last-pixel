# Last Pixel

Last Pixel is an original browser-first 2.5D survival shooter: one dense water town, short
readable matches, deterministic rules, and a final-circle finish.

> **Stable public build:** D6.3 single-player
>
> **Multiplayer status:** local owner-verification candidate; no stable public matchmaking URL is
> advertised yet.

## Play Now

**[Open the D6.3 browser game](https://cyh29hao.github.io/last-pixel/)**

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

## Multiplayer Development

The private development line no longer treats a separate lightweight online demo as the target.
The current local candidate enters the same Phaser `CombatScene` used by the accepted D6.3 solo
game, while the server remains authoritative for movement, interactions, combat, and results.

Fresh local two-browser verification passed guest entry, room readiness, shared-scene movement,
pickup, damage, elimination, and matching settlement. The candidate is still waiting for owner
play acceptance and a broader long-session interaction matrix. It is therefore an engineering
candidate, not a public multiplayer release.

The older owner-PC Tailscale route is deliberately not promoted here: repeated tests exposed a
one-way WebSocket failure mode, so it is not evidence of production-quality play.

## Verification Snapshot

The current private workspace gate passes:

- research: 9 tests
- game core: 154 tests
- protocol: 11 tests
- client: 133 tests
- game server: 34 tests
- repository typecheck, lint, formatting, tests, and builds
- Pages artifact leak scan and JavaScript budget gate

The already published Pages build remains the stable D6.3 solo artifact. Replacing it with a newer
artifact requires a separate review and explicit publication decision.

## Availability and Boundaries

The public `main` branch is a fail-closed showcase containing only this README. The isolated
`gh-pages` branch contains only the scanned compiled solo artifact. Private TypeScript source,
source maps, internal documents, research material, credentials, and the multiplayer server are
not published here.

The current public build is an original graybox. Production art/audio, final balance, full Bot
behavior, mobile controls, and a deployed multiplayer product are not included. Last Pixel is not
an official remake, port, or licensed continuation of any existing game.

## Next Gates

1. Owner feel comparison between the accepted offline build and the shared-scene online candidate
2. Extended doors, vehicles, throwables, healing, inventory, death-box, reconnect, and settlement
   verification
3. Fixed-origin hosted multiplayer deployment only after the first two gates pass

The earlier D5.95 milestone remains available as a historical
[prerelease](https://github.com/Cyh29hao/last-pixel/releases/tag/d5.95-playtest).
