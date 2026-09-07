# Terrain north-star (fulcrumRust)

Parked from Evan overnight (2026-09-07). Flat world — **not** a spherical No Man’s Sky planetoid. Feel: Transvoxel / Lengyel-class smooth voxels, semi-detailed near, chunked far (bobgar look-language OK).

## Host (Hypha)

- Transvoxel-style density mesher + chunk LOD / distance
- Eval first: https://transvoxel.org + Lengyel tables
- Rust port candidate: https://github.com/ling0x/transvoxel
- Look language: [bobgar Transvoxel demo](https://bobgar.itch.io)
- **Hypha owns the mesher** (regular/transition cells, LOD, table lookup). Do not paste Lengyel tables into Lab-Rat.

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

- https://github.com/sjoerdev/voxel-engine
- https://github.com/DXGatech/Smooth-Infinite-Voxel-Terrain
- https://github.com/bw2012/UnrealSandboxTerrain
- https://github.com/qwertzui11/voxelTerrain

Reuse week-one concrete/dirt/sand DNA where it fits. Prefer one solid host over parallel rebuilds.

## Stamps (Lab-Rat) — fulcrumRust #15

Organic voxel surface structures + smart-material tags onto Hypha’s density field. Not a 3D paint editor.

- **Materials:** dirt / sand / rock / concrete / organic on **8 m** cells (rule-based)
- **Structures:** sit-on-surface mushroom / web / rock / lip / ripple / grit (skip yard + spawn)
- **Host handoff:** Lab-Rat ships `VoxelHost` stub + `classify` / `stamp_field`; Hypha implements real heightfield + meshed stamped cells + LOD
- Detail: fulcrumRust `docs/STAMPS.md` + house `STAMP_FEEL_LOCK.md`

## Void-spore + wear leftovers (Lab-Rat #20)

Visual DNA for Hypha’s Transvoxel grade — still not a mesher.

- Shared `density_stamp_2d` drives yard silhouettes **and** concrete crack / edge-wear
- Wear leftovers (`ConcreteCrack` / `ConcreteEdge` / `VoidSporeWeb` / `VoidSporeBloom`) write into density + material channels
- Keep `classify` + `stamp_field` + `density_stamp_2d` wear when swapping real `VoxelHost`
- Grade verts grimdark via `VoxelMaterial::tint` / `luma`; brutalist masses are the upward scale target
- Hypha eval pile (sjoerdev / DXGatech / UnrealSandboxTerrain / qwertzui11) stays host DNA — Lab-Rat does not own tables

## Not this shelf

Locus AI (Augury) · guns (Range Tech) · CE editor / range levels / web CE.
