# Terrain north-star (fulcrumRust)

Parked from Evan overnight (2026-09-07). Flat world — **not** a spherical No Man’s Sky planetoid. Feel: Transvoxel / Lengyel-class smooth voxels, semi-detailed near, chunked far (bobgar look-language OK).

## Host (Hypha)

- Transvoxel-style density mesher + chunk LOD / distance
- Eval first: https://transvoxel.org + Lengyel tables
- Rust port candidate: https://github.com/ling0x/transvoxel

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

## Not this shelf

Locus AI (Augury) · guns (Range Tech) · CE editor / range levels / web CE.
