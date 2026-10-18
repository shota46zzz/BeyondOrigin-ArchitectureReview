# OW-01 Cave — Architecture Draft v1

State: `DRAFT_BUILD_ONLY`; visual review pending. This document records the draft design, not WBS status or Structure NBT approval.

## Specification basis and open conflict

`docs/01_洞窟.md`, `docs/GAME_DESIGN.md`, and `docs/ARCHITECTURE_DESIGN.md` define a **medium** cave, with a 60–100 block effective exploration area. The multi-dungeon production request called OW-01 **small**. The draft follows the existing dungeon-specific medium specification pending a Human decision on the scale conflict.

## Shape and circulation

- Architecture ID: `overworld/ow01_cave/draft_v1` (`ow01_cave_draft_v1` capture target).
- Local bounds: X `[-32,33)`, Y `[0,26)`, Z `[-4,90)`; +Z moves into the hill.
- Flat preview anchor: `(600000,4,600000)` in copied world `ow01-cave-draft-v1-evidence-20261018`.
- An irregular stone ridge encloses an entrance gallery, old mining traces, two side explorations, a main cavern, and a fixed deep reward chamber. The gallery and rooms are carved from the landform; they are not boxed rooms behind one facade.
- The main path is entrance Z0 → first gallery Z16–27 → main cavern Z37–55 → deep route Z66–78 → reward plinth Z79–81. The western branch loops back to the cavern; the eastern branch is a small exploration pocket.
- The stone-brick plinth reserves a later reward location. There is no functional chest, spawner, loot, boss, or Worldgen integration.

## Preview and validation

- Development-only placement command: `/bo debug ow01_cave_draft_v1`. This uses a fixed anchor and refuses occupied/nonflat preview cells.
- Capture command after placement: `/bo debug architecture_review ow01_cave_draft_v1`.
- `OverworldCaveDraftPlan.create()` validates its bounds while placing blocks and checks a continuous excavated 3D air path from the entrance to the deep chamber. This does **not** prove player walking or safe floor transitions.
- Minecraft 26.2 / NeoForge development client placed 34,830 blocks and captured all 8/8 1280×720 views. `compileJava` passed. The copied preview world saved cleanly.
- The exterior front, both sides and oblique image, plus gallery, branch, cavern and reward-room images were inspected. Small daylight openings remain in the cavern/reward roof as draft cave collapse features; their final visual quality needs review.
- Unknown: real terrain integration, natural-cave fitting, Minecraft walking, mob line of sight, lighting, and runtime Structure asset validation. The flat preview is only an authoring environment.

No approved Ancient Ruins, White Castle, or other saved NBT was modified.
