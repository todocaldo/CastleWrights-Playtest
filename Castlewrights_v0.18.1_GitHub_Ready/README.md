# Castlewrights v0.18.1 — Broken Pass / Construction Intelligence

This is a focused experimental update to v0.18.0. The standalone `index.html` is ready for a GitHub Pages repository root and has no external runtime dependencies. `Castlewrights_v0.18.1.html` is an identical, version-named copy.

## Changes

- Campaign Chapter 2 is now **The Broken Pass**: cliffs block lateral approaches and create two genuine attack corridors (narrow north; wider south), with a constrained central build space. Cliff cells block both building and movement; enemies spawn on the approach lanes. Chapter 1's open map and sandbox mode are preserved.
- **Tower access:** friendly troops can enter towers via an accessible adjoining courtyard position, including a staircase/access transition past a diagonally adjoining fortification. Enemies remain subject to diagonal barriers. A tower's access is separately tested and shown with a green/red dashed outline.
- **Preview access assessment:** hovering is not required. Tap to preview a wall, diagonal, or building, then see prospective gate-to-keep courtyard connectivity and accessible tower count before confirming placement. Preview costs no gold.
- **Construction-phase line of sight:** preview a new tower to see its reach automatically, or tap an existing tower / use **Tower sightlines** and **Inspect next tower** to see clear (teal) and range-limited-but-blocked (amber) cells. The overlay uses the same `los()` function as combat. Elevated archers retain the original single-adjacent-wall allowance.
- All other costs, gold grants, building/troop choices, and chapter progression remain unchanged.

## Known limitations

- The diagonal wall still uses the pre-existing simplified corner-obstruction model rather than exact polygon-based collision. The special friendly tower-access accommodation is a game rule, not a complete wall-walk/stairway simulation.
- Tower firing coverage is calculated using the game's existing integer grid/range and simplified obstacle sampling; real-world firing arcs and height are not modeled.
- No new troop command, combat balance, or economy rebalance is included.
- Full unassisted six-siege campaign balance and physical mobile device behavior are not verified.

See `TEST_REPORT.md` for checks actually run.
