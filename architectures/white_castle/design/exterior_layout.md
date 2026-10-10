# White Castle exterior layout — proposal for AI Design Review

Status: `DESIGN_REVIEW_PENDING`; coordinates are design cells, not placed blocks. This plan supersedes the **preliminary building envelopes only** in `exterior_spec.md`. It does not alter the Round 3 draft or evidence.

## Datum and site

- Local X east/right, local +Z from gate toward Keep. Anchor `(500000,4,500000)`; local Y=0 is flat-world ground datum. A local cell `(x,y,z)` maps to world `(500000+x,4+y,500000+z)` for the unrotated draft.
- All tabulated bounds are half-open: `[min,max)`. Site `X[-110,110) × Z[-90,170)` = **220 × 260**. Highest occupied cell may be local Y=120 (main finial); no design block above it. Site boundary remains a planning limit, not a confirmed worldgen envelope.
- The composition is axial but not a row of identical blocks: the foreground gate and flanking walls frame a broad court; an 11-wide climb reaches planted terraces; palace masses step backward and upward; four unequal-height roofs/towers flank a single 120-high main spire.

| ID / feature | X | Z | Y / surface or top | Purpose and ownership |
|---|---:|---:|---:|---|
| G0 gatehouse | [-30,30) | [-78,-53) | shell [0,33) | Center passage X[-6,6); gate façade and portcullis silhouette. |
| GT-W / GT-E gate towers | [-43,-26) / [26,43) | [-77,-60) | top 48 | Intentionally overlap G0 by four X cells and its north/south envelope; gate owns inner wall, tower owns outer pier above it. |
| C0 lower court | [-72,72) | [-53,-10) | walking Y=2 | Arrival and tower-route branches; dry paved axis X[-8,9). |
| S0 processional stair | [-6,5) | [-25,30) | walking Y=2→18 | Width **11**; tiered landings, continuous central route; intersects C0 at its south end and terrace T0 at its north end. |
| T0 garden terrace | [-72,72) | [27,62) | walking Y=18 | Main planted upper court; stair/terrace overlap Z27..29 is an intentional shared landing. |
| S1 palace threshold stair | [-7,8) | [55,72) | walking Y=18→26 | Width 15; overlaps garden Z55..61 and palace forecourt Z65..71; only this connector changes elevation. |
| P0 main palace | [-50,50) | [65,155) | base 26, eave 50, roof ridge 68 | 100×90 shell, front great-hall volume and rear throne volume; roof is deliberately taller than preliminary top 55. |
| W-W / W-E palace wings | [-88,-50) / [50,88) | [71,145) | base 24, eave 40, ridge 56 | 38×74 each. Their inner faces meet P0 exactly at X=-50 and X=50; crossing via authored 5-wide openings. |
| FT-W / FT-E forward towers | [-77,-58) / [58,77) | [82,101) | base 24, top 85 / 89 | 19×19. Embedded in wing footprints with tower ownership at shared cells, not duplicate construction. |
| RT-W / RT-E rear towers | [-77,-58) / [58,77) | [126,145) | base 24, top 93 / 95 | 19×19; unequal heights reinforce depth while remaining below spire. |
| CS main tower/spire | [-13,13) | [125,151) | base 54, finial cell Y=120 | 26×26 tower volume over the rear palace. Transfer/buttress loads go to outer arena walls; its ground-level footprint is **not** a solid arena obstruction. |
| CT-W / CT-E front corner turrets | [-52,-39) / [39,52) | [59,72) | top 65 | 13×13; T0/P0 transition, thin in silhouette. |
| CT-RW / CT-RE rear corner turrets | [-52,-39) / [39,52) | [143,156) | top 64 / 67 | Rear palace termination; 2-cell site margin to rear curtain. |
| OW-W / OW-E curtain lines | [-104,-98) / [98,104) | [-56,123) | top 22..30 | 6-thick perimeter line; project inward at north ends toward wings, not a rigid closed rectangle. |
| OW-R rear broken line | [-98,98) | [158,164) | top 18..24 | Broken at X[-15,16) and at two side view slots. Avoids an opaque wall behind the palace. |

All primary masses stay inside the site: extreme designed X is ±104 within `[-110,110)`; extreme Z is -78..164 within `[-90,170)`. The spire finial is the only Y=120 point; no tower, roof dormer or wall exceeds it. The foreground approach outside Z=-90 is reserved for later terrain survey, not secretly included in the 260-block site.

## Joins and deliberate intersections

| Join | Design rule | Passage / view condition |
|---|---|---|
| Gatehouse ↔ lower court | G0 rear threshold at Z=-53, court begins Z=-53. Gate owns lintel; C0 owns the walking floor. | 12-wide axial opening; no one-block lip. |
| Gate towers ↔ G0 | Tower outer piers replace G0 wall only in the four-cell shared strip. | Defensible upper walk, still subordinate to P0. |
| Court ↔ S0 ↔ garden | S0 is the sole owner of treads in its 11-wide strip. C0/T0 omit their generic paving there. | No mandatory jump; detailed tread/landing schedule in `elevation_plan.md`. |
| Garden ↔ palace threshold | S1 is sole tread owner; T0/P0 omit generic floor within it. | Garden's side walk remains open beside the stair. |
| Wings ↔ P0 | Faces meet at X=±50; no air gap. Five-wide doorways proposed around Z84..89 and Z120..125; actual room-side stairs are pending. | Side loops return to main palace, without forcing a tower climb into the axial route. |
| Towers ↔ wings | Tower volumes are embedded, not freestanding collision-free boxes. Each tower owns its 19×19 footprint; wing roof and floor are clipped to tower shell. | Stairs live within towers; final walkability is Human/Minecraft review, not assumed here. |
| CS ↔ throne volume | Tower begins at Y54, above the arena ceiling line; its supporting piers are outside the 35×28 combat clearance. | View from throne to spire base is possible; support and lighting remain engineering review items. |
| Rear wall ↔ palace | 3-block minimum visible separation between P0 rear Z155 and rear line Z158. Broken center line avoids a dead-end vista. | No claimed playable rear exit yet. |

## Plan view (symbolic, not to scale)

```text
                    +Z / KEEP / rear
   ┌─ broken rear curtain ── gap ── broken curtain ─┐
   │  rear tower   ┌── MAIN SPIRE ──┐  rear tower   │
   │  west wing ┌──┤ palace / throne ├──┐ east wing │
   │  front tower│  │  GREAT HALL    │  │front tower │
   │             └──┴── S1 entrance ┴──┘            │
   │               GARDEN TERRACE                   │
   │                 11-WIDE S0                      │
   │               LOWER COURT                      │
   └─ west wall ─── GATEHOUSE ───── east wall ──────┘
                   -Z / approach
```

The older `WHITE_CASTLE_LAYOUT_V2_PROPOSED.md` and Round 3 authoring dimensions describe an earlier compact draft. They are not construction authority for this exterior redesign. Required gameplay concepts remain allocated in `interior_allocation.md`; final path and terrain need later approval.
