# Checkpoint peek findings (fulcrumRust)

Parked from Evan’s first full `main` peek (2026-09-07). Growth yard + curl read OK.

## Closed by fulcrumRust #12 (2026-09-07)

- **Look / move mismatch** — locked: Y-up world, `yaw = 0` looks **+Z**; WASD look-relative; mouse-right increases yaw
- **Sideways gun** — SMG long axis is **look** (bore along +fwd); mag dots run along the bore
- **No visible bullets** — feel-lab tip→impact tracers + muzzle flash + spark/mark live
- **Wall camera / lean** — Q/E wall-clamped peek (feel-lab +lean = left); Augury glasses add `SLIDE` / `SPD` / `HT` labels only (no ammo HUD)

## Closed by fulcrumRust #13 (2026-09-07)

- **Yard graybox slabs** — Lab-Rat fidelity pass so peeks read **growth**, not slabs:
  - **2D stamp** — short-segment glowing webbing + anastomosis rings + quiet grit + spore core
  - **Organic 3D** — thin bent stem + volva, wide cap with gills, side fruit, plume webbing (mushroom silhouette)
  - **Creeper** — low olive tubes on meandering tendrils / forks; soil-hugging anastomosis (short AABB steps)
- CPU boxes, no collide; curl **1 / 2 / 3** and plot origins unchanged. See fulcrumRust `docs/GROWTH_POC.md`.

## Closed by fulcrumRust #14 (2026-09-07)

- **Brick SMG** — replaced by **MP9-Z** feel-lab silhouette kit (stock / receiver / pic rail / handguard / barrel / flash hider / polymer grips / seated smg_20 stick + brass plaque / iron·holo·acog hoods / short .45 can)
- **Optic cycle** — **V** iron → holo → acog; ADS poses `ads` / `ads_holo` / `ads_acog`; FOV hip **90** / iron ADS **60** / holo ADS **60** / acog ADS **25**; look sens scales with FOV
- **Suppressor** — **N** toggles .45 can; HoB + tracer spawn follow can tip (`suppressor_tip_z = -0.507`); flash hider hides when mounted
- Unchanged house locks: 20-rd + 4 mags, 1200 rpm / recoil / gravity / zero, axes + tracers + Q/E lean + slide + Ctrl+mouse height + wheel speed, Lab-Rat yard / curl

## Closed by fulcrumRust #15 (2026-09-07)

- **Smart material stamps** — rule-based **dirt / sand / rock / concrete / organic** on 8 m cells (no paint editor)
- **Sit-on-surface structures** — mushroom / web / rock outcrop / concrete lip / sand ripple / grit; skip growth yard + spawn
- **Append-after-bake** — Hypha grayboxes keep indices; `VoxelHost` stub for real heightfield later
- **Glasses** — off yard: `DIRT  STAMP` / `ROCK  STAMP` / … (labels only)
- Yard plots + curl **1 / 2 / 3** unchanged. See fulcrumRust `docs/STAMPS.md` + house `STAMP_FEEL_LOCK.md`.


## Closed by fulcrumRust #16 (2026-09-07)

- **Gray slab extract gone** — bake-once Transvoxel isosurface (`TerrainHost` + crates.io `transvoxel` 2.0); flat world, not a planetoid
- **Distance LOD** — center subdiv **16** / ring-1 **8** / outer **4** + Lengyel transition faces; smoke peek `terrain_tris≈3354 lods=3`
- **Lab-Rat consume live** — `sample_channels` + `density_stamp_2d` / `WearStamp` drive density + material; verts grade from `VoxelMaterial::tint` (no second material story)
- **Grimdark extract lock** — ashen wash / slate sides / brutalist vertex paint, proc wear/cracks, void-spore stamp tints, cheap distance haze; hideout stays small/unfogged
- Yard plots + curl **1 / 2 / 3** + MP9-Z / heat / Locus / menus unchanged; `AuguryLocusSpawn` reserved on a rise
- Detail: fulcrumRust `docs/TERRAIN.md` + house `TERRAIN_NORTHSTAR.md` / `AESTHETIC_DIEGETIC_LOCK.md`

