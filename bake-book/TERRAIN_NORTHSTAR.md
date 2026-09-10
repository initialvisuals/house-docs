# Terrain north-star (fulcrumRust)

Parked from Evan overnight (2026-09-07). Flat world — **not** a spherical No Man’s Sky planetoid. Feel: Transvoxel / Lengyel-class smooth voxels, semi-detailed near, chunked far (bobgar look-language OK). Lab-Rat #38 ships the **shape-agnostic stamp / paint substrate** Hypha consumes — any authored shape → density + material; not more one-off scars. Lab-Rat #39 is the **extract-yard scale harness** for that substrate.

## First big-map brief (Evan 2026-09-08) — landed Hypha #81

First true big map for fulcrumRust extract. **Landed #81** (2026-09-09) as **19×19 / 304 m / 92 416 m²** (~8× old 7×7). Live host is **#142 37×37 / 592 m / 350 464 m²** (~4× the #81 yard; linear ~1.95×) + **#137 11×11** player-eye stream (`STREAM_RINGS` 5 · live hold=4/16 · coalesce=2/2) + **#151** cheap LOD-3 `visible=5/19` / desert `8` / 128 m / soft rim ~422 m + underfoot **32/16/8/4**. **#108** amortizes cook (cook=1/2 · prefetch=5 m · splash-pumped load-in) — not a new map size. **#123** deepens play (`defer=worker/paint/gpu` · skip far mask-only remesh). **#137** is the radius + warm-hold layer (prefetch=5+heading · shipped hold=2/12). **#142** is the next ~4× area expand + pend coalesce — **not** a STREAM radius bump. **#151** is STREAM past extract / desert floor / soft rim — fine window stays 11×11. Stamp pad stays **7×7** / far-cold (#23 guts cold). Walls **off**. This supersedes #43 **7×7 / 112 m / 12 544 m²** as the live walk lock. #16 / #23 / #43 / #60 / #61 / #81 stay prior shipped facts.

| Beat | Lock |
|------|------|
| **1. Higher res** | Already **#61** (32/16/4). **#81** keeps underfoot **32/16/8/4** (8-subdiv bridge so every adjacent step 2:1). Further res stays Hypha — do not claim more shipped |
| **2. Drop walls** | **Landed #81** — outer walls off; open horizon, soft XZ clamp |
| **3. ~8× extend** | **Landed #81** — **19×19 / 304 m / 92 416 m²** (~8× old 7×7). Prior fact — not the live yard |
| **3b. ~4× again** | **Landed #142** — **37×37 / 592 m / 350 464 m²** (~4× #81; linear ~1.95×). STREAM stays 11×11. Pend coalesce admit 2 / cap 2 |
| **4. Chunks** | **Landed #81** — chunked Transvoxel stream, not a single bake slab |
| **5. Scatter / PBR / deform** | **Landed #80** — DISP bake-down + `Deform` / `GroundScatter` filled at `8,-6` / 5 m · `-10,14` / 6 m. `PBR_HEIGHT_AMP` **0.028** · `SCATTER_AMP` **0.018** · pad half **56**. Smoke `pbr=tint plugs=slope+deform+scatter` |
| **6. Slope materials** | **Landed #81** — Hypha slope COL hooks (`pbr=tint` default). Vertex albedo only. NRM/GLOSS parked. Lab-Rat `classify_slope` + DISP bake-down **#80** |
| **7. Distance load** | **Landed #81** — local-player stream by eyes. Live **#137 11×11** (`STREAM_RINGS` 5). **#108** amortizes cook (cook=1/2 · prefetch=5 m · splash-pumped load-in). **#123** deepens play (`defer=worker/paint/gpu` · skip far mask-only remesh). **#137** heading prefetch + shipped hold=2/12. Live hold **#151** 4/16 + cheap LOD-3 `visible=5/19` + desert `8` (void → coarse floor — not unload/void past extract). **#142** pend coalesce `2/2` (not a STREAM radius bump). Beabim peer feet `stream_anchors` **landed #83** (coordinate only — Transvoxel rewrite / terrain sync still parked) |

### Seat ownership

