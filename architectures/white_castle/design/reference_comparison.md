# White Castle reference comparison and AI Design Review packet

Status: `DESIGN_REVIEW_PENDING` — **design only, no architecture build**.

## Evidence and visual reading

Source: `architectures/white_castle/references/manifest.json`, branch `white-castle-exterior-redesign`. All eight original PNGs were opened as images during this design pass, not merely found by filename. Local file SHA-256 and byte lengths matched manifest **8/8** on 2026-10-10. The 07 image is the primary target; 01 and 08 are deliberately secondary.

| Image | Visual content actually inspected | Translation / restraint |
|---|---|---|
| 01 `gothic_cathedral_extreme` | Huge pale cathedral, very dense needle pinnacles, enormous central arched opening, blue glazing. | Borrow large pointed opening and vertical rhythm; reject all-over needles. |
| 02 `blue_rose_window_detail` | Large blue patterned glazing within a stepped white arch; side wall bays and cornices. | One feature blue window in central façade, smaller pane bays elsewhere. |
| 03 `gothic_interior_windows` | Dark interior arcade, tall pale stone window reveals, blue/gray glass and wide walking aisle. | Tall side-light windows and legible hall pillars; keep external palette white. |
| 04 `height_chart` | Bars give hierarchy from low wall/gate through Keep/towers to 120-high central spire. | Preserve unique 120-high apex; use lower 85–95 side towers. |
| 05 `site_plan` | Axial gate, staircase, garden, palace/arena; two pairs of flanking towers within a rectangular 220×260 boundary. | Set exact half-open envelopes in `exterior_layout.md`; diagram is not block-accurate. |
| 06 `silhouette_diagram` | Simple white central shaft with dark tall roof, stepped lower side masses. | Height rhythm and dark cap logic; add depth/layering beyond the diagram. |
| 07 `main_exterior_target` | White complex rising in planted tiers from a broad stair; substantial left/right lower masses, bridges/arcades, dark steep roofs, multiple slim towers, central upper spire. | Primary composition: garden ascent, layered wings, asymmetric towers, dark roofs and singular central apex. |
| 08 `gothic_castle_extreme` | Pale castle crowded with spires, repeated pinnacles and deep pointed openings. | Reuse a few buttress/arch motifs; avoid the visual density as a whole. |

## Comparison of proposal to primary image 07

| Criterion | Image 07 | Proposed plan | Gap / review action |
|---|---|---|---|
| Distant silhouette | Complex tiers, one highest center, several flanking peaks. | Gate 48, palace roof 68, forward 85/89, rear 93/95, center 120. | 3D oblique render required: front/rear towers share X bands and may merge. |
| White wall / dark roof contrast | Broad white masonry under blue-black steep roofs. | White concrete/quartz/diorite fields; provisional deepslate roof. | Roof color and texture need Human approval under normal Minecraft light. |
| Main approach | Broad rising stair and planted terraces. | S0 width 11, rise 16; T0 144×35; S1 to palace Y26. | Reference stair may read broader than 11; flanking terraces/rails must carry visual width without changing the required 11-wide route. |
| Palace layering | Low wings and tall center with overlapping roofs and arcades. | Wings ridge 56, palace ridge 68, central shaft to 120; tower intersections explicitly owned. | Façade elevation and 3D draft must prove joints look built, not colliding. |
| Blue windows | Tall blue accents among pale arches. | Light-gray pane majority, one strong blue central window and limited accents. | Exact blue-glass pattern is stylized to Minecraft scale; no image-exact rose window claim. |
| Side structures / bridges | Additional distant wings, arches and elevated links. | Two wings, embedded tower pairs, lower curtain and side loops. | Reference includes more secondary bridges/buildings; omit for now to keep 220×260 envelope and clear hierarchy. Candidate later only after exterior review. |
| Garden texture | Trees/hedges along tiers and stair. | T0 reserved for vegetation and parapets. | Species, density and biome integration remain unapproved; flat-world source is not a worldgen solution. |

## Consistency audit

The six design files share site X[-110,110), Z[-90,170), center X=0, anchor `(500000,4,500000)`, local main apex Y120, 11-wide S0 and half-open footprint notation. All proposed occupied X/Z bounds remain inside the site. Palace/wing faces meet at X=±50, with explicit planned door bands. Wing/tower and palace/spire intersections are **intentional single-owner volumes** that require later detailed block ownership, rather than a false claim of collision-free prefabs. The garden/stair and gate/court overlaps are designated tread/floor interfaces. The arena contains at least a proposed 35×28 clear rectangle beneath the spire. No NBT or placed block proves these design relationships yet.

## Review request and open decisions

Please judge (1) resemblance to image 07 from front and both oblique elevations, (2) legibility of four side towers, (3) roof/wing/spire junctions and main-spire support outside the 35×28 arena, (4) 11-wide stair reading as a monumental approach within the planted terraces, (5) white/dark/blue palette in vanilla lighting, and (6) whether required White Castle rooms and tower progression fit without flattening the silhouette.

Human decisions still pending: exact tower-route interpretation against `docs/05_白い城.md`; roof material; final side of treasury; terrain/site adaptation; whether the reference's extra bridges are required; and design approval before any Draft Build. `exterior_spec.md` still names an obsolete `references/exterior_target.png` pending-upload placeholder and has older preliminary massing numbers; the actual approved input is the eight-image manifest here. These source discrepancies are surfaced for review, not silently rewritten.

**Final state: DESIGN_REVIEW_PENDING.** Round 3 evidence remains immutable. No architecture, Generator, Minecraft world, NBT or Gameplay has been modified for this redesign.
