# OW-08 最深部 — Architecture Draft v1

State: **DRAFT / Visual Review pending**. This code is a development authoring draft. It is not a Structure NBT, approved asset, runtime worldgen asset, encounter, reward, or Gameplay implementation.

## Design source

- `docs/08_最深部ダンジョン.md`
- `docs/ARCHITECTURE_DESIGN.md` §13.8 and its Lv5 footprint guidance
- `docs/BEYOND_ORIGIN_DESIGN_BIBLE.md` §16.1

The specified sequence remains: surface entrance → buried temple → seal corridor → ancient arsenal → deep cave → collapsed underground city → World Core → boss. The draft is local X -132..132, Y -48..19, Z -12..393 (inclusive); its 265×406 horizontal outer envelope reaches the Lv5 scale. The actually carved playable volume is intentionally irregular. Its outermost east/west galleries make the broad footprint meaningful, but they need visual review and walking checks.

## Authored spatial layout

| Place | Local X | Floor Y | Z | Architectural identity |
|---|---:|---:|---:|---|
| Surface entrance | -18..18 | 0 | -12..24 | broken stone approach, standing crown and descent |
| Buried temple | -33..33 | -12 | 30..82 | four column ranks, axial processional floor |
| Seal corridor | -12..12 | -16 | 83..132 | repeating seal ribs and distinct stone bands |
| Ancient arsenal | 18..69 | -20 | 103..154 | vaulted weapons hall and empty display plinths |
| Deep cave | -56..56 | around -27 | 148..217 | irregular tuff vault, rooted outcrops, supported floor, shelves, bridge |
| Collapsed city | -90..90 | -39 | 211..300 | irregular excavated vault, plaza, civic ruins, roads, supported bridges, drainage, towers |
| Lateral galleries | -131..-96, 96..131 | -40 | 236..297 | west and east edge exploration loops |
| World Core | -39..39 | -42 | 301..340 | nested stone rings, core obelisks |
| Boss arena | -42..42 | -43 | 341..393 | open 75×42 combat floor, outer pillars and dais |

The city is formed as an excavated irregular vault; its architectural landmarks and roads are placed into this void. Civic structures have different sizes, heights and damaged roof states. The tunnel from arsenal joins the cave before the city; a second cave ledge provides lateral exploration. The drainage cut is bridged by three street crossings, and each side gallery has its own connection. All reward positions are empty reserved architecture; no chest, spawner, mob or boss behavior is placed.

## Draft placement and capture

Use only a **disposable copy** of the flat development world. At a remote blank anchor whose surface is Y=4, run:

```
/bo debug deepest_draft <anchorX> 4 <anchorZ>
/bo debug architecture_review ow08_deepest_draft_v1
```

The command only works in a private development singleplayer Overworld and requires operator permissions. It applies a large excavation and will replace blocks inside its coordinate envelope. It should not be used in an existing played world. The integrated screenshot target contains five exterior views of the surface marker and 15 named interior/close views from the temple through the boss arena. The full architecture bounds are included in capture metadata. The server command reports the number of block writes; repeated writes to the same cell count repeatedly.

## Visual review history

Fix Round 1 AI Re-Review viewed 18 of 19 Minecraft PNGs and returned `NEEDS_FIX`: the boss arena, Core, and identity of temple/corridor/arsenal were improved, while the cavern wall remained too concentric and the city and bridge needed closer evidence. Fix Round 2 changes the cave and city vault shapes, adds wall-rooted rock volumes and a supported cave floor, adds a city belfry, and includes a low bridge-support camera. The city envelope starts after the cave vista so it cannot create a flat wall across the cave. Fix Round 2 was captured in a disposable flat-world copy at `(730000,4,730000)` with 20 PNGs and remains **AI/Human visual review pending**.

No formal NBT is produced. The captured PNGs and metadata must be inspected against the current build before GitHub publication.

## Checks and limits

`DeepestDraftLayout.validate()` rejects missing stages, out-of-range areas, large axial gaps and excessive adjacent stage elevation changes. `DeepestDraftPlan` rejects every attempted write outside its declared 3D envelope and checks vertical world limits at placement time. Architecture intentionally contains no `GHAST`, mobs, spawners or vaults. World Core illumination is visual architecture only.

Still unverified: physical walking route and headroom at every transition, support under every bridge, structural silhouette in Minecraft, complete absence of floating details, player route length/1–2 hour pacing, actual Ravager movement volume, lighting balance, natural worldgen terrain integration, NBT save/reload, multiplayer. A draft screenshot does not resolve these points. Human and AI Visual Review must precede any asset approval.

## Specification conflicts

No OW-08 source conflict was found. The user's “特大” wording and the finalized “Lv5専用 / 250–400m / 1–2時間” guidance both require a much larger scope than ordinary large dungeons. This draft follows the explicit Lv5 route and keeps enemy/reward figures as future design requirements without implementing Gameplay.
