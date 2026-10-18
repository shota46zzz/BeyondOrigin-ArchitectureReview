# OW-04 Underground Base — Architecture Draft v1

Status: **DRAFT / VISUAL REVIEW PENDING**. No Structure NBT, gameplay entities, spawners, chests, or worldgen integration.

## Specification basis

`docs/04_地下基地.md`, `docs/ARCHITECTURE_DESIGN.md` §13.4, and `docs/GAME_DESIGN.md` define this as a **large** dungeon. The multi-dungeon request calls it medium; the finalized size remains large pending Human specification reconciliation. The draft follows the required sequence: concealed entrance → security → captured-villager hall → administration → weapons → research → storage → power → deep hangar. Villagers, guards, rewards, and devices are reserved in the space only.

## Form and route

Local coordinates relative to `(700000,4,700000)`, +Z toward the deep hangar. Bounds X -42..42, Y -31..13, Z -14..174. Low, irregular surface bunker, side walls, and signal mast indicate a hidden military complex without forming a castle. A descending central security spine reaches an upper underground level, then a second ramp reaches storage, power, and the large hangar. Offset wings create a more varied footprint than parallel rooms in a large rectangle. The hangar has a tall structural frame, overlook and central dais.

The detention wing has a broad holding space and grille. It reserves room for future persistent villagers and post-clear reuse; no villagers or state logic are placed. The research wing is reserved for Witch combat. Power and hangar reserve large objective spaces. No gameplay allocation is finalized.

## Preview and validation limits

Use `/bo debug ow04_underground_base_draft` in a **copy** of the flat development world. The draft carves below that copy's surface. Automatic capture uses `-Pow04BaseAutoPreview=<copied world name>` and the existing Architecture Review Capture. The validation checks declared bounds, key air spaces, flat source surface, and no occupied above-surface cells before placement. It does not prove walkability, AI navigation, biome-aware terrain integration, or player-base suitability. Human visual review remains required.
