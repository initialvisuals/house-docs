# Terrain north-star (fulcrumRust)

Parked from Evan overnight (2026-09-07). Flat world — **not** a spherical No Man’s Sky planetoid. Feel: Transvoxel / Lengyel-class smooth voxels, semi-detailed near, chunked far (bobgar look-language OK). Lab-Rat #38 ships the **shape-agnostic stamp / paint substrate** Hypha consumes — any authored shape → density + material; not more one-off scars. Lab-Rat #39 is the **extract-yard scale harness** for that substrate.

## Morning lock (2026-09-07)

Evan: **stay on the extract yard** — refine + expand it as a **scale / perf testbed**. Lab-Rat #39 `apply_yard_harness` is that test (`growth::yard_bounds` ≈ **110 m²**; flatten disk tracks it). Stamp/paint substrate (density + material channels, shape-agnostic) over one-off scars. Mesh shapes OK to play with. Bigger world-gen later. HDRI stays Range Tech.

## Host (Hypha) — shipped fulcrumRust #16

First Transvoxel extract terrain host (flat world, not a planetoid). Bake-once at deploy.

| Lock | Detail |
|------|--------|
| **Crate** | crates.io **`transvoxel` 2.0** (`Gnurfos/transvoxel_rs`, Lengyel tables) — not a paste into Lab-Rat |
| **Host** | `TerrainHost` implements Lab-Rat `VoxelHost`; `stamp_field` + `sample_channels` feed density + `VoxelMaterial` |
| **Distance LOD** | center subdiv **16**, ring-1 subdiv **8**, outer subdiv **4** + Lengyel transition faces toward finer neighbours |
| **Skin** | verts grade from `VoxelMaterial::tint` / `luma`; cracks / edge-wear / void-spore scale from Lab-Rat `density_stamp_2d` + `WearStamp` |
| **Atmosphere** | darker clear + colder dual lights + cheap distance haze in `fs_world` (hideout stays unfogged) |
| **Hooks** | sit-on-surface structures stay; `AuguryLocusSpawn` reserved on a rise |
| **Not day-one** | live LOD recook · tunnel cutouts · runtime carve · globe |
| **Far guts (#23)** | Shared Locus `ACTIVATE_M`/`SLEEP_M`; far stamp guts + growth/Locus upload stay cold. **#39** near harness pad stays warm |

North-star refs still hold: https://transvoxel.org + Lengyel · [bobgar demo](https://bobgar.itch.io) look-language · ling0x as swap candidate (not vendored). Detail: fulcrumRust `docs/TERRAIN.md`.


## Distance activation / far-guts cold (Hypha #23)

Hardens extract cost so far chunks stay cheap — aligned with Augury Locus far-cold. Reuses #16 `TerrainHost` (no mesher rebuild). CE labyrinth DNA only (not a web port).

| Lock | Detail |
|------|--------|
| **Shared dials** | `ACTIVATE_M` **24** / `SLEEP_M` **32** — same hysteresis as Augury Locus (`activation.rs` asserts equality) |
| **Bake rings** | Match Transvoxel LOD 0/1/2; far rings skip stamp-structure / wear density consume + per-vert wear walk |
| **Far extract bake** | Stamp plates / structures / wear stay out (collide boxes still land); far crates/poles skipped; brutalist compounds stay for horizon |
| **Live cold** | Growth + Locus GPU uploads skip past `ACTIVATE_M`; yard Idle still visible; cycle/curl keep ticking. **#39** near yard (harness pad ≈ **110 m²**) stays warm (`bake_guts_warm`); harness primitives are near-warm only |
| **Smoke peek** | #23: `near_chunk=862` · `far_chunk=45` · `guts_warm=17` · `guts_cold=140` · `terrain_tris=3168` (~19× cheaper far mean). **#39 harness:** `layers=43` · `prims=216` · `yard_m2=110` · `guts_warm=75` · `guts_cold=140` · `near_chunk=858` · `far_chunk=45` · `terrain_tris=3182`. Far cheapness holds (`far_chunk < near_chunk`) |

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

## Extract HDRI (Range Tech + desk)

Evan: one **`.hdr`** day plate today (2k–4k). Drop in `atelier/hdris/` — **not** the 1k texture dump. Procedural sky stays until Range Tech wires ToD.

## Not this shelf

Locus AI (Augury) · guns (Range Tech) · CE editor / range levels / web CE.
