# Castlewrights v0.18.1 — Verification report

## Verified locally

- JavaScript syntax validation with Node `--check`: passed.
- Chromium via Playwright, rendered using `page.set_content` because this test browser blocks navigation to local files.
- Chapter 1 remains an open battlefield.
- Chapter 2: northern pass accepts columns 2–3; southern pass accepts columns 3–5; other approach cells are impassable cliffs.
- Chapter 2: keep and south gate placed; required gate-to-keep courtyard reported connected.
- Tower placement preview reports post-placement courtyard status and tower access, and tower can be confirmed.
- An adjoining diagonal wall did not remove access to the tested tower.
- Tower firing coverage toggle works in construction phase, before deployment.
- Wall preview updates access diagnostics without consuming gold or modifying the real wall collection.
- An actual Chapter 2 combat simulation spawned eight enemies only in prescribed pass cells and reached defeat when the keep was destroyed at tick 13. This tests termination, not win balance.
- 390px viewport had no page-level horizontal overflow or JavaScript exceptions in these scenarios.

## Not established

- All potential keep/gate configurations and every diagonal / tower arrangement.
- Realistic full chapter combat balance or human playtesting.
- Six-siege no-cheat campaign completion.
- Physical touchscreen ergonomics, especially selecting tightly packed edges.
