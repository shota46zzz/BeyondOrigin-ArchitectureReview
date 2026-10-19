# OW-06 Black Castle — Architecture Draft v1

Status: `DRAFT / VISUAL_REVIEW_PENDING`. This is development-time architecture authoring code. There is no approved Structure NBT, runtime placement, gameplay, boss logic, reward, or worldgen integration.

## Design source and specification difference

- `docs/06_黒い城.md`: extra-large, Black Knight King, 64×64 arena, and the progression below.
- `docs/ARCHITECTURE_DESIGN.md` §13.6 and `docs/GAME_DESIGN.md`: extra-large cursed royal fortress, central hall + king arena landmarks.
- The multi-dungeon request calls OW-06 “large”; existing finalized documents say **extra-large**. This draft uses the documented extra-large program and records the wording difference for Human review.

## First-pass spatial composition

Coordinates are local and half-open where written as bounds. +Z leads inward from the gate. The draft is deliberately long enough to give the 64×64 arena its own silhouette rather than hiding it inside the hall.

| Space | Local X | Local Z | Approximate floor Y | Form / role |
|---|---:|---:|---:|---|
| Gate and twin gate turrets | -35..34 | -24..2 | 0 | Open 11-wide entry under a heavy bridge; defensive skyline |
| Courtyard and broken royal statue | -49..49 | 2..43 | 0–2 | Broad sky court and readable central landmark |
| West Hunter Tower | -54..-32 | 40..62 | 0, 12, 24 | Stout crown and two-wide internal stairs |
| East Mirror Tower | 32..54 | 40..62 | 0, 12, 24 | Taller open spire and two-wide internal stairs |
| Central Great Hall | -31..31 | 44..90 | 1, 16, 31–41 | Columned nave, side galleries, high pitched roof |
| Cursed Corridor | -15..15 | 91..119 | 1 down to -9 | Narrower recesses remain on the main route |
| Underground Altar | -19..19 | 120..139 | -10 | Excavated altar chamber; no reward/encounter content |
| Ascending route / Phantom Garden | -30..30 | 139..169 | -9 up to 2 | Re-emergence into a roofless garden |
| Boss Arena | **-32..31** | **170..233** | 2 | **64×64 clear fighting floor** with outer walls outside the combat square |
| Rear throne | -7..7 | 236..240 | 3–4 | Arena endpoint beyond the protected fighting floor |

The authored block envelope is `X [-67,68) / Y [-12,55) / Z [-25,241)`. The boss fighting volume is `X [-32,32) / Y [3,21) / Z [170,234)`; normal structure elements are outside that clear volume. The roofed hall, unequal towers, open court, sunken altar, roofless garden, and independent arena are intended to read as a fortress complex from front, side, and oblique views.

## Reproduction

Use a **copy** of a flat development world with a surface at Y14 or higher and a clear approximately 140×266 site. The command is development-only:

```text
/bo debug black_castle_draft
```

The unrotated local anchor is 28 blocks south of the command player's position, on the measured surface. The placement registers review ID `ow06_black_castle_draft_v1` with 16 named interior/close views plus five exterior views. The command refuses non-flat or occupied sampled sites and never exports or loads NBT.

## Automated guard and unfinished checks

- Every block write is checked against the declared 3D envelope.
- The preview command samples terrain height and above-ground vacancy before placing.
- The arena reserves the full 64×64 square; there are no pillars or normal spawner placements in it.
- Fix Round 2 was placed in a disposable flat-world copy at anchor `(690000,4,690000)` and captured in 21 Minecraft PNG views. This validates the pictured draft only; step geometry, route walking, tower ascent, natural-terrain blending, and exhaustive floating-block checks remain **UNVERIFIED**. A sampled site check does not prove every block of a world is empty.
- Castle-scale roof, lighting, ruin variation, and the ceremonial spatial rhythm require AI/Human visual review. This is a first Draft, not an approved asset.

## Visual review fixes

Fix Round 1 closed the altar's broad bright gap and the great hall's central upper gap. AI Visual Re-Review of 18/18 Minecraft images returned `NEEDS_FIX` for R01 (east/west silhouette), R03 (garden legibility), and R06 (tower distinction), while R04 was closed. Fix Round 2 added two supported cross-wings and a stepped curtain, small uneven overgrown garden beds, a glazed vertical Mirror Tower face/crown, and a Hunter Tower firing platform/slits. The central progression, altar closure, hall roof, and open 64×64 arena are retained. Fix Round 2 still needs AI and Human visual review.

## Protected scope

No Ancient Ruins, White Castle, existing Structure NBT, or gameplay data is changed by the Black Castle authoring command. The command must only be run in a separate draft world; it is not a runtime fallback.
