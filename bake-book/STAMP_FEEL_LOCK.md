# World / stamp feel lock (fulcrumRust)

Parked from Evan → Lab-Rat → steal map (PR #3, 2026-09-07).

- **Bake stamps on hub skin:** blend of quiet authored grit + loud organic scars (plume webbing / anastomosis) as readable landmarks
- **Stamp volume:** stretch **up** into voxels (compounds, ladders/stairs, height extrusions) more than deep tunnel guts
- **World depth:** stay **shallow** unless a compound needs a basement — not a deep tunnel sim
- **Multiple stamps** → height/structure into voxel at rigidize-on-spawn

## Near-spawn yard silhouette fidelity (PR #13)

Peeks must read **growth**, not graybox slabs. Same three plots / cycle / curl binds:

| Plot | Silhouette lock |
|------|-----------------|
| **2D STAMP** | Short-segment glowing webbing, slightly broken anastomosis rings, quiet grit blotches, spore core (flat overlay) |
| **ORGANIC 3D** | Thin bent stem + volva, wide cap (gills/dome), side fruit, plume webbing — mushroom, not a brick pillar |
| **CREEPER** | Low olive tubes on meandering tendrils with forks; soil-hugging anastomosis; short AABB steps so diagonals stay tubes |

CPU boxes, no collide; mesh under existing growth buffers. Detail lives in fulcrumRust `docs/GROWTH_POC.md`.

## Curl on growth plots (PR #9)

Stand on a yard plot (2D stamp / organic / creeper):
- **1** gas wilt
- **2** freeze stiffen → crack-back
- **3** burn char / recede

Per-plot fields; growth recovers after envelope. Glasses toast names the field (labels only — not ammo HUD). Binds do not steal H / LMB / Tab.

Source of truth: https://github.com/initialvisuals/fulcrumRust/blob/main/docs/STEAL_MAP.md
