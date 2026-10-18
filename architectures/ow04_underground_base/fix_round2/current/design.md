# OW-04 Underground Base — Architecture Fix Round 2

Status: **DRAFT / AI VISUAL RE-REVIEW PENDING**. No approved Structure NBT, gameplay, or worldgen integration.

## Review basis

Fix Round 1 Evidence: `875bc925ecbfba52baaa7310b04a403206868ada`. [ChatGPT AI Visual Re-Review](https://chatgpt.com/c/6ad551d6-357c-83ec-a6bc-c192a1c580bf) inspected 19/19 Minecraft PNGs and returned `NEEDS_FIX`. It marked detention/administration differentiation and hangar use resolved. Remaining issues were the surface entrance silhouette, armory readability, repeated security spine, lower ramp connection evidence, and machinery readability. It also requested inspection of a possible floor gap visible at the edge of the weapons screenshot. SHA-256 was independently checked by Codex, not by that reviewer.

## Draft changes

- The original entry axis remains open. Unequal forward gate wings, a stepped lintel and roof tiers add depth to the bunker face within the existing X/Y/Z bounds.
- The weapons wing now has three wall storage cages per side, upright rack elements, and an offset inspection island. Its main entrance aisle remains clear.
- Two different guard stations and contrasting floor sections interrupt the security spine. The central seven-block path remains open.
- The reactor has side windows revealing the lit core, separated pipes and a control station. A separate laboratory work position is retained.
- The lower ramp geometry is unchanged. Additional views show its middle, stairs from the lower level, and the lower transition hub with its side exits.
- A plan assertion checks that all floor cells across X -14..-8 and Z 78..83 at local Y -10 are present beneath the armory threshold. The earlier blue image edge was not reproduced with the revised view; this is a targeted floor check, not a full room scan.

The previous 19 camera names are retained and five more views cover the close entrance, armory floor, lower ramp middle, lower ramp exit and lower hub connection. Images use the same daytime profile and interior render visibility aid; they do not establish natural lighting.

## Preview and validation

The final disposable preview is `run/saves/ow04-base-fix-round2-preview5-20261019`, anchor `(710000,4,710000)`. The 24 Minecraft PNGs and metadata were captured from this copy. Placement completed with 148,670 block cells and passed plan bounds, key-space, route and armory-threshold floor checks. `compileJava` and targeted `ArchitectureReviewTargetTest` / `NamedReviewViewpointTest` passed. Each PNG SHA-256 matches `metadata.json`.

Physical walking, mob navigation, natural terrain integration, lighting, village containment, NBT, gameplay, and worldgen remain unverified. The individual design's large scale versus the multi-dungeon brief's medium scale remains Human Decision Pending. Formal Human Review and asset approval have not occurred.
