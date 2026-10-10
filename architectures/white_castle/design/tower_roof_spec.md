# White Castle tower, spire and roof specification

Status: `DESIGN_REVIEW_PENDING`. All coordinates and joins refer to `exterior_layout.md`.

## Roof hierarchy

| Roof / tower | Footprint | Eave → peak Y | Proposed geometry |
|---|---|---:|---|
| Main palace nave | X[-50,50), Z[65,110) | 50→68 | Steep two-plane roof over Great Hall; several 5–7-wide dormers, not an unbroken dark slab. |
| Rear palace / arena | X[-50,50), Z[110,155) | 52→65 outside main spire | Lower cross-gables frame the tower; arena ceiling stays below spire support level. |
| West/east wings | X[-88,-50), [50,88), Z[71,145) | 40→56 | Roof ridge runs Z, with transverse gables at forward and rear entrances. Clip under embedded towers. |
| Forward towers | 19×19 at Z[82,101) | eave 62/65 → peaks 85/89 | Narrow steep pyramidal or octagonal-feeling cap using stepped block rings. |
| Rear towers | X[-42,-23), [23,42), Z[126,145) | eave 70/72 → peaks 93/95 | Palace-side towers, inward of forward pair; sharper caps and asymmetric finials. |
| Main spire | X[-13,13), Z[125,151) | shell begins Y60, shoulder 78 → peak **120** | Tall white shaft over a Y54..59 transfer deck; dark steep cap with one finial cell at Y120. |
| Gate towers | 17×17 at Z[-77,-60) | eave 35 → peak 48 | Small dark caps; do not compete with palace tower group. |

The silhouette intentionally differs from preliminary `exterior_spec.md`: palace ridge 68 rather than whole palace top 55; forward towers 85/89 and rear towers 93/95 rather than paired identical peaks. The fixed site and 120-high main apex remain unchanged. No roof overhang extends beyond site X[-110,110), Z[-90,170).

## Materials and construction logic

- **Proposed, not finalized:** polished deepslate stairs/slabs and deepslate tiles for the dark roof field, with sparing dark prismarine or blue-gray accent around feature dormers. The block palette document deliberately leaves roof material open; AI/Human review must approve this choice before build.
- Roof slopes use real stair/slab layering and full-block backing. Avoid a huge hollow dark prism projected from the façade. Every visible eave has white quartz cornice or corbel support.
- Gothic verticality comes from a small number of legible tower peaks, dormers and buttresses. Do not repeat 01/08-style microspires on every wall bay.
- Forward tower feet embed in wing shells; rear tower feet embed in palace side bands. Tower plans own their overlapping 19×19 cells. Wing/palace roofs terminate against tower wall with flashing/cornice, not through the tower interior.
- Front/rear palace roof planes meet through a framed cross-gable near Z107..114. The main spire's plinth sits above the Y54..59 transfer deck and replaces rear roof cells within X[-13,13), Z[125,151) at Y60 and above. No support enters the arena clear volume.
- At all wing/tower, cross-gable and spire joints use the cell ownership and precedence in `phase1_revision_sections.md`; broad roof envelopes in this document are visual volumes and are clipped by that rule.
- The main spire may be decorative and inaccessible above its observation level; no speculative climb to Y120 is needed for the dungeon route. Wing/gate towers that are used for play require actual internal stairs in later authoring.

## Review questions

1. Is the 120:95:89:68 height rhythm close enough to reference 07 when seen at approach distance?
2. Are four side towers distinct in actual Minecraft oblique views after the rear pair moves inward, or does perspective still merge one near-side pair?
3. Can the palace cross-gable and spire plinth be supported outside the throne combat clearance without a visually heavy beam across the arena?
4. Does the provisional dark roof palette read as the reference's blue-black material in vanilla lighting?
