# White Castle window and façade specification

Status: `DESIGN_REVIEW_PENDING`. This refines `block_palette.md`; it does not change game blocks.

## Palette and feature placement

| Element | Candidate vanilla block palette | Use |
|---|---|---|
| Main white wall field | white concrete with quartz bricks and limited polished diorite | Broad clean white planes, visible between window bays. Avoid uniform quartz texture over every surface. |
| Structural rib / window frame | quartz bricks, quartz stairs, quartz slabs, quartz pillar where direction fits | 2–3-cell-deep buttress at meaningful span breaks, corbel-supported cornice, pointed arch. |
| Ordinary glazing | `minecraft:light_gray_stained_glass_pane` | Most hall, wing and tower openings; pane is explicit, not full glass blocks. |
| Feature glazing | `minecraft:light_blue_stained_glass_pane`, sparse `minecraft:blue_stained_glass_pane` | Central palace window, throne/treasury accent, selected upper room. Saturated blue is a focal accent, not every bay. |
| Clear glazing | `minecraft:glass_pane` | Limited outlooks and tower observation slits where colored glass would obscure play. |
| Roof field | provisional polished deepslate / deepslate tile stairs, slabs and blocks | Dark roof contrast, pending material approval in `tower_roof_spec.md`. |

`minecraft:iron_bars` are prohibited in normal windows. No prison-window exception is assumed for this design.

## Window schedule

| Façade | Candidate opening geometry | Rhythm / sightline |
|---|---|---|
| Great Hall front and side X≈±50, Z72..104 | 5–7-wide, 11–13-high pointed arch openings; glass pane begins above a 3-high plinth. | Three dominant bays on the approach face, 4–5 side bays per side, separated by real buttresses. Center front bay is blue; lateral bays gray. |
| Throne façade and rear Z110..155 | 5–7-wide, 10–12-high arches above arena sightline; near throne a single larger feature composition. | Break regular spacing near the main spire and boss stage. Do not let glass occupy load-bearing tower feet. |
| Palace wings X≈±88 / ±50, Z71..145 | 3–5-wide, 5–7-high paired lancets | Mostly light gray. Place paired blue accent only at special room ends. Avoid perfect mirrored repetition between wings. |
| Tower shafts | 2–3-wide, 3–6-high openings, stacked with long solid sections | Keep stair headroom and landings; glass does not replace the tower's structural corners. |
| Upper Gallery / upper rooms | 2–4-wide, 4–6-high | Aim outward and across garden; parapets remain low enough for views but safe for player movement. |

## Gothic detail rule

At each major bay, first establish a readable pointed arch with stair/slab stepped shoulders, then add 1–2-block white recessed frame, then set panes back by one cell. A 2–3-cell-deep buttress lands at wall pier rather than crossing windows. A horizontal cornice at eave level binds the building masses, but wing cornices terminate cleanly at the embedded tower wall. Rose-window reference 02 is a **motif**: one large blue tracery window on the central façade is enough; copying the full enormous circular pattern would compete with the 120-high spire and may exceed vanilla block-scale legibility. Reference 03's dark interior reinforces tall side-light openings and spaced pillars; it is not permission to convert the white exterior into a dark stone hall.

Window positions are **candidate design bays**, not guaranteed unobstructed openings. In build planning, test each against wall thickness, upper floor slab, roof slope, tower stair and arena boundary. If a bay conflicts, shift or omit the bay before cutting a structural support. Light transmission and mob-spawn impact are later Lighting/Gameplay decisions.
