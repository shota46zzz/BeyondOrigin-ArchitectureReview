# OW-06 Black Castle — Draft Fix Round 1

Status: `DRAFT_BUILD_ONLY` / AI re-review pending / Human approval pending. No NBT, Gameplay, Boss AI, or Worldgen integration.

## Source and placement

- Architecture ID: `ow06_black_castle_draft_v1`
- Previous fixed Evidence: `f30a18c09af4ebe8a83e276adaef6ccfb740c42a`
- Code commit: `45cfd76` (`codex/ow06-black-castle-draft`)
- Flat-world review copy: `ow06-black-castle-fix-round1-final2-20261020`
- Anchor: `(690000, 4, 690000)`
- Bounds: X `-67..67`, Y `-12..54`, Z `-25..240` (metadata max exclusive)
- Protected boss fighting volume: X `-32..31`, Z `170..233` (64 × 64)

## Review issues addressed

- R01: joined the gate to both curtain walls, added supported side galleries and rear wall transitions, and paved the common castle ground. The intentional ruined openings remain.
- R02: enclosed the altar passage and stair sides; the nine-block-wide stair route remains open.
- R03: added uneven garden beds, dead trees, and small side ruins.
- R04: closed the great hall end-wall sky band while retaining narrow upper slits and the side clerestory.
- R05: added flat arena floor inlay, side-wall buttresses, and a rear throne facade outside the protected fighting volume.
- R06: differentiated the Mirror and Hunter tower upper silhouettes.

## Verification limits

`compileJava` passed. Minecraft placement and all 18 screenshots completed in a new disposable flat-world copy. The screenshot metadata records SHA-256 per PNG. Images establish visual appearance; walking, mob navigation, natural terrain integration, NBT, and Gameplay remain unverified. No formal Architecture approval is implied.
