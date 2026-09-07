# Terrain north-star (fulcrumRust)

Parked from Evan overnight (2026-09-07). Flat world — **not** a spherical No Man’s Sky planetoid. Feel: Transvoxel / Lengyel-class smooth voxels, semi-detailed near, chunked far (bobgar look-language OK).

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

North-star refs still hold: https://transvoxel.org + Lengyel · [bobgar demo](https://bobgar.itch.io) look-language · ling0x as swap candidate (not vendored). Detail: fulcrumRust `docs/TERRAIN.md`.

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
- Wear leftovers (`ConcreteCrack` / `ConcreteEdge` / `VoidSporeWeb` / `VoidSporeBloom`) write into density + material channels
- Keep `classify` + `stamp_field` + `density_stamp_2d` wear on the live `TerrainHost`
- **Hypha #16** grades verts grimdark via `VoxelMaterial::tint` / `luma`; brutalist masses are the upward scale target
- Hypha eval pile (sjoerdev / DXGatech / UnrealSandboxTerrain / qwertzui11) stays host DNA — Lab-Rat does not own tables

## Not this shelf

Locus AI (Augury) · guns (Range Tech) · CE editor / range levels / web CE.
