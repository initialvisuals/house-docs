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
- **Sign lock** — **Q** = left / +lean · **E** = right / −lean (do not invert)
- **Dials** — `lean_offset` **0.18** · `lean_roll` **0.12** · `lean_spring` **8.0** · `lean_skin` **0.08** · `lean_viewmodel` **0.16**
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
- Reverb zone stub: hideout (tight / drier) vs extract (industrial yard)
- Smoke: `audio=100% zone=EXTRACT spatial=1.00`; FX `0` still silences fire; `Slot::Locus` rides FX
- File slots / shot propagation later. Detail: house `EXTRACTION_AUDIO_LOCK.md` + fulcrumRust `engine/src/audio.rs`

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

- **Live HoB zero + arcade/sim launch** — per-kit rpm/recoil/HoB sheet was already authored (#22); this PR makes zero distance + arcade↔sim **live**
- **Dials** — `ZERO_PRESETS_M` **[50.0, 100.0, 200.0]** m; default `zero_dist_m` **100**; default `hob_zero` **true** (SIM)
- **O** — cycle live zero presets 50 → 100 → 200 → 50 (HoB solve). Shared across MP9-Z / SR-25 / M24 so G-swap does not hide the solve (`FeelSheet::cycle_zero`)
- **P** — arcade (aim-dir launch) ↔ sim (height-over-bore + ballistic zero) via `hob_zero` (`FeelSheet::toggle_hob_zero`). Shared launch mode across kits
- **Honesty** — changing zero preset changes muzzle **launch dir** only (not muzzle position); arcade vs sim launch dirs differ; sim aims up to meet sight zero; arcade launches along aim
- Toast: `ZERO  {n} M` / `LAUNCH  ARCADE` / `LAUNCH  SIM` (age **1.2s**, `Slot::Cycle`)
- Glasses status strip (labels only, never a second ammo HUD): `Z{zero_dist_m:.0}  SIM|ARCADE` e.g. `Z100  SIM`
- Intact / do not steal: **[ ]** stay ToD clock; **−/=** stay exposure; **9/0** left free; does not steal T/C/R/Q/E/Z/B/V/N/U/`/F/X/H/1/2/3/G/Mouse4; tip→impact tracers / muzzle / sparks stay; reload / knife / bandage / lean / inspect / ToD stay seated
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust `FeelSheet::cycle_zero` / `toggle_hob_zero`

## Closed by fulcrumRust #35 (2026-09-07)

- **Hold-J heat-tune dump** — Range Tech; hold **J** = heat-tune dump. **I** is no longer free — I is Augury stim (#37).
- **Feel** — sustained AUTO on the seated kit (`FeelState::try_heat_tune` / `fire_shot(..., heat_tune: true)`); uses kit `auto_interval_sec` while tuning (ignores SEMI hold gate)
- Recoil impulse + camera punch skipped; leftover LMB punch stomped while J is down (`recoil_punch` / `recoil_rot` / `cam_recoil_p` / `cam_recoil_y` zeroed) so the gun stays still
- Same cook path: `FeelState.barrel_energy` still climbs so tip cards + lobe go live for live dialing (no second heat cook)
- **Ammo dial cheat** — mag **still spends** while holding; **release refills** the seated mag via `DayOneKit::refill_mag` (tops stick to `smg_mag_size`, does **not** spend a reserve)
- Glasses: `HEAT TUNE` label only (amber-ish overlay) — never a second ammo HUD; must not count mag rounds
- Intact / do not steal: ToD **[ ]**/K/L/−/=/,/. · lean Q/E · inspect ` · reload R · knife Mouse4/C · bandage T · O/P zero/launch · I stim · Y host · O/P/T/C/R/Q/E/Z/B/V/N/U/`/F/X/H/G/I/Y/1/2/3/Mouse4
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
- Intact / do not steal: **I** stim (#37), **O**/**P** HoB zero (#33), hold-**J** heat-tune (#35), T/C/R/Q/E/Z/B/V/N/U/`/F/M/1/2/3/Mouse4
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

- **Extract-yard scale harness** — Lab-Rat expanded the extract yard into a scale/perf harness for the #38 stamp/paint substrate. Stay on the extract yard — not a bigger world map. No Standard / Monk one-off scars. HDRI stays Range Tech
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
- Near LOD unchanged: center subdiv **16**, ring-1 **8**, outer **4**. Do **not** raise near LOD — that A/B stays later
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
- **Graphics (live window + post stubs)** — Window mode live via winit: **Borderless** = default launch; **Windowed** = decorated 1280×720; **Exclusive** = exclusive video mode when OS/GPU expose one, else borderless fallback. Also `--windowed` / `FULCRUM_WINDOW=borderless|windowed|exclusive`. Post toggles persist and are live-read stubs until GPU passes — they **no-op safely** and must **not** be packed into Range Tech ToD / Goegap / HDRI uniforms: AO, AA, CA (+ strength default **0.35**, step **0.05**, range **0–1**), film grain, DoF. Hint: `POST STUB UNTIL GPU · WINDOW LIVE · A/D NUDGE`
- **Gameplay (real)** — Glasses labels toggle + crosshair toggle (real — drop quads when off). Hint: `SHOOT FEEL STAYS · ENTER TOGGLE`
- **Controls** — Look scale sits on feel-lab sens: `LOOK_MUL` default **1.0**, min **0.25**, max **2.0**, step **0.05**; Invert Y toggle. Binds stay README. Hint: `LOOK SITS ON FEEL-LAB SENS · BINDS IN README`
- **Audio** — Untouched — still Range Tech #21 Voice/Music/FX mixer
- **Persist** — `project.json` in cwd, or `FULCRUM_SETTINGS=/path/to.json`
- **Esc walk** — Hypha pane / Audio → Options → title or HOLD (same stack as #45)
- Peek: `cargo run` → Options → Graphics window live; post stubs persist; Gameplay glasses/crosshair; Controls look/invert; Esc backs; Audio still #21
- Ownership: Augury owns title + HOLD chrome + Options list shell + logo seat. Hypha owns Graphics/Gameplay/Controls guts + window mode + post stubs + persist. Range Tech keeps Audio mixer. Still no second ammo HUD. No atelier push
- GPU post passes (SSAO/FXAA/CA/grain/DoF **actual shaders**) still cooking — do **not** claim those shipped
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` / `AESTHETIC_DIEGETIC_LOCK.md` + fulcrumRust STEAL_MAP Hypha settings rows

## Closed by fulcrumRust #47 (2026-09-07)

- **Brass eject** — Range Tech leftover feel-lab FX on the same `TracerField`. Live fire from seated kit `ejectionPort`: `MP9Z_EJECT` **(0.036, −0.014, 0.018)** · `SR25_EJECT` **(0.038, 0.008, 0.018)** · `M24_EJECT` **(0.03, 0.018, 0.055)**. Camera-right toss; `CASING_GRAVITY` **12**; bounce then sleep; `CASING_FADE` **6** s; `MAX_CASINGS` **48**. Hide-not-despawn via `casing_draw_m` **55**. Hold-J heat-tune dump (#35) skips brass so the lattice stays still
- **Ricochet / spent slug** — feel-lab `trySpawnSpentSlugBounce` — **NOT** a bounce table. `SLUG_CHANCE` **1/16**; `SLUG_GRAZE_MAX` |n·vhat| ≤ **0.52** (dead-on still punches). Reflect incoming vel, keep 8–18% (`SLUG_KEEP_MIN`/`MAX` **0.08–0.18**); `SLUG_SPEED_MIN`/`MAX` **2.2–16**. Spent-slug visual `MAX_SLUGS` **24**; scuff mark instead of punch plug. Optional FX bus `Slot::Ricochet` ping at skip point
- **Richer impact geo** — punch vs scuff + `IMPACT_HOLE_VARIANTS` **10** + rim chips + stuck-slug plug (brass SMG / steel DMR+bolt). Rides existing spark/mark path — not a rebuild
- **`casing_draw_m` 55** — `FxDrawDials` hide-not-despawn XZ lane for brass + spent slugs (clamp 8–200 via `live_casing`). #19 row now: `muzzle_draw_m` **28** (8–80) · `spark_draw_m` **55** (8–200) · `casing_draw_m` **55** · `decal_draw_m` **700** (50–2000)
- Tracers / muzzle flash / #19 draw-distance stay; kits / lean / ToD+HDRI / knife / bandage / reload / heat-tune / Locus / Transvoxel / listen-server unchanged. Mag chrome stays diegetic — no second ammo HUD
- Audio: FX bus routes now include ricochet (with fire/dry/reload/cycle/pickup/putdown/Locus/swipe/wrap)
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust STEAL_MAP FX rows

## Controller lock (Evan bind wins)

Shipped in fulcrumRust #12. Overrides soft aim-offset wheel-height where they disagreed:

- **Q / E** — peek left / right
- **Shift then Ctrl** — slide carry (sprint + crouch rising edge)
- **Hold Ctrl + mouse up/down** — analog eye height (does **not** pitch-look)
- **Mouse wheel** — move speed (**not** height; aim-offset uses wheel for crouch height — Evan’s bind wins)
- No double-jump day-one

## Holding steady

- Hypha: distance activation / far-guts cold landed (#23) on #16 host; extract sky sample shared with Range Tech clock (#24); **#27 binaural / positional stereo on FX landed** (partial — shot propagation / file mix later); **#34 listen-server / invite stub landed** (partial — handshake/presence only; world sync / dedicated infra parked); **#42 Windows one-click release builder landed** (basic; quality/flag still open); **wider extract chunk radius landed (#43)** (7×7 / 3 rings / 112 m / 12 544 m²; extra far ring only; near LOD 16/8/4 unchanged); next expand A/B = **near LOD later**; **#46 Options guts landed** (Graphics/Gameplay/Controls + borderless default + persist; post toggles persist as stubs and no-op safely — steal CE/Mycelium; no atelier push); GPU post passes (SSAO/FXAA/CA/grain/DoF actual shaders) still cooking — **not done**; next live LOD recook / tunnel cutouts / SVG density-mask ingest; keep sit-on-surface CPU boxes as peek leftover
- Augury: Locus Standard (#18) + Inked (#26) landed; spatial CE DNA partial via #27; **Chamber keeps spatial/reverb DNA** (does not take file slots); **down/death stub #36 landed** (partial — death cam / teammate net stabilize / timed surface kill / full loot loop later); **#37 I-stim / Y-host bind lock**; **#41 FoW title mark landed** (vendored CE header on the #11 shell); **#45 title+HOLD analysis-core polish + Options list shell landed** (white frames / white hairline; HOLD **SYSTEM PAUSED**; Graphics/Audio/Gameplay/Controls list — Audio live #21); Hypha tab guts / window / persist shipped #46 — not a second overlay; GPU post shaders still cooking; next Sonderer/Monk/Oculus/crawler + stamp spawn filters (prefer rock/concrete; avoid organic)
- Lab-Rat: void-spore grimdark + density-driven concrete wear landed (#20); **#30 loud Inked void-spore hotspot landed**; **#38 shape-agnostic stamp/paint substrate landed** (channels + primitives; no new scar kinds; yard/Inked/curl stay consumers); **#39 extract-yard scale harness landed** (`apply_yard_harness`, pad ≈110 m², near-warm/far-cold; smoke `layers=`/`prims=`/`yard_m2=`); Hypha #43 `ExtractStubHost` rides **7×7** (`STUB_GRID = 7`; smoke may also show `rings=` / `extract_m2=`); stamps stay **quiet on audio**; next wet-lab beats stay on STEAL_MAP (SVG/density-mask ingest / experiment log)
- Range Tech: day/night clock + sky (#24), wall-clamped lean (#25), hold-` inspect (#28), bandage use (#31) landed; **#32 reload DNA landed** (Hold-R peek / tap-R reload / double-tap SWAP); **#33 live HoB zero / arcade↔sim launch landed**; **#35 heat-tune dump landed** (hold-J; **I** is Augury stim #37); **#40 Goegap HDRI on extract ToD landed** (/** plate toggle; glasses `HDRI` / `PROC`); **#47 leftover feel-lab FX landed** (brass eject / graze ricochet + spent slug / richer impact geo / `casing_draw_m` **55**); Voice/Music/FX buses (#21) carry Hypha/#27 spatial + #47 ricochet ping (**FX bus live**); **authored SFX file slots cooking** (weapon/move off CE/FoW packs into those buses; rustles / rattles / slides meant to come over) — **not done** (do not claim file slots shipped); basic one-click Windows `build.bat` **landed as Hypha #42**; quality/flag options still cooking / open (Lab-Rat mirror for pycelium later — no dials invented here); **embodied feel pass cooking** (transpose aim-offset guns/attachments/controller into fulcrumRust, outside materials/range geo; sweet medium vs CE/FoW OG controller + action audio cues) — **not done**

Steal from this shelf + steal map. Not chat scroll.
