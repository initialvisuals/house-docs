# Overnight brief (2026-09-08)

Parked from Evan first big-map brief; clerk shelf cook refreshes this pulse.

## Direction

- **First true big map** — extract Transvoxel: higher res, drop outer walls, extend **~8×**, chunk the voxel, load chunks by distance from players (listen-server aware). See `TERRAIN_NORTHSTAR.md`. **Brief only — not shipped.**
- **Lab-Rat stamps** — slope/angle materials, dirt/scatter/deform, PBR bake-down. Atelier **150 roughness + textures/PBR ~26 sets landed**; plugs wait for Evan **clean** yell
- **Range Tech** — kits + FX draw-distance on the wider yard; store `dBXpg` after clean
- **Augury** — menu video bg / brand after clean
- **Reuse** — #16 host / #23 far-cold / #43 7×7 / **#61 32/16/4** / #60 grit mips stay the live extract; do not rebuild from zero

## Landed on main overnight (clerk pulse)

| Seat | Shipped |
|------|--------|
| **Range Tech** | #22 SR-25/M24 · #24 day/night+sky · #25 wall lean · #28 hold-` inspect · **#62 atelier SFX** |
| **Hypha** | #16 Transvoxel host · #23 far-guts cold · #24 sky lights (with Range) · **#43 7×7 radius** · **#60 grit mips** · **#61 32/16/4** |
| **Augury** | #18 Locus Standard · #26 Locus Inked |
| **Lab-Rat** | #20 void-spore + concrete wear · #38 stamp/paint substrate · #39 yard harness · **#58 quiet grit** |
| **Clerk** | CREDITS planted in-PR; shelf #43/#58/#60/#61/#62 dials into bake-book |

## Still cooking

| Seat | Open |
|------|------|
| **Hypha** | **First big-map brief** (2026-09-08) — **not shipped**. Live remains #43 **7×7 / 3 rings / 112 m / 12 544 m²** + near LOD **32/16/4** (#61) + #60 mips. Owns: drop outer walls · **~8×** extend · chunked Transvoxel · **load chunks by distance from players** (listen-server aware). **#46 Options guts + #55 GPU post landed** (AO/AA/CA/grain/DoF; smoke `post=aa`; not full bloom/god-ray). Menus/settings chrome stays Augury |
| **Lab-Rat** | Slope/angle materials · dirt/scatter/deform · PBR bake-down. Atelier PBR batch **in**; plugs wait for Evan **clean** yell. #58/#60 stay the only yard plugs until then |
| **Augury** | FoW title/main menu layout + settings clone cooking (clone FoW OG; #41 title mark already landed) — **not done**. Menu video bg / brand **after clean**. FoW OG input manager in scope |
| **Range Tech** | Quality/flag options on the #42 `build.bat` still cooking / open. Kits + FX draw-distance retune on the wider yard. Store `dBXpg` after clean. **Embodied feel pass landed #57** / **Evan peek landed #59** / **#62 SFX vendor landed** |

Deliberately still out: CE editor, shooting-range levels, web CE, live pycelium mesocosm on hot path. Do **not** claim the big map shipped.

Source of truth: `docs/STEAL_MAP.md` in fulcrumRust + this shelf.
