# World / stamp feel lock (fulcrumRust)

Parked from Evan → Lab-Rat → steal map (PR #3, 2026-09-07).

- **Bake stamps on hub skin:** blend of quiet authored grit + loud organic scars (plume webbing / anastomosis) as readable landmarks
- **Void-spore terraforming:** hellish mushroom / 2D density cracks = Lab-Rat visual DNA for Hypha terrain (PR #20)
- **Stamp volume:** stretch **up** into voxels (compounds, ladders/stairs, height extrusions) more than deep tunnel guts
- **World depth:** stay **shallow** unless a compound needs a basement — not a deep tunnel sim
- **Multiple stamps** → height/structure into voxel at rigidize-on-spawn

## Smart material stamps + sit-on-surface structures (PR #15)

First Lab-Rat voxel-world slice. **Not** a 3D paint editor. **Not** Hypha chunk/LOD/mesher. Growth yard + curl **1 / 2 / 3** unchanged.

| Lock | Detail |
|------|--------|
| **Materials** | Rule-based **dirt / sand / rock / concrete / organic** on **8 m** cells |
| **Rules** | Yard → organic; perimeter lip → concrete; spawn pad → dirt; steep / high stub-height → rock; far flat + hash → sand; leftover peaks → organic bleed or ruin concrete |
| **Structures** | Sit-on-surface PoC: mushroom cap, anastomosis web, rock outcrop, concrete lip, sand ripple, grit block |
| **Skip** | Growth yard + spawn pad overlays so plots stay readable |
| **Append** | Stamps append after existing bake — Hypha grayboxes keep indices |
| **Host** | `VoxelHost` — **Hypha #16** `TerrainHost` is the live heightfield + mesher |
| **Glasses** | Off yard: `DIRT  STAMP` / `ROCK  STAMP` / … (thin analysis-knowledge-core; labels only) |
| **Seed** | `FULCRUM_SEED` feeds extract bake + stamp field |

## Density + material consume channels (PR #17)

Evan lock: terrain look is **Transvoxel** (seamless LOD). Lab-Rat does **not** own the mesher or Lengyel tables.

| Lock | Detail |
|------|--------|
| **API** | `sample_channels` / `fill_chunk_samples` expose signed density + `VoxelMaterial` |
| **Density sign** | `> 0` solid, `< 0` air, `0` isosurface (Hypha may flip for port) |
| **Grid order** | `fill_chunk_samples`: `ix` fastest, then `iy`, then `iz` |
| **Ownership** | Hypha hosts Transvoxel + far-chunk simplify; Lab-Rat only stamps + channels |
| **Peek leftover** | CPU boxes stay readable; consume path is the sample channels |

Shipped: Hypha #16 `TerrainHost` + crates.io `transvoxel` 2.0 samples channels into chunks. Steal-next: live LOD recook / tunnel cutouts; Augury spawn filters prefer rock/concrete, avoid organic. Detail: fulcrumRust `docs/STAMPS.md` + `docs/TERRAIN.md`.


## Void-spore terraforming + density-driven wear (PR #20)

Lab-Rat visual DNA for Hypha terrain. FoW / post-apoc grimdark — hellish void spores, not cute mushrooms. **Not** a mesher.

| Lock | Detail |
|------|--------|
| **2D density stamp** | Shared `growth::density_stamp_2d` — veins + anastomosis rings + grit + spore core (yard + wear driver) |
| **Yard silhouettes** | Void-spore 2D webbing / hellish mushroom / spore-tipped creeper; **fourth scar under Inked** (`INKED_HOTSPOT`, not a new plot); curl **1 / 2 / 3** unchanged (Inked pad shares the 2D field) |
| **Concrete wear** | `WearKind::ConcreteCrack` / `ConcreteEdge` from the 2D field onto brutalist perimeter masses |
| **Void-spore bleed** | `WearKind::VoidSporeWeb` + `VoidSporeBloom` on organic cells (terraforming volume); **`VoidSporeCrack`** on the Inked pad |
| **Inked AOE hotspot** | Pinned `VoidSporeWeb` + `VoidSporeCrack` at `growth::INKED_HOTSPOT` **(−5.10, 0, 8.20)** / reach **1.55**; denser/louder than quiet 2D grit; Lab-Rat leftover, not Augury disc |
| **Structures** | Sit-on-surface adds **void-spore bloom** + **brutalist mass** (with #15 set) |
| **Grimdark grade** | `VoxelMaterial::luma` / tint — crushed materials; organic dirt bleed = takeover webs |
| **Consume** | Wear leftovers are solid on density (`> 0`); Hypha grades verts the same way |
| **Ownership** | Lab-Rat stamps + wear leftovers; Hypha meshes + grades; Augury avoids organic / void-spore spawn until growth-enemy pass |

Detail: fulcrumRust `docs/STAMPS.md`. Shipped: Hypha #16 grades verts grimdark + samples wear into chunks. Steal-next: Augury spawn filters prefer rock/concrete.

## Near-spawn yard silhouette fidelity (PR #13)

Peeks must read **growth**, not graybox slabs. Same three plots / cycle / curl binds:

| Plot | Silhouette lock |
|------|-----------------|
| **2D STAMP** | Short-segment glowing webbing, slightly broken anastomosis rings, quiet grit blotches, spore core (flat overlay) |
| **ORGANIC 3D** | Thin bent stem + volva, wide cap (gills/dome), side fruit, plume webbing — mushroom, not a brick pillar |
| **CREEPER** | Low olive tubes on meandering tendrils with forks; soil-hugging anastomosis; short AABB steps so diagonals stay tubes |

CPU boxes, no collide; mesh under existing growth buffers. **Fourth leftover (not a plot):** loud ink/void scar under Inked at `INKED_HOTSPOT`. Detail lives in fulcrumRust `docs/GROWTH_POC.md`.

## Curl on growth plots (PR #9)

Stand on a yard plot (2D stamp / organic / creeper) **or the Inked scar**:
- **1** gas wilt
- **2** freeze stiffen → crack-back
- **3** burn char / recede

Per-plot fields; growth recovers after envelope. The Inked hotspot **shares the 2D stamp field** (webbing OR Inked pad wilt the same AOE; remnants stay — not a softlock). Glasses toast names the field (labels only — not ammo HUD). Binds do not steal H / LMB / Tab.

Source of truth: https://github.com/initialvisuals/fulcrumRust/blob/main/docs/STEAL_MAP.md
