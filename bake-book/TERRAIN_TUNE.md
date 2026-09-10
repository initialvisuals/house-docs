# Terrain tune (FoW iterator — underfoot + Refresh)

House contract for the live FoW terrain tune panel (2026-09-10). **Holding / locked intent — not shipped.** Steal from this sheet, not chat. Do **not** invent numeric defaults beyond tip-locked dials already named. No invented step ranges. Clerk owns this sheet.

Aim-offset style iterator: dials + **Refresh** / partial remesh. **Not** a full world regen.

## Intent

Live terrain tune panel so Lab-Rat + Hypha can iterate grit / COL / STREAM / horizon without cooking the whole extract again. Refresh bakes the dirty window. Partial remesh is Hypha. Soft RimHook / sand COL already tipped — this iterator **retunes**, it does **not** re-own chrome.

## Peek mode (LOCKED default)

1. **Underfoot + Refresh** first (matches walk feel) — Hypha preference, Lab-Rat OK
2. Ghost cam as second peek

Do **not** flip the default to ghost-first. Ghost is a second peek, not the walk lock.

## Lab-Rat dials (live / ghost / refresh bake)

Grit / COL / UV / rock / desert COL + the refresh bake path. Texture crawl / grit flicker lives here (mips), not on STREAM Options.

| Dial | Tip lock | Note |
|------|----------|------|
| grit tile m · COL mix | named — no new default | Iterator retunes existing grit/COL mix. Step ranges parked until Lab-Rat sheets them |
| `STABLE_LOCUS_RES` | **16** (#152) | Color / wear / COL snap to far-mip loci |
| `MATERIAL_HOLD_M` | **2.5** (#152) | Finer-pack hold past the mesh face. Not STREAM hold |
| `LUMA_GRAIN` | ±**0.08** (#152) | Fine pack may nudge far-locus luma. Promote cannot jump past the cap |
| desert `col` tile | **2.8** (#157) | Vendor `pbr_sand_col` on the #151 skirt |
| skirt quad m | **4** (#157) | Was 8. Vertex paint can show tiles past extract |
| `FULCRUM_UV` scale | existing mips only | #101 / #112 `promote_for_uv`. Scale does not remesh. Do **not** invent a new mip |
| stamp rock lobe count / shade bias | named — no new default | Iterator retunes. Do **not** invent a lobe count here |

Height / DISP stay bilinear (#152). Extra grit still building-faces-only. Chunk metres held. Off STREAM.

## Hypha dials (same panel — need Refresh / partial remesh)

STREAM / horizon / desert rings / prefetch / cook budget + remesh. STREAM Options alone will **not** kill most pop/noise — they only grow fine cook.

| Dial | Tip lock | Note |
|------|----------|------|
| STREAM window / wide / resident | `StreamPolicy` / `FULCRUM_STREAM` | Already tipped on #151. Iterator retunes. Do **not** invent new policy names or presets |
| fine `STREAM_RINGS` | **11×11** (#151) | Fine window held. Wide / resident grow it |
| hold GPU · TTL · coalesce | named — no new default | Iterator retunes the already-tipped hold / coalesce leftover. Do **not** invent a new hold |
| horizon `visible` | **5/19** (#151) | Cheap LOD-3 past extract (void → coarse floor) |
| desert rings | **8** (#151) | Flat desert skirt past extract |
| prefetch / cook budget | hitch vs holes | Iterator retunes the already-tipped cook path. Do **not** invent a new cook default |

## Explicit

- STREAM Options alone won’t kill most pop/noise — only grow fine cook.
- Texture crawl / grit flicker = Lab-Rat mips (#152).
- Soft LOD pop inside a cell still parked.
- Soft RimHook (#151 / #156) / sand COL (#157) already tipped — iterator retunes, does **not** re-own chrome.
- AIM TUNE / Options tip cooks stay Range / Hypha Graphics — not this panel.

## Seat map

| Seat | Owns |
|------|------|
| **Lab-Rat** | grit/COL/UV/rock/desert COL dials + refresh bake path |
| **Hypha** | STREAM/horizon/desert rings/prefetch/cook budget + remesh |
| **Range / Augury / Beabim** | Off |
| **Clerk** | This sheet |

## Parked

- Invented step ranges until Lab-Rat sheets them.
- Soft LOD pop inside a cell.
- AIM TUNE / Options tip cooks.
- Full world regen. This panel is Refresh / partial remesh only.
- New numbers beyond the tip locks named above.

See `PEEK_FINDINGS.md` Holding / locked intent — terrain tune iterator. Overnight cooks steal from this sheet + fulcrumRust `docs/TERRAIN.md` + `docs/STAMP_PBR_DIAL_SHEET.md`.
