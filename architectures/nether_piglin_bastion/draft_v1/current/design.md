# Piglin Bastion — Architecture Draft v1

State: **DRAFT_BUILD_ONLY / AI Visual Review pending / Human Review pending**. This is a development-time preview, not a saved Structure NBT or production Worldgen asset.

## Design source and composition

- Sources: [`11_ピグリン砦.md`](11_ピグリン砦.md), `ARCHITECTURE_DESIGN.md` §13.11, and `BEYOND_ORIGIN_DESIGN_BIBLE.md` §16.2.
- Local bounds (inclusive): X -80..80, Y -12..38, Z -12..182. The flat Overworld copy uses anchor `(900000,4,900000)` for visual authoring only.
- The raid route climbs from a broken gate across lava channels into a large elevated treasure hall. Lower left and right quarters hold separate barracks/forge remnants and lead to two side vaults. An upper vault behind the hall leads down to one secret deep vault. The site has multiple tower heights, broken rooflines, and irregular volcanic ground.
- Treasure alcoves, direct treasure positions, and guard locations are architectural **reservations** marked by inert blackstone. No valuable blocks, chests, Piglin Brutes, mobs, spawners, or reward logic are placed. The Human direction forbids Ghasts here.
- The Draft creates its own fortress-city outline rather than reusing a vanilla Bastion Structure. Fixed blackstone and basalt are the authored look; natural Nether terrain integration remains a later Worldgen task.

## Preview and limits

The Plan checks bounds, the main hall floor/headroom, the secret descent, both side connection floors, and the secret focus marker. These static checks do not establish actual survival traversal, Hoglin circulation, natural terrain fit, or reward balance.

Use `/bo debug nether_piglin_bastion_draft_v1` only in a private development singleplayer flat-world copy at an empty anchor. `/bo debug architecture_review nether_piglin_bastion_draft_v1` captures five exterior and ten interior Minecraft views with metadata and PNG SHA-256. The optional `-PnetherPiglinBastionAutoPreview=<copied-world-name>` runs placement and capture after load.

Formal Architecture approval, NBT, Gameplay, Worldgen, and WBS completion remain outside this Draft.
