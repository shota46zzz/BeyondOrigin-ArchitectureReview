# White Castle Phase 1 Revision — sections, silhouettes and joint ownership

Status: `DESIGN_REVIEW_PENDING`, revised after AI Design Review of commit `eb297b9003c1a0159f0973020ce1b014bbf4e6c6`. **Design geometry only.** No block placement, NBT, Gameplay or Round 3 Evidence change is authorized. This file resolves WD-01/02/03/04 in the coordinate plan; visual/build proof remains pending.

All X/Z bounds are half-open. Site: X[-110,110), Z[-90,170); anchor `(500000,4,500000)`; +Z goes from gate to Keep; local Y0 is flat-world ground. Main stair is 11 wide. Main finial occupies at most Y120. Reference `07_main_exterior_target.png` remains the primary exterior goal.

## WD-01 — Throne Arena and main spire section

The protected arena air is **X[-18,17) × Z[114,142) × Y[30,54)**: 35×28 in plan, with 24 blocks of vertical clearance. No hidden floor or pier may enter this volume. Its supporting floor is at block Y29, walking surface Y30. The main spire shell is X[-13,13) × Z[125,151) × Y[60,121), ending with its highest finial cell Y120. The 6-layer transfer assembly occupies Y[54,60) and is the only structure allowed directly above the protected air. Neither the deck nor hanging corbels may descend to Y53.

| Support / transfer element | Exact proposed block-cell range | Relationship to arena |
|---|---|---|
| West side pier band | X[-25,-19), Z[123,147), Y[26,54) | Ends at X=-20, one full cell before protected X=-18. Joins west palace side wall and rear-tower footing. |
| East side pier band | X[18,24), Z[123,147), Y[26,54) | Begins at X=18, one full cell after protected last X=16. Joins east palace side wall and rear-tower footing. |
| Rear pier / arcade band | X[-25,24), Z[142,151), Y[26,54) | Begins at Z142, exactly beyond protected last Z141; large rear door openings require later block-state design. |
| Continuous transfer plate | X[-25,24), Z[123,151), Y[54,57) | Full 3-cell-thick ceiling/bridge under the spire shell; its underside is Y54, outside protected air. |
| Front transfer rib | X[-25,24), Z[123,126), Y[57,60) | Stiffens plate above protected air; ties to side pier tops through the plate. |
| Rear transfer rib | X[-25,24), Z[142,151), Y[57,60) | Above rear piers; carries back of spire plinth. |
| Side transfer ribs | X[-25,-19) and [18,24), Z[126,142), Y[57,60) | Above side piers; connect front/rear ribs into a rectangular frame. |
| Spire plinth / shell | X[-13,13), Z[125,151), Y[60,121) | Sits on transfer level; no column descends through arena. White shaft, dark roof and single Y120 apex. |

At Z130, the cross-section is:

```text
Y120                            ^ finial (single apex)
Y60..119                [ white shaft / dark spire ]
Y54..59      ================= TRANSFER DECK =================
Y30..53      || west pier ||  35-wide ARENA AIR  || east pier ||
Y29          _______________ arena floor ______________________
                 X<-18      X[-18,17)       X>=17
```

The diagram is schematic; the **tabulated exact ranges** govern. In the direction of Z, protected arena air ends before the rear pier starts. The continuous transfer plate and raised ribs span the arena at roof level. In Minecraft, quartz/deepslate structural blocks do not fall, but the design must still **look** supported: expose at least two end buttresses on each side and arch/step the transfer fascia upward at Y54..59. No decorative pendant enters Y[30,54). The rear side tower and side-pier volumes overlap at their outermost cells; support ownership wins there. Proposed construction is logically collision-free against the protected arena prism, not verified by a Minecraft sightline, navigation run or physical engineering analysis.

## WD-02 — four-tower projection check

Forward towers stay in the outer wings: FT-W X[-77,-58), FT-E X[58,77), Z[82,101), peaks Y85/89. Rear towers move inward to the palace side bands: RT-W X[-42,-23), RT-E X[23,42), Z[126,145), peaks Y93/95. Rear micro-turrets in the preliminary table are omitted. The center spire X[-13,13), peak Y120 remains unique.

**Axial front projection** (view from -Z; 16-cell outer gaps and 10-cell inner gaps):

```text
X: -77  -58  -42  -23  -13   13   23   42   58   77
   [ FT-W ]   [ RT-W ]   [  CS  ]   [ RT-E ]   [ FT-E ]
      85         93         120         95         89  <- peak Y
```

**Approximate oblique construction projections.** To assess left/right approach views without falsely claiming a rendered image, project each tower center to `u = x + k(z-100)` from design-left, and `u = x - k(z-100)` from design-right, with `k=0.35`. This is an orthographic planning proxy, **not** Minecraft camera perspective. FT centers are (±67.5,91.5), RT centers (±32.5,135.5), and CS center (0,138). Rounded projected centers:

The corresponding three-panel vector **planning diagram** is [`silhouette_study.svg`](silhouette_study.svg). Its simplified roof shapes are conceptual; the table here supplies the exact projection inputs.

