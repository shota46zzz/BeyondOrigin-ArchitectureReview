# White Castle — Exterior Redesign (Design Draft)

Status: DESIGN_ONLY / NOT APPROVED FOR BUILD. Phase 1 Revision supersedes this file's preliminary massing table for coordinate decisions. The sole current proposal is `exterior_layout.md`, `elevation_plan.md`, `tower_roof_spec.md`, `window_facade_spec.md`, `interior_allocation.md`, `reference_comparison.md`, and `phase1_revision_sections.md` together.
Reference set: `architectures/white_castle/references/manifest.json` and its eight PNGs. `07_main_exterior_target.png` is primary; all 8 local PNGs were visually opened and their SHA-256 values matched manifest 8/8 on 2026-10-10.

## Goal
Rebuild the exterior design around the supplied white Gothic fantasy castle reference: a dramatically tall central spire, layered side towers, steep dark roofs, ornate vertical windows, and terraced approach. Do not prioritize fitting exterior to existing room dimensions. White Castle is intended to be larger than Ancient Ruins.

## Site & coordinates
- Footprint: 220 (X) × 260 (Z) blocks, local X=-110..109 and Z=-90..169 (inclusive).
- Preserve coordinate convention: anchor (500000,4,500000), X=0 central axis, +Z toward Keep, local Y=0 ground.
- Site footprint is agreed; individual buildings below are preliminary, not approved implementation coordinates.

## Superseded preliminary massing (historical only; DO NOT BUILD FROM THIS TABLE)
| Feature | Width x depth | Top Y | Center (X,Z) |
|---|---|---|---|
| Main palace / Keep | 100 x 90 | 55 | (0,105) |
| Central spire | 25 x 25 | 120 | (0,128) |
| Forward side towers | 19 x 19 | 85 | (+/-64,92) |
| Rear side towers | 19 x 19 | 95 | (+/-64,145) |
| Small corner towers | 13 x 13 | 65 | (+/-46,65) and (+/-46,145) |
| Palace wings | 35 x 80 | 48 | (+/-67,105) |
| Upper garden terrace | 140 x 35 | 18 | (0,39) |
| Main staircase | width 11, ~55 long | 18 | (0,-6) |
| Gatehouse | 60 x 25 | 32 | (0,-65) |
| Gate towers | 17 x 17 | 48 | (+/-32,-65) |
| Outer walls | 5-7 thick | 22-30 | site perimeter |

The values above were an initial brainstorming envelope. In particular, the palace roof height, rear-tower X positions and corner-turret count differ from the active Phase 1 Revision. Resolve any implementation from `exterior_layout.md` and `phase1_revision_sections.md`, never this table. Human approval is still required before a build.

## Architectural requirements
- White concrete, quartz bricks and polished diorite as main wall palette.
- Steep, dark-colored pitched roofs and Gothic spires; stagger heights to avoid a flat box silhouette.
- Standard windows: `minecraft:light_gray_stained_glass_pane`.
- Feature windows: `minecraft:light_blue_stained_glass_pane` or `minecraft:blue_stained_glass_pane`.
- Transparent windows when needed: `minecraft:glass_pane`.
- Frames: quartz bricks / quartz stairs / quartz slabs.
- Do not use `minecraft:iron_bars` as windows. Only consider iron bars in specifically approved prison or underground utility contexts.
- Tall arched windows with scale varying by building: hall ~9-13 high, upper rooms ~4-6, towers ~3-6.
- Preserve the functional concepts of Great Hall, Throne Arena, Upper Gallery, Upper Rooms, Undercroft, and width-11 main stair, while allowing replanning to suit new exterior.
- Upper spire interiors may be decorative and inaccessible.

## Workflow gates
1. Verify the eight original reference PNGs under `references/` against `manifest.json` and inspect them visually. Completed for the Phase 1 design pass; any later revision should use the same evidence set.
2. Produce exterior silhouette, massing, elevations, and overlap/bounds plan, comparing explicitly against the reference.
3. AI design review and human approval.
4. Only then create a separate Draft Build; review its exterior against the reference before interior completion.

Never modify Round 3 fixed evidence at commit `4753bdfbae33d1ab699896c70ba5d91e3898e616`. No NBT or Gameplay work is authorized.
