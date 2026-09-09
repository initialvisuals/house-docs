# fulcrumRust — last-pass lock (Evan dump 2026-09-06 evening)

Canonical feel / systems answers. Steal map + seats update from this sheet.

## Where to read (2026-09-08)

fulcrumRust owns the port docs: `docs/STEAL_MAP.md`, `docs/AXIS.md`, `docs/TERRAIN.md`, `docs/MILESTONE_01_PLAYABLE.md`, `docs/CHANNELS.md`, plus `STAMPS.md` / `GROWTH_POC.md`. Patch A feedback checkpoint is repo-root `patch notes A.txt` (#72) — `X` / `~` / `*` / `·` ledger + seat owners; not a replacement for STEAL_MAP or MILESTONE. House-docs bake-book is the **dial shelf** — readable enough for seats without reading every `.rs`. Steal from the shelf + steal map. Not chat scroll. Vector mag dump (Range Tech muzzle / FX — **live steal landed #89**) → `VECTOR_MAG_DUMP.md`. Heat cards → `../heat-card-dial-sheet.md`. Pixellation / floor-warp (Hypha post dial **landed #90**; Augury aesthetic only) → this sheet Menus / Post / Graphics dump + sibling **Pixellation / floor-warp**. **1P viewmodel ≠ 3P biped gun** (MP honesty — **partial shipped #91** peer hip gun stub; full 3P kit honesty still open) → this sheet + `PEEK_FINDINGS.md`. **Scope glass** (when LPVO — holding / **not shipped**) + **Evan asset-ask path** → this sheet + `PEEK_FINDINGS.md`. **CE Home debugger** (Augury **landed #110**; Home LOGS COPY / tracker toggles **landed #121**; End stays AIM TUNE) → this sheet + `PEEK_FINDINGS.md`. **Stream hitch amortize** (Hypha **landed #108**; hitch *visibility* stays Augury #110 / #121) → this sheet + `PEEK_FINDINGS.md` Closed by #108 + `TERRAIN_NORTHSTAR.md`. **Transvoxel UV consume** (Hypha **landed #112**; Lab-Rat owns the #101 sheet) → this sheet + `PEEK_FINDINGS.md` Closed by #112. **Subtract crawl pad network** (Lab-Rat **landed #114**; shallow enterable network, not a tunnel sim) → this sheet + `PEEK_FINDINGS.md` Closed by #114 + `STAMP_FEEL_LOCK.md`. **Kit handling / ergo / MOA** (Range Tech **landed #113**; `HandlingStats` / `FeelSheet::handling`; ADS `blend_speed` **6.4** × kit ergo; `hold_spring` **7.0** stays sibling) → this sheet + `PEEK_FINDINGS.md` Closed by #113. **World/sim leftover** (Beabim **landed #119**; KIND_SHOT / KIND_LOCUS / KIND_BODY; peer shot muzzle = biped hip stub; joiner plants soles only) → this sheet + `PEEK_FINDINGS.md` Closed by #119. **Hatch/elevator glasses UX** (Augury **landed #115**; hatch toggle + shaft ride **X**; timed surface kill still `~`) → this sheet + `PEEK_FINDINGS.md` Closed by #115 + `AESTHETIC_DIEGETIC_LOCK.md`. **Door / extract cancel chrome** (Augury **landed #120**; `GATE_SECS` **2.20** / `COOL_SECS` **0.55**; walk-away cancels; timed surface kill still `~`) → this sheet + `PEEK_FINDINGS.md` Closed by #120 + `AESTHETIC_DIEGETIC_LOCK.md` + fulcrumRust `docs/GATE_DIAL_SHEET.md`. **No-pause live sim + KIND_RAID shared instance** (Beabim **landed #122**; mute local pawn only; leftover = `GATE_SECS` **2.20**; honors `Cancelled`; glasses stay Augury) → this sheet + `PEEK_FINDINGS.md` Closed by #122 + fulcrumRust `docs/GATE_DIAL_SHEET.md` KIND_RAID row. **PreferredHand + new-profile onboard** (Hypha **landed #116**; Right default · NEW PROFILE gate · `project.json` permanent vs live · death clears live · extract→stash stub · H seats Range crossover, no mesh flip) → this sheet + `PEEK_FINDINGS.md` Closed by #116. Overnight cooks steal from the shelf.

## Day-one kit
- **SMG** basic 20-round mag
- **4 mags** + one in the gun
- **Knife**
- **Bandage**
- **Stim** (1) — self-revive while downed on **I** (fulcrumRust #37; stub shipped #36); not a standing heal
- Find other weapons on enemies / in boxes / loose in world
- Mag reload is **tap-R** (not empty-only) / **double-tap SWAP** — leftover discarded; Hold-R is peek only (fulcrumRust #32)

## Kit picker + attachments (fulcrumRust #14 + #22)
- Day-one spawn is the **feel-lab MP9-Z silhouette** (procedural boxes), not the brick SMG
- Feel-lab kit stubs also seated: **SR-25** (DMR rail + 20-rd box) + **M24** (bolt + 5-rd clip + scope tube)
- Kit metal/grit PBR stub **landed #64** — boxes stay color-only (albedo mix + roughness/mask) on MP9-Z / SR-25 / M24; TRIMSHEET_MICRO + MetalPanel/Corroded 256² crops + scratch/print masks; gold+black tech trim hairlines, not gold-plate, not Locus veins. Store `dBXpg` greeble pack still **open**/missing. `FULCRUM_KIT` / `FULCRUM_ATELIER` read-only
- **G** cycles MP9-Z → SR-25 → M24; **4 / 5 / 6** seat directly; **U** stays unaimed-hold cycle (Chest → LowHip → Canted; glasses **LOW HIP** on the #99 shotgun step · **CANT 45** on Canted · **CANT ADS** in `ads_cant`); **1 / 2 / 3** stay Lab-Rat curl
- Mag chrome stays diegetic on the seated kit — well count **is** mag size (MP9-Z **20** / SR-25 **20** / M24 **5**); Hold-R peek / tap-R reload / double-tap SWAP (fulcrumRust #32); leftover discarded; no HUD ammo counter
- **V** — cycle optic on the seated kit’s allow-list (SMG iron/holo/acog; SR-25 + scope; M24 iron/scope); ADS pose + FOV follow. LPVO glass (greyscale ramp / IOR / no-PiP bodycam) is **holding** until LPVO — Hypha Graphics when it lands; Range AIM TUNE placements first (#97). Do **not** claim LPVO or glass shipped
- **N** — toggle .45 suppressor / can mounts; muzzle / flash / tracer spawn follow the kit tip (`kit_mesh::muzzle_tip_local` — front of the forward-most heat-tagged box; birdcage / can). `muzzle_socket_local` stays the authored fallback. Landed #67
- FOV lock: hip **90** · iron ADS **60** · holo ADS **60** · acog ADS **25** · canted ADS **60** CQC (#100 — ACOG/scope zoom does not follow a CQC cant)
- Per-kit ballistics (`FeelSheet::fire` + `FeelSheet::handling` **#113**): MP9-Z AUTO ~1200 rpm / 300 m/s / kick 1.0 · SR-25 SEMI 0.14 s / 785 m/s / kick 1.15 · M24 bolt 0.65 s / 810 m/s / kick 1.75; HoB / muzzle / heat τ on the feel sheet (attachments do not invent new gameplay mags). Live ADS blend is `blend_speed` **6.4** × kit ergo (MP9 **8.00** / SR-25 **6.40** / M24 **5.12** — not a fixed stub). Handling scales authored kick / pitch / yaw by `1/handling` (MP9 **1.15** · SR-25 **1.00** · M24 **0.90**; `ads_recoil_mul` **0.6** stays). Hip MOA cone after `hip_honest_dir` (MP9 **4.0** · SR-25 **1.2** · M24 **0.40**; ADS × **0.22**). Mag fill is a reload-clock stub (default **1.0**; authored 1.10 / 0.46 s). Live zero via **− / =** 50/100/200 wrap (fulcrumRust #78; was **O** #33). Launch is **SIM only** — HoB + gravity / zero; leftover `hob_zero` ignored; **P** unused (fulcrumRust #76). Hip honesty via `hip_honest_dir` (ads=0 on aim; ads=1 keeps the SIM solve — landed #67)

## First playable flow
Title **Deploy / Host / Join** gates a **NEW PROFILE** sheet (**landed #116**, Hypha) — must pick RIGHT / LEFT before first raid. Permanent local profile in `project.json`; live raid is a session copy (death clears live).
1. **Loading screens** cover bake/hitch — player never sees hitching except true CPU/geo overload
2. Small **interior hideout** (drawers, tables, lights, pickups, door) — geometry mostly authored
3. World **finalized before** hideout spawn (rigidize-on-start)
4. Door (**F** only — no walk-in auto-deploy, #51; **#120** arms `GATE_SECS` **2.20** countdown, walk-away cancels) → transition → **Forever Winter–style extraction test map** (PoC playground for loop + controller feel)

## World bake (Hypha)
- Prefer proving **hub + extract linked by tunnel** early if it doesn’t block the window; otherwise one medium Forever Winter instance is fine day-one
- Near-spawn **void-spore growth PoCs**: denser 2D webbing, hellish mushroom, spore-tipped creeper (curl **1 / 2 / 3** live)
- **Smart material stamps** (Lab-Rat #15 + #20): dirt/sand/rock/concrete/organic on 8 m cells, grimdark luma + sit-on-surface (void-spore bloom / brutalist mass) + density-driven concrete wear
- **Transvoxel consume channels** (Lab-Rat #17): `sample_channels` / `fill_chunk_samples` — density `> 0` solid; Hypha owns mesher / LOD / tables
- **Shape-agnostic stamp/paint substrate** (Lab-Rat #38): any authored shape → density + material; ChannelOp Union/Subtract/Paint/Replace; paint writes real / UX stubbed; mesh→voxel convert. Yard/Inked/curl stay consumers. Lab-Rat writes; Hypha remeshes
- **Subtract crawl pad network** (Lab-Rat #114): **landed**. Shallow enterable Subtract network under the pad (mouth → mid → pocket → +Z spur + west/east + kink). Radii **0.42–0.50**. `CRAWL_DROP` **0.38** m. Mouth XZ **−1.60, 8.20** · Pocket **0.25, 9.15**. Glasses `CRAWL  SUBTRACT`. Union lip stretches **up**. Pad stays shallow; bowl above `SLAB_Y0` **−0.7**. Full guts / live voxel collide still `[~]`. See `PEEK_FINDINGS.md` Closed by #114
- **Extract-yard scale harness** (Lab-Rat #39): stay on the extract yard; `apply_yard_harness` via `StampField::layers`; pad ≈ **110 m²**; near-warm / far-cold (`guts_cold` **140**); smoke `layers=` `prims=` `yard_m2=`
- **Quiet grit greyscales** (Lab-Rat #58): vendored 256² luma in `assets/stamps/` (`grit_grunge` / `grit_crack` / `grit_dust`); `grit.rs` tiled world-XZ (stamp +Y); `sample_channels` quiet height under loud scars; `grit::rough` wear; `FULCRUM_GRIT=` / `FULCRUM_ATELIER=` stay read-only **load** paths. Live yard plugs with #80 slope/PBR. Smoke `grit=`. Near source for Hypha #60 mips
- **LOD-tied grit / material mips** (Hypha #60): `lod_mips.rs` BC4-class 8-bit height/rough on Transvoxel rings — near **256²** (#58 vendor) / mid **64²** / far **16²**; far drops grain hashes; `sample_channels` + `stamp_wear_scale` pick the ring from world XZ; in-repo `grit_*.png` until more grit cooks. Smoke `grit_mips=256/64/16 n=196608 f=768`. **#112** `promote_for_uv` keeps a finer existing pack when `FULCRUM_UV` scale > 1 (scale 2 → mid 64²; scale 4 → near 256²) — never a new mip, never remesh
- **Wider extract chunk radius** (Hypha #43): `TerrainHost` **5×5 → 7×7**; **3 Chebyshev rings / 112 m span / 12 544 m²** (was 2 rings / 80 m / 6 400 m²); extra **far** ring only. Far-cold still `lod >= 2` + Locus `ACTIVATE_M` **24** / `SLEEP_M` **32**. Lab-Rat `STUB_GRID = 7`. Near LOD raise **shipped #61**
- **Near LOD raise** (Hypha #61): then bake-once Transvoxel subdivs **32/16/4** (was 16/8/4). Grid stayed #43 **7×7**. Near step **2:1**. **#81** live underfoot **32/16/8/4**. Grit mips stay **256² / 64² / 16²** (#60). Amortized recook under budget **later landed #108**. Live octree / unconstrained Sync dump / tunnels / runtime carve still parked (**#114** is a shallow pad network, not those cutouts)
- **First big-map** (Hypha #81): **landed**. Live host **19×19 / 304 m / 92 416 m²** + **9×9** player-eye stream (`STREAM_RINGS` 4) + underfoot **32/16/8/4**. Walls **off**. Stamp pad still **7×7** / far-cold. Slope COL hooks (`pbr=tint` default) — vertex albedo only; NRM/GLOSS parked. Stream hitch amortize **landed #108** (cook=1/2 · prefetch=5 m · splash-pumped load-in on that same 9×9). Lab-Rat slope/PBR/dirt/scatter/deform plugs **landed #80** (DISP bake-down + `Deform` / `GroundScatter` filled). Beabim peer feet `stream_anchors` **landed #83** (coordinate only — Transvoxel rewrite still parked). #79 land sway + heightfield FX kept. Range heat / ballistics / binds / Augury chrome **not touched**. See `TERRAIN_NORTHSTAR.md`
- **Stream hitch amortize** (Hypha #108): **landed**. Hitch *fix* on the #81 9×9 — not a new map size. Load-in skeleton on frame 0; splash keeps presenting; **2** extracts / frame (`COOK_BUDGET_LOAD`) until idle; GPU upload only when the window is ready. Play **1** extract / frame (`COOK_BUDGET_PLAY`); dirty jobs underfoot-first via `TerrainHost::pump_stream`. **5 m** face prefetch upgrades the next already-resident neighbor to lod 0 *before* the step — does **not** open a second 9×9. Walk inside a cell with focus+LOD unchanged stays a no-op. Emits Augury Home `STREAM` / `BAKE` (`r=` `cold=` `pend=`) into #110 logger (#121 tracks can quiet STREAM/BAKE). Smoke `cook=1/2 prefetch=5` next to `subdivs=32/16/8/4`. Mesher stolen — no greenfield mesher. Live octree / residual soft LOD pop inside a cell still parked. See `PEEK_FINDINGS.md` Closed by #108 + `TERRAIN_NORTHSTAR.md`
- **Slope/PBR + dirt/scatter/deform plugs** (Lab-Rat #80): **landed**. `classify_slope` + 256² DISP bake-down + 64² COL/NRM thumbs. Fills `StampKind::Deform` / `GroundScatter` at #81 XZ (`8,-6` / `-10,14`). `PBR_HEIGHT_AMP` **0.028** · `SCATTER_AMP` **0.018** · `STAMP_PAD_HALF_M` **56**. Smoke `pbr=tint plugs=slope+deform+scatter`. Hypha #81 still owns vertex COL bind. NRM/GLOSS GPU parked. Stamp pad stays **7×7**
- **Blender UV dials** (Lab-Rat #101): **landed**. Stamp / PBR / grit share a Blender Mapping-node sheet — scale X/Y · offset X/Y · rotate (CCW about +Y). `engine/src/uv.rs` location (m) → rotate → scale (UV repeats). `scale > 1` tiles smaller. Identity default (`1,1 + 0,0 r=0`) keeps today's yard. `FULCRUM_UV=sx,sy,ox,oy,deg` (or `FULCRUM_UV_SCALE` / `_OFFSET` / `_ROTATE`). Texture tiles only — **never** geo / **never** Transvoxel shrink. Hypha #112 `lod_mips::promote_for_uv` + TerrainHost wear/COL honor `uv::xform` on Transvoxel skin. Smoke `uv=1.00,1.00+0.00,0.00 r=0`. Peek `FULCRUM_UV=2,2` → more grain, same geo. AXIS_LOCK stamp **+Y** stays separate
- **Transvoxel UV consume** (Hypha #112): **landed**. TerrainHost / material sample so Lab-Rat #101 stamp/PBR UV dials actually read on Transvoxel terrain — **texture only, never geo / never remesh / never chunk shrink**. `promote_for_uv` / `material_lod` stay on the existing 256/64/16 chain (scale 2 → mid 64² instead of far 16²; scale 4 → near 256²). `paint` / `stamp_wear_scale*` / `uv_skin` wear hashes follow `uv::xform`. `pbr_shelf` COL `sample_with` + wrap (scale 2 at XZ == identity at 2× XZ). Mesh / density / `CHUNK_METERS` 16 / `lod_for_world` untouched. Lab-Rat owns the sheet; Hypha owns skin consume. See `PEEK_FINDINGS.md` Closed by #112
- **Biped foot plant** (Hypha #88): **landed**. Samples Range #79 `World::surface_height` → `TerrainHost::height_at` + `support_surface_y`. FOLLOW **8.5** · DEADZONE **0.04** · RISE **2.2** · SINK **6.5** · SNAP_ERR **1.15** · LIFT_MAX **0.14** · BOOT_HALF_H center **0.11**. Soft Mycelium ride at cube-stub scale — not Mixamo clips, not 2-bone IK. Locus `step` no longer writes `pos.y = 0`. Dummy + grounded #83 peers share `biped::plant_simple_root`. Mesher / LOD / stamps untouched (#81 host stays). A-notes `[·] enemies walk into terrain` → **X**. STEAL_MAP biped **todo → partial** (plant + host hooks; Mixamo / player body / 2-bone IK / GPU skin parked)
- **Transvoxel extract host** (Hypha #16): crates.io `transvoxel` 2.0; live underfoot **32/16/8/4** (#81; was #61 32/16/4) + transition faces; `TerrainHost` implements `VoxelHost`; verts grade from Lab-Rat tint + wear; grimdark haze **#86** (extract **375 / 520**; hideout `haze_max` **0**); slope COL tint default #81
- **Distance activation / far-guts cold** (Hypha #23): shared Locus `ACTIVATE_M` **24** / `SLEEP_M` **32**; far stamp guts + growth/Locus upload stay cold (~19× cheaper far mean)

## Downed / revive
- HP→0 **downs** (prone crawl + thin bleed) — not menu death. Bleed-out ~`BLEED_SECS` **22.0**; extra hits while downed shave `BLEED_HIT_SECS` **6.0**. Clock expiry → `DEAD` + dark bag. Shipped Augury #36; death cam / teammate net / full loot loop still parked.
- Teammate **stabilize**, then heal with **items** (no magic heal) — hold **F** (`STABILIZE_HOLD_SECS` **1.45**); self while downed, or yard dummy when standing nearby (`REACH_M` **1.85**). Glasses `STAB STUB  NO NET` / `SELF-STAB STUB`. Solo placeholder — no fake net. Teammate net stabilize still parked.
- Equipment required — or take off the downed body
- **Self-revive** via revive stim on person — **I** while downed (`STIM_REVIVE_HP` **35**); day-one kit `stim: 1`; yard vial `YARD_STIM` **(3.55, 0, 3.20)** in front of dummy `YARD_DUMMY` **(3.55, 0, 4.55)** (`[F] PICK UP STIM`). Not a standing heal. Alive **I** is a no-op (no consume). **Y** is listen-server host (#34; Beabim #83 pose), alive only — does **not** stim. Downed Y is a no-op for both host and stim.
- Slash a downed **Locus Standard** (or similar) → **critical revive rally** — **Mouse4 / C** on a **downed or dying** Locus while you are downed or alive ≤ `RALLY_LOW_HP` **25** → `RALLY` (`RALLY_HP` **45** / `RALLY_ARMOR` **20**, stands if downed)
- **T** bandage (+40 HP, #31) is the item heal: while downed and **not** stabilized, glasses `NEED STAB` (no consume); after stabilize, T stands you up with the heal chunk. See Down / death stub section.

## Inventory / HUD
- MyceliumEngine **slot system** (stub OK)
- **Tab** = inventory / status (includes health)
- Health + armour **bottom-left**
- Ammo peek / mag swap (fulcrumRust #32): **Hold R** (`RELOAD_PEEK_HOLD_SEC` **0.20**) lights peek chrome only — does not start a reload; release after a hold is not a tap. **Tap R** (short press, reload on RELEASE) = basic swap (`RELOAD_BASIC_SEC` **1.10**) when `in_mag < capacity` AND reserves > 0 (**NOT** empty-only). **Double-tap R** (`RELOAD_DOUBLE_TAP_SEC` **0.30** from first tap) = emergency SWAP (`RELOAD_EMERGENCY_SEC` **0.46**). Last-pass feel-lab also named hold **Numpad 0** as a peek bind — fulcrumRust shipped Hold-R peek / tap-R reload / double-tap SWAP
- Hold **`** (Backquote; last-pass `~`) = inspect weapon (fulcrumRust #28 — reload-lift look-over overlay; glasses `INSPECT` only; inspect still wins over reload dip)
- **B** = fire mode
- Hold **J** = heat-tune dump (fulcrumRust #35); **I** is Augury stim (#37)
- **G** = cycle kits MP9-Z → SR-25 → M24 (fulcrumRust #22); **4 / 5 / 6** seat directly
- **T** = bandage use (fulcrumRust #31); **G** stays kit cycle. While downed unstabilized: `NEED STAB` (no consume); after stabilize, T stands + heals (#36)
- **I** = stim self-revive while downed (Augury #37). Not a standing heal. Alive **I** is a no-op (no consume)
- **Y** = listen-server host while alive (#34; Beabim #83 pose). Does **not** stim. Downed **Y** is a no-op (no host, no stim)
- **V** = cycle optic on seated kit allow-list
- **N** = toggle .45 suppressor / can mounts
- **M** = map
- **/** = Goegap plate on/off (fulcrumRust #40). Does **not** steal **M**
- **Z** = drop held kit as world bag (fulcrumRust #19); **F** = pickup / swap. Hideout door is **F** only (#51 — walk-into-door does not auto-deploy). **F** arms `GATE_SECS` **2.20** glasses countdown (`DOOR  DEPLOY  N%`) — not instant deploy (**#120**); walk away cancels; cool-off **0.55**. **F** tap near death bag = light corpse-reclaim stub; hold **F** = stabilize stub (self / yard dummy) or `[F] PICK UP STIM` when applicable — shipped stub (fulcrumRust #36). Hold-**F** on quiet hatch toggles OPEN/CLOSED; on Akira shaft rides surface ↔ cap lip ↔ exit pad (**#115**, `HOLD_SECS` **1.15**). OPEN quiet hatch presence arms extract-out countdown (`EXTRACT  N%`, **#120**). Tap-**F** pickup still wins. Stabilize / dummy / stim / corpse / loot still steal **F**. Downed cancels a ride
- **Space** = CE hop + one air hop + land overlay (same #59 hop — **not** a second land system). `JUMP_FORCE` **12** / `|GRAVITY|` **30** / one air hop **unchanged**. **#79** softener: punch **0.028** rad · duck **0.08 m** · shake **0.14** gate **13** (normal hop ~12 does not shake) · sway eye **0.014** / yaw **0.012** / roll **0.018** · decay **4.6**. Horizontal move must not eat `vel.y`. Landed #59; softener #79. Prior FPS-first **"no double-jump"** / single-hop-only (#51) is superseded (same way #51 superseded earlier "no jump")
- **[ / ]** = extract clock ±30 min (fulcrumRust #24); **K** = dawn/noon/dusk/night snap; **L** = live cycle
- **− / =** = step live zero 50 / 100 / 200 m wrap (fulcrumRust #78). Exposure keyboard unbound (no second pair; sky `nudge_exposure` may still exist). **, / .** = cloud cover (extract only; hideout unfogged). **#86:** clouds default **0.63** (was 0; **,** / **.** still nudge); **/** HDRI toggle stays. **#87:** dump **sunSize 0.62** rides the disc
- **O** (hold) = raid extract-check intent (`Session::extract_checking`; fulcrumRust #78). **Not** zero. Hideout is a no-op. Augury EXTRACT elbow card **landed #85** (no popup). Hatch toggle + shaft ride **landed #115**. Door / extract cancel chrome **landed #120** (`GATE_SECS` **2.20**; hold-O still intent only — countdown wins while armed). Timed surface kill still **~**. **P** unused after #76 (no arcade↔sim; no new bind)
- **X** = prone
- Canted hold + high/low ready from aim-offset. **U** = Chest → LowHip (`hip_low` **#99** shotgun low-ready; glasses **LOW HIP**) → Canted (glasses **CANT 45**). Viewmodel eases via `hold_spring` **7.0** (**landed #109**); glasses still snap CHEST / LOW HIP / CANT 45. RMB from Chest/LowHip = seated optic ads (LowHip still irons). **U** → CANT + RMB → `ads_cant` @ 60° CQC (**landed #100**). hold-**Mouse5** from any hold → `ads_cant` @ 60° CQC (does not steal U / RMB / melee). Glasses in `ads_cant` **CANT ADS**
- **H** = viewmodel **crossover shoulder / left-corner peek** on the existing FoW H bind (travel landed #59; tilt path **landed #84**; RH hip bias + slight straighten **landed #94**; one more body-width + ready-hip Y **landed #98**). Authored hip +X ~**0.24** (right; live **0.2403 / −0.2128 / −0.1833** — ready hold, not chin-weld); `shoulder_cross_x` **−0.281** / `shoulder_cross_y` **0.032**; springs across the chest to a partial left (~**−0.041** X / ~**−0.181** Y, cap `shoulder_x_min` **−0.055**). ADS keeps **0.32**. Extra left probe `shoulder_viewmodel` **0.12**. Left hold pitch/yaw/roll **0.04 / 0.10 / 0.08** (supersedes #84 chest-cross 0.08/0.32/0.39) on existing ViewmodelDials / ADS cant DNA (`apply_shoulder_crossover` → `PoseOffset` → `pose_basis`). Live hip_low is **#99** shotgun low-ready (MP9-Z **0.2403 / −0.3528 / −0.1513** / pitch **0.145**; glasses **LOW HIP**; LowHip ADS still irons). Live `ads_cant` is **#100** Greyzone CQC (MP9-Z **0.0423 / −0.148 / −0.136** / yaw **0.11**; glasses **CANT 45** / **CANT ADS**). Not a capsule/eye slide, not a mesh mirror, no `scale.x = −1` / mirrored kit boxes. Help remaps off H
- **End** = live aim-offset / attachment tuner (fulcrumRust #97). Thin in-raid panel + glasses `AIM TUNE`. Feel-lab Home remapped like X→Z. Insert = WEAPON ↔ ATTACH · PageDown = pose / attachment target · PageUp = step size · ↑↓ axis · ←→ / num± nudge · Delete = paste-ready JSON (feel-lab `example_smg` object + attachments). Writes the **same** `ViewmodelDials` + `AttachmentOffsets` — not a second pose system. #97 End tuner nudges **#98** ready-hip / H + **#99** hip_low + **#100** `ads_cant`. **AIM TUNE LIVE persist landed #103** (Hypha `project.json` `aim_live` default **true** + `aim_tune.example_smg` / `example_rifle` / `example_sniper`; pose `{x,y,z,rotX,rotY,rotZ}`; attach optic/can; load on Deploy; each LIVE nudge flushes; partial merge keeps #98/#99/#100; #97 End / Delete dump stay; RECORD stub — no bind)
- **Home** = CE debugger toggle (fulcrumRust #110). Tabs **LOGS** · **TELE** · **CHEAT** (←/→ cycle). Hitch WARN >33 ms / HITCH >100 ms. Glasses `DEBUG`. **End** stays AIM TUNE. Persist `project.json` `debugger_tab` (shares file with Range `aim_live` / `aim_tune` — one `persist_settings()` flush). LOGS COPY + tracker toggles **landed #121** — **Enter** COPY full boot→now ring (clipboard + cwd `fulcrum.logs`; `FULCRUM_LOGS` override) · ring **800** · `[sssss.mmm]` · Insert/Delete **STREAM** · **BAKE** · **GATE** · **PLAY**/GAMEPLAY · **INT**/INTERNAL · `log_*` in `project.json` default **on** · medium edge events · TELE max ms stays when tracks off

## Axes + controller lock (fulcrumRust #12 + #51 AXIS_LOCK)
- Three spaces — do **not** unify. Camera/viewmodel local **−Z**; CE FBX **+X** (`rotY − π/2`); sim barrel / FX **+Z**. Lab-Rat stamps stay **+Y** (not this lock). Detail: `AXIS_LOCK.md` + fulcrumRust `docs/AXIS.md`
- World is **Y-up**; pawn `yaw = 0` looks **+Z** (hideout door / extract yard) — same *vector* as arcade sim barrel when the bore matches look; **not** camera-local −Z
- Evan dizzy-play (#51): **subtract** mouse X (invert horizontal); **invert A/D** including slide A/D bias. WASD otherwise camera-relative on that yaw. Eye formula stays `+lean → −flat_right`. Do not unify the three forwards to "fix" FX
- SMG long axis is **look** / sim barrel +Z (not camera −Z, not CE +X); mag dots along the bore
- **Q / E** — **Q = peek right** (same side as inverted A) · **E = peek left** (landed #59). Eye formula stays `+lean → −flat_right`. Depth feel-lab **0.5 / 0.5** (`leanOffset` / `leanMax`). #25 wall clamp / spring / yard covers stay. Extra left probe on H crossover helps left-corner leans
- **Shift then Ctrl** — slide carry (sprint + crouch rising edge) **while grounded** (#78). Midair Shift+Ctrl cannot zero `vel.y` / hover
- **Hold Ctrl + mouse up/down** — analog eye height; does **not** pitch-look
- **Mouse wheel** — move speed (**not** height). Aim-offset uses wheel for crouch height; **Evan’s bind wins**
- Variable walk; **hold Shift** = sprint; grounded sprint→crouch slide via the Shift→Ctrl rising edge above (#78 — no midair float-slide)
- Hideout door **F** only (#51) — walk-into-door no longer auto-deploys. **F** arms `GATE_SECS` **2.20** countdown (**#120**) — not instant deploy. Walk away cancels; stay commits. Cool-off **0.55**
- **Space** — CE hop + one air hop + land overlay (landed #59; softener #79). `JUMP_FORCE` **12** / `|GRAVITY|` **30** / one air hop **unchanged**; punch **0.028** rad · duck **0.08 m** · shake **0.14** gate **13** · sway eye **0.014** / yaw **0.012** / roll **0.018** · decay **4.6**. Horizontal move must not eat `vel.y`. Same #59 hop — **not** a second land system. Prior FPS-first "no double-jump" / #51 single-jump-only is superseded
- Glasses may show `SLIDE` / `SPD` / `HT` / stamp material / `LOCUS  STANDARD|INKED  <brain>` / `INK HOTSPOT` / `INSPECT` / `RELOAD` / `SWAP` / `BANDAGE` / `EMPTY` / `Z{n}  SIM` / `HEAT TUNE` / `AIM TUNE` (End tuner #97) / `DEBUG` (Home debugger #110; LOGS COPY #121) / `LOW HIP` (U-cycle #99) / `CANT 45` / `CANT ADS` (canted CQC #100) / `HOST` / `JOIN` / `PEER` / `DOWNED` / `DEAD` / `STIM` / `NO STIM` / `RALLY` / `NEED STAB` / `STAB STUB  NO NET` / `HDRI` / `PROC` (ToD strip, fulcrumRust #40) / `DRY` / `YARD` / `OUT` (reverb volumes #56) / `EXTRACT` (hold-O #85 elbow card; **#115** `OPEN` / `CLOSED` / `SHAFT`; **#120** `EXTRACT  N%` while armed) / `HATCH` / `SHAFT` / `HOLD F  OPEN` (hatch #115) / `DOOR  F  DEPLOY` / `DOOR  DEPLOY  N%` (#120) labels only — never a second ammo/health HUD. Interact cards are embodied + L-elbow to the world pin (**#85**), not a centered HUD

## AXIS_LOCK (fulcrumRust #51)

Three spaces — do **not** unify. House shelf: `AXIS_LOCK.md`. Canonical: fulcrumRust `docs/AXIS.md` + `engine/src/axis.rs`.

| Space | Forward | Used for |
|-------|---------|----------|
| Camera / viewmodel local | **−Z** | Hold offsets, FP kit, `ejectionPort` |
| CE FBX authoring | **+X** | Stolen CE numbers; apply `rotY − π/2` after FP is −Z aligned |
| Sim barrel / mounts | **+Z** | Projectiles, TP grip, FX (flash, tracers, impact, stuck-slug, brass, ricochet) |

Pawn world look at yaw 0 is **+Z**. Same *vector* as arcade sim barrel when bore matches look — **not** camera-local −Z. Lab-Rat stamp **+Y** is a different content space — leave it.

FX (#47 corrected by #51): muzzle flash long axis = sim barrel +Z; brass toss = camera-right, brass orientation = sim barrel +Z; impact hole/chips/squat plug thin along world normal via `sim_barrel_basis` (RH); spent slug long axis = outgoing vel. #47 left-handed `forward × Y` mixed camera local into barrel geo — that was wrong. Do not invert Q/E lean signs to "fix" FX.

## Dizzy-play (fulcrumRust #51)

Supersedes stale #12 wording where it conflicts. Lean / slide / Ctrl-height / wheel stay #12.

1. **Invert horizontal mouse** — subtract look X (mouse-right looks left at yaw 0). Old #12 "mouse-right increases yaw" is stale
2. **Invert A/D strafe** — including slide A/D bias. Eye formula stays `+lean → −flat_right`. **#59 Q/E binds:** Q = peek right (−lean), E = peek left (+lean)
3. **Hideout door** — keep **F** prompt; walk-into-door no longer auto-deploys. Must press F. **Later landed #120** — F arms `GATE_SECS` **2.20** countdown (not instant deploy); walk away cancels
4. **Jump** — **landed #59**; softener **#79**. CE `JUMP_FORCE` **12** / `|GRAVITY|` **30**, one air hop **unchanged**. Same #59 hop overlay — **not** a second land system. Punch **0.028** rad · duck **0.08 m** · shake **0.14** gate **13** (normal hop ~12 does not shake) · sway eye **0.014** / yaw **0.012** / roll **0.018** · decay **4.6**. Horizontal move must not eat `vel.y`. Prior FPS-first **"no double-jump"** / single-jump-only (#51) is superseded (same way #51 superseded earlier "no jump")

## Heat / ADS
- Heat tell: **both** (diegetic barrel + glasses readout). **Live draw (landed #66):** colorless post UV warp — lattice is post input only; no world-pipeline orange card/lobe. Glasses `HEAT TUNE` (#35) stays the readout
- ADS/hip: **both**, weighted by enemy/context
- Heat-tune dump (fulcrumRust #35): hold **J** climbs the same `barrel_energy` cook with recoil / camera punch skipped; glasses `HEAT TUNE` only — see Heat-tune dump section. Range Tech owns cook / heat dials / hold-J. Live defaults are the **#71 blend** (v77 / dump stay DNA). Hypha owns the post path (#66)
- Heat cards look: v77 `updateBarrelHeatCardMorph` upward shimmer / lattice crawl stays the **spatial input** (landed #59). Barrel haze RGB `1.0 / lerp(0.14,0.70,h) / lerp(0.025,0.16,h²)` is feel-lab reference — **live fulcrumRust draw is colorless warp (#66)**. Live card defaults are the **#71 blend** on `heat-card-dial-sheet.md` (v77 / later dump stay DNA). Lattice vertex RGB forced to zero so this path cannot become an orange draw. Dump-dial blend cooking/~ → **landed/X** (#71). **#89** did **not** retune HeatDials; CE tip **0.2.8** preferred if a later Range cook retunes muzzle-adjacent haze — not a heat-card rewrite
- ADS viewmodel DoF (landed #68): disc blur on near depth when ADS + Options **DOF**. Radius **0.0048** UV-x at ads=1 · taps **12** · amount `ads_factor` (skip < 0.02; hip = 0) · near fade full ≤ **0.90 m**, gone by **2.20 m** · far DoF smoothstep **9 → 46 m** unchanged (#55) · breath mul **1.6 parked**. Same #55 pass / same Options **DOF** as #66 heat warp. See ADS viewmodel DoF section

## Visible shot feedback (fulcrumRust #12 + #19 + #59 + #67 + #89)
- LMB spends a round → muzzle flash + ballistic tracer + spark burst + hit mark (feel-lab language)
- Tracer speed / gravity / length from the SMG feel sheet. **#59:** tracers live until impact (feel-lab sanity **180 s**, linger **2 s**). Every strike plays FX `hit` (optional `hit.wav` if present; else procedural 780 Hz grit + 220→90). Graze still pings `ricochet`
- **#67 Patch A:** spawn + flash sit on the kit heat-box front (`kit_mesh::muzzle_tip_local`), not the feel-lab socket center (`muzzle_local` z=−0.405). Hip launch uses `hip_honest_dir` (ads=0 stays on **aim**; ads=1 keeps the SIM HoB/zero solve) so the 100 m HoB loft from a right-low hip muzzle is not a close-range up+right miss. Streak is feel-lab tip→impact: `tracer_len` is length again (not a 0.55 m receiver skip); back of the streak clamped to the tip. Distant speed scale kept once the slug is past the gun. Did **not** fight Hypha #66 / did **not** ship heat color. Lab-Rat terrain untouched
- FX draw-distance (hide-not-despawn, fulcrumRust #19 + #47): `muzzle_draw_m` **28** (clamp 8–80) · `spark_draw_m` **55** (clamp 8–200) · `casing_draw_m` **55** (clamp 8–200 via `live_casing`) · `decal_draw_m` **700** (clamp 50–2000) — walking back restores; they do not fill forever
- **#89 Range Tech projectile feel (landed):** existing `TracerField` / AXIS_LOCK sim barrel **+Z** / #79 heightfield snap. No new physics. HeatDials / #71 seated unchanged. Live dials:

| Dial | Now |
|------|-----|
| Muzzle flash | Long yellowish-white **rectangular slab** on can tip (`half.z` ≫ `half.x`) + pale-yellow rim flush on the tip |
| Muzzle debris | 4–6 orange sparks, life 0.07–0.17 s |
| Streak | visualLength floor **max(1.5, speed×0.035)** / cap **18** m |
| Core color | **2.85 / 2.25 / 0.95** |
| Slug head | **0.07** m bright nub (`TRACER_SLUG_LEN`) |
| Wake trail | 1–2 fading segments, tip-clamped |
| Hit flash | **0.15** s disc (grows 0.5→2.5, fade `1−√t`) |
| Punch sparks | **8–12**, 0.22–0.40 s, 35% white |
| Scuff sparks | **4–6**, 0.15–0.28 s, amber |
| Receiver glyphs | **fire pulse** red/orange on dump |

  Artistic auth frame stays `VECTOR_MAG_DUMP.md`. Local light / optic still reference-only unless already on the feel sheet. CE tip **0.2.8** preferred if a later cook retunes muzzle-adjacent haze — **not** a heat-card rewrite, not Beabim, not profile onboard. Do **not** steal pixel dither / floor warp — Hypha **#90** owns the post dial (`warp_strength` **0.01**); Augury aesthetic only. Do **not** reopen orange heat cards / invent bloom / godRays

## Props / audio / growth
- Destructible crates, boxes, cabinets with drawers from FoW
- Audio files from all repos + generated fills for gaps
- Living mycelium growth-enemy (gas/freeze/burn curl; sprint-grow) = Lab-Rat DNA hosted on extraction map

## Control DNA resolution
- **Locked** by fulcrumRust #12 + #51 + #59 + **#66** + **#67** + **#71** + **#76** + **#78** + **#79** + **#84** + **#85** + **#89** + **#94** + **#97** + **#98** + **#99** + **#100** + **#103** + **#109** + **#110** + **#113** + **#115** + **#116** + **#120** + **#121**: FoW scheme + aim-offset feel with Evan bind overrides above. #51 dizzy-play is the live look / strafe / door. **#59** landed Q/E flip + deepen, CE hop + air hop + land overlay, H viewmodel crossover, heat v77 look (spatial input), tracers-until-impact + FX `hit`. **#84** landed H tilt path (not a mesh mirror). **#94** landed Patch A RH hip bias first +0.08 + left hold **0.04 / 0.10 / 0.08** (supersedes #84 chest-cross 0.08/0.32/0.39). **#97** landed the live **End** aim-offset / attachment tuner on those same ViewmodelDials + kit_mesh sockets (Home debugger **later landed #110**; glasses `AIM TUNE`). **#103** landed AIM TUNE LIVE persist into Hypha `project.json` (`aim_live` default **true**; partial merge keeps #98/#99/#100; #97 End / Delete dump stay; RECORD stub — no bind). **#110** landed the Augury CE Home debugger (**Home** toggle · LOGS / TELE / CHEAT · hitch WARN/HITCH; glasses `DEBUG`; End stays AIM TUNE). **#98** landed one more body-width + ready-hip Y (MP9-Z hip **0.2403 / −0.2128 / −0.1833**; `shoulder_cross_x` **−0.281** / `shoulder_cross_y` **0.032**; #97 tuner still live). **#99** landed U-cycle `hip_low` shotgun low-ready (MP9-Z **0.2403 / −0.3528 / −0.1513** / pitch **0.145**; glasses **LOW HIP**; LowHip ADS still irons). **#100** landed canted 45° Greyzone CQC ADS on `ads_cant` (MP9-Z **0.0423 / −0.148 / −0.136** / yaw **0.11**; U+RMB / hold-Mouse5 @ 60° CQC; glasses **CANT 45** / **CANT ADS**). **#109** landed U-cycle hold springs (`hold_spring` **7.0**; same exp-approach as ADS / H / sprint; H `shoulder_spring` **8.0** / sprint **6.2** unchanged; glasses still snap; first-U seed-before-cycle; STEAL_MAP pose-ease → **in**; ADS `blend_speed` **6.4** stays its own dial — **#113** scales it by kit ergo). **#113** landed kit handling / ergo / MOA (`HandlingStats` / `FeelSheet::handling`; ADS blend **6.4** × ergo; handling → recoil `1/handling`; hip MOA after `hip_honest_dir`; ADS × **0.22**; `hold_spring` **7.0** stays sibling; STEAL_MAP handling → **in**). **#66** landed the live heat tell as colorless post UV warp (Hypha; lattice = post input only). **#67 Patch A** sits on top of **−/=** zero (#78; was **O** #33) + #76 SIM-only + #59 tracers: kit-tip spawn + hip aim-dir honesty + tip→impact streak clamp (did not fight #66). **#71** landed the Range Tech dump-dial blend on that #66 path (cooking/~ → landed/X). **#78** landed hold-**O** extract intent (Augury EXTRACT elbow card **landed #85**, no popup), **−/=** zero 50/100/200, grounded slide gate (no midair float-slide). **#115** landed hold-**F** hatch OPEN/CLOSED + shaft RIDE/EXIT (hold-O `EXTRACT  OPEN|CLOSED|SHAFT`; no modal popup; timed surface kill still `~`). **#120** landed door / extract cancel chrome (**F** arms `GATE_SECS` **2.20**; OPEN hatch arms extract-out; walk-away cancels; `COOL_SECS` **0.55**; timed surface kill still `~`). **#116** landed PreferredHand + new-profile onboard (Right default · NEW PROFILE gate · `project.json` `profile_onboarded` + `preferred_hand` permanent vs live · death clears live · extract→stash stub · `shoulder_t` 0 = authored RH / 1 = existing left dest — no mesh flip). **#79** softened the same #59 land overlay (punch **0.028** · duck **0.08** · shake **0.14** gate **13** + inertia sway; hop 12/30/1 **unchanged**) and snapped brass / tracer ends / marks to extract heightfield / wall support (`first_hit` walls-only; AXIS_LOCK +Z unchanged). **#89** landed projectile feel on the same `TracerField` (rect slab + debris + slug/wake + punch/scuff flash + fire-pulse glyphs; visualLength **1.5 / 18**; SIM / HoB / HeatDials unchanged). No remaining soft overlap on height / wheel. Lean / hop / H / hip-fire muzzle / U-cycle pose ease no longer cooking. Orange world heat cards are **not** the live path.
- **/** = Goegap plate on/off (fulcrumRust #40). Does **not** steal **M** (map).
- **Embodied feel pass landed #57** — Range Tech. Aim-offset guns / attachments / controller transposed at **medium** vs CE / FoW (outside materials and range geometry). Dials: look inertia queue **26** · ADS look **0.86** / blend **6.4** · sprint high-ready **6.2** · slide carry **10.3 / 0.98 / 1.02** · jump land punch then **0.052** rad overlay (**#79** live **0.028** + sway). `AXIS_LOCK` three spaces stay. See section below.

## Locus Standard + Inked + distance activation (fulcrumRust #18 + #26)
- Fightable **Locus Standard** + **Locus Inked** on the extract yard
  - Standard pad `YARD_STANDARD` **(5.15, 0, 7.85)** — right of creeper; ash/bone + rust-orange eyes
  - Inked pad `YARD_INKED` **(−5.10, 0, 8.20)** — left of 2D webbing; darker/hooded/thinner + cyan eyes + cheap ink-zone disc (Augury chrome); Lab-Rat #30 owns the loud stamp under the pad
- Brain: **Idle → Alert → Chase / Engage → Recover**; Dead = ragdoll flop stub
- Distance gate: `ACTIVATE_M` **24** / `SLEEP_M` **32** / `HEAR_M` **18** (far guts cold; shot crack can wake)
- Combat: `MAX_HP` **80**, kit `SMG_PELLET` **14**, Engage slash **10**
- Family TODO: Sonderer / Monk / Oculus / crawler
- Extract plant **landed #88** — `tick_on` samples the #79/#81 heightfield; `step` no longer writes `pos.y = 0`. Hideout / unit tests keep flat-floor `tick`. Brains still Augury
- Glasses labels only: `LOCUS  STANDARD|INKED  <brain>` — see `LOCUS_AI_LOCK.md` + `AESTHETIC_DIEGETIC_LOCK.md`

## Hold-` inspect pose (fulcrumRust #28)
- Hold **`** (Backquote; last-pass `~`) — reload-lift look-over overlay (feel-lab has no named inspect; Backquote is the debugger panel there)
- Raise + closer + yaw/roll so the receiver faces the lens; release returns to current hold (hip / low / cant / ADS / sprint_high)
- Overlay only — does not eat **U** / **RMB** / **V** / **N** / **B** / **Z**; fire blocked while up; B still toggles SEMI/AUTO
- Glasses `INSPECT` label only — no numeric ammo HUD

## Bandage use stub (fulcrumRust #31)
- **T** = bandage use. Last-pass named the *item*, not the key. **G** stays kit cycle.
- Does not steal **H** shoulder, **X** prone, **C** / **Mouse4** knife, **Q** / **E** lean, **Z** drop, **B** fire-mode, **V** optic, **N** can, **U** hold, **`** inspect, **F** pickup, **1** / **2** / **3** curl.
- Day-one kit already lists bandage:1 — this PR adds the use path.
- Consume 1 → **+40** health (`BANDAGE_HEAL` in `engine/src/kit.rs`); armor untouched; cap at `max_health`.
- Blocked at full HP (no consume). Empty press → glasses `EMPTY`. Successful use → glasses `BANDAGE`.
- FX: `Slot::Wrap` on the FX bus (cloth rustle stub, on-body like knife swipe). Not a heal chime.
- Works empty-handed; bandage stays on person when **Z** drops the gun (same as knife).
- Down / death now shipped #36: while downed and **not** stabilized, **T** shows `NEED STAB` and does not consume; after stabilize, T stands you up with the heal chunk. **T** is not a magic revive.

## World drop / pickup (fulcrumRust #19)
- **Z** drops held kit as loose world kit + canvas bag pad (last-pass bind; feel-lab used X)
- Snapshot keeps **in-mag + reserve mags + optic + can + fire mode**; cheap UUID (8-4-4-4-12) survives drop↔pickup
- **F** picks up or swaps (current kit lands at feet first); empty hands hide viewmodel / heat cards / fire
- Cap **8** loose drops; oldest despawns (`WORLD_DROP_CAP`)
- Knife / bandage stay on person; mag chrome stays diegetic on the kit — no HUD ammo counter


## Void-spore grimdark + concrete wear (fulcrumRust #20)
- Shared `density_stamp_2d` drives yard silhouettes **and** concrete crack / edge-wear leftovers
- Wear kinds: `ConcreteCrack` / `ConcreteEdge` / `VoidSporeWeb` / `VoidSporeBloom` / `VoidSporeCrack`; wear is solid on density for Hypha
- Grimdark `VoxelMaterial::luma`; sit-on-surface adds void-spore bloom + brutalist mass
- Curl **1 / 2 / 3** + glasses stamp labels unchanged (#30 shares the 2D field with the Inked pad)
- See `STAMP_FEEL_LOCK.md` + `AESTHETIC_DIEGETIC_LOCK.md` + fulcrumRust `docs/STAMPS.md`

## Inked AOE void-spore hotspot (fulcrumRust #30)
- Living loud ink / void-spore floor scar under Inked: `growth::INKED_HOTSPOT` = `locus::YARD_INKED` **(−5.10, 0, 8.20)**; `INKED_HOTSPOT_REACH` **1.55**
- Flat leftover, not a fourth yard plot; denser/louder than quiet 2D grit; reuses #20 `density_stamp_2d` / WearStamp DNA
- Pinned WearStamps: `VoidSporeWeb` + **`VoidSporeCrack`**
- Curl **1 / 2 / 3** shares the 2D stamp field (webbing OR Inked pad); remnants stay — not a softlock
- Glasses: `INK HOTSPOT` (and curl toast) on the scar off the Locus prompt; Augury still owns Inked AI + ink disc
- See `STAMP_FEEL_LOCK.md` + `LOCUS_AI_LOCK.md` + fulcrumRust `docs/GROWTH_POC.md` / `docs/STAMPS.md`

## Audio buses Voice / Music / FX (fulcrumRust #21)
- Feel-lab Settings **Audio** DNA — **not a DAW**; file-slot **wiring** shipped #54; day-one handmade atelier vendor **landed #62** (atelier WAVs in `assets/sfx/`; missing / bad file → procedural)
- Buses **Voice / Music / FX** into a **master**; gains clamp **0–2**, default **1.00 / 100%**; effective = `master * bus`
- Title + pause **Options** open the Augury shell (#45); Hypha Graphics/Gameplay/Controls panes live (#46); **Audio** is Range Tech #21 Voice/Music/FX plus **#82 DEVICE** (cursor 0, above the buses); **A/D** or **←/→** nudge bus **0.05** / cycle DEVICE; Esc Hypha pane / Audio → Options → title/pause; dials persist across Deploy
- **DEVICE** (landed #82): default **SYSTEM DEFAULT** via cpal `default_output_device()` (Windows / OS default). Cycle A/D or arrows; Enter / click also steps (same DNA as Graphics **WINDOW**). Persist `output_device` in `project.json` (empty / `default` / `system` = OS default). Missing pick: keep the pin; playback falls back to OS default. Same #21 mixer stereo render → thin cpal voice (oneshots + Music-bed loop) — **not** a second mix tree. UI tick plays on the newly selected device. Code: `engine/src/audio_out.rs` (Stream on window thread — not Sync). Bus dials unchanged
- Routes: **FX** = fire / dry / reload / cycle / pickup / putdown / Locus / swipe / wrap / ricochet / footstep / slide / jump / land; **Voice** = UI confirm; **Music** = hideout / extract playlist **landed #64** (five titled beds; hideout+extract advance shuffle; Options Music dial; missing → two-tone stub)
- Hard check: SMG fire SFX respect FX (FX `0` silent). File preferred when present; missing → procedural. See `EXTRACTION_AUDIO_LOCK.md` + `engine/src/audio.rs` / `engine/src/audio_out.rs`
- File-slot **wiring** shipped #54. Day-one handmade vendor **IN** via #62 (small set, not a full CE / aim-offset pack dump). Range Tech owns weapon/move SFX + DEVICE on this bus. Shot propagation still later. Controller feel-medium dials shipped #57 — that is not this row. See Authored SFX file slots (#54 + #62) + Options Audio DEVICE (#82).

## Day-one binaural / positional stereo on FX (fulcrumRust #27 + #56)
- Hypha + Augury CE FoW spatial DNA rides the **same** #21 Voice / Music / FX tree — **not a fourth bus**
- Listener follows the leaned camera basis (#25); HRTF-ish pan = equal-power ILD + Woodworth ITD + exponential distance
- World-posed FX: gunshots (muzzle), Locus slash (Standard + Inked), drops (putdown / pickup), ricochet ping at graze skip (#47); on-body FX: swipe / bandage `wrap` (#31); Voice centered; Music ambient bed
- **Reverb volumes shipped #56** (two-zone stub retired): hideout interior **DRY** · extract yard pad **YARD** · open extract **OUT** (wetter / longer tail). Authored AABB proxies; first XZ hit wins; miss → outdoor. **FX wet send only** — Voice / Music stay dry dual-mono. Glasses peek `DRY` / `YARD` / `OUT`. Listener follows camera. No extra bind. Walk off the yard pad to hear outdoor
- `Slot::Locus` / `Slot::Wrap` / `Slot::Ricochet` (#47) ride FX; file-slot **wiring** shipped #54; day-one handmade vendor **landed #62**; DEVICE cycle **landed #82**; shot propagation still later. Augury (**Chamber**) owns spatial + authored volumes + FX wet send; Range Tech owns mixer + file slots + DEVICE on the same bus
- Smoke: `zone=EXTRACT spatial=1.00 sfx=file/13`; FX `0` still silences fire
- See `EXTRACTION_AUDIO_LOCK.md` + fulcrumRust `engine/src/audio.rs`

## Transvoxel extract host (fulcrumRust #16)
- Flat-world bake-once isosurface via crates.io **`transvoxel` 2.0** (Lengyel); **not** a globe
- Distance LOD: live underfoot **32 / 16 / 8 / 4** + transition faces (**#81**; was #61 32/16/4). Every adjacent step **2:1**. Stamp-pad radius stays #43
- Live grid **19×19 / 304 m / 92 416 m²** + **9×9** stream (Hypha #81). Stamp pad still **7×7** / 112 m / 12 544 m² (#43; far-cold)
- Stream cook **#108**: `COOK_BUDGET_PLAY` **1** / `COOK_BUDGET_LOAD` **2** · prefetch **5 m** · splash-pumped load-in. Same 9×9 — not a second window
- `TerrainHost` consumes Lab-Rat `sample_channels` + `density_stamp_2d` / `WearStamp`; skin = `VoxelMaterial::tint` + #81 slope COL (`pbr=tint` default)
- Extract atmosphere: ashen/slate/brutalist vertex paint, void-spore stamp tints, cheap distance haze **#86** (fog **375 / 520**; hideout `haze_max` **0**). Walls **off**
- Parked: live octree / unconstrained Sync dump · residual soft LOD pop inside a cell · tunnels · runtime carve · Transvoxel rewrite / world sync · NRM/GLOSS GPU. **#114** is a shallow enterable pad network, not those parked cutouts. Amortized recook under budget **shipped #108**. Peer feet `stream_anchors` **landed #83** (coordinate only). Near LOD raise **shipped #61**. First big-map **landed #81**. Texture mips / compression **shipped #60** on the same **distance rings** (near 256² / mid 64² / far 16²; far softer). In-repo grit mips stay until Lab-Rat cooks more — see Texture LOD compress. See `TERRAIN_NORTHSTAR.md` + fulcrumRust `docs/TERRAIN.md`


## Distance activation / far-guts cold (fulcrumRust #23)
- Shared Augury Locus dials: `ACTIVATE_M` **24** / `SLEEP_M` **32** (CE labyrinth DNA; `activation.rs`)
- Bake rings match Transvoxel LOD; far rings skip stamp-structure / wear consume; far plates stay out of extract bake (collide boxes land); brutalist compounds stay on horizon
- Growth + Locus GPU uploads skip past `ACTIVATE_M`; near yard unchanged; reuses #16 `TerrainHost`
- Smoke: `near_chunk=862` · `far_chunk=45` · `guts_warm=17` · `guts_cold=140` · `terrain_tris=3168`
- See `TERRAIN_NORTHSTAR.md` / `LOCUS_AI_LOCK.md` + fulcrumRust `docs/TERRAIN.md`

## Wider extract chunk radius (fulcrumRust #43)
- Hypha; `TerrainHost` grid **5×5 → 7×7** (smallest honest odd widen): one extra **far** ring only
- Playable extract: **3 Chebyshev rings / 112 m span / 12 544 m²** (was 2 rings / 80 m / 6 400 m²)
- Near LOD then 16/8/4 (#43 did not raise it). **#61 shipped** the raise: center **32** · ring-1 **16** · outer **4**. Live walk lock **landed #81** (32/16/8/4 + 19×19 open). Stamp pad **still 7×7**
- Far-cold still maps `lod >= 2` → heightfield-only + shares Locus `ACTIVATE_M` **24** / `SLEEP_M` **32**
- Lab-Rat `ExtractStubHost` stays aligned (`STUB_GRID = 7`); near yard pad `yard_m2` ≈ **110** unchanged
- Smoke prints `rings=` / `extract_m2=` next to `near_chunk` / `far_chunk` / `yard_m2`:
  `near_chunk=858 far_chunk=39 guts_warm=75 guts_cold=216 rings=3 extract_m2=12544 yard_m2=110 locus_hp=24 terrain_tris=4034 lods=3`
  Far mean chunk ~**22×** cheaper than near; extra far ring added cold guts; yard pad + Locus stay
- Stay out of Atelier / HDRI / title mark on that pass. No new named scars
- See `TERRAIN_NORTHSTAR.md` / `STAMP_FEEL_LOCK.md` + fulcrumRust `docs/TERRAIN.md`

## Near LOD raise (fulcrumRust #61)

Hypha. Queued A/B after #43. Reuse the existing Transvoxel host. [PR #61](https://github.com/initialvisuals/fulcrumRust/pull/61) (`5f52913d`).

- Bake-once subdivs **32/16/4** (was 16/8/4). Near step **2:1** (32→16) so Lengyel faces still stitch. Outer stays coarse (4)
- Grid/radius stay #43: **7×7 / 3 Chebyshev rings / 112 m / 12 544 m²**
- Grit mips stay #60: **256² / 64² / 16²**. Far still heightfield-only / cold guts
- Smoke: `terrain_tris=11118 lods=3 subdivs=32/16/4 near_chunk=3290 far_chunk=39 guts_warm=75 guts_cold=216 rings=3 extract_m2=12544 grit_mips=256/64/16 n=196608 f=768`. Far mean ~**84×** cheaper than near
- Parked: live octree / unconstrained Sync dump · tunnels · runtime carve. Live walk lock **landed #81**. Stream hitch amortize **later landed #108**
- See `TERRAIN_NORTHSTAR.md` + fulcrumRust `docs/TERRAIN.md`

## First big-map open extract (Hypha — landed #81)

Evan lock. **Shipped** [fulcrumRust #81](https://github.com/initialvisuals/fulcrumRust/pull/81) (2026-09-09, `73dc8fe4`). **Hypha** owns host / stream / slope COL. Lab-Rat deform/scatter identity hooks were reserved here — **filled later #80**. Stamp pad still **7×7** / far-cold. #79 land sway + heightfield FX kept. Range heat / ballistics / binds / Augury chrome **not touched**.

| Dial | Lock |
|------|------|
| **Extract** | **19×19 / 304 m / 92 416 m²** (~8× old 7×7) |
| **Walls** | **Off** — open horizon, soft XZ clamp |
| **Stream** | **9×9** window (`STREAM_RINGS` 4) by player eyes. **#108** amortizes cook on this same window (cook=1/2 · prefetch=5 m · splash-pumped load-in) — not a second 9×9. Beabim #83 `stream_anchors` also returns remote feet (coordinate only) |
| **Underfoot** | **32 / 16 / 8 / 4** — every adjacent step **2:1** (was 32/16/4) |
| **Stamp pad** | Still **7×7** / far-cold (#23 guts cold) |
| **PBR** | Slope COL hooks (`pbr=tint` default). Vertex albedo only. NRM/GLOSS parked |
| **Lab-Rat** | `Deform` / `GroundScatter` + `LabRatDeform` / `LabRatScatter` identity reserved here. **Filled later #80** |
| **Seams** | One extract density on every LOD · 8-subdiv bridge (32→16→8→4 stays 2:1 Lengyel) · yard flatten outer **9.2 → 20 m**. Residual soft LOD pop inside a cell / far-4 horizon parked. Stream hitch amortize **later landed #108** |
| **Smoke** | `subdivs=32/16/8/4` `extract_m2=92416` `resident=` `stream_cold=` `pbr=` |

| Beat | Lock |
|------|------|
| **1. Higher res** | Already **#61** (32/16/4). **#81** keeps **32/16/8/4**. Further res stays Hypha |
| **2. Drop walls** | **Landed #81** |
| **3. ~8× extend** | **Landed #81** — 19×19 / 304 m / 92 416 m² |
| **4. Chunks** | **Landed #81** — 9×9 stream |
| **5. Scatter / PBR / deform** | **Landed #80** — DISP bake-down + `Deform` / `GroundScatter` filled at `8,-6` / `-10,14`. Smoke `plugs=slope+deform+scatter` |
| **6. Slope materials** | **Landed #81** — Hypha vertex COL tint default; NRM/GLOSS parked. Lab-Rat `classify_slope` + DISP bake-down **#80** |
| **7. Distance load** | **Landed #81** — local-player stream. **#108** amortizes that same 9×9 (cook=1/2 · prefetch=5 m). Beabim peer feet `stream_anchors` **landed #83** (coordinate only — no Transvoxel rewrite) |

See `TERRAIN_NORTHSTAR.md` + `PEEK_FINDINGS.md` Closed by #81 / Closed by #108. Hypha #88 consumes this same #79/#81 column for pawn plant — mesher untouched. Lab-Rat plugs **landed later #80**.

## Stream hitch amortize (Hypha — landed #108)

Evan lock. **Shipped** [fulcrumRust #108](https://github.com/initialvisuals/fulcrumRust/pull/108) (2026-09-09, `b3be2974`). **Hypha** owns amortized cook on the existing #81 9×9 stream — not a new map size. Hitch *fix* is this cook; hitch *visibility* stays Augury #110 / #121 (Hypha emits, does not rebuild Home). Residual soft LOD pop / live octree stay parked leftovers.

| Dial | Lock |
|------|------|
| **Load-in** | Skeleton (density + stamps + props) on frame 0; splash keeps presenting; **2** extracts / frame (`COOK_BUDGET_LOAD`) until idle; GPU upload only when the window is ready. No Sync whole **9×9** dump on one frame |
| **Play** | **1** extract / frame (`COOK_BUDGET_PLAY`). Dirty jobs sorted underfoot-first via `TerrainHost::pump_stream` |
| **Prefetch** | **5 m** face prefetch upgrades the next already-resident neighbor to lod 0 *before* the step. Does **not** open a second 9×9 |
| **No-op** | Walk inside a cell with focus+LOD unchanged stays a no-op; stale LOD stays until the budget reaches it |
| **Emit** | Augury Home `STREAM` / `BAKE` (`r=` `cold=` `pend=`) into #110 logger (#121 tracks can quiet STREAM/BAKE) |
| **Smoke** | `cook=1/2 prefetch=5` next to `subdivs=32/16/8/4` |
| **Parked** | Live octree · residual soft LOD pop inside a cell · unconstrained Sync dump |

| Seat | Owns |
|------|------|
| **Hypha** | Stream hitch *fix* (#108). Mesher stolen (`TerrainHost` / `extract_one` / activation) — no greenfield mesher |
| **Augury** | Hitch *visibility* (#110 / #121). Hypha emits; does not rebuild Home chrome |

Out of scope (do **not** claim shipped by #108): live octree · residual soft LOD pop · new map size · Range poses / AIM TUNE / loot · Lab-Rat UV (#101) · Beabim net · Augury Home tabs.

See `PEEK_FINDINGS.md` Closed by #108 + `TERRAIN_NORTHSTAR.md`.

## Slope/PBR + dirt/scatter/deform plugs (Lab-Rat — landed #80)

Evan lock. **Shipped** [fulcrumRust #80](https://github.com/initialvisuals/fulcrumRust/pull/80) (2026-09-09, `2cda73bc`). **Lab-Rat** owns slope tags + DISP bake-down + deform/scatter stamps. Hypha #81 still owns vertex COL bind. NRM/GLOSS GPU parked. Stamp pad stays **7×7**. Hypha 19×19 walk consumes `sample_channels` only.

| Dial | Lock |
|------|------|
| **Slope** | `classify_slope` tags dirt / sand / rock / concrete / organic on the stamp pad |
| **Stamps** | Fills Hypha reserved `StampKind::Deform` / `GroundScatter` + `HookKind::LabRatDeform` / `LabRatScatter` at #81 XZ |
| **PBR bake-down** | 256² greyscale DISP + 64² COL/NRM thumbs in `assets/stamps/` (CliffJagged / GroundClay / ConcreteWall / GroundMoss — not 4k 48-bit) |
| **COL hooks** | `pbr::ColHook` / `col_png` / `hypha_col_alias` — Hypha can consume. Lab-Rat does **not** own vertex COL bind |
| `PBR_HEIGHT_AMP` | **0.028** m |
| `SCATTER_AMP` | **0.018** m |
| `STAMP_PAD_HALF_M` | **56** m |
| `DEFORM_XZ` / r | `8, -6` / **5** m |
| `SCATTER_XZ` / r | `-10, 14` / **6** m |
| **Load** | vendored; `FULCRUM_GRIT` then `FULCRUM_ATELIER` (read-only) |
| **Smoke** | `pbr=tint plugs=slope+deform+scatter` + Hypha `gfx=` |

Do **not** claim NRM/GLOSS GPU bind. Do **not** claim Hypha vertex COL as Lab-Rat. Do **not** claim the whole roughness→stamp cook (SVG / density-mask / experiment-log still open). Range / Augury / Beabim / biped / Graphics dump stay out.

See `PEEK_FINDINGS.md` Closed by #80 + `STAMP_FEEL_LOCK.md` / `TERRAIN_NORTHSTAR.md`.

## Blender UV dials (Lab-Rat — landed #101)

Evan lock. **Shipped** [fulcrumRust #101](https://github.com/initialvisuals/fulcrumRust/pull/101) (2026-09-09, `c4e1490e` / `0ae97a0c`). **Lab-Rat** owns the UV sheet. Hypha #112 owns skin consume (`promote_for_uv` + wear/COL honor). Texture tiles only — never geo. Stamp **+Y** stays AXIS_LOCK.

| Dial | Lock |
|------|------|
| **Sheet** | scale X/Y · offset X/Y · rotate (CCW about +Y) — Blender Mapping-node |
| **Order** | Location (metres) → rotate → scale (UV repeats). `scale > 1` tiles smaller |
| **Identity** | `1,1 + 0,0 r=0` — keeps today's yard |
| **Override** | `FULCRUM_UV=sx,sy,ox,oy,deg` or `FULCRUM_UV_SCALE` / `_OFFSET` / `_ROTATE` |
| **Consume** | `GreyMap` / `HeightPack8` before wrap. Hypha #112 `promote_for_uv` + TerrainHost wear/COL honor via `uv::xform` |
| **Smoke** | `uv=1.00,1.00+0.00,0.00 r=0` |
| **Peek** | `FULCRUM_UV=2,2` → more grain, same geo/hills/chunks |

Do **not** claim NRM/GLOSS GPU · whole roughness→stamp · Transvoxel resize · atelier writes. AXIS_LOCK stamp +Y stays separate.

See `PEEK_FINDINGS.md` Closed by #101 / Closed by #112 + `STAMP_FEEL_LOCK.md`.

## Transvoxel UV consume (Hypha — landed #112)

Evan lock. **Shipped** [fulcrumRust #112](https://github.com/initialvisuals/fulcrumRust/pull/112) (2026-09-09, `35929282` / `b1ad2816`). **Hypha** owns skin consume. Lab-Rat owns the #101 sheet (`uv.rs` / GreyMap / HeightPack8). Texture only — never remesh / never chunk shrink.

| Dial | Lock |
|------|------|
| **`promote_for_uv` / `material_lod`** | Existing 256/64/16 chain only. `FULCRUM_UV` scale > 1 keeps a finer existing pack (scale 2 → mid 64² instead of far 16²; scale 4 → near 256²) |
| **TerrainHost** | `paint` / `stamp_wear_scale*` / `uv_skin` — vertex wear / cracks hashes follow `uv::xform`; no remesh |
| **`pbr_shelf` COL** | Explicit `sample_with` + wrap. Scale 2 at XZ == identity at 2× XZ |
| **Untouched** | Mesh / density / `CHUNK_METERS` 16 / `lod_for_world` |
| **Peek** | Identity looks like #101. `FULCRUM_UV=2,2` → more grain on same hills. Identity default keeps today's yard |

Do **not** claim NRM/GLOSS GPU · remesh · chunk resize · Lab-Rat bake rewrite. Range AIM TUNE / poses · Beabim net · Augury Home · #108 stream hitch stay out.

See `PEEK_FINDINGS.md` Closed by #112 + Closed by #101.

## Subtract crawl pad network (Lab-Rat — landed #114)

Evan lock. **Shipped** [fulcrumRust #114](https://github.com/initialvisuals/fulcrumRust/pull/114) (2026-09-09, `8fa74c03` / `28c09bd7`; merge tip `898454a0`). **Lab-Rat** owns the Subtract crawl. Deepens Patch A `[~]` (was a two-capsule dent) into a shallow enterable network under the pad. House world-depth stays **shallow** — not a tunnel sim. Full underground / live voxel collide still `[~]`.

| Dial | Lock |
|------|------|
| **Path** | mouth → mid → pocket → +Z spur + west/east branches + bent anastomosis kink |
| **Radii** | **0.42–0.50** (prone-sized; was 0.24–0.28). Pocket / mouth / spur = ellipsoid chambers |
| **Wander** | existing `density_stamp_2d` (same DNA as 2D stamp / wear) |
| `CRAWL_DROP` | **0.38** m mouth bowl. `DensityField::stamp_height_delta` → `growth::crawl_floor_delta` |
| `SLAB_Y0` | **−0.7** — bowl stays above the Transvoxel slab |
| Mouth XZ | **−1.60, 8.20** |
| Pocket XZ | **0.25, 9.15** |
| **Lip** | concrete Union around the mouth stretches **up** (compound, not deeper guts) |
| **Glasses** | `CRAWL  SUBTRACT` in mouth / pocket (wins over Locus `ALERT_M` **14** m, same as plot pins). Thin leftover plate at the mouth |
| **Smoke** | none new — existing `prims=` / `growth=` / `yard_m2=` still print harness cost |

Do **not** claim full guts / live voxel collide / tunnel sim. Hypha cook/prefetch/LOD · Range feel · Beabim · Augury Home · `uv.rs` stay out.

See `PEEK_FINDINGS.md` Closed by #114 + `STAMP_FEEL_LOCK.md`.

## Extract day/night clock + procedural sky (fulcrumRust #24)
- Feel-lab Settings **Lighting** DNA on extract only; hideout stays authored interior / unfogged (ToD does not leak inside). **#86** locks the dump defaults on this same path — not a second sky. **#87** completed the HDRI sun disc on that same sample
- Default clock **06:21** (`TOD_DEFAULT` 6.35); sun path rise ~6:05 / set ~19:42; noon elev **56°**
- Dials: **[ / ]** ±30 min · **K** dawn→noon→dusk→night · **L** live cycle (`LIVE_HOURS_PER_SEC` 0.25) · **, / .** clouds (step 0.10) · **/** Goegap plate on/off (#40; does not steal **M**). **#78:** **− / =** step zero (was exposure). Exposure keyboard unbound — no second pair; sky `nudge_exposure` may still exist (leftover mul **1.44**). **#86:** clouds default **0.63** (was 0; **,** / **.** still nudge); **/** HDRI toggle stays. **#87:** dump **sunSize 0.62** rides the procedural disc/halo
- **No XOR sky** — one ToD sample drives ambient / key / fill / fog + procedural dome; dual color-aware lights. #40 plate rides the same sample. **#87** completed the HDRI sun disc (not a second sky)
- **#86 dump lock** — fog **375 / 520** (`LightingFrame` haze start/range; was 16 / 48) · light*Mul **0.11 / 0.41 / 0.61 / 2.11 / 1.65 / 1.06** (already `sky::AMB_MUL` / `FILL_MUL` / `HEMI_MUL` / `KEY_MUL` / `RIM_MUL` / `MOON_MUL`) · exp **1.44** (already `sky::EXPOSURE_MUL`) · `sunPunch` **0.51** (existing sky disc/halo `sun_dir.w`) · `skyHdri` on · cam **0.05 / 2000** (`perspective_rh` / post linear-Z; was 0.06 / 280). Hideout `haze_max` **0**. **#87:** **sunSize 0.62** now drives disc/halo exponents (`mix(1800, 80)`) — no longer parked
- Grimdark: `EXTRACT_SKY_LUMA` **0.20** crushes noon to ashen (house aesthetic lock); Day HDRI shipped #40 (Goegap 4k; missing file stays procedural). **#87:** sky keeps Reinhard × **0.20**; solar texels use white-point **8 × 0.55** (was Reinhard w=1 × 0.20 everywhere — ~0.21 hole)
- Glasses on extract: `HH:MM  BAND  EXP x.xx  HDRI|PROC` labels only — never a second ammo HUD
- See `AESTHETIC_DIEGETIC_LOCK.md` + Hypha Graphics dump (#86) + HDRI sun disc (#87) + fulcrumRust `engine/src/sky.rs` / `engine/src/hdri.rs`

## Wall-clamped Q/E lean polish (fulcrumRust #25 + #59)
- Range Tech aim-offset / Engine #3 polish on existing #12 lean — no controller rebuild
- **#59 sign:** **Q = peek right** (−lean, same side as inverted A) · **E = peek left** (+lean). Eye formula stays `+lean → −flat_right`. #25 then said Q = left / +lean — superseded for binds, not the eye formula
- **#59 depth:** feel-lab **0.5 / 0.5** (`leanOffset` / `leanMax`), superseding #25 shallow `lean_offset` **0.18** / `lean_roll` **0.12**
- MoveDials that stay: `lean_spring` **8.0** · `lean_skin` **0.08** · `lean_viewmodel` **0.16**
- Spring enter/exit, then hard ceiling after the spring so walking into a wall cannot push past clearance; release still springs out (no snap)
- Camera probe uses those MoveDials
- Viewmodel pad (`lean_viewmodel` **0.16**) + extra left probe on H crossover (`shoulder_viewmodel` **0.12**) help left-corner leans
- Origin already inside a wall: `probe_clearance` reports 0 clearance
- Yard: two collide covers at extract yard mouth (`YARD_LEAN_COVERS`) on the Transvoxel pad; stay off plots / Locus / spawn
- Untouched: kits / drop / audio / ToD / Locus / Transvoxel; slide / Ctrl+mouse height / wheel speed stay
- See fulcrumRust `engine/src/feel.rs` + `engine/src/player.rs`

## Crossover shoulder / left-corner peek (fulcrumRust #59; tilt #84; RH hip #94 / #98; hip_low #99; ads_cant #100; hold springs #109)

Evan lock. **Travel landed** [fulcrumRust #59](https://github.com/initialvisuals/fulcrumRust/pull/59). **Tilt path landed** [fulcrumRust #84](https://github.com/initialvisuals/fulcrumRust/pull/84). **RH hip bias + left straighten landed** [fulcrumRust #94](https://github.com/initialvisuals/fulcrumRust/pull/94). **One more body-width + ready-hip Y landed** [fulcrumRust #98](https://github.com/initialvisuals/fulcrumRust/pull/98). **Low-hip shotgun stance landed** [fulcrumRust #99](https://github.com/initialvisuals/fulcrumRust/pull/99). **Canted 45° Greyzone CQC ADS landed** [fulcrumRust #100](https://github.com/initialvisuals/fulcrumRust/pull/100). **U-cycle hold springs landed** [fulcrumRust #109](https://github.com/initialvisuals/fulcrumRust/pull/109). Range Tech. Quiet influence — house words: **crossover shoulder / left-corner peek** (no franchise name-drop in shelf / READMEs / public copy).

| Dial | Lock |
|------|------|
| **Authored hip** | +X ~**0.24** (right; live MP9-Z **0.2403 / −0.2128 / −0.1833** — ready hold, not chin-weld; was #94 **0.1843 / −0.1688 / −0.1953**) |
| **H hold** | Springs the **viewmodel** across the chest to a partial left (~**−0.041** X / ~**−0.181** Y, cap `shoulder_x_min` **−0.055**) |
| **Travel deepen** | `shoulder_cross_x` **−0.281** / `shoulder_cross_y` **0.032** (**#98**; was #94 −0.225 / −0.012) — keeps dest ~−0.041 X / ~−0.181 Y |
| **Tilt** | **#94** slight straighten pitch/yaw/roll **0.04 / 0.10 / 0.08** (supersedes #84 chest-cross **0.08 / 0.32 / 0.39**) on existing ViewmodelDials / ADS cant DNA — **#98** left this gold vertical |
| **hip_low** | **#99** shotgun low-ready. MP9-Z **0.2403 / −0.3528 / −0.1513** / pitch **0.145** (was #98 **0.2403 / −0.2788 / −0.1633** / 0.0765). U-cycle glasses **LOW HIP**. RMB from LowHip = iron ADS (not `ads_cant`). Ready hip / hip_cant / H stay #98 |
| **ads_cant** | **#100** Greyzone CQC. MP9-Z **0.0423 / −0.148 / −0.136** / pitch/yaw/roll **0.024 / 0.11 / 0.785**. U+RMB / hold-Mouse5 @ 60° CQC. Glasses **CANT 45** / **CANT ADS**. hip_low stays #99 |
| **hold_spring** | **#109** U-cycle pose ease. **7.0** — house-medium between ADS `blend_speed` **6.4** and H `shoulder_spring` **8.0**. Sprint **6.2** / inspect **10.0** unchanged. Glasses still snap; viewmodel springs. Live ADS blend is **6.4** × kit ergo (**#113**) — not folded into this dial |
| **Not** | A capsule / eye slide. Mesh mirror / `scale.x = −1`. Infinite travel. Inward yaw to fake H aim. Chin-weld. Canted-holo mesh / IOR glass |
| **Left probe** | `shoulder_viewmodel` **0.12** — helps left-corner leans |
| **ADS** | Keeps **0.32** of the crossover (travel and tilt). ADS X stays feel-lab bore-center. LowHip RMB still irons. Canted CQC ADS is **#100** |
| **H** | Existing FoW shoulder habit — viewmodel crossover, not a new key |
| **PreferredHand** | **#116** Hypha. `shoulder_t` **0** = authored RH · **1** = existing left dest. Seats this Range H crossover. **No** `scale.x = −1` |
| **Seat** | Range Tech. Same #59 feel PR as lean flip / hop / heat look / distant hit. Tilt path **#84**. First +0.08 / left hold **#94**. Live hip / ready-Y **#98**. Live hip_low **#99**. Live ads_cant **#100**. Live hold springs **#109**. Hypha PreferredHand **#116** seats H |

See `PEEK_FINDINGS.md` Closed by #59 / Closed by #84 / Closed by #94 / Closed by #98 / Closed by #99 / Closed by #100 / Closed by #109 / Closed by #113 / Closed by #116 + H shoulder-swap tilt (#84) + Patch A RH hip bias (#94) + RH body-width + ready-hip Y (#98) + low-hip shotgun stance (#99) + canted CQC ADS (#100) + U-cycle hold springs (#109) + kit handling / ergo / MOA (#113) + PreferredHand onboard (#116).

## Mag reload DNA (fulcrumRust #32)
- Scheme: **Hold R** (~200 ms) = peek chrome only (does not start reload; release after a hold is not a tap). **Tap R** = short press, reload on RELEASE when `in_mag < capacity` AND reserves > 0 (NOT empty-only). **Double-tap R** (~300 ms from first tap) = emergency SWAP
- Dials (`engine/src/kit.rs` + `session.rs`): `RELOAD_PEEK_HOLD_SEC` **0.20** · `RELOAD_DOUBLE_TAP_SEC` **0.30** · `RELOAD_BASIC_SEC` **1.10** (basic mag-out pose stub) · `RELOAD_EMERGENCY_SEC` **0.46** (faster slap, same 1-reserve cost)
- Leftover rounds discarded on both paths (reserve is whole mags, not pocketed partials). Emergency’s higher-cost feel is dumping a half-stick
- Glasses labels only: `RELOAD` (basic) / `SWAP` (emergency) — never a numeric ammo HUD
- Intact / do not steal: knife, bandage, lean, inspect, ToD, kits
- Viewmodel: `reload_t` mag-out dip; inspect overlay still wins over reload dip

## Live HoB zero / launch dials (fulcrumRust #33; SIM-only #76; −/= #78)
- Per-kit rpm / recoil / HoB sheet was already authored (#22); #33 made zero distance + arcade↔sim **live**. **#76 supersedes the dual path** — launch is **SIM only** (HoB + gravity / zero); arcade aim-dir dead; leftover `hob_zero` ignored. **#78** moves the zero bind: **− / =** step, not **O**
- Constants: `ZERO_PRESETS_M` **[50.0, 100.0, 200.0]** m; default `zero_dist_m` **100**. Leftover `hob_zero` stays sheet-shaped (`HOB_ZERO_DEFAULT` **true**) — gameplay no longer reads it
- **− / =** — step live zero down / up 50 / 100 / 200 → wrap (HoB solve). Shared across MP9-Z / SR-25 / M24 so G-swap does not hide the solve (`FeelSheet::step_zero`). Replaces **O** cycling (#33)
- **O** — then cycled those presets. **#78:** hold extract-check intent (`Session::extract_checking`). **Not** zero. Hideout is a no-op. Augury EXTRACT elbow card **landed #85** (no popup). Hatch toggle + shaft ride **landed #115**. Door / extract cancel chrome **landed #120**; timed surface kill still **~**
- **P** — unused after #76 (no new bind). `FeelSheet::toggle_hob_zero` + session **P** apply gone; **P** no longer sets an input edge. Then #33 arcade (aim-dir) ↔ sim (HoB + ballistic zero)
- Honesty: changing zero preset changes muzzle **launch dir** only (not muzzle position). **#76:** one SIM model (`solve_ballistic_launch` — not a precomputed bake). Sim aims up to meet sight zero. Arcade aim-dir return in `muzzle_and_launch` is dead
- **#67 sits on top** — does not replace **−/=**. `hip_honest_dir` blends aim → solved by existing ADS↔hip weight: ads=0 stays on aim; ads=1 keeps this SIM solve. **−/=** still changes the zero; it bites when aimed. **O** / **P** do not. Not a new cone at #67 — **#113** later adds a hip MOA cone *after* `hip_honest_dir`. Per-kit recoil / `yaw_walk` stay authored (MP9-Z kick 1.0 · SR-25 1.15 · M24 1.75); live kick is × `1/handling`
- Toast: `ZERO  {n} M` (age **1.2s**, `Slot::Cycle`). `LAUNCH  ARCADE` / `LAUNCH  SIM` gone with **P**
- Glasses status strip (labels only, never a second ammo HUD): `Z{zero_dist_m:.0}  SIM` e.g. `Z100  SIM` — never `ARCADE`
- Intact / do not steal: **[ / ]** stay ToD clock; exposure keyboard unbound (no second pair); **9 / 0** left free; does not steal **T** / **C** / **R** / **Q** / **E** / **Z** / **B** / **V** / **N** / **U** / **`** / **F** / **X** / **H** / **1** / **2** / **3** / **G** / **Mouse4**; tip→impact tracers / muzzle / sparks stay; reload / knife / bandage / lean / inspect / ToD stay seated

## Patch A muzzle tip + honest hip fire (Range Tech — landed #67)

Evan lock. **Shipped** [fulcrumRust #67](https://github.com/initialvisuals/fulcrumRust/pull/67) (2026-09-08, `258b90fb`). **Range Tech** owns it. Focused ballistics / tracers / muzzle slice — no new systems, no heat-card color, no Lab-Rat terrain, no fight with Hypha #66 (colorless post warp **landed #66**). **−/=** HoB zero (#78; was **O** #33) + **#76 SIM-only** and #59 tracers-until-impact + FX `hit` stay; Patch A sits on top. **P** unused. **O** is hold extract intent (#78).

| Dial | Was | Now |
|------|-----|-----|
| **Spawn origin** | Feel-lab socket center (`muzzle_local` z=−0.405, flash-hider middle) | Front face of the forward-most **heat-tagged kit box** (birdcage / can) via `kit_mesh::muzzle_tip_local` (same DNA the viewmodel already draws). `muzzle_socket_local` stays the authored fallback |
| **Hip launch** | SIM 100 m HoB from a right-low hip muzzle → close-range **up + right** of the reticle | `hip_honest_dir`: ads=0 stays on **aim**; ads=1 keeps the SIM HoB/zero solve. Existing ADS↔hip weight. Not a new cone at #67 — **#113** later adds hip MOA after `hip_honest_dir`. **−/=** still changes the zero; it bites when aimed. **O** is extract intent (#78). **P** unused (#76) |
| **Streak** | `tracer_len` (0.55 m) used as a **receiver skip**; then a 10 m box drawn backward through the gun | Spawn **on the tip**. `tracer_len` is length again. Back of the streak clamped to the tip (feel-lab tip→impact). Distant speed scale kept once the slug is past the gun |

Do **not** claim `dBXpg` / full metal-tech kits / NRM-GLOSS GPU / whole roughness→stamp shipped. First big-map host **landed #81**. Lab-Rat plugs **landed later #80**. Heat tell is Hypha #66 colorless post warp — this PR did not fight #66 and did not ship heat color. Music playlist beds **are** shipped #64. Kit metal/grit PBR stub **is** shipped #64.

See `PEEK_FINDINGS.md` Closed by #67.

## SIM-only launch (Range Tech — landed #76)

Evan lock. **Shipped** [fulcrumRust #76](https://github.com/initialvisuals/fulcrumRust/pull/76) (2026-09-09, `28be5580`). **Range Tech** owns it. Flips #33’s dual-path launch to one live model. No projectile rewrite, no heat, no terrain. Ledger: `[X] sim-default / single model (#76 Range Tech)`.

| Dial | Was | Now |
|------|-----|-----|
| **Launch path** (`hob_zero` / `muzzle_and_launch`) | **P** arcade↔sim (`false` = aim-dir, `true` = HoB + gravity / zero) | **SIM only** — live HoB + gravity / zero solve; arcade aim-dir branch dead; leftover `hob_zero` ignored |
| **P** | arcade↔sim toggle | unused (no new bind). `toggle_hob_zero` + session **P** apply gone; **P** no longer sets an input edge |
| **O** | cycle 50 / 100 / 200 m zero | then still cycled those presets. **#78:** hold extract intent — not zero |
| kit recoil / `yaw_walk` | MP9-Z kick 1.0 · SR-25 1.15 · M24 1.75 + distinct walks | unchanged |

“Bake” here is **not** a precomputed trajectory. `solve_ballistic_launch` stays the existing feel-lab low-arc solve so shots share one deterministic model. **#67** hip honesty stays on top: ads=0 on aim; ads=1 keeps this SIM solve. Glasses `Z{n}  SIM` only — never `ARCADE`. Toast `ZERO  {n} M` stays; `LAUNCH  ARCADE` / `LAUNCH  SIM` gone. **#78:** zero distance is **−/=** (`FeelSheet::step_zero`), not **O**.

See `PEEK_FINDINGS.md` Closed by #76.

## Hold-O extract / −/= zero / grounded slide (Range Tech — landed #78)

Evan lock. **Shipped** [fulcrumRust #78](https://github.com/initialvisuals/fulcrumRust/pull/78) (2026-09-09, `e86bfa79`). **Range Tech** owns hold-O raid intent, **−/=** zero, grounded slide gate. **The Augury** EXTRACT elbow card **landed #85** (no popup — not landed by #78). Hatch toggle + shaft ride **later landed #115**. Door / extract cancel chrome **later landed #120**. Timed surface kill / extract loot loop still **~**. No heat / ballistics rewrite / Lab-Rat terrain. Ledger: hold-O check wired; glasses EXTRACT chrome is #85; ride/toggle is **X/#115**; door / extract cancel is **X/#120**; timed kill stays `~`.

| Dial | Was | Now |
|------|-----|-----|
| **O** | cycle live zero 50 → 100 → 200 m (#33; stayed after #76) | **hold** raid extract-check intent (`Session::extract_checking`). **Not** zero. Hideout is a no-op. Augury EXTRACT elbow card **landed #85** (no popup). **#115** reads `OPEN` / `CLOSED` / `SHAFT`. **#120** countdown wins while armed |
| **− / =** | exposure (default mul **1.44**, step 0.08) | zero down / up 50 / 100 / 200 m wrap (`FeelSheet::step_zero`). Replaces O cycling |
| Exposure keyboard | **− / =** | unbound (no second pair; do not invent one). Sky `nudge_exposure` may still exist for leftover edges |
| **P** | unused (#76) | unused (SIM-only stays) |
| **Shift+Ctrl** | slide start on sprint→crouch rising edge (ungrounded) | **grounded only**. Midair Shift+Ctrl cannot zero `vel.y` / hover. Grounded sprint→crouch slide still works |

**#76 SIM-only stays:** one HoB + gravity / zero model; leftover `hob_zero` ignored; **P** unused. **#67** hip honesty stays on top: ads=0 on aim; ads=1 keeps this SIM solve. Zero distance is now **−/=**, not **O**. **[ / ]** stay ToD · **, / .** stay clouds · **/** stays HDRI.

See `PEEK_FINDINGS.md` Closed by #78.

## Land sway softener + heightfield-grounded FX (Range Tech — landed #79)

Evan lock. **Shipped** [fulcrumRust #79](https://github.com/initialvisuals/fulcrumRust/pull/79) (2026-09-09, `fc6fb9a7` / `dfd04821`). **Range Tech** owns land overlay soften + heightfield ground FX. Same **#59** hop overlay — **not** a second land system. Hop DNA stays CE `JUMP_FORCE` **12** / `|GRAVITY|` **30** / one air hop. **AXIS_LOCK** sim barrel **+Z** for FX orientation unchanged; toss still camera-right.

| Dial | Was | Now |
|------|-----|-----|
| `jump_land_punch` | 0.052 rad | **0.028** rad |
| `jump_land_duck` | 0.14 m | **0.08** m |
| `jump_land_shake` | 0.20 m | **0.14** m |
| `jump_land_shake_gate` | 8 m/s | **13** m/s (normal hop ~12 does not shake) |
| `jump_land_sway_eye` | ad-hoc | **0.014** m at walk × impact |
| `jump_land_sway_yaw` | — | **0.012** rad at walk-strafe × impact (overlay; does not write yaw) |
| `jump_land_sway_roll` | — | **0.018** rad at walk-strafe × impact (camera-roll path) |
| `jump_land_sway_decay` | (punch 10.5) | **4.6** 1/s |
| hop 12 / 30 / 1 | 12 / 30 / 1 | **unchanged** |
| Brass / tracer / impact ground | flat `floor_y` / pawn feet / phantom y=0 slab | extract `World::surface_height(x,z)` / wall support AABB tops; hideout stays y=0; `first_hit` walls-only |

Sway is sampled at the land frame from current `vel.xz` vs look-forward / look-right, then exponential-decayed. Punch still subtracts from aim pitch; yaw/roll are overlays on `aim_forward` / `camera_basis_aim_roll`. Tracer ends + marks snap to that column; cheap slope normal so marks sit flush. Ground belongs to the heightfield.

**#78** hold-O / −/= zero / grounded slide stays. **#76** SIM-only stays. Augury EXTRACT elbow card **landed #85** (no popup). Hatch toggle + shaft ride **later landed #115**. Door / extract cancel chrome **later landed #120**. Do **not** claim a second land system or timed surface kill. First big-map host **landed #81** (this PR did not ship it). Lab-Rat slope/PBR/dirt/scatter/deform plugs **landed later #80**. NRM/GLOSS / further roughness→stamp still parked.

See `PEEK_FINDINGS.md` Closed by #79.

## Colorless muzzle heat (Hypha — landed #66)

Evan lock. **Shipped** [fulcrumRust #66](https://github.com/initialvisuals/fulcrumRust/pull/66) (2026-09-08, `05dd80ad`). **Hypha** owns the post path. Range Tech keeps `FeelState.barrel_energy` / heat-tune hold-**J** / heat dials on `heat-card-dial-sheet.md` — live defaults are the **#71 blend** (v77 / dump stay DNA). Same #55 fullscreen `engine/src/post.rs` stack as #68 ADS DoF — no second composer, no new Graphics sliders.

| Dial | Lock |
|------|------|
| **Live tell** | Colorless post UV warp. Warped scene color is the entire tell — no orange RGB / emissive heat-card output |
| **World draw** | Gone. Heat cards are **not** drawn through the opaque world pipeline (removed world-pass indexed draw of heat mesh) |
| **Lattice** | Existing tip-anchored heat lattice kept only as **spatial input** → one post field `post.heat: vec4` = center UV.xy, strength, radius |
| **`heat_warp_uv`** | Applied **before** scene color sample. Animated UV displacement only |
| **Lattice RGB** | Forced to zero so this path cannot become an orange draw |
| **HUD / glasses** | Still composite after post. Glasses / live sheet still drive the #71 dial fields |
| **Siblings** | #59 v77 shimmer intent (lattice crawl stays spatial input). #67 Patch A (explicitly did not fight #66). #68 ADS near on the same stack. #55 GPU post stack. **#71 dump-dial blend** (Range Tech; did not reopen orange cards). **#90** `pixel_warp_uv` sits after `heat_warp_uv` (heat body not edited) |

Do **not** invent new Graphics sliders or claim full Mycelium bloom/god-ray heat. Do **not** flip `dBXpg` / NRM-GLOSS GPU / whole roughness→stamp to shipped. First big-map host **landed #81**. Lab-Rat plugs **landed later #80**. Do **not** reopen orange cards.

See `PEEK_FINDINGS.md` Closed by #66.

## Heat dial blend toward aim-offset dump (Range Tech — landed #71)

Evan lock. **Shipped** [fulcrumRust #71](https://github.com/initialvisuals/fulcrumRust/pull/71) (2026-09-08, `117c8baa`). **Range Tech** owns heat dials on the Hypha **#66** colorless post path. Dump-dial blend cooking/~ → **landed/X**. #66 architecture stays — tip lattice → post UV warp; no orange card draw. v77 / later aim-offset dump stay DNA on `heat-card-dial-sheet.md`. Glasses / live sheet still drive the fields.

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

Post strength + radius stay on the **#66** path: at dial **0.01** keep lattice amp; at **0.11** use visual × 0.11; default **0.07** lands 60% toward quieter dump; **0** still kills warp. Radius: `card_size` + `lobe` pull scale/cap from **0.65 / 0.18** toward **0.50 / 0.12**; lattice bbox still anchors. WGSL `heat_warp_uv` unchanged (sample-only UV displace). Overlay disc lobe stays parked (`HEAT_LOBE_DISCS = 0`).

Intent: organic gas, less cartoony/wobbly. Tip-anchored lattice DNA stays. No second heat system. Do **not** reopen orange cards. **#89** did **not** retune HeatDials — CE tip **0.2.8** is the preferred DNA if a later Range cook retunes muzzle-adjacent haze (not a heat-card rewrite).

See `heat-card-dial-sheet.md` + `PEEK_FINDINGS.md` Closed by #71.

## Heat-tune dump (fulcrumRust #35)
- Bind: hold **J** = heat-tune dump. **I** is no longer free — I is Augury stim (#37).
- Feel: sustained AUTO on the seated kit (`FeelState::try_heat_tune` / `fire_shot(..., heat_tune: true)`); uses kit `auto_interval_sec` while tuning (ignores SEMI hold gate)
- Recoil impulse + camera punch skipped; leftover LMB punch stomped while J is down (`recoil_punch` / `recoil_rot` / `cam_recoil_p` / `cam_recoil_y` zeroed) so the gun stays still
- Same cook path: `FeelState.barrel_energy` still climbs so the tip lattice feeds `post.heat` (#66) for live dialing (no second heat cook). Lattice is post input only — no world-pipeline orange card
- Ammo dial cheat: mag **still spends** while holding; **release refills** the seated mag via `DayOneKit::refill_mag` (tops stick to `smg_mag_size`, does **not** spend a reserve)
- Glasses: `HEAT TUNE` label only (amber-ish overlay) — never a second ammo HUD; must not count mag rounds
- Intact / do not steal: ToD **[ ]**/K/L/,/. · −/= zero (#78) · hold-O extract intent (#78) · lean Q/E · inspect ` · reload R · knife Mouse4/C · bandage T · P unused (#76) · I stim · Y host · O/P/T/C/R/Q/E/Z/B/V/N/U/`/F/X/H/G/I/Y/1/2/3/Mouse4
- Tests that define the lock: `heat_tune_climbs_energy_without_camera_punch`, `heat_tune_does_not_fight_tod_lean_inspect_reload_knife_bandage_zero`, `heat_tune_glasses_do_not_count_mag`, `j_is_heat_tune_hold_without_stealing_binds`

## Listen-server pose presence + HOLD JOIN (fulcrumRust #34 + Beabim #83; invite leftover #91; loot trail #102; world/sim leftover #119; no-pause + KIND_RAID #122)

Seat: **Beabim** owns this MP slice (listen-server / two-instance sync / join panel / live-profile loot trail / world-sim leftover / no-pause / shared instance). Hypha #34 was the handshake-only stub. [PR #83](https://github.com/initialvisuals/fulcrumRust/pull/83) (`24eaca4b`). Invite leftover + peer names + gun pose **landed #91** (`c4d75c11`). Live-profile loot trail **landed #102** (`6fc0d5d6`). World/sim leftover **landed #119** (`6562070e726c0ae69719598bdc294a1f51d2e37e`). No-pause + KIND_RAID shared instance **landed #122** (`cbb26d8796faa9e476e8695fb4b118486d1759b3`) — #83 stays the pose / HOLD JOIN foundation. Augury #120 still owns glasses HOLD % / `GATE_SECS` **2.20**.

- Thin `std::net` UDP hub in `engine/src/net.rs` (#34). Title **HOST** / **JOIN**; in-game **Y** while alive arms listen-server; `--host` / `--join fulcrum://ip:port` (also bare `host:port` and `fw://`); env `FULCRUM_JOIN`
- Default port **7777** (`FULCRUM_PORT` override). LAN iface if OS has one, else loopback
- **#83 POSE** after HELLO/WELCOME (~20 Hz): feet `xyz`, yaw, pitch, grounded, crouch. Host assigns peer ids on WELCOME and relays poses. **#91** same packet + **muzzle xyz + gun yaw/pitch**
- Cheap **5-box** operator silhouette (slate) — not Mixamo / not Locus. **#91** 3-box gun stub on networked muzzle — **partial** 1P ≠ 3P (biped hip stub); full 3P kit honesty still open
- Grounded peer Y rides the **#81 19×19 heightfield** (Range #79 snap DNA). Packet Y ignored when grounded — no phantom `y=0` slab, no floating on a lie. Airborne hops keep networked Y. Dummy + grounded silhouettes plant via Hypha #88 `biped::plant_simple_root` (same column; packet / handshake / HOLD join stay #83). **#91** gun Y rides the same snap
- #81 `stream_anchors` returns remote feet so the **9×9** window can follow a peer (coordinate only — no Transvoxel rewrite)
- **HOLD JOIN** — Esc → **JOIN** → type `fulcrum://ip:port` / `fw://` / bare `ip:port` / `localhost` → Enter. No app restart. Title **JOIN** without `--join` opens the same sheet. `--join` / `FULCRUM_JOIN` still one-click. **#91** leftover INVITE + `fulcrum.invite` seeds the field
- Glasses labels only: `HOST  fulcrum://ip:port` (#91; was `HOST  ip:port`), then `JOIN` / `PEER` after HELLO/WELCOME — never a second ammo HUD
- **#102 KIND_LOOT** on the #91 UDP leftover. Host relays; both sides apply drop/take by `InstanceId`. Hairline `{NAME} DROP/TAKE KIT` via `plan_name_tag` (`FULCRUM_NAME` / HOST / P{id}). Starting kits stay local. Solo `net=off` unchanged — no trail chrome
- **#119 KIND_SHOT / KIND_LOCUS / KIND_BODY** on the #83/#91/#102 UDP leftover (`HYPH` magic). Host-relayed shot + death bag; host leftover Locus ~10 Hz (slot + pos + yaw + HP + brain + ragdoll flop). HELLO dumps current yard. Peer shot muzzle = `reconstructed_gun` + look dir — does **not** publish 1P `muzzle_world()`. Joined peer **plants soles only** — does **not** tick a second Locus brain
- **#122 no-pause** — Esc HOLD / Options / JOIN chrome **mutes the local pawn only**. Raid keeps ticking (pose / shots / Locus leftover). Focus loss / alt-tab releases grab — **does not HOLD or freeze** (no bullet bulk catch-up). Augury HOLD list / "SYSTEM PAUSED" chrome not restyled
- **#122 KIND_RAID** — host-authoritative leftover = Augury `GATE_SECS` **2.20** (house-docs #80 / fulcrumRust #120). Door **F** / OPEN quiet hatch presence arm the #120 glasses countdown; host then commits both peers to the same raid id + host seed (dest extract or hideout). Augury leave-volume / `GateEvent::Cancelled` → KIND_RAID CANCEL. Inventory / death soft-cancel too. No forced transition. Solo `net=off` uses the #120 countdown (no invented handshake / raid id / trail). Glasses HOLD % stay Augury. Dial sheet: fulcrumRust `docs/GATE_DIAL_SHEET.md` KIND_RAID row
- Honesty: two instances agree on **peer presence** (pose + silhouette) + **#102** kit loot trail + **#119** shot / Locus leftover / death bag + **#122** shared raid instance (same raid id + host seed) while menus mute the local pawn only. Range feel / HoB / heat / brass / 1P hip stay local — **no** full world replication / land feel / H tilt (#84) / audio device (#82) / Graphics dump (#86) / HDRI sun (#87) / Locus brain tick on the joiner / stamps / COL / deform / scatter / Transvoxel rewrite / Augury elbow / hatch UX (#85) / world seed / ToD / full PvEvP sim / Mixamo player body
- Solo **Deploy** unchanged (`net=off` on smoke)
- Does **not** steal **I** stim (#37), hold-**O** extract intent (#78 / #85), **−/=** zero (#78), **P** unused (#76), hold-**J** heat-tune (#35), or T/C/R/Q/E/Z/B/V/N/U/`/F/M/1/2/3/Mouse4
- Bind: **Y** alive host only (#34). Stim is **I** while downed (#37). Seats do not fight — downed Y is a no-op for host and stim.

## Down / death stub (fulcrumRust #36 + #37 bind)
- HP→0 **downs** (prone crawl + thin bleed) — not menu death. Glasses `DOWNED`. Bleed-out ~`BLEED_SECS` **22.0**; extra hits while downed shave `BLEED_HIT_SECS` **6.0**. Clock expiry → `DEAD` + dark bag.
- Constants (`engine/src/down.rs`): `BLEED_SECS` **22.0** · `BLEED_HIT_SECS` **6.0** · `STABILIZE_HOLD_SECS` **1.45** · `STIM_REVIVE_HP` **35** · `RALLY_HP` **45** / `RALLY_ARMOR` **20** / `RALLY_LOW_HP` **25** · `REACH_M` **1.85**
- Yard props: dummy `YARD_DUMMY` **(3.55, 0, 4.55)** · stim vial `YARD_STIM` **(3.55, 0, 3.20)** (in front of dummy)
- **I** while downed = stim self-revive (day-one kit `stim: 1`; yard vial `[F] PICK UP STIM`). Not a standing heal. Empty → glasses `NO STIM`. Success → `STIM` and stand at 35 HP. Alive **I** is a no-op (no consume).
- **Y** while alive = listen-server host (#34; Beabim #83 pose). Does **not** stim. Downed **Y** is a no-op for both host and stim.
- Hold **F** = stabilize stub (self while downed, or yard dummy when standing nearby). Glasses: `STAB STUB  NO NET` / `SELF-STAB STUB`. Prompt: `HOLD F  SELF-STAB STUB`. Solo placeholder — no fake net. **F** tap near bag = light corpse-reclaim stub (hold for stab; tap on bag — shipped stub).
- **T** bandage (+40 HP, Range Tech #31) unchanged as heal item. While downed and **not** stabilized: glasses `NEED STAB` (no consume). After stabilize: T stands you up with the heal chunk. Prompt: `STABILIZED  T HEAL / I STIM / SLASH RALLY`
- **Mouse4 / C** knife slash on a **downed or dying** Locus while you are downed or low (≤25 HP) → `RALLY` burst (+45 HP / +20 armor, stands if downed)
- Bleed-out ~22s → `DEAD` + dark bag; a new bleed-out **replaces** previous bag; **F** tap on bag = light corpse-reclaim stub (`DEAD  BAG STUB` / `CORPSE RECLAIM STUB`)
- Glasses/toasts labels only (never a second ammo/health HUD): `DOWNED` · `DEAD` · `STIM` · `NO STIM` · `STIM  PICKUP` · `STAB STUB  NO NET` · `RALLY` · `NEED STAB` · `DEAD  BAG STUB` · `CORPSE RECLAIM STUB` · prompts like `HOLD F  SELF-STAB STUB` / `[F] PICK UP STIM` / `STABILIZED  T HEAL / I STIM / SLASH RALLY`
- Intact / do not steal: **T** stays bandage · knife Mouse4/C · lean Q/E · inspect ` · reload R · kits G/4/5/6 · curl 1/2/3 · ToD **[ ]**/K/L/,/. · −/= zero (#78) · hold-O extract intent (#78) · P unused (#76) · hold-J heat-tune · listen-server title HOST/JOIN + `--host` / `--join` / HOLD JOIN (#83) stay. **I** is stim (does not steal Y host). **Y** is host alive-only (does not steal I stim).
- Tests that define the lock: `y_hosts_i_stims_without_stealing_binds`, `y_alive_hosts_i_downed_stims_without_crossing`.
- Parked / still TODO (do not claim done): death cam; teammate net stabilize; timed surface kill; full extract loot loop.

## Shape-agnostic stamp / paint substrate (fulcrumRust #38)

Lab-Rat technology lock — stop one-off stamp content (Standard scar, Monk AOE, extra yard silhouettes). Any authored shape converts into density + material, or paint details later. Does **not** own Transvoxel, Locus AI, or guns.

| Dial | Lock |
|------|------|
| **Density** | `> 0` solid, `< 0` air, `0` isosurface (same as Transvoxel consume; Hypha may flip for a port) |
| **Material** | dirt / sand / rock / concrete / organic (grimdark tint/luma) |
| **Grid** | `fill_grid` / `fill_chunk_samples`: `ix` fastest, then `iy`, then `iz` |
| **ChannelOp** | Union / Subtract / Paint / Replace (`engine/src/channels.rs`) |
| **Primitives** | sphere / ellipsoid / capsule / box / ribbon / brush / height-mask / mesh / volume |
| **Stack** | `ChannelStack` ordered compose; `StampField::layers` (authored extras) vs `StampField::content` (compiled consumers); `StampSlot::primitive` empty until fed |
| **Paint** | writes real today; brush UX stubbed. `density_delta > 0` puffs solid; `< 0` + Subtract carves; material-only with density 0 on existing solid |
| **Mesh→voxel** | `MeshStamp` → `voxelize_mesh` (step ~0.10–0.25 m, pad) → `SampledVolume` → `stamp_volume` (prefer compounds); `stamp_mesh` for small live SDF. World meters, Y-up, CCW outside |
| **2D mask** | `Mask2D` → `Primitive::height_mask`; helper `primitive_from_density_2d` — #39 harness applies it on the three existing plots via `layers` as a shallow anonymous scale test (still not a fourth named plot) |
| **Consumers stay** | sit-on-surface ellipsoids; wear ribbons (prefer capsule for new work); Inked hotspot; yard plots + curl **1 / 2 / 3** (CPU boxes; #39 also writes `primitive_from_density_2d` into `layers`); **#114** shallow Subtract crawl network (mouth → pocket; prone radii **0.42–0.50**); Hypha StampSlots empty until fed |
| **Ownership** | Lab-Rat writes / Hypha remeshes. Out of scope: Transvoxel tables/LOD, Locus AI, guns, 3D paint editor, live carve |

Consume path unchanged: `sample_channels` / `fill_chunk_samples`. See `STAMP_FEEL_LOCK.md` + fulcrumRust `docs/CHANNELS.md`.

## Extract-yard scale harness (fulcrumRust #39)

Stay **on the extract yard** for what #39 shipped as a scale/perf harness for the #38 stamp/paint substrate. Not a bigger world map on that pass. First big-map walk **landed #81**; stamp / harness pad stays **7×7**. No Standard / Monk one-off scars. HDRI stays Range Tech.

| Dial | Lock |
|------|------|
| **Pad** | `growth::yard_bounds` ≈ **110 m²** (baseline before harness ≈ **54 m²**); flatten disk tracks it so plots stay playable |
| **`apply_yard_harness`** | Anonymous SDF lattice + larger paint brushes + 2D-mask convert of the three existing plots through `StampField::layers` — not a fourth named plot |
| **Near / far** | Near yard stays warm (`bake_guts_warm`). Far guts stay cold (Hypha #23). Harness primitives are near-warm only; smoke fails if a layer center is far. `guts_cold` stayed **140** |
| **Smoke** | `growth=544 curled=580 stamps=100 structs=55 wears=117 content=173 layers=43 prims=216 yard_m2=110` · `guts_warm=75 guts_cold=140 near_chunk=858 far_chunk=45 terrain_tris=3182`. Baseline: `layers=0 prims≈content yard_m2≈54 guts_warm=32`. Far cheapness holds (`far_chunk < near_chunk`). Growth GPU boxes still under 620 |

See `STAMP_FEEL_LOCK.md` / `TERRAIN_NORTHSTAR.md` + fulcrumRust `docs/CHANNELS.md`.

## Texture LOD compress (2026-09-07)

Atelier roughness packs are **4k 48-bit PNG** — too large for extract. Do **not** ship raw 4k 48-bit into the yard. Quiet grit greyscales **landed #58** (vendored bake-downs + `sample_channels` quiet height + `grit::rough` wear). Hypha ring-mip texture LOD **shipped #60**. Lab-Rat slope/PBR/dirt/scatter/deform plugs **landed #80**. Blender UV dials **landed #101** — tile those packs without shrinking geo. Hypha Transvoxel UV consume **landed #112** (`promote_for_uv` + wear/COL honor). Atelier **150 roughness + textures/PBR ~26 sets landed**. Evan **clean** yell 2026-09-08 ~00:00 ET — atelier plugs **open**. Whole roughness→stamp cook is **not** done (SVG / density-mask / experiment-log still open).

| Seat | Lock |
|------|------|
| **Lab-Rat** | Bake greyscales **down before density** — 8-bit / half-res / BC4-style height packs. Quiet grit under loud scars. Wire on **fulcrumRust only**. **#58 landed** first in-repo 256² set — the near source for #60. Slope/PBR/dirt/scatter/deform plugs **landed #80**. Blender UV dials **landed #101** (`uv::xform` / `FULCRUM_UV`; identity default; texture tiles only). See Quiet grit greyscales + Blender UV dials |
| **Hypha** | LOD-tied mips / compression **shipped #60** on Transvoxel **distance rings**. Near **256²** (Lab-Rat vendor) · mid **64²** box mip · far **16²** box mip (cheaper / softer; far drops grain hashes). **#112** `promote_for_uv` + TerrainHost wear/COL honor Lab-Rat `#101` `uv::xform` — not a chunk resize / not a remesh. In-repo `assets/stamps/grit_*.png` until Lab-Rat cooks more. Smoke `grit_mips=256/64/16 n=196608 f=768` `uv=` |
| **Atelier** | Plugs **open** (was read-only). PBR batch **in** (150 roughness + textures/PBR ~26 sets). #58 `FULCRUM_GRIT=` / `FULCRUM_ATELIER=` stay read-only **load** paths |

See `STAMP_FEEL_LOCK.md` + `TERRAIN_NORTHSTAR.md` + `AESTHETIC_DIEGETIC_LOCK.md` + `ATELIER_PORTFOLIO_STEAL.md`.

## Quiet grit greyscales (fulcrumRust #58)

Lab-Rat. Feel lock: quiet authored grit + loud scars now has in-repo vendored height/rough modulators. [PR #58](https://github.com/initialvisuals/fulcrumRust/pull/58) (`f3be0d4f`).

| Dial | Lock |
|------|------|
| **Assets** | `assets/stamps/grit_grunge.png` · `grit_crack.png` · `grit_dust.png` — 256² luma (~83 KB) from atelier `grunge_4` / `paint cracks` / `dust and smudge_2`. Already bake-down sized — **not** raw 4k 48-bit |
| **Sample** | `engine/src/grit.rs` tiled world-XZ (stamp **+Y** height). Yard-weighted; far guts stay heightfield-only |
| **Channels** | `sample_channels` quiet height under compiled content so loud void-spore / webbing / Inked scars stay landmarks |
| **Wear** | Hypha vertex wear scale picks up `grit::rough` beside 2D-density cracks / `WearStamp`s |
| **Overrides** | Optional read-only: `FULCRUM_GRIT=` (same filenames) or `FULCRUM_ATELIER=` (local checkout, downsample on load). No submodule. No atelier writes |
| **Smoke** | `grit=vendor` (or `atelier` / `dir` if override) |
| **Still open** | SVG / density-mask ingest · experiment log · further roughness→stamp (PBR batch in; slope/PBR/dirt/scatter/deform plugs **landed #80**; Blender UV dials **landed #101**; Hypha UV consume **landed #112**; NRM/GLOSS GPU parked). Hypha ring-mips **landed #60**. Atelier plugs **open** (2026-09-08 clean) |
| **Out of scope** | Range Tech controller · Augury Locus · Hypha Transvoxel tables |

See `STAMP_FEEL_LOCK.md` + fulcrumRust `docs/STAMPS.md` / `docs/CHANNELS.md`.

## Goegap HDRI on extract ToD (fulcrumRust #40)

Range Tech day plate on the #24 extract clock. Hideout stays authored interior / unfogged.

- Asset: Poly Haven **Goegap** 4k Radiance RGBE (~22MB, CC0 / Greg Zaal). `engine/build.rs` fetches **one** file at build time into `engine/assets/hdris/` (not a submodule, not the atelier texture dump). Atelier raw is fallback. Missing file → procedural dome (honest).
- Feel: Radiance RGBE decode → equirect sky/env (`engine/src/hdri.rs`). Same ToD sample still drives ambient / key / fill / fog / dome — **no XOR sky**. Plate yaw tracks the clock sun. Night fades the day plate back to the procedural dome (stars stay). **#87** completed the HDRI sun disc on that same sample (not a second sky)
- Grimdark: `EXTRACT_SKY_LUMA` **0.20** keeps noon ashen. **#87:** sky keeps Reinhard × **0.20**; solar texels use white-point **8 × 0.55** + knee-compress (was Reinhard w=1 × 0.20 everywhere — ~0.21 hole)
- **/** toggles Goegap plate on/off — does **not** steal **M** (map). Existing ToD dials: **[ / ]** · **K** · **L** · **, / .**. **#78:** **− / =** is zero (was exposure). Exposure keyboard unbound (no second pair). **#86:** `skyHdri` already default on; **/** still toggles; clouds default **0.63**. **#87:** dump **sunSize 0.62** rides the disc/halo (`mix(1800, 80)`); HDRI live complements disc **0.55 / 0.18**
- Glasses: `06:21  DAWN  EXP 1.44  HDRI` (or `PROC` when plate off / missing) — labels only, never a second ammo HUD
- Smoke: `clock=06:21 hdri=goegap` (or procedural)
- Intact / do not steal: Lab-Rat stamps, Hypha Transvoxel, Augury Locus / down / death, listen-server, kits, knife, bandage, reload, heat-tune, **M** map
- See `AESTHETIC_DIEGETIC_LOCK.md` + fulcrumRust `engine/src/hdri.rs`

## FoW title mark (fulcrumRust #41)

Augury seats Evan’s Fulcrum of Will header as the title wordmark on the #11 shell. Grim lowfi title. Runtime does not clone atelier or CE. Do not invent a replacement mark (atelier `brand/` was README-only).

| Dial | Lock |
|------|------|
| **Asset** | `assets/brand/fulcrum-of-will-header.png` from `_CONCRETE_ECHO_` `@4_15_26` `public/images/Fulcrum Of will Header.png` (2048-wide, aspect kept) |
| **Seat** | `MARK_MAX_W` **1.70** · `MARK_MAX_H` **0.40** · `MARK_CENTER_Y` **0.58** (clip-space y-up) |
| **Fit** | `clip_aspect = image_aspect / window_aspect` — not stretched junk on non-square windows |
| **Clearance** | Bottom of mark must clear Deploy hit row (`mark_clears_deploy`) |
| **Chrome** | Bitmap `FULCRUM OF WILL` text removed — PNG is the wordmark. Gold tick / gold hairline gone (#45) — white hairline + tight white frames. Logo seat unchanged |
| **Hits** | **Deploy / Continue / Options / Esc** hit rows stay. #45 frames them white. No second ammo HUD |
| **Tests** | `vendored_header_is_a_wide_png`, `decode_matches_ihdr`, `title_seat_keeps_pixel_aspect` (16:9 / 4:3 / 21:9) |

See `AESTHETIC_DIEGETIC_LOCK.md` + fulcrumRust `engine/src/brand.rs`.

## Title + HOLD analysis-core polish (fulcrumRust #45)

Augury chrome on the existing FoW title (#11/#41) and HOLD pause shell. Logo seat #41 unchanged. Not a second ammo HUD. Stays off atelier.

| Dial | Lock |
|------|------|
| **Ink** | Thin white mono — not heat/ammo gold |
| **Frames** | Tight white frames on Deploy/Host/Join/Continue/Options/Quit |
| **Hairline** | Gold tick / gold hairline gone → white hairline; darker ground |
| **HOLD** | Tight white-framed panel, left rule, **SYSTEM PAUSED** (CE pause language); Resume / Options / Quit to menu |
| **Options list** | Lists **Graphics / Audio / Gameplay / Controls**. Augury owns the shell; Hypha guts shipped #46 |
| **Live tab** | **Audio** still opens Range Tech #21 Voice/Music/FX mixer (persists) + **#82 DEVICE** row. Graphics/Gameplay/Controls filled #46 (no longer disabled `HYPHA` placeholders) |
| **Confirm** | Confirm on a Hypha tab opens that pane (#46). Audio still #21 |
| **Esc** | Hypha pane / Audio → Options → title/pause |
| **Mark** | #41 seat stands: `MARK_MAX_W` **1.70** / `MARK_MAX_H` **0.40** / `MARK_CENTER_Y` **0.58** |

See `AESTHETIC_DIEGETIC_LOCK.md`. Hypha window / tab guts / persist shipped #46. GPU post stack live #55 (toggles change the image; not full HDR bloom / god-ray). **#66** colorless heat warp and **#68** ADS near sit on that same pass / same Options **DOF**. **#86** Graphics dump fills thin FOG / CAM rows on that Graphics pane — does **not** invent bloom / god-ray / brightness / gamma paths. **#87:** dump **sunSize 0.62** rides the sky disc (no longer parked). **#90:** Options Graphics **WARP** after CAM FAR (`warp_strength` default **0.01**).

## Menus / settings ownership (Evan dump 2026-09-07; Augury shell #45; Hypha guts #46; GPU post #55; colorless heat #66; ADS near #68; Graphics dump #86; HDRI sun #87; pixellation / WARP #90)

Augury shell polish shipped #45 (title + HOLD chrome + Options list shell + logo seat). Hypha Graphics/Gameplay/Controls guts + window mode + persist shipped #46. GPU post stack live **#55** — toggles change the image (AO/AA/CA/grain/DoF). **#66** colorless muzzle heat and **#68** ADS near DoF sit on that same pass. **#86** Graphics dump locks fog / cam / sky defaults + thin Options FOG / CAM rows. **#87** completed the HDRI sun disc (dump **sunSize 0.62** rides the disc). **#90** pixellation / floor-warp adds Options Graphics **WARP** after CAM FAR (`warp_strength` default **0.01**, step **0.01**, 0 = off; mix toward CE PIXEL SCALE **2**). Honest: not the full Mycelium HDR bloom / god-ray / contact-shadow chain — do **not** invent bloom / god-ray / brightness / gamma paths. Logo/title mark #41 still stands.

| Seat | Owns |
|------|------|
| **Augury** | Title + HOLD analysis-core chrome (#45). Options list shell. Logo/title mark #41. Layout/colors/buttons remain Augury. **CE Home debugger overlay landed #110** — thin white frames, fade-in white mono; glasses `DEBUG` (still labels only, never a second ammo HUD). Home LOGS COPY / tracker toggles **landed #121**. End stays Range AIM TUNE |
| **Hypha** | Graphics / Gameplay / Controls tab guts + window mode + persist — **shipped #46**. GPU post stack **#55** (AO/AA/CA(+strength)/grain/DoF) — toggles change the image; HUD/glasses still after post. **#66** colorless muzzle heat (`heat_warp_uv` before scene sample; lattice = post input only). **#68** ADS near + far on that same Options **DOF** flag. **Graphics dump landed #86** — thin Options **FOG / FOG NEAR / FOG FAR / CAM NEAR / CAM FAR** + sky / post defaults (fog **375 / 520** · cam **0.05 / 2000** · clouds **0.63** · sunPunch **0.51** · light*Mul **0.11 / 0.41 / 0.61 / 2.11 / 1.65 / 1.06** · exp **1.44** · skyHdri on; hideout `haze_max` **0**). **HDRI sun disc landed #87** — dump **sunSize 0.62** rides the disc. **Pixellation / WARP landed #90** — Options Graphics **WARP** after CAM FAR (`GFX_LEN` 12→13; fog/cam/#86 rows keep indices); `warp_strength` default **0.01** (lowest positive CE-like step; step **0.01**; range **0.0–1.0**; 0 = off); persist `project.json` `{:.2}` → `0.01`; mix toward CE PIXEL SCALE **2**. Augury aesthetic only — do **not** claim Augury shipped the dial. Do **not** invent bloom / godRays / brightness / gamma. Borderless default; windowed 1280×720; exclusive (borderless fallback). Persist `project.json` / `FULCRUM_SETTINGS` (fog / cam sit alongside Range `output_device`). **Not** packed into Range Tech ToD / Goegap / HDRI uniforms. Steal from CE/Mycelium. Does **not** dump atelier into Options Graphics. LOD-tied texture mips hook Transvoxel distance rings — see Texture LOD compress |
| **Range Tech** | Audio mixer stays #21 Voice/Music/FX (untouched by #46). Options **DEVICE** cycle **landed #82** on that pane (SYSTEM DEFAULT; persist `output_device`; thin cpal voice — not a second mixer). Owns `barrel_energy` / heat dials / heat-tune hold-J. Live heat defaults are the **#71 blend** (v77 / dump stay DNA). ADS viewmodel DoF dials **landed #68** on Hypha’s #55 pass (same Options **DOF**). Hypha owns the #66 colorless heat post path. **AIM TUNE LIVE persist landed #103** (steals Hypha `project.json` path; `aim_live` default **true**; `aim_tune.example_smg` / `example_rifle` / `example_sniper`; pose `{x,y,z,rotX,rotY,rotZ}`; attach optic/can; partial merge keeps #98/#99/#100; #97 End stays; RECORD stub — no bind). **CE Home debugger landed #110** shares that file (`debugger_tab`) — one `persist_settings()` flush; **#121** `log_*` rides the same file (default **on**); End stays AIM TUNE |
| **Input** | FoW OG input manager also in scope (steal into fulcrumRust) — still cooking |

Esc Hypha pane / Audio → Options → title/pause. Still no second ammo HUD. See `AESTHETIC_DIEGETIC_LOCK.md`. Existing #12–#68 sections stay (including #66 colorless heat). Graphics dump defaults live on **#86**. HDRI sun disc live on **#87**. Pixellation / WARP live on **#90**.

## Hypha Options guts (fulcrumRust #46)

Filled the disabled `HYPHA` stub tabs on Augury’s #45 Options list. Not a second settings overlay. Title / HOLD / Options chrome + FoW logo seat stay Augury.

| Dial | Lock |
|------|------|
| **Window** | Live via winit. **Borderless** = default launch. **Windowed** = decorated 1280×720. **Exclusive** = exclusive video mode when OS/GPU expose one, else borderless fallback. Also `--windowed` / `FULCRUM_WINDOW` (`borderless` / `windowed` / `exclusive`) |
| **Post** | Live GPU passes **#55**. AO, AA, CA (+ strength default **0.35**, step **0.05**, range **0–1**), film grain, DoF persist via #46 `project.json` / `FULCRUM_SETTINGS` and change the image. **#66** colorless muzzle heat (`heat_warp_uv` before scene sample; lattice = post input only — no world-pipeline orange card). **#90** pixellation / floor-warp (`pixel_warp_uv` after `heat_warp_uv`; heat body not edited). **#68** ADS near + far on that same Options **DOF** flag — no second composer. Must **not** pack into Range Tech ToD / Goegap / HDRI uniforms. HUD/glasses still after post. Honest: not full HDR bloom / god-ray / contact-shadow — **#86** does **not** invent those paths. **#87** sunSize rides the sky disc (not a post slider) |
| **FOG / CAM** | **#86** thin live rows on this pane: **FOG** (extract `haze_max`; hideout stays **0**) · **FOG NEAR / FOG FAR** **375 / 520** · **CAM NEAR / CAM FAR** **0.05 / 2000**. Persist `project.json` alongside Range `output_device`. Indices stay after **#90** |
| **WARP** | **#90** thin live row after CAM FAR (`GFX_LEN` 12→13). `warp_strength` default **0.01** (lowest positive CE-like step; `0.01 < 0.1`); step **0.01**; range **0.0–1.0**; **0 = off**. Shader `pixel_warp_uv` skips only at `s <= 0.0` so the default actually runs. Mix identity UV toward CE PIXEL SCALE **2** (half-res snap). Persist `project.json` `warp_strength` `{:.2}` → `0.01` |
| **Graphics hint** | `POST / FOG / CAM / WARP  ·  A/D NUDGE` |
| **Gameplay** | Glasses labels toggle + crosshair toggle (real — drop quads when off). Hint: `SHOOT FEEL STAYS · ENTER TOGGLE` |
| **Controls** | Look scale on feel-lab sens: `LOOK_MUL` default **1.0**, min **0.25**, max **2.0**, step **0.05**; Invert Y toggle. Binds stay README. Hint: `LOOK SITS ON FEEL-LAB SENS · BINDS IN README` |
| **Audio** | Untouched by #46 — Range Tech #21 Voice/Music/FX mixer. **#82** DEVICE row sits above the buses on that pane |
| **Persist** | `project.json` in cwd, or `FULCRUM_SETTINGS=/path/to.json`. #82 `output_device` · **#90** `warp_strength` · **#103** `aim_live` / `aim_tune.*` · **#116** `profile_onboarded` / `preferred_hand` live on the same file |
| **Esc** | Hypha pane / Audio → Options → title or HOLD (same stack as #45) |

See `AESTHETIC_DIEGETIC_LOCK.md`. No second ammo HUD. Does not dump atelier into Options Graphics. GPU stack that made toggles change the image is #55. Colorless heat warp on that stack is #66. Pixellation / floor-warp on that stack is **#90** (`pixel_warp_uv` after `heat_warp_uv`). ADS near layer on that stack is #68. Graphics dump fog / cam / sky defaults are **#86**. HDRI sun disc is **#87**.

## Hypha GPU post stack (fulcrumRust #55)

Follows #46 Settings Graphics toggles. Flags already persisted via `project.json` / `FULCRUM_SETTINGS` and previously no-op'd. #55 wires a real fullscreen wgpu stack so toggles change the image. #46 remains guts/persist. **#66** colorless muzzle heat and **#68** ADS near DoF sit on this same pass — #55 stays the GPU stack land.

- Scene color + sampleable depth, then one fullscreen pass (Mycelium `POST_PASS_ORDER` compressed):
  - **Heat** — `#66` `heat_warp_uv` **before** scene color sample (center UV / strength / radius from the tip lattice). Colorless UV displacement only — no orange RGB / emissive heat-card output. Heat body **not** edited by #90
  - **Pixel** — `#90` `pixel_warp_uv` **after** `heat_warp_uv` (`let uv = pixel_warp_uv(heat_warp_uv(input.uv))`). Mix identity UV toward CE PIXEL SCALE **2** (half-res snap). `PostStack` writes `pixel: [warp_strength, 0, 0, 0]`. Distinct from heat haze
  - **AO** — depth hemisphere SSAO (8 taps; Mycelium `ssao.rs` DNA, no G-buffer)
  - **AA** — luma-edge FXAA (Mycelium `fxaa.rs`; TAA later)
  - **CA** — radial R/B offset; strength slider already in Options
  - **Grain** — hashed film grain last so FXAA does not eat it
  - **DoF** — then far-field blur only (viewmodel stayed sharp). **#68** adds ADS near on the same pass / same Options **DOF** flag (ADS near + far). Far stays smoothstep **9 → 46 m**
- HUD / glasses still draw on the swapchain after post
- Not packed into Range Tech ToD / Goegap lighting params
- Smoke: `post=aa` (default AA on); keeps #54 `sfx=file/`. **#90** `gfx=` appends ` warp=0.01` only — existing `fog/375/520 cam=0.05/2000` substring stays
- Headless naga parse/validate of the post WGSL
- Honest: toggles change the image. Not the full Mycelium HDR bloom / god-ray / contact-shadow chain. **#86** does **not** invent bloom / godRays / brightness / gamma paths. **#87:** dump **sunSize 0.62** rides the sky disc (no longer parked)
- Stay out: Atelier, Range Tech bat/HDRI ToD/shoot feel/FX file slots, Augury title mark/HOLD/reverb

See `AESTHETIC_DIEGETIC_LOCK.md` + Colorless muzzle heat (#66) + Pixellation / floor-warp (#90) + ADS viewmodel DoF (#68).

## ADS viewmodel DoF (Range Tech — landed #68)

Evan lock. **Shipped** [fulcrumRust #68](https://github.com/initialvisuals/fulcrumRust/pull/68) (2026-09-08, `266ab088`). **Range Tech** owns the steal; seats on Hypha’s existing fullscreen `engine/src/post.rs` stack. One pass — no second composer, no new Options system. Source: feel-lab `ADS_DOF_*` / `adsDofAmount` / `initAdsDof`. #55 remains the GPU stack land; #68 is the ADS near layer on that stack.

| Dial | Lock |
|------|------|
| **ADS near DoF** | Disc blur on near depth when ADS + Options **DOF**. Depth stand-in for feel-lab `VIEWMODEL_LAYER` (single RT). Gun softens under ADS; hip + range stay sharp on that layer |
| **Radius** | **0.0048** UV-x at ads=1 (range 0–0.012). `ADS_DOF_RADIUS` |
| **Taps** | **12** (range 4–24; plus center + inner ring). `ADS_DOF_TAPS_DEFAULT` |
| **Amount** | `ads_factor` (skip < 0.02); hip = 0. No hold-breath / vault / reload terms |
| **Breath mul** | **1.6 parked** (constant + test only). Space is hop here; no hold-breath bind |
| **Near fade** | Full soften ≤ **0.90 m**, gone by **2.20 m**. Kit tip ~0.7 m; range stays sharp |
| **Far DoF** | smoothstep **9 → 46 m**, unchanged (#55) |
| **Toggle / persist** | Same Options **DOF** / `project.json` `depth_of_field`. Drives both near + far layers |

Do **not** invent a second EffectComposer / viewmodel RT, always-on ADS blur with DoF off, Space-as-hold-breath, or new Graphics sliders for radius/taps. This PR did **not** ship heat color — live tell is Hypha #66 colorless post warp on the same stack. Lab-Rat / profile / stash / MP / hands / inventory untouched.

See `PEEK_FINDINGS.md` Closed by #68.

## Leftover feel-lab FX (fulcrumRust #47)

Range Tech leftover feel-lab stack on the same #12/#19 `TracerField`. Tip already had tracers + muzzle + spark/mark + FX draw-distance — those stay. Not a rebuild. **#67** streak clamp sits on this field: spawn on the kit tip; `tracer_len` is length (not a receiver skip); back of the streak never drawn behind the tip.

- **FxDrawDials** (updated #19 row): `muzzle_draw_m` **28** (clamp 8–80) · `spark_draw_m` **55** (clamp 8–200) · `casing_draw_m` **55** NEW (clamp 8–200 via `live_casing`) — hide-not-despawn XZ lane for brass + spent slugs · `decal_draw_m` **700** (clamp 50–2000)
- **Brass eject** — live fire from seated kit `ejectionPort`: `MP9Z_EJECT` **(0.036, −0.014, 0.018)** · `SR25_EJECT` **(0.038, 0.008, 0.018)** · `M24_EJECT` **(0.03, 0.018, 0.055)**. Camera-right toss; `CASING_GRAVITY` **12**; bounce then sleep; `CASING_FADE` **6** s; `MAX_CASINGS` **48**. Hide-not-despawn via `casing_draw_m` **55**. Hold-**J** heat-tune dump (#35) skips brass so the lattice stays still. **#79:** sleep Y snaps to extract `World::surface_height(x,z)` / wall support AABB tops (hideout stays y=0) — not a flat `floor_y` or pawn-feet plane
- **Ricochet / spent slug** — feel-lab `trySpawnSpentSlugBounce` — **NOT** a bounce table. `SLUG_CHANCE` **1/16**; `SLUG_GRAZE_MAX` |n·vhat| ≤ **0.52** (dead-on still punches). Reflect incoming vel, keep 8–18% (`SLUG_KEEP_MIN`/`MAX` **0.08–0.18**); `SLUG_SPEED_MIN`/`MAX` **2.2–16**. Spent-slug visual `MAX_SLUGS` **24**; scuff mark instead of punch plug. Optional FX bus `Slot::Ricochet` ping at skip point. **#79:** spent also raise via support AABB tops + heightfield column
- **Richer impact geo** — punch vs scuff + `IMPACT_HOLE_VARIANTS` **10** + rim chips + stuck-slug plug (brass SMG / steel DMR+bolt). Rides existing spark/mark path — not a rebuild. **#79:** tracer ends + marks snap to that column; cheap slope normal so marks sit flush. `first_hit` is **walls-only** — no phantom y=0 slab. Ground belongs to the heightfield. **#89:** punch **8–12** sparks (0.22–0.40 s, 35% white) · scuff **4–6** amber (0.15–0.28 s) · 0.15 s hit-flash disc — was punch/scuff same 5–8 / 0.15–0.35 s, no hit flash
- Audio: FX bus routes now include ricochet (with fire/dry/reload/cycle/pickup/putdown/Locus/swipe/wrap)
- Intact / do not steal: tracers / muzzle flash / #19 draw-distance stay; kits / lean / ToD+HDRI / knife / bandage / reload / heat-tune / Locus / Transvoxel / listen-server unchanged. Mag chrome stays diegetic — no second ammo HUD
- #51 AXIS_LOCK: FX long/thin axis is **sim barrel +Z** (`axis::sim_barrel_basis`) — not camera/viewmodel −Z, not CE +X. Brass toss stays camera-right; brass long axis is barrel +Z. Do not rotate Lab-Rat stamps to fix sideways plugs. See `AXIS_LOCK.md`
- See fulcrumRust `engine/src/tracers.rs` + `engine/src/feel.rs` (`FxDrawDials`) + `engine/src/kit_mesh.rs` (`ejectionPort`) + `engine/src/axis.rs` + STEAL_MAP FX rows
- Vector mag dump flash / grit / glyphs **landed #89** on this field — see Projectile feel (#89)

## Vector mag dump (Range Tech — landed #89)

Evan aim-offset / Vector feel **artistic auth** stays on `VECTOR_MAG_DUMP.md`. **Live steal landed #89** (Range Tech) — rect slab + debris + slug/wake + punch/scuff flash + fire-pulse glyphs on existing `TracerField`. Local light / optic still **reference-only** unless already on the feel sheet. Heat stays on `heat-card-dial-sheet.md` (#66 / #71). Hypha pixellation / floor warp **landed #90** (post dial `warp_strength` **0.01**; Augury aesthetic only). Do **not** reopen orange heat cards or invent bloom / godRays. Live spawn stays `#67` kit-tip; flash long axis stays sim barrel **+Z**. Not a Vector kit swap.

## Projectile feel (Range Tech — landed #89)

Evan lock. **Shipped** [fulcrumRust #89](https://github.com/initialvisuals/fulcrumRust/pull/89) (2026-09-09, `a3e28ec0`). **Range Tech** owns it. Deepens projectile visuals / feel toward CE gold on existing `TracerField` — **no new physics**, no SIM rewrite. Ledger: `[·] projectiles from CE (Range Tech)` → **X**. Private DNA: FoW / feel-lab projectile feel + Evan’s Vector mag-dump frame. Public shelf stays feel-lab style.

| Dial | Was | Now | Stolen |
|------|-----|-----|--------|
| Muzzle flash shape | Round core `splat(0.018)` + 3 petals | Long yellowish-white **rectangular slab** on can tip (`half.z` ≫ `half.x`) + pale-yellow rim flush on the tip | Vector dump frame + feel-lab tip flash |
| Muzzle debris | none | 4–6 orange sparks, life 0.07–0.17 s | Dump-frame shards |
| Streak max | 10 m | **18** m | feel-lab `visualLength` cap |
| Streak floor (in flight) | authored 0.55 | **max(1.5, speed×0.035)** | feel-lab `max(1.5, speed*0.035)` |
| Core color | `0.95/0.72/0.28 × opacity` | **2.85 / 2.25 / 0.95** | feel-lab `setRGB(2.85, 2.25, 0.95)` |
| Slug head | none (uniform box) | **0.07** m bright nub | feel-lab `TRACER_SLUG_LEN` |
| Wake trail | none | 1–2 fading segments, tip-clamped | FoW / feel trail language |
| Hit flash | none | **0.15** s disc (grows 0.5→2.5, fade `1−√t`) | impact-plane bloom |
| Punch sparks | 5–8, 0.15–0.35 s | **8–12**, 0.22–0.40 s, 35% white | impact dump + feel-lab white mix |
| Scuff sparks | same as punch | **4–6**, 0.15–0.28 s, amber | punch vs scuff |
| Receiver glyphs | peek-only | **fire pulse** red/orange on dump | dump-frame receiver marks |
| SIM launch / HoB / gravity | #76 | **unchanged** | — |
| AXIS_LOCK +Z / #79 snap | in | **unchanged** | — |
| HeatDials / haze | #71 blend | **unchanged** — CE tip **0.2.8** preferred if a later cook retunes muzzle-adjacent haze | not a heat-card rewrite |

Intact siblings: #67 kit-tip spawn · #76 SIM-only · #71 heat blend · #79 heightfield snap · #12/#19/#47/#59 tracer field. Do **not** claim heat-card rewrite, terrain #80, Beabim sync, profile onboard, Augury hatch/labels, Aim-offset Home debugger, kit mesh rewrite, or grit as this PR. Pixellation / floor warp **later landed #90** (Hypha post dial; Augury aesthetic only).

See `VECTOR_MAG_DUMP.md` + `PEEK_FINDINGS.md` Closed by #89.

## Windows one-click release builder (fulcrumRust #42 + #48)

Hypha #42; Range Tech #48. Honest Windows release path — not quality/flag options (those stay open; Lab-Rat may mirror for pycelium later — no dials invented here). Linux/CI unchanged. Does not wrap with `cmd /k`. Does not touch atelier, HDRI/ToD, kits, terrain.

- **`build.bat`** — `cargo build --release -p app` (package from `app/Cargo.toml`). Prepends `%USERPROFILE%\.cargo\bin` so double-click PATH still finds rustup. Clear miss if cargo absent (`https://rustup.rs`)
- **Always pause** — success AND failure (single `:finish` path). `/nopause` is only for `build-and-run.bat` so the game can launch without a mid-script keypress
- **Tee cargo** — repo-root `build.log` (overwrite each run) via PowerShell `Tee-Object`; redirect+`type` fallback if PowerShell is missing
- After successful build, print `dir /T:W` mtime + size of `target\release\app.exe`. Start/end timestamps and `Result: OK` / `FAILED`
- If the Explorer window still vanishes: open `build.log` (README one-liner + on-screen hint)
- **`.gitattributes`** — `*.bat text eol=crlf` so cmd.exe does not skip `pause` on LF-only files
- **`build-and-run.bat`** — builds then launches that binary **in this console** (wait on process). No `start`+detach, no `timeout /t` (feel-lab `StartServer.bat` DNA). Extra args pass through (`--host`, `--smoke`, …). On build failure: pause and point at `build.log` (no silent `exit /b 1`)
- README: Windows double-click `build.bat`; if the window vanishes, open `build.log`

## Embodied feel pass (Range Tech — landed #57)

Evan lock. **Shipped** [fulcrumRust #57](https://github.com/initialvisuals/fulcrumRust/pull/57) (2026-09-07, `a678468a` / `e1c05b76`). **Range Tech** owns it. Tune dials only — do **not** rewrite the controller. `AXIS_LOCK` three spaces stay. No materials / range geo.

Aim-offset **looks/feels correct** for guns, attachments, controller — **transpose** that work into fulcrumRust. Concrete Echo / FoW OG for embodied cues — **medium** sweet spot.

| Cue | Feel-lab | Medium (shipped) |
|-----|----------|------------------|
| Look inertia | instant | queue **26** (CE camera_fx heavier; flick conserved) |
| ADS look / blend | 1.0 FOV-only / 8 | **0.86** / **6.4** × kit ergo (**#113** — MP9 **8.00** / SR-25 **6.40** / M24 **5.12**) |
| Sprint high-ready | 9 | **6.2** |
| Slide carry | 9.6 / 0.88 / 1.2 | **10.3 / 0.98 / 1.02** |
| Jump land punch | none | then **0.052** rad overlay (does not write `pitch`). **#79** live **0.028** + inertia sway |

U-cycle `hold_spring` **7.0** **later landed #109** — ADS `blend_speed` **6.4** stays its own dial; **#113** scales it by kit ergo (not a fixed stub). H `shoulder_spring` **8.0** / sprint **6.2** unchanged siblings.

Binds stay #12 + #51 invert look/strafe + F-only door. **#59** landed Q/E flip + CE hop + H crossover. Hypha #55 GPU post and Augury #56 DRY/YARD/OUT reverb volumes kept.

Day-one handmade SFX vendor **landed #62** — that is audio files, not these controller dials. See Authored SFX file slots (#54 + #62).

See `AESTHETIC_DIEGETIC_LOCK.md`. Steal from this shelf + steal map — not chat scroll.

## Evan peek feel (Range Tech — landed #59)

Evan lock. **Shipped** [fulcrumRust #59](https://github.com/initialvisuals/fulcrumRust/pull/59) (2026-09-07, `6359ae97`). **Range Tech** owns it. Quiet influence — house words: **crossover shoulder / left-corner peek**. `AXIS_LOCK` three spaces stay. #51 invert look/strafe + F-only door stay. #57 medium dials stay. #58 grit stays. #56 reverb volumes stay. Kits / ToD / SFX FILE_SLOTS / Options post stay.

| Cue | Lock |
|-----|------|
| **H crossover** | Authored hip +X ~**0.24** (right; live **0.2403 / −0.2128 / −0.1833** — ready hold). Viewmodel springs to partial left (~**−0.041** X / ~**−0.181** Y, cap `shoulder_x_min` **−0.055**). `shoulder_cross_x` **−0.281** / `shoulder_cross_y` **0.032**. Extra left probe `shoulder_viewmodel` **0.12**. ADS keeps **0.32**. Arms-limited — not a capsule/eye slide, not a mesh mirror, not infinite travel. Existing H bind, not a new key. **#94** slight straighten pitch/yaw/roll **0.04 / 0.10 / 0.08** (supersedes #84 chest-cross 0.08/0.32/0.39) — no `scale.x = −1`. Live hip_low **#99** (MP9-Z **0.2403 / −0.3528 / −0.1513** / pitch **0.145**; glasses **LOW HIP**). Live ads_cant **#100** (MP9-Z **0.0423 / −0.148 / −0.136** / yaw **0.11**; glasses **CANT 45** / **CANT ADS**) |
| **Lean flip + deepen** | **Q = peek right** (same side as inverted A) · **E = peek left**. Eye formula stays `+lean → −flat_right`. Depth **0.5 / 0.5** (`leanOffset` / `leanMax`), superseding #25 0.18/0.12. Wall clamp / spring / yard covers stay |
| **Hop** | CE `JUMP_FORCE` **12** / `|GRAVITY|` **30**, one air hop **unchanged**. Same #59 hop overlay — **not** a second land system. **#79** softener: punch **0.028** rad · duck **0.08 m** · shake **0.14** gate **13** (normal hop ~12 does not shake) · sway eye **0.014** / yaw **0.012** / roll **0.018** · decay **4.6**. Horizontal move must not eat `vel.y` |
| **Heat look (v77)** | `updateBarrelHeatCardMorph` upward shimmer / lattice crawl stays the **spatial input** (not static orange blobs). Barrel haze RGB `1.0 / lerp(0.14,0.70,h) / lerp(0.025,0.16,h²)` is feel-lab reference. **Live draw is Hypha colorless post UV warp (#66)** — lattice = post input only; no world-pipeline orange card. Live card defaults are the **#71 blend** on `heat-card-dial-sheet.md` (v77 / dump stay DNA) |
| **Ballistics / distant hit** | Tracers live until impact (sanity **180 s**, linger **2 s**). Every strike plays FX `hit` (optional `hit.wav`; else procedural 780 Hz grit + 220→90). Graze still pings `ricochet`. Day-one FILE_SLOTS vendor **landed #62** (optional `hit.wav`; missing → procedural). Shot propagation still later. **#67 Patch A sits on top:** kit-tip spawn + `hip_honest_dir` + tip→impact streak clamp. Did not fight Hypha #66 / did not ship heat color |

## Authored SFX vs spatial split (day-one FILE_SLOTS vendor landed #62)

Initial Visuals Group Chat 2026-09-07. File-slot **wiring** shipped #54. Day-one handmade atelier vendor **landed #62** — small set into FILE_SLOTS, not a full CE / aim-offset pack dump. #21 FX bus is **live**. Authored audio (rustles / rattles / slides) comes over that bus. Mixer / Options Audio FX / Augury spatial+#56 reverb stay untouched. Controller feel-medium dials shipped #57 — that is not this row.

| Seat | Owns |
|------|------|
| **Range Tech** | Weapon / move SFX **file slots** off CE / FoW packs into the live #21 Voice / Music / FX buses. Not a fourth bus. Wiring shipped #54. Day-one handmade vendor landed #62. Remix first ±6% fire/foot/reload jitter **landed #64**; full remix minting still **open**. Music playlist beds **landed #64**. Options **DEVICE** cycle **landed #82** (SYSTEM DEFAULT; persist `output_device`; thin cpal voice). |
| **Augury (Chamber)** | Keeps spatial / reverb DNA (#27 HRTF/ITD + #56 DRY/YARD/OUT volumes, FX wet send only). Does not take the file slots. |
| **Lab-Rat** | Stamps stay **quiet on audio** |

#21 Audio tab + #27 spatial path + #56 volumes stay. Shot propagation still later. Future extra FX ids / authored+CE synth mix remain open. See `AESTHETIC_DIEGETIC_LOCK.md` + `EXTRACTION_AUDIO_LOCK.md`.

## Authored SFX file slots (fulcrumRust #54 + #62)

Range Tech feel-lab `sfx.slots[id]` on the **same** #21 FX bus — **not** a second mixer. Status **IN** for the day-one handmade vendor: #54 wiring + #62 atelier WAVs in `assets/sfx/`. Small handmade set — not a full CE / aim-offset pack dump. Shot propagation still later. `.ogg` names reserved; decode WAV-only this beat. Controller feel-medium dials shipped #57 — that is not this row.

| Dial | Lock |
|------|------|
| **Load** | `mixer.play(Slot::*)` loads `assets/sfx/<id>.wav` (or `FULCRUM_SFX` override dir) |
| **Fallback** | Missing / bad file → existing procedural tone |
| **FX gain** | Options Audio FX dial scales the buffer; FX `0` still silent |
| **File-backed slots** | fire · dry · reload_release / insert / seat · pickup · putdown · swipe · wrap · footstep · slide · jump · land |
| **Optional** | `hit.wav` (atelier darkBead_impact1; #59 already plays FX `hit`) |
| **Reserved (synth until file)** | cycle · locus · ricochet |
| **Vendor** | ~22.05 kHz 16-bit mono WAVs in `assets/sfx/` — atelier `sfx_/` CE/feel (main `f094157`, read-only). Not a full pack dump |
| **Move cues live** | walk rustle (`footstep`) · sprint-crouch slide · Space hop + land |
| **Weapon cues** | already on FX; prefer the file |
| **Ownership** | Range Tech file slots / Augury Chamber spatial + #56 volumes (FX wet send) / Lab-Rat quiet stamps |
| **Left alone** | AXIS_LOCK · Locus brains · terrain/stamps · Options Graphics · mixer / FX dial / Augury spatial+#56 reverb |

See `EXTRACTION_AUDIO_LOCK.md` + fulcrumRust `assets/sfx/README.md`.

## SFX remix DNA (Evan 2026-09-08 ~00:00 ET)

Range Tech. Creative reuse **OK** — pitch / speed / effects to mint new one-shots from existing packs. Indie underground vibe. Do **not** overuse the same stem. #54 wiring + #62 handmade vendor stay the live FILE_SLOTS fill. Remix is how more one-shots get minted without a full pack dump. Same #21 FX bus — not a second mixer. Voice / Music stay dry dual-mono (#56). First application **landed #64** — fire / foot / reload ±6% pitch/speed jitter on the live #62 vendor. Mixer / Options FX / Augury spatial stay honest (FX `0` still silent). Remix DNA policy stays; full remix pack minting still **open**. See `EXTRACTION_AUDIO_LOCK.md`.

## Music beds (landed #64)

Shuffle of five atelier `music/` titles on hideout / extract beds: **CONCRETE_ECHO** · **Terraform** · **The Memory of The Augury** · **guttertrash** · **A Shattered Remnant From A Collapsed Distant Star**. Small 8 s / 22.05 kHz / 16-bit mono loops in fulcrumRust `assets/music/` (not the 5–11 MB MP3s). Each hideout / extract start advances the shuffle. Options Audio Music dial still scales the bed. Missing file → old two-tone stub. Same #21 Voice / Music / FX tree — not a fourth bus. Music stays dry dual-mono (#56). Voice / FX / Augury spatial+reverb untouched. Overrides: `FULCRUM_MUSIC` / `FULCRUM_ATELIER` read-only. Playback rides the #82 DEVICE pick (thin cpal voice). See `EXTRACTION_AUDIO_LOCK.md`.

## Options Audio DEVICE (Range Tech — landed #82)

Evan lock. **Shipped** [fulcrumRust #82](https://github.com/initialvisuals/fulcrumRust/pull/82) (2026-09-09, `12676383`). **Range Tech** owns DEVICE + mixer. Augury still owns spatial/reverb. Hypha still owns Options Graphics post. No heat / terrain / Beabim / Augury labels / CE projectiles. Ledger: `[X] audio device dropdown in Options (Range Tech)`.

| Dial | Lock |
|------|------|
| **Row** | Options **Audio** `DEVICE` (cursor 0, above Voice / Music / FX). Bus dials unchanged (0–2 / 100%) |
| **Default** | **SYSTEM DEFAULT** — cpal `default_output_device()` (Windows / OS default) |
| **Cycle** | A/D or arrows; Enter / click also steps (same DNA as Graphics **WINDOW**) |
| **Persist** | `output_device` in `project.json` (empty / `default` / `system` = OS default) |
| **Missing pick** | Keep the pin; playback falls back to OS default |
| **Route** | Same #21 mixer stereo render → thin cpal voice (oneshots + Music-bed loop). **Not** a second mix tree |
| **Hear it** | UI tick plays on the newly selected device |
| **Code** | `engine/src/audio_out.rs` — cpal enumerate + stream. Stream handle stays on the window thread (`Stream` is not Sync) |

Do **not** invent a second mixer, new bus, or extra bind. Do **not** claim Augury spatial rewrite or Hypha Graphics post. #21 Voice/Music/FX · #54/#62 file slots · #64 playlist · #27/#56 spatial+reverb stay.

See `PEEK_FINDINGS.md` Closed by #82 + `EXTRACTION_AUDIO_LOCK.md`.

## H shoulder-swap tilt (Range Tech — landed #84)

Evan lock. **Shipped** [fulcrumRust #84](https://github.com/initialvisuals/fulcrumRust/pull/84) (2026-09-09, `7d7e18f5`). **Range Tech** owns H tilt on existing ViewmodelDials / ADS cant DNA. Travel stays **#59**. Same `apply_shoulder_crossover` → `PoseOffset` → `pose_basis` as ADS/hip cant — **not** a second viewmodel system. PreferredHand + new-profile onboard **later landed #116**.

| Dial | Was | Now |
|------|-----|-----|
| `shoulder_cross_x / y / z` | hip +X ~**0.10** → ~**−0.041** | unchanged |
| `shoulder_x_min` | **−0.055** | unchanged (arms-limited; not a full left park) |
| `shoulder_cross_pitch` | *(none)* | **0.08** — chest-cross lift (ADS cant 0.02 / hip cant 0.0365 DNA) |
| `shoulder_cross_yaw` | 0.16 | **0.32** — inward yaw that reads |
| `shoulder_cross_roll` | 0.10 | **0.39** — half of U-cycle / ADS cant 0.785 |
| `shoulder_ads_keep` | **0.32** | unchanged (ADS keeps a fraction of travel and tilt) |
| `shoulder_spring` | **8.0** | unchanged |
| `shoulder_viewmodel` | **0.12** | unchanged |
| Kit boxes / `scale.x` | authored +X | still authored — **no `scale.x = −1`**; ejection stays gun-right |

**Not** a capsule/eye slide, not a mesh mirror, no mirrored kit boxes.

| Seat | Owns |
|------|------|
| **Range Tech** | H travel (#59) + tilt path (#84). First +0.08 / left hold **#94**. Live hip / ready-Y **#98**. Live hip_low **#99**. Live ads_cant **#100** |
| **Hypha** | PreferredHand + new-profile onboard — **later landed #116**. Do **not** claim as this PR |

Live hip / `shoulder_cross` / left tilt **superseded #98** (after #94 first +0.08) — hip **0.2403 / −0.2128 / −0.1833**; `shoulder_cross_x` **−0.281** / `shoulder_cross_y` **0.032**; pitch/yaw/roll **0.04 / 0.10 / 0.08** (slight straighten, not chest-cross cant). Live hip_low **superseded #99**. Live ads_cant **landed #100**. See RH hip one more body-width + ready-hip Y (#98) + low-hip shotgun stance (#99) + canted CQC ADS (#100).

See `PEEK_FINDINGS.md` Closed by #84.

## Patch A RH hip bias (Range Tech — landed #94)

Evan lock. **Shipped** [fulcrumRust #94](https://github.com/initialvisuals/fulcrumRust/pull/94) (2026-09-09, `a3a42e4f`). **Range Tech** owns RH hip X + H travel deepen + left-hold straighten on existing ViewmodelDials. Position only on RH — no inward yaw to fake aim. H dest stays ~**−0.041**. PreferredHand + new-profile onboard **later landed #116**.

| Dial | Main | Now |
|------|------|-----|
| MP9-Z hip / hip_low X | 0.1043 | **0.1843** (+0.08) |
| MP9-Z hip_cant X | 0.1393 | **0.2193** |
| MP9-Z sprint_high X | 0.21 | **0.29** |
| SR-25 hip / hip_low X | 0.12 | **0.20** |
| SR-25 hip_cant / sprint_high X | 0.155 / 0.22 | **0.235 / 0.30** |
| M24 hip / hip_low X | 0.125 | **0.205** |
| M24 hip_cant / sprint_high X | 0.16 / 0.23 | **0.24 / 0.31** |
| ADS hold X (iron / holo / acog / sniper / cant) | feel-lab bore-center | unchanged |
| inspect X | 0.0593 | unchanged |
| `shoulder_cross_x` | −0.145 | **−0.225** (keeps H dest ~−0.041) |
| `shoulder_x_min` | **−0.055** | unchanged |
| `shoulder_cross_pitch` / yaw / roll | #84 **0.08 / 0.32 / 0.39** chest-cross | **0.04 / 0.10 / 0.08** slight straighten |
| Kit boxes / `scale.x` | authored +X | still authored — **no `scale.x = −1`** |

**Not** a mesh mirror, not the old #84 chest-cross cant, no inward yaw to fake aim. #89 tracers / particles stay. Tip spawn + `hip_honest_dir` unchanged.

| Seat | Owns |
|------|------|
| **Range Tech** | RH hip X + H travel deepen + left-hold straighten (#94) |
| **Hypha** | PreferredHand + new-profile onboard — **later landed #116**. Do **not** claim as this PR |

See `PEEK_FINDINGS.md` Closed by #94. Live **End** tuner on these same dials **landed #97**. Live hip / ready-Y **superseded #98**. Live hip_low **superseded #99**.

## Aim-offset tuner + attachment sockets (Range Tech — landed #97)

Evan lock. **Shipped** [fulcrumRust #97](https://github.com/initialvisuals/fulcrumRust/pull/97) (2026-09-09, `6908ec88` / `8ac9130b`). **Range Tech** owns the live aim-offset / attachment offset tuner DNA only — not Home chrome, not hitch logger, not EffectComposer, not a second pose system. `AimTuner` writes the **same** `ViewmodelDials` + `AttachmentOffsets` (optic / can from authored `kit_mesh` sockets). Identity PoseOffset = live authored mounts (**#98** after the body-width + ready-Y pass; was #94 when #97 shipped). Home debugger **later landed #110** (was #95 tip / unbound at #97 ship). **AIM TUNE LIVE persist landed #103** — End→Hypha `project.json`; #97 End / Delete dump stay.

| Dial | Lock |
|------|------|
| Toggle | **End** (feel-lab Home remapped like X→Z). Home debugger **later landed #110** |
| Mode | Insert = WEAPON ↔ ATTACH |
| Target | PageDown = pose / attachment |
| Step | PageUp cycle · FINE default |
| Axis | ↑↓ select · ←→ / num± nudge · PX PY PZ RX RY RZ |
| Dump | Delete = paste-ready JSON (feel-lab `example_smg` object + attachments) |
| LIVE persist | **landed #103** — Hypha `project.json` · `aim_live` default **true** · End sheet `LIVE` / `OFF` |
| Glasses | `AIM TUNE` |

| Step | pos | rot |
|------|-----|-----|
| MICRO | **0.0005** | **0.001** |
| FINE (default) | **0.002** | **0.005** |
| MED | **0.01** | **0.02** |
| COARSE | **0.05** | **0.1** |

#97 End tuner nudges **#98** ready-hip / H + **#99** hip_low + **#100** `ads_cant` (MP9-Z hip **0.2403 / −0.2128 / −0.1833**; ADS iron X **0.0084**; SR-25 / M24 hip **0.256 / −0.224 / −0.208** / **0.261 / −0.229 / −0.228**; `shoulder_cross_x` **−0.281** / `shoulder_cross_y` **0.032**; hip_low MP9-Z **0.2403 / −0.3528 / −0.1513** / pitch **0.145**; ads_cant MP9-Z **0.0423 / −0.148 / −0.136** / yaw **0.11**; left hold slight straighten stays). Kit boxes + muzzle tip follow live can/optic offsets. World drops stay authored identity.

| Seat | Owns |
|------|------|
| **Range Tech** | Live End tuner DNA on existing ViewmodelDials + kit_mesh sockets (#97). LIVE persist into Hypha `project.json` (#103) |
| **Augury** | Home debugger **later landed #110**. Do **not** claim shipped by #97 / #103 |

See `PEEK_FINDINGS.md` Closed by #97 / Closed by #103.

## AIM TUNE LIVE persist (Range Tech — landed #103)

Evan lock. **Shipped** [fulcrumRust #103](https://github.com/initialvisuals/fulcrumRust/pull/103) (2026-09-09, `74da84e3` / `e0452f82`). **Range Tech** steals the Hypha Graphics/Audio `project.json` persist path so End AIM TUNE peeks survive quit/relaunch. Does **not** take Augury Home (debugger **later landed #110**). #97 End tuner / Delete JSON dump schema stay.

| Key | Default | Live bind |
|-----|---------|-----------|
| `aim_live` | **true** (RECORD/LIVE stub) | End sheet `LIVE` / `OFF`. Later RECORD toggle — **no bind** |
| `aim_tune.example_smg` | authored MP9-Z + identity optic/can | **End** · WEAPON / ATTACH · G / 4 |
| `aim_tune.example_rifle` | authored SR-25 | G / 5 |
| `aim_tune.example_sniper` | authored M24 | G / 6 |
| Pose keys | `hip` `hip_low` `hip_cant` `sprint_high` `ads` `ads_cant` `ads_holo` `ads_acog` `ads_sniper_scope` `inspect` | PageDown |
| Attach keys | `attachments.optic` `attachments.can` | Insert → ATTACH |
| Pose object | `{x,y,z,rotX,rotY,rotZ}` | same Delete dump schema |

Load on Deploy / new session (`Settings::boot` → `Session::apply_aim_settings`). Each End nudge when LIVE flushes the Hypha persist path. Partial merge: missing kits/poses keep authored **#98 / #99 / #100** numbers (ready-hip / low-hip / ads_cant stay those peeks until nudged).

| Seat | Owns |
|------|------|
| **Range Tech** | AIM TUNE LIVE persist on Hypha `project.json` (#103). #97 End stays |
| **Hypha** | Persist path (`project.json` / `FULCRUM_SETTINGS`) — Range steals, does not take Graphics guts |
| **Augury** | Home debugger **later landed #110**. Do **not** claim shipped by #103 |

Out of scope (do **not** claim shipped by #103): Augury Home tabs/logger (that is **#110**) · bake-permanent-defaults rewrite · UV (#101) · Beabim · heat rewrite · RECORD toggle bind.

See `PEEK_FINDINGS.md` Closed by #103.


## CE Home debugger (Augury — landed #110)

Evan lock. **Shipped** [fulcrumRust #110](https://github.com/initialvisuals/fulcrumRust/pull/110) (2026-09-09, `7ff3c311`). **The Augury** owns the native Home overlay (not a TS paste). Verified against CE `utils/debug.tsx` on `_CONCRETE_ECHO_` `4_15_26` (v0.2.8). **End** stays Range AIM TUNE (#97 / #103). Hitch *visibility* is this cook; Hypha stream hitch *fix* **later landed #108**. Home LOGS COPY + tracker toggles **later landed #121**. Closes clerk #95 / #104 overnight hitch path (Home logger tab).

| Dial | Value |
|------|--------|
| Bind | **Home** toggle (CE). **End** stays Range AIM TUNE (#97 / #103) |
| Tabs | **LOGS** · **TELE** · **CHEAT** (←/→ cycle; CE names LOGS / TELEMETRY / CHEATS) |
| Hitch warn | frame **> 33 ms** → `WARN` |
| Hitch spike | frame **> 100 ms** → `HITCH` |
| Reason tags | `FRAME` · `LOAD` (boot/deploy gate) · `STREAM` (Transvoxel remesh) · `BAKE` (extract rigidize ms) · `GATE` (HIDEOUT / DEPLOY / EXTRACT) |
| Ring | 256 timed lines (CE ~800); 8 visible rows; Up/Down scroll. Ring **800** **later landed #121** |
| Telemetry | 1s FPS, last/max frame ms, warn/spike counts, pos, place, stream resident/cold, HP/AR |
| Cheats | **GOD** skip `apply_player_wound` · **NOCLIP** skip walls + playable clamp · **TELEPORT** current-world spawn · **SPAWN** `Locus::standard` at look+4 m (extract; hideout stub log) |
| Persist | `project.json` `debugger_tab` (optional; shares file with Range `aim_live` / `aim_tune` — one `persist_settings()` flush). `log_*` **later landed #121** |
| Chrome | analysis-knowledge-core: thin white frames, fade-in white mono. Glasses `DEBUG` |

Raw wall-clock frame time is measured **before** the 50 ms sim clamp (a 400 ms bake/stream hitch still prints `400ms`).

| Seat | Owns |
|------|------|
| **Augury** | Native Home debugger overlay (#110). Glasses `DEBUG`. Analysis-core chrome. LOGS COPY / tracks **later landed #121** |
| **Range Tech** | **End** AIM TUNE (#97) + LIVE persist (#103) — untouched |
| **Hypha** | Stream hitch *fix* **later landed #108**. Persist path shared (`debugger_tab` + `aim_live` / `aim_tune`) |

Out of scope (do **not** claim shipped by #110): Hypha stream hitch *fix* (that is **#108**) · shoot/feel · stamps/UV · MP sync · hatch elevator (**later landed #115**) · CE WEAPON/ATTACHMENT tuner (already **End**) · CE PERF/PHYS/RENDER/heartbeat/combat-log flags (house-docs steal later) · full CE debugger tab contract beyond this native shell.

See `PEEK_FINDINGS.md` Closed by #110. Hitch *fix* shelf: Closed by #108. LOGS COPY / tracks: Closed by #121.

## Home LOGS COPY + tracker toggles (Augury — landed #121)

Evan lock. **Shipped** [fulcrumRust #121](https://github.com/initialvisuals/fulcrumRust/pull/121) (2026-09-09, `2416ec09`). **The Augury** owns the LOGS follow-up peek after Home LOGS. #110 stays the tabs+logger foundation. Verified against CE `utils/debug.tsx` on `_CONCRETE_ECHO_` `4_15_26`: LOGS COPY dumps the boot ring; settings keep separate tracker checkboxes. Does **not** rewrite Hypha stream hitch amortize (#108). Emits/tags richer STREAM lines Hypha already feeds.

| Dial | Value |
|------|--------|
| Bind | **Home** LOGS. **End** AIM TUNE untouched |
| Copy | **Enter** on LOGS copies the **full** boot→now ring (clipboard via existing leftover helper + cwd `fulcrum.logs`; `FULCRUM_LOGS` override) |
| Ring | **800** timed lines (CE ~800). Overlay still 8 rows, Up/Down scroll |
| Timestamp | `[sssss.mmm]` on every dump/overlay line |
| Tracks | **STREAM** · **BAKE** · **GATE** · **PLAY**/GAMEPLAY · **INT**/INTERNAL — Insert selects, Delete toggles. Off quiets that category (not one console dump) |
| Persist | `project.json` `log_stream` / `log_bake` / `log_gate` / `log_gameplay` / `log_internal` (default **on**) + existing `debugger_tab` |
| Hitch | warn **> 33 ms** / spike **> 100 ms** stay. TELE **max ms** still updates when a track is off |
| Events | medium, edge-only — BOOT / GPU / GATE / STREAM r↑ cold↓ / FIRE (burst start) / HIT / AI brain / HATCH / WOUND / DOWN / DEAD / STIM / HEAL / RELOAD / SLASH / DROP / TAKE / CHEAT / COPY. No per-frame spam |
| Chrome | analysis-knowledge-core. Glasses `DEBUG` |

| Seat | Owns |
|------|------|
| **Augury** | Home LOGS COPY + tracker toggles (#121). Glasses `DEBUG`. Analysis-core chrome. Hitch *visibility* stays Augury |
| **Range Tech** | **End** AIM TUNE (#97) + LIVE persist (#103) — untouched |
| **Hypha** | Stream hitch amortize (#108) — not rewritten. Emits STREAM/BAKE; #121 tags richer STREAM lines |

Out of scope (do **not** claim shipped by #121): Hypha #108 hitch amortize rewrite · End AIM TUNE · door/extract cancel · Beabim pause/MP · Range feel · stamps.

See `PEEK_FINDINGS.md` Closed by #121. Foundation: Closed by #110. Hitch *fix* shelf: Closed by #108.

## RH hip one more body-width + ready-hip Y (Range Tech — landed #98)

Evan lock. **Shipped** [fulcrumRust #98](https://github.com/initialvisuals/fulcrumRust/pull/98) (2026-09-09, `48518709` / `5b02e2ab`). **Range Tech** owns RH hip-family + `shoulder_cross` so RH matches left-hold gold (slightly tighter) and default HIP is a ready hold, not chin-weld. Dial-only on existing ViewmodelDials. Position only on RH — no inward yaw, no `scale.x = −1`. H dest stays ~**−0.041** X / ~**−0.181** Y. #98 did **not** ship a shotgun low-hip — that U-cycle deepen **later landed #99**. PreferredHand + new-profile onboard **later landed #116**.

| Dial | Main (#94) | Now |
|------|------------|-----|
| MP9-Z `hip` X / Y / Z | 0.1843 / −0.1688 / −0.1953 | **0.2403 / −0.2128 / −0.1833** (+0.056 X = 2 × MP9 `receiver_half.x` **0.028** / polymer shell **0.056**; Y **−0.044** ready-hip drop; Z **+0.012** tighter) |
| MP9-Z `hip_low` X / Y / Z | 0.1843 / −0.2788 / −0.1753 | **0.2403 / −0.2788 / −0.1633** at #98 (+X/+Z only). Live **superseded #99** |
| MP9-Z `hip_cant` X / Y / Z | 0.2193 / −0.1938 / −0.2103 | **0.2753 / −0.1938 / −0.1983** (Y stays; +X/+Z only) |
| MP9-Z `sprint_high` X | 0.29 | **0.346** (X only) |
| SR-25 `hip` X / Y / Z | 0.20 / −0.18 / −0.22 | **0.256 / −0.224 / −0.208** |
| M24 `hip` X / Y / Z | 0.205 / −0.185 / −0.24 | **0.261 / −0.229 / −0.228** |
| ADS hold X (iron / holo / acog / sniper / cant) | feel-lab bore-center | unchanged |
| inspect X | 0.0593 | unchanged |
| `shoulder_cross_x` | −0.225 | **−0.281** (keeps H dest ~−0.041) |
| `shoulder_cross_y` | −0.012 | **0.032** (keeps H dest Y ~−0.181 after the RH drop) |
| `shoulder_x_min` | **−0.055** | unchanged |
| left pitch / yaw / roll | #94 **0.04 / 0.10 / 0.08** | unchanged — gold already vertical |
| Kit boxes / `scale.x` | authored +X | still authored — **no `scale.x = −1`** |

**Not** a mesh mirror, no inward yaw to fake aim. #89 tracers / particles stay. Tip spawn + `hip_honest_dir` unchanged. #97 End tuner still live for fine polish. Live hip_low **superseded #99**.

| Seat | Owns |
|------|------|
| **Range Tech** | RH hip-family + `shoulder_cross` body-width + ready-Y (#98) |
| **Hypha** | PreferredHand + new-profile onboard — **later landed #116**. Do **not** claim as this PR |

See `PEEK_FINDINGS.md` Closed by #98. #97 End tuner nudges these **#98** ready-hip / H defaults. Live hip_low is **#99**.

## Low-hip shotgun stance (Range Tech — landed #99)

Evan lock. **Shipped** [fulcrumRust #99](https://github.com/initialvisuals/fulcrumRust/pull/99) (2026-09-09, `ed6dff0e`). **Range Tech** owns U-cycle `hip_low` so LowHip is a true shotgun low-ready, not a 6 cm nudge under walking hip. Dial-only `ViewmodelDials.hip_low` (MP9 / SR-25 / M24). Position + pitch only — no inward yaw, no `scale.x = −1`. Ready hip / hip_cant / ADS / H crossover stay **#98**. RMB from LowHip = iron ADS (not `ads_cant`). Not chin-weld. Greyzone 45° canted CQC ADS **later landed #100**. PreferredHand + new-profile onboard **later landed #116**.

| Dial | Main (#98) | Now |
|------|------------|-----|
| MP9-Z `hip_low` X / Y / Z | 0.2403 / **−0.2788** / −0.1633 | **0.2403 / −0.3528 / −0.1513** (X same; **−0.074 Y**; +0.012 Z tucked) |
| MP9-Z `hip_low` pitch | 0.0765 | **0.145** (~8° muzzle down; +0.0685) |
| MP9-Z `hip_low` yaw / roll | 0 / 0 | **unchanged** — no cant |
| MP9-Z ready `hip` | 0.2403 / −0.2128 / −0.1833 | **unchanged** (#98 lock) |
| Ready → low Y gap | 0.066 | **0.140** |
| SR-25 `hip_low` Y / Z / pitch | −0.29 / −0.188 / 0.08 | **−0.364 / −0.176 / 0.148** |
| M24 `hip_low` Y / Z / pitch | −0.295 / −0.208 / 0.078 | **−0.369 / −0.196 / 0.146** |
| ADS hold X / `ads_cant` | iron 0.0084 / roll 0.785 | **unchanged** at #99 — Greyzone CQC ADS **later landed #100** |
| `shoulder_cross_*` | #98 H dest ~−0.041 / ~−0.181 | **unchanged** |
| U-cycle glasses | LOW | **LOW HIP** |

**U-cycle:** Chest (`hip`) → LowHip (`hip_low`) → Canted (`hip_cant`) → Chest. Glasses LowHip **LOW HIP**. Still shootable. #97 End AIM TUNE still nudges `hip_low`. Viewmodel pose ease **later landed #109** (`hold_spring` **7.0**); glasses still snap.

**Not** a mesh mirror, no inward yaw, no Beabim / heat / terrain. Greyzone 45° canted CQC ADS is **#100** (not this hip_low cook).

| Seat | Owns |
|------|------|
| **Range Tech** | U-cycle `hip_low` shotgun low-ready (#99) |
| **Hypha** | PreferredHand + new-profile onboard — **later landed #116**. Do **not** claim as this PR |

See `PEEK_FINDINGS.md` Closed by #99. #97 End tuner still live for fine polish on these #99 hip_low defaults. Ready-hip / H stay #98. Canted CQC ADS **later landed #100**.

## Canted 45° Greyzone CQC ADS (Range Tech — landed #100)

Evan lock. **Shipped** [fulcrumRust #100](https://github.com/initialvisuals/fulcrumRust/pull/100) (2026-09-09, `842b3efa`). **Range Tech** owns `ads_cant` so cant carries into *aim*, not just `hip_cant`. Dial-only `ViewmodelDials.ads_cant` (MP9 / SR-25 / M24). RMB from U-cycle CANT + hold-Mouse5 both enter that pose. Canted ADS FOV is the holo **60°** CQC lane — ACOG/scope zoom does not follow a CQC cant. Glasses **CANT 45** / **CANT ADS**. `ads_for(Canted, _)` already returned `ads_cant`; this cook makes that target a first-class CQC aim pose (was rolled hip-cant parked near iron). `hip_low` stays **#99**. Ready-hip / hip_cant / primary ADS / H stay **#98**. #97 End AIM TUNE still nudges `ads_cant`. PreferredHand + new-profile onboard **later landed #116**.

| Dial | Main (#99) | Now |
|------|------------|-----|
| MP9-Z `ads_cant` X / Y / Z | 0.034 / −0.142 / −0.172 | **0.0423 / −0.148 / −0.136** |
| MP9-Z `ads_cant` pitch / yaw / roll | 0.02 / 0.035 / 0.785 | **0.024 / 0.11 / 0.785** (roll stays) |
| X meaning | leftover slide | iron **0.0084** + optic-root **0.048·sin45** (eye on the 45° rail, bore not under the LPVO) |
| Z meaning | iron-ish | CQC-close (holo −0.1335 lane) |
| Yaw meaning | leftover ~2° | inward to body (~6° / 0.11) |
| SR-25 / M24 `ads_cant` | 0.036–0.037 / −0.148 / −0.182 | **0.0468 / −0.154 / −0.148** (root 0.052·sin45) |
| `hip_low` | #99 −0.3528 / pitch 0.145 | **unchanged** |
| Iron ADS X | 0.0084 | **unchanged** (bore-center) |
| ready-hip / `hip_cant` / H | #98 locks | **unchanged** |

**Binds:** Primary RMB from Chest/LowHip → seated optic ads (unchanged). **U** → CANT + RMB → `ads_cant` @ 60° CQC. hold-**Mouse5** from any hold → `ads_cant` @ 60° CQC (does not steal U / RMB / melee). Glasses Canted **CANT 45**; in `ads_cant` **CANT ADS**.

**Not** a canted-holo mesh, no IOR/bodycam glass, no mesh flip, no Beabim / heat / terrain.

| Seat | Owns |
|------|------|
| **Range Tech** | `ads_cant` CQC aim pose (#100) |
| **Hypha Graphics** | IOR / canted-holo mesh — **when LPVO**. Do **not** claim shipped |
| **Hypha** | PreferredHand + new-profile onboard — **later landed #116**. Do **not** claim as this PR |

See `PEEK_FINDINGS.md` Closed by #100. #97 End tuner still live for fine polish on these #100 `ads_cant` defaults. hip_low stays #99. Ready-hip / H stay #98. U-cycle pose ease **later landed #109**.

## U-cycle hold springs (Range Tech — landed #109)

Evan lock. **Shipped** [fulcrumRust #109](https://github.com/initialvisuals/fulcrumRust/pull/109) (2026-09-09, `6108cf91` / `fc30eb30`). **Range Tech** owns U-cycle pose ease so Chest / LOW HIP / CANT no longer snap. `home_hold` was feeding `blend_aim` as the hip on the same frame; now eases pos+rot toward the selected HomeHold on the existing ADS / H / sprint exp-approach path (`k = 1 − e^{−rate·dt}`). ADS enter speed stays its own dial — **#113** scales `blend_speed` **6.4** by kit ergo (not folded into `hold_spring`). Glasses still snap CHEST / LOW HIP / CANT 45; the viewmodel springs. Inspect and sprint_high still lerp on top of the eased home. Mouse5 / RMB cant-ADS paths stay. 1P viewmodel only — Beabim 3P stubs untouched. Load phases never tick FeelState, so the first U after deploy seeds `hold_blend` from the current home *before* cycle. STEAL_MAP pose-ease → **in**. #98/#99/#100 poses · #97 End tuner · #103 LIVE persist · #57/#59 springs DNA stay. PreferredHand + new-profile onboard **later landed #116**.

| Lane | Dial | Rate | Role |
|------|------|------|------|
| U-cycle home (pos+rot) | `hold_spring` | **7.0** | NEW — house-medium between ADS and H |
| ADS enter / exit | `blend_speed` | **6.4** (feel-lab 8) | own dial — **#113** scales by kit `HandlingStats.ergo` (not folded into `hold_spring`) |
| H crossover | `shoulder_spring` | **8.0** | unchanged |
| Sprint high-ready | `sprint_hold` | **6.2** | unchanged |
| Inspect overlay | hardcoded | **10.0** | unchanged |

**Not** Beabim / 3P, heat, terrain, PreferredHand, or ADS `blend_speed` folded into `hold_spring`.

| Seat | Owns |
|------|------|
| **Range Tech** | 1P U-cycle hold springs (`hold_spring` **7.0**) |
| **Beabim** | 3P stubs — **untouched**. Do **not** claim shipped |
| **Hypha** | PreferredHand + new-profile onboard — **later landed #116**. Do **not** claim as this PR |

See `PEEK_FINDINGS.md` Closed by #109. #97 End / #103 LIVE stay. Poses stay #98/#99/#100. Kit handling / ergo / MOA **later landed #113**.

## Kit handling / ergo / MOA (Range Tech — landed #113)

Evan lock. **Shipped** [fulcrumRust #113](https://github.com/initialvisuals/fulcrumRust/pull/113) (2026-09-09, `719deae6` / `421d61b8`; merge tip `b2d384144c8ad23d500f59a0c3a02ab3d41b92f8`). **Range Tech** owns the thin kit sheet. `HandlingStats` is a readable view over the per-kit fire/ADS numbers `FeelSheet` already owns — fire and ADS consume those same fields. Not house mastery, not a gear UI, not a skills system. 1P feel only. #109 `hold_spring` **7.0** stays sibling (ADS blend is **not** folded into it). STEAL_MAP handling → **in**. House mastery row stays parked.

| Dial | Lock |
|------|------|
| **Ergo → ADS** | Base `blend_speed` **6.4** × kit ergo. MP9-Z **1.25** → **8.00**; SR-25 **1.00** → **6.40**; M24 **0.80** → **5.12**. Still the ADS spring |
| **Handling → recoil** | `1 / handling` on authored kick / pitch / yaw. `ads_recoil_mul` **0.6** stays. Handling MP9 **1.15** · SR-25 **1.00** · M24 **0.90** |
| **Authored kick / pitch / yaw** | Per-gun (MP9 1.0 / 0.012 / 0.008 · SR-25 1.15 / 0.018 / 0.010 · M24 1.75 / 0.035 / 0.012) |
| **MOA** | Hip cone (minutes) after `hip_honest_dir` (no 100 m loft miss). ADS × **0.22**. Hip MP9 **4.0** · SR-25 **1.2** · M24 **0.40** |
| **Velocity / cycle** | Same `muzzle_speed` / `cyclic_rpm` / interval as `SmgFireDials` (MP9 300 / 1200 · SR-25 785 / 0.14s · M24 810 / 0.65s) |
| **Mag fill** | `ReloadKind::duration_for(mag_fill)` stub. Defaults **1.0** (authored 1.10 / 0.46 s) |

**Not** house mastery / gear UI / Beabim 3P / net / loot / heat rewrite / Lab-Rat / Augury Home / PreferredHand.

| Seat | Owns |
|------|------|
| **Range Tech** | 1P `HandlingStats` / `FeelSheet::handling` (#113) |
| **Beabim** | 3P / net / loot — **untouched**. Do **not** claim shipped |
| **Hypha** | PreferredHand + new-profile onboard — **later landed #116**. Do **not** claim as this PR |
| **house** | House mastery row — **parked**. Do **not** claim shipped |

See `PEEK_FINDINGS.md` Closed by #113. #109 `hold_spring` **7.0** stays sibling. #97 End / #103 LIVE stay. Poses stay #98/#99/#100.


## PreferredHand + new-profile onboard (Hypha — landed #116)

Evan lock. **Shipped** [fulcrumRust #116](https://github.com/initialvisuals/fulcrumRust/pull/116) (2026-09-09, `6018f8ad384cbc0bcf6e7d9c818f2d23f3d145ad` / tip `d531b27f11281f993f53ccbf8d1579a8539ad91e`). **Hypha** owns PreferredHand + NEW PROFILE onboard. Range H travel / tilt / hip / springs / ergo stay Range (#59/#84/#94/#98/#99/#100/#109/#113). A-notes already `[X]` PreferredHand onboard / `[~]` persistent+live profile (stash stub) — do not invent A-note PRs / rewrite A-notes.

| Dial | Lock |
|------|------|
| **PreferredHand** | Enum on input/profile. **Right** default if unset |
| **NEW PROFILE** | Title Deploy / Host / Join gate. Must pick RIGHT / LEFT before first raid |
| **Permanent** | `project.json` `profile_onboarded` + `preferred_hand` |
| **Live** | Session copy of permanent. Death clears live |
| **Extract→stash** | Stub hook. Beabim KIND_LOOT already covers Z/F raid items. Full PMC stash / character tab later |
| **shoulder_t** | **0** = authored RH · **1** = existing left dest. Seats Range H crossover. **No** `scale.x = −1` / mesh flip |

**Not** full PMC stash / character tab / world-pool death loot / Beabim net sync of PreferredHand. Does **not** steal Range ergo / MOA / pose springs, Augury hatch, Lab-Rat stamps, Beabim world/sim / loot trail, root README.

| Seat | Owns |
|------|------|
| **Hypha** | PreferredHand enum · NEW PROFILE gate · `project.json` permanent vs live · death-clears-live · extract→stash stub · `shoulder_t` seats Range H (#116) |
| **Range Tech** | H travel / tilt / hip / springs / ergo (#59/#84/#94/#98/#99/#100/#109/#113) — **untouched**. Do **not** claim as this PR |
| **Beabim** | KIND_LOOT Z/F trail (#102) · world/sim leftover (#119) · no-pause / KIND_RAID (#122) — **untouched**. No PreferredHand net sync |
| **Augury** | Hatch / EXTRACT elbows (#85/#115) — **untouched** |
| **Lab-Rat** | Stamps — **untouched** |

See `PEEK_FINDINGS.md` Closed by #116. Range H dest stays #98. KIND_LOOT stays #102.

## 1P viewmodel ≠ 3P biped gun (MP honesty) — partial shipped #91

Evan lock (2026-09-09 InitialVisuals). **Partial shipped #91** — peer biped hip gun stub (`reconstructed_gun`). Full 3P kit honesty / hands / gear sync still **open**. Overnight cooks steal from this shelf. Goes with HANDS down the road.

**Dial:** first-person weapon viewmodel ≠ multiplayer biped + weapons + gear.

- Fake / artistic posing (hip fire sold for feel, canted CQC, etc.) can stay **aggressive on the 1P viewmodel**
- Other players must **not** see guns sticking through eyeballs for "artistic merit"
- Separate the 1P weapon viewmodel from the MP biped + weapons + gear
- **#91** landed a 3-box gun stub on the networked muzzle — biped-honest hip, not 1P `muzzle_world()` / #94/#98/#99 cant
- **#119** peer shot muzzle uses that same hip stub + look dir — does **not** publish 1P cant
- Do **not** claim Mixamo / full 3P kit honesty

| Seat | Owns |
|------|------|
| **Range Tech** | 1P dials / AIM TUNE (#97 End sheet); #94/#98/#99 hip stay 1P-only |
| **Beabim** | 3P sync path — peer gun stub **landed #91**; peer shot muzzle **#119** uses that hip stub; full kit honesty still open |
| **Lab-Rat** | Stamps stay out |

See `PEEK_FINDINGS.md` Holding / locked intent — 1P ≠ 3P + Closed by #91 + Closed by #119.

## Scope glass (when LPVO lands) — holding / not shipped

Evan lock (2026-09-09 InitialVisuals). **Holding until LPVO — not shipped.** Overnight cooks steal from this shelf. Do **not** claim LPVO or glass live.

- **Ramp** — greyscale / black-and-white. **Not** a color ramp
- **Curve** — fake curve of the glass + thickness; cut lines or flatten parts (Blender-style)
- **Magnify** — IOR glass + ramp-driven magnify
- **Shader** — bodycam optic: **no PiP**. Glass / radial / reflect in the **scope pass**
- Live **V** iron/holo/acog + FOV stay #14/#22. Hoods stay boxes

| Seat | Owns |
|------|------|
| **Range Tech** | AIM TUNE placements first (#97 End sheet) |
| **Hypha Graphics** | IOR / ramp / magnify / bodycam scope pass — **when LPVO** |
| **Augury** | Glasses stay labels only — not a second optic HUD / PiP |
| **Lab-Rat** | Stamps — not this row |

See `PEEK_FINDINGS.md` Holding — greyscale glass + Evan asset-ask.

## Evan asset-ask path — holding / locked intent

Evan lock (2026-09-09 InitialVisuals). **Holding / locked intent — not shipped.** Overnight cooks steal from this shelf.

- Clone from Concrete Echo / aim-offset **attachment tables** first
- If missing: **ask Evan** — he has **this week** (from 2026-09-09) to model + texture. Primitives stay scaffolding
- Style grows with peeks (void-spore + grit floor; authored fills in)
- Lab-Rat stamps keep **procedural grit** until the asset list lands, then bake onto authored

| Seat | Owns |
|------|------|
| **Range Tech** | Kit / attachment clone from CE + aim-offset tables; AIM TUNE sit (#97) |
| **Lab-Rat** | Procedural grit until the list; then bake onto authored |
| **Evan** | This-week model + texture for missing ask |
| **Hypha** | Does **not** invent glass/LPVO assets here |

Store `dBXpg` still **open**. Kit PBR stub stays #64. Do **not** claim authored attachments / LPVO glass / Evan models shipped. See `PEEK_FINDINGS.md` Holding — greyscale glass + Evan asset-ask.

## Hypha Graphics dump (landed #86)

Evan lock. **Shipped** [fulcrumRust #86](https://github.com/initialvisuals/fulcrumRust/pull/86) (2026-09-09, `13865b3f`). **Hypha** owns Options Graphics / sky / post defaults. Steal Evan’s aim-offset Settings Lighting dump onto existing fulcrumRust Graphics / post / sky dials after **#81** 19×19 open extract. Thin Options bindings only where the render path already supported the value. Persist `project.json` alongside Range `output_device`.

| Dump key | Value | Path |
|----------|--------|------|
| fogEnabled | true | Options **FOG** + extract `haze_max` (hideout stays **0**) |
| fogNear / fogFar | **375 / 520** | Options + `LightingFrame` haze start/range (was 16 / 48) |
| lightAmbMul / lightFillMul / lightHemiMul | **0.11 / 0.41 / 0.61** | already `sky::AMB_MUL` / `FILL_MUL` / `HEMI_MUL` |
| lightKeyMul / lightRimMul / lightMoonMul | **2.11 / 1.65 / 1.06** | already `sky::KEY_MUL` / `RIM_MUL` / `MOON_MUL` |
| exposureMul | **1.44** | already `sky::EXPOSURE_MUL` |
| sunPunch | **0.51** | existing sky disc/halo (`sun_dir.w`) |
| clouds | **0.63** | `SkyState` default (was 0; **,** / **.** still nudge) |
| skyHdri | true | already default; **/** still toggles |
| camNear / camFar | **0.05 / 2000** | Options + `perspective_rh` / post linear-Z (was 0.06 / 280) |
| adsDofTaps / adsDofRadius | **12 / 0.0048** | already **#68** |

| Dial | Lock |
|------|------|
| **Options Graphics** | **FOG / FOG NEAR / FOG FAR / CAM NEAR / CAM FAR** rows live + persist. **#90** adds **WARP** after CAM FAR (`GFX_LEN` 12→13; these #86 rows keep indices) |
| **Exposure keyboard** | Still unbound after **#78** (no second pair; sky `nudge_exposure` may still exist) |
| **,** / **.** | Clouds still work (step 0.10) |
| **/** | HDRI toggle stays |
| **Do not invent** | bloom **0.08** · godRays **2** · brightness / gamma **1 / 1** — no existing GPU path |
| **sunSize** | dump **0.62** — parked here; **#87** now rides the sky disc/halo (`mix(1800, 80)`) |
| **Parked** | Heat haze dials — Range **#71**. HDRI sun black-out / blow-out **completed #87** (shared Range Tech + Hypha) |

| Seat | Owns |
|------|------|
| **Hypha** | Options Graphics / sky / post defaults (#86) |
| **Range Tech** | Heat / binds / ballistics / Audio DEVICE — **not** this PR |
| **Lab-Rat** | Stamps — **not** this PR |
| **Augury** | Chrome untouched (Hypha only fills the Graphics list) |

Do **not** invent bloom / god-ray / brightness / gamma paths. sunSize is **no longer parked** — see HDRI sun disc (#87). Do **not** claim Range Audio DEVICE / H tilt / terrain / stamps as this PR. Pixellation / floor-warp is a later Hypha row — see **#90**.

See `PEEK_FINDINGS.md` Closed by #86 + Closed by #87 + Closed by #90.

## Pixellation / floor-warp (Hypha — landed #90)

Evan lock. **Shipped** [fulcrumRust #90](https://github.com/initialvisuals/fulcrumRust/pull/90) (2026-09-09, `54a99f10`). Seat: **Hypha** owns the post dial. **Augury** owns the aesthetic note only — do **not** claim Augury shipped the dial. Steal on the existing post / Options / `project.json` path. No rewrite. Direction lock FoW pixellation influence is live via Hypha post — do **not** steal into Range.

| Dial | Lock |
|------|------|
| **`warp_strength`** | Default **0.01** — lowest positive CE-like step (`0.01 < 0.1`). Same small-step DNA as `CAM_NEAR_STEP` / heat live-gate |
| **Step** | **0.01** — Options A/D / Enter |
| **Range** | **0.0–1.0**. **0 = off** |
| **Skip** | Shader `pixel_warp_uv` skips only at `s <= 0.0` so the default actually runs |
| **Snap** | Mix identity UV toward CE PIXEL SCALE **2** (half-res snap) |
| **Persist** | `project.json` `warp_strength` `{:.2}` → `0.01` |
| **Options** | Graphics **WARP** after CAM FAR. `GFX_LEN` 12→13. Fog/cam/#86 rows keep their indices and values |
| **`PostStack`** | Writes `pixel: [warp_strength, 0, 0, 0]`. New `pixel_warp_uv` after `heat_warp_uv` (heat body not edited) |
| **Smoke** | `gfx=` appends ` warp=0.01` only. Existing `fog/375/520 cam=0.05/2000` substring stays |
| **STEAL_MAP** | Augury pixellation `todo` → **partial**. Fog / stars / proc tex still open |
| **A-notes** | No pixellation/warp ledger row — none invented |

Keep **`heat_warp_uv` (#66 / #71)** distinct from **`pixel_warp_uv` (#90)**. Heat haze stays Range #71 on the Hypha #66 colorless path. Heat stays on `heat-card-dial-sheet.md` — no new root warp dial-sheet.

| Seat | Owns |
|------|------|
| **Hypha** | Post dial / Options **WARP** / `PostStack` pixel mix (#90) |
| **Augury** | Aesthetic note only — **not** the dial |
| **Range Tech** | Heat / binds / ballistics — **not** this PR. Do not steal pixel dither / floor warp |

Intact: Heat haze (#71 / #66) · HDRI sun (#87) · fog/cam dump (#86) · binds · stamps · net · bipeds. Do **not** claim bloom / godRays, Range heat rewrite, Lab-Rat stamps, Beabim MP, or Greyzone canted ADS as this PR.

See `PEEK_FINDINGS.md` Closed by #90 + `AESTHETIC_DIEGETIC_LOCK.md`.

## Augury elbow smart-labels (landed #85)

Evan lock. **Shipped** [fulcrumRust #85](https://github.com/initialvisuals/fulcrumRust/pull/85) (2026-09-09, `f3d60a24`). **The Augury** owns glasses EXTRACT chrome + diegetic interact cards. Range Tech #78 already wired hold-O raid intent (`Session::extract_checking`). No heat / Graphics dump / H tilt / Audio DEVICE.

| Peek | Lock |
|------|------|
| **Card** | Thin white analysis-knowledge-core (`SmartLabel` / `CardPlan`) + **L-elbow / leader** to the world interact pin |
| **Not** | Centered HUD plate (old `-0.34, -0.268` retired for interact cards) |
| **Hold-O** | Paints `EXTRACT` on the nearest in-front hatch/shaft — elbow card, **no popup**. Release clears. **#115** reads `OPEN` / `CLOSED` / `SHAFT`. **#120** countdown wins while armed |
| **EXTRACT** | White mono (not heat/ammo gold). Tip mark + quiet angular junk; curl/Locus edge tints |
| **Hatches** | Yard pad (`-24/-24`, `18/-28`, `-28/16` + shaft `18/-12`) — not GRID_ORIGIN (19×19 rim) |
| **Status strip** | PLACE / clock / INSPECT / … unchanged. **Never** a second ammo HUD |
| **Landed #115** | Hold-F hatch OPEN/CLOSED + shaft RIDE/EXIT (no modal popup) |
| **Landed #120** | Door **F** / OPEN hatch cancellable countdown (`GATE_SECS` **2.20** / `COOL_SECS` **0.55`) |
| **Still ~** | Timed surface kill / extract loot loop |

| Seat | Owns |
|------|------|
| **The Augury** | Elbow cards + EXTRACT chrome (#85) |
| **Range Tech** | Hold-O intent flag (#78) — **not** this PR |
| **Hypha** | Graphics dump (#86) — **not** this PR |

Hatch toggle + shaft ride **landed #115**. Door / extract cancel chrome **landed #120**. Do **not** claim timed surface kill / extract loot loop shipped. Do **not** invent bloom / god-rays or Range / Hypha / Lab-Rat work as this PR.

See `PEEK_FINDINGS.md` Closed by #85 + `AESTHETIC_DIEGETIC_LOCK.md`.


## Augury hatch/elevator glasses UX (landed #115)

Evan lock. **Shipped** [fulcrumRust #115](https://github.com/initialvisuals/fulcrumRust/pull/115) (2026-09-09, `eb8618df` / `eb811e74`; merge tip `469d46b0`). **The Augury** owns hold-F hatch toggle + Akira shaft ride on the #85 elbows. Range #78 already wired hold-O raid intent. No modal popup. Timed surface kill / extract loot loop still **~**. Does **not** remesh Hypha world solids.

| Peek | Lock |
|------|------|
| **HatchBoard** | Quiet hatches start **CLOSED**; hold-**F** toggles OPEN/CLOSED (`engine/src/hatch.rs`) |
| **Shaft** | Loud Akira shaft: hold-**F** rides surface → cap lip → exit pad |
| **Idle glasses** | `HATCH  HOLD F  OPEN` / `SHAFT  HOLD F  RIDE` — thin white mono, L-leader |
| **Holding** | `HOLD F  OPEN  42%` (same `HOLD F  VERB  N%` language as stabilize) |
| **Hold-O** | `EXTRACT  OPEN` / `CLOSED` / `SHAFT` — elbow card, **no popup** |
| **Draw** | Open-well rings + ride cage on existing Augury extra-solids path |
| **F steal** | Stabilize / dummy / stim / corpse / loot still steal **F**. Tap-F pickup still wins. Downed cancels a ride (no float) |
| **Plots** | Yard pad `-24/-24` · `18/-28` · `-28/16` + shaft `18/-12` |
| **Still ~** | Timed surface kill / extract loot loop |

| Dial | Value | Notes |
|------|-------|-------|
| `HOLD_SECS` | **1.15** | Commit toggle / ride. Same glasses language as stabilize (`STABILIZE_HOLD_SECS` **1.45**) |
| `COOL_SECS` | **0.55** | Extra wait after release |
| `must_release` | **true after commit** | Opposite action cannot start until **F** is released |
| `RIDE_SECS` | **1.40** | Surface ↔ cap lerp (smoothstep). Snap to dest so we do not undershoot and re-arm |
| `SHAFT_CAP_Y` | **16.65** | Authored cap top (`+16.4` box + half 0.25) |
| `CAP_LIP_X` | **1.95** | Between tower half **1.6** and cap half **2.2** — standable, not inside collide |
| `EXIT_PAD_X` | **2.65** | Outside shaft interact half **1.9** so ride-down cannot re-arm |
| `CAP_KEEP_M` | **2.05** | Walk off the lid = free EXIT (no hold) |

| Seat | Owns |
|------|------|
| **The Augury** | HatchBoard + shaft ride + glasses chrome (#115) |
| **Range Tech** | Hold-O intent flag (#78) — **not** this PR |
| **Hypha** | World solids / remesh — **not** this PR |

Do **not** claim timed surface kill / extract loot loop shipped. Do **not** invent bloom / god-rays or Range / Hypha / Lab-Rat work as this PR. Door / extract cancel chrome **later landed #120**.

See `PEEK_FINDINGS.md` Closed by #115 + `AESTHETIC_DIEGETIC_LOCK.md`.

## Augury door/extract cancel chrome (landed #120)

Evan lock. **Shipped** [fulcrumRust #120](https://github.com/initialvisuals/fulcrumRust/pull/120) (2026-09-09, `77f0cd67` / `4aaf40a` / `3db2e7e`; merge tip `089e0ad0`). **The Augury** owns cancellable door / extract countdown chrome on the #85 elbows. Same HOLD % language as hatch #115. Walk away / leave volume cancels. Stay commits. Timed surface kill / extract loot loop still **~**. Esc/alt-tab pause + shared-instance handshake **later landed #122** (Beabim; leftover = `GATE_SECS` **2.20**; glasses stay this PR). In-repo dial sheet: fulcrumRust `docs/GATE_DIAL_SHEET.md`.

| Peek | Lock |
|------|------|
| **Door** | **F** edge arms `DOOR  DEPLOY  N%`. Walk-into-door still does **not** auto-deploy (#51). Not instant deploy |
| **Extract** | **OPEN** quiet hatch presence arms `EXTRACT  N%`. Hold-**F** still toggles OPEN/CLOSED. Shaft is a ride, not extract-out |
| **Cancel** | Leave volume. Hold-**F** close / ride also drops the count |
| **Commit door** | Still in volume → `begin_deploy` → extract |
| **Commit extract** | Still in volume → Hypha `extract_transfer_to_stash` stub, then hideout. Kit stays |
| **Hold-O** | Still intent only (`OPEN` / `CLOSED` / `SHAFT`) — countdown wins while armed |
| **Glasses** | Analysis-core white mono (not gold). Idle `DOOR  F  DEPLOY`; armed `DOOR  DEPLOY  N%` · `EXTRACT  N%` |
| **`GateSignal`** | Local leftover. Arm / frac for Beabim. No new KIND. Handshake / Esc-pause **later landed #122** |
| **Still ~** | Timed surface kill / extract loot loop |

| Dial | Value | Notes |
|------|-------|-------|
| `GATE_SECS` | **2.20** | Stay in door / OPEN hatch volume to commit |
| `COOL_SECS` | **0.55** | After cancel, do not immediately re-arm (same cool-off fairness as hatch #115 / house-docs #78) |

#115 hatch HOLD/RIDE dials stay intact (`HOLD_SECS` **1.15** · hatch `COOL_SECS` **0.55** · `must_release` · `RIDE_SECS` **1.40** · `SHAFT_CAP_Y` **16.65** · `CAP_LIP_X` **1.95** · `EXIT_PAD_X` **2.65** · `CAP_KEEP_M` **2.05`).

| Seat | Owns |
|------|------|
| **The Augury** | GateBoard + door / extract cancel chrome (#120) |
| **Range Tech** | Hold-O intent flag (#78) — **not** this PR |
| **Hypha** | `extract_transfer_to_stash` stub on extract-out commit — PreferredHand guts **not** this PR |
| **Beabim** | Handshake / Esc-pause — **later landed #122**. Glasses stay Augury |

Do **not** claim timed surface kill / extract loot loop shipped. Beabim pause/handshake **later landed #122**. Do **not** claim Hypha PreferredHand guts as this PR.

See `PEEK_FINDINGS.md` Closed by #120 + `AESTHETIC_DIEGETIC_LOCK.md` + fulcrumRust `docs/GATE_DIAL_SHEET.md`.

## HDRI sun black-out / blow-out (landed #87)

Evan lock. **Shipped** [fulcrumRust #87](https://github.com/initialvisuals/fulcrumRust/pull/87) (2026-09-09, `5f2577d6`). **Range Tech + Hypha** on the #86 dump base. Softens the Goegap plate solar region + procedural disc so the sun is a disc, not a crushed hole or a white spec. Same ToD sample still lights dome + plate — **no second sky**. Ledger: HDRI sun **·→X**.

| Path | was (#86) | now (#87) |
|------|-----------|-----------|
| plate tone | Reinhard w=1 × 0.20 everywhere (~0.21 hole) | sky keeps grimdark Reinhard × **0.20**; solar texels white-point **8 × 0.55**; knee-compress so bilinear / f16 cannot spike Inf |
| disc | `pow(dot, 1400)` × 1.8 × `(1 − hdri×0.55)` needle | dump **sunSize 0.62** → `mix(1800, 80)`; HDRI live complements disc **0.55 / 0.18** |
| after exposure | hard clip / white spec | local shoulder: core ~(0.12, 0.95); asymptote **0.95** + clamp **0.96** |

| Dump key | Value | This PR |
|----------|--------|---------|
| fogNear / fogFar | **375 / 520** | unchanged (#86) |
| lightKeyMul | **2.11** | unchanged (other light*Mul stay) |
| exposureMul | **1.44** | unchanged |
| clouds | **0.63** | unchanged |
| sunPunch | **0.51** | unchanged |
| sunSize | **0.62** | **was** parked / `pow(1400)` needle → **now** disc/halo softness |
| skyHdri | **true** | unchanged; **/** still toggles |
| camNear / camFar | **0.05 / 2000** | unchanged |

| Dial | Lock |
|------|------|
| **Not a second sky** | Same ToD sample lights dome + plate |
| **bloom / godRays** | still **no path** |
| **brightness / gamma** | still **no path** |
| **Smoke** | `gfx=fog/375/520 cam=0.05/2000 clouds=0.63 punch=0.51 size=0.62` |

| Seat | Owns |
|------|------|
| **Range Tech + Hypha** | HDRI sun disc / plate solar-region tone (#87) |
| **Hypha** | Options Graphics / sky / post defaults (#86) — dump fog / cam / punch stay |
| **Range Tech** | Heat / binds / ballistics / Audio DEVICE — **not** this PR |
| **Augury** | Chrome — **not** this PR |

Do **not** invent bloom / god-rays or a second sky. Do **not** claim Range heat / Augury chrome / Lab-Rat stamps as this PR.

See `PEEK_FINDINGS.md` Closed by #87 + `AESTHETIC_DIEGETIC_LOCK.md`.

## Two-instance pose sync + HOLD JOIN (Beabim — landed #83)

Evan lock. **Shipped** [fulcrumRust #83](https://github.com/initialvisuals/fulcrumRust/pull/83) (2026-09-09, `24eaca4b`). Seat: **Beabim** owns this MP slice (listen-server / two-instance sync / join panel / live-profile loot trail / world-sim leftover / no-pause / shared instance). Hypha #34 stays the UDP hub / HELLO/WELCOME / **Y**-host / `--join` foundation. Flips handshake-only + "no in-game text field" + parked peer pos.

| Dial | Lock |
|------|------|
| **POSE** | UDP after HELLO/WELCOME (~20 Hz): feet `xyz`, yaw, pitch, grounded, crouch. Host assigns peer ids on WELCOME and relays. **#91** adds muzzle `xyz` + gun yaw/pitch |
| **Silhouette** | Cheap **5-box** operator (slate) — not Mixamo / not Locus. **#91** 3-box gun stub — **partial** 1P ≠ 3P; full kit honesty still open |
| **Grounded Y** | Rides **#81 19×19 heightfield** (Range #79 snap DNA). Packet Y ignored when grounded — no phantom `y=0` slab, no floating on a lie. Airborne hops keep networked Y. Dummy + grounded silhouettes plant via Hypha #88 `biped::plant_simple_root` (same column; packet / handshake / HOLD join stay #83). **#91** gun Y rides the same snap |
| **Stream anchors** | #81 `stream_anchors` returns remote feet so the **9×9** window can follow a peer (coordinate only — no Transvoxel rewrite) |
| **HOLD JOIN** | Esc → **JOIN** → type `fulcrum://ip:port` / `fw://` / bare `ip:port` / `localhost` → Enter. No app restart. Title **JOIN** without `--join` opens the same sheet. `--join` / `FULCRUM_JOIN` still one-click. **#91** leftover INVITE + `fulcrum.invite` seeds the field |
| **Port** | Default **7777** (`FULCRUM_PORT` override) |
| **Glasses** | Still `HOST` / `JOIN` / `PEER` labels only — never a second ammo HUD. **#91** glasses `HOST  fulcrum://ip:port` |
| **Binds** | **Y** host (alive; #91 re-copy while hosting) · **I** stim · hold-**O** extract untouched |
| **Loot trail** | **#102** KIND_LOOT on the #91 leftover — host-relayed Z/F by `InstanceId`; hairline `{NAME} DROP/TAKE KIT` |
| **World/sim leftover** | **#119** KIND_SHOT / KIND_LOCUS / KIND_BODY on the #83/#91/#102 leftover — host-relayed shot + death bag; host leftover Locus ~10 Hz |
| **No-pause + KIND_RAID** | **#122** Esc HOLD / Options / JOIN mute the local pawn only; raid keeps ticking; leftover = `GATE_SECS` **2.20**; honors `Cancelled`; glasses stay Augury |

**Still local (deliberately):** HoB / heat / brass / land feel / H tilt (#84) / audio device (#82) / Graphics dump (#86) / HDRI sun (#87) / Locus brain tick on the joiner + yard stamps / COL / deform / scatter / Transvoxel rewrite / Augury elbow / hatch UX (#85) / world seed / ToD / drops (**later landed #102** kit trail) / shoot + Locus leftover + death bag (**later landed #119**). **No** full world replication / PvEvP sim / Mixamo player body.

See `PEEK_FINDINGS.md` Closed by #83. Invite leftover / names / gun stub: Closed by #91. Loot trail: Closed by #102. World/sim leftover: Closed by #119. No-pause + KIND_RAID: Closed by #122.

## Invite leftover + peer names + gun pose (Beabim — landed #91)

Evan lock. **Shipped** [fulcrumRust #91](https://github.com/initialvisuals/fulcrumRust/pull/91) (2026-09-09, `c4d75c11`). Seat: **Beabim** owns this MP slice (listen-server / invite / pose / loot trail / world-sim leftover). Hypha #34 + Beabim #83 stay the UDP hub / HELLO/WELCOME / **Y**-host / HOLD JOIN / `stream_anchors` foundation. Flips leftover invite typing + unnamed peers + gunless 5-box.

| Dial | Lock |
|------|------|
| **INVITE leftover** | Title **HOST** (and `--host` / Deploy) binds listen, then opens leftover **INVITE** sheet (same JOIN analysis-core chrome). Pause while hosting: **INVITE** (same list seat as JOIN). Enter copies |
| **Glasses** | `HOST  fulcrum://ip:port` — still labels only, never a second ammo HUD |
| **Y re-copy** | **Y** while hosting re-copies the invite |
| **fulcrum.invite** | File leftover (LAN + LOOP `127.0.0.1`) so second-instance JOIN seeds without memorizing IP. OS clipboard best-effort (`clip` / `pbcopy` / `wl-copy` / `xclip`) — file always works |
| **JOIN accept** | Title JOIN / HOLD JOIN still accept `fulcrum://` / `fw://` / bare `ip:port` / `localhost` |
| **Peer names** | HELLO + NAME after WELCOME. `FULCRUM_NAME` if set, else **HOST** / **P{id}**. Fade-in white mono over remote head (hairline only). Does **not** steal Augury elbow cards |
| **POSE** | Same UDP ~20 Hz now carries feet + look + **muzzle xyz + gun yaw/pitch** |
| **Gun stub** | Remote 5-box slate operator gets a 3-box gun stub on the networked muzzle (`reconstructed_gun`) |
| **Plant** | Grounded feet consume Hypha #88 `plant_simple_root` on the #81 heightfield (coordinate only — no foot-plant / Transvoxel rewrite). Gun Y rides the same snap |
| **1P ≠ 3P** | **Partial.** Peer gun is a biped hip stub. Does **not** publish 1P `muzzle_world()` — no #94/#98/#99 hip / low-hip / artistic cant on the remote operator. Do **not** claim Mixamo / full 3P kit honesty |

**Still local (deliberately):** HoB / heat / brass · Range #89 CE projectiles · Range #113 handling · #94/#98/#99 1P hip · #97 AIM TUNE · Lab-Rat #80 stamps / COL / deform / scatter / UV **later landed #101** · Hypha #88 foot-plant rewrite / Transvoxel / pixellation · Augury elbow / hatch UX (#85) · PreferredHand / new-profile onboard **later landed #116** · live-profile loot trail **later landed #102** · shoot / Locus leftover / death bag **later landed #119** · Clerk Patch A ledger restamp.

See `PEEK_FINDINGS.md` Closed by #91. Loot trail: Closed by #102. World/sim leftover: Closed by #119. No-pause + KIND_RAID: Closed by #122.

## Live-profile loot trail (Beabim — landed #102)

Evan lock. **Shipped** [fulcrumRust #102](https://github.com/initialvisuals/fulcrumRust/pull/102) (2026-09-09, `6fc0d5d6`). Seat: **Beabim** owns this MP slice (listen-server / invite / pose / live-profile loot trail / world-sim leftover). Hypha #34 + Beabim #83 / #91 stay the UDP hub / HELLO/WELCOME / **Y**-host / HOLD JOIN / INVITE leftover / names / gun stub foundation. Flips local-only Z/F after two-instance pose. World/sim leftover **later landed #119**.

| Dial | Lock |
|------|------|
| **KIND_LOOT** | On the #91 UDP leftover. Host relays; both sides apply drop/take by `InstanceId` |
| **Crumbs** | Hairline `{NAME} DROP/TAKE KIT` via `plan_name_tag` (thin white mono). `FULCRUM_NAME` / HOST / P{id} from #91. **Not** Augury EXTRACT / hatch elbows |
| **Host Z** | Other instance sees the loose kit + `HOST DROP …` |
| **Other F** | Host loses that id + `P1 TAKE …` |
| **Starting kits** | Local (each instance keeps minted loadout). Swap is DROP then TAKE |
| **Pose / gun stub** | #91 unchanged (biped hip, **1P ≠ 3P** partial) |
| **Solo** | `net=off` unchanged — no trail chrome |

**Still local (deliberately):** HoB / heat / brass / Range #89 / #113 handling · shoot / Locus leftover / death bag **later landed #119** · 1P hip / low-hip / cant / AIM TUNE / #103 live-save · Lab-Rat stamps / UV **later landed #101** · Augury hatch / EXTRACT elbows · PreferredHand **later landed #116** · full live-profile stash · mid-air drop bounce (remote sees settled rest) · knife-rally / joiner slash / stabilize dummy (`NO NET`)

See `PEEK_FINDINGS.md` Closed by #102. World/sim leftover: Closed by #119. No-pause + KIND_RAID: Closed by #122.

## World/sim leftover — shoot / Locus / bodies (Beabim — landed #119)

Evan lock. **Shipped** [fulcrumRust #119](https://github.com/initialvisuals/fulcrumRust/pull/119) (2026-09-09, `6562070e726c0ae69719598bdc294a1f51d2e37e`). Seat: **Beabim** owns this MP slice (listen-server / invite / pose / loot trail / world-sim leftover). Hypha #34 + Beabim #83 / #91 / #102 stay the UDP hub / HELLO/WELCOME / **Y**-host / HOLD JOIN / INVITE leftover / names / gun stub / KIND_LOOT foundation. Flips local-only shoot / Locus / bodies after two-instance pose + loot trail.

| Dial | Lock |
|------|------|
| **KIND_SHOT** | Host-relayed on the #83/#91/#102 UDP leftover (`HYPH` magic). Peer sees tracer + fire FX from **biped hip + look dir** (`reconstructed_gun`) |
| **1P ≠ 3P** | Peer shot muzzle does **not** publish 1P `muzzle_world()` — house lock held. Hip stub, not 1P cant |
| **KIND_LOCUS** | ~10 Hz host leftover: slot + pos + yaw + HP + brain + ragdoll flop. HELLO dumps current yard. Joined peer **plants soles only** — does **not** tick a second Locus brain |
| **Hunt** | Host hunts the nearest operator (local + remotes). Joined deploy does not mint a second yard |
| **KIND_BODY** | Death-bag drop/reclaim (host-relayed, one shared bag) |
| **Two-instance** | Share shoot events, Locus presence/ragdoll, and the death bag — not just pose + loot. Hairline leftover only — no new glasses chrome |
| **Solo** | `net=off` unchanged |

**Still local (deliberately):** Range feel / HoB / heat / brass / 1P hip / AIM TUNE (#113 handling etc.) · knife-rally HP · Locus slash HP on the joiner (host wound only if the hunted operator is the host) · teammate stabilize dummy (`NO NET`) · timed surface kill · death cam · stamps / Transvoxel / hatch elbows · PreferredHand **later landed #116** (local profile; no Beabim net sync) · full PvEvP / dedicated infra

See `PEEK_FINDINGS.md` Closed by #119. No-pause + KIND_RAID: Closed by #122.

## No-pause live sim + shared extract handshake (Beabim — landed #122)

Evan lock. **Shipped** [fulcrumRust #122](https://github.com/initialvisuals/fulcrumRust/pull/122) (2026-09-09, merge tip `cbb26d8796faa9e476e8695fb4b118486d1759b3`). Seat: **Beabim** owns this MP slice (listen-server / invite / pose / loot trail / world-sim leftover / no-pause / shared instance). Hypha #34 + Beabim #83 / #91 / #102 / #119 stay the UDP hub / HELLO/WELCOME / **Y**-host / HOLD JOIN / INVITE leftover / names / gun stub / KIND_LOOT / KIND_SHOT / KIND_LOCUS / KIND_BODY foundation. Augury #120 still owns glasses HOLD % / `GATE_SECS` **2.20** / `COOL_SECS` **0.55**. Flips frozen-raid Esc / alt-tab + local-only door **F** after two-instance pose + world/sim leftover. In-repo dial sheet: fulcrumRust `docs/GATE_DIAL_SHEET.md` KIND_RAID row — do **not** steal Augury glasses dials.

| Dial | Lock |
|------|------|
| **No-pause** | Esc HOLD / Options / JOIN chrome **mutes the local pawn only**. Raid keeps ticking (pose / shots / Locus leftover) |
| **Focus loss** | Alt-tab / unfocus releases grab — **does not HOLD or freeze** (no bullet bulk catch-up) |
| **HOLD chrome** | Augury HOLD list / "SYSTEM PAUSED" **not restyled** |
| **KIND_RAID leftover** | Host-authoritative. Timer = Augury `GATE_SECS` **2.20** (house-docs #80 / fulcrumRust #120). Honors `GateEvent::Cancelled` / leave-volume |
| **Arm** | Door **F** / OPEN quiet hatch presence arm the #120 glasses countdown; host then commits both peers to the same raid id + host seed (dest extract or hideout) |
| **Cancel** | Augury leave-volume / `Cancelled` → KIND_RAID CANCEL. Inventory / death soft-cancel too. No forced transition. Cool-off stays Augury **0.55** |
| **Glasses** | `DOOR  DEPLOY  N%` / `EXTRACT  N%` stay Augury #120 — **not rewritten** |
| **Solo `net=off`** | Uses the #120 countdown (stay commits, walk away cancels). No invented handshake / raid id / trail |
| **1P ≠ 3P** | Held. #91 hip stub + #119 hip-stub shot muzzle unchanged |

**Still local (deliberately):** Range feel / HoB / heat / brass / 1P hip / AIM TUNE · knife-rally / joiner slash / stabilize dummy · stamps / Transvoxel hitch / PreferredHand · Lab-Rat stamps · Augury glasses HOLD % / hatch art / timed surface kill · full PvEvP / dedicated infra

See `PEEK_FINDINGS.md` Closed by #122 + fulcrumRust `docs/GATE_DIAL_SHEET.md` KIND_RAID row.

## Biped foot plant / terrain follow (Hypha — landed #88)

Evan lock. **Shipped** [fulcrumRust #88](https://github.com/initialvisuals/fulcrumRust/pull/88) (2026-09-09, `78e11990`). Seat: **Hypha** owns plant / ride / Mixamo host hooks. Steals the Range #79 heightfield column — **not** a mesher rewrite. Augury brains stay. Beabim #83 packet / handshake / HOLD join stay.

| Dial | Lock |
|------|------|
| **root Y** | Heightfield column — pelvis + each boot, mean of feet. `World::surface_height` → `TerrainHost::height_at` + `support_surface_y` |
| **FOLLOW** | **8.5** 1/s — Mycelium `IK_BLEND_RATE` 8, quieter for boxes |
| **DEADZONE** | **0.04** m — ignore micro hunt |
| **RISE_RATE** | **2.2** m/s — climb without popping through mesh |
| **SINK_RATE** | **6.5** m/s — catch the column — no midair hang |
| **SNAP_ERR** | **1.15** m — first plant snaps; later only a large *down* error snaps |
| **LIFT_MAX** | **0.14** m — per-boot slope offset; no FBIK |
| **BOOT_HALF_H** | center **0.11** m — sole on root Y (was center 0.18) |
| **Locus** | `step` no longer writes `pos.y = 0`. Extract `tick_on` + heightfield; hideout / unit tests keep flat-floor `tick` |
| **Dummy + #83 peers** | `biped::plant_simple_root` (same column). Packet / handshake / HOLD join stay #83 |
| **Mixamo sockets** | Pelvis / Foot_L / Foot_R / Head + planted `BipedRoot` — host hooks only. Form-check solids for tests — not a second yard enemy, not GPU skin, not Augury brains |
| **STEAL_MAP** | Biped **todo → partial** (plant + host hooks). Mixamo clips / player body / 2-bone IK / GPU skin still parked |
| **A-notes** | `[·] enemies walk into terrain` → **X** |

Do **not** claim Mixamo clip import / GPU skin / player body / 2-bone IK / mesher rewrite. Range shoot/feel/heat/binds · Lab-Rat #80 plugs · Beabim #83 net rewrite · HDRI sun stay out.

See `PEEK_FINDINGS.md` Closed by #88.

## Kit metal/grit PBR stub (landed #64)

Range Tech. Store `dBXpg` greeble pack was **not** on the shelf — still **open**/missing. Used what was: brand/TRIMSHEET_MICRO (+ grey); atelier textures/PBR MetalPanelRectangular / MetalCorroded (256² crops); handful of scratch / fingerprint roughness masks from the 150-roughness pack. Boxes stay color-only (stub PBR): albedo mix + roughness/mask on MP9-Z / SR-25 / M24. House DNA: **gold+black tech trim** hairlines, not gold-plate, not Locus veins. Crops vendored in fulcrumRust `assets/kit/`. Atelier read-only (`FULCRUM_KIT` / `FULCRUM_ATELIER`). Do **not** claim full metal-tech / `dBXpg` kits shipped — only this stub. See `AESTHETIC_DIEGETIC_LOCK.md`.

## Still soft / seat-owned timing
- **Scope glass** (when LPVO) — **holding / not shipped** (Evan 2026-09-09). Greyscale / B&W ramp (**not** color); fake curve + thickness (Blender-style cut/flatten); IOR + ramp-driven magnify; bodycam optic **no PiP** (glass/radial/reflect in the scope pass). Hypha Graphics when LPVO; Range AIM TUNE placements first (#97). Live **V** iron/holo/acog stay. Do **not** claim LPVO or glass shipped
- **Evan asset-ask path** — **holding / locked intent** (Evan 2026-09-09). Clone CE / aim-offset attachment tables first; missing → ask Evan (this week to model + texture); primitives stay scaffolding. Style grows with peeks (void-spore + grit floor). Lab-Rat keeps procedural grit until the asset list, then bake onto authored. Do **not** invent a replacement pack
- **1P viewmodel ≠ 3P biped gun** (MP honesty) — **partial shipped #91** (Evan 2026-09-09). Peer biped hip gun stub landed; full 3P kit honesty / hands / gear sync still open. Range Tech owns 1P dials / AIM TUNE; Beabim owns the 3P path; Lab-Rat stamps stay out. Artistic 1P posing may stay aggressive; peers must not see guns through eyeballs. Do **not** claim Mixamo / full 3P kit honesty. HANDS later
- Exact day-one world: single medium instance vs hub+tunnel+extract (Hypha chooses if Evan didn’t hard-pick)
- Near LOD raise **shipped #61** (then subdivs **32/16/4**). Live underfoot **#81 32/16/8/4**. Stamp pad stays Hypha #43 **7×7**. Stream hitch amortize **landed #108** (cook=1/2 · prefetch=5 m · splash-pumped load-in). **#114** is a shallow enterable pad network (not those parked cutouts). Live octree / unconstrained Sync dump / residual soft LOD pop / full tunnel cutouts / runtime carve / live voxel collide / Transvoxel rewrite still parked. Beabim peer feet `stream_anchors` **landed #83** (coordinate only)
- First big-map host **landed #81**. Live walk is **19×19 / 304 m / 92 416 m²** + **9×9** stream. Stream hitch amortize **landed #108** on that same 9×9. Stamp pad still **7×7**. Slope COL tint default; NRM/GLOSS parked. Lab-Rat slope/PBR/dirt/scatter/deform plugs **landed #80** (DISP bake-down + deform/scatter filled). Blender UV dials **landed #101** (texture tiles only — never geo). Hypha Transvoxel UV consume **landed #112** (`promote_for_uv` + wear/COL honor). Beabim peer feet follow remotes **#83**. Continues on fulcrumRust
- Biped foot plant **landed #88**. FOLLOW **8.5** / DEADZONE **0.04** / RISE **2.2** / SINK **6.5** / SNAP_ERR **1.15** / LIFT_MAX **0.14** / BOOT_HALF_H center **0.11**. STEAL_MAP biped **partial** (plant + host hooks). Mixamo clips / player body / 2-bone IK / GPU skin still parked. Mesher untouched
- Menus / settings: Augury title+HOLD chrome + Options shell shipped #45; Hypha Graphics/Gameplay/Controls + window + persist shipped #46; GPU post stack shipped **#55** (AO/AA/CA/grain/DoF; smoke `post=aa`; not full bloom/god-ray); **colorless muzzle heat landed #66** (sample-only UV warp; no new Graphics sliders); **pixellation / WARP landed #90** (`warp_strength` default **0.01**; Options **WARP** after CAM FAR; `GFX_LEN` 12→13; mix toward CE PIXEL SCALE **2**; `pixel_warp_uv` after `heat_warp_uv`; persist `{:.2}` → `0.01`; smoke ` warp=0.01` only; Augury aesthetic only); **ADS viewmodel DoF landed #68** (ADS near + far on the same Options **DOF**); **heat dial blend landed #71** (Range Tech; dump-dial cooking/~ → landed/X; #66 path stays); **Options Audio DEVICE landed #82** (SYSTEM DEFAULT; cycle DNA = Graphics WINDOW; persist `output_device`; thin cpal voice — not a second mixer); **Graphics dump landed #86** (thin Options **FOG / FOG NEAR / FOG FAR / CAM NEAR / CAM FAR** + persist; fog **375 / 520** · cam **0.05 / 2000** · clouds **0.63** · sunPunch **0.51** · light*Mul **0.11 / 0.41 / 0.61 / 2.11 / 1.65 / 1.06** · exp **1.44** · skyHdri on; hideout `haze_max` **0**; bloom / godRays / brightness / gamma **no path**); **HDRI sun disc landed #87** (dump **sunSize 0.62** rides the disc)
- One-click Windows `build.bat` **landed as Hypha #42 + Range Tech #48** (always pause + `build.log` tee); quality/flag options still cooking / open (Lab-Rat mirror for pycelium later — no dials invented here)
- Embodied feel pass: Range Tech medium dials **landed #57** (look inertia queue **26**; ADS **0.86** / **6.4**; sprint high-ready **6.2**; slide **10.3 / 0.98 / 1.02**; land punch then **0.052** rad overlay — **#79** live punch **0.028** + inertia sway; AXIS_LOCK stay; no materials / range geo). U-cycle `hold_spring` **7.0** **later landed #109** — ADS `blend_speed` **6.4** stays its own dial; **#113** scales it by kit ergo (not a fixed stub)

- Evan peek feel **landed #59**: H viewmodel crossover (hip +X ~0.24 → partial left ~−0.041 X / ~−0.181 Y, cap `shoulder_x_min` −0.055; ADS **0.32**; **#94** slight straighten pitch/yaw/roll **0.04 / 0.10 / 0.08**, supersedes #84 chest-cross 0.08/0.32/0.39 — not a mesh mirror); lean flip + deepen (**Q = peek right** / **E = peek left**; depth **0.5 / 0.5**); CE hop + air hop (`JUMP_FORCE` **12** / `|GRAVITY|` **30** / one air hop **unchanged**); **#79** land softener punch **0.028** · duck **0.08 m** · shake **0.14** gate **13** + inertia sway; heat motion v77 shimmer stays Range Tech spatial input / `barrel_energy` / hold-J; **live tell is Hypha colorless post UV warp landed #66** (lattice = post input only; no world-pipeline orange card); tracers live until impact + FX `hit`. Day-one handmade SFX vendor **landed #62**. **Patch A muzzle landed #67** — kit-tip spawn (`muzzle_tip_local`) + `hip_honest_dir` + tip→impact streak clamp. **−/=** zero + #59 tracers-until-impact stay; **P** unused (#76); **O** is hold extract intent (#78). #67 did **not** fight #66 and did **not** ship heat color. **ADS viewmodel DoF landed #68** — ADS near + far on the same #55 pass / same Options **DOF** (radius **0.0048**; taps **12**; near fade 0.90→2.20 m; breath mul **1.6 parked**). #68 did **not** ship heat color (live tell is Hypha #66). **Heat dial blend landed #71** — dump-dial cooking/~ → landed/X; live defaults sit between old bake and the dump (haze **0.07** / size **0.83** / scaleX **0.396** / lobe **0.698**); #66 colorless path stays; no orange card redraw. **SIM-only launch landed #76** — one HoB + gravity / zero model; arcade aim-dir dead; leftover `hob_zero` ignored; **P** unused; **−/=** 50/100/200 (#78); #67 hip honesty on the single SIM model. **Hold-O extract / −/= zero / grounded slide landed #78** — raid `Session::extract_checking`; **O** is **not** zero; Augury EXTRACT elbow card **landed #85** (no popup); hatch toggle + shaft ride **landed #115**; door / extract cancel chrome **landed #120**; timed surface kill still **~**; midair Shift+Ctrl cannot float-slide. **Land sway softener + heightfield FX landed #79** — same #59 hop overlay (**not** a second land system); punch **0.028** / duck **0.08** / shake **0.14** gate **13** + sway eye/yaw/roll + decay **4.6**; brass / tracers / marks snap to extract heightfield / wall support; `first_hit` walls-only; AXIS_LOCK +Z unchanged. Lab-Rat terrain untouched. Music playlist beds **landed #64**. Kit metal/grit PBR stub **landed #64**. Store `dBXpg` still **open**. First big-map host **landed #81**. **Options Audio DEVICE landed #82** — SYSTEM DEFAULT; A/D or arrows / Enter / click (Graphics WINDOW DNA); persist `output_device` (empty / `default` / `system` = OS default); missing pin kept, playback falls back to OS default; same #21 mixer → thin cpal voice; UI tick on the new pick. **H shoulder-swap tilt landed #84** — tilt path; live left hold **#94** slight straighten pitch/yaw/roll **0.04 / 0.10 / 0.08** (supersedes #84 chest-cross 0.08/0.32/0.39); travel dest ~−0.041 X / ~−0.181 Y / cap **−0.055** / ads_keep **0.32**; not a capsule/eye slide, not a mesh mirror, no `scale.x = −1`. PreferredHand / new-profile onboard **later landed #116**. **Patch A RH hip bias landed #94** — first +0.08; live hip **superseded #98**; ADS X / tip spawn / `hip_honest_dir` / #89 tracers stay. **Aim-offset tuner + attachment sockets landed #97** — live **End** sheet on existing ViewmodelDials + kit_mesh optic/can sockets (Insert WEAPON↔ATTACH · PageDown target · PageUp MICRO/FINE/MED/COARSE · Delete JSON; glasses `AIM TUNE`); Home debugger **later landed #110**; authored defaults now **#98**; not Home chrome at #97, not hitch logger at #97, not EffectComposer, not a second pose system. **AIM TUNE LIVE persist landed #103** — End LIVE flush → Hypha `project.json` (`aim_live` default **true**; `aim_tune.example_smg` / `example_rifle` / `example_sniper`; pose `{x,y,z,rotX,rotY,rotZ}`; attach optic/can; load on Deploy; partial merge keeps #98/#99/#100); #97 End / Delete dump stay; End stays AIM TUNE; RECORD stub — no bind. **CE Home debugger landed #110** — **Home** toggle · LOGS / TELE / CHEAT · hitch WARN/HITCH · glasses `DEBUG`; shares `project.json` `debugger_tab` with Range `aim_live` / `aim_tune`; hitch *visibility* only; hitch *fix* **later landed #108** — not CE heartbeat flags / End tuner changes. **Home LOGS COPY + tracker toggles landed #121** — **Enter** COPY · ring **800** · timestamps · Insert/Delete tracks · `log_*` persist default on · medium edge events · TELE max ms stays when tracks off. **Stream hitch amortize landed #108** — cook=1/2 · prefetch=5 m · splash-pumped load-in on the #81 9×9; emits `STREAM` / `BAKE` into #110; residual soft LOD pop / live octree parked. **RH hip one more body-width + ready-hip Y landed #98** — MP9-Z hip **0.2403 / −0.2128 / −0.1833**; `shoulder_cross_x` **−0.281** / `shoulder_cross_y` **0.032**; no mesh flip. **Low-hip shotgun stance landed #99** — MP9-Z `hip_low` **0.2403 / −0.3528 / −0.1513** / pitch **0.145** (gap **0.140** vs ready **−0.2128**); SR-25 **−0.364 / −0.176 / 0.148**; M24 **−0.369 / −0.196 / 0.146**; U-cycle glasses **LOW HIP**; RMB from LowHip = iron ADS (not `ads_cant`); not chin-weld; #97 End tuner still live; ready hip / hip_cant / ADS / H stay #98. **Canted 45° Greyzone CQC ADS landed #100** — MP9-Z `ads_cant` **0.0423 / −0.148 / −0.136** / pitch/yaw/roll **0.024 / 0.11 / 0.785** (roll stays); SR-25 / M24 **0.0468 / −0.154 / −0.148**; U+RMB / hold-Mouse5 @ 60° CQC; glasses **CANT 45** / **CANT ADS**; hip_low stays #99; #97 End tuner still live; not a canted-holo mesh / IOR glass / mesh flip / Beabim / heat / terrain. **U-cycle hold springs landed #109** — `hold_spring` **7.0** (house-medium between ADS `blend_speed` **6.4** and H `shoulder_spring` **8.0**); same exp-approach path; glasses still snap CHEST / LOW HIP / CANT 45; inspect / sprint_high lerp on eased home; first-U seed-before-cycle; 1P only; STEAL_MAP pose-ease → **in**; ADS blend stays its own dial — **#113** scales it by kit ergo. **Kit handling / ergo / MOA landed #113** — `HandlingStats` / `FeelSheet::handling`; ADS `blend_speed` **6.4** × ergo (MP9 **8.00** / SR-25 **6.40** / M24 **5.12**); handling → recoil `1/handling`; hip MOA after `hip_honest_dir`; ADS × **0.22**; `hold_spring` **7.0** stays sibling; not house mastery / gear UI / Beabim 3P / heat / PreferredHand. **Hypha Graphics dump landed #86** — Options FOG / CAM NEAR/FAR + sky / post defaults (fog **375 / 520** · cam **0.05 / 2000** · clouds **0.63** · sunPunch **0.51**); exposure keyboard still unbound after #78; **,** / **.** clouds still work; **/** HDRI toggle stays; do **not** invent bloom / god-ray / brightness / gamma. **HDRI sun disc landed #87** — dump **sunSize 0.62** rides the procedural disc/halo (no longer parked); plate solar-region tone + soft disc; not a second sky. **Pixellation / WARP landed #90** — `warp_strength` **0.01**; Options **WARP** after CAM FAR; mix toward CE PIXEL SCALE **2**; Augury aesthetic only — do not steal into Range. Range heat / binds / ballistics / Audio DEVICE **not touched**. **Biped foot plant landed #88** — heightfield column; FOLLOW **8.5** / DEADZONE **0.04** / RISE **2.2** / SINK **6.5** / SNAP_ERR **1.15** / LIFT_MAX **0.14** / BOOT_HALF_H center **0.11**; Mixamo sockets Pelvis / Foot_L / Foot_R / Head host hooks only; A-notes enemies-walk-into-terrain **X**; STEAL_MAP biped **partial**; Mixamo clips / player body / 2-bone IK / GPU skin parked; mesher untouched. **Projectile feel landed #89** — rect slab + 4–6 debris (0.07–0.17 s) + visualLength **1.5 / 18** + core **2.85 / 2.25 / 0.95** + slug **0.07** + wake 1–2 + hit flash **0.15** s + punch **8–12** (35% white) / scuff **4–6** amber + fire-pulse glyphs on existing `TracerField`; SIM / HoB / gravity **unchanged** (#76); HeatDials **unchanged** (#71); AXIS_LOCK +Z / #79 snap stay; CE tip **0.2.8** preferred if a later cook retunes muzzle-adjacent haze — not a heat-card rewrite, not Beabim, not profile onboard. Shot propagation still later

- Texture compression (2026-09-07): atelier roughness packs are **4k 48-bit PNG** — too large. Do **not** ship raw 4k 48-bit into the yard. Lab-Rat **#58 quiet grit greyscales landed** (vendored 256² bake-downs + `sample_channels` quiet height + `grit::rough` wear — the near source). Hypha LOD-tied mips **shipped #60** on Transvoxel **distance rings** (near 256² / mid 64² / far 16²; far softer). Slope/PBR/dirt/scatter/deform plugs **landed #80**. Blender UV dials **landed #101** (scale/offset/rotate; identity default; `FULCRUM_UV`; Hypha #112 `promote_for_uv` + wear/COL honor; texture-only). Do **not** claim the whole roughness→stamp cook. Near LOD raise **shipped #61**; live underfoot **#81 32/16/8/4**; grit mips stay. First big-map host **landed #81**. See `STAMP_FEEL_LOCK.md` + `TERRAIN_NORTHSTAR.md`
- Atelier: plugs **open** (Evan **clean** yell 2026-09-08 ~00:00 ET). PBR batch **in** (150 roughness + textures/PBR ~26 sets). #58 / #80 `FULCRUM_GRIT=` / `FULCRUM_ATELIER=` stay read-only **load** paths. `FULCRUM_UV` is Lab-Rat tile override, not an atelier write. Lab-Rat slope/PBR/dirt/scatter/deform plugs **landed #80**. Blender UV dials **landed #101**. Hypha Transvoxel UV consume **landed #112**. Further roughness → stamp stays on **fulcrumRust only** — bake-down first; SVG / density-mask / experiment-log still open. Range Tech kit metal/grit PBR stub **landed #64**; store `dBXpg` still **open**. Music playlist beds **landed #64**. Augury FoW brand / menu video **when cut ready**
- **SFX remix DNA** (2026-09-08 ~00:00 ET): creative reuse OK — pitch / speed / effects to mint new one-shots from existing packs; indie underground vibe; don’t overuse the same stem. #62 vendor stays the live FILE_SLOTS fill. First ±6% fire/foot/reload jitter **landed #64**; full remix minting still **open**
- Holocron (Evan gift 2026-09-08): atelier `Holocron_Visualizer.py` + `Analyze-Holocron.ps1` — tree nested-rectangle viewer for file bases. Cut down monoliths (agent context; overwrite loss). Slope/PBR plugs **landed #80**. Lab-Rat rust-friendly rewrite still waits on SVG / density-mask / monolith splits. Later: `channels.rs` / stamp stacks / `feel` / `kit_mesh`. See `TOOLS.md`. Do **not** claim rewrite shipped
- PreferredHand + new-profile onboard — **landed #116** (Hypha owns it). Right default · NEW PROFILE gate · `project.json` permanent vs live · death clears live · extract→stash stub · H seats Range crossover, no mesh flip. **#84** / **#91** / **#94** / **#97** / **#98** / **#99** / **#100** / **#102** / **#103** / **#109** / **#110** / **#113** / **#115** parked it at ship time — do **not** claim those PRs shipped it. Full PMC stash / character tab / world-pool death loot / Beabim net sync of PreferredHand still later
- Augury glasses EXTRACT chrome **landed #85** (elbow card, no popup). CE Home debugger **landed #110**. Home LOGS COPY + tracker toggles **landed #121**. Hatch toggle + shaft ride **landed #115**. Door / extract cancel chrome **landed #120**. Timed surface kill still **open**. Hypha stream hitch *fix* **landed #108**. Residual soft LOD pop / live octree still parked. CE PERF/PHYS/RENDER/heartbeat/combat-log flags — house-docs steal later
- Growth PoCs after window exists
- Shot propagation on the spatial FX path (binaural day-one landed #27; reverb volumes landed #56; file-slot wiring landed #54; handmade vendor landed #62; DEVICE cycle landed #82)
- Authored SFX vs spatial split: Range Tech file-slot **wiring** shipped #54; day-one handmade vendor **landed #62** (small set, not a full pack dump). **SFX remix DNA** first ±6% fire/foot/reload jitter **landed #64**; full remix minting still **open**. Music playlist beds **landed #64**. Options **DEVICE** cycle **landed #82**. Shot propagation still later. Augury (Chamber) keeps spatial/reverb DNA (**volumes shipped #56**); Lab-Rat stamps stay quiet on audio (Initial Visuals Group Chat 2026-09-07)

Source chat: Initial Visuals Group Chat, 2026-09-06. Controller axis lock: fulcrumRust PR #12 (2026-09-07).
MP9-Z kit: fulcrumRust PR #14 (2026-09-07).
Smart stamps: fulcrumRust PR #15 (2026-09-07).
Transvoxel consume channels: fulcrumRust PR #17 (2026-09-07).
Locus Standard AI: fulcrumRust PR #18 (2026-09-07).
World drop/pickup + FX draw dials: fulcrumRust PR #19 (2026-09-07).
Void-spore grimdark + concrete wear: fulcrumRust PR #20 (2026-09-07).
Audio buses Voice / Music / FX: fulcrumRust PR #21 (2026-09-07).
Transvoxel extract host: fulcrumRust PR #16 (2026-09-07).
SR-25 + M24 kit stubs: fulcrumRust PR #22 (2026-09-07).
Distance activation / far-guts cold: fulcrumRust PR #23 (2026-09-07).
Extract day/night clock + procedural sky: fulcrumRust PR #24 (2026-09-07). **−/=** exposure **superseded #78** — keyboard unbound; **−/=** is zero. HDRI sun disc **completed #87**.
Wall-clamped Q/E lean polish: fulcrumRust PR #25 (2026-09-07).
Locus Inked on yard: fulcrumRust PR #26 (2026-09-07).
Day-one binaural / positional stereo on FX: fulcrumRust PR #27 (2026-09-07).
CE reverb volumes (DRY / YARD / OUT, FX wet send): fulcrumRust PR #56 (2026-09-07) — The Augury.
Hold-` inspect pose: fulcrumRust PR #28 (2026-09-07).
Lab-Rat Inked void-spore hotspot: fulcrumRust PR #30 (2026-09-07).
Bandage use stub: fulcrumRust PR #31 (2026-09-07).
Mag reload DNA: fulcrumRust PR #32 (2026-09-07).
Live HoB zero / launch dials: fulcrumRust PR #33 (2026-09-07). Dual-path arcade↔sim **superseded #76** — **P** unused. Zero bind **superseded #78** — **−/=** 50/100/200; **O** is hold extract intent.
Listen-server + invite stub: fulcrumRust PR #34 (2026-09-07). Handshake-only + no in-game join field **superseded #83**. Leftover INVITE + names + gun stub **landed #91**. Loot trail **landed #102**. World/sim leftover **landed #119**. No-pause + KIND_RAID **landed #122**.
Beabim two-instance pose sync + HOLD JOIN (UDP **POSE** ~20 Hz; 5-box slate silhouette; grounded Y rides #81 heightfield; `stream_anchors` follow remotes; Esc → JOIN types invite; port **7777**; **Y** host / **I** stim / hold-**O** extract stay; terrain / audio stay local; shoot / Locus leftover **later landed #119**; no-pause + KIND_RAID **later landed #122**): fulcrumRust PR #83 (2026-09-09) — **landed**. `24eaca4b`. Grounded silhouettes share Hypha #88 `plant_simple_root`. Invite leftover + names + gun stub **later landed #91**. Loot trail **later landed #102**. World/sim leftover **later landed #119**. No-pause + KIND_RAID **later landed #122**. See `PEEK_FINDINGS.md` Closed by #83.
Beabim invite leftover + peer names + gun pose (INVITE sheet after HOST / `--host` / Deploy; pause **INVITE**; Enter copies; glasses `HOST  fulcrum://ip:port`; **Y** while hosting re-copies; file leftover `fulcrum.invite` LAN + LOOP `127.0.0.1`; clipboard best-effort; HELLO + NAME → `FULCRUM_NAME` else **HOST** / **P{id}**; fade-in white mono over remote head; POSE + muzzle `xyz` + gun yaw/pitch; 3-box biped hip gun stub; does **not** publish 1P `muzzle_world()`; loot trail **later landed #102**; world/sim leftover **later landed #119**; no-pause + KIND_RAID **later landed #122**): fulcrumRust PR #91 (2026-09-09) — **landed**. `c4d75c11`. See `PEEK_FINDINGS.md` Closed by #91.
Beabim live-profile loot trail (KIND_LOOT host-relayed Z/F by `InstanceId`; hairline `{NAME} DROP/TAKE KIT` via `plan_name_tag`; `FULCRUM_NAME` / HOST / P{id}; starting kits stay local; swap is DROP then TAKE; solo `net=off` no trail chrome; 1P≠3P held #91; shoot / Locus leftover / death bag **later landed #119**; no-pause + KIND_RAID **later landed #122**): fulcrumRust PR #102 (2026-09-09) — **landed**. `6fc0d5d6`. See `PEEK_FINDINGS.md` Closed by #102.
Beabim world/sim leftover (KIND_SHOT / KIND_LOCUS / KIND_BODY on the #83/#91/#102 UDP leftover `HYPH`; host-relayed shot + death bag; host leftover Locus ~10 Hz slot+pos+yaw+HP+brain+ragdoll; HELLO dumps yard; peer shot muzzle = `reconstructed_gun` + look dir — does **not** publish 1P `muzzle_world()`; joiner plants soles only — no second Locus brain; two-instance share shoot / Locus / death bag; solo `net=off` unchanged; Range feel / HoB / heat / brass / knife-rally / joiner slash / stabilize / stamps / hatch / PreferredHand **later landed #116** (local profile; no Beabim net sync) / full PvEvP stay local; no-pause + KIND_RAID **later landed #122**): fulcrumRust PR #119 (2026-09-09) — **landed**. `6562070e726c0ae69719598bdc294a1f51d2e37e`. See `PEEK_FINDINGS.md` Closed by #119.
Beabim no-pause live sim + KIND_RAID shared extract handshake (Esc HOLD / Options / JOIN mute the local pawn only; raid keeps ticking; focus loss / alt-tab releases grab — does not HOLD or freeze; leftover = Augury `GATE_SECS` **2.20**; honors `Cancelled`; glasses HOLD % stay Augury; solo `net=off` uses the #120 countdown; no invented handshake / raid id / trail; #83/#91/#102/#119 pose/shots/loot/world-sim unchanged; house lock **1P≠3P** held): fulcrumRust PR #122 (2026-09-09) — **landed**. Merge tip `cbb26d8796faa9e476e8695fb4b118486d1759b3`. See `PEEK_FINDINGS.md` Closed by #122 + fulcrumRust `docs/GATE_DIAL_SHEET.md` KIND_RAID row.
Heat-tune dump (hold-J): fulcrumRust PR #35 (2026-09-07).
Down / death stub: fulcrumRust PR #36 (2026-09-07).
Augury I-stim / Y-host bind: fulcrumRust PR #37 (2026-09-07).
Shape-agnostic stamp/paint substrate: fulcrumRust PR #38 (2026-09-07).
Extract-yard scale harness: fulcrumRust PR #39 (2026-09-07).
Quiet grit greyscales (vendored 256² + sample_channels quiet height + grit::rough wear): fulcrumRust PR #58 (2026-09-07) — **landed**. Atelier read-only. Near source for Hypha #60 ring-mips.
Goegap day plate on extract ToD: fulcrumRust PR #40 (2026-09-07). **−/=** exposure **superseded #78**. HDRI sun disc **completed #87**.
FoW title mark on the #11 shell: fulcrumRust PR #41 (2026-09-07).
Windows one-click release builder: fulcrumRust PR #42 (2026-09-07).
Windows builder stay-open + `build.log` tee: fulcrumRust PR #48 (2026-09-07).
Yard expand A/B (wider chunk radius first): clerk lock, Initial Visuals Group Chat (2026-09-07) — **shipped** Hypha #43.
Wider extract chunk radius (7×7 / 3 rings / 112 m / 12 544 m²): fulcrumRust PR #43 (2026-09-07).
Title + HOLD analysis-core polish: fulcrumRust PR #45 (2026-09-07).
Hypha Options Graphics/Gameplay/Controls guts: fulcrumRust PR #46 (2026-09-07). **#86** adds thin FOG / CAM rows on that Graphics pane.
Leftover feel-lab FX (brass / ricochet / impact variety / casing_draw_m): fulcrumRust PR #47 (2026-09-07). Ground snap **superseded #79** — heightfield / wall support; `first_hit` walls-only. Punch/scuff spark counts + hit flash **superseded #89**.
AXIS_LOCK + dizzy-play: fulcrumRust PR #51 (2026-09-07) — see `AXIS_LOCK.md`.
Hypha GPU post stack (AO/AA/CA/grain/DoF): fulcrumRust PR #55 (2026-09-07). **#66** colorless muzzle heat and **#68** ADS near sit on the same pass / same Options **DOF**.
Menus / settings ownership: Evan dump (2026-09-07) — Augury shell shipped #45; Hypha guts shipped #46; GPU post stack shipped #55; colorless heat shipped #66; ADS near DoF shipped #68; Graphics dump shipped #86.
Embodied feel pass (aim-offset × CE/FoW medium dials, Range Tech): fulcrumRust PR #57 (2026-09-07) — **landed**. U-cycle `hold_spring` **7.0** **later landed #109** (ADS `blend_speed` **6.4** stays its own dial — **#113** scales it by kit ergo).
Evan peek feel (lean flip + deepen, CE hop + air hop, heat v77 look, H crossover, tracers-until-impact + FX `hit`): fulcrumRust PR #59 (2026-09-07) — **landed**. H tilt path **superseded #84**. Live hip / left hold **superseded #94** / **#98**. See `PEEK_FINDINGS.md` Closed by #59.
Hypha colorless muzzle heat (sample-only `heat_warp_uv`; lattice = post input only; no world-pipeline orange card): fulcrumRust PR #66 (2026-09-08) — **landed**. Range Tech keeps `barrel_energy` / heat dials / hold-J. Live defaults are the **#71 blend**. See `PEEK_FINDINGS.md` Closed by #66.
Range Tech Patch A muzzle (kit-tip spawn + `hip_honest_dir` + tip→impact streak clamp): fulcrumRust PR #67 (2026-09-08) — **landed**. Sits on **−/=** zero (#78; was **O** #33) + #76 SIM-only + #59 tracers-until-impact; does not replace them. Did not fight Hypha #66 / did not ship heat color. Lab-Rat terrain untouched. See `PEEK_FINDINGS.md` Closed by #67.
Range Tech ADS viewmodel DoF (ADS near + far on #55 stack; radius **0.0048** / taps **12** / near fade 0.90→2.20 m; breath mul **1.6 parked**): fulcrumRust PR #68 (2026-09-08) — **landed**. Same Options **DOF** / `project.json` `depth_of_field`. See `PEEK_FINDINGS.md` Closed by #68.
Range Tech heat dial blend toward aim-offset dump (was→now→stolen on the #66 post path; haze **0.07** / size **0.83** / scaleX **0.396** / lobe **0.698**; dump-dial cooking/~ → landed/X): fulcrumRust PR #71 (2026-09-08) — **landed**. #66 architecture stays; no orange card redraw. Glasses / live sheet still drive fields. See `PEEK_FINDINGS.md` Closed by #71 + `heat-card-dial-sheet.md`.
Range Tech SIM-only launch (one HoB + gravity / zero model; arcade aim-dir dead; leftover `hob_zero` ignored; **P** unused; #67 hip honesty + per-kit recoil/`yaw_walk` stay): fulcrumRust PR #76 (2026-09-09) — **landed**. Not a precomputed bake. Zero distance is **−/=** after #78 (was **O**). See `PEEK_FINDINGS.md` Closed by #76.
Range Tech hold-O extract / −/= zero / grounded slide: fulcrumRust PR #78 (2026-09-09) — **landed**. Hold-**O** raid intent (`Session::extract_checking`); **O** is **not** zero; **−/=** step 50/100/200; exposure keyboard unbound; midair Shift+Ctrl cannot float-slide. Augury EXTRACT elbow card **landed #85** (no popup). Hatch toggle + shaft ride **landed #115**. Door / extract cancel chrome **later landed #120**; timed surface kill still **~**. #76 SIM-only + **P** unused + #67 hip honesty stay. See `PEEK_FINDINGS.md` Closed by #78.
Range Tech land sway softener + heightfield-grounded FX: fulcrumRust PR #79 (2026-09-09) — **landed**. Same #59 hop overlay — **not** a second land system. Punch **0.028** · duck **0.08** · shake **0.14** gate **13** + sway eye **0.014** / yaw **0.012** / roll **0.018** · decay **4.6**. Hop 12/30/1 **unchanged**. Brass / tracer ends / marks snap to extract `World::surface_height` / wall support; `first_hit` walls-only; no flat `floor_y` / pawn feet / phantom y=0. AXIS_LOCK sim barrel **+Z** unchanged. See `PEEK_FINDINGS.md` Closed by #79.
Range Tech Options Audio output DEVICE (SYSTEM DEFAULT via cpal `default_output_device()`; A/D or arrows / Enter / click cycle; persist `output_device`; missing pin kept, playback falls back to OS default; same #21 mixer → thin cpal voice; UI tick on the new pick; Stream on window thread — not Sync): fulcrumRust PR #82 (2026-09-09) — **landed**. `12676383`. Bus dials unchanged. Not a second mix tree. See `PEEK_FINDINGS.md` Closed by #82 + `EXTRACTION_AUDIO_LOCK.md`.
Range Tech H shoulder-swap tilt (chest-cross pitch/yaw/roll **0.08 / 0.32 / 0.39** on existing ViewmodelDials / ADS cant DNA; travel stays #59 hip +X ~0.10 → ~−0.041 / `shoulder_x_min` **−0.055** / ads_keep **0.32** / `shoulder_viewmodel` **0.12**; not a capsule/eye slide, not a mesh mirror, no `scale.x = −1`; PreferredHand / new-profile onboard **later landed #116**): fulcrumRust PR #84 (2026-09-09) — **landed**. `7d7e18f5`. Live hip / left tilt **superseded #94** / **#98**. See `PEEK_FINDINGS.md` Closed by #84.
Augury elbow smart-labels (thin white analysis-core card + L-elbow / leader to the world interact pin; not a centered HUD; hold-**O** EXTRACT elbow card, no popup; EXTRACT white mono; no second ammo HUD; hatches on yard pad `-24/-24` · `18/-28` · `-28/16` + shaft `18/-12`; hatch toggle + shaft ride **later landed #115**; door / extract cancel chrome **later landed #120**; timed surface kill still **~**): fulcrumRust PR #85 (2026-09-09) — **landed**. `f3d60a24`. See `PEEK_FINDINGS.md` Closed by #85 + `AESTHETIC_DIEGETIC_LOCK.md`.
Hypha Graphics dump (Options **FOG / FOG NEAR / FOG FAR / CAM NEAR / CAM FAR** + persist `project.json`; fog **375 / 520** · cam **0.05 / 2000** · clouds **0.63** · sunPunch **0.51** · light*Mul **0.11 / 0.41 / 0.61 / 2.11 / 1.65 / 1.06** · exp **1.44** · skyHdri on; hideout `haze_max` **0**; bloom / godRays / brightness / gamma **no path**; heat haze stays Range #71; **sunSize 0.62** was parked — **#87** rides the disc): fulcrumRust PR #86 (2026-09-09) — **landed**. `13865b3f`. See `PEEK_FINDINGS.md` Closed by #86.
Range Tech + Hypha HDRI sun black-out / blow-out (Goegap plate solar-region tone + dump **sunSize 0.62** soft disc; sky Reinhard × 0.20 / solar white-point **8 × 0.55**; disc `mix(1800, 80)` + HDRI complement **0.55 / 0.18**; local shoulder 0.95 / clamp 0.96; #86 fog / punch / exp / cam stay; not a second sky; bloom / godRays still no path): fulcrumRust PR #87 (2026-09-09) — **landed**. `5f2577d6`. See `PEEK_FINDINGS.md` Closed by #87.
Hypha biped foot plant / terrain follow (heightfield column; FOLLOW **8.5** / DEADZONE **0.04** / RISE **2.2** / SINK **6.5** / SNAP_ERR **1.15** / LIFT_MAX **0.14** / BOOT_HALF_H center **0.11**; Mixamo sockets Pelvis / Foot_L / Foot_R / Head host hooks only; A-notes `[·] enemies walk into terrain` → **X**; STEAL_MAP biped **todo → partial**; Mixamo clips / player body / 2-bone IK / GPU skin parked; mesher untouched): fulcrumRust PR #88 (2026-09-09) — **landed**. `78e11990`. See `PEEK_FINDINGS.md` Closed by #88.
Range Tech projectile feel (rect slab + 4–6 debris / visualLength **1.5 / 18** / core **2.85 / 2.25 / 0.95** / slug **0.07** / wake 1–2 / hit flash **0.15** s / punch **8–12** 35% white / scuff **4–6** amber / fire-pulse glyphs on existing `TracerField`; SIM / HoB / HeatDials unchanged; AXIS_LOCK +Z / #79 snap stay; CE tip **0.2.8** preferred for later muzzle-adjacent haze — not a heat-card rewrite): fulcrumRust PR #89 (2026-09-09) — **landed**. `a3e28ec0`. See `PEEK_FINDINGS.md` Closed by #89 + `VECTOR_MAG_DUMP.md`.
Hypha pixellation / warp strength floor (`PostToggles.warp_strength` default **0.01**; Options Graphics **WARP** after CAM FAR; `GFX_LEN` 12→13; persist `project.json` `{:.2}` → `0.01`; `pixel_warp_uv` after `heat_warp_uv`; mix toward CE PIXEL SCALE **2**; smoke `gfx=` appends ` warp=0.01` only; existing `fog/375/520 cam=0.05/2000` stays; STEAL_MAP Augury pixellation **todo → partial**; Augury aesthetic only — do not steal into Range; heat/sun/fog/binds/stamps/net/bipeds untouched): fulcrumRust PR #90 (2026-09-09) — **landed**. `54a99f10`. See `PEEK_FINDINGS.md` Closed by #90.
Range Tech Patch A RH hip bias (authored hip **+X 0.1843** was ~0.10; `shoulder_cross_x` **−0.225** keeps H dest ~−0.041 / `shoulder_x_min` **−0.055** / ads_keep **0.32**; left hold slight straighten pitch/yaw/roll **0.04 / 0.10 / 0.08** supersedes #84 chest-cross 0.08/0.32/0.39; ADS X / inspect X / tip spawn / `hip_honest_dir` / #89 tracers stay; not a mesh mirror / no `scale.x = −1`; PreferredHand / new-profile onboard **later landed #116**): fulcrumRust PR #94 (2026-09-09) — **landed**. `a3a42e4f`. Live End tuner on these same dials **later landed #97**. Live hip / ready-Y **superseded #98**. See `PEEK_FINDINGS.md` Closed by #94.
Range Tech aim-offset tuner + attachment sockets (live **End** sheet on existing ViewmodelDials + kit_mesh optic/can sockets; Insert WEAPON↔ATTACH · PageDown pose/attachment · PageUp MICRO/FINE/MED/COARSE · Delete JSON; glasses `AIM TUNE`; Home debugger **later landed #110**; authored defaults now **#98**; identity PoseOffset = live authored mounts; not Home chrome at #97, not hitch logger at #97, not EffectComposer, not a second pose system; kit boxes + muzzle tip follow live can/optic offsets; world drops stay authored identity): fulcrumRust PR #97 (2026-09-09) — **landed**. `6908ec88` / `8ac9130b`. AIM TUNE LIVE persist **later landed #103**. Home debugger **later landed #110**. See `PEEK_FINDINGS.md` Closed by #97.
Range Tech AIM TUNE LIVE persist (End LIVE flush → Hypha `project.json`; `aim_live` default **true**; `aim_tune.example_smg` / `example_rifle` / `example_sniper`; pose `hip` `hip_low` `hip_cant` `sprint_high` `ads` `ads_cant` `ads_holo` `ads_acog` `ads_sniper_scope` `inspect` each `{x,y,z,rotX,rotY,rotZ}`; attach `optic` / `can`; load on Deploy / `Settings::boot` → `Session::apply_aim_settings`; each LIVE nudge flushes; partial merge keeps authored **#98 / #99 / #100**; #97 End / Delete dump stay; End stays AIM TUNE; RECORD toggle stub — no bind; not bake-permanent-defaults / UV / Beabim / heat): fulcrumRust PR #103 (2026-09-09) — **landed**. `74da84e3` / `e0452f82`. Home debugger **later landed #110**. See `PEEK_FINDINGS.md` Closed by #103.
Augury CE Home debugger (native overlay — not a TS paste; **Home** toggle · LOGS / TELE / CHEAT · hitch WARN >33 ms / HITCH >100 ms · reason tags FRAME / LOAD / STREAM / BAKE / GATE · ring 256 / 8 rows · telemetry 1s FPS · cheats GOD / NOCLIP / TELEPORT / SPAWN · persist `debugger_tab` shares `project.json` with Range `aim_live` / `aim_tune`; glasses `DEBUG`; analysis-core thin white frames / fade-in white mono; End stays AIM TUNE #97/#103; hitch *visibility* only; hitch *fix* **later landed #108** — not CE heartbeat flags / End tuner changes; LOGS COPY / tracks **later landed #121**): fulcrumRust PR #110 (2026-09-09) — **landed**. `7ff3c311`. See `PEEK_FINDINGS.md` Closed by #110. Hitch *fix*: Closed by #108. LOGS COPY: Closed by #121.
Augury Home LOGS COPY + event tracker toggles (**Enter** COPY full boot→now ring via leftover helper + cwd `fulcrum.logs` / `FULCRUM_LOGS`; ring **800**; `[sssss.mmm]`; Insert/Delete **STREAM** · **BAKE** · **GATE** · **PLAY**/GAMEPLAY · **INT**/INTERNAL; `log_*` persist default **on**; hitch warn >33 / spike >100 stay; TELE max ms stays when tracks off; medium edge events BOOT / GPU / GATE / STREAM r↑ cold↓ / FIRE / HIT / AI / HATCH / WOUND / DOWN / DEAD / STIM / HEAL / RELOAD / SLASH / DROP / TAKE / CHEAT / COPY; glasses `DEBUG`; #110 stays tabs+logger foundation; does **not** rewrite Hypha #108 hitch amortize — emits/tags richer STREAM lines): fulcrumRust PR #121 (2026-09-09) — **landed**. `2416ec09`. See `PEEK_FINDINGS.md` Closed by #121.
Hypha stream hitch amortize (cook=1/2 · prefetch=5 m · splash-pumped load-in on the existing #81 9×9; `COOK_BUDGET_PLAY` **1** / `COOK_BUDGET_LOAD` **2**; 5 m face prefetch does **not** open a second 9×9; skeleton + splash-pumped load-in; no Sync whole 9×9 dump; emit `STREAM` / `BAKE` `r=` `cold=` `pend=` into #110 logger; walk inside a cell with focus+LOD unchanged stays a no-op; mesher stolen — no greenfield mesher; live octree / residual soft LOD pop inside a cell parked; Range poses / AIM TUNE / loot · Lab-Rat UV · Beabim net · Augury Home tabs untouched): fulcrumRust PR #108 (2026-09-09) — **landed**. `b3be2974`. See `PEEK_FINDINGS.md` Closed by #108 + `TERRAIN_NORTHSTAR.md`.
Range Tech RH hip one more body-width + ready-hip Y (MP9-Z hip **0.2403 / −0.2128 / −0.1833** was #94 0.1843 / −0.1688 / −0.1953; +0.056 X = 2 × MP9 `receiver_half.x` 0.028; Y **−0.044** ready-hip drop; Z **+0.012** tighter; hip_cant +X/+Z only; sprint_high X **0.29 → 0.346**; SR-25 hip **0.256 / −0.224 / −0.208**; M24 hip **0.261 / −0.229 / −0.228**; `shoulder_cross_x` **−0.281** / `shoulder_cross_y` **0.032** keeps H dest ~−0.041 X / ~−0.181 Y; `shoulder_x_min` **−0.055**; ADS X / left pitch/yaw/roll **0.04 / 0.10 / 0.08** unchanged; #97 End tuner still live on these #98 ready-hip / H defaults; live hip_low **superseded #99**; not a mesh flip / Beabim / heat / terrain / PreferredHand onboard): fulcrumRust PR #98 (2026-09-09) — **landed**. `48518709` / `5b02e2ab`. See `PEEK_FINDINGS.md` Closed by #98.
Range Tech low-hip shotgun stance (U-cycle `hip_low`; MP9-Z **0.2403 / −0.3528 / −0.1513** / pitch **0.145** was #98 0.2403 / −0.2788 / −0.1633 / 0.0765; Y **−0.074**; gap **0.140** vs ready **−0.2128**; Z tucked; SR-25 **−0.364 / −0.176 / 0.148**; M24 **−0.369 / −0.196 / 0.146**; glasses **LOW HIP**; RMB from LowHip = iron ADS not `ads_cant`; ready hip / hip_cant / ADS / H stay #98; #97 End tuner still live; Greyzone CQC ADS **later landed #100**; U-cycle pose ease **later landed #109**; not a mesh mirror / Beabim / heat / terrain / PreferredHand onboard): fulcrumRust PR #99 (2026-09-09) — **landed**. `ed6dff0e`. See `PEEK_FINDINGS.md` Closed by #99.
Range Tech canted 45° Greyzone CQC ADS (dial-only `ViewmodelDials.ads_cant`; MP9-Z **0.0423 / −0.148 / −0.136** / pitch/yaw/roll **0.024 / 0.11 / 0.785** was 0.034 / −0.142 / −0.172 / 0.02 / 0.035 / 0.785; X = iron 0.0084 + optic-root 0.048·sin45; Z = CQC-close holo −0.1335 lane; yaw inward ~6°; SR-25 / M24 **0.0468 / −0.154 / −0.148**; U+RMB / hold-Mouse5 @ 60° CQC; glasses **CANT 45** / **CANT ADS**; hip_low stays #99; ready-hip / hip_cant / primary ADS / H stay #98; #97 End tuner still live; not a canted-holo mesh / IOR glass / mesh flip / Beabim / heat / terrain / PreferredHand onboard): fulcrumRust PR #100 (2026-09-09) — **landed**. `842b3efa`. U-cycle pose ease **later landed #109**. See `PEEK_FINDINGS.md` Closed by #100.
Range Tech U-cycle hold springs (Chest / LOW HIP / CANT pose ease; `hold_spring` **7.0** house-medium between ADS `blend_speed` **6.4** and H `shoulder_spring` **8.0**; sprint **6.2** / inspect **10.0** unchanged; same exp-approach `k = 1 − e^{−rate·dt}`; glasses still snap CHEST / LOW HIP / CANT 45; viewmodel springs; inspect / sprint_high lerp on eased home; first-U seed-before-cycle so load phases do not init onto LowHip; 1P only; STEAL_MAP pose-ease → **in**; #98/#99/#100 poses · #97 End tuner · #103 LIVE persist · #57/#59 springs DNA stay; not Beabim / 3P / heat / terrain / PreferredHand / ADS blend folded into `hold_spring`; ADS `blend_speed` **6.4** stays its own dial — **#113** scales it by kit ergo): fulcrumRust PR #109 (2026-09-09) — **landed**. `6108cf91` / `fc30eb30`. See `PEEK_FINDINGS.md` Closed by #109.
Range Tech kit handling / ergo / MOA (`HandlingStats` / `FeelSheet::handling` drives existing 1P fire/ADS dials; ADS `blend_speed` **6.4** × kit ergo — MP9 **8.00** / SR-25 **6.40** / M24 **5.12**; handling → recoil `1/handling` on authored kick / pitch / yaw; `ads_recoil_mul` **0.6** stays; hip MOA after `hip_honest_dir` — MP9 **4.0** · SR-25 **1.2** · M24 **0.40**; ADS × **0.22**; velocity / cycle stay `SmgFireDials`; mag_fill reload stub default **1.0**; `hold_spring` **7.0** stays sibling; STEAL_MAP handling → **in**; house mastery row stays parked; not house mastery / gear UI / Beabim 3P / net / loot / heat rewrite / Lab-Rat / Augury Home / PreferredHand): fulcrumRust PR #113 (2026-09-09) — **landed**. `719deae6` / `421d61b8`; merge tip `b2d384144c8ad23d500f59a0c3a02ab3d41b92f8`. See `PEEK_FINDINGS.md` Closed by #113.
Augury hatch/elevator glasses UX (hold-F hatch OPEN/CLOSED + Akira shaft RIDE/EXIT on #85 elbows; `HatchBoard`; idle `HATCH  HOLD F  OPEN` / `SHAFT  HOLD F  RIDE`; holding `HOLD F  OPEN  42%`; hold-O `EXTRACT  OPEN|CLOSED|SHAFT`; no modal popup; `HOLD_SECS` **1.15** · `COOL_SECS` **0.55** · `must_release` after commit · `RIDE_SECS` **1.40** · `SHAFT_CAP_Y` **16.65** · `CAP_LIP_X` **1.95** · `EXIT_PAD_X` **2.65** · `CAP_KEEP_M` **2.05**; open-well rings + ride cage on extra-solids; tap-F pickup still wins; downed cancels a ride; yard plots `-24/-24` · `18/-28` · `-28/16` + shaft `18/-12`; door / extract cancel chrome **later landed #120**; timed surface kill / extract loot loop still **~**): fulcrumRust PR #115 (2026-09-09) — **landed**. `eb8618df` / `eb811e74`; merge tip `469d46b0`. See `PEEK_FINDINGS.md` Closed by #115 + `AESTHETIC_DIEGETIC_LOCK.md`.
Augury door/extract cancel chrome (hideout door **F** + OPEN quiet hatch arm `GATE_SECS` **2.20** glasses countdown; same HOLD % language as hatch #115; walk away cancels; stay commits; `COOL_SECS` **0.55**; idle `DOOR  F  DEPLOY`; armed `DOOR  DEPLOY  N%` · `EXTRACT  N%`; analysis-core white mono, not gold; hold-O still intent only — countdown wins while armed; shaft is a ride, not extract-out; `GateSignal` local leftover — no new KIND; Esc/alt-tab pause + KIND_RAID handshake **later landed #122** (Beabim; leftover = `GATE_SECS` **2.20**; glasses stay this PR); timed surface kill / extract loot loop still **~**; in-repo `docs/GATE_DIAL_SHEET.md`): fulcrumRust PR #120 (2026-09-09) — **landed**. `77f0cd67` / `4aaf40a` / `3db2e7e`; merge tip `089e0ad0`. See `PEEK_FINDINGS.md` Closed by #120 + `AESTHETIC_DIEGETIC_LOCK.md`.
Hypha PreferredHand + new-profile onboard (PreferredHand enum **Right** default if unset; Title Deploy / Host / Join gates NEW PROFILE — must pick RIGHT / LEFT before first raid; `project.json` `profile_onboarded` + `preferred_hand` permanent vs live session copy; death clears live; extract→stash stub — KIND_LOOT already covers Z/F; `shoulder_t` 0 = authored RH / 1 = existing left dest — no `scale.x = −1` / mesh flip; does **not** steal Range ergo / MOA / pose springs · Augury hatch · Lab-Rat stamps · Beabim world/sim / loot trail · root README; not full PMC stash / character tab / world-pool death loot / Beabim net sync of PreferredHand): fulcrumRust PR #116 (2026-09-09) — **landed**. `6018f8ad384cbc0bcf6e7d9c818f2d23f3d145ad` / tip `d531b27f11281f993f53ccbf8d1579a8539ad91e`. See `PEEK_FINDINGS.md` Closed by #116.
Texture LOD compress + atelier read-only: clerk lock, Initial Visuals (2026-09-07). Lab-Rat **#58 quiet grit greyscales landed** (vendored bake-downs); Hypha ring-mip texture LOD **shipped #60** (256/64/16; far softer; atelier read-only). Further roughness→stamp still open. Quiet influence — no franchise name-drop. See `PEEK_FINDINGS.md` Closed by #60 / `STAMP_FEEL_LOCK.md` / `TERRAIN_NORTHSTAR.md`.
LOD-tied grit / material mips (near 256² / mid 64² / far 16² BC4-style; far drops grain hashes; atelier read-only): fulcrumRust PR #60 (2026-09-07) — **landed**. Hypha. See `PEEK_FINDINGS.md` Closed by #60.
Near LOD raise (16/8/4 → 32/16/4; grid/radius stay #43; grit mips stay #60): fulcrumRust PR #61 (2026-09-08) — **landed**. Hypha. See `PEEK_FINDINGS.md` Closed by #61.
Authored SFX vs spatial split (Range Tech file slots / Augury Chamber spatial / Lab-Rat quiet stamps): Initial Visuals Group Chat (2026-09-07) — wiring shipped #54; day-one handmade vendor landed #62; DEVICE cycle landed #82; shot propagation still later.
Authored SFX file slots: fulcrumRust PR #54 (2026-09-07) — wiring. Handmade atelier vendor: fulcrumRust PR #62 (2026-09-08) — **landed**. Small set, not a full CE / aim-offset pack dump.
First big-map (drop walls · ~8× extend · chunked Transvoxel · slope COL · local-player stream): Evan dump (2026-09-08) / Hypha **#81 landed**. Stamp pad still 7×7. Stream hitch amortize **later landed #108** on that same 9×9. Lab-Rat slope/PBR/dirt/scatter/deform plugs **landed #80**. NRM/GLOSS parked. Beabim peer feet `stream_anchors` **landed #83** (coordinate only). Range Tech kits+FX draw + `dBXpg` still **open**; kit PBR stub + music playlist **landed #64** / Augury FoW brand+menu video **when cut ready**. Atelier PBR batch **in** (150 roughness + textures/PBR ~26 sets). See `TERRAIN_NORTHSTAR.md` + `PEEK_FINDINGS.md` Closed by #81 / #108 / #80.
Hypha 19×19 open extract + chunk stream + slope COL hooks: fulcrumRust PR #81 (2026-09-09) — **landed**. `73dc8fe4`. Underfoot **32/16/8/4**. Smoke `subdivs=32/16/8/4` `extract_m2=92416` `resident=` `stream_cold=` `pbr=`. Stream hitch amortize **later landed #108**. Do **not** claim NRM-GLOSS GPU / world replication / Range heat as this PR. Lab-Rat plugs **landed later #80**. Peer feet `stream_anchors` **landed later #83**. See `PEEK_FINDINGS.md` Closed by #81.
Lab-Rat slope/PBR + dirt/scatter/deform plugs (`classify_slope` + 256² DISP bake-down + `Deform` / `GroundScatter` filled at `8,-6` / `-10,14`; `PBR_HEIGHT_AMP` **0.028** / `SCATTER_AMP` **0.018** / pad half **56**; smoke `pbr=tint plugs=slope+deform+scatter`; Hypha #81 owns vertex COL; NRM/GLOSS parked): fulcrumRust PR #80 (2026-09-09) — **landed**. `2cda73bc`. See `PEEK_FINDINGS.md` Closed by #80.
Lab-Rat subtract crawl pad network (shallow mouth → mid → pocket → +Z spur + west/east + kink; radii **0.42–0.50**; `CRAWL_DROP` **0.38** m; Mouth XZ **−1.60, 8.20** · Pocket **0.25, 9.15**; glasses `CRAWL  SUBTRACT`; Union lip stretches **up**; bowl above `SLAB_Y0` **−0.7**; full guts / live voxel collide still `[~]`): fulcrumRust PR #114 (2026-09-09) — **landed**. `8fa74c03` / `28c09bd7`; merge tip `898454a0`. See `PEEK_FINDINGS.md` Closed by #114 + `STAMP_FEEL_LOCK.md`.
Atelier clean yell + SFX remix DNA + Music playlist beds: Evan dump (2026-09-08 ~00:00 ET) — atelier plugs **open** (was read-only). Lab-Rat slope/PBR/dirt/scatter/deform plugs **landed #80**. Range Tech `dBXpg` still **open**. Music playlist + kit metal/grit PBR stub **landed #64**. Remix first ±6% jitter **landed #64**; full remix minting still **open**. Augury FoW brand/menu video when cut ready · Hypha big-map continues on fulcrumRust. Do **not** claim NRM-GLOSS / whole roughness→stamp / `dBXpg` / menu video shipped. 8× open extract **is** shipped #81. See `ATELIER_PORTFOLIO_STEAL.md` + `EXTRACTION_AUDIO_LOCK.md` + `PEEK_FINDINGS.md` Closed by #80 / #81.
Range Tech music playlist + kit metal/grit PBR stub + ±6% FX remix jitter: fulcrumRust PR #64 (2026-09-08) — **landed**. Five titled beds; stub PBR on MP9-Z / SR-25 / M24; store `dBXpg` still missing. See `EXTRACTION_AUDIO_LOCK.md` + `PEEK_FINDINGS.md` Closed by #64.
Holocron viewer gift (atelier `tools_for_ai_and_dev/Holocron_Visualizer.py` + `Analyze-Holocron.ps1`): Evan dump (2026-09-08) — tree nested-rectangle file-base viewer; cut monoliths (agent context; overwrite loss). Slope/PBR plugs **landed #80**. Lab-Rat rust rewrite still waits on SVG / density-mask / monolith splits. See `TOOLS.md`.
Vector mag dump (aim-offset / Vector feel — rect yellow-white muzzle flash + orange grit + diegetic red receiver glyphs + flash-as-local-light): clerk shelf 2026-09-09; **live steal landed #89**. Artistic auth frame stays `VECTOR_MAG_DUMP.md` (local light / optic still reference-only). Pixel dither / floor warp **landed #90** (Hypha post dial `warp_strength` **0.01**; Augury aesthetic only). Do **not** invent bloom / godRays or reopen orange heat cards. See `VECTOR_MAG_DUMP.md` + `PEEK_FINDINGS.md` Closed by #89 / Closed by #90.
1P viewmodel ≠ 3P biped gun (MP honesty — fake / artistic 1P posing OK; peers must not see guns through eyeballs; Range Tech 1P / AIM TUNE · Beabim 3P sync · Lab-Rat stamps out; HANDS later): Evan lock (2026-09-09 InitialVisuals) — **partial shipped #91** (peer biped hip gun stub). Full 3P kit honesty / hands / gear sync still open. Do **not** claim Mixamo / full 3P kit honesty. See `PEEK_FINDINGS.md` Holding / locked intent — 1P ≠ 3P + Closed by #91.
Scope glass (greyscale / B&W ramp · fake curve + thickness · IOR + ramp magnify · bodycam no-PiP scope pass; Hypha Graphics when LPVO; Range AIM TUNE placements first): Evan lock (2026-09-09 InitialVisuals) — **holding until LPVO, not shipped**. Do **not** claim LPVO or glass live. See `PEEK_FINDINGS.md` Holding — greyscale glass + Evan asset-ask.
Evan asset-ask path (clone CE / aim-offset attachment tables first; missing → ask Evan this week to model + texture; primitives stay scaffolding; style grows with peeks; Lab-Rat procedural grit until the list, then bake onto authored): Evan lock (2026-09-09 InitialVisuals) — **holding / locked intent, not shipped**. Do **not** claim authored attachments / Evan models shipped. See `PEEK_FINDINGS.md` Holding — greyscale glass + Evan asset-ask.