## Closed by fulcrumRust #17 (2026-09-07)

- **Transvoxel consume channels** — Lab-Rat `sample_channels` / `fill_chunk_samples` expose signed density + `VoxelMaterial` for Hypha’s mesher
- **Density sign lock** — `> 0` solid, `< 0` air, `0` isosurface (Hypha may flip for port)
- **Ownership** — Hypha owns Transvoxel tables / LOD / far-chunk simplify; Lab-Rat does not paste Lengyel tables
- CPU-box overlays remain peekable leftover until Hypha meshes. See fulcrumRust `docs/STAMPS.md` + house `TERRAIN_NORTHSTAR.md`.

## Closed by fulcrumRust #18 (2026-09-07)

- **Locus Standard on yard** — graybox biped (capsule boxes, rust-eye0) at `YARD_STANDARD` (5.15, 0, 7.85), right of Lab-Rat creeper
- **Thin brain** — CE shape Idle→Alert→Chase/Engage→Recover; Dead = ragdoll flop stub
- **Distance activation** — `ACTIVATE_M` 24 / `SLEEP_M` 32 / `HEAR_M` 18; far guts skip path/hunt; shot crack can wake
- **MP9-Z wound** — Range Tech tracers already slab-hit walls; #18 adds living hurtbox hitscan + visual stop (`SMG_PELLET` 14); Engage slash 10
- **Inked** palette stub only — not spawned. TODO family: Inked / Sonderer / Monk / Oculus / crawler
- Glasses: `LOCUS  STANDARD  IDLE|ALERT|…` labels only. See house `LOCUS_AI_LOCK.md`.

## Closed by fulcrumRust #19 (2026-09-07)

- **World drop / pickup** — **Z** drops held MP9-Z as loose world kit + canvas bag pad (feel-lab X remapped to last-pass Z); snapshot keeps in-mag + reserve mags + optic + can + fire mode; cheap UUID survives drop↔pickup; **F** picks up / swaps (held kit lands at feet first); empty hands hide viewmodel / heat cards / fire; cap **8** oldest despawn; knife/bandage stay on person
- **FX draw-distance dials** — feel-lab hide-not-despawn XZ: `muzzle_draw_m` **28** (8–80), `spark_draw_m` **55**, `decal_draw_m` **700**; walking back shows them again; #12 flash/spark/mark stay live
- Mag chrome stays diegetic on the kit — no HUD ammo counter

## Closed by fulcrumRust #20 (2026-09-07)

- **Void-spore grimdark yard** — denser 2D webbing / hellish mushroom / spore-tipped creeper via shared `density_stamp_2d` (veins + anastomosis rings + grit + spore core). Curl **1 / 2 / 3** unchanged
- **Concrete crack / edge-wear** — `WearStamp` leftovers driven by the same 2D density field; brutalist masses on perimeter concrete; wear feeds `sample_channels` so Hypha can mesh scars
- **Smart materials grimdark grade** — dirt / sand / rock / concrete / organic crushed luma (`VoxelMaterial::luma`); organic dirt bleed = void-spore takeover webs
- Peek: stamp (left) hellish webbing not gray plate; center mushroom dark fruiting body; creeper tips spore; off-yard perimeter lip carries cracks + chipped edges; glasses still `CONCRETE  STAMP`
- Detail: fulcrumRust `docs/STAMPS.md` + house `STAMP_FEEL_LOCK.md` / `AESTHETIC_DIEGETIC_LOCK.md`

## Closed by fulcrumRust #21 (2026-09-07)

- **Audio buses Voice / Music / FX** — feel-lab Settings Audio DNA (not a DAW); gains **0–2** default **1.00 / 100%** into a master; Options three-row sheet (title + pause); A/D or ←/→ nudge **0.05**; Esc back; dials persist across Deploy
- **Routes** — FX: fire / dry / reload / cycle / pickup / putdown; Voice: UI confirm; Music: hideout / extract ambient bed stub
- **Hard check** — SMG fire SFX respect FX bus (FX `0` silent; half quieter); procedural tones only; file slots later
- Detail: house `EXTRACTION_AUDIO_LOCK.md` + fulcrumRust `engine/src/audio.rs`

