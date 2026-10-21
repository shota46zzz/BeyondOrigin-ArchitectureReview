# Nether Demon Castle — Architecture Draft v1

Status: `DRAFT_BUILD_ONLY`. Human must judge scale and any Ghast use after seeing Minecraft evidence. This is not a Structure NBT, Gameplay implementation, or Worldgen asset.

## Design source

`docs/12_魔王城.md` and `docs/ARCHITECTURE_DESIGN.md` require a very large Nether royal fortress with outer walls, towers, gate, courtyard, great hall, prison, armory, research/magic rooms, royal quarter, treasury and throne room. The Design Bible is supplementary. Boss base entity, combat, loot, spawner functions and final enemy placements remain outside this Draft. The Human permits consideration of Ghasts only for this castle and requires a final scale decision first. No Ghast or other mob is placed.

## Proposed size and layout

Local bounds X `-108..108`, Y `-12..55`, Z `-15..238` (217×254 footprint); flat copied-world anchor `(1000000,4,1000000)`. A heavy outer curtain and four corner towers establish the distant silhouette. A 19-block gate opens onto a large courtyard. The courtyard has two clear, unroofed **candidate** volumes of about 40×48 blocks with 20 blocks of air above the floor. These volumes are a scale test for possible future aerial combat, not approval to place Ghasts. The center remains a dry, 11-block processional route. A tall vaulted great hall leads to a throne hall and raised dais. The side wings house prison, armory, research, royal and treasury areas. Side passages and courtyard reserve exploration space without implementing enemies or reward containers.

The castle is intentionally larger and taller than the Nether fortress and Piglin bastion Drafts. The final dimensions, Ghast feasibility, enemy regions and boss arena adequacy are **HUMAN DECISION PENDING** after visual review. No Ghast is intended in the other Nether dungeons.

## Preview and limits

Use a safe copy of the flat preview world. Run `gradle runClient -PnetherDemonCastleAutoPreview=nether-demon-castle-draft-preview-v3-20261021 --offline`; the opt-in placement command is `/bo debug nether_demon_castle_draft_v1`. Minecraft captures named exterior, courtyard, side-room and throne views. Capture load bounds are compact, while metadata records full architecture bounds.

Flat-world placement and screenshots do not prove normal Nether terrain integration, walking, mob flight, standard lighting, NBT, Gameplay or Worldgen. Ghast projectile block protection has not been implemented.
