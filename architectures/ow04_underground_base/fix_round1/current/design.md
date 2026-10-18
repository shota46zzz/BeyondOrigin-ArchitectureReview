# OW-04 Underground Base — Architecture Fix Round 1

Status: **DRAFT / AI VISUAL RE-REVIEW PENDING**. This is an iteration of the flat-world architecture draft, not a Structure NBT or approved asset.

## Review basis

Draft v1 Evidence: `f208c40493e10b4de9538634b978ffa3e2af0858` in `shota46zzz/BeyondOrigin-ArchitectureReview`. AI Visual Review returned `NEEDS_FIX`: the surface entrance read as a flat box, interior wings lacked architectural identities, and the security spine and hangar needed more functional construction. The review did not establish physical walkability or worldgen suitability.

## Local iteration

The existing entrance → security → detention/administration → weapons/laboratory → lower ramp → power/hangar sequence and original envelope are retained. The surface bunker now has offset defensive cheeks, parapet fragments, vents, an observation slit and separate equipment pads. Detention has three cells and a guard desk; administration has a split command deck; the magazine has recessed storage bays; the laboratory has an isolation booth and work islands; power has a reactor stack and feed lines; the hangar has side service pads, cargo stacks and a suspended crane. Security bulkheads break up the spine while leaving its central route open. These are architectural draft features; no mobs, villagers, loot, spawners, machinery logic or gameplay were added.

The preview uses the copied flat world `ow04-base-fix-round1-preview2-20261019` and anchor `(710000,4,710000)`. It does not overwrite the Draft v1 preview. Use `/bo debug ow04_underground_base_fix_round1` only in a disposable world copy. `-Pow04BaseAutoPreview=<copied world name>` performs placement and 19-view capture. The original 15 views are retained, with four closeups added. The review images use a neutral daytime profile and render-state night vision for interior visibility, so they are not a lighting assessment.

## Validation and open limits

The preview placement ran the plan's declared-bounds, key-space and route-connectivity checks and placed 147,477 cells. `compileJava` and targeted `ArchitectureReviewTargetTest` / `NamedReviewViewpointTest` passed. All 19 Minecraft PNGs were captured; each SHA-256 matches `metadata.json`. Physical walking, mob navigation, terrain integration in natural biomes, and post-clear base use remain unverified. The size conflict remains: dungeon-specific design describes a large base, while the multi-dungeon brief called OW-04 medium. Human specification reconciliation is pending. Formal Human Review, NBT approval, gameplay and worldgen are not started.