## Closed by fulcrumRust #22 (2026-09-07)

- **Feel-lab kit stubs** — selectable **SR-25** (DMR) + **M24** (bolt) silhouettes beside day-one **MP9-Z**; spawn still MP9-Z
- **Picker binds** — **G** cycles MP9-Z → SR-25 → M24; **4 / 5 / 6** seat directly; **U** stays unaimed-hold cycle; **1 / 2 / 3** stay Lab-Rat curl
- **Per-kit ballistics** (`FeelSheet::fire`): MP9-Z AUTO ~1200 rpm / 300 m/s / kick 1.0 · SR-25 SEMI 0.14 s / 785 m/s / kick 1.15 · M24 bolt 0.65 s / 810 m/s / kick 1.75; HoB / muzzle / heat τ follow the feel-lab sheet
- **Mag chrome = mag size** — well count is capacity (MP9-Z **20** / SR-25 **20** / M24 **5**); Hold-R peek unchanged; still no HUD ammo counter
- **Optics** — **V** cycles the seated kit’s allow-list (SMG iron/holo/acog; SR-25 + scope; M24 iron/scope); **N** can still mounts
- Drop/pickup, heat, Locus, yard, audio buses, Transvoxel host unchanged

## Closed by fulcrumRust #23 (2026-09-07)

- **Distance activation / far-guts cold** — Hypha `engine/src/activation.rs` shares Augury Locus `ACTIVATE_M` **24** / `SLEEP_M` **32** hysteresis (CE labyrinth DNA; not a web port)
- **Bake rings = Transvoxel LOD** — fine / mid / far match `lod_for` 0/1/2; far rings skip stamp-structure / wear density consume + per-vert wear walk; far plates / structures / wear stay out of extract bake (collide boxes still land); far crates/poles skipped; brutalist compounds stay for horizon
- **Live cold** — Growth + Locus GPU uploads skip past `ACTIVATE_M` (yard Idle still visible; cycle/curl keep ticking); near playable yard unchanged
- **Smoke peek** — `near_chunk=862` · `far_chunk=45` · `guts_warm=17` · `guts_cold=140` · `terrain_tris=3168` (~**19×** cheaper far mean; 140 far stamp guts stayed cold)
- Reuses #16 `TerrainHost` — no mesher rebuild. Detail: fulcrumRust `docs/TERRAIN.md` + house `TERRAIN_NORTHSTAR.md` / `LOCUS_AI_LOCK.md`

## Controller lock (Evan bind wins)

Shipped in fulcrumRust #12. Overrides soft aim-offset wheel-height where they disagreed:

- **Q / E** — peek left / right
- **Shift then Ctrl** — slide carry (sprint + crouch rising edge)
- **Hold Ctrl + mouse up/down** — analog eye height (does **not** pitch-look)
- **Mouse wheel** — move speed (**not** height; aim-offset uses wheel for crouch height — Evan’s bind wins)
- No double-jump day-one

## Holding steady

- Hypha: distance activation / far-guts cold landed (#23) on #16 host; next live LOD recook / tunnel cutouts / SVG density-mask ingest; keep sit-on-surface CPU boxes as peek leftover
- Augury: Locus Standard + distance activation landed (#18); next Inked/Sonderer/Monk/Oculus/crawler + stamp spawn filters (prefer rock/concrete; avoid organic)
- Lab-Rat: void-spore grimdark + density-driven concrete wear landed (#20); next wet-lab beats stay on STEAL_MAP (SVG/density-mask ingest / experiment log)
- Range Tech: SR-25 + M24 feel-lab kit stubs landed (#22); next day-night clouds + HDR pairing; spatial / binaural still Augury DNA on top of the Voice/Music/FX buses

Steal from this shelf + steal map. Not chat scroll.