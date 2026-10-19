# OW-04 Underground Base — Architecture Fix Round 5

Status: **DRAFT / AI VISUAL RE-REVIEW PENDING**. No approved Structure NBT, gameplay, or worldgen integration.

## Review basis

The [Fix Round 4 AI Visual Re-Review](https://chatgpt.com/c/6ad55cad-bb3c-83ee-90a8-b6166fef8050) inspected 27/27 Minecraft PNGs from Evidence commit `dba09ef1da69197ee1e6336647b22b8808a09cf9` and returned `NEEDS_FIX`. R01 remained MEDIUM: the near entrance improved, but the distant oblique and side views still read as a long low roofline. R02-R05 and N01 were resolved with no visible regression. The reviewer requested a roof-height change across the surface building, not another portal-only accent.

## Local draft changes

- The entrance's raised mass now extends over the existing roof behind the facade; its upper tier reaches the established Y=13 bound and stops before the central vent.
- Staggered short parapets and exterior buttresses segment both side silhouettes without enlarging the established overall bounds.
- The 15-wide entrance opening, descending route, interior rooms, lower ramp, reactor, hangar and existing underground footprint remain unchanged.
- The 27 Fix Round 4 review cameras remain unchanged for direct visual comparison.

## Preview and checks

Disposable preview: `run/saves/ow04-base-fix-round5-preview-20261019`, anchor `(710000,4,710000)`. Placement completed with **149,782 block cells** and passed the plan's bounds, key-space, route and weapons-threshold checks. Minecraft captured **27/27 PNGs** in `build/architecture-review/ow04_underground_base_fix_round5`; every PNG SHA-256 matches `metadata.json`. `compileJava` and targeted `ArchitectureReviewTargetTest` / `NamedReviewViewpointTest` passed.

The screenshots use an interior visibility aid and do not establish normal lighting. Physical walking, mob navigation, natural terrain integration, villager containment, NBT, gameplay and worldgen remain unverified. The dungeon-specific large-scale design versus the multi-dungeon medium-scale request remains Human Decision Pending. Human Review and formal asset approval have not occurred.
