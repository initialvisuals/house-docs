# Heat card dial sheet (aim-offset)

Canonical artistic-auth params for barrel heat cards. Steal into MyceliumEngine / Concrete Echo from this sheet, not chat scroll.

**Source:** aim-offset **v77** (`073955d`), hard refresh `app.js?v=20260906v77`  
**Parked:** 2026-09-06 by InitialVisualsAdmin

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

## Steal notes
- Engine/CE: mirror dials as presentation-only until gameplay needs heat
- Keep bottom-center pin when changing W/H
- fulcrumRust #59 landed the v77 shimmer / lattice crawl + barrel haze RGB above — not static orange blobs. Card geometry dials on this sheet stay the lock
- fulcrumRust #66 landed the Hypha colorless post path (sample-only `heat_warp_uv`; card geometry dials on this sheet remain the lock; barrel haze RGB from #59 is feel-lab reference — live fulcrumRust draw is colorless warp)
