# OW-07 Tower — Architecture Draft v1

State: `DRAFT_BUILD_ONLY`; Minecraft visual review and player traversal pending. This is an authoring draft, not a WBS status or approved Structure NBT.

## Source and architectural intent

`docs/07_タワー.md`, `docs/ARCHITECTURE_DESIGN.md`, and `docs/BEYOND_ORIGIN_DESIGN_BIBLE.md` describe a medium, approximately five-floor, repeatable combat tower without a boss. The tower has Trial Spawner combat spaces, normal/ominous Vault locations, varied rooms and balconies, and a top floor spacious enough to consider one Ravager. OW-07 contains no Ghast or Evoker. The player request authorizes Architecture Draft only, so every gameplay object here is a spatial reservation.

The octagonal exterior narrows from radius 20 at the gate to radius 16 at the crown. Its dark deepslate plinth, tuff-brick body, polished tuff floors, chiseled bands, window slots, projecting buttresses, and four raised crown finials make the five levels legible from outside. The roof is deliberately open over the upper arena. The draft has a five-block-wide south entry and an approach aligned with the vertical stair core. It is not a row of boxes hidden by an outer wall.

## Coordinates and progression

- Architecture ID: `overworld/ow07_tower/draft_v1`; review target: `ow07_tower_draft_v1`.
- Local bounds: X `[-22,23)`, Y `[0,43)`, Z `[-25,23)`; south approach is negative Z.
- Independent flat-preview anchor: `(670000,4,670000)` in a disposable copied world.
- Floor 1 at Y1: gate, orientation hall, side chambers.
- Floor 2 at Y8: ring gallery, four Trial Spawner candidate bays at X/Z ±7.
- Floor 3 at Y15: split gallery and four Vault candidate bays at X ±12, Z ±9. Normal/ominous assignment remains open.
- Floor 4 at Y22: stepped lookout platforms and two Trial Spawner candidate bays at X ±7, Z7.
- Floor 5 at Y29: open upper arena, clear central 17×17 and wider usable perimeter. The crown reaches Y42; a future single Ravager has room to maneuver. No boss arena or boss behavior is implied.
- Four three-block-wide stair flights occupy X10..12, Z-10..-4. Each ascends seven blocks, has solid support and a corresponding opening in the next floor. The path to each flight enters from the floor; the last stair meets the upper landing at Z-3. This geometry must still be checked by walking in Minecraft.
- Deliberate vertical exploration: lower side chambers, ring gallery, split central step and opposed side bays, upper lookouts, open-air arena. No hidden room or shortcut is finalized at this Draft stage.

## Review and limits

- Development placement: `/bo debug ow07_tower_draft_v1`, only in a singleplayer flat copy with the fixed anchor unoccupied.
- Evidence capture: `/bo debug architecture_review ow07_tower_draft_v1`. Views cover all four exterior directions, upper silhouette, gate, each combat floor, a staircase and the upper arena.
- Optional auto-preview: `runClient -Pow07TowerAutoPreview=<copied-world-name>`; use only while no other client/evidence capture is active.
- The generator enforces local bounds, entrance opening, four complete three-wide stair runs with two-block headroom, and a clear top combat center. `compileJava` is the minimum pre-preview validation.
- No actual Spawner, Trial Spawner, Vault, chest, mob, loot, boss, NBT export, or Worldgen integration. Natural-world ground fitting, enemy pathing, actual movement, line of sight, lighting and visual quality remain unverified until Minecraft review.

The standalone Draft does not read or alter Ancient Ruins, White Castle, or any approved NBT.
