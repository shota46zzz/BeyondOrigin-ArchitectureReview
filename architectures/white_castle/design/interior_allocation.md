# White Castle interior allocation inside the exterior massing

Status: `DESIGN_REVIEW_PENDING`. The exterior envelopes from `exterior_layout.md` were selected first. Room locations below test whether the required dungeon can fit; they are not a gameplay implementation, approved route or NBT.

## Proposed functional volumes

| Function | Host shell and candidate clear envelope (half-open) | Floor / clear top Y | Access concept |
|---|---|---:|---|
| Gate passage and defense | G0 X[-6,6), Z[-78,-53) | 0→2 / 7 | Gate to lower court; upper passage in gate shell and side towers. |
| Lower courtyard | C0 X[-72,72), Z[-53,-10), excluding S0 tread strip | 2 / open sky | Central approach plus east/west exploration branches. |
| East ranged tower loop | FT-E and adjacent east wing, X[50,88), Z[71,108) | 24 / tower upper landings TBD | Optional encounter loop with return toward hall; exact enemy specification remains in dungeon design. |
| West melee tower loop | FT-W and west wing X[-88,-50), Z[71,108) | 24 / upper landings TBD | Parallel optional loop, architecturally distinct from east. |
| Great Hall | P0 X[-38,38), Z[72,105) | 26 / 49 | 76×33 gross clear rectangle before column islands; 7-wide processional axis X[-3,4) reserved. |
| Upper Gallery | P0 perimeter around Hall, X[-45,-35) and [35,45), Z[76,104) | 40 / 49 | Overlooks Hall without covering the central volume; branch stair design pending. |
| Royal Quarters / Upper Rooms | Rear P0 side bands X[-47,-29), [29,47), Z[108,142) and upper side rooms | 30 / 48 | Elevated side route around arena. Use exterior lancets at façade bands. |
| Antechamber | P0 X[-24,24), Z[105,112) | 30 / 40 | Readable transition into throne zone. |
| Throne Arena / boss room | P0 X[-28,28), Z[112,145) | 30 / 54 | **Minimum clear fight rectangle X[-18,17), Z[114,142)** = 35×28; no main tower pier, permanent obstruction or low beam inside it. |
| Treasury | East or west wing rear, candidate X[54,84), Z[110,134) | 24 / 39 | High-status Evoker-related treasure room per dungeon design; final side and enemy placement not decided. |
| Undercroft / service area | Beneath rear palace outside boss footing, candidate X[-24,24), Z[72,103) | -8 / 24 | Concept retained from earlier draft; descent, foundations and world terrain are unresolved. No pit is authored here. |

The existing Round 3 Great Hall, Throne Arena, Upper Gallery, Upper Rooms and Undercroft are **functional references**, not voxel geometry to be transplanted unchanged. Their earlier compact coordinates conflict with the new 220×260 silhouette. No current Human-reviewed White Castle NBT is being regenerated. The revised arena clear rectangle is larger than the earlier 35×28 planning minimum, while exact boss playability remains untested.

## Route, joins and protected clearances

Proposed main route: gate → lower court → 11-wide main stair → upper garden → 15-wide palace threshold → Great Hall → royal/antechamber threshold → Throne Arena. The east and west tower/wing routes are meaningful side loops reconnecting to Great Hall or antechamber. `docs/05_白い城.md` lists east then west tower before Great Hall; the later Human-approved optional-tower interpretation documented in `WHITE_CASTLE_LAYOUT_V2_PROPOSED.md` differs. **This remains a specification interpretation conflict for Human**, and the new design does not silently declare the towers optional in final gameplay.

Wing-to-palace doors meet at X=±50 around Z84..89 and Z120..125; their exact Y levels, corridor widths and in-game walking continuity must be surveyed during draft construction. Tower stairs stay inside 19×19 envelopes with at least 2-wide intended passage, but their treads/headroom have not been measured. The spire plinth begins at Y54, just above arena clearance; its support must follow the perimeter outside X[-18,17), Z[114,142). A failed structural or visual review requires relocating supports or revising the overlap, not shrinking the fight space without approval.

The design leaves gameplay quantities unchanged: White Castle ordinary spawner and chest targets, enemies, boss values and reward rules remain controlled by `docs/05_白い城.md`, `docs/GAME_DESIGN.md` and later systems. No spawner, chest, block, NBT or game rule is created by this document.
