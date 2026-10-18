# OW-04 Underground Base — Architecture Fix Round 4

Status: **DRAFT / AI VISUAL RE-REVIEW PENDING**. No approved Structure NBT, gameplay, or worldgen integration.

## Review basis

The [Fix Round 3 AI Visual Re-Review](https://chatgpt.com/c/6ad5594e-664c-83ee-88ff-95fe65277c9c) inspected 26/26 Minecraft PNGs from Evidence commit `89b0098b688b70afc75f8e5e27e4770d93f3b2bf` and returned `NEEDS_FIX`. R05 reactor readability was resolved, while R01 remained MEDIUM because the surface entrance still had a predominantly horizontal silhouette in front and distant views. R02/R03/R04/N01 and the detention, administration and hangar spaces showed no visual regression. The reviewer requested a stronger central roof-height difference and segmentation of the dark entrance band within the existing bounds.

## Local draft changes

- The forward caps of the unequal entrance wings were lowered, while their rear roofs and vents remain.
- A stepped central canopy now reaches the existing Y=13 upper bound. Offset stone ribs break the continuous dark front band.
- The 15-wide opening, entrance axis, descending route and site bounds remain unchanged.
- The existing 26 review views remain. `surface_profile` provides an additional distant side perspective. The `entrance` camera is farther back so the complete roof profile is visible.
- No further changes were made to the reactor, interior wings, lower ramp or hangar.

## Preview and checks

Final disposable preview: `run/saves/ow04-base-fix-round4-preview2-20261019`, anchor `(710000,4,710000)`. Placement completed with **149,008 block cells** and passed the plan's bounds, key-space, route and weapons-threshold checks. Minecraft captured **27/27 PNGs** in `build/architecture-review/ow04_underground_base_fix_round4`; every PNG SHA-256 matches `metadata.json`. `compileJava` and targeted `ArchitectureReviewTargetTest` / `NamedReviewViewpointTest` passed.

The screenshots use an interior visibility aid and do not establish normal lighting. Physical walking, mob navigation, natural terrain integration, villager containment, NBT, gameplay and worldgen remain unverified. The dungeon-specific large-scale design versus the multi-dungeon medium-scale request remains Human Decision Pending. Human Review and formal asset approval have not occurred.