| View | FT-W | RT-W | CS | RT-E | FT-E | Consequence |
|---|---:|---:|---:|---:|---:|---|
| Front (`k=0`) | -67.5 | -32.5 | 0 | 32.5 | 67.5 | Five distinct center positions; intervals disjoint. |
| Left (`+0.35`) | -70.5 | -20.1 | 13.3 | 44.9 | 64.5 | Right pair center separation ≈19.6, just more than 19-wide tower. |
| Right (`-0.35`) | -64.5 | -44.9 | -13.3 | 20.1 | 70.5 | Left pair center separation ≈19.6; mirrored depth read. |

```text
LEFT OBLIQUE (planning proxy)       RIGHT OBLIQUE (planning proxy)
FT-W    RT-W   CS   RT-E FT-E      FT-W RT-W   CS   RT-E    FT-E
 85      93   120     95   89       85    93   120    95      89
```

The gap is narrow in oblique views and perspective can close it. Different roof peaks and the rear towers' deeper Z position must carry the separation. AI/Human review still requires actual front/left/right screenshots **after** design approval and Draft Build; these diagrams only reject an obvious front-coordinate overlap before building.

## WD-03 — seam sections and block precedence

The broad envelopes in `exterior_layout.md` identify masses. At a shared cell, exactly one module places the final block. This priority applies only to **design of the future draft**, not to existing Round 3 assets:

1. Protected route/arena clearance removes any generic floor, roof or decoration inside its air prism.
2. Main spire transfer support and rear-tower footing own their explicitly tabulated cells.
3. Tower shell owns its footprint where it overlaps a wing or palace shell.
4. Palace shell owns its cells at the wing contact face and main ridge.
5. Wing shell owns the remaining wing cells.
6. Cornice/flashing owns surface trim only after structural cell ownership is settled.

| Joint | Exact seam / section | Roof, wall, floor resolution |
|---|---|---|
| Forward tower ↔ wing | FT X[-77,-58) / [58,77), Z[82,101), Y[24,90). Wing roof Y40..56 is **omitted** within FT X/Z. | FT wall and interior stairs own the footprint. Wing floor stops at tower wall except a 3–5-wide doorway chosen in detail design; wing roof eave butts into FT at Y40 with 1–2 cell stepped quartz flashing. |
| Rear tower ↔ palace | RT X[-42,-23) / [23,42), Z[126,145), Y[26,96). Palace rear roof Y52..65 is **omitted** within RT X/Z. | RT wall and stair core own its prism. Palace rear side corridors meet an authored doorway outside the protected X[-18,17) arena clear strip; cornice terminates against RT wall. |
| Wing ↔ palace | Wing east begins X50 where P0 ends X50; west wing ends X-50 where P0 begins X-50. Contact Z[71,145). | P0 owns its wall at x49/-50; wing owns x50/-51. Matched door voids at Z[84,89) and [120,125), floor level aligned in later detailing. No overlap or open air slit. |
| Front palace roof ↔ rear palace roof | Cross-gable seam Z[107,114), X[-50,50), eave Y50..52, ridges 68/65. | P0 owns both fields. Higher front roof stops at framed cross-gable; rear roof tucks under a 2-cell flashing band. Avoid two full roof planes occupying the same cells. |
| Rear palace roof ↔ spire | Spire X[-13,13), Z[125,151), shell begins Y60; transfer ring Y54..59. | P0 roof is clipped from transfer-ring cells, not punched through after the fact. CS owns its shell at Y60+. White cornice conceals roof junction; no roof plane penetrates shaft. |
| Stair ↔ terrace | S0 X[-6,5), Z[-25,30), T0 begins Z27; S1 X[-7,8), Z[55,72). | Stair owns all tread/floor cells in overlap, terrace/garden owns adjacent cells. Backing/support is continuous below walking surface. |

Final stair facing, roof stair orientation, light support, door lintel and visual seam quality require Minecraft draft review. The exact half-open bands above are sufficient to prevent two design modules from claiming the same roof/floor volume without an explicit owner.

## WD-04 — source precedence and still-open gates

For this exterior redesign, read `exterior_layout.md` + this revision first. Then read `elevation_plan.md`, `tower_roof_spec.md`, `window_facade_spec.md`, `interior_allocation.md`, and `reference_comparison.md`. `exterior_spec.md` is high-level intent and marks its preliminary table **historical**. The eight PNGs in `references/` and `manifest.json` are the actual visual reference set; no `references/exterior_target.png` is expected. Existing Round 3 code/evidence and older White Castle V2 documents describe a different compact draft and are not this redesign's construction coordinates.

Human decisions remain: mandatory or optional east/west towers under `docs/05_白い城.md`; final roof material; terrain integration; treasury side; whether additional bridges are needed; and approval of this exterior design. This section resolves coordinate-level collisions as a **proposal**, not built/walk-tested proof. `DESIGN_REVIEW_PENDING` remains the final state.
