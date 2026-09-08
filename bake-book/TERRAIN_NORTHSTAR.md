# Terrain north-star (fulcrumRust)

Parked from Evan overnight (2026-09-07). Flat world — **not** a spherical No Man’s Sky planetoid. Feel: Transvoxel / Lengyel-class smooth voxels, semi-detailed near, chunked far (bobgar look-language OK). Lab-Rat #38 ships the **shape-agnostic stamp / paint substrate** Hypha consumes — any authored shape → density + material; not more one-off scars. Lab-Rat #39 is the **extract-yard scale harness** for that substrate.

## Morning lock (2026-09-07)

Evan: **stay on the extract yard** — refine + expand it as a **scale / perf testbed**. Lab-Rat #39 `apply_yard_harness` is that test (`growth::yard_bounds` ≈ **110 m²**; flatten disk tracks it). Stamp/paint substrate (density + material channels, shape-agnostic) over one-off scars. Mesh shapes OK to play with. Bigger world-gen later. HDRI stays Range Tech.

**Wider extract chunk radius shipped #43** — `TerrainHost` **7×7 / 3 Chebyshev rings / 112 m span / ~12.5k m²** (was 5×5 / 2 rings / 80 m / 6 400 m²); one extra **far** ring only. **Near LOD raise shipped #61** — center subdiv **32** / ring-1 **16** / outer **4** (was 16/8/4). Grid/radius stay #43. Stay on extract yard — not a bigger world map.

## Host (Hypha) — shipped fulcrumRust #16

First Transvoxel extract terrain host (flat world, not a planetoid). Bake-once at deploy.

