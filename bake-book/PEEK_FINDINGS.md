# Checkpoint peek findings (fulcrumRust)

Parked from Evan’s first full `main` peek (2026-09-07). Growth yard + curl read OK. Same-day feel dump **landed #59**. Hypha ring-mip texture LOD **landed #60**. Hypha near LOD raise **landed #61**. Range Tech handmade atelier SFX vendor **landed #62**. Range Tech music playlist + kit metal/grit PBR stub + ±6% remix jitter **landed #64**. Hypha colorless muzzle heat **landed #66**. Range Tech Patch A muzzle **landed #67**. Range Tech ADS viewmodel DoF **landed #68**. Range Tech heat dial blend **landed #71**. Range Tech SIM-only launch **landed #76**. First big-map brief (2026-09-08) is **Holding** — do **not** claim shipped. Evan **clean** yell 2026-09-08 ~00:00 ET — atelier plugs **open**.

## Patch A checkpoint (fulcrumRust #72)

Living A-feedback checkpoint — **not** a replacement for `STEAL_MAP` or `MILESTONE_01_PLAYABLE`. Repo-root [`patch notes A.txt`](https://github.com/initialvisuals/fulcrumRust/blob/main/patch%20notes%20A.txt) ([#72](https://github.com/initialvisuals/fulcrumRust/pull/72)). Marks: `X` done / on main · `~` partial / in progress / shallow first pass · `*` next / ready for a careful cook when greenlit · `·` parked / not started. Seats: Range Tech | Hypha | Lab-Rat | The Augury | Evan | house. Overnight cooks and seats read open A asks from that file; do **not** invent PR numbers. Do **not** copy the ledger here. Range Tech dump-dial blend is **landed #71** (`X` on the house shelf — A-notes `~` for that row is stale). Range Tech sim-default / single model is **landed #76** (`X` on the house shelf).

## Holding — first big-map brief (Evan 2026-09-08)

**Brief only. Do not claim shipped.**

First true big map for fulcrumRust extract. Live shelf remains #16 host + #23 far-cold + #43 **7×7 / 112 m / 12 544 m²** + near LOD **32/16/4** (#61) + #60 grit mips + #39 yard pad ≈ **110 m²**.

- **Hypha** host: drop outer walls · extend **~8×** · chunked Transvoxel · **load chunks by distance from players** (listen-server aware — #34 handshake exists; terrain sync still parked). Near LOD raise **already landed #61** (32/16/4). Big-map **continues on fulcrumRust**
- **Lab-Rat** stamps: slope/angle materials · dirt/scatter/deform · PBR bake-down. Evan **clean** yelled 2026-09-08 ~00:00 ET — atelier plugs **open**. Atelier **150 roughness + textures/PBR ~26 sets landed**. #58/#60 stay the live yard plugs until more grit cooks. Holocron rust rewrite **after** slope/PBR — see `TOOLS.md`
- **Range Tech**: kits + FX draw-distance on the wider yard; kit metal/grit PBR stub **landed #64**; store `dBXpg` still **open**; Music playlist beds **landed #64**; ADS viewmodel DoF **landed #68**; heat dial blend **landed #71**
- **Augury**: FoW brand / menu video **when cut ready**

Do **not** claim the 8× map, wall drop, chunk stream, slope materials, Lab-Rat PBR plugs, `dBXpg`, full metal-tech kits, or menu video shipped. Music playlist beds **are** shipped #64. Kit metal/grit PBR stub **is** shipped #64. See `TERRAIN_NORTHSTAR.md`.

## Open — texture / atelier leftovers (roughness→stamp still open)

Range Tech Evan peek feel **landed #59**. Hypha ring-mip texture LOD **landed #60**. Hypha near LOD raise **landed #61**. Range Tech handmade atelier SFX vendor **landed #62**. Range Tech music playlist + kit metal/grit PBR stub **landed #64**. Hypha colorless muzzle heat **landed #66** (sample-only `heat_warp_uv` on the #55 post stack — lattice is post input only; no world-pipeline orange card). Range Tech Patch A muzzle **landed #67** (kit-tip spawn + `hip_honest_dir` + tip→impact streak clamp — hip-fire no longer behind the handguard / upper-right of the reticle; did not fight #66). Range Tech ADS viewmodel DoF **landed #68** (ADS near + far on the same #55 pass / Options **DOF**). Range Tech heat dial blend **landed #71** (was→now→stolen on the #66 post path — haze **0.07** / size **0.83** / scaleX **0.396** / lobe **0.698**; #66 colorless path stays). Range Tech SIM-only launch **landed #76** (arcade aim-dir + **P** toggle dead; leftover `hob_zero` ignored; **O** 50/100/200 stay). Further Lab-Rat roughness→stamp still open (atelier PBR batch **in**; Evan **clean** yelled — plugs **open**). Do **not** claim the whole roughness→stamp cook. Do **not** claim Lab-Rat grit/slope/PBR plugs or `dBXpg` shipped.

- **Texture compression** — atelier roughness packs are **4k 48-bit PNG** (too large). Do **not** ship raw 4k 48-bit into the yard. Lab-Rat **#58 landed** the vendored near packs (256² bake-downs under loud scars). Hypha LOD-tied mips **landed #60** on Transvoxel **distance rings** (near 256² / mid 64² / far 16²; far drops grain hashes). In-repo grit mips stay #60 until Lab-Rat cooks more. Do **not** claim the whole roughness→stamp cook
- **Atelier** — plugs **open** (Evan **clean** yell 2026-09-08 ~00:00 ET). PBR batch **in** (150 roughness + textures/PBR ~26 sets). #58 optional `FULCRUM_GRIT=` / `FULCRUM_ATELIER=` stay read-only **load** paths. Crew may plug; bake-down first
- **Lab-Rat** — **#58 quiet grit greyscales landed** (vendored bake-downs + `sample_channels` quiet height + `grit::rough` wear — the near source for #60). Grit / slope / PBR plugs **open**. Further roughness → stamp stays on **fulcrumRust only**; bake-down first. SVG / density-mask / experiment-log still open. Slope/angle + scatter/deform sit on the big-map brief. Holocron rust rewrite **after** those plugs (`channels.rs` / stamp stacks / `feel` / `kit_mesh`) — see `TOOLS.md`
- Day-one FILE_SLOTS vendor **landed #62**. **SFX remix DNA** — creative reuse OK (pitch/speed/effects; indie underground; don’t overuse the same stem). First application **landed #64** — fire/foot/reload ±6% pitch/speed jitter on the #62 vendor; full remix minting still **open**. **Music** playlist beds **landed #64** (five titled beds; hideout+extract advance shuffle; Options Music dial; missing → two-tone stub). Shot propagation / full CE pack dump still later — that is audio files, not the #59 feel dials

## Closed by fulcrumRust #12 (2026-09-07)

- **Look / move mismatch** — locked: Y-up world, `yaw = 0` looks **+Z**; WASD look-relative. #12 authored mouse-right increases yaw; **#51 AXIS_LOCK** subtracts mouse X (invert horizontal) + invert A/D — see Closed by #51
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
- **Suppressor** — **N** toggles .45 can; HoB + tracer spawn follow can tip (`suppressor_tip_z = -0.507`); flash hider hides when mounted. **#67** live spawn is `kit_mesh::muzzle_tip_local` (heat-box front); `muzzle_socket_local` / can tip stay the authored fallback
- Unchanged house locks: 20-rd + 4 mags, 1200 rpm / recoil / gravity / zero, axes + tracers + Q/E lean + slide + Ctrl+mouse height + wheel speed, Lab-Rat yard / curl

## Closed by fulcrumRust #15 (2026-09-07)

- **Smart material stamps** — rule-based **dirt / sand / rock / concrete / organic** on 8 m cells (no paint editor)
- **Sit-on-surface structures** — mushroom / web / rock outcrop / concrete lip / sand ripple / grit; skip growth yard + spawn
- **Append-after-bake** — Hypha grayboxes keep indices; `VoxelHost` stub for real heightfield later
- **Glasses** — off yard: `DIRT  STAMP` / `ROCK  STAMP` / … (labels only)
- Yard plots + curl **1 / 2 / 3** unchanged. See fulcrumRust `docs/STAMPS.md` + house `STAMP_FEEL_LOCK.md`.


## Closed by fulcrumRust #16 (2026-09-07)

- **Gray slab extract gone** — bake-once Transvoxel isosurface (`TerrainHost` + crates.io `transvoxel` 2.0); flat world, not a planetoid
- **Distance LOD** — then center subdiv **16** / ring-1 **8** / outer **4** + Lengyel transition faces; smoke peek `terrain_tris≈3354 lods=3`. **#61** later raised to **32/16/4**
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
- **Inked** palette stub only then — spawned later in #26. TODO family: Sonderer / Monk / Oculus / crawler
- Glasses: `LOCUS  STANDARD  IDLE|ALERT|…` labels only. See house `LOCUS_AI_LOCK.md`.

## Closed by fulcrumRust #19 (2026-09-07)

- **World drop / pickup** — **Z** drops held MP9-Z as loose world kit + canvas bag pad (feel-lab X remapped to last-pass Z); snapshot keeps in-mag + reserve mags + optic + can + fire mode; cheap UUID survives drop↔pickup; **F** picks up / swaps (held kit lands at feet first); empty hands hide viewmodel / heat cards / fire; cap **8** oldest despawn; knife/bandage stay on person
- **FX draw-distance dials** — feel-lab hide-not-despawn XZ: `muzzle_draw_m` **28** (8–80), `spark_draw_m` **55**, `casing_draw_m` **55**, `decal_draw_m` **700**; walking back shows them again; #12 flash/spark/mark stay live
- Mag chrome stays diegetic on the kit — no HUD ammo counter

## Closed by fulcrumRust #20 (2026-09-07)

- **Void-spore grimdark yard** — denser 2D webbing / hellish mushroom / spore-tipped creeper via shared `density_stamp_2d` (veins + anastomosis rings + grit + spore core). Curl **1 / 2 / 3** unchanged
- **Concrete crack / edge-wear** — `WearStamp` leftovers driven by the same 2D density field; brutalist masses on perimeter concrete; wear feeds `sample_channels` so Hypha can mesh scars
- **Smart materials grimdark grade** — dirt / sand / rock / concrete / organic crushed luma (`VoxelMaterial::luma`); organic dirt bleed = void-spore takeover webs
- Peek: stamp (left) hellish webbing not gray plate; center mushroom dark fruiting body; creeper tips spore; off-yard perimeter lip carries cracks + chipped edges; glasses still `CONCRETE  STAMP`
- Detail: fulcrumRust `docs/STAMPS.md` + house `STAMP_FEEL_LOCK.md` / `AESTHETIC_DIEGETIC_LOCK.md`

## Closed by fulcrumRust #21 (2026-09-07)

- **Audio buses Voice / Music / FX** — feel-lab Settings Audio DNA (not a DAW); gains **0–2** default **1.00 / 100%** into a master; Options **Audio** tab is the live three-row mixer (title + pause; #45 sits the Options list; #46 filled Graphics/Gameplay/Controls; Audio still this mixer); A/D or ←/→ nudge **0.05**; Esc Hypha pane / Audio → Options → title/pause; dials persist across Deploy
- **Routes** — FX: fire / dry / reload / cycle / pickup / putdown; Voice: UI confirm; Music: hideout / extract ambient bed stub
- **Hard check** — SMG fire SFX respect FX bus (FX `0` silent; half quieter); file-slot wiring shipped #54; handmade vendor landed #62 (missing → procedural)
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

## Closed by fulcrumRust #24 (2026-09-07)

- **Extract day/night clock** — feel-lab Settings Lighting DNA on the yard (default **06:21** / `TOD_DEFAULT` 6.35); hideout stays authored interior / unfogged
- **Dials** — **[ / ]** clock ±30 min (wrap 0–24) · **K** snap dawn→noon→dusk→night · **L** live day↔night cycle · **− / =** exposure mul (feel-lab **1.44** default) · **, / .** cloud cover
- **No XOR sky** — one ToD sample drives ambient / key / fill / fog + procedural dome together; dual color-aware lights
- **Grimdark luma crush** — `EXTRACT_SKY_LUMA` **0.20** keeps noon ashen (not a bright sandbox); Day HDRI shipped #40 (Goegap 4k plate; atelier stub is fallback)
- **Glasses** — `06:21  DAWN  EXP 1.44` labels only on extract (not a second ammo HUD); #40 adds `HDRI` / `PROC`
- Transvoxel host / kits / drop / audio / heat / Locus / far-guts activation untouched. Smoke: `clock=06:21` plus near/far guts peeks
- Detail: fulcrumRust `engine/src/sky.rs` + house `AESTHETIC_DIEGETIC_LOCK.md` / `FULCRUMRUST_LAST_PASS_LOCK.md`

## Closed by fulcrumRust #25 (2026-09-07)

- **Wall-clamped Q/E lean polish** — Range Tech aim-offset / Engine #3 polish on existing #12 lean (no controller rebuild)
- **Sign lock** — then **Q** = left / +lean · **E** = right / −lean. **#59 supersedes sign + depth:** **Q = peek right** (−lean, same side as inverted A) · **E = peek left** (+lean). Eye formula stays `+lean → −flat_right`
- **Dials** — then `lean_offset` **0.18** · `lean_roll` **0.12**. **#59 depth** feel-lab **0.5 / 0.5** (`leanOffset` / `leanMax`). `lean_spring` **8.0** · `lean_skin` **0.08** · `lean_viewmodel` **0.16** stay; wall clamp / spring / yard covers stay
- **Spring then ceiling** — spring enter/exit, then hard ceiling after the spring so walking into a wall cannot push past clearance; release still springs out (no snap)
- Camera probe uses those MoveDials (no hardcoded 0.18 / 0.12)
- **Viewmodel pad** (`lean_viewmodel` **0.16**): E peeks stop the gun leading side at geometry (0.18 m camera travel is shorter than the capsule)
- Origin already inside a wall: `probe_clearance` reports 0 clearance
- **Yard** — two collide covers at extract yard mouth (`YARD_LEAN_COVERS`) on the Transvoxel pad; stay off plots / Locus / spawn
- Kits / drop / audio / heat / ToD / Locus / Transvoxel; slide / Ctrl+mouse height / wheel speed stay
- Detail: fulcrumRust `engine/src/feel.rs` + `engine/src/player.rs` + house `FULCRUMRUST_LAST_PASS_LOCK.md`

## Closed by fulcrumRust #26 (2026-09-07)

- **Locus Inked on yard** — second fightable graybox; darker / hooded / thinner silhouette, cyan eye0, cheap ink-zone disc under feet (Augury chrome; Lab-Rat #30 owns the loud stamp under the pad)
- **Same brain + wake meters** as Standard — Idle→Alert→Chase/Engage→Recover + ragdoll stub; shared Hypha `ACTIVATE_M` **24** / `SLEEP_M` **32**
- **Pad** `YARD_INKED` **(−5.10, 0, 8.20)** — left of 2D webbing; does not overlap Standard (right of creeper) or lean covers
- **Kit hitscan** wounds Inked via the same `apply_shot` path; glasses `LOCUS  INKED  …` labels only
- Family TODO remains: Sonderer / Monk / Oculus / crawler + stamp spawn filters
- Detail: house `LOCUS_AI_LOCK.md` + fulcrumRust `engine/src/locus.rs`

## Closed by fulcrumRust #27 (2026-09-07)

- **Day-one binaural / positional stereo on FX** — Hypha + Augury; CE FoW spatial DNA on the **same** #21 Voice / Music / FX tree (**not** a fourth bus)
- Listener follows leaned camera (#25); HRTF-ish pan = equal-power ILD + Woodworth ITD + exponential distance
- World-posed FX: gunshots (muzzle), Locus slash (Standard + Inked), drops (putdown / pickup); Voice centered; Music ambient bed
- Reverb was a two-zone stub here (hideout tight/drier vs extract industrial). **Superseded by #56** authored AABB volumes DRY / YARD / OUT
- Smoke: `audio=100% zone=EXTRACT spatial=1.00`; FX `0` still silences fire; `Slot::Locus` rides FX
- File-slot wiring shipped #54; handmade vendor landed #62; shot propagation later. Detail: house `EXTRACTION_AUDIO_LOCK.md` + fulcrumRust `engine/src/audio.rs`

## Closed by fulcrumRust #28 (2026-09-07)

- **Hold-` inspect pose** — Range Tech; feel-lab has no named inspect (Backquote = debugger panel there). Steal reload-lift look-over DNA as a hold overlay
- Hold **`** (Backquote / last-pass `~`): raise + closer + yaw/roll so the receiver faces the lens
- Release returns to the **current** hold (hip / low / cant / ADS / sprint_high)
- Overlay only — does **not** eat **U** / **RMB** / **V** / **N** / **B** / **Z**; fire blocked while up (muzzle turned); B still toggles SEMI/AUTO
- Glasses `INSPECT` label only — no numeric ammo HUD
- Untouched: kits / lean / ToD / audio / heat / Locus Standard+Inked / Transvoxel
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust STEAL_MAP inspect row

## Closed by fulcrumRust #30 (2026-09-07)

- **Loud void-spore hotspot under Locus Inked** — living floor scar at `growth::INKED_HOTSPOT` = `locus::YARD_INKED` **(−5.10, 0, 8.20)**; `INKED_HOTSPOT_REACH` **1.55**. Flat leftover, not a fourth yard plot
- Reuses #20 `density_stamp_2d` / WearStamp DNA; denser/louder than quiet 2D grit. Pinned WearStamps: `VoidSporeWeb` + new **`VoidSporeCrack`**
- Curl **1 / 2 / 3** shares the 2D stamp field (webbing OR Inked pad); remnants stay — not a softlock
- Glasses: **`INK HOTSPOT`** (and curl toast) when standing on the scar off the Locus prompt; Augury still owns Locus labels + cheap ink-zone disc chrome
- Ownership: Lab-Rat owns the loud growth stamp under the pad; Augury still owns Inked AI + ink disc
- Peek: Title → Deploy → extract; slightly **left** of 2D webbing; Inked stands on loud ink hotspot; optional **1 / 2 / 3** wilt
- Detail: fulcrumRust `docs/GROWTH_POC.md` + `docs/STAMPS.md` + house `STAMP_FEEL_LOCK.md` / `LOCUS_AI_LOCK.md`

## Closed by fulcrumRust #31 (2026-09-07)

- **Bandage use stub** — **T** bandage use (last-pass named the *item*, not the key; **G** stays kit cycle). Does not steal **H** shoulder, **X** prone, **C** / **Mouse4** knife, **Q** / **E** lean, **Z** drop, **B** fire-mode, **V** optic, **N** can, **U** hold, **`** inspect, **F** pickup, **1** / **2** / **3** curl.
- Day-one kit already lists bandage:1 — this PR adds the use path. Consume 1 → **+40** health (`BANDAGE_HEAL`); armor untouched; cap at `max_health`. Blocked at full HP (no consume).
- Glasses: `BANDAGE` on use / `EMPTY` on empty press — labels only, never a second ammo/health HUD
- FX: `Slot::Wrap` on the #21 FX bus (cloth rustle stub, on-body like knife swipe). Not a heal chime.
- Works empty-handed; bandage stays on person when **Z** drops the gun (same as knife). No down/death (Augury owns that later).
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust `engine/src/kit.rs` / `session.rs` / `input.rs` / `audio.rs`

## Closed by fulcrumRust #32 (2026-09-07)

- **R scheme** — **Hold R** (~200 ms) peek chrome only (does not start reload; release after a hold is not a tap). **Tap R** short press, reload on RELEASE when `in_mag < capacity` AND reserves > 0 (NOT empty-only). **Double-tap R** (~300 ms from first tap) = emergency SWAP
- **Dials** (`kit.rs` + `session.rs`): `RELOAD_PEEK_HOLD_SEC` **0.20** · `RELOAD_DOUBLE_TAP_SEC` **0.30** · `RELOAD_BASIC_SEC` **1.10** · `RELOAD_EMERGENCY_SEC` **0.46** (same 1-reserve cost)
- **Discard** — leftover rounds discarded on both paths (reserve is whole mags, not pocketed partials). Emergency’s higher-cost feel is dumping a half-stick
- Glasses: `RELOAD` (basic) / `SWAP` (emergency) labels only — never a numeric ammo HUD
- Intact: knife, bandage, lean, inspect, ToD, kits. Viewmodel `reload_t` mag-out dip; inspect overlay still wins over reload dip

## Closed by fulcrumRust #33 (2026-09-07)

- **Live HoB zero + arcade/sim launch** — per-kit rpm/recoil/HoB sheet was already authored (#22); this PR makes zero distance + arcade↔sim **live**. **#76 supersedes the dual path** — launch is **SIM only** (HoB + gravity / zero); arcade aim-dir dead; leftover `hob_zero` ignored
- **Dials** — `ZERO_PRESETS_M` **[50.0, 100.0, 200.0]** m; default `zero_dist_m` **100**; then default `hob_zero` **true** (SIM). **O** 50/100/200 stay. Leftover `hob_zero` is sheet-shaped only after #76
- **O** — cycle live zero presets 50 → 100 → 200 → 50 (HoB solve). Shared across MP9-Z / SR-25 / M24 so G-swap does not hide the solve (`FeelSheet::cycle_zero`). **Stays**
- **P** — then arcade (aim-dir launch) ↔ sim (height-over-bore + ballistic zero) via `hob_zero` (`FeelSheet::toggle_hob_zero`). Shared launch mode across kits. **#76:** **P** unused (no new bind); `toggle_hob_zero` + session **P** apply gone; **P** no longer sets an input edge
- **Honesty** — changing zero preset changes muzzle **launch dir** only (not muzzle position). Then arcade vs sim launch dirs differed; sim aims up to meet sight zero; arcade launched along aim. **#76:** one SIM model (`solve_ballistic_launch` — not a precomputed bake). **#67** sits on top — hip fire uses `hip_honest_dir` (ads=0 on aim; ads=1 keeps this SIM solve). **O** still changes the zero; it bites when aimed. **P** does not
- Toast: then `ZERO  {n} M` / `LAUNCH  ARCADE` / `LAUNCH  SIM` (age **1.2s**, `Slot::Cycle`). **#76:** `ZERO  {n} M` stays; `LAUNCH  ARCADE` / `LAUNCH  SIM` gone with **P**
- Glasses status strip (labels only, never a second ammo HUD): then `Z{zero_dist_m:.0}  SIM|ARCADE`. **#76:** `Z{n}  SIM` only (ARCADE dead) e.g. `Z100  SIM`
- Intact / do not steal: **[ ]** stay ToD clock; **−/=** stay exposure; **9/0** left free; does not steal T/C/R/Q/E/Z/B/V/N/U/`/F/X/H/1/2/3/G/Mouse4; tip→impact tracers / muzzle / sparks stay; reload / knife / bandage / lean / inspect / ToD stay seated
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust `FeelSheet::cycle_zero`. `toggle_hob_zero` removed #76

## Closed by fulcrumRust #35 (2026-09-07)

- **Hold-J heat-tune dump** — Range Tech; hold **J** = heat-tune dump. **I** is no longer free — I is Augury stim (#37).
- **Feel** — sustained AUTO on the seated kit (`FeelState::try_heat_tune` / `fire_shot(..., heat_tune: true)`); uses kit `auto_interval_sec` while tuning (ignores SEMI hold gate)
- Recoil impulse + camera punch skipped; leftover LMB punch stomped while J is down (`recoil_punch` / `recoil_rot` / `cam_recoil_p` / `cam_recoil_y` zeroed) so the gun stays still
- Same cook path: `FeelState.barrel_energy` still climbs so the tip lattice feeds live dialing (no second heat cook). **#66** later made that lattice post input only — no world-pipeline orange card
- **Ammo dial cheat** — mag **still spends** while holding; **release refills** the seated mag via `DayOneKit::refill_mag` (tops stick to `smg_mag_size`, does **not** spend a reserve)
- Glasses: `HEAT TUNE` label only (amber-ish overlay) — never a second ammo HUD; must not count mag rounds
- Intact / do not steal: ToD **[ ]**/K/L/−/=/,/. · lean Q/E · inspect ` · reload R · knife Mouse4/C · bandage T · O zero (#33) · P unused (#76) · I stim · Y host · O/P/T/C/R/Q/E/Z/B/V/N/U/`/F/X/H/G/I/Y/1/2/3/Mouse4
- Tests that define the lock: `heat_tune_climbs_energy_without_camera_punch`, `heat_tune_does_not_fight_tod_lean_inspect_reload_knife_bandage_zero`, `heat_tune_glasses_do_not_count_mag`, `j_is_heat_tune_hold_without_stealing_binds`
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust STEAL_MAP heat-tune row

## Closed by fulcrumRust #34 (2026-09-07)

- **Listen-server + invite stub** — Hypha; thin `std::net` UDP hub in `engine/src/net.rs` (MyceliumEngine had no portable net crate)
- **Host** — title **HOST** (or **Y** while alive in hideout/extract) binds UDP and mints `fulcrum://ip:port`; `--host` arms title cursor and also listens after Deploy
- Default port **7777** (`FULCRUM_PORT` override). LAN iface if OS has one, else loopback
- **Join** — `--join fulcrum://ip:port` (also bare `host:port` and `fw://`); env `FULCRUM_JOIN`. Title **JOIN** confirms. No in-game text field this pass
- Glasses labels only: `HOST  ip:port`, then `JOIN` / `PEER` after HELLO/WELCOME — never a second ammo HUD
- Honesty: handshake / presence only — both machines still sim locally; **no** world replication / shoot/Locus/terrain/audio rewrite / PvEvP sim
- Solo **Deploy** unchanged (`net=off` on smoke)
- Intact / do not steal: **I** stim (#37), **O** HoB zero (#33), **P** unused (#76), hold-**J** heat-tune (#35), T/C/R/Q/E/Z/B/V/N/U/`/F/M/1/2/3/Mouse4
- Bind: **Y** alive host only (#34). Stim is **I** while downed (#37). Seats do not fight — downed Y is a no-op for host and stim.
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust STEAL_MAP Net row (todo→partial)

## Closed by fulcrumRust #36 (2026-09-07)

- **Down / death stub** — Augury; HP→0 **downs** (prone crawl + thin bleed) — not menu death. Bleed-out ~`BLEED_SECS` **22.0**; extra hits while downed shave `BLEED_HIT_SECS` **6.0**. Clock expiry → `DEAD` + dark bag.
- **Dials** (`engine/src/down.rs` + `kit.rs` + `session.rs`): `BLEED_SECS` **22.0** · `BLEED_HIT_SECS` **6.0** · `STABILIZE_HOLD_SECS` **1.45** · `STIM_REVIVE_HP` **35** · `RALLY_HP` **45** / `RALLY_ARMOR` **20** / `RALLY_LOW_HP` **25** · `REACH_M` **1.85**. Yard: dummy `YARD_DUMMY` **(3.55, 0, 4.55)** · stim `YARD_STIM` **(3.55, 0, 3.20)** (vial in front of dummy)
- **Binds (superseded by #37)** — **I** (downed) = stim self-revive (day-one kit `stim: 1`; not a standing heal). **Y** (alive) = Hypha listen-server host (#34). Downed Y does not host and does not stim. Alive I is a no-op (no consume).
- Hold **F** = stabilize stub (self while downed, or yard dummy when standing nearby). Glasses: `STAB STUB  NO NET` / `SELF-STAB STUB`. Solo placeholder — no fake net. **F** tap near bag = light corpse-reclaim stub.
- **T** bandage (+40 HP, #31) unchanged as heal item. While downed unstabilized: glasses `NEED STAB` (no consume). After stabilize: T stands + heals.
- **Mouse4 / C** knife slash on a **downed or dying** Locus while you are downed or low (≤25 HP) → `RALLY` (+45 HP / +20 armor, stands if downed)
- Glasses/toasts labels only (never a second ammo/health HUD): `DOWNED` · `DEAD` · `STIM` · `NO STIM` · `STIM  PICKUP` · `STAB STUB  NO NET` · `RALLY` · `NEED STAB` · `DEAD  BAG STUB` · `CORPSE RECLAIM STUB`. Stabilized prompt: `T HEAL / I STIM / SLASH RALLY` (#37; was `Y STIM`)
- Parked / still TODO (do not claim done): death cam; teammate net stabilize; timed surface kill; full extract loot loop
- Peek: Title → Deploy → yard dummy + stim right of spawn (off lean covers / plots / Locus pads). Down via Locus slash (glasses `DOWNED`, HP bar `DOWN`). **I** stim → stand at 35 HP; or hold **F** then **T**. Alive **Y** hosts (does not consume stim). Downed **Y** is a no-op. Dummy hold **F** → `STAB STUB  NO NET`. Knife a Locus corpse while downed or ≤25 HP → `RALLY`. Ignore revive ~22s bleed → `DEAD` + dark bag; die again elsewhere — previous bag gone; **F** on bag = reclaim stub.
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust `engine/src/down.rs` / `kit.rs` / `session.rs`

## Closed by fulcrumRust #37 (2026-09-07)

- **Augury bind split** — stim on **I**; **Y** stays Hypha host. Supersedes the #36 KeyY bind split (downed Y = stim / alive Y = host).
- **I** (downed) = stim self-revive (day-one kit `stim: 1`; yard vial `YARD_STIM` **(3.55, 0, 3.20)** in front of dummy; `[F] PICK UP STIM`). Not a standing heal. Alive **I** is a no-op (does not consume).
- **Y** (alive) = Hypha listen-server host (#34). Second press re-toasts invite. Does **not** stim. Downed **Y** is a no-op for both host and stim.
- Stabilized prompt / glasses: `T HEAL / I STIM / SLASH RALLY` (was `Y STIM`). Inventory `[I] STIM`.
- Hold **F** stabilize stub, **T** bandage, knife slash-rally, death-bag F reclaim unchanged from #36. Dial constants unchanged: `BLEED_SECS` **22.0** · `BLEED_HIT_SECS` **6.0** · `STABILIZE_HOLD_SECS` **1.45** · `STIM_REVIVE_HP` **35** · `RALLY_HP` / `RALLY_ARMOR` / `RALLY_LOW_HP` · `REACH_M` · `YARD_DUMMY` / `YARD_STIM`.
- Heat-tune (#35): hold **J** still; **I** is Augury stim (no longer free).
- Tests that define the lock: `y_hosts_i_stims_without_stealing_binds`, `y_alive_hosts_i_downed_stims_without_crossing`.
- Glasses labels still labels-only (never a second ammo/health HUD): `DOWNED` · `DEAD` · `STIM` · `NO STIM` · `HOST` · etc.
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust STEAL_MAP Hypha net + Augury down rows

## Closed by fulcrumRust #38 (2026-09-07)

- **Shape-agnostic stamp / paint substrate** — Lab-Rat hardens channels so any authored shape converts into density + material (or paint later). No new scar kinds / Standard scars / Monk AOE / extra yard silhouettes
- **API** — `ChannelOp` Union / Subtract / Paint / Replace; primitives sphere / ellipsoid / capsule / box / ribbon / brush / height-mask / mesh / volume; `StampField::layers` vs `::content`; paint writes real, brush UX stubbed; mesh→voxel via `voxelize_mesh` → `stamp_volume`
- **Consumers stay** — sit-on-surface leftovers, wear ribbons, Inked hotspot, yard plots + curl **1 / 2 / 3** compile into `StampField::content`; Hypha reserved StampSlots empty until fed
- Does **not** own Transvoxel / Locus AI / guns. Lab-Rat writes; Hypha remeshes
- Detail: fulcrumRust `docs/CHANNELS.md` + house `STAMP_FEEL_LOCK.md` / `TERRAIN_NORTHSTAR.md`

## Closed by fulcrumRust #39 (2026-09-07)

- **Extract-yard scale harness** — Lab-Rat expanded the extract yard into a scale/perf harness for the #38 stamp/paint substrate. Stay on the extract yard for what #39 shipped — not a bigger world map on that pass. First big-map brief (2026-09-08) is the next lock — not shipped. No Standard / Monk one-off scars. HDRI stays Range Tech
- **`apply_yard_harness`** — writes anonymous SDF lattice + larger paint brushes + 2D-mask convert of the three existing plots through `StampField::layers` (not a fourth named plot)
- **Expanded near pad** — `growth::yard_bounds` ≈ **110 m²** (baseline before harness ≈ **54 m²**); flatten disk tracks it so plots stay playable
- **Near-warm / far-cold** — near yard stays warm (`bake_guts_warm`); far guts stay cold (Hypha #23). Harness primitives are near-warm only; smoke fails if a layer center is far. `guts_cold` stayed **140**
- **Smoke cost line** (Hypha can see it):
  `growth=544 curled=580 stamps=100 structs=55 wears=117 content=173 layers=43 prims=216 yard_m2=110`
  `guts_warm=75 guts_cold=140 near_chunk=858 far_chunk=45 terrain_tris=3182`
  Baseline before harness: `layers=0 prims≈content yard_m2≈54 guts_warm=32`. Far cheapness holds (`far_chunk < near_chunk`). Growth GPU boxes still under 620
- **2D mask** — #38 wording that `primitive_from_density_2d` is opt-in and **not** auto-applied to live yard plots is stale: the harness stamps it on the three existing plots as a shallow anonymous scale test (still not a fourth named plot)
- Detail: fulcrumRust `docs/CHANNELS.md` + `docs/GROWTH_POC.md` + house `STAMP_FEEL_LOCK.md` / `TERRAIN_NORTHSTAR.md`

## Closed by fulcrumRust #40 (2026-09-07)

- **Goegap HDRI on extract ToD** — Range Tech; Poly Haven **Goegap** 4k Radiance RGBE (~22MB, CC0 / Greg Zaal). `engine/build.rs` fetches **one** file at build time into `engine/assets/hdris/` (not a submodule, not the atelier texture dump). Atelier raw is fallback. Missing file → procedural dome (honest).
- **Feel DNA** — Radiance RGBE decode → equirect sky/env (`engine/src/hdri.rs`). Same ToD sample still drives ambient / key / fill / fog / dome — **no XOR sky**. Plate yaw tracks the clock sun. Night fades the day plate back to the procedural dome (stars stay). Grimdark luma crush (`EXTRACT_SKY_LUMA` 0.20) keeps noon ashen.
- Hideout stays authored interior / unfogged.
- **/** toggles Goegap plate on/off — does **not** steal **M** (map). Existing ToD dials unchanged: **[ / ]** clock ±30 min · **K** dawn→noon→dusk→night · **L** live cycle · **− / =** exposure · **, / .** clouds.
- Glasses: `06:21  DAWN  EXP 1.44  HDRI` (or `PROC` when plate off / missing) — labels only, never a second ammo HUD.
- Smoke: `cargo run -- --smoke` prints `clock=06:21 hdri=goegap` (or procedural).
- Intact / do not steal: Lab-Rat stamps, Hypha Transvoxel, Augury Locus / down / death, listen-server, kits, knife, bandage, reload, heat-tune, **M** map.
- Detail: fulcrumRust `engine/src/hdri.rs` + house `AESTHETIC_DIEGETIC_LOCK.md` / `FULCRUMRUST_LAST_PASS_LOCK.md`

## Closed by fulcrumRust #41 (2026-09-07)

- **FoW title mark** — Augury; Evan’s Fulcrum of Will title header is the title wordmark on the #11 shell. Bitmap `FULCRUM OF WILL` text removed — header PNG is the wordmark. Subtitle / list stay. Gold rule later gone in #45 (white hairline)
- **Vendored asset** — `assets/brand/fulcrum-of-will-header.png` from `_CONCRETE_ECHO_` `@4_15_26` `public/images/Fulcrum Of will Header.png` (2048-wide, aspect kept). Atelier `brand/` was README-only — do not invent a replacement mark; runtime does not clone atelier or CE
- **Seat math** (`engine/src/brand.rs`): `MARK_MAX_W` **1.70** · `MARK_MAX_H` **0.40** · `MARK_CENTER_Y` **0.58** (clip-space y-up). Fit: `clip_aspect = image_aspect / window_aspect` so the header is not stretched junk on non-square windows. Bottom of mark must clear Deploy hit row (`mark_clears_deploy`)
- **Deploy / Continue / Options / Esc** hit rows and behavior unchanged. No second ammo HUD
- Tests that define the lock: `vendored_header_is_a_wide_png`, `decode_matches_ihdr`, `title_seat_keeps_pixel_aspect` (16:9 / 4:3 / 21:9)
- Peek: `cargo run` → first frame grim title with FoW header mark above DEPLOY / HOST / JOIN / CONTINUE / OPTIONS / QUIT; Enter / W/S / click / title Esc same as #11
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` / `AESTHETIC_DIEGETIC_LOCK.md` + fulcrumRust `engine/src/brand.rs`

## Closed by fulcrumRust #42 (2026-09-07)

- **Windows one-click release builder** — Hypha; honest `build.bat` = `cargo build --release -p app` (package from `app/Cargo.toml`). Does not touch atelier, HDRI/ToD, kits, terrain
- **PATH** — prepends `%USERPROFILE%\.cargo\bin` so double-click PATH still finds rustup. Clear miss if cargo absent (`https://rustup.rs`); pause on failure; print `target\release\app.exe`
- **`build-and-run.bat`** — builds then launches that binary **in this console** so the window is waited on. No `start`+detach, no `timeout /t` (feel-lab `StartServer.bat` DNA: Git Bash / Firefox `timeout.exe` spam). Extra args pass through (`--host`, `--smoke`, …)
- **README** — Windows double-click `build.bat` one-liner
- Quality/flag options still open / not invented here. Lab-Rat may want the same pattern for pycelium later
- Peek: double-click `build.bat` / `build-and-run.bat` on Windows
- Linux/CI unchanged. Detail: fulcrumRust `build.bat` / `build-and-run.bat` + house `FULCRUMRUST_LAST_PASS_LOCK.md`

## Closed by fulcrumRust #43 (2026-09-07)

- **Wider extract chunk radius** — Hypha; `TerrainHost` grid **5×5 → 7×7** (smallest honest odd widen): one extra **far** ring only
- Playable extract: **3 Chebyshev rings / 112 m span / 12 544 m²** (was 2 rings / 80 m / 6 400 m²)
- Near LOD then unchanged: center subdiv **16**, ring-1 **8**, outer **4**. **#61** later raised to **32/16/4** (that A/B)
- Far-cold still maps `lod >= 2` → heightfield-only + shares Locus `ACTIVATE_M` **24** / `SLEEP_M` **32**
- Lab-Rat `ExtractStubHost` stays aligned (`STUB_GRID = 7`)
- Smoke prints `rings=` / `extract_m2=` next to `near_chunk` / `far_chunk` / `yard_m2`. Example:
  `near_chunk=858 far_chunk=39 guts_warm=75 guts_cold=216 rings=3 extract_m2=12544 yard_m2=110 locus_hp=24 terrain_tris=4034 lods=3`
  Far mean chunk ~**22×** cheaper than near; extra far ring added cold guts; yard pad + Locus stay
- Stay out of Atelier / HDRI / title mark. No new named scars
- Detail: fulcrumRust `docs/TERRAIN.md` + house `TERRAIN_NORTHSTAR.md` / `FULCRUMRUST_LAST_PASS_LOCK.md`

## Closed by fulcrumRust #45 (2026-09-07)

- **Title + HOLD analysis-core polish** — Augury; FoW/CE grim lowfi chrome on the existing #11/#41 title and HOLD pause shell. Thin white mono (not heat/ammo gold). Tight white frames on Deploy/Host/Join/Continue/Options/Quit. Gold tick / gold hairline gone → white hairline; darker ground
- **HOLD** — tight white-framed panel, left rule, **SYSTEM PAUSED** (CE pause language); Resume / Options / Quit to menu
- **Options stub** — lists **Graphics / Audio / Gameplay / Controls**. Graphics/Gameplay/Controls were disabled `HYPHA` placeholders; **#46 filled those guts**. **Audio** still opens the live Range Tech #21 Voice/Music/FX mixer (persists)
- Audio overlay restyled to the same chrome; Esc Hypha pane / Audio → Options → title/pause
- Logo seat from #41 unchanged (vendored FoW header mark, `MARK_MAX_W` **1.70** / `MARK_MAX_H` **0.40** / `MARK_CENTER_Y` **0.58**)
- Not a second ammo HUD. Stays off atelier
- Peek: `cargo run` — framed title list under FoW mark; Options → Audio still nudges 0–2 / 100%; Esc backs one sheet at a time; in-game Esc → HOLD
- Detail: house `AESTHETIC_DIEGETIC_LOCK.md` / `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust STEAL_MAP Augury menu rows

## Closed by fulcrumRust #46 (2026-09-07)

- **Hypha Options guts** — filled the disabled `HYPHA` stub tabs on Augury’s #45 Options list. Not a second settings overlay. Title / HOLD / Options chrome + FoW logo seat stay Augury (#45/#41)
- **Graphics (live window + persist)** — Window mode live via winit: **Borderless** = default launch; **Windowed** = decorated 1280×720; **Exclusive** = exclusive video mode when OS/GPU expose one, else borderless fallback. Also `--windowed` / `FULCRUM_WINDOW=borderless|windowed|exclusive`. Post toggles persist (`project.json` / `FULCRUM_SETTINGS`) and must **not** be packed into Range Tech ToD / Goegap / HDRI uniforms: AO, AA, CA (+ strength default **0.35**, step **0.05**, range **0–1**), film grain, DoF. This peek they no-op'd; **#55** wired the GPU stack so they change the image. Hint then: `POST STUB UNTIL GPU · WINDOW LIVE · A/D NUDGE` (now `POST LIVE · AA ON`)
- **Gameplay (real)** — Glasses labels toggle + crosshair toggle (real — drop quads when off). Hint: `SHOOT FEEL STAYS · ENTER TOGGLE`
- **Controls** — Look scale sits on feel-lab sens: `LOOK_MUL` default **1.0**, min **0.25**, max **2.0**, step **0.05**; Invert Y toggle. Binds stay README. Hint: `LOOK SITS ON FEEL-LAB SENS · BINDS IN README`
- **Audio** — Untouched — still Range Tech #21 Voice/Music/FX mixer
- **Persist** — `project.json` in cwd, or `FULCRUM_SETTINGS=/path/to.json`
- **Esc walk** — Hypha pane / Audio → Options → title or HOLD (same stack as #45)
- Peek: `cargo run` → Options → Graphics window live; post toggles persist (GPU live **#55**); Gameplay glasses/crosshair; Controls look/invert; Esc backs; Audio still #21
- Ownership: Augury owns title + HOLD chrome + Options list shell + logo seat. Hypha owns Graphics/Gameplay/Controls guts + window mode + persist (**#46**); GPU post stack **#55**. Range Tech keeps Audio mixer. Still no second ammo HUD. No atelier push
- #46 remains guts/persist. GPU post stack that made toggles change the image is **#55**
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` / `AESTHETIC_DIEGETIC_LOCK.md` + fulcrumRust STEAL_MAP Hypha settings rows

## Closed by fulcrumRust #47 (2026-09-07)

- **Brass eject** — Range Tech leftover feel-lab FX on the same `TracerField`. Live fire from seated kit `ejectionPort`: `MP9Z_EJECT` **(0.036, −0.014, 0.018)** · `SR25_EJECT` **(0.038, 0.008, 0.018)** · `M24_EJECT` **(0.03, 0.018, 0.055)**. Camera-right toss; `CASING_GRAVITY` **12**; bounce then sleep; `CASING_FADE` **6** s; `MAX_CASINGS` **48**. Hide-not-despawn via `casing_draw_m` **55**. Hold-J heat-tune dump (#35) skips brass so the lattice stays still
- **Ricochet / spent slug** — feel-lab `trySpawnSpentSlugBounce` — **NOT** a bounce table. `SLUG_CHANCE` **1/16**; `SLUG_GRAZE_MAX` |n·vhat| ≤ **0.52** (dead-on still punches). Reflect incoming vel, keep 8–18% (`SLUG_KEEP_MIN`/`MAX` **0.08–0.18**); `SLUG_SPEED_MIN`/`MAX` **2.2–16**. Spent-slug visual `MAX_SLUGS` **24**; scuff mark instead of punch plug. Optional FX bus `Slot::Ricochet` ping at skip point
- **Richer impact geo** — punch vs scuff + `IMPACT_HOLE_VARIANTS` **10** + rim chips + stuck-slug plug (brass SMG / steel DMR+bolt). Rides existing spark/mark path — not a rebuild
- **`casing_draw_m` 55** — `FxDrawDials` hide-not-despawn XZ lane for brass + spent slugs (clamp 8–200 via `live_casing`). #19 row now: `muzzle_draw_m` **28** (8–80) · `spark_draw_m` **55** (8–200) · `casing_draw_m` **55** · `decal_draw_m` **700** (50–2000)
- Tracers / muzzle flash / #19 draw-distance stay; kits / lean / ToD+HDRI / knife / bandage / reload / heat-tune / Locus / Transvoxel / listen-server unchanged. Mag chrome stays diegetic — no second ammo HUD
- Audio: FX bus routes now include ricochet (with fire/dry/reload/cycle/pickup/putdown/Locus/swipe/wrap)
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust STEAL_MAP FX rows

## Closed by fulcrumRust #48 (2026-09-07)

- **Windows builder stay-open + `build.log` tee** — Range Tech polish on #42 one-click. Explorer double-click was closing with no readable success/fail. Does not wrap with `cmd /k`. Still does not touch atelier, HDRI, kits, or terrain
- **Always pause** — `build.bat` pauses on success AND failure (single `:finish` path). `/nopause` is only for `build-and-run.bat` so the game can launch without a mid-script keypress
- **Tee cargo** — repo-root `build.log` (overwrite each run) via PowerShell `Tee-Object`; redirect+`type` fallback if PowerShell is missing
- After successful build, print `dir /T:W` mtime + size of `target\release\app.exe`. Start/end timestamps and `Result: OK` / `FAILED`
- If the Explorer window still vanishes: open `build.log` (README one-liner + on-screen hint)
- **`.gitattributes`** — `*.bat text eol=crlf` so cmd.exe does not skip `pause` on LF-only files
- **`build-and-run.bat`** — no more silent `exit /b 1` on build failure — pause and point at `build.log`
- Quality/flag options remain open / not invented here (Lab-Rat may mirror for pycelium later)
- Peek: double-click `build.bat` on Windows; window stays; `build.log` in repo root
- Linux/CI unchanged. Detail: fulcrumRust `build.bat` / `build-and-run.bat` + house `FULCRUMRUST_LAST_PASS_LOCK.md`

## Closed by fulcrumRust #51 (2026-09-07)

- **AXIS_LOCK** — three spaces, do **not** unify. Camera/viewmodel local **−Z** (hold offsets, FP kit, `ejectionPort`); CE FBX **+X** (`rotY − π/2` after FP is already −Z aligned); sim barrel / FX **+Z** (`axis::sim_barrel_basis`). Pawn world look at yaw 0 is **+Z** (hideout door / extract yard) — same *vector* as arcade sim barrel when the bore matches look; **not** camera-local −Z
- **FX on barrel +Z** — #47 leftover feel-lab FX (flash / tracers / impact / stuck-slug / brass / ricochet) sits on `sim_barrel_basis`. Brass toss stays camera-right; brass long axis is barrel +Z, not toss, not camera −Z. Sideways plugs/chips/brass were camera −Z mixed into barrel geo
- **Lab-Rat stamps stay +Y** — mesh ingest is authored +Y up, CCW from outside. Do not rotate stamps to fix sideways plugs
- **Evan dizzy-play** (supersedes stale #12 wording where it conflicts):
  1. **Invert horizontal mouse** — subtract look X (mouse-right looks left at yaw 0). Old #12 "mouse-right increases yaw" is stale
  2. **Invert A/D strafe** — including slide A/D bias. Eye formula stays `+lean → −flat_right`. **#59 Q/E binds:** Q = peek right (−lean), E = peek left (+lean)
  3. **Hideout door** — keep **F** prompt; walk-into-door no longer auto-deploys. Must press F
  4. **Jump** — **Space** single hop shipped #51. **Superseded #59:** CE hop + one air hop + land duck / shake. Prior FPS-first "no double-jump" / single-jump-only is superseded (same way #51 superseded earlier "no jump")
- Do not unify the three forwards to "fix" FX. #12 look/move/gun + tracers and #25 wall clamp / spring / yard covers stay. Lean sign + depth live on #59
- Detail: house `AXIS_LOCK.md` + `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust `docs/AXIS.md` / `engine/src/axis.rs`

## Closed by fulcrumRust #54 (2026-09-07)

- **Authored SFX file slots** — Range Tech feel-lab `sfx.slots[id]` on the **same** #21 FX bus (not a second mixer). `mixer.play(Slot::*)` loads `assets/sfx/<id>.wav` (or `FULCRUM_SFX` override). Options Audio FX dial scales the buffer. Missing / bad file → existing procedural fallback
- **File-backed slots** — fire, dry, reload_release / insert / seat, pickup, putdown, swipe, wrap, footstep, slide, jump, land (placeholder WAVs ~22.05 kHz 16-bit mono). `.ogg` names reserved; decode WAV-only this beat
- **Move cues live** — walk rustle, sprint-crouch slide, Space hop + land. Weapon cues already on FX now prefer the file
- **Ownership** — Range Tech owns weapon/move SFX on the FX bus; Augury (Chamber) keeps spatial (#27) + authored reverb volumes (#56); Lab-Rat stamps stay quiet. Evan lock: all authored audio comes over (clothing rustles, rattles, slides)
- **#54 remains the wiring ship** — file slots on the #21 FX bus + placeholder WAVs. Day-one handmade atelier vendor **landed #62** (small set into FILE_SLOTS; not a full CE / aim-offset pack dump). Shot propagation still later. Do **not** claim every future authored music/SFX pack or Augury authored+CE synth mix as done. Controller feel-medium dials shipped #57 — that is not this row
- Left alone: AXIS_LOCK, Locus brains, terrain/stamps, Options Graphics. No second mixer
- Detail: house `EXTRACTION_AUDIO_LOCK.md` + `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust `assets/sfx/README.md`

## Closed by fulcrumRust #55 (2026-09-07)

- **Hypha GPU post stack live** — wires #46 Graphics toggles so they change the image. Flags already persisted via `project.json` / `FULCRUM_SETTINGS`; previously no-op'd
- Scene color + sampleable depth, then one fullscreen wgpu pass (Mycelium `POST_PASS_ORDER` compressed):
  - **AO** — depth hemisphere SSAO (8 taps; Mycelium `ssao.rs` DNA, no G-buffer)
  - **AA** — luma-edge FXAA (Mycelium `fxaa.rs`; TAA later)
  - **CA** — radial R/B offset; strength slider already in Options
  - **Grain** — hashed film grain last so FXAA does not eat it
  - **DoF** — then far-field blur only (viewmodel stayed sharp). **#68** adds the ADS near layer on the same pass / same Options **DOF** flag (ADS near + far)
- **#66** colorless muzzle heat sits on this same pass: `heat_warp_uv` before scene color sample. Lattice is post input only — no world-pipeline orange card
- HUD / glasses still draw on the swapchain after post
- Not packed into Range Tech ToD / Goegap lighting params
- Smoke: `post=aa` (default AA on); keeps #54 `sfx=file/`
- Headless naga parse/validate of the post WGSL
- Honest: toggles change the image. Not the full Mycelium HDR bloom / god-ray / contact-shadow chain
- Stay out: Atelier, Range Tech bat/HDRI ToD/shoot feel/FX file slots, Augury title mark/HOLD/reverb
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` / `AESTHETIC_DIEGETIC_LOCK.md`

## Closed by fulcrumRust #56 (2026-09-07)

- **CE reverb volumes** — The Augury. Authored AABB proxies replace the #27 phase-only two-zone stub. Hideout interior **DRY** · extract yard pad **YARD** · open extract **OUT** (wetter / longer tail)
- **FX wet send only.** Voice / Music stay dry dual-mono. Same #21 bus tree — not a second mixer. #54 file slots still render through that FX wet send
- **Peek** — glasses `DRY` / `YARD` / `OUT` (labels only, never a second ammo HUD). Listener follows camera. **No extra bind.** Walk off the yard pad to hear outdoor
- Smoke: `audio=100% zone=EXTRACT spatial=1.00 sfx=file/13` (`cargo test --workspace` 329 passed)
- Does **not** steal Range Tech mixer / file slots (#21 + #54) or Hypha Options Graphics post (#55)
- Detail: house `EXTRACTION_AUDIO_LOCK.md` + fulcrumRust `engine/src/audio.rs`

## Closed by fulcrumRust #57 (2026-09-07)

- **Feel medium polish** — Range Tech. Embodied feel pass (Evan lock): aim-offset guns/attachments/controller as steal source; CE/FoW for embodied cues — **medium** into fulcrumRust. Tune dials only; do not rewrite the controller. [PR #57](https://github.com/initialvisuals/fulcrumRust/pull/57) (`a678468a` / `e1c05b76`)
- **Dials** (feel-lab → medium shipped):
  - Look inertia: instant → queue **26** (CE camera_fx heavier; flick conserved)
  - ADS look / blend: 1.0 FOV-only / 8 → **0.86** / **6.4** (extra weight only while aiming)
  - Sprint high-ready: 9 → **6.2**
  - Slide carry: 9.6 / 0.88 / 1.2 → **10.3 / 0.98 / 1.02**
  - Jump land punch: none → **0.052** rad overlay (does not write `pitch`)
- **AXIS_LOCK** three spaces stay. No materials / range geo
- Binds stay #12 + #51 invert look/strafe + F-only door. **#59** landed Q/E flip + CE hop + H crossover. Hypha #55 GPU post and Augury #56 DRY/YARD/OUT reverb volumes kept
- Day-one handmade SFX vendor **landed #62** — that is audio files, not these controller dials
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust PR #57

## Closed by fulcrumRust #58 (2026-09-07)

- **Quiet grit greyscales** — Lab-Rat. Authored grit from a tiny atelier sample set now modulates stamp height + wear/rough on the extract yard, layered **under** loud void-spore / webbing / Inked leftover scars. [PR #58](https://github.com/initialvisuals/fulcrumRust/pull/58) (`f3be0d4f`)
- **Vendored bake-downs** — three 256² luma crops in `assets/stamps/` (~83 KB total): `grit_grunge.png` ← atelier `grunge_4.png` · `grit_crack.png` ← `paint cracks.png` · `grit_dust.png` ← `dust and smudge_2.png`. Already bake-down sized — **not** raw 4k 48-bit
- **`engine/src/grit.rs`** — tiled world-XZ maps (stamp **+Y** height). Yard-weighted; far guts stay heightfield-only
- **`sample_channels`** — quiet height under compiled content so loud scars stay landmarks
- **Wear** — Hypha vertex wear scale picks up `grit::rough` beside 2D-density cracks / `WearStamp`s
- **Overrides** — optional read-only: `FULCRUM_GRIT=` (same filenames) or `FULCRUM_ATELIER=` (local checkout, downsample on load). No submodule. No atelier writes
- Smoke prints `grit=vendor` (or `atelier` / `dir` if override)
- Out of scope: Range Tech controller / lean / jump / heat / ballistics. Augury Locus. Hypha Transvoxel tables. Atelier repo writes. Hypha ring-mip texture LOD later landed #60 (this PR owns the quiet near packs only)
- Detail: house `STAMP_FEEL_LOCK.md` + `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust `docs/STAMPS.md` / `docs/CHANNELS.md`

## Closed by fulcrumRust #59 (2026-09-07)

- **Evan peek feel** — Range Tech. Lean, hop, heat look, H crossover, ballistics / distant hit. [PR #59](https://github.com/initialvisuals/fulcrumRust/pull/59) (`6359ae97`). Quiet influence — house words: **crossover shoulder / left-corner peek**. AXIS_LOCK three spaces stay. #51 invert look/strafe + F-only door stay. #57 medium dials stay. #58 grit stays. #56 reverb volumes stay. Kits / ToD / SFX FILE_SLOTS / Options post stay
- **Crossover shoulder / left-corner peek (H)** — authored hip +X ~**0.10** (right). **H** springs the **viewmodel** across the chest to a partial left (~**−0.041**, cap `shoulder_x_min` **−0.055**) — arms-limited, not a capsule/eye slide, not a full mirror, not infinite travel. Extra left probe (`shoulder_viewmodel` **0.12**) helps left-corner leans. ADS keeps **0.32** of the crossover. Viewmodel crossover on the existing H bind (FoW shoulder habit), not a new key
- **Lean flip + deepen** — after #51 invert, **Q = peek right** (same side as inverted A), **E = peek left**. Eye formula stays `+lean → −flat_right`. Depth feel-lab **0.5 / 0.5** (`leanOffset` / `leanMax`), superseding #25 shallow 0.18/0.12. Wall clamp / spring / yard covers from #25 stay
- **CE hop + air hop + land duck/shake** — Evan supersedes #51 no-double. CE `JUMP_FORCE` **12** / `|GRAVITY|` **30**, one air hop, land duck **0.14 m** + shake **0.2** when impact > 8. Horizontal move must not eat `vel.y` (that was why the hop stayed shallow). #57 land punch **0.052** rad overlay stays
- **Heat motion (v77)** — `updateBarrelHeatCardMorph` upward shimmer / lattice crawl stays the **spatial input** (not static orange blobs). Barrel haze RGB `1.0 / lerp(0.14,0.70,h) / lerp(0.025,0.16,h²)` is feel-lab reference. **Live fulcrumRust draw is Hypha colorless post UV warp landed #66** — lattice = post input only; no world-pipeline orange card. Locked card geometry DNA stays on `heat-card-dial-sheet.md` (aim-offset v77). Live fulcrumRust defaults are the **#71 blend** on that sheet
- **Ballistics / distant hit** — tracers live until impact (feel-lab sanity **180 s**, linger **2 s**). Every strike plays FX `hit` (optional `hit.wav` if present; else procedural 780 Hz grit + 220→90). Graze still pings `ricochet`. Day-one FILE_SLOTS vendor **landed #62** (optional `hit.wav` now atelier darkBead; missing → procedural). Shot propagation still later. **#67 Patch A** sits on top (kit-tip spawn + `hip_honest_dir` + tip streak clamp); did not fight Hypha #66 / did not ship heat color
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust STEAL_MAP Range Tech rows

## Closed by fulcrumRust #60 (2026-09-07)

- **LOD-tied grit / material mips** — Hypha. Bake-once Transvoxel distance rings (#16 / #23 / #43) get a mip chain on Lab-Rat #58 quiet grit packs. [PR #60](https://github.com/initialvisuals/fulcrumRust/pull/60) (`15b0a62a`). Range Tech feel / lean / jump / heat stay on #59 (this PR does not fight them)
- **`engine/src/lod_mips.rs`** — single-channel 8-bit height / rough packs (BC4-class, not RGB):
  - **Near (LOD 0, subdiv 16):** Lab-Rat 256² vendor bake
  - **Mid (LOD 1, subdiv 8):** 64² box mip
  - **Far (LOD 2, subdiv 4):** 16² box mip — cheaper texels, softer read
- `sample_channels` and vertex wear (`stamp_wear_scale` + far-ring crack/wear hashes) pick the ring from world XZ
- Far vertex paint drops high-freq grain / ridge hashes (softer material, not a second material story)
- Atelier stays **read-only** — in-repo `assets/stamps/grit_*.png` only
- Smoke: `grit_mips=256/64/16 n=196608 f=768`
- Lab-Rat #58 quiet grit packs remain the near source; Hypha owns the mip chain. Whole roughness→stamp cook is **not** done (further Lab-Rat bake-downs still separate). Near LOD raise **landed #61** (subdivs **32/16/4**; grit mips stay 256/64/16). Next lock = **first big-map brief** (2026-09-08) — not shipped
- Detail: house `TERRAIN_NORTHSTAR.md` + `FULCRUMRUST_LAST_PASS_LOCK.md` + `STAMP_FEEL_LOCK.md` + fulcrumRust `engine/src/lod_mips.rs`

## Closed by fulcrumRust #61 (2026-09-08)

- **Near LOD raise** — Hypha. Bake-once Transvoxel subdivs **16/8/4 → 32/16/4**. [PR #61](https://github.com/initialvisuals/fulcrumRust/pull/61) (`5f52913d`). The A/B #43 deferred. Range Tech feel / Lab-Rat stamps / Augury brains stay; this PR does not fight them
- **Subdivs** — center **32** · ring-1 **16** · outer **4**. Near step stays **2:1** (32→16) so Lengyel transition faces still stitch toward finer neighbours. Outer stays coarse (4)
- **Grid / radius stay #43** — **7×7 / 3 Chebyshev rings / 112 m / 12 544 m²**. Extra far ring still cold
- **Grit mips stay #60** — **256² / 64² / 16²** on the same rings. Far still heightfield-only / cold guts
- Smoke: `terrain_tris=11118 lods=3 subdivs=32/16/4 near_chunk=3290 far_chunk=39 guts_warm=75 guts_cold=216 rings=3 extract_m2=12544 grit_mips=256/64/16 n=196608 f=768`. Far mean ~**84×** cheaper than near
- Parked: live LOD recook · tunnels · runtime carve. Next lock = **first big-map brief** (2026-09-08) — not shipped
- Detail: house `TERRAIN_NORTHSTAR.md` + `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust `docs/TERRAIN.md`

## Closed by fulcrumRust #62 (2026-09-08)

- **Handmade atelier SFX vendor** — Range Tech. Small handmade set of atelier `sfx_/` CE/feel WAVs into fulcrumRust `assets/sfx/` FILE_SLOTS. [PR #62](https://github.com/initialvisuals/fulcrumRust/pull/62) (`1b949794`). #54 remains the **wiring** ship (file slots on the #21 FX bus). #62 fills those slots. Placeholders from #54 replaced
- One 22.05 kHz 16-bit mono WAV per FILE_SLOTS id, plus optional `hit.wav`. Missing / bad file still → procedural fallback
- Mapped (atelier main `f094157`, **read-only** — no clone / no write):
  - fire ← vector SMG last-with-tail
  - dry ← weapon_shoot_failure
  - reload_release / insert / seat ← vector mag remove / insert / cock
  - pickup / putdown ← PickupA / foley_grab
  - swipe ← locus movement_woosh_air
  - wrap ← rustling
  - footstep / slide / jump / land ← concrete steps + gear_rattle
  - hit.wav (optional) ← darkBead_impact1
- Mixer, Options Audio FX dial, and Augury spatial / #56 reverb stay untouched. Lab-Rat stamps stay quiet
- Honesty: small handmade vendor — not a full CE / aim-offset pack dump. Shot propagation still later. Future extra FX ids / authored+CE synth mix remain open
- Atelier stays **read-only**
- Evan peek: fire SMG, dry-click empty, tap-R reload, F/Z pickup-drop, swipe, wrap, walk/slide/hop — cues should read CE/feel clothing + Vector, not tiny placeholder beeps
- Detail: house `EXTRACTION_AUDIO_LOCK.md` + `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust `assets/sfx/`

## Closed by fulcrumRust #64 (2026-09-08)

- **Music playlist beds** — Range Tech. Shuffle of five atelier `music/` titles on hideout / extract: CONCRETE_ECHO · Terraform · The Memory of The Augury · guttertrash · A Shattered Remnant From A Collapsed Distant Star. [PR #64](https://github.com/initialvisuals/fulcrumRust/pull/64). Small 8 s / 22.05 kHz / 16-bit mono loops in `assets/music/` (not the 5–11 MB MP3s). Each hideout / extract start advances the shuffle. Options Audio Music dial still scales. Missing → two-tone stub. Same #21 tree; Music stays dry dual-mono (#56). Voice / FX / Augury spatial+reverb untouched
- **Kit metal/grit PBR stub** — Range Tech. Store `dBXpg` greeble pack was **not** on the shelf — still **open**/missing. Used TRIMSHEET_MICRO (+ grey) + atelier MetalPanelRectangular / MetalCorroded 256² crops + handful of scratch / fingerprint roughness masks. Boxes stay color-only (stub PBR): albedo mix + roughness/mask on MP9-Z / SR-25 / M24. House DNA: **gold+black tech trim** hairlines, not gold-plate, not Locus veins. Crops in `assets/kit/`. Do **not** claim full metal-tech / `dBXpg` kits shipped
- **SFX remix first application** — fire / foot / reload ±6% pitch/speed jitter on the live #62 FILE_SLOTS vendor. Mixer / Options FX / Augury spatial stay honest (FX `0` still silent). Remix DNA policy stays; full remix pack minting still **open**
- Atelier stays **read-only** (`FULCRUM_MUSIC` / `FULCRUM_KIT` / `FULCRUM_ATELIER`)
- Detail: house `EXTRACTION_AUDIO_LOCK.md` + `AESTHETIC_DIEGETIC_LOCK.md` + `FULCRUMRUST_LAST_PASS_LOCK.md`

## Closed by fulcrumRust #66 (2026-09-08)

- **Colorless muzzle heat** — Hypha. Live heat tell is **colorless post UV warp** — not an orange world-pipeline card/lobe draw. [PR #66](https://github.com/initialvisuals/fulcrumRust/pull/66) (`05dd80ad`). Same #55 fullscreen post stack; HUD / glasses still after post
- **World draw gone** — heat cards are no longer drawn through the opaque world pipeline (removed world-pass indexed draw of heat mesh). A same-pass card cannot refract the scene behind it and instead read as opaque orange
- **Lattice = post input** — existing tip-anchored heat lattice kept only as spatial input → one post field `post.heat: vec4` = center UV.xy, strength, radius
- **`heat_warp_uv`** — fullscreen post applies animated UV displacement **before** scene color sample. Warped scene color is the entire tell — no orange RGB / emissive heat-card output
- **Lattice RGB forced to zero** — this path cannot become an orange draw
- Energy cook remains Range Tech `FeelState.barrel_energy` / heat-tune hold-**J**. Live card defaults are the **#71 blend** on `heat-card-dial-sheet.md` (v77 / dump stay DNA). Hypha owns the post path
- Intact siblings: #59 v77 shimmer intent (lattice crawl stays spatial input); #67 Patch A muzzle (explicitly did not fight #66); #68 ADS viewmodel DoF on the same post stack; #55 GPU post stack; **#71 dump-dial blend** (Range Tech; did not reopen orange cards)
- Do **not** invent new Graphics sliders or claim full Mycelium bloom/god-ray heat. First big-map / `dBXpg` / Lab-Rat atelier plugs stay **not shipped**
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust `engine/src/post.rs` / `engine/src/render.rs`

## Closed by fulcrumRust #67 (2026-09-08)

- **Patch A muzzle tip + honest hip fire** — Range Tech. Hip-fire was leaving the receiver/handguard and drifting upper-right of the reticle. ADS was already fine. Focused slice — no new systems, no heat-card color, no Lab-Rat terrain, no fight with Hypha #66. [PR #67](https://github.com/initialvisuals/fulcrumRust/pull/67) (`258b90fb`)
- **Spawn origin** — was feel-lab socket center (`muzzle_local` z=−0.405, flash-hider middle). Now front face of the forward-most **heat-tagged kit box** (birdcage / can) via `kit_mesh::muzzle_tip_local` (same DNA the viewmodel already draws). `muzzle_socket_local` stays the authored fallback
- **Hip launch** — was SIM 100 m HoB from a right-low hip muzzle → close-range **up + right** of the reticle. Now `hip_honest_dir`: ads=0 stays on **aim**; ads=1 keeps the SIM HoB/zero solve. Uses existing ADS↔hip weight. Not a new cone. **O** still changes the zero; it bites when aimed. **#76:** **P** unused — no arcade dir
- **Streak** — was `tracer_len` (0.55 m) used as a **receiver skip**; then a 10 m box drawn backward through the gun. Now spawn **on the tip**. `tracer_len` is length again. Back of the streak clamped to the tip (feel-lab tip→impact). Distant speed scale kept once the slug is past the gun
- Intact: **O** HoB zero (#33; **#76** SIM-only — **P** unused); tracers-until-impact + FX `hit` (#59). This PR did **not** ship heat color and did **not** fight Hypha #66 (colorless post warp **landed #66**). Lab-Rat terrain untouched. Profile/stash/MP/hands/inventory still open
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust STEAL_MAP ballistics row

## Closed by fulcrumRust #68 (2026-09-08)

- **ADS viewmodel DoF** — Range Tech. Steal aim-offset ADS viewmodel DoF into Hypha’s existing fullscreen `engine/src/post.rs` stack. One pass — no second composer, no new Options system. [PR #68](https://github.com/initialvisuals/fulcrumRust/pull/68) (`266ab088`). Source: feel-lab `ADS_DOF_*` / `adsDofAmount` / `initAdsDof`
- **ADS near DoF** — Disc blur on near depth when ADS + Options **DOF**. Depth stand-in for feel-lab `VIEWMODEL_LAYER` (single RT). Gun softens under ADS; hip + range stay sharp on that layer
- **Radius** — **0.0048** UV-x at ads=1 (range 0–0.012). `ADS_DOF_RADIUS`
- **Taps** — **12** (range 4–24; plus center + inner ring). `ADS_DOF_TAPS_DEFAULT`
- **Amount** — `ads_factor` (skip < 0.02); hip = 0. No hold-breath / vault / reload terms
- **Breath mul** — **1.6 parked** (constant + test only). Space is hop here; no hold-breath bind
- **Near fade** — Full soften ≤ **0.90 m**, gone by **2.20 m**. Kit tip ~0.7 m; range stays sharp
- **Far DoF** — smoothstep **9 → 46 m**, unchanged (#55)
- **Toggle / persist** — Same Options **DOF** / `project.json` `depth_of_field`. Drives both near + far layers
- Intact: #55 GPU stack / far DoF / Options persist. No second composer. No new Graphics sliders. This PR did **not** ship heat color — live tell is Hypha #66 colorless post warp on the same stack. Lab-Rat / profile / stash / MP / hands / inventory untouched
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust `engine/src/post.rs`

## Closed by fulcrumRust #71 (2026-09-08)

- **Heat dial blend toward aim-offset dump** — Range Tech. Live `HeatDials` sit **between** the previous fulcrum bake and Evan’s later dump. [PR #71](https://github.com/initialvisuals/fulcrumRust/pull/71) (`117c8baa`). Seat: Range Tech owns heat dials on the Hypha **#66** colorless post path. Dump-dial blend cooking/~ → **landed/X**. No orange card redraw
- **Key now (blended):** haze_strength **0.07** (was 0.01 / stolen 0.11) · card_size **0.83** (1.01 / 0.71) · scale_x **0.396** (0.69 / 0.20) · scale_y **1.745** (1.63 / 1.86) · segs **26** (31 / 20) · wind **1.40** · friction **1.075** · feather **1.585** · lobe **0.698** (1.22 / 0.35). barrel_heat **0.05** / ground **2.0** / count **14** / masters **true** unchanged
- **Post strength + radius (still #66):** at 0.01 keep lattice amp; at 0.11 use visual × 0.11; default 0.07 lands 60% toward quieter dump; 0 still kills warp. Radius: card_size + lobe pull scale/cap from 0.65/0.18 toward 0.50/0.12; lattice bbox still anchors. WGSL `heat_warp_uv` unchanged. Overlay disc lobe stays parked (`HEAT_LOBE_DISCS = 0`)
- Intent: organic gas, less cartoony/wobbly. Tip-anchored lattice DNA stays. No second heat system. Glasses / live sheet still drive fields. v77 / aim-offset dump stay DNA on `heat-card-dial-sheet.md`
- Intact: #66 colorless path · #59 lattice crawl as spatial input · #67 Patch A · #68 ADS near. Do **not** reopen orange cards
- Detail: house `heat-card-dial-sheet.md` + `FULCRUMRUST_LAST_PASS_LOCK.md`

## Closed by fulcrumRust #76 (2026-09-09)

- **SIM-only launch** — Range Tech. Flips #33’s dual-path launch to one live model. No projectile rewrite, no heat, no terrain. [PR #76](https://github.com/initialvisuals/fulcrumRust/pull/76) (`28be5580`). Seat: Range Tech. Ledger: `[X] sim-default / single model (#76 Range Tech)`
- **Launch path** — was **P** arcade↔sim (`hob_zero` false = aim-dir, true = HoB + gravity / zero). Now **SIM only** — live HoB + gravity / zero solve in `muzzle_and_launch`; `!hob_zero` aim-dir return dead; leftover `hob_zero` ignored
- **P** — unused (no new bind). `FeelSheet::toggle_hob_zero` + session **P** apply gone; **P** no longer sets an input edge
- **O** — still cycles 50 / 100 / 200 m zero presets (`FeelSheet::cycle_zero`). Shared across kits
- **Bake** — not a precomputed trajectory. `solve_ballistic_launch` stays the feel-lab low-arc solve so shots share one deterministic model
- **#67 hip honesty stays** — `hip_honest_dir`: ads=0 on aim; ads=1 keeps this SIM solve. Per-kit recoil / `yaw_walk` stay (MP9-Z kick 1.0 · SR-25 1.15 · M24 1.75 + distinct walks)
- Toast / glasses: `ZERO  {n} M` stays; `LAUNCH  ARCADE` / `LAUNCH  SIM` gone. Glasses `Z{n}  SIM` only — never `ARCADE`
- Intact: #67 hip honesty · per-kit recoil cones · **O** zero · #59 tracers-until-impact. Do **not** invent a new bind for **P**
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust `muzzle_and_launch` / `solve_ballistic_launch`

## Controller lock (Evan bind wins)

Shipped in fulcrumRust #12. Overrides soft aim-offset wheel-height where they disagreed:

- **Q / E** — **Q = peek right** (same side as inverted A) · **E = peek left**. Eye formula stays `+lean → −flat_right`. Depth **0.5 / 0.5**. #25 wall clamp / spring / yard covers stay
- **H** — viewmodel **crossover shoulder / left-corner peek** on the existing FoW H bind (landed #59). Not a capsule/eye slide
- **Shift then Ctrl** — slide carry (sprint + crouch rising edge)
- **Hold Ctrl + mouse up/down** — analog eye height (does **not** pitch-look)
- **Mouse wheel** — move speed (**not** height; aim-offset uses wheel for crouch height — Evan’s bind wins)
- **Space** — CE hop + one air hop + land duck / shake (landed #59). Prior FPS-first "no double-jump" / #51 single-hop-only is superseded (same way #51 superseded earlier "no jump")

## Holding steady

- Hypha: distance activation / far-guts cold landed (#23) on #16 host; extract sky sample shared with Range Tech clock (#24); **#27 binaural / positional stereo on FX landed** (partial — shot propagation later; file-slot wiring landed #54; handmade vendor landed #62); **#34 listen-server / invite stub landed** (partial — handshake/presence only; world sync / dedicated infra parked); **#42 Windows one-click release builder landed** (basic; quality/flag still open); **wider extract chunk radius landed (#43)** (7×7 / 3 rings / 112 m / 12 544 m²; extra far ring only); **near LOD raise landed #61** (subdivs **32/16/4**; near step 2:1; outer stays 4); **next lock = first big-map brief** (2026-09-08) — **not shipped** (drop walls · ~8× · chunked Transvoxel · load chunks by distance from players, listen-server aware; continues on fulcrumRust); **#46 Options guts landed** (Graphics/Gameplay/Controls + borderless default + persist — steal CE/Mycelium; does not dump atelier into Options); **#55 GPU post stack landed** (AO/AA/CA/grain/DoF fullscreen wgpu; toggles change the image; smoke `post=aa`; not full HDR bloom / god-ray / contact-shadow); **colorless muzzle heat landed #66** (`heat_warp_uv` before scene sample; lattice = post input only; no world-pipeline orange card; HUD/glasses still after post); **ADS viewmodel DoF landed #68** (ADS near + far on that same pass / same Options **DOF**); **LOD-tied grit / material mips landed #60** (near **256²** Lab-Rat vendor / mid **64²** / far **16²** BC4-style 8-bit; far drops grain hashes; in-repo grit mips stay until Lab-Rat cooks more; smoke `grit_mips=256/64/16 n=196608 f=768`); Lab-Rat **#58 quiet grit greyscales** remain the vendored near packs (not the whole roughness→stamp cook); next live LOD recook / tunnel cutouts / SVG density-mask ingest; keep sit-on-surface CPU boxes as peek leftover
- Augury: Locus Standard (#18) + Inked (#26) landed; spatial CE DNA via #27; **#56 CE reverb volumes landed** (DRY / YARD / OUT AABB proxies; FX wet send only; glasses peek; two-zone stub retired); **Chamber owns spatial/reverb** (does not take file slots); **down/death stub #36 landed** (partial — death cam / teammate net stabilize / timed surface kill / full loot loop later); **#37 I-stim / Y-host bind lock**; **#41 FoW title mark landed** (vendored CE header on the #11 shell); **#45 title+HOLD analysis-core polish + Options list shell landed** (white frames / white hairline; HOLD **SYSTEM PAUSED**; Graphics/Audio/Gameplay/Controls list — Audio live #21); Hypha tab guts / window / persist shipped #46 — not a second overlay; **#55 GPU post live** (HUD/glasses still after post); **#66 heat warp** sits on that stack; **#68 ADS near** sits on that stack (same Options **DOF**); **#51 dizzy-play landed** (invert look + A/D, F-only door); **#59 hop landed** (CE hop + air hop + land duck/shake — #51 single hop superseded); FoW brand / menu video **when cut ready** (big-map brief); next Sonderer/Monk/Oculus/crawler + stamp spawn filters (prefer rock/concrete; avoid organic)
- Lab-Rat: void-spore grimdark + density-driven concrete wear landed (#20); **#30 loud Inked void-spore hotspot landed**; **#38 shape-agnostic stamp/paint substrate landed** (channels + primitives; no new scar kinds; yard/Inked/curl stay consumers); **#39 extract-yard scale harness landed** (`apply_yard_harness`, pad ≈110 m², near-warm/far-cold; smoke `layers=`/`prims=`/`yard_m2=`); Hypha #43 `ExtractStubHost` rides **7×7** (`STUB_GRID = 7`; smoke may also show `rings=` / `extract_m2=`); stamps stay **quiet on audio**; **quiet grit greyscales landed #58** (vendored 256² `grit_{grunge,crack,dust}.png` + `sample_channels` quiet height + `grit::rough` wear; smoke `grit=`); further roughness → stamp stays on **fulcrumRust only** — bake greyscales **down before density** (8-bit / half-res / BC4-style height packs); do **not** ship raw 4k 48-bit into the yard; atelier plugs **open** (Evan **clean** yell 2026-09-08 ~00:00 ET); PBR batch **in** (150 roughness + textures/PBR ~26 sets) — grit / slope / PBR plugs **open**; first big-map brief owns slope/angle + dirt/scatter/deform — **not shipped**; Holocron rust rewrite **after** slope/PBR (`TOOLS.md`); next wet-lab beats stay on STEAL_MAP (SVG/density-mask ingest / experiment log)
- Range Tech: day/night clock + sky (#24), wall-clamped lean (#25), hold-` inspect (#28), bandage use (#31) landed; **#32 reload DNA landed** (Hold-R peek / tap-R reload / double-tap SWAP); **#33 live HoB zero landed** (**#76** SIM-only — **P** unused; leftover `hob_zero` ignored; **O** 50/100/200 stay); **#35 heat-tune dump landed** (hold-J; **I** is Augury stim #37); **#40 Goegap HDRI on extract ToD landed** (/** plate toggle; glasses `HDRI` / `PROC`); **#47 leftover feel-lab FX landed** (brass eject / graze ricochet + spent slug / richer impact geo / `casing_draw_m` **55**); **#51 AXIS_LOCK landed** (cam −Z / CE +X / barrel +Z; Lab-Rat +Y separate; FX on `sim_barrel_basis`; dizzy-play invert look/strafe + F-only door); Voice/Music/FX buses (#21) carry Hypha/#27 spatial + #47 ricochet ping (**FX bus live**); **authored SFX file-slot wiring shipped #54**; **handmade atelier vendor landed #62** (weapon/move off CE/feel `sfx_/` into those buses; rustles / rattles / slides come over; small set, not a full pack dump; missing → procedural); shot propagation still later; one-click Windows `build.bat` **#48 stay-open + `build.log` tee landed**; quality/flag options still cooking / open (Lab-Rat mirror for pycelium later — no dials invented here); **feel medium polish landed #57** (look inertia queue **26**; ADS look **0.86** / blend **6.4**; sprint high-ready **6.2**; slide carry **10.3 / 0.98 / 1.02**; jump land punch **0.052** rad overlay; AXIS_LOCK stay; no materials/range geo); **Evan peek landed #59** — **crossover shoulder / left-corner peek** (H viewmodel; authored hip +X ~0.10 → partial left ~−0.041, cap `shoulder_x_min` −0.055; ADS **0.32**); lean flip + deepen (**Q = peek right** / **E = peek left**; depth **0.5 / 0.5**; #25 clamp/spring/yard stay); CE hop + air hop (`JUMP_FORCE` **12** / `|GRAVITY|` **30**; land duck **0.14 m** + shake **0.2** when impact > 8; #57 land punch **0.052** stays); heat motion v77 shimmer / lattice crawl stays Range Tech spatial input / `barrel_energy` / hold-J; **live tell is Hypha colorless post UV warp landed #66** (lattice = post input only; no world-pipeline orange card); tracers live until impact (sanity **180 s**, linger **2 s**) + FX `hit`; **Patch A muzzle landed #67** — kit-tip spawn (`muzzle_tip_local`) + `hip_honest_dir` (ads=0 on aim; ads=1 SIM HoB/zero) + tip→impact streak clamp (`tracer_len` is length, not a receiver skip); hip-fire no longer behind the handguard / upper-right of the reticle; **O** + #59 tracers-until-impact stay; **P** unused (#76); #67 did **not** fight #66 and did **not** ship heat color; **ADS viewmodel DoF landed #68** — disc blur on near depth when ADS + Options **DOF** (radius **0.0048** UV-x at ads=1; taps **12**; amount `ads_factor`, skip < 0.02; hip = 0; near fade full ≤ **0.90 m**, gone by **2.20 m**; far DoF smoothstep **9 → 46 m** unchanged; breath mul **1.6 parked**); same #55 pass / same Options **DOF**; gun softens under ADS; hip + range stay sharp on that layer; #68 did **not** ship heat color (live tell is Hypha #66); **heat dial blend landed #71** — live defaults sit between old bake and the dump (haze **0.07** / size **0.83** / scaleX **0.396** / lobe **0.698**; #66 colorless path stays; no orange card redraw); **SIM-only launch landed #76** — one HoB + gravity / zero model; arcade aim-dir dead; **P** unused; leftover `hob_zero` ignored; **O** 50/100/200 stay; #67 hip honesty on the single SIM model; Lab-Rat terrain untouched; first big-map brief: kits + FX draw-distance on the wider yard; kit metal/grit PBR stub **landed #64**; store `dBXpg` still **open**; **SFX remix DNA** (pitch/speed/effects; indie underground; don’t overuse the same stem) — first ±6% fire/foot/reload jitter **landed #64**; full remix minting still **open**; Music playlist beds **landed #64**
- Atelier: plugs **open** (Evan **clean** yell 2026-09-08 ~00:00 ET). PBR batch **in** (150 roughness + textures/PBR ~26 sets). #58 optional `FULCRUM_GRIT=` / `FULCRUM_ATELIER=` stay read-only **load** paths (downsample on load). Lab-Rat further roughness → stamp stays on fulcrumRust only — bake-down first; grit / slope / PBR **open**; do **not** ship raw 4k 48-bit PNG into the yard

Steal from this shelf + steal map. Not chat scroll.
