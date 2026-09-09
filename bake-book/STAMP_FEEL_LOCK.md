# World / stamp feel lock (fulcrumRust)

Parked from Evan → Lab-Rat → steal map (PR #3, 2026-09-07).

- **Bake stamps on hub skin:** blend of quiet authored grit + loud organic scars (plume webbing / anastomosis) as readable landmarks
- **Void-spore terraforming:** hellish mushroom / 2D density cracks = Lab-Rat visual DNA for Hypha terrain (PR #20)
- **Locus obsidian veins:** black **obsidian + gold crack veins** — loud-scar stamp material on **Inked / Monk** pads. Pairs with void-spore grit. Distinct from Range Tech kit chrome (gold+black **tech trim**, not gold-plate). **Do not put Locus veins on gun kits** (Initial Visuals Group Chat 2026-09-07)
- Influence is **quiet** (BT black / chiral gold vibe) — **do not name-drop** franchises in shelf, READMEs, or public copy; no pastiche chase.
- **Stamp volume:** stretch **up** into voxels (compounds, ladders/stairs, height extrusions) more than deep tunnel guts
- **World depth:** stay **shallow** unless a compound needs a basement — not a deep tunnel sim
- **Multiple stamps** → height/structure into voxel at rigidize-on-spawn
- **Texture compress (2026-09-07):** atelier roughness packs are **4k 48-bit PNG** — too large. Bake greyscales **down before density** (8-bit / half-res / BC4-style height packs). Do **not** ship raw 4k 48-bit into the yard. **#58 landed** the first bake-down sample set (256² 8-bit-style packs). Quiet grit under loud scars. Atelier plugs **open** (Evan **clean** yell 2026-09-08 ~00:00 ET). Hypha ring-mip texture LOD **landed #60** — see `TERRAIN_NORTHSTAR.md`. **Blender UV dials landed #101** — scale/offset/rotate tiles stamp/PBR/grit without shrinking geo (identity default; `FULCRUM_UV`). Stamp +Y stays AXIS_LOCK
- **First big-map (2026-09-08 / landed #81 + #80):** Hypha walk is **19×19** open. Stamp / harness pad stays **7×7** / far-cold. Slope COL hooks reserved on host (`pbr=tint`) — Hypha #81 vertex albedo only. Lab-Rat slope/PBR/dirt/scatter/deform plugs **landed #80** (DISP bake-down + `Deform` / `GroundScatter` filled at `8,-6` / `-10,14`). NRM/GLOSS GPU parked. Atelier **150 roughness + textures/PBR ~26 sets landed**. See `TERRAIN_NORTHSTAR.md`

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
| **Locus obsidian veins** | Black **obsidian + gold crack veins** on **Inked / Monk** pads — loud-scar stamp, pairs with void-spore grit. Not Range Tech kit chrome. **Veins stay off gun kits** (2026-09-07 group chat). Influence is **quiet** (BT black / chiral gold vibe) — no franchise name-drop / no pastiche chase. |
| **Structures** | Sit-on-surface adds **void-spore bloom** + **brutalist mass** (with #15 set) |
| **Grimdark grade** | `VoxelMaterial::luma` / tint — crushed materials; organic dirt bleed = takeover webs |
| **Consume** | Wear leftovers are solid on density (`> 0`); Hypha grades verts the same way |
| **Ownership** | Lab-Rat stamps + wear leftovers; Hypha meshes + grades; Augury avoids organic / void-spore spawn until growth-enemy pass |

Detail: fulcrumRust `docs/STAMPS.md`. Shipped: Hypha #16 grades verts grimdark + samples wear into chunks. Steal-next: Augury spawn filters prefer rock/concrete.

## Shape-agnostic stamp / paint substrate (PR #38)

Evan direction: stop one-off stamp content (Standard scar, Monk AOE, extra yard silhouettes). Harden the technology so any authored shape converts into density + material, or paint details later. **Not** Transvoxel / Locus AI / guns. Yard plots / Inked hotspot / curl stay consumers.

| Lock | Detail |
|------|--------|
| **Direction** | Shape-agnostic channels — feed a primitive; do not add a `WearKind` / `SurfaceKind` for the next landmark |
| **Convention** | `DensitySample.density`: `> 0` solid, `< 0` air, `0` isosurface (same as Transvoxel consume; Hypha may flip for a port). `material`: dirt / sand / rock / concrete / organic (grimdark tint/luma). Grid: `fill_grid` / `fill_chunk_samples` `ix` fastest, then `iy`, then `iz` |
| **ChannelOp** | Union / Subtract / Paint / Replace (`engine/src/channels.rs`) |
| **Primitives** | sphere / ellipsoid / capsule / box / ribbon / brush / height-mask / mesh / volume. `ChannelStack` ordered compose; `StampField::layers` (authored extras) vs `StampField::content` (compiled consumers). `StampSlot::primitive` on reserved Hypha slots (empty until a shape is fed; `apply_stamp_delta` consumes) |
| **Paint** | `StampField::paint` / `ChannelStack::paint` — writes are real today; brush UX stubbed. `density_delta > 0` puffs solid; `< 0` + Subtract carves; material-only with density 0 on existing solid |
| **Mesh→voxel** | `MeshStamp` → `voxelize_mesh` (step ~0.10–0.25 m, pad) → `SampledVolume` → `stamp_volume` (prefer for compounds); `stamp_mesh` for small live SDF. World meters, Y-up, CCW outside |
| **2D mask** | `Mask2D` → `Primitive::height_mask`; helper `primitive_from_density_2d` — #39 harness applies it on the three existing plots via `StampField::layers` as a shallow anonymous scale test (still not a fourth named plot) |
| **Consumers stay** | Sit-on-surface leftovers (ellipsoids); concrete/void-spore wear (ribbons — prefer capsule for new work); Inked hotspot under `growth::INKED_HOTSPOT`; yard plots + curl **1 / 2 / 3** (still CPU boxes; #39 also writes `primitive_from_density_2d` into `layers`); Hypha reserved StampSlots empty until fed. `sample_channels` / `fill_chunk_samples` still the Hypha consume path |
| **Ownership** | Lab-Rat writes; Hypha remeshes. Out of scope: Transvoxel tables/LOD, Locus AI, guns, 3D paint editor, live carve |

Closed-form feed: `field.stamp(Primitive::…)`. Detail: fulcrumRust `docs/CHANNELS.md`.

## Texture compression — greyscale bake-down (2026-09-07)

Atelier roughness packs are **large** (4k 48-bit PNG). Do **not** ship raw 4k 48-bit into the yard. Lab-Rat owns the bake-down; Hypha owns ring mips. Atelier plugs **open** (Evan **clean** yell 2026-09-08 ~00:00 ET). **#58** is the first landed bake-down sample set (256² 8-bit-style packs) — the near source. Hypha ring-mips **landed #60**. Slope/PBR/dirt/scatter/deform plugs **landed #80**. Atelier **150 roughness + textures/PBR ~26 sets landed**. Whole roughness→stamp cook is **not** done (SVG / density-mask / experiment-log still open).

| Lock | Detail |
|------|--------|
| **Lab-Rat** | Bake greyscales **down before density** — 8-bit / half-res / BC4-style height packs. Quiet grit under loud scars (webbing / mushroom / Inked leftover stay landmarks). Wire on **fulcrumRust only**. **#58 landed** first in-repo set: `assets/stamps/grit_{grunge,crack,dust}.png`. Slope/PBR/dirt/scatter/deform plugs **landed #80** |
| **Hypha** | LOD-tied mips / compression **landed #60** on Transvoxel **distance rings** — grit vs loud scars (near **256²** Lab-Rat vendor; mid **64²**; far **16²** cheaper / softer). See `TERRAIN_NORTHSTAR.md` |
| **Atelier** | Plugs **open** (was read-only). HDRI + PBR batch landed. #58 `FULCRUM_GRIT=` / `FULCRUM_ATELIER=` stay read-only **load** paths. See `ATELIER_PORTFOLIO_STEAL.md` |

Detail: house `AESTHETIC_DIEGETIC_LOCK.md` + `FULCRUMRUST_LAST_PASS_LOCK.md`.

## Quiet grit greyscales (PR #58)

Lab-Rat. Feel lock: quiet authored grit + loud scars now has in-repo vendored height/rough modulators. **Not** a new `WearKind`. Lab-Rat still owns these quiet grit packs under loud scars; Hypha ring-mips **landed #60** on the same packs.

| Lock | Detail |
|------|--------|
| **Ownership** | Lab-Rat. #58 shipped under atelier read-only; plugs **open** 2026-09-08. Env overrides stay read-only load paths |
| **Assets** | Three 256² luma crops in `assets/stamps/` (~83 KB total): `grit_grunge.png` ← atelier `grunge_4.png` · `grit_crack.png` ← `paint cracks.png` · `grit_dust.png` ← `dust and smudge_2.png`. Already bake-down sized — **not** raw 4k 48-bit |
| **Sample** | `engine/src/grit.rs` tiled world-XZ maps (stamp **+Y** height). Yard-weighted; far guts stay heightfield-only |
| **Channels** | `sample_channels` adds quiet height under compiled content so loud void-spore / webbing / Inked scars stay landmarks |
| **Wear** | Hypha vertex wear scale picks up `grit::rough` beside 2D-density cracks / `WearStamp`s |
| **Overrides** | Optional read-only: `FULCRUM_GRIT=` (same filenames) or `FULCRUM_ATELIER=` (local checkout, downsample on load). No submodule. No atelier writes |
| **Smoke** | `grit=vendor` (or `atelier` / `dir` if override) |
| **Out of scope** | Range Tech controller · Augury Locus · Hypha Transvoxel tables · atelier repo writes. Hypha ring-mip texture LOD **landed #60** (this PR owns the quiet near packs only) |

Detail: fulcrumRust `docs/STAMPS.md` + `docs/CHANNELS.md` + `assets/stamps/README.md`.

## Slope/PBR + dirt/scatter/deform plugs (PR #80)

Lab-Rat. Fills the Hypha reserved deform/scatter slots and bakes PBR greyscales down onto the stamp pad. **Not** Hypha vertex COL bind (#81). **Not** NRM/GLOSS GPU. Stamp pad stays **7×7**.

| Lock | Detail |
|------|--------|
| **Slope** | `classify_slope` tags dirt / sand / rock / concrete / organic on the stamp pad |
| **Stamps** | `StampKind::Deform` / `GroundScatter` + `HookKind::LabRatDeform` / `LabRatScatter` at #81 XZ (`8,-6` / 5 m · `-10,14` / 6 m) |
| **PBR bake-down** | 256² greyscale DISP + 64² COL/NRM thumbs (CliffJagged / GroundClay / ConcreteWall / GroundMoss — not 4k 48-bit) |
| **COL hooks** | `pbr::ColHook` / `col_png` / `hypha_col_alias` — Hypha can consume. Lab-Rat does **not** own vertex COL |
| **Dials** | `PBR_HEIGHT_AMP` **0.028** m · `SCATTER_AMP` **0.018** m · `STAMP_PAD_HALF_M` **56** m |
| **Load** | vendored; `FULCRUM_GRIT` then `FULCRUM_ATELIER` (read-only) |
| **Smoke** | `pbr=tint plugs=slope+deform+scatter` + Hypha `gfx=` |
| **Still parked** | NRM/GLOSS GPU · SVG / density-mask / experiment-log · whole roughness→stamp |

Detail: house `TERRAIN_NORTHSTAR.md` + `PEEK_FINDINGS.md` Closed by #80 + fulcrumRust `docs/STAMPS.md`.

## Extract-yard scale harness (PR #39)

Stay **on the extract yard** for what #39 shipped — scale/perf harness for the #38 stamp/paint substrate. Not a bigger world map on that pass. First big-map walk **landed #81**; stamp / harness pad stays **7×7**. Deform/scatter plugs **landed #80**. No Standard / Monk one-off scars. HDRI stays Range Tech.

| Lock | Detail |
|------|--------|
| **Pad** | `growth::yard_bounds` ≈ **110 m²** (baseline before harness ≈ **54 m²**); flatten disk tracks it so plots stay playable |
| **`apply_yard_harness`** | Anonymous SDF lattice + larger paint brushes + 2D-mask convert of the three existing plots through `StampField::layers` (not a fourth named plot) |
| **Near / far** | Near yard stays warm (`bake_guts_warm`). Far guts stay cold (Hypha #23). Harness primitives are near-warm only; smoke fails if a layer center is far. `guts_cold` stayed **140** |
| **Host (#43 / #81)** | Stamp / harness pad stays **7×7** (`STUB_GRID = 7`). Hypha walk is **#81 19×19**. Near pad `yard_m2` ≈ **110** unchanged. Smoke may also show `rings=` / `extract_m2=` |
| **Smoke** | `growth=544 curled=580 stamps=100 structs=55 wears=117 content=173 layers=43 prims=216 yard_m2=110` · `guts_warm=75 guts_cold=140 near_chunk=858 far_chunk=45 terrain_tris=3182`. Baseline: `layers=0 prims≈content yard_m2≈54 guts_warm=32`. Far cheapness holds (`far_chunk < near_chunk`). Growth GPU boxes still under 620 |

Detail: fulcrumRust `docs/CHANNELS.md` + `docs/GROWTH_POC.md` / `docs/STAMPS.md` / `docs/TERRAIN.md`. Stamp / harness pad stays **7×7** (~110 m² / extract-pad **12 544 m²**); Hypha walk is **#81 19×19**.

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
