# Focused verification — v0.18.9

- JavaScript syntax check: PASS (`node --check`).
- Defense campaign initializes at 390px and 1280px: PASS, no JavaScript exceptions.
- Experimental assault initializes at 390px and 1280px: PASS, no JavaScript exceptions.
- Recruits assigned to groups; attack launched; turn-by-turn resolution completes with a victory in a prepared seven-unit test force: PASS, victory on Turn 9.
- Weak one-spearman attacking force yields a defeat rather than a forced victory: PASS.
- Custom group side and wall-selection changes reflected in group UI: PASS.
- Assault-to-campaign mode change resets to original keep placement: PASS.
- No page-level horizontal overflow at 390px or 1280px during checked flows: PASS.
- Controlled sally scenario: nearby reachable crossbowman selected ahead of a nearer raider; once the crossbowman is eliminated, raider selected: PASS.

## Not yet verified
- Complete automated six-siege defense regression.
- Exhaustive sally path topology under all damaged-gate and wall combinations.
- Balance across multiple offensive force compositions/seeds.
- Physical mobile-device tap ergonomics.
- Battle parity across both modes: assault currently uses a simplified own turn loop, sharing geometry and movement helpers rather than every defense combat rule.
