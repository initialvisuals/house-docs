# Heat card dial sheet (aim-offset)

Canonical artistic-auth params for barrel heat cards. Steal into MyceliumEngine / Concrete Echo from this sheet, not chat scroll.

**Source:** aim-offset **v77** (`073955d`), hard refresh `app.js?v=20260906v77`  
**Parked:** 2026-09-06 by InitialVisualsAdmin  
**Live fulcrumRust defaults:** Range Tech **#71 blend** on Hypha **#66** colorless post path (was → now → stolen). v77 / later aim-offset dump stay DNA. Glasses / live sheet still drive the fields.

## Layers
- Master
- Barrel cards
- Ground height-fog (ground still default **OFF**)

## Strengths (split)
- **Barrel warp** — cards + lobe
- **Ground haze** — separate from barrel
- **Barrel haze RGB** (v77 look, landed fulcrumRust #59) — `1.0 / lerp(0.14,0.70,h) / lerp(0.025,0.16,h²)` — feel-lab reference. Live fulcrumRust draw is Hypha colorless post UV warp (**landed #66**) — not an orange world card

## Card geometry
- **Card size** — remapped **0.05–2.50** (low end = thin ribbon)
- **Card width / Card height** — pinned at **bottom-center** on the tube
- **Card count** — **0–20**, tip-weighted scatter
- **Slice count** — **4–32** (default **16**)
- **Feather** — outer → inner core

## Motion / trail
- **Wind / Friction** — upper trail on swing (Unity trail-renderer vibe)
- **Shimmer / lattice** — v77 `updateBarrelHeatCardMorph` upward shimmer / lattice crawl (landed fulcrumRust #59)

## Lobe
- **Lobe size** — independent muzzle circle (seated on tip)

## Persist
- Copy-settings persists all of the above (artistic authorization → solidify defaults)

## fulcrumRust live defaults (Range Tech — landed #71)

Range Tech owns heat dials on the Hypha **#66** post path. Defaults sit **between** the previous fulcrum bake (`was`) and Evan's later aim-offset dump (`stolen`). Intent: organic gas, less cartoony/wobbly. Tip-anchored lattice DNA stays. No second heat system. No orange card redraw. Glasses / live sheet still drive these fields.

| dump key | field | was | now (blended) | stolen | blend |
|---|---|---:|---:|---:|---|
| barrelHeat | barrel_heat | 0.05 | 0.05 | 0.05 | identical |
| heatHazeStrength | haze_strength | 0.01 | **0.07** | 0.11 | 60% toward dump |
| heatHazeGroundStrength | ground_strength | 2.0 | 2.0 | 2.0 | identical |
| heatHazeCardSize | card_size | 1.01 | **0.83** | 0.71 | 60% toward dump |
| heatHazeCardScaleX | scale_x | 0.69 | **0.396** | 0.20 | 60% toward dump |
| heatHazeCardScaleY | scale_y | 1.63 | **1.745** | 1.86 | midpoint |
| heatHazeCardCount | count | 14 | 14 | 14 | identical |
| heatHazeCardSegs | segs | 31 | **26** | 20 | midpoint |
| heatHazeWind | wind | 1.26 | **1.40** | 1.54 | midpoint |
| heatHazeFriction | friction | 1.0 | **1.075** | 1.15 | midpoint |
| heatHazeFeather | feather | 1.62 | **1.585** | 1.55 | midpoint |
| heatHazeLobeSize | lobe | 1.22 | **0.698** | 0.35 | 60% toward dump |
| masters / heatGrabSplit | master, barrel_haze, ground_haze, grab_split | true | true | true | identical |

### Post strength + radius (still #66 path)

- **Strength:** at dial **0.01** keep lattice amp; at **0.11** use visual × 0.11; default **0.07** lands 60% toward quieter dump; **0** still kills warp (Options / glasses / live sheet)
- **Radius:** `card_size` + `lobe` pull scale/cap from **0.65 / 0.18** toward **0.50 / 0.12**; lattice bbox still anchors
- WGSL `heat_warp_uv` unchanged (sample-only UV displace). Overlay disc lobe stays parked (`HEAT_LOBE_DISCS = 0`)

## Steal notes
- Engine/CE: mirror dials as presentation-only until gameplay needs heat
- Keep bottom-center pin when changing W/H
- fulcrumRust #59 landed the v77 shimmer / lattice crawl + barrel haze RGB above — not static orange blobs. Card geometry DNA on this sheet stays the lock
- fulcrumRust #66 landed the Hypha colorless post path (sample-only `heat_warp_uv`; barrel haze RGB from #59 is feel-lab reference — live fulcrumRust draw is colorless warp)
- fulcrumRust #71 landed the Range Tech dump-dial blend (live defaults above). Glasses / live sheet still drive fields. #66 architecture lock stays — do **not** reopen orange cards
