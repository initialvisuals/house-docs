# Patch B1 catch-up (Clerk · 2026-09-16)

Shelf backlog after antigravity tip + staff breakout. **Docs only.** Steal tip SHAs / dials from fulcrumRust — do not invent numbers.

Tip at catch-up: `d08042e` (Escape / online PVPVE·PVE) on `origin/main`. Master seed bake: `c1341c7`.

## Landed on tip (mark shelf)

| Slice | Tip note | Steal |
|-------|----------|-------|
| **Master world seed** | `MASTER_WORLD_SEED` `0x7A4C_8E19_3D5B_6F02` — HOST+join same bake; random re-seed parked | `engine/src/lib.rs` · PatchB1 |
| **Water 4×4 subcells** | `push_water_sheet` — 8 m × 8 m subcells; quads only when submerged below `WATER_TABLE_Y - 0.02` | `engine/src/terrain.rs` |
| **Shore clamp** | Corrosion streaks restricted off flat dry desert | `terrain.rs` / COL |
| **Downed CE glitch** | Scanlines · tear bars · chroma · pulsing vignette via `Session::wound_post` | `engine/src/post.rs` · Augury death chrome |
| **interact_near** | Eye/fwd ray · max reach **2.8** · replaces feet AABB prompts | `world.rs` / `session.rs` |
| **Z backpack drop** | Equipped pack → `ContainerKind::Backpack` world object + SEARCH | `session.rs` |
| **Corpse / stash** | EnemyCorpse on Locus/Thrall death · Hideout stash 36 · Field stash terminals 12 | `loot.rs` / `session.rs` |
| **Loot suite 50+** | Modular Military* guns/optics/grips/muzzles/mags/ammo/packs + Space quick-all cards | `loot.rs` · Range feel · Beabim KIND |
| **Escape / online** | Esc closes sheets → Title; Title Esc does not quit; PVPVE/PVE 1-click | `runtime.rs` · `d08042e` |
| **Bridges** | Concrete water bridges + pillars · cell spacing **~320 m** · none inside **~120 m** of origin · deck `WATER_TABLE_Y + 1.15` · pillars every **8 m** | `scar.rs` · Hypha — need water gap away from hideout |
| **Server pre-bake** | Master world map + container pre-bake on dedicated startup | `828d971e` |

## Queued cooks (do not claim shipped)

| Seat | Row |
|------|-----|
| **Lab-Rat** | Water tar UV · scatter grass/scrub/rocks/garbage/Locus litter (CE steal) |
| **Hypha** | Flat spawn (no holes) · overhang ribbon · bike friction · Soft LOD parked · Filter **#251** when tip-clean |
| **Range** | Stamina over-tired · biped arm/H-flip · kit/attach bridge for extra Military* guns |
| **Augury** | Chrome tip audit · Sonderer mesh · glasses-N parked |
| **Beabim** | KIND loot sync audit · client join honesty · 64-cap spin-new · **#221** no plant |
| **Clerk** | Branch delete candidates `Play` · `cursor/dev-b/c-ce74` (0 ahead) — only on Evan yell |

## Gate

Cursor cloud agents from Grok Bot need usage / on-demand. This shelf used **GitHub MCP only** (no Cursor VM).

## Pointers

- fulcrumRust root [`PatchB1.md`](https://github.com/initialvisuals/fulcrumRust/blob/main/PatchB1.md)
- [`docs/WANT_CHECKLIST.md`](https://github.com/initialvisuals/fulcrumRust/blob/main/docs/WANT_CHECKLIST.md)
- [`docs/WANT_LEFTOVER.md`](https://github.com/initialvisuals/fulcrumRust/blob/main/docs/WANT_LEFTOVER.md)
- [`docs/EXTRACT_LOOT_DIAL_SHEET.md`](https://github.com/initialvisuals/fulcrumRust/blob/main/docs/EXTRACT_LOOT_DIAL_SHEET.md)