| Lock | Detail |
|------|--------|
| **Crate** | crates.io **`transvoxel` 2.0** (`Gnurfos/transvoxel_rs`, Lengyel tables) — not a paste into Lab-Rat |
| **Host** | `TerrainHost` implements Lab-Rat `VoxelHost`; `stamp_field` + `sample_channels` feed density + `VoxelMaterial` |
| **Distance LOD** | center subdiv **32**, ring-1 subdiv **16**, outer subdiv **4** + Lengyel transition faces toward finer neighbours (**#61**; was 16/8/4). Near step **2:1** (32→16). Radius **unchanged** by #61 |
| **Grid / radius (#43)** | `TerrainHost` **7×7** / 3 Chebyshev rings / 112 m / **12 544 m²** (was 5×5 / 2 rings / 80 m / 6 400 m²); extra **far** ring only |
| **Skin** | verts grade from `VoxelMaterial::tint` / `luma`; cracks / edge-wear / void-spore scale from Lab-Rat `density_stamp_2d` + `WearStamp` |
| **Atmosphere** | darker clear + colder dual lights + cheap distance haze in `fs_world` (hideout stays unfogged) |
| **Hooks** | sit-on-surface structures stay; `AuguryLocusSpawn` reserved on a rise |
| **Not day-one** | live LOD recook · tunnel cutouts · runtime carve · globe. Near LOD raise **shipped #61**; wider radius shipped #43 |
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

Near yard stays the extract pad (expanded harness, not a bigger world map). Steal map: Hypha chunk-LOD row + Augury enemy-activation notes. Detail: fulcrumRust `docs/TERRAIN.md` + `LOCUS_AI_LOCK.md`.

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

`ChannelOp`: Union / Subtract / Paint / Replace. `StampField::layers` (authored extras) vs `StampField::content` (compiled consumers: sit-on-surface, wear, Inked hotspot, yard/curl). Hypha `sample_channels` / `fill_chunk_samples` unchanged. Lab-Rat writes; Hypha remeshes.

Detail: fulcrumRust `docs/CHANNELS.md` + house `STAMP_FEEL_LOCK.md`.

## Extract-yard scale harness (Lab-Rat #39)

Stay **on the extract yard**. `apply_yard_harness` is the perf/scale test of the #38 substrate — not a bigger world map. No Standard / Monk one-off scars. HDRI stays Range Tech.

| Lock | Detail |
|------|--------|
| **Pad** | `growth::yard_bounds` ≈ **110 m²** (baseline before harness ≈ **54 m²**); flatten disk tracks it so plots stay playable |
| **Writes** | Anonymous SDF lattice + larger paint brushes + 2D-mask convert of the three existing plots through `StampField::layers` (not a fourth named plot) |
| **Near / far** | Near yard stays warm (`bake_guts_warm`). Far guts stay cold (#23). Harness primitives near-warm only; smoke fails if a layer center is far. `guts_cold` stayed **140** |
| **Smoke** | keys `layers=` `prims=` `yard_m2=` · `layers=43` · `prims=216` · `yard_m2=110` · `guts_warm=75` · `guts_cold=140` · `near_chunk=858` · `far_chunk=45` · `terrain_tris=3182`. Baseline: `layers=0 prims≈content yard_m2≈54 guts_warm=32`. Far cheapness holds (`far_chunk < near_chunk`). Growth GPU boxes still under 620 |

Detail: fulcrumRust `docs/CHANNELS.md` + `docs/GROWTH_POC.md` / `docs/TERRAIN.md`.

## Wider extract chunk radius (Hypha #43)

Shipped the clerk lock: **wider chunk radius first**. Stay on the extract yard — not a bigger world map. Extra **far** ring only. Near LOD raise **shipped later as #61**.

| Lock | Detail |
|------|--------|
| **Grid** | `TerrainHost` **5×5 → 7×7** (smallest honest odd widen) |
| **Playable extract** | **3 Chebyshev rings / 112 m span / 12 544 m²** (was 2 rings / 80 m / 6 400 m²) |
| **Near LOD** | Unchanged *by #43*: then 16/8/4. **#61 shipped** the raise: **32/16/4** |
| **Far-cold** | Still `lod >= 2` → heightfield-only; shares Locus `ACTIVATE_M` **24** / `SLEEP_M` **32** |
| **Lab-Rat stub** | `ExtractStubHost` aligned (`STUB_GRID = 7`) |
| **Smoke peek** | `near_chunk=858 far_chunk=39 guts_warm=75 guts_cold=216 rings=3 extract_m2=12544 yard_m2=110 locus_hp=24 terrain_tris=4034 lods=3`. Far mean ~**22×** cheaper than near; extra far ring added cold guts; yard pad + Locus stay |

Stay out of Atelier / HDRI / title mark. No new named scars. Detail: fulcrumRust `docs/TERRAIN.md`.

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
| **Parked** | Live LOD recook · tunnels · runtime carve |

Stay out of Range Tech guns / Augury brains / Lab-Rat stamp baking. Detail: fulcrumRust `docs/TERRAIN.md`.

## Texture LOD / compression (Hypha + Lab-Rat, 2026-09-07)

Atelier roughness is **4k 48-bit PNG** — too fat for the yard. Do **not** ship raw 4k 48-bit into extract.

| Seat | Lock |
|------|------|
| **Lab-Rat** | Bake greyscales **down before density** (8-bit / half-res / BC4-style height packs). Quiet grit under loud scars. Wire on fulcrumRust only. **#58 landed** first vendored 256² set (`grit_{grunge,crack,dust}.png`) — the near source for #60. Whole roughness→stamp cook still separate |
| **Hypha** | LOD-tied mips / compression **landed #60** on Transvoxel **distance rings**. Near **256²** (Lab-Rat #58 vendor) · mid **64²** box mip · far **16²** box mip (cheaper / softer; far drops grain hashes). Atelier **read-only** (`assets/stamps/grit_*.png`). Smoke `grit_mips=256/64/16 n=196608 f=768`. Near LOD raise **shipped #61** (subdivs 32/16/4); grit mips stay 256/64/16 on the same rings |
| **Atelier** | Still **read-only** for crew writes while Evan pushes |

See `STAMP_FEEL_LOCK.md` + `AESTHETIC_DIEGETIC_LOCK.md` + `FULCRUMRUST_LAST_PASS_LOCK.md`.

## Extract HDRI (Range Tech + desk) — shipped fulcrumRust #40

Evan: one **`.hdr`** day plate (2k–4k). **#40** landed Poly Haven **Goegap** 4k on extract ToD (`engine/assets/hdris/`; atelier raw is fallback). Procedural dome stays when plate off / missing. HDRI stays Range Tech. See `AESTHETIC_DIEGETIC_LOCK.md` + `FULCRUMRUST_LAST_PASS_LOCK.md`.

## Not this shelf

Locus AI (Augury) · guns (Range Tech) · CE editor / range levels / web CE.