| Seat | Owns |
|------|------|
| **Hypha** | Host — **8×** / walls off / chunk stream / local-player distance load **landed #81**. Next **~4×** area + pend coalesce **landed #142** (37×37 / 592 m / 350 464 m² · rings 18 · `coalesce=2/2` — not a STREAM radius bump). Stream hitch amortize **landed #108** (cook=1/2 · prefetch=5 m · splash-pumped load-in). Worker STREAM extract+paint **landed #123** (`defer=worker/paint/gpu` · skip far mask-only remesh). Play STREAM 11×11 + warm hold **landed #137** (`STREAM_RINGS` 5 · prefetch=5+heading · shipped hold=2/12). STREAM past extract / desert / soft rim **landed #151** (live hold=4/16 · `visible=5/19` · `desert=8` / 128 m · soft rim ~422 m `hook=augury`). Transvoxel UV consume **landed #112** (`promote_for_uv` + TerrainHost wear/COL honor; texture-only, never remesh). Beabim peer feet `stream_anchors` **landed #83** (coordinate only). Biped foot plant **landed #88** — consumes #79/#81 heightfield column; mesher / LOD / stamps untouched. Continues on fulcrumRust (Transvoxel rewrite / live octree / unconstrained Sync dump parked; amortized recook under budget is shipped #108; worker/paint/gpu deepen shipped #123; radius + warm hold shipped #137; 4× world + pend coalesce shipped #142; STREAM past extract shipped #151) |
| **Lab-Rat** | Stamps — slope/PBR/dirt/scatter/deform plugs **landed #80** (DISP bake-down + `Deform` / `GroundScatter` filled). Slope COL hooks reserved on host **#81** (Hypha vertex albedo only). Atelier **150 roughness + textures/PBR ~26 sets landed**. NRM/GLOSS GPU parked. **#81** reserved identity only — **#80** filled the plugs |
| **Range Tech** | Kits + FX draw-distance on the wider yard; kit metal/grit PBR stub **landed #64**; store `dBXpg` still **open**; Music playlist beds **landed #64**. #79 land sway + heightfield FX kept. Heat / ballistics / binds **not touched** |
| **Augury** | FoW brand / menu video **when cut ready**. Chrome **not touched** |

#16 / #23 / #43 / #60 / #61 stay shipped facts. #39 yard pad ≈ **110 m²** + stamp pad **7×7** stay the near extract / far-cold guts. Live walk world is **#142** on top of **#81** + **#151** horizon/desert/rim. Stream hitch amortize **#108**. Worker STREAM extract+paint **#123**. Play STREAM 11×11 + warm hold **#137** (live hold **#151** 4/16). 4× world + pend coalesce **#142**. STREAM past extract **#151**. UV consume **#112**. Lab-Rat plugs **#80**. Peer feet stream anchors **#83**. Pawn plant on that column **#88** (mesher untouched). See `FULCRUMRUST_LAST_PASS_LOCK.md` + `PEEK_FINDINGS.md` Closed by #81 / #108 / #123 / #137 / #142 / #151 / #112 / #80 / #83 / #88.

## Morning lock (2026-09-07)

Evan then: **stay on the extract yard** — refine + expand it as a **scale / perf testbed**. Lab-Rat #39 `apply_yard_harness` is that test (`growth::yard_bounds` ≈ **110 m²**; flatten disk tracks it). Stamp/paint substrate (density + material channels, shape-agnostic) over one-off scars. Mesh shapes OK to play with. HDRI stays Range Tech.

**Wider extract chunk radius shipped #43** — then `TerrainHost` **7×7 / 3 Chebyshev rings / 112 m span / ~12.5k m²** (was 5×5 / 2 rings / 80 m / 6 400 m²); one extra **far** ring only. Stamp pad **still 7×7**. **Near LOD raise shipped #61** — then center subdiv **32** / ring-1 **16** / outer **4** (was 16/8/4). **Live host lock landed #142** on top of #81 / #137 — 37×37 open + **11×11** stream + underfoot **32/16/8/4** + coalesce=2/2. **#151** cheap LOD-3 past extract + desert floor + soft rim (live hold **4/16**). **#81** stays the prior 8× / 19×19 fact. **#108** amortizes cook (cook=1/2 · prefetch=5 m · splash-pumped load-in). **#123** deepens play (`defer=worker/paint/gpu` · skip far mask-only remesh). **#137** live window **11×11** (shipped hold=2/12; live **#151** 4/16).

## Host (Hypha) — shipped fulcrumRust #16

First Transvoxel extract terrain host (flat world, not a planetoid). Bake-once at deploy.

