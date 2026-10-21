# Nether Fortress — Architecture Draft v1

State: **DRAFT_BUILD_ONLY / AI Visual Review pending / Human Review pending**. This is a development-time layout and Minecraft preview. No Structure NBT or production Worldgen asset is created.

## Sources and composition

- Sources: [`10_冥府要塞.md`](10_冥府要塞.md), `ARCHITECTURE_DESIGN.md` §13.10, and `BEYOND_ORIGIN_DESIGN_BIBLE.md` §16.2.
- Local bounds (inclusive): X -82..82, Y -9..38, Z -12..178. The safe flat-world copy uses anchor `(850000,4,850000)` in the Overworld for visual authoring only.
- Central composition: a fortified gate and lava-side causeway lead to a round open hub. The hub has a west defensive wing for the Knight, an east raised open court for the flying Mage, and a separate guarded bridge to a final treasure hall. Both boss areas and the final seals are inert architectural markers.
- The west hall is heavy and roofed, with a broad readable arena. The east route climbs four blocks into an open court with higher pillars and interrupted arches. Different roof and tower heights create the fortress-city silhouette without copying a vanilla Nether Fortress.
- Detached piers, bridge supports, lava channels, and an irregular volcanic apron break the perimeter into several masses. They are fixed authoring materials for the Draft; fitting natural Nether terrain is a later Worldgen task.

## Constraints and verification

- The Human direction permits Ghasts only as a possible Demon Castle decision. This Draft authors **no Ghast** and no other mob, boss behavior, ordinary spawner, loot chest, or treasure block.
- The Plan validates the complete central route's floor and two-block headroom, both branch floors, and the architectural boss/reward markers. These static checks do not establish survival traversal, boss mobility, or natural terrain safety.
- The opt-in `/bo debug nether_fortress_draft_v1` command places the Draft only in a private development singleplayer flat-world copy at the empty anchor. `/bo debug architecture_review nether_fortress_draft_v1` captures five exterior and ten interior Minecraft views with PNG SHA-256 metadata. `-PnetherFortressAutoPreview=<copied-world-name>` automates placement and capture after world load.

Formal Architecture approval, NBT, Gameplay, boss AI, Worldgen, and WBS completion all remain outside this Draft.
