# OW-03 Airship — Fix Round 1 Draft

State: `DRAFT_BUILD_ONLY`; AI visual re-review and Human review pending. No NBT, gameplay, functional spawner, chest, boss, or worldgen integration.

Draft v1 visual review identified a flat gas envelope and hull, a sparse deck, weak helm and reward room identity, sparse lower-deck use cues, and an indistinct Phantom exterior reservation. Fix Round 1 reshapes the gas envelope, adds supported suspension stays and hull ribs, adds deck stations and a framed starboard reservation platform, gives the crew and cargo areas use cues, strengthens the engine structural rhythm around the three inactive positions, and broadens the helm reward room with an empty stone plinth. The main deck combat lane and two broad lower-deck stairs remain.

This is still a fixed high-altitude flat-world Architecture Draft. The stern gangway's natural-terrain landing, physical walking, Pillager/Phantom paths, ordinary lighting, reward behavior, NBT, and Worldgen remain outside the visual review.

Validation: `compileJava` and targeted `ArchitectureReviewTargetTest` PASS. The development-client plan validation and placement PASS with 28,404 cells at `(640000,100,640000)` in `ow03-airship-fix-round1-preview3-20261020`, an isolated copy of the flat development world. Seventeen Minecraft PNGs were captured and 17/17 SHA-256 values match `metadata.json`. The widened gas bag was raised so the lookout ladder hatch remains clear.
