# White Castle — Exterior Redesign (Design Draft)

Status: DESIGN_ONLY / NOT APPROVED FOR BUILD.
Reference image: `architectures/white_castle/references/exterior_target.png` (PENDING UPLOAD; do not claim image inspected until present).

## Goal
Rebuild the exterior design around the supplied white Gothic fantasy castle reference: a dramatically tall central spire, layered side towers, steep dark roofs, ornate vertical windows, and terraced approach. Do not prioritize fitting exterior to existing room dimensions. White Castle is intended to be larger than Ancient Ruins.

## Site & coordinates
- Footprint: 220 (X) × 260 (Z) blocks, local X=-110..109 and Z=-90..169 (inclusive).
- Preserve coordinate convention: anchor (500000,4,500000), X=0 central axis, +Z toward Keep, local Y=0 ground.
- Site footprint is agreed; individual buildings below are preliminary, not approved implementation coordinates.

## Preliminary massing (relative heights above ground, roof included)
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

Resolve overlap, geometry, and exact local bounds in design review before any build.

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
1. Place the original reference PNG into references and verify it is readable by Codex.
2. Produce exterior silhouette, massing, elevations, and overlap/bounds plan, comparing explicitly against the reference.
3. AI design review and human approval.
4. Only then create a separate Draft Build; review its exterior against the reference before interior completion.

Never modify Round 3 fixed evidence at commit `4753bdfbae33d1ab699896c70ba5d91e3898e616`. No NBT or Gameplay work is authorized.
