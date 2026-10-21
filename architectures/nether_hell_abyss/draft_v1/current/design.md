# Nether Hell Abyss — Architecture Draft v1

Status: `DRAFT_BUILD_ONLY`; Human and AI visual review pending. This is not a Structure NBT or Worldgen asset.

## Design basis

`docs/13_地獄の深淵.md` specifies a long Lv5 expedition through all Nether environments, ending in a large, quiet, circular colosseum. `docs/ARCHITECTURE_DESIGN.md` and the Design Bible supplement that intent. The arena reserves space for a future sword-focused boss but implements no boss, spawner, mob, loot, hazard mechanic, or reward. Per Human direction, Ghasts are excluded here; the Demon Castle alone may be considered separately after its size review.

## Fixed Draft layout

Local bounds X `-92..92`, Y `-24..43`, Z `-12..345`; anchor `(950000,4,950000)` in a disposable flat Overworld copy. The dry route is 9 blocks wide from Z `-10..252`. Distinct sequential scenes are lava cavern/sea, Nether Wastes with a side cave, soul basin, crimson/warped forest, basalt delta, ruins of fortress and Piglin civilization, mining remains, then the colosseum. Small structures and terrain masses shape each scene; the player can branch away from the central spine. The final arena is centered at `(0,0,295)` with radius 48. Its inner radius 43 is flat and buildable, with no placed obstacles or scripted hazards. The rim is interrupted by an 11-block entrance.

This is a flat-world shape study. Natural Nether terrain adaptation, lava safety, walking/mob routing, gameplay budget, normal lighting, and boss combat are `UNKNOWN` until later validation. The plan uses inert architectural blocks only; visible lava is environmental Draft scenery. No Ghast or other entity is placed.

## Preview and evidence

Run `gradle runClient -PnetherHellAbyssAutoPreview=nether-hell-abyss-draft-preview-v2-20261021 --offline` against a safe copy of the flat preview world. The opt-in command is `/bo debug nether_hell_abyss_draft_v1`. This places the Draft at the anchor and starts Minecraft screenshot capture. The capture load region is deliberately smaller than the full architecture bounds because a 358-block-long site exceeds normal render distance at some cameras. Metadata retains the full architecture bounds; named split aerials and scene views cover both halves. Screenshots alone cannot verify continuous walking or Worldgen.
