# OW-03 Airship Architecture Draft v1

State: `DRAFT_BUILD_ONLY` — Human and AI visual review pending. This is not a Structure NBT, runtime asset, gameplay implementation, or approved dungeon.

## Source and form

- Sources: `03_飛空艇.md`, `ARCHITECTURE_DESIGN.md` §13.3, and the supplementary Design Bible.
- Architecture ID: `overworld/ow03_airship/draft_v1`; debug target `ow03_airship_draft_v1`.
- Fixed local bounds: X -19..19, Y 0..47, Z -51..49. Anchor in a disposable flat Overworld copy: `(640000,100,640000)`.
- Longitudinal axis: stern and boarding at negative Z, sculpted bow at positive Z.
- Silhouette: narrowed keel, curved hull, side strakes and ribs, full main deck, raised stern cabin, mast/lookout, suspended striped gas envelope, side engine fins.
- Materials: dark oak hull and beams, spruce decks, wool envelope, iron engine fittings. No placed mob, spawner, chest, vault, boss, loot or active machinery.

## Planned progression and reservation

1. Stern gangway at Z -51..-42; its remote connection to terrain is a future world placement decision.
2. Central deck Y14, full deck running the ship length.
3. Crew quarters below deck around Z -38..-15, entered by a four-wide stair at Z -27..-20.
4. Cargo hold around Z -13..10, with frames and open combat aisle.
5. Engine room around Z 12..30. Three inactive apparatus positions: local X -7, 0, +7 / Y9 / Z20. The approved three-device mechanic is reserved; no activation logic exists.
6. Return stair at Z 24..31 and starboard external deck X9..16 / Z12..31. Phantom event and exterior combat space are reserved, without a spawner.
7. Mast lookout at Y27 with ladder and scenery control.
8. Raised helm in stern cabin around X -9..9 / Z -38..-25.
9. Enclosed final reward room around X -7..-4 / Z -34..-29. The Flight Sword reward is reserved, not placed.

The exact progression locking, 8–12 spawner positions, 7–10 chest locations, and enemy behavior await Gameplay design. No boss arena is included because the dungeon specification has no boss.

## Preview and evidence

Use a disposable copy of a flat development world. From a Creative player in a private singleplayer Overworld, run `/bo debug ow03_airship_draft_v1`, then `/bo debug architecture_review ow03_airship_draft_v1`. The first command refuses occupied planned cells; the second records five exterior and nine authored review viewpoints in `build/architecture-review/ow03_airship_draft_v1/` with `metadata.json` and PNG hashes. An opt-in startup capture is available with `-Dbeyond_origin.ow03_airship.autopreview=true` on a fresh preview copy.

The debug placer is intentionally fixed to a high, remote location; it does not sample terrain or perform Worldgen. Screenshots are required before Visual Review. Build validation alone does not establish visual quality, physical walkability, terrain connection, or Human approval.

## Automated checks and open questions

- `compileJava` and the targeted `ArchitectureReviewTargetTest` pass in the isolated worktree.
- The plan checks local bounds, gross volume, lower deck continuity, three engine positions, and lookout opening during creation. Development-client placement and screenshot capture are still pending.
- Open design decision: how the stern gangway connects to real terrain or discovery point. Worldgen integration is outside Draft scope.
- Potential visual issues to inspect: balloon/hull proportions, deck-to-lower stairs, helm/reward-room legibility, support fin silhouette, exterior safety rails, and mast lookout.
