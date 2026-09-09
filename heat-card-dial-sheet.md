# Heat card dial sheet (aim-offset)

Canonical artistic-auth params for barrel heat cards. Steal into MyceliumEngine / Concrete Echo from this sheet, not chat scroll.

**Source:** aim-offset **v77** (`073955d`), hard refresh `app.js?v=20260906v77`  
**Parked:** 2026-09-06 by InitialVisualsAdmin  
**Live fulcrumRust defaults:** Range Tech **#129** CE tip **0.2.8** lock on Hypha **#66** colorless post path (was #71 blend → now CE tip → stolen dump). #71 blend / aim-offset dump stay DNA landmarks — not live. Glasses / live sheet still drive the fields.  
**Sibling:** Vector mag dump (muzzle rect flash / grit / glyphs — live steal **landed #89**) → [`bake-book/VECTOR_MAG_DUMP.md`](bake-book/VECTOR_MAG_DUMP.md). Not heat. Do **not** reopen orange cards.

## Layers
- Master
- Barrel cards
- Ground height-fog (flag ON, strength **0.0** — no fog blob)

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

## fulcrumRust live defaults (Range Tech — landed #129 CE tip 0.2.8)

Range Tech owns heat dials on the Hypha **#66** post path. Live `HeatDials` + post strength/radius are Evan's locked CE tuner from `_CONCRETE_ECHO_` `4_15_26` `barrelHeatCanon.ts` (house-locked 2026-09-09). Past #71 dump-blend. #66 colorless post path stays. #89 projectile feel untouched. Cards do the look; barrel warp at enable floor; **no fog blob**. Tip-anchored lattice DNA stays. No second heat system. No orange card redraw. Glasses / live sheet still drive these fields.

WAS = **#71 blend** (prior live / DNA). STOLEN = aim-offset dump (DNA). NOW = CE tip **0.2.8**.

| dump key | field | was (#71 blend) | now (CE tip 0.2.8) | stolen dump |
|---|---|---:|---:|---:|
| barrelHeat | barrel_heat | 0.05 | **1.0** | 0.05 |
| heatHazeStrength | haze_strength | 0.07 | **0.01** | 0.11 |
| heatHazeGroundStrength | ground_strength | 2.0 | **0.0** | 2.0 |
| heatHazeCardSize | card_size | 0.83 | **0.99** | 0.71 |
| heatHazeCardScaleX | scale_x | 0.396 | **0.28** | 0.20 |
| heatHazeCardScaleY | scale_y | 1.745 | **0.86** | 1.86 |
| heatHazeCardCount | count | 14 | **20** | 14 |
| heatHazeCardSegs | segs | 26 | **32** | 20 |
| heatHazeWind | wind | 1.40 | **1.56** | 1.54 |
| heatHazeFriction | friction | 1.075 | **0.74** | 1.15 |
| heatHazeFeather | feather | 1.585 | **1.90** | 1.55 |
| heatHazeLobeSize | lobe | 0.698 | **0.40** | 0.35 |
| masters / heatGrabSplit | master, barrel_haze, ground_haze, grab_split | true | true | true |

### Post strength + radius (still #66 path)

- **Strength:** `visual * haze`. Haze **0.01** is the enable-floor (subtle warp; #71 remap 0.01→lattice×1.35 was the fog). **0** still kills warp (Options / glasses / live sheet)
- **Radius:** scale/cap **0.40 / 0.08** (muzzle-adjacent; short cards + tight lobe kill the blob). Lattice bbox still anchors. Tip-weighted lattice energy + energy-weighted post UV so the field sits on the can, not a haze cloud
- WGSL `heat_warp_uv` unchanged (sample-only UV displace). Overlay disc lobe stays parked (`HEAT_LOBE_DISCS = 0`)

## Steal notes
- Engine/CE: mirror dials as presentation-only until gameplay needs heat
- Keep bottom-center pin when changing W/H
- fulcrumRust #59 landed the v77 shimmer / lattice crawl + barrel haze RGB above — not static orange blobs. Card geometry DNA on this sheet stays the lock
- fulcrumRust #66 landed the Hypha colorless post path (sample-only `heat_warp_uv`; barrel haze RGB from #59 is feel-lab reference — live fulcrumRust draw is colorless warp)
- fulcrumRust #71 landed the Range Tech dump-dial blend (DNA / prior blend — **not live**). Glasses / live sheet still drive fields. #66 architecture lock stays — do **not** reopen orange cards
- fulcrumRust #89 (Range Tech projectile feel) did **not** retune HeatDials. Heat stays Range dials; vector mag dump stays #89
- fulcrumRust #129 locked live HeatDials to CE tip **0.2.8** (`_CONCRETE_ECHO_` `4_15_26` `barrelHeatCanon.ts`, house-locked 2026-09-09; merge `54c558a`). Cards do the look; barrel warp at enable floor; no fog blob. Past #71 dump-blend. #66 colorless post path stays. #89 projectile feel untouched
