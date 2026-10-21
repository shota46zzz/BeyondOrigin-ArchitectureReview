# Nether Lava Cave — Architecture Draft v1

State: **DRAFT_BUILD_ONLY / AI Visual Review pending / Human Review pending**. The code is a development-time preview; it is not a saved Structure NBT or Worldgen asset.

## Design source and route

- Source: [`09_溶岩洞窟.md`](09_溶岩洞窟.md), `ARCHITECTURE_DESIGN.md` §13.9, `BEYOND_ORIGIN_DESIGN_BIBLE.md` §16.2. The latest Human direction forbids Ghasts here; only 魔王城 may use them.
- Local bounds (inclusive): X -42..42, Y -36..28, Z -8..104. Flat preview anchor `(760000,4,760000)` is a disposable Overworld copy used only for visual authoring. The Nether terrain and Worldgen interface remain untested.
- Main route: cave mouth → huge vertical cavern → descending 7-wide stone path → high bridge over a lava lake → deep reward chamber. Slopes change by at most one block per Z row; stair treads mark the drops for the return climb.
- Separate east side gallery and overlook joins the main route near the upper cavern and the lower lake approach. The upper connector uses a three-wide ramp; the lower connector is level.
- Lava surface is local Y -27, with a lined volcanic basin, islands, and supported bridge. The reward plinth is inert: no chest, item, spawner, or mob behavior is implemented.
- Fixed blackstone/basalt/netherrack are the authored cave identity. Adaptation to surrounding Nether terrain is a later Worldgen design task; no sandstone is authored into the cave.

## Draft validation and review

The Plan checks bounds, continuity of the central floor, two-block headroom on the central route, no height jump greater than one block between adjacent route rows, bridge height above lava, and the reward plinth. This is static geometry validation, not a guarantee of real player movement or natural terrain safety.

The debug command `/bo debug nether_lava_cave_draft_v1` accepts only private development singleplayer on the copied flat world at an empty anchor. `/bo debug architecture_review nether_lava_cave_draft_v1` captures five outside and eight inside Minecraft views with metadata and PNG SHA-256. The optional `-PnetherLavaCaveAutoPreview=<copied-world-name>` triggers placement and capture after world load.

No final Architecture approval, NBT, Gameplay, boss, Worldgen, or WBS status is inferred from this Draft. Human review is required after complete Minecraft evidence.
