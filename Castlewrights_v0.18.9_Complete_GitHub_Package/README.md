# Castlewrights v0.18.9 — Sally Corrections + Experimental Assault

A single-file, offline-capable browser game. Deploy `index.html` at the root of GitHub Pages, or open it directly in a modern browser.

## Mode selection
- **Campaign (6 sieges):** Existing full defense campaign, inherited from v0.18.8.
- **Sandbox (3 sieges):** Existing defense sandbox.
- **Experimental Assault (1 mission):** Eastern Watch, a deliberately isolated single assault scenario.

Change the **Mode** selector and press **New game**.

## Sally correction
- Selected melee units prioritize reachable **crossbowmen**; when none are viable they pursue the **nearest reachable attacker** within a radius of six map tiles of the sortie anchor.
- Targets are retained to avoid oscillating between similar threats; a crossbowman can override a non-crossbow target.
- Low-health and no-target withdrawal remains in effect.
- Soldiers can return using an alternate passable route. Being inside the castle but away from the post is tracked as **displaced**, not falsely as trapped outside.
- The prior two-soldier limit and map-based exit selection remain.

## Experimental assault controls
1. Choose **Experimental Assault (1 mission)** in Mode, then press **New game**.
2. Choose one of three groups and recruit troops into it with your 120-gold total budget.
3. Assign each group's approach (north/east/south/west) and an order: **Breach selected wall** or **Assault keep**.
4. For Breach, tap a white wall or gold gate segment on the game board to choose the target.
5. Press **Launch assault**, then **Advance one turn** or **Resolve assault**.
6. Export the assault's JSON event history using **Export assault JSON**.

Victory: bring the target keep to zero HP within 24 turns. Loss: all attackers killed or the turn limit expires.

## Important limitations
- The attack scenario is an experimental *role-reversal slice*, not another chapter in the defense campaign. It uses the same grid/edge barrier system, shared obstacle/path movement helpers, and nominal troop damage values, but currently has its own compact turn resolver and enemy-garrison AI.
- Attack archers use simplified range checks (without the full defense simulation's obstruction and elevation model); melee unit engagement and group formations are also simplified.
- Troops in one group follow the same objective, but this does not confer formation bonuses or coordinated timing.
- The preset garrison, assault cost balance and 24-turn limit have not been statistically tuned.
- The original defensive campaign has not received a full six-siege automated regression in this release.

## Files
`index.html` is the Pages entry point. `Castlewrights_v0.18.9.html` is the versioned equivalent. `TEST_REPORT.md` documents focused verification.
