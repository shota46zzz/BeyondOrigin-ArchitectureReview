# White Castle elevation and ascent plan

Status: `DESIGN_REVIEW_PENDING`. Use the half-open X/Z convention and anchor from `exterior_layout.md`. Y values are local to world anchor Y=4. Height labels below are planning surfaces or inclusive silhouette peaks; they are not yet block placement instructions.

## Axial sequence and elevation

| Segment | Local centerline Z | Walking Y | Visible cross-section from -Z |
|---|---:|---:|---|
| Gate threshold | -78..-53 | 0→2 by two approach treads | 33-high gate shell framed by 48-high gate towers. |
| Lower court | -53..-25 | 2 | Open 144-wide breathing space; flanking 22..30-high curtain segments. |
| Main stair S0 | -25..29 | 2→18 | 11-wide central climb, low planting/stone rails to either side; not a flat 55-long ramp. |
| Garden T0 | 27..61 | 18 | Broad planted terrace, balustrade and lateral outlook; axial sightline to main façade. |
| Palace threshold S1 | 55..71 | 18→26 | 15-wide short climb to palace base. |
| Great Hall / palace front | 72..105 | 26 floor, eave 50, ridge 68 | Three-depth composition: arcade at 26..38; hall windows 34..49; steep roof ridge 68. |
| Royal / throne rear | 106..155 | 30 floor, arena clear top 54 | Main spire begins above rear volume at 54, finial Y120. |

For S0, use four groups of four 1-block rises separated by 8–10-block landings within Z[-25,30). This spends 16 rises across the 55-block depth; all other columns are level treads or landings. The exact four group starts remain block-state detailing, but every 1-block rise must be a usable stair/slab arrangement, never a mandatory jump. S1 similarly uses eight 1-block rises across 17 Z columns. The garden/palace slabs omit cells owned by these stair strips; supports fill below every public tread to natural terrain at build time. The flat-world Y values are a design datum, not a terrain cut/fill estimate.

## Front elevation, seen from the gate

| Horizontal field | Silhouette height | Reading |
|---|---:|---|
| X[-104,-88) and [88,104) | 22..30 | Interrupted low curtain, not a wall hiding the palace. |
| Gate towers X[-43,-26), [26,43) | 48 | Foreground frame; each roof/finial is well below palace side towers. |
| Wing roofs X[-88,-50), [50,88) | 56 | Dark rising planes behind garden, with white buttressed façades. |
| Forward tower peaks X[-77,-58), [58,77) | 85 / 89 | First high points to either side of palace. |
| Rear tower peaks X[-42,-23), [23,42) | 93 / 95 | Distinct inner silhouettes separated by 16 X cells from forward towers; rooted in palace side bands. |
| Main palace ridge X[-50,50) | 68 | Broad horizontal counterweight below thin vertical spire. |
| Central spire X[-13,13) | **120** | Unique apex; visible from gate despite forward roofs. |

The revised forward and rear tower pairs project into four disjoint X intervals from an axial frontal view. Their Z separation (82..101 versus 126..145), different heights and roof profiles add depth. Approximate left/right oblique projections and diagrams are recorded in `phase1_revision_sections.md`; Minecraft perspective remains unverified.

## Side elevation and sections

From east or west, the foreground gate peaks at 48, outer wall at 22..30, planted upper terrace at 18, wing roofs at 56, front/rear tower peaks at 85/89 and 93/95, palace ridge at 68, then main spire at 120. The descending order toward the gate gives depth; isolated towers never form a uniform 90-high fence.

At Z≈88 (Great Hall) the central section is court Y2 → stair → garden Y18 → palace floor Y26 → clear hall 26..50 → roof to 68. At Z≈130 (arena) the central section is arena floor Y30 → clear combat volume Y30..53 → transfer deck Y54..59 → spire shell Y60..120. Side piers remain outside X[-18,17), and rear piers start at Z142, beyond the arena rectangle. Exact design cell bands are in `phase1_revision_sections.md`; the arena is not narrowed.

No block is proposed above local Y120 (world Y124). Highest corner roof is local 95; the spire therefore retains ≥25 blocks of height dominance. This is a visual hierarchy target, not a line-of-sight proof from every world terrain position.