| Lock | Detail |
|------|--------|
| **Crate** | crates.io **`transvoxel` 2.0** (`Gnurfos/transvoxel_rs`, Lengyel tables) — not a paste into Lab-Rat |
| **Host** | `TerrainHost` implements Lab-Rat `VoxelHost`; `stamp_field` + `sample_channels` feed density + `VoxelMaterial` |
| **Distance LOD** | Live underfoot **32 / 16 / 8 / 4** + Lengyel transition faces (**#81**; was #61 32/16/4). Every adjacent step **2:1**. #61 near raise stays a prior fact |
| **Grid / radius** | Live **#142 37×37 / 592 m / 350 464 m²** + **#137 11×11** stream (`STREAM_RINGS` 5 · live hold=4/16 · coalesce=2/2) + **#151** `visible=5/19` / `desert=8` / 128 m / soft rim ~422 m. **#81** prior 8× was **19×19 / 304 m / 92 416 m²**. Stamp pad stays **#43 7×7 / 112 m / 12 544 m²** / far-cold |
| **Skin** | verts grade from `VoxelMaterial::tint` / `luma`; cracks / edge-wear / void-spore scale from Lab-Rat `density_stamp_2d` + `WearStamp` |
| **Atmosphere** | darker clear + colder dual lights + cheap distance haze in `fs_world` (hideout stays unfogged) |
| **Hooks** | sit-on-surface structures stay; `AuguryLocusSpawn` reserved on a rise |
| **Not day-one** | live octree / unconstrained Sync dump · tunnel cutouts · runtime carve · globe · Transvoxel rewrite / world sync. **#114** is a shallow enterable pad network, not those parked cutouts. Amortized recook under budget **shipped #108** (cook=1/2 · prefetch=5 m). Worker extract+paint deepen **shipped #123** (`defer=worker/paint/gpu`). Play STREAM 11×11 + warm hold **shipped #137** (prefetch=5+heading · shipped hold=2/12). 4× world + pend coalesce **shipped #142** (37×37 · rings 18 · `coalesce=2/2` — not a STREAM radius bump). STREAM past extract / desert / soft rim **shipped #151** (live hold=4/16 · `visible=5/19` · `desert=8` — not unload/void past extract). Peer feet `stream_anchors` **landed #83** (coordinate only). Pawn plant on the #79/#81 column **landed #88** (mesher untouched). Near LOD raise **shipped #61**. First big-map **landed #81**. Wider radius / stamp pad shipped #43 |
| **Far guts (#23)** | Shared Locus `ACTIVATE_M`/`SLEEP_M`; far stamp guts + growth/Locus upload stay cold. **#39** near harness pad stays warm. **#43** extra far ring stays cold |

North-star refs still hold: https://transvoxel.org + Lengyel · [bobgar demo](https://bobgar.itch.io) look-language · ling0x as swap candidate (not vendored). Detail: fulcrumRust `docs/TERRAIN.md`.


## Distance activation / far-guts cold (Hypha #23)

Hardens extract cost so far chunks stay cheap — aligned with Augury Locus far-cold. Reuses #16 `TerrainHost` (no mesher rebuild). CE labyrinth DNA only (not a web port).

| Lock | Detail |
|------|--------|
| **Shared dials** | `ACTIVATE_M` **24** / `SLEEP_M` **32** — same hysteresis as Augury Locus (`activation.rs` asserts equality) |
| **Bake rings** | Match Transvoxel LOD 0/1/2; far rings skip stamp-structure / wear density consume + per-vert wear walk |
| **Far extract bake** | Stamp plates / structures / wear stay out (collide boxes still land); far crates/poles skipped; brutalist compounds stay for horizon |
| **Live cold** | Growth + Locus GPU uploads skip past `ACTIVATE_M`; yard Idle still visible; cycle/curl keep ticking. **#39** near yard (harness pad ≈ **110 m²**) stays warm (`bake_guts_warm`); harness primitives are near-warm only |
| **Smoke peek** | #23: `near_chunk=862` · `far_chunk=45` · `guts_warm=17` · `guts_cold=140` · `terrain_tris=3168` (~19× cheaper far mean). **#39 harness:** `layers=43` · `prims=216` · `yard_m2=110` · `guts_warm=75` · `guts_cold=140` · `near_chunk=858` · `far_chunk=45` · `terrain_tris=3182`. **#43 radius:** `near_chunk=858` · `far_chunk=39` · `guts_warm=75` · `guts_cold=216` · `rings=3` · `extract_m2=12544` · `yard_m2=110` · `terrain_tris=4034` · `lods=3` (~22× cheaper far mean). **#61 near LOD:** `terrain_tris=11118` · `lods=3` · `subdivs=32/16/4` · `near_chunk=3290` · `far_chunk=39` · `guts_warm=75` · `guts_cold=216` · `rings=3` · `extract_m2=12544` · `grit_mips=256/64/16` · `n=196608` · `f=768` (~84× cheaper far mean). Far cheapness holds (`far_chunk < near_chunk`) |

Near yard / stamp pad stay the extract guts on the **7×7** far-cold ring. Live walk world is **#142** on top of **#81**. Steal map: Hypha chunk-LOD row + Augury enemy-activation notes. Detail: fulcrumRust `docs/TERRAIN.md` + `LOCUS_AI_LOCK.md`.

## Consume channels (Lab-Rat #17)

Lab-Rat ships the density + material sample path Hypha feeds into Transvoxel. Not another mesher.

| API | Role |
|-----|------|
| `DensitySample` / `sample_channels` | Signed density + `VoxelMaterial` at a point |
| `fill_chunk_samples` | Regular grid fill (`ix` fastest, then `iy`, then `iz`) |

**Density convention:** `> 0` solid (below heightfield / inside structure / inside a wear leftover), `< 0` air, `0` isosurface. Hypha flips the sign if the chosen port disagrees.

CPU-box overlays stay a peekable leftover; the consume path is the density/material sample. Far-chunk simplify + transition cells stay Hypha.

Detail: fulcrumRust `docs/STAMPS.md` + steal-map Transvoxel row.

## Resource pile (eval, don’t wholesale port)

House `TERRAIN_NORTHSTAR` used as an **eval pile** for #16 — not a perfect-pick gate. Prefer one solid host over parallel rebuilds.

| Source | Verdict for #16 |
|--------|-----------------|
| [transvoxel.org](https://transvoxel.org) + Lengyel | **North-star.** Tables via the crate. |
| crates.io **`transvoxel` 2.0** | **Shipped.** |
| [ling0x/transvoxel](https://github.com/ling0x/transvoxel) | Swap candidate; not vendored. |
| [sjoerdev/voxel-engine](https://github.com/sjoerdev/voxel-engine) | Look/perf only — not a mesher. |
| [DXGatech/Smooth-Infinite-Voxel-Terrain](https://github.com/DXGatech/Smooth-Infinite-Voxel-Terrain) | Later live LOD / octree DNA; UE-bound. |
| [bw2012/UnrealSandboxTerrain](https://github.com/bw2012/UnrealSandboxTerrain) | Carve / mat-count later; not day-one. |
| [qwertzui11/voxelTerrain](https://github.com/qwertzui11/voxelTerrain) | Far-chunk simplify reference. |

Reuse week-one concrete/dirt/sand DNA where it fits.

## Stamps (Lab-Rat) — fulcrumRust #15

Organic voxel surface structures + smart-material tags onto Hypha’s density field. Not a 3D paint editor.

- **Materials:** dirt / sand / rock / concrete / organic on **8 m** cells (rule-based)
- **Structures:** sit-on-surface mushroom / web / rock / lip / ripple / grit (skip yard + spawn)
- **Host handoff:** Lab-Rat ships `VoxelHost` + `classify` / `stamp_field`; **Hypha #16** implements real heightfield + meshed stamped cells + distance LOD
- Detail: fulcrumRust `docs/STAMPS.md` + house `STAMP_FEEL_LOCK.md`

## Void-spore + wear leftovers (Lab-Rat #20)

Visual DNA for Hypha’s Transvoxel grade — still not a mesher.

- Shared `density_stamp_2d` drives yard silhouettes **and** concrete crack / edge-wear
- Wear leftovers (`ConcreteCrack` / `ConcreteEdge` / `VoidSporeWeb` / `VoidSporeBloom` / `VoidSporeCrack`) write into density + material channels
- Keep `classify` + `stamp_field` + `density_stamp_2d` wear on the live `TerrainHost`
- **Hypha #16** grades verts grimdark via `VoxelMaterial::tint` / `luma`; brutalist masses are the upward scale target
- Hypha eval pile (sjoerdev / DXGatech / UnrealSandboxTerrain / qwertzui11) stays host DNA — Lab-Rat does not own tables

## Shape-agnostic stamp / paint substrate (Lab-Rat #38)

Technology lock for Hypha consume — **not** another mesher and **not** Transvoxel host ownership (see Host #16 above). Feed a shape; do not add a new WearKind for the next landmark.

| Feed | Path |
|------|------|
| **Closed-form SDF** | `field.stamp(Primitive::…)` — sphere / ellipsoid / capsule / box / ribbon / brush / height-mask / mesh / volume |
| **Paint** | `StampField::paint` / `ChannelStack::paint` — writes real; brush UX stubbed. `density_delta > 0` puffs; `< 0` + Subtract carves; density 0 = material-only on existing solid |
| **Mesh→voxel** | `MeshStamp` → `voxelize_mesh` (step ~0.10–0.25 m, pad) → `SampledVolume` → `stamp_volume` (prefer compounds); `stamp_mesh` for small live SDF. World meters, Y-up, CCW outside |
| **2D mask / pycelium** | `Mask2D` → `Primitive::height_mask`; helper `primitive_from_density_2d` — #39 harness applies it on the three existing plots via `StampField::layers` as a shallow anonymous scale test (still not a fourth named plot) |

`ChannelOp`: Union / Subtract / Paint / Replace. `StampField::layers` (authored extras) vs `StampField::content` (compiled consumers: sit-on-surface, wear, Inked hotspot, yard/curl, **#114** shallow Subtract crawl; **#127** probe consume appends at bake). **#130** sandbox pedon is an off-stream leftover overlay — `StampField::layers` / `stream_rev` stay cold; STREAM remesh stays Hypha **#123**; pad crawl stays **#114**. Hypha `sample_channels` / `fill_chunk_samples` unchanged. Lab-Rat writes; Hypha remeshes.

Detail: fulcrumRust `docs/CHANNELS.md` + house `STAMP_FEEL_LOCK.md`.

## Extract-yard scale harness (Lab-Rat #39)

Stay **on the extract yard** for what #39 shipped. `apply_yard_harness` is the perf/scale test of the #38 substrate — not a bigger world map on that pass. First big-map walk **landed #81**; stamp / harness pad stays **7×7**. No Standard / Monk one-off scars. HDRI stays Range Tech.

| Lock | Detail |
|------|--------|
| **Pad** | `growth::yard_bounds` ≈ **110 m²** (baseline before harness ≈ **54 m²**); flatten disk tracks it so plots stay playable |
| **Writes** | Anonymous SDF lattice + larger paint brushes + 2D-mask convert of the three existing plots through `StampField::layers` (not a fourth named plot) |
| **Near / far** | Near yard stays warm (`bake_guts_warm`). Far guts stay cold (#23). Harness primitives near-warm only; smoke fails if a layer center is far. `guts_cold` stayed **140** |
| **Smoke** | keys `layers=` `prims=` `yard_m2=` · `layers=43` · `prims=216` · `yard_m2=110` · `guts_warm=75` · `guts_cold=140` · `near_chunk=858` · `far_chunk=45` · `terrain_tris=3182`. Baseline: `layers=0 prims≈content yard_m2≈54 guts_warm=32`. Far cheapness holds (`far_chunk < near_chunk`). Growth GPU boxes still under 620 |

Detail: fulcrumRust `docs/CHANNELS.md` + `docs/GROWTH_POC.md` / `docs/TERRAIN.md`.

## Wider extract chunk radius (Hypha #43)

Shipped the then clerk lock: **wider chunk radius first**. Extra **far** ring only. Near LOD raise **shipped later as #61**. Stamp pad **still 7×7**. Live walk lock **landed #81**.

| Lock | Detail |
|------|--------|
| **Grid** | `TerrainHost` **5×5 → 7×7** (smallest honest odd widen) |
| **Playable extract** | **3 Chebyshev rings / 112 m span / 12 544 m²** (was 2 rings / 80 m / 6 400 m²) |
| **Near LOD** | Unchanged *by #43*: then 16/8/4. **#61 shipped** the raise: **32/16/4**. **#81** live underfoot **32/16/8/4** |
| **Far-cold** | Still `lod >= 2` → heightfield-only; shares Locus `ACTIVATE_M` **24** / `SLEEP_M` **32** |
| **Lab-Rat stub** | `ExtractStubHost` aligned (`STUB_GRID = 7`) |
| **Smoke peek** | `near_chunk=858 far_chunk=39 guts_warm=75 guts_cold=216 rings=3 extract_m2=12544 yard_m2=110 locus_hp=24 terrain_tris=4034 lods=3`. Far mean ~**22×** cheaper than near; extra far ring added cold guts; yard pad + Locus stay |

Stay out of Atelier / HDRI / title mark on that pass. No new named scars. Live walk lock **landed #81**. Detail: fulcrumRust `docs/TERRAIN.md`.

## Near LOD raise (Hypha #61)

Queued A/B after #43. Reuse the existing Transvoxel host — no greenfield rebuild. Grid/radius stay #43. Grit mips stay #60.

| Lock | Detail |
|------|--------|
| **Subdivs** | Center **32** · ring-1 **16** · outer **4** (was 16/8/4) |
| **Near step** | **2:1** (32→16) so Lengyel transition faces still stitch toward finer neighbours |
| **Outer** | Stays coarse (**4**) so far guts stay cheap |
| **Grid / radius** | Still **7×7 / 3 Chebyshev rings / 112 m / 12 544 m²** (#43) |
| **Grit mips** | Still **256² / 64² / 16²** on the same rings (#60). Far still heightfield-only / cold guts |
| **Smoke peek** | `terrain_tris=11118 lods=3 subdivs=32/16/4 near_chunk=3290 far_chunk=39 guts_warm=75 guts_cold=216 rings=3 extract_m2=12544 grit_mips=256/64/16 n=196608 f=768`. Far mean ~**84×** cheaper than near |
| **Parked** | Live octree / unconstrained Sync dump · tunnels · runtime carve (**#114** is a shallow pad network, not those parked tunnels). Live walk lock **landed #81** (32/16/8/4 + 19×19 open). Stream hitch amortize **later landed #108** |

Stay out of Range Tech guns / Augury brains / Lab-Rat stamp baking. Detail: fulcrumRust `docs/TERRAIN.md`.

## First big-map open extract (Hypha #81)

First true big map. Reuse the existing Transvoxel host — no greenfield rebuild. Stamp pad stays #43 **7×7** / far-cold. #79 land sway + heightfield FX kept. [PR #81](https://github.com/initialvisuals/fulcrumRust/pull/81) (`73dc8fe4`).

| Lock | Detail |
|------|--------|
| **Extract** | **19×19 / 304 m / 92 416 m²** (~8× old 7×7) |
| **Walls** | **Off** — open horizon, soft XZ clamp |
| **Stream** | Live **11×11** window (`STREAM_RINGS` 5 — **#137**; #81 opened 9×9). **#108** amortizes cook (cook=1/2 · prefetch=5 m · splash-pumped load-in). **#123** deepens play (`defer=worker/paint/gpu` · skip far mask-only remesh). **#137** heading prefetch + shipped hold=2/12. Live hold **#151** 4/16 + cheap LOD-3 `visible=5/19` + desert `8`. **#83** `stream_anchors` also returns remote feet so the window can follow a peer (coordinate only — no Transvoxel rewrite) |
| **Underfoot** | **32 / 16 / 8 / 4** — every adjacent step **2:1** (was 32/16/4; 16→4 opened voxel gaps) |
| **Stamp pad** | Still **7×7** / far-cold (#23 guts cold) |
| **PBR** | Slope COL hooks (`pbr=tint` default). Vertex albedo only. NRM/GLOSS parked |
| **Lab-Rat** | `Deform` / `GroundScatter` + `LabRatDeform` / `LabRatScatter` identity reserved here. **Filled later #80** |
| **Seams** | One extract density on every LOD (ChannelField vs HeightOnly fixed) · 8-subdiv bridge so 32→16→8→4 stays 2:1 Lengyel · yard flatten outer **9.2 → 20 m** so pad eases into hills. Residual soft LOD pop inside a cell still parked. Far-4 / void-past-extract horizon **later landed #151** cheap LOD-3 (`visible=5/19`) + desert floor. Stream hitch amortize **later landed #108**. Worker STREAM extract+paint **later landed #123** |
| **Smoke** | `subdivs=32/16/8/4` `extract_m2=92416` `resident=` `stream_cold=` `pbr=` |
| **Parked** | NRM/GLOSS GPU · Transvoxel rewrite / world sync · live octree / unconstrained Sync dump · Range heat. Amortized recook under budget **later landed #108**. Worker extract+paint deepen **later landed #123**. Lab-Rat plugs **landed later #80**. Peer feet `stream_anchors` **landed #83** (coordinate only). Pawn plant on this column **landed #88** (mesher / LOD / stamps untouched) |

Stay out of Range heat cards / ballistics / binds / Augury chrome. Detail: fulcrumRust `docs/TERRAIN.md`. See `PEEK_FINDINGS.md` Closed by #88 / Closed by #108 / Closed by #123 / Closed by #137 / Closed by #151.

## Stream hitch amortize (Hypha #108)

Hitch *fix* layer 1 — not a new map size. [PR #108](https://github.com/initialvisuals/fulcrumRust/pull/108) (`b3be2974`). Hitch *visibility* stays Augury #110 (Hypha emits `STREAM` / `BAKE`, does not rebuild Home chrome). Mesher stolen (`TerrainHost` / `extract_one` / activation) — no greenfield mesher. Worker/paint/gpu deepen **later landed #123**. Play STREAM 11×11 + warm hold **later landed #137**.

| Lock | Detail |
|------|--------|
| **Load-in** | Skeleton (density + stamps + props) on frame 0; splash keeps presenting; **2** extracts / frame (`COOK_BUDGET_LOAD`) until idle; GPU upload only when the window is ready. No Sync whole-window dump on one frame |
| **Play** | **1** extract / frame (`COOK_BUDGET_PLAY`). Dirty jobs sorted underfoot-first via `TerrainHost::pump_stream` |
| **Prefetch** | **5 m** face prefetch upgrades the next already-resident neighbor to lod 0 *before* the step. Live heading prefetch **#137** |
| **No-op** | Walk inside a cell with focus+LOD unchanged stays a no-op; stale LOD stays until the budget reaches it |
| **Emit** | Augury Home `STREAM` / `BAKE` (`r=` `cold=` `pend=`) into #110 logger |
| **Smoke** | `cook=1/2 prefetch=5` next to `subdivs=32/16/8/4` |
| **Parked** | Live octree · residual soft LOD pop inside a cell · unconstrained Sync dump |

Stay out of Range poses / AIM TUNE / loot · Lab-Rat UV (#101) · Beabim net · Augury Home tabs. See `PEEK_FINDINGS.md` Closed by #108 + `FULCRUMRUST_LAST_PASS_LOCK.md`. Worker extract+paint deepen: Closed by #123. Radius + warm hold: Closed by #137.

## Worker STREAM extract+paint (Hypha #123)

Deepen of stream hitch *fix* after #108 amortize — not a new map size. [PR #123](https://github.com/initialvisuals/fulcrumRust/pull/123) (`b4725b8c`). Hitch *visibility* stays Augury #110 / #121 (Hypha emits only — no debugger rewrite). CHANNELS stay bake-time. Load splash stays sync. Play STREAM 11×11 + warm hold **later landed #137**.

| Lock | Detail |
|------|--------|
| **Play** | Worker extract+paint. Hitch thread never `sample_channels` on play Transvoxel extract. Worker owns extract+paint. Tick only applies one finished mesh then leftover paint/GPU |
| **`defer`** | **`worker/paint/gpu`** |
| **Cook / prefetch** | #108 stays: cook=1/2 · cook_ms **8/16** · face prefetch **5 m**. Live heading + hold **#137** |
| **Far remesh** | Skip far mask-only remesh when R climbs (no lod-2/3 storm on row add) |
| **Emit** | STREAM `extract0` / `paint` / `gpu` + hitch-thread ms + r↑/cold↓ into #121 Home LOGS |
| **Smoke** | Lab-Rat `probes=off` **and** Hypha `cook_ms` / `defer` |

Stay out of Lab-Rat stamps / Range / Beabim / GATE / Augury Home chrome. Lab-Rat **#130** sandbox pedon is an off-stream leftover overlay — does **not** remesh this STREAM. Pad crawl stays **#114**. See `PEEK_FINDINGS.md` Closed by #123 + `FULCRUMRUST_LAST_PASS_LOCK.md`. Radius + warm hold: Closed by #137.

## Play STREAM 11×11 + warm hold (Hypha #137)

Radius + warm-return layer on #108 / #123 hitch — not a new map size. [PR #137](https://github.com/initialvisuals/fulcrumRust/pull/137) (`4ea0c1e4`; follow-up `a26628a`). Hitch *fix* layers stay #108 / #123. Hitch *visibility* stays Augury #110 / #121 / #128. Dial sheet: fulcrumRust `docs/TERRAIN.md`.

| Lock | Detail |
|------|--------|
| **Window** | `STREAM_RINGS` **5** / **11×11** (was 4 / 9×9). Leading edge **80 m**, not 64 m |
| **Prefetch** | **5 m** face + **walk heading** (reverse included). One cheap lod-3 look-ahead past the hot ring |
| **Hold** | GPU halo `HOLD_RINGS` **2** + CPU TTL `RESIDENT_TTL_SECS` **12** (`hold=2/12`). Return walk promotes / republishes — no extract. Flush / smoke still drop (rim spawn-cold honest). Soft LOD pop OK |
| **Cook / hitch** | Unchanged from #123: cook=1/2 · cook_ms **8/16** · defer=`worker/paint/gpu`. Hole-fill heading-side first. Halo-exit `hold_publish` keeps extract0 / gpu on separate play ticks. TELE MAX ~30 ms apply/queue |
| **Smoke** | `prefetch=5+heading` `hold=2/12` `defer=worker/paint/gpu` |

Stay out of Lab-Rat 7×7 stamp pad / Range / Beabim / Augury Home chrome / #131 biped / #136 landmark ride. See `PEEK_FINDINGS.md` Closed by #137 + `FULCRUMRUST_LAST_PASS_LOCK.md`. Live hold / horizon / desert / soft rim **later landed #151** (`hold=4/16` — do **not** read #137 `hold=2/12` as the live tip).

## 4× world scale + pend coalesce (Hypha #142)

Next ~4× area expand on the #81 host — **not** a STREAM radius bump. [PR #142](https://github.com/initialvisuals/fulcrumRust/pull/142) (`d1eb09df`). Hitch *fix* layers stay #108 / #123. Play STREAM 11×11 + warm hold stay #137. Dial sheet: fulcrumRust `docs/TERRAIN.md`. Rim pads: fulcrumRust `docs/SPAWNS.md`.

| Lock | Detail |
|------|--------|
| **Extract** | **37×37 / 592 m / 350 464 m²** (was #81 **19×19 / 304 m / 92 416 m²**). ~4× area; linear ~1.95×. World rings **9 → 18** (`RING_COUNT = GRID / 2`). Spawn stays origin |
| **Stream (held)** | **11×11** (`STREAM_RINGS` 5 / `r=5`). Prefetch **5+heading** same. Resident hold **2/12** same at ship (live **later landed #151** `hold=4/16`). Cook/hitch **1/2 · 8/16 · defer=worker/paint/gpu** same |
| **Pend coalesce** | Admit **2** / cap **2** (`coalesce=2/2`). Play truncates heading/hole sort so mid-drain does not admit another leading-edge storm. Home SPIKE is `pendΔ ≥ 2`. Motivated by Lab-Rat walk dump max=319.4 ms · warn=15 · spike=4 when pend jumped +8/+16/+18 |
| **GPU concat** | Walk-forward appends new hole-fills. Full rebuild when a leftover leaves the GPU halo or a resident remeshes |
| **Rim spawn** | **144 → 288 m** via `probes::rim_radius_m()` / `GRID_ORIGIN`. Inside `playable_half_m` **295.25**. Smoke `spawns=rim=8`. Beabim / Lab-Rat must not hardcode 144 |
| **Stamp pad** | Still **7×7**. Lab-Rat CHANNELS / pedon left alone |
| **Smoke** | `extract_m2=350464` `rings=18` `prefetch=5+heading` `hold=2/12` `defer=worker/paint/gpu` `coalesce=2/2` `spawns=rim=8` |
| **Leftover** | If seams/empty air at the new rim or on a long sprint, bump `STREAM_RINGS` to 6 / 13×13 **before** cook/hitch. If walk SPIKEs return, lower `PEND_ADMIT` to 1 before growing the window. Flatten / shared-face density not retuned for extra rings. Far-4 / void-past-extract horizon **later landed #151** cheap LOD-3 (`visible=5/19`) + desert floor. Residual soft LOD pop inside a cell still parked |

Stay out of Range feel / AIM TUNE / heat · Beabim net/PVP/HOST (consume `player_spawns` only) · Lab-Rat 7×7 / CHANNELS / pedon · Augury Home chrome. Do **not** claim STREAM_RINGS bumped. See `PEEK_FINDINGS.md` Closed by #142 + `FULCRUMRUST_LAST_PASS_LOCK.md`. STREAM past extract / desert / soft rim **later landed #151**.

## STREAM past extract + desert floor + soft rim (Hypha #151)

Horizon / exterior / hold / rim-hook on the #142 37×37 host — **not** a fine STREAM radius bump. [PR #151](https://github.com/initialvisuals/fulcrumRust/pull/151) (merge `0f6171cf`). Hitch *fix* layers stay #108 / #123. Fine window stays #137 **11×11**. Pend coalesce stays #142 `2/2`. Dial sheet: fulcrumRust `docs/TERRAIN.md`.

| Lock | Detail |
|------|--------|
| **Window (held)** | `STREAM_RINGS` **5** / **11×11**. Leading edge **80 m**. Hitchy cook set held — do **not** claim the fine window grew. `wide` / `resident` grow this |
| **Horizon** | Cheap LOD-3 past extract: `visible=5/19` so the 37×37 yard does not hole (void → coarse floor) |
| **Exterior** | Flat desert skirt `desert=8` / **128 m** (heightfield + skirt mesh; sand stamp hook / height only — no rock lobes). Lab-Rat COL later |
| **Hold** | **2/12 → 4/16** (GPU halo / CPU TTL). Return walk promotes / republishes — no extract. Flush / smoke still drop |
| **`StreamPolicy`** | `window` / `wide` / `resident` via env `FULCRUM_STREAM` or Options Graphics **STREAM**. Wide = r=18 hold=8/30. Resident = whole-extract fine + hold=18/inf (RTX 3060 peek) |
| **Soft rim** | World block at extract+desert (~**422 m**): damp outward vel; spring back; no clip slap. `RimHook` / `Debugger::note_rim` → `RIM APPROACH\|BLOCK\|CLEAR hook=augury` for Augury glasses glitch + radio crackle — do **not** invent Slain chrome |
| **Held** | Prefetch **5+heading** · cook/hitch **1/2 · 8/16 · defer=worker/paint/gpu** · #142 `coalesce=2/2`. Extract still **37×37 / 592 m / 350464 m²**. Stamp pad **7×7** |
| **Smoke** | `hold=4/16` `stream=window` `visible=5/19` `desert=8` `coalesce=2/2` `defer=worker/paint/gpu` `extract_m2=350464` |

Stay out of Lab-Rat 7×7 / CHANNELS / pedon / grit crawl · Range feel / AIM TUNE / heat · Beabim net/PVP/HOST · Augury glasses chrome / Slain rewrite · rock desert / Lab-Rat COL. Residual soft LOD pop inside a cell / live octree still parked. See `PEEK_FINDINGS.md` Closed by #151 + `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust `docs/TERRAIN.md`.

## Texture LOD / compression (Hypha + Lab-Rat, 2026-09-07)

Atelier roughness is **4k 48-bit PNG** — too fat for the yard. Do **not** ship raw 4k 48-bit into extract.

| Seat | Lock |
|------|------|
| **Lab-Rat** | Bake greyscales **down before density** (8-bit / half-res / BC4-style height packs). Quiet grit under loud scars. Wire on fulcrumRust only. **#58 landed** first vendored 256² set (`grit_{grunge,crack,dust}.png`) — the near source for #60. Slope/PBR/dirt/scatter/deform plugs **landed #80**. Atelier **150 roughness + textures/PBR ~26 sets landed**. Whole roughness→stamp cook still separate (SVG / density-mask / experiment-log)
| **Hypha** | LOD-tied mips / compression **landed #60** on Transvoxel **distance rings**. Near **256²** (Lab-Rat #58 vendor) · mid **64²** box mip · far **16²** box mip (cheaper / softer; far drops grain hashes). **#112** `promote_for_uv` + TerrainHost wear/COL honor Lab-Rat #101 `uv::xform` — texture-only, never remesh. In-repo `assets/stamps/grit_*.png` until Lab-Rat cooks more. Smoke `grit_mips=256/64/16 n=196608 f=768`. Near LOD raise **shipped #61**; live underfoot **#81 32/16/8/4**. Grit mips stay 256/64/16. First big-map host **landed #81** (not a grit-mip raise). Live walk extents **#142** 37×37 |
| **Atelier** | Plugs **open** (was read-only). PBR batch **in** (150 roughness + textures/PBR ~26 sets). #58 `FULCRUM_GRIT=` / `FULCRUM_ATELIER=` stay read-only **load** paths |

See `STAMP_FEEL_LOCK.md` + `AESTHETIC_DIEGETIC_LOCK.md` + `FULCRUMRUST_LAST_PASS_LOCK.md`.

## Extract HDRI (Range Tech + desk) — shipped fulcrumRust #40

Evan: one **`.hdr`** day plate (2k–4k). **#40** landed Poly Haven **Goegap** 4k on extract ToD (`engine/assets/hdris/`; atelier raw is fallback). Procedural dome stays when plate off / missing. HDRI stays Range Tech. See `AESTHETIC_DIEGETIC_LOCK.md` + `FULCRUMRUST_LAST_PASS_LOCK.md`.

## Not this shelf

Locus **brains** (Augury) · guns (Range Tech) · CE editor / range levels / web CE. Hypha #88 consumes the #79/#81 heightfield column for pawn plant — not a mesher rewrite, not Augury brains.
