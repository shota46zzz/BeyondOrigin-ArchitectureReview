# OW-01 cave — Architecture Fix Round 1

State: **DRAFT / AI and Human Visual Review pending**. This is a development-only architecture revision. Draft v1 code and its fixed Evidence commit remain unchanged. No NBT, Gameplay, loot, spawner, or Worldgen asset is produced.

## Scope

The Minecraft review of Draft v1 found an overly symmetrical exterior mound, repetitive support posts, a regular cavern shell, and a possible reward chamber roof gap. This round keeps the original footprint and route. It changes only the cave landform, carved surface shape, sparse mining traces, and rear stone shell.

- The entrance ridge now has different east and west tapers, an off-center high shoulder, and a slightly shifted tunnel mouth.
- The chamber and gallery cross sections vary smoothly, with irregular ceiling and wall offsets rather than tiny random block noise.
- Paired timber posts are replaced with three incomplete off-axis mining remnants.
- The rear ridge maintains a stone shell over the reward chamber; the reward plinth and room position remain reserved.

## Preview and evidence

- Separate copied flat development world: `ow01-cave-fix-round1-preview2-20261018`
- Anchor: `(600000,4,600000)`
- Debug command: `/bo debug ow01_cave_fix_round1`
- Evidence target: `/bo debug architecture_review ow01_cave_fix_round1`
- Eight real Minecraft PNG views, including entrance, sides, gallery, branch, main cavern and deep reward.

The preview placement wrote 36,105 unique solid blocks. The built-in route check and out-of-bounds guard passed during placement. `compileJava` passed and all eight captured PNG SHA-256 digests match metadata. Physical player traversal, exact roof block coverage over every cell, support of every rock overhang, natural Worldgen adaptation and final NBT reproduction remain unverified.

## Decisions and limits

The mismatch between the user's “small” size label and the older individual dungeon specification remains **Human Decision Pending**. This revision keeps the existing Draft v1 footprint. The screenshot can show whether the mountain silhouette is convincing; code checks do not approve visual quality. Keep this revision separate from formal Architecture approval.
