# Checkpoint peek findings (fulcrumRust)

Parked from Evan’s first full `main` peek (2026-09-07). Growth yard + curl read OK. Same-day feel dump **landed #59**. Hypha ring-mip texture LOD **landed #60**. Hypha near LOD raise **landed #61**. Range Tech handmade atelier SFX vendor **landed #62**. Range Tech music playlist + kit metal/grit PBR stub + ±6% remix jitter **landed #64**. Hypha colorless muzzle heat **landed #66**. Range Tech Patch A muzzle **landed #67**. Range Tech ADS viewmodel DoF **landed #68**. Range Tech heat dial blend **landed #71**. Range Tech SIM-only launch **landed #76**. Range Tech hold-O extract / −/= zero / grounded slide **landed #78**. Range Tech land sway softener + heightfield-grounded FX **landed #79**. Hypha first big-map 19×19 open extract + slope COL **landed #81**. Range Tech Options Audio output DEVICE / cpal cycle **landed #82**. Range Tech H shoulder-swap tilt **landed #84**. Beabim two-instance pose sync + in-pause JOIN **landed #83**. Hypha Graphics dump **landed #86**. Augury elbow smart-labels **landed #85**. Range Tech + Hypha HDRI sun black-out / blow-out **landed #87**. Hypha biped foot plant / terrain follow **landed #88**. Lab-Rat slope/PBR/dirt/scatter/deform plugs **landed #80**. Range Tech projectile feel **landed #89**. Range Tech Patch A RH hip bias **landed #94**. Range Tech aim-offset tuner + attachment sockets **landed #97**. Range Tech RH hip one more body-width + ready-hip Y **landed #98**. **1P viewmodel ≠ 3P biped gun** (MP honesty) is **holding / locked intent — not shipped** (Evan 2026-09-09). **Scope glass** (when LPVO) + **Evan asset-ask path** are **holding / not shipped** (Evan 2026-09-09). Overnight cooks steal from this shelf. Evan **clean** yell 2026-09-08 ~00:00 ET — atelier plugs **open**.

## Patch A checkpoint (fulcrumRust #72)

Living A-feedback checkpoint — **not** a replacement for `STEAL_MAP` or `MILESTONE_01_PLAYABLE`. Repo-root [`patch notes A.txt`](https://github.com/initialvisuals/fulcrumRust/blob/main/patch%20notes%20A.txt) ([#72](https://github.com/initialvisuals/fulcrumRust/pull/72)). Marks: `X` done / on main · `~` partial / in progress / shallow first pass · `*` next / ready for a careful cook when greenlit · `·` parked / not started. Seats: Range Tech | Hypha | Lab-Rat | The Augury | Evan | house. Overnight cooks and seats read open A asks from that file; do **not** invent PR numbers. Do **not** copy the ledger here. Range Tech dump-dial blend is **landed #71** (`X` on the house shelf — A-notes `~` for that row is stale). Range Tech sim-default / single model is **landed #76** (`X` on the house shelf). Range Tech hold-O extract intent / **−/=** zero / grounded slide is **landed #78** (`X` on the house shelf). Augury glasses polish + EXTRACT elbow card is **landed #85** (`X` on the house shelf — hatch elevator / toggle / timed kill popup stay `~`). Range Tech land overlay soften + heightfield ground FX is **landed #79** (`X` on the house shelf — hop 12/30/1 **unchanged**; same #59 overlay, not a second land system). Hypha first big-map 19×19 open extract + chunk stream + slope COL is **landed #81** (`X` on the house shelf — vertex albedo only). Lab-Rat slope/PBR/dirt/scatter/deform plugs **landed #80** (`X` on the house shelf — DISP bake-down + deform/scatter filled; NRM-GLOSS still parked; SVG / density-mask / experiment-log still open). Beabim two-instance pose sync + HOLD JOIN is **landed #83** (`X` on the house shelf — peer feet / `stream_anchors` follow remotes; shoot / Locus / terrain rewrite / audio stay local). Range Tech Options Audio output DEVICE / cpal cycle is **landed #82** (`X` on the house shelf — A-notes already `X` from #82; bus dials unchanged). Range Tech H shoulder-swap tilt is **landed #84** (`X` on the house shelf — travel dest ~−0.041 / cap **−0.055** / ads_keep **0.32**; live left hold **#94** slight straighten pitch/yaw/roll **0.04 / 0.10 / 0.08**, supersedes #84 chest-cross 0.08/0.32/0.39; not a mesh mirror. PreferredHand / new-profile onboard stays house/Hypha parked). Hypha Graphics dump is **landed #86** (`X` on the house shelf — thin Options **FOG / FOG NEAR / FOG FAR / CAM NEAR / CAM FAR** + sky / post defaults; persist `project.json` alongside Range `output_device`; hideout `haze_max` **0**; bloom / godRays / brightness / gamma stay parked / no path). Range Tech + Hypha HDRI sun black-out / blow-out is **landed #87** (`X` on the house shelf — dump **sunSize 0.62** now rides the procedural disc/halo; plate solar-region tone + soft disc; #86 fog / punch / exp / cam stay; bloom / godRays still no path). Hypha biped foot plant / terrain follow is **landed #88** (`X` on the house shelf — A-notes `[·] enemies walk into terrain` → **X**; STEAL_MAP biped **todo → partial** — plant + host hooks; Mixamo clips / player body / 2-bone IK / GPU skin still parked). Range Tech projectiles from CE / feel-lab visualLength + Vector dump flash is **landed #89** (`X` on the house shelf — A-notes `[·] projectiles from CE (Range Tech)` → **X**; SIM / HoB / gravity stay #76; HeatDials stay #71; AXIS_LOCK +Z / #79 snap unchanged). Range Tech Patch A RH hip bias is **landed #94** (`X` on the house shelf — first +0.08; live hip / ready-Y **superseded #98**). Range Tech aim-offset tuner + attachment sockets is **landed #97** (`X` on the house shelf — A-notes ledger `~` / parked `·` for this cook is stale). Live **End** sheet on existing `ViewmodelDials` + `kit_mesh` optic/can sockets; Home stays unbound / Augury. Range Tech RH hip one more body-width + ready-hip Y is **landed #98** (`X` on the house shelf — MP9-Z hip **0.2403 / −0.2128 / −0.1833**; `shoulder_cross_x` **−0.281** / `shoulder_cross_y` **0.032** keeps H dest ~−0.041 X / ~−0.181 Y; hip_low Y stays #94 **−0.2788**; left pitch/yaw/roll **0.04 / 0.10 / 0.08** unchanged. #97 End tuner still live — authored defaults are now #98).

## Vector mag dump (Range Tech — landed #89)

Evan aim-offset / Vector feel reference. **Live steal landed #89** (Range Tech). Rect slab + debris + slug/wake + punch/scuff flash + fire-pulse glyphs sit on existing `TracerField`. Artistic auth frame stays `VECTOR_MAG_DUMP.md` (local light / optic still reference-only unless already on the feel sheet). Hypha / Augury own pixel dither + floor warp separately. Do **not** reopen orange heat cards or invent bloom / godRays. Intact siblings: #67 tip spawn · #76 SIM · #71 heat · #79 heightfield.

## Holding — first big-map leftovers (Evan 2026-09-08 / landed #81)

**Host landed #81.** Peer feet stream anchors **landed #83**. Lab-Rat slope/PBR/dirt/scatter/deform plugs **landed #80**. Do **not** claim NRM/GLOSS GPU / whole roughness→stamp / world replication / Range heat.

Live shelf: #16 host + #23 far-cold + **#81 19×19 / 304 m / 92 416 m²** + **9×9** stream + underfoot **32/16/8/4** + #60 grit mips + #39/#43 stamp pad **7×7** / yard ≈ **110 m²**. Walls **off**.

- **Hypha** host: drop walls · ~8× · chunk stream · local-player distance load **landed #81**. Graphics dump **landed #86** (Options FOG / CAM NEAR/FAR + sky / post defaults; hideout stays unfogged). HDRI sun disc **landed #87** (shared Range Tech + Hypha; dump **sunSize 0.62** rides the disc). Beabim peer feet + `stream_anchors` follow remotes **landed #83** (coordinate only — Transvoxel rewrite / terrain sync still parked). Biped foot plant / terrain follow **landed #88** (samples #79/#81 column; FOLLOW **8.5** / DEADZONE **0.04** / RISE **2.2** / SINK **6.5** / SNAP_ERR **1.15** / LIFT_MAX **0.14** / BOOT_HALF_H center **0.11**; mesher untouched). Residual LOD pop inside a chunk / far-4 horizon parked
- **Beabim** MP: two-instance UDP **POSE** + HOLD JOIN panel **landed #83**. Grounded silhouettes share Hypha #88 `plant_simple_root` (packet / handshake / HOLD join stay #83). Shoot / HoB / heat / Locus / stamps / audio / ToD stay **local**. **1P ≠ 3P** (holding / locked intent) — do **not** claim the #83 5-box is full 3P kit honesty; 3P gun / gear path still open
- **Lab-Rat** stamps: slope COL hooks (`pbr=tint`) **landed #81** vertex albedo only (Hypha owns that bind). Slope/PBR/dirt/scatter/deform plugs **landed #80** — `classify_slope` + DISP bake-down + `Deform` / `GroundScatter` filled at #81 XZ (`8,-6` / `-10,14`). Stamp pad stays **7×7**. NRM/GLOSS GPU parked. Evan **clean** yelled 2026-09-08 ~00:00 ET — atelier plugs **open**. Atelier **150 roughness + textures/PBR ~26 sets landed**. #58/#60/#80 stay the live yard plugs. Holocron rust rewrite still waits on SVG / density-mask / monolith splits — see `TOOLS.md`
- **Range Tech**: kits + FX draw-distance on the wider yard; kit metal/grit PBR stub **landed #64**; store `dBXpg` still **open**; Music playlist beds **landed #64**; ADS viewmodel DoF **landed #68**; heat dial blend **landed #71**; land sway + heightfield FX **landed #79**; Options Audio DEVICE **landed #82**; H shoulder-swap tilt **landed #84**. Patch A RH hip bias **landed #94** (first +0.08; live hip **superseded #98**). Aim-offset tuner + attachment sockets **landed #97** (live **End** sheet / glasses `AIM TUNE`; Home stays Augury; authored defaults now **#98**). RH hip one more body-width + ready-hip Y **landed #98** (hip **0.2403 / −0.2128 / −0.1833**; `shoulder_cross_x` **−0.281**; hip_low Y stays #94 **−0.2788**). HDRI sun disc **landed #87** (shared Hypha; dump **sunSize 0.62** rides the disc). Projectile feel **landed #89** (rect slab + debris + slug/wake + punch/scuff flash + fire-pulse glyphs — Vector mag dump live steal; artistic frame still `VECTOR_MAG_DUMP.md`). Heat cards / ballistics / binds **not touched** by #81. Heat / binds / ballistics / Audio DEVICE **not touched** by #86 / #87. #89 did **not** retune HeatDials / SIM / AXIS_LOCK +Z / #79 snap
- **Augury**: FoW brand / menu video **when cut ready**. Chrome **not touched** by #81 / #86. Elbow smart-labels **landed #85** (EXTRACT elbow card, no popup; hatch elevator / toggle / timed kill still **~**)

Do **not** claim NRM/GLOSS GPU, whole roughness→stamp, world replication / shoot/Locus/terrain sync, Range heat, `dBXpg`, full metal-tech kits, menu video, Mixamo clip import / GPU skin / player body, 2-bone IK, mesher rewrite, **LPVO**, or **scope glass** shipped. 8× open extract + wall drop + chunk stream + slope COL **are** shipped #81. Lab-Rat slope/PBR/dirt/scatter/deform plugs **are** shipped #80. Peer feet stream anchors + HOLD JOIN **are** shipped #83 (pose presence only). Music playlist beds **are** shipped #64. Kit metal/grit PBR stub **is** shipped #64. Options Audio DEVICE **is** shipped #82. Hypha Graphics dump **is** shipped #86 (fog 375/520 · cam 0.05/2000 · clouds 0.63 · sunPunch 0.51 — not bloom / god-rays). HDRI sun disc **is** shipped #87 (sunSize **0.62** rides the disc). Biped plant + host hooks **are** shipped #88 (STEAL_MAP biped **partial**). Projectile feel **is** shipped #89 (rect slab + debris + slug/wake + punch/scuff flash + fire-pulse glyphs — not a ballistics rewrite). RH hip bias **is** shipped #94 (first +0.08; live hip **superseded #98**). Aim-offset tuner + attachment sockets **is** shipped #97 (live End sheet; Home stays Augury — not CE Home tabs/logger; authored defaults now **#98**). RH hip one more body-width + ready-hip Y **is** shipped #98 (hip **0.2403 / −0.2128 / −0.1833**; `shoulder_cross_x` **−0.281** / `shoulder_cross_y` **0.032**; hip_low Y stays #94 **−0.2788** — not a mesh mirror, not a new shotgun pose). See `TERRAIN_NORTHSTAR.md`.

## Open — texture / atelier leftovers (roughness→stamp still open)

Range Tech Evan peek feel **landed #59**. Hypha ring-mip texture LOD **landed #60**. Hypha near LOD raise **landed #61**. Range Tech handmade atelier SFX vendor **landed #62**. Range Tech music playlist + kit metal/grit PBR stub **landed #64**. Hypha colorless muzzle heat **landed #66** (sample-only `heat_warp_uv` on the #55 post stack — lattice is post input only; no world-pipeline orange card). Range Tech Patch A muzzle **landed #67** (kit-tip spawn + `hip_honest_dir` + tip→impact streak clamp — hip-fire no longer behind the handguard / upper-right of the reticle; did not fight #66). Range Tech ADS viewmodel DoF **landed #68** (ADS near + far on the same #55 pass / Options **DOF**). Range Tech heat dial blend **landed #71** (was→now→stolen on the #66 post path — haze **0.07** / size **0.83** / scaleX **0.396** / lobe **0.698**; #66 colorless path stays). Range Tech SIM-only launch **landed #76** (arcade aim-dir + **P** toggle dead; leftover `hob_zero` ignored). Range Tech hold-O extract / **−/=** zero / grounded slide **landed #78** (**O** is **not** zero; Augury EXTRACT elbow card **landed #85** — no popup; hatch elevator / toggle / timed kill still **~**). Range Tech land sway softener + heightfield FX **landed #79** (punch **0.028** / duck **0.08** / shake **0.14** gate **13** + inertia sway; hop 12/30/1 **unchanged**; brass/tracers/marks snap to extract heightfield — no flat `floor_y` / pawn feet). Hypha first big-map **landed #81** (19×19 open + 9×9 stream + slope COL `pbr=tint`). Range Tech Options Audio output DEVICE **landed #82** (SYSTEM DEFAULT via cpal `default_output_device()`; A/D or arrows / Enter / click cycle; persist `output_device`; same #21 mixer → thin cpal voice). Range Tech H shoulder-swap tilt **landed #84** (tilt path; live left hold **#94** slight straighten pitch/yaw/roll **0.04 / 0.10 / 0.08**, supersedes #84 chest-cross 0.08/0.32/0.39; travel dest ~−0.041 / `shoulder_x_min` **−0.055** / ads_keep **0.32**; not a mesh mirror / no `scale.x = −1`; PreferredHand onboard stays house/Hypha parked). Range Tech Patch A RH hip bias **landed #94** (first +0.08; live hip **superseded #98**; ADS X / tip spawn / `hip_honest_dir` / #89 tracers stay). Range Tech aim-offset tuner + attachment sockets **landed #97** (**End** toggle; Insert WEAPON↔ATTACH; PageDown pose/attachment; PageUp step; Delete JSON; glasses `AIM TUNE`; Home stays Augury; authored defaults now **#98**). Range Tech RH hip one more body-width + ready-hip Y **landed #98** (MP9-Z hip **0.2403 / −0.2128 / −0.1833**; `shoulder_cross_x` **−0.281** / `shoulder_cross_y` **0.032**; hip_low Y stays #94 **−0.2788**; left pitch/yaw/roll **0.04 / 0.10 / 0.08** unchanged). Hypha Graphics dump **landed #86** (Options **FOG / FOG NEAR / FOG FAR / CAM NEAR / CAM FAR** + persist `project.json`; extract haze 375/520 · cam 0.05/2000 · clouds **0.63** · sunPunch **0.51**; hideout `haze_max` **0**; bloom / godRays / brightness / gamma **no path**). Range Tech + Hypha HDRI sun disc **landed #87** (dump **sunSize 0.62** rides the procedural disc/halo; plate solar-region tone + soft disc — not a second sky). Augury elbow smart-labels **landed #85** (embodied card + L-elbow to interact pin; hold-O EXTRACT, no popup). Hypha biped foot plant **landed #88** (heightfield column; FOLLOW **8.5** / DEADZONE **0.04** / RISE **2.2** / SINK **6.5** / SNAP_ERR **1.15** / LIFT_MAX **0.14** / BOOT_HALF_H center **0.11**; Mixamo sockets Pelvis / Foot_L / Foot_R / Head host hooks only; STEAL_MAP biped **partial**). Lab-Rat slope/PBR/dirt/scatter/deform plugs **landed #80** (`classify_slope` + DISP bake-down + deform/scatter filled; smoke `pbr=tint plugs=slope+deform+scatter`). Range Tech projectile feel **landed #89** (rect slab + 4–6 debris / visualLength **1.5 / 18** / core **2.85 / 2.25 / 0.95** / slug **0.07** / wake 1–2 / hit flash **0.15** s / punch **8–12** / scuff **4–6** / fire-pulse glyphs; SIM #76 + HeatDials #71 + AXIS_LOCK +Z + #79 snap unchanged). Further roughness→stamp still open (SVG / density-mask / experiment-log). Do **not** claim the whole roughness→stamp cook. Do **not** claim NRM-GLOSS GPU or `dBXpg` shipped.

- **Texture compression** — atelier roughness packs are **4k 48-bit PNG** (too large). Do **not** ship raw 4k 48-bit into the yard. Lab-Rat **#58 landed** the vendored near packs (256² bake-downs under loud scars). Hypha LOD-tied mips **landed #60** on Transvoxel **distance rings** (near 256² / mid 64² / far 16²; far drops grain hashes). In-repo grit mips stay #60 until Lab-Rat cooks more. Do **not** claim the whole roughness→stamp cook
- **Atelier** — plugs **open** (Evan **clean** yell 2026-09-08 ~00:00 ET). PBR batch **in** (150 roughness + textures/PBR ~26 sets). #58 optional `FULCRUM_GRIT=` / `FULCRUM_ATELIER=` stay read-only **load** paths. Crew may plug; bake-down first
- **Lab-Rat** — **#58 quiet grit greyscales landed** (vendored bake-downs + `sample_channels` quiet height + `grit::rough` wear — the near source for #60). Slope/PBR/dirt/scatter/deform plugs **landed #80** (DISP bake-down + `Deform` / `GroundScatter` filled). Slope COL hooks reserved on host **#81** (vertex albedo only — Hypha owns that bind). Further roughness → stamp stays on **fulcrumRust only**; bake-down first. SVG / density-mask / experiment-log still open. Holocron rust rewrite still waits on those leftovers (`channels.rs` / stamp stacks / `feel` / `kit_mesh`) — see `TOOLS.md`
- Day-one FILE_SLOTS vendor **landed #62**. **SFX remix DNA** — creative reuse OK (pitch/speed/effects; indie underground; don’t overuse the same stem). First application **landed #64** — fire/foot/reload ±6% pitch/speed jitter on the #62 vendor; full remix minting still **open**. **Music** playlist beds **landed #64** (five titled beds; hideout+extract advance shuffle; Options Music dial; missing → two-tone stub). Options **Audio** DEVICE cycle **landed #82** (SYSTEM DEFAULT; persist `output_device`; missing pin kept, playback falls back to OS default; same #21 mixer → thin cpal voice — not a second mix tree). Shot propagation / full CE pack dump still later — that is audio files, not the #59 feel dials

## Closed by fulcrumRust #12 (2026-09-07)

- **Look / move mismatch** — locked: Y-up world, `yaw = 0` looks **+Z**; WASD look-relative. #12 authored mouse-right increases yaw; **#51 AXIS_LOCK** subtracts mouse X (invert horizontal) + invert A/D — see Closed by #51
- **Sideways gun** — SMG long axis is **look** (bore along +fwd); mag dots run along the bore
- **No visible bullets** — feel-lab tip→impact tracers + muzzle flash + spark/mark live. **#89** deepened the feel (rect slab + debris + slug/wake + punch/scuff flash) on the same `TracerField` — no new physics
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
- **Grimdark extract lock** — ashen wash / slate sides / brutalist vertex paint, proc wear/cracks, void-spore stamp tints, cheap distance haze; hideout stays small/unfogged. **#86** locks extract haze **375 / 520** + `haze_max` (hideout stays **0**)
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

- **Audio buses Voice / Music / FX** — feel-lab Settings Audio DNA (not a DAW); gains **0–2** default **1.00 / 100%** into a master; Options **Audio** tab is the live mixer (title + pause; #45 sits the Options list; #46 filled Graphics/Gameplay/Controls; Audio still this mixer); A/D or ←/→ nudge **0.05**; Esc Hypha pane / Audio → Options → title/pause; dials persist across Deploy. **#82** adds a **DEVICE** row (cursor 0, above Voice / Music / FX) — bus dials unchanged
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
- **Dials** — **[ / ]** clock ±30 min (wrap 0–24) · **K** snap dawn→noon→dusk→night · **L** live day↔night cycle · then **− / =** exposure mul (feel-lab **1.44** default) · **, / .** cloud cover. **#78:** **− / =** step zero; exposure keyboard unbound (no second pair; sky `nudge_exposure` may still exist). **#86:** clouds default **0.63** (was 0; **,** / **.** still nudge); `sunPunch` **0.51**; fog **375 / 520**; cam **0.05 / 2000**. **#87:** dump **sunSize 0.62** rides the procedural disc/halo
- **No XOR sky** — one ToD sample drives ambient / key / fill / fog + procedural dome together; dual color-aware lights. **#87** completed the HDRI sun disc on that same sample (not a second sky)
- **Grimdark luma crush** — `EXTRACT_SKY_LUMA` **0.20** keeps noon ashen (not a bright sandbox); Day HDRI shipped #40 (Goegap 4k plate; atelier stub is fallback). **#87:** sky keeps Reinhard × **0.20**; solar texels use white-point **8 × 0.55** (was Reinhard w=1 × 0.20 everywhere — ~0.21 hole)
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

- **Live HoB zero + arcade/sim launch** — per-kit rpm/recoil/HoB sheet was already authored (#22); this PR makes zero distance + arcade↔sim **live**. **#76 supersedes the dual path** — launch is **SIM only** (HoB + gravity / zero); arcade aim-dir dead; leftover `hob_zero` ignored. **#78** moves the zero bind to **−/=**
- **Dials** — `ZERO_PRESETS_M` **[50.0, 100.0, 200.0]** m; default `zero_dist_m` **100**; then default `hob_zero` **true** (SIM). Then **O** 50/100/200. Leftover `hob_zero` is sheet-shaped only after #76. **#78:** **−/=** step those presets
- **O** — then cycled live zero presets 50 → 100 → 200 → 50 (HoB solve). Shared across MP9-Z / SR-25 / M24 so G-swap does not hide the solve (`FeelSheet::cycle_zero`). **#78:** hold extract-check intent — **not** zero
- **P** — then arcade (aim-dir launch) ↔ sim (height-over-bore + ballistic zero) via `hob_zero` (`FeelSheet::toggle_hob_zero`). Shared launch mode across kits. **#76:** **P** unused (no new bind); `toggle_hob_zero` + session **P** apply gone; **P** no longer sets an input edge
- **Honesty** — changing zero preset changes muzzle **launch dir** only (not muzzle position). Then arcade vs sim launch dirs differed; sim aims up to meet sight zero; arcade launched along aim. **#76:** one SIM model (`solve_ballistic_launch` — not a precomputed bake). **#67** sits on top — hip fire uses `hip_honest_dir` (ads=0 on aim; ads=1 keeps this SIM solve). **#78:** **−/=** still changes the zero; it bites when aimed. **O** / **P** do not
- Toast: then `ZERO  {n} M` / `LAUNCH  ARCADE` / `LAUNCH  SIM` (age **1.2s**, `Slot::Cycle`). **#76:** `ZERO  {n} M` stays; `LAUNCH  ARCADE` / `LAUNCH  SIM` gone with **P**
- Glasses status strip (labels only, never a second ammo HUD): then `Z{zero_dist_m:.0}  SIM|ARCADE`. **#76:** `Z{n}  SIM` only (ARCADE dead) e.g. `Z100  SIM`
- Intact / do not steal: **[ ]** stay ToD clock; then **−/=** stay exposure. **#78:** **−/=** is zero; exposure keyboard unbound. **9/0** left free; does not steal T/C/R/Q/E/Z/B/V/N/U/`/F/X/H/1/2/3/G/Mouse4; tip→impact tracers / muzzle / sparks stay; reload / knife / bandage / lean / inspect / ToD stay seated
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust `FeelSheet::step_zero` (#78). `toggle_hob_zero` removed #76

## Closed by fulcrumRust #35 (2026-09-07)

- **Hold-J heat-tune dump** — Range Tech; hold **J** = heat-tune dump. **I** is no longer free — I is Augury stim (#37).
- **Feel** — sustained AUTO on the seated kit (`FeelState::try_heat_tune` / `fire_shot(..., heat_tune: true)`); uses kit `auto_interval_sec` while tuning (ignores SEMI hold gate)
- Recoil impulse + camera punch skipped; leftover LMB punch stomped while J is down (`recoil_punch` / `recoil_rot` / `cam_recoil_p` / `cam_recoil_y` zeroed) so the gun stays still
- Same cook path: `FeelState.barrel_energy` still climbs so the tip lattice feeds live dialing (no second heat cook). **#66** later made that lattice post input only — no world-pipeline orange card
- **Ammo dial cheat** — mag **still spends** while holding; **release refills** the seated mag via `DayOneKit::refill_mag` (tops stick to `smg_mag_size`, does **not** spend a reserve)
- Glasses: `HEAT TUNE` label only (amber-ish overlay) — never a second ammo HUD; must not count mag rounds
- Intact / do not steal: ToD **[ ]**/K/L/,/. · −/= zero (#78) · hold-O extract intent (#78) · lean Q/E · inspect ` · reload R · knife Mouse4/C · bandage T · P unused (#76) · I stim · Y host · O/P/T/C/R/Q/E/Z/B/V/N/U/`/F/X/H/G/I/Y/1/2/3/Mouse4
- Tests that define the lock: `heat_tune_climbs_energy_without_camera_punch`, `heat_tune_does_not_fight_tod_lean_inspect_reload_knife_bandage_zero`, `heat_tune_glasses_do_not_count_mag`, `j_is_heat_tune_hold_without_stealing_binds`
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust STEAL_MAP heat-tune row

## Closed by fulcrumRust #34 (2026-09-07)

- **Listen-server + invite stub** — Hypha; thin `std::net` UDP hub in `engine/src/net.rs` (MyceliumEngine had no portable net crate)
- **Host** — title **HOST** (or **Y** while alive in hideout/extract) binds UDP and mints `fulcrum://ip:port`; `--host` arms title cursor and also listens after Deploy
- Default port **7777** (`FULCRUM_PORT` override). LAN iface if OS has one, else loopback
- **Join** — `--join fulcrum://ip:port` (also bare `host:port` and `fw://`); env `FULCRUM_JOIN`. Title **JOIN** confirms. Then no in-game text field. **#83** adds in-pause **JOIN** panel (Esc → JOIN → type invite → Enter; title JOIN without `--join` opens the same sheet)
- Glasses labels only: `HOST  ip:port`, then `JOIN` / `PEER` after HELLO/WELCOME — never a second ammo HUD. **#83** keeps those labels
- Honesty: then handshake / presence only. **#83** adds UDP **POSE** presence (~20 Hz feet/yaw/pitch) — both machines still sim locally; **no** world replication / shoot/Locus/terrain/audio rewrite / PvEvP sim
- Solo **Deploy** unchanged (`net=off` on smoke)
- Intact / do not steal: **I** stim (#37), hold-**O** extract intent (#78), **−/=** zero (#78), **P** unused (#76), hold-**J** heat-tune (#35), T/C/R/Q/E/Z/B/V/N/U/`/F/M/1/2/3/Mouse4
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

- **Extract-yard scale harness** — Lab-Rat expanded the extract yard into a scale/perf harness for the #38 stamp/paint substrate. Stay on the extract yard for what #39 shipped — not a bigger world map on that pass. First big-map walk **landed #81**; stamp / harness pad stays **7×7**. No Standard / Monk one-off scars. HDRI stays Range Tech
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
- **Feel DNA** — Radiance RGBE decode → equirect sky/env (`engine/src/hdri.rs`). Same ToD sample still drives ambient / key / fill / fog / dome — **no XOR sky**. Plate yaw tracks the clock sun. Night fades the day plate back to the procedural dome (stars stay). Grimdark luma crush (`EXTRACT_SKY_LUMA` 0.20) keeps noon ashen. **#87** completed the HDRI sun disc: plate solar-region tone + dump **sunSize 0.62** soft disc (not a second sky).
- Hideout stays authored interior / unfogged.
- **/** toggles Goegap plate on/off — does **not** steal **M** (map). Existing ToD dials: **[ / ]** clock ±30 min · **K** dawn→noon→dusk→night · **L** live cycle · **, / .** clouds. Then **− / =** exposure. **#78:** **− / =** is zero; exposure keyboard unbound.
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
- **Options stub** — lists **Graphics / Audio / Gameplay / Controls**. Graphics/Gameplay/Controls were disabled `HYPHA` placeholders; **#46 filled those guts**. **Audio** still opens the live Range Tech #21 Voice/Music/FX mixer (persists). **#82** DEVICE row sits above the buses
- Audio overlay restyled to the same chrome; Esc Hypha pane / Audio → Options → title/pause
- Logo seat from #41 unchanged (vendored FoW header mark, `MARK_MAX_W` **1.70** / `MARK_MAX_H` **0.40** / `MARK_CENTER_Y` **0.58**)
- Not a second ammo HUD. Stays off atelier
- Peek: `cargo run` — framed title list under FoW mark; Options → Audio still nudges 0–2 / 100%; Esc backs one sheet at a time; in-game Esc → HOLD
- Detail: house `AESTHETIC_DIEGETIC_LOCK.md` / `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust STEAL_MAP Augury menu rows

## Closed by fulcrumRust #46 (2026-09-07)

- **Hypha Options guts** — filled the disabled `HYPHA` stub tabs on Augury’s #45 Options list. Not a second settings overlay. Title / HOLD / Options chrome + FoW logo seat stay Augury (#45/#41)
- **Graphics (live window + persist)** — Window mode live via winit: **Borderless** = default launch; **Windowed** = decorated 1280×720; **Exclusive** = exclusive video mode when OS/GPU expose one, else borderless fallback. Also `--windowed` / `FULCRUM_WINDOW=borderless|windowed|exclusive`. Post toggles persist (`project.json` / `FULCRUM_SETTINGS`) and must **not** be packed into Range Tech ToD / Goegap / HDRI uniforms: AO, AA, CA (+ strength default **0.35**, step **0.05**, range **0–1**), film grain, DoF. This peek they no-op'd; **#55** wired the GPU stack so they change the image. Hint then: `POST STUB UNTIL GPU · WINDOW LIVE · A/D NUDGE` (now `POST LIVE · AA ON`). **#86** adds thin live rows **FOG / FOG NEAR / FOG FAR / CAM NEAR / CAM FAR** on that same pane + persist (alongside Range `output_device`)
- **Gameplay (real)** — Glasses labels toggle + crosshair toggle (real — drop quads when off). Hint: `SHOOT FEEL STAYS · ENTER TOGGLE`
- **Controls** — Look scale sits on feel-lab sens: `LOOK_MUL` default **1.0**, min **0.25**, max **2.0**, step **0.05**; Invert Y toggle. Binds stay README. Hint: `LOOK SITS ON FEEL-LAB SENS · BINDS IN README`
- **Audio** — Untouched by #46 — Range Tech #21 Voice/Music/FX mixer. **#82** later added the DEVICE row on that same pane
- **Persist** — `project.json` in cwd, or `FULCRUM_SETTINGS=/path/to.json`
- **Esc walk** — Hypha pane / Audio → Options → title or HOLD (same stack as #45)
- Peek: `cargo run` → Options → Graphics window live; post toggles persist (GPU live **#55**); Gameplay glasses/crosshair; Controls look/invert; Esc backs; Audio still #21
- Ownership: Augury owns title + HOLD chrome + Options list shell + logo seat. Hypha owns Graphics/Gameplay/Controls guts + window mode + persist (**#46**); GPU post stack **#55**. Range Tech keeps Audio mixer. Still no second ammo HUD. No atelier push
- #46 remains guts/persist. GPU post stack that made toggles change the image is **#55**
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` / `AESTHETIC_DIEGETIC_LOCK.md` + fulcrumRust STEAL_MAP Hypha settings rows

## Closed by fulcrumRust #47 (2026-09-07)

- **Brass eject** — Range Tech leftover feel-lab FX on the same `TracerField`. Live fire from seated kit `ejectionPort`: `MP9Z_EJECT` **(0.036, −0.014, 0.018)** · `SR25_EJECT` **(0.038, 0.008, 0.018)** · `M24_EJECT` **(0.03, 0.018, 0.055)**. Camera-right toss; `CASING_GRAVITY` **12**; bounce then sleep; `CASING_FADE` **6** s; `MAX_CASINGS` **48**. Hide-not-despawn via `casing_draw_m` **55**. Hold-J heat-tune dump (#35) skips brass so the lattice stays still. **#79:** sleep Y + tracer ends + marks snap to extract heightfield / wall support — not a flat `floor_y` or pawn-feet plane. `first_hit` walls-only
- **Ricochet / spent slug** — feel-lab `trySpawnSpentSlugBounce` — **NOT** a bounce table. `SLUG_CHANCE` **1/16**; `SLUG_GRAZE_MAX` |n·vhat| ≤ **0.52** (dead-on still punches). Reflect incoming vel, keep 8–18% (`SLUG_KEEP_MIN`/`MAX` **0.08–0.18**); `SLUG_SPEED_MIN`/`MAX` **2.2–16**. Spent-slug visual `MAX_SLUGS` **24**; scuff mark instead of punch plug. Optional FX bus `Slot::Ricochet` ping at skip point
- **Richer impact geo** — punch vs scuff + `IMPACT_HOLE_VARIANTS` **10** + rim chips + stuck-slug plug (brass SMG / steel DMR+bolt). Rides existing spark/mark path — not a rebuild. **#89:** punch **8–12** sparks (0.22–0.40 s, 35% white) · scuff **4–6** amber (0.15–0.28 s) · 0.15 s hit-flash disc — was punch/scuff same 5–8 / 0.15–0.35 s, no hit flash
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
  - Jump land punch: none → then **0.052** rad overlay (does not write `pitch`). **#79** live punch **0.028** + inertia sway
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
- **Crossover shoulder / left-corner peek (H)** — authored hip +X ~**0.24** (right; live **#98** **0.2403 / −0.2128 / −0.1833** — ready hold, not chin-weld). **H** springs the **viewmodel** across the chest to a partial left (~**−0.041** X / ~**−0.181** Y, cap `shoulder_x_min` **−0.055**) — arms-limited, not a capsule/eye slide, not a full mirror, not infinite travel. Extra left probe (`shoulder_viewmodel` **0.12**) helps left-corner leans. ADS keeps **0.32** of the crossover. Viewmodel crossover on the existing H bind (FoW shoulder habit), not a new key. **#98** sits on #84 tilt path / #94 first +0.08: `shoulder_cross_x` **−0.281** / `shoulder_cross_y` **0.032**; left hold pitch/yaw/roll **0.04 / 0.10 / 0.08** (supersedes #84 chest-cross 0.08/0.32/0.39) — not a mesh mirror / no `scale.x = −1`. hip_low Y stays #94 **−0.2788**
- **Lean flip + deepen** — after #51 invert, **Q = peek right** (same side as inverted A), **E = peek left**. Eye formula stays `+lean → −flat_right`. Depth feel-lab **0.5 / 0.5** (`leanOffset` / `leanMax`), superseding #25 shallow 0.18/0.12. Wall clamp / spring / yard covers from #25 stay
- **CE hop + air hop + land overlay** — Evan supersedes #51 no-double. CE `JUMP_FORCE` **12** / `|GRAVITY|` **30**, one air hop **unchanged**. Same #59 hop — **not** a second land system. Then land duck **0.14 m** + shake **0.2** when impact > 8 + punch **0.052**. **#79** softener: punch **0.028** rad · duck **0.08 m** · shake **0.14** gate **13** (normal hop ~12 does not shake) · sway eye **0.014** / yaw **0.012** / roll **0.018** · decay **4.6**. Horizontal move must not eat `vel.y` (that was why the hop stayed shallow)
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
- Lab-Rat #58 quiet grit packs remain the near source; Hypha owns the mip chain. Whole roughness→stamp cook is **not** done (further Lab-Rat bake-downs still separate). Near LOD raise **landed #61** (subdivs **32/16/4**; grit mips stay 256/64/16). Live walk lock **landed #81**
- Detail: house `TERRAIN_NORTHSTAR.md` + `FULCRUMRUST_LAST_PASS_LOCK.md` + `STAMP_FEEL_LOCK.md` + fulcrumRust `engine/src/lod_mips.rs`

## Closed by fulcrumRust #61 (2026-09-08)

- **Near LOD raise** — Hypha. Bake-once Transvoxel subdivs **16/8/4 → 32/16/4**. [PR #61](https://github.com/initialvisuals/fulcrumRust/pull/61) (`5f52913d`). The A/B #43 deferred. Range Tech feel / Lab-Rat stamps / Augury brains stay; this PR does not fight them
- **Subdivs** — center **32** · ring-1 **16** · outer **4**. Near step stays **2:1** (32→16) so Lengyel transition faces still stitch toward finer neighbours. Outer stays coarse (4)
- **Grid / radius stay #43** — **7×7 / 3 Chebyshev rings / 112 m / 12 544 m²**. Extra far ring still cold
- **Grit mips stay #60** — **256² / 64² / 16²** on the same rings. Far still heightfield-only / cold guts
- Smoke: `terrain_tris=11118 lods=3 subdivs=32/16/4 near_chunk=3290 far_chunk=39 guts_warm=75 guts_cold=216 rings=3 extract_m2=12544 grit_mips=256/64/16 n=196608 f=768`. Far mean ~**84×** cheaper than near
- Parked: live LOD recook · tunnels · runtime carve. Live walk lock **landed #81**
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
- **Hip launch** — was SIM 100 m HoB from a right-low hip muzzle → close-range **up + right** of the reticle. Now `hip_honest_dir`: ads=0 stays on **aim**; ads=1 keeps the SIM HoB/zero solve. Uses existing ADS↔hip weight. Not a new cone. **#78:** **−/=** still changes the zero; it bites when aimed. **O** is extract intent. **#76:** **P** unused — no arcade dir
- **Streak** — was `tracer_len` (0.55 m) used as a **receiver skip**; then a 10 m box drawn backward through the gun. Now spawn **on the tip**. `tracer_len` is length again. Back of the streak clamped to the tip (feel-lab tip→impact). Distant speed scale kept once the slug is past the gun
- Intact: **−/=** HoB zero (#78; was **O** #33; **#76** SIM-only — **P** unused); tracers-until-impact + FX `hit` (#59). This PR did **not** ship heat color and did **not** fight Hypha #66 (colorless post warp **landed #66**). Lab-Rat terrain untouched. Profile/stash/MP/hands/inventory still open
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
- **O** — then still cycled 50 / 100 / 200 m zero presets (`FeelSheet::cycle_zero`). Shared across kits. **#78:** hold extract intent — not zero; **−/=** steps those presets
- **Bake** — not a precomputed trajectory. `solve_ballistic_launch` stays the feel-lab low-arc solve so shots share one deterministic model
- **#67 hip honesty stays** — `hip_honest_dir`: ads=0 on aim; ads=1 keeps this SIM solve. Per-kit recoil / `yaw_walk` stay (MP9-Z kick 1.0 · SR-25 1.15 · M24 1.75 + distinct walks)
- Toast / glasses: `ZERO  {n} M` stays; `LAUNCH  ARCADE` / `LAUNCH  SIM` gone. Glasses `Z{n}  SIM` only — never `ARCADE`
- Intact: #67 hip honesty · per-kit recoil cones · **−/=** zero (#78) · #59 tracers-until-impact. Do **not** invent a new bind for **P**
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust `muzzle_and_launch` / `solve_ballistic_launch`

## Closed by fulcrumRust #78 (2026-09-09)

- **Hold-O extract / −/= zero / grounded slide** — Range Tech. Patch A input/move trio on #76 SIM-only. [PR #78](https://github.com/initialvisuals/fulcrumRust/pull/78) (`e86bfa79`). Seat: **Range Tech** owns hold-O raid intent flag, **−/=** zero, grounded slide gate. **The Augury** EXTRACT elbow card **landed #85** (no popup). Full hatch popup (elevator / toggle / timed kill) still **~**
- **Hold O** — raid-only `Session::extract_checking`. **O is not zero.** Hideout is a no-op. Augury EXTRACT elbow card **landed #85** (no popup); hatch elevator / toggle / timed kill still **~**
- **− / =** — step zero down / up 50 / 100 / 200 m wrap (`FeelSheet::step_zero`). Replaces O cycling. Shared across MP9-Z / SR-25 / M24
- **Exposure keyboard** — unbound (no second pair; do not invent one). Sky `nudge_exposure` may still exist for leftover edges
- **Kill float-slide** — existing slide start is now **grounded only**. Midair Shift+Ctrl cannot zero `vel.y` / hover. Grounded sprint→crouch slide still works
- Intact: #76 SIM-only · **P** unused · one HoB + gravity / zero model · #67 hip honesty · **[ / ]** ToD · **, / .** clouds · **/** HDRI. Do **not** reopen arcade/**P**, heat color, `dBXpg`. First big-map host **landed #81**
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust `Session::extract_checking` / `FeelSheet::step_zero`

## Closed by fulcrumRust #79 (2026-09-09)

- **Landing sway softener + heightfield-grounded FX** — Range Tech. Same #59 hop overlay — **not** a second land system. [PR #79](https://github.com/initialvisuals/fulcrumRust/pull/79) (`fc6fb9a7` / `dfd04821`). Seat: **Range Tech** owns land overlay soften + heightfield ground FX. Hop DNA stays CE `JUMP_FORCE` **12** / `|GRAVITY|` **30** / one air hop
- **Land overlay** — punch **0.028** rad (was 0.052) · duck **0.08 m** (was 0.14) · shake **0.14** gate **13** (was 0.20 / 8; normal hop ~12 does not shake) · sway eye **0.014** / yaw **0.012** / roll **0.018** at walk × impact · decay **4.6**. Procedural inertia from horizontal vel / move dir, scaled by impact. Yaw overlay does not write `yaw`
- **Heightfield FX** — brass / tracers / impacts snap to extract `World::surface_height(x,z)` / wall support AABB tops (hideout stays y=0). Tracer ends + marks flush via cheap slope normal. `first_hit` is **walls-only** — no phantom y=0 slab. Ground belongs to the heightfield
- **AXIS_LOCK** — sim barrel **+Z** for FX orientation unchanged; toss still camera-right
- Intact: hop 12/30/1 · #78 hold-O / −/= / grounded slide · #76 SIM-only · **P** unused · Augury EXTRACT elbow card **landed #85** (no popup); full hatch popup still **~**. Do **not** claim a second land system or full extract popup. First big-map host **landed #81** (this PR did not ship it)
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust `engine/src/feel.rs` / `engine/src/tracers.rs`

## Closed by fulcrumRust #80 (2026-09-09)

- **Slope/PBR + dirt/scatter/deform plugs** — Lab-Rat. Fills Hypha reserved `StampKind::Deform` / `GroundScatter` + `HookKind::LabRatDeform` / `LabRatScatter` at the same XZ as #81. [PR #80](https://github.com/initialvisuals/fulcrumRust/pull/80) (`2cda73bc`). Seat: **Lab-Rat**. Hypha #81 still owns vertex COL bind. NRM/GLOSS GPU parked
- **Slope/angle** — `classify_slope` tags dirt / sand / rock / concrete / organic on the stamp pad
- **PBR bake-down** — 256² greyscale DISP crops + 64² COL/NRM thumbs in `assets/stamps/` (CliffJagged / GroundClay / ConcreteWall / GroundMoss — not 4k 48-bit)
- **COL hooks Hypha can consume** — `pbr::ColHook` / `col_png` / `hypha_col_alias`. Lab-Rat does **not** own vertex COL bind
- **Stamp pad** — stays **7×7**. Hypha 19×19 walk consumes `sample_channels` only
- **Dial sheet:**

| Dial | Value |
|------|--------|
| `PBR_HEIGHT_AMP` | **0.028** m |
| `SCATTER_AMP` | **0.018** m |
| `STAMP_PAD_HALF_M` | **56** m |
| `DEFORM_XZ` / r | `8, -6` / **5** m |
| `SCATTER_XZ` / r | `-10, 14` / **6** m |
| Load | vendored; `FULCRUM_GRIT` then `FULCRUM_ATELIER` (read-only) |

- **Smoke** — `pbr=tint plugs=slope+deform+scatter` + Hypha `gfx=`
- Intact: #81 host / vertex COL · stamp pad 7×7 · #58/#60 grit. Do **not** claim NRM/GLOSS GPU bind · Hypha vertex COL as Lab-Rat · whole roughness→stamp (SVG / density-mask / experiment-log still open) · Range / Augury / Beabim / biped / Graphics dump
- Detail: house `STAMP_FEEL_LOCK.md` + `TERRAIN_NORTHSTAR.md` + `FULCRUMRUST_LAST_PASS_LOCK.md`

## Closed by fulcrumRust #81 (2026-09-09)

- **19×19 open extract + chunk stream + slope COL hooks** — Hypha. First true big map. [PR #81](https://github.com/initialvisuals/fulcrumRust/pull/81) (`73dc8fe4`). Seat: **Hypha** owns host / stream / slope COL. Lab-Rat deform/scatter identity hooks were reserved here — **filled later #80**. Continues parked draft #63 (closed). Rebased onto #79 land sway + heightfield FX
- **Extract** — **19×19 / 304 m / 92 416 m²** (~8× old 7×7). Walls **off** — open horizon, soft XZ clamp
- **Stream** — **9×9** window (`STREAM_RINGS` 4) by player eyes. Stamp pad still **7×7** / far-cold (#23 guts cold)
- **Underfoot LOD** — **32 / 16 / 8 / 4** — every adjacent step **2:1** (was 32/16/4; 16→4 was opening voxel gaps)
- **PBR** — slope COL hooks (`pbr=tint` default). Vertex albedo only. NRM/GLOSS parked
- **Lab-Rat** — `Deform` / `GroundScatter` + `LabRatDeform` / `LabRatScatter` identity reserved here. **Filled later #80** (DISP bake-down + deform/scatter stamps)
- **Seams Patch A** (dark-pad → hills): one extract density on every LOD (ChannelField vs HeightOnly disagreement fixed) · 8-subdiv bridge so 32→16→8→4 stays 2:1 Lengyel · yard flatten outer **9.2 → 20 m** so pad eases into hills. Residual LOD pop inside a chunk / far-4 horizon still parked
- **Smoke** — `subdivs=32/16/8/4` `extract_m2=92416` `resident=` `stream_cold=` `pbr=`
- Intact: #79 land sway + heightfield FX · #16/#23/#43/#60/#61 prior facts. Do **not** claim NRM-GLOSS GPU / world replication / Range heat as this PR. Lab-Rat plugs **landed later #80**. Peer feet `stream_anchors` **landed later #83** (coordinate only — no Transvoxel rewrite)
- Not touched: Range heat cards · ballistics · binds · Augury chrome
- Detail: house `TERRAIN_NORTHSTAR.md` + `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust `docs/TERRAIN.md`

## Closed by fulcrumRust #82 (2026-09-09)

- **Options Audio output DEVICE** — Range Tech. Explicit host-output pick; audio still follows OS default unless cycled. [PR #82](https://github.com/initialvisuals/fulcrumRust/pull/82) (`12676383`). Seat: **Range Tech** owns DEVICE + mixer. Augury still owns spatial/reverb. Hypha still owns Options Graphics post. No heat / terrain / Beabim / Augury labels / CE projectiles
- **Row** — Options **Audio** `DEVICE` (cursor 0, above Voice / Music / FX). Bus dials unchanged (0–2 / 100%)
- **Default** — **SYSTEM DEFAULT** via cpal `default_output_device()` (Windows / OS default)
- **Cycle** — A/D or arrows; Enter / click also steps (same DNA as Graphics **WINDOW**)
- **Persist** — `output_device` in `project.json` (empty / `default` / `system` = OS default)
- **Missing pick** — keep the pin; playback falls back to OS default
- **Route** — same #21 mixer stereo render → thin cpal voice (oneshots + Music-bed loop). **Not** a second mix tree
- **Hear it** — UI tick plays on the newly selected device
- **Code** — `engine/src/audio_out.rs` (cpal enumerate + stream; Stream on window thread — not Sync) + Options Audio DEVICE row
- Intact: #21 Voice/Music/FX · #54/#62 file slots · #64 playlist · #27/#56 spatial+reverb · #81 host. Do **not** claim a second mixer, Augury spatial rewrite, or Hypha Graphics post
- Detail: house `EXTRACTION_AUDIO_LOCK.md` + `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust `engine/src/audio_out.rs`

## Closed by fulcrumRust #84 (2026-09-09)

- **H shoulder-swap tilt** — Range Tech. Preferred hand / shoulder swap reads as a real tilt across the chest, not a left-right mesh mirror. [PR #84](https://github.com/initialvisuals/fulcrumRust/pull/84) (`7d7e18f5`). Seat: **Range Tech** owns H tilt on existing ViewmodelDials / ADS cant DNA. Travel stays **#59**. PreferredHand + new-profile onboard stays **parked** house/Hypha
- **Travel (unchanged)** — `shoulder_cross_x / y / z` hip +X ~**0.10** → ~**−0.041** · `shoulder_x_min` **−0.055** (arms-limited; not a full left park) · `shoulder_ads_keep` **0.32** · `shoulder_spring` **8.0** · `shoulder_viewmodel` **0.12**
- **Tilt (new)** — `shoulder_cross_pitch` **0.08** (chest-cross lift; ADS cant 0.02 / hip cant 0.0365 DNA) · `shoulder_cross_yaw` **0.16 → 0.32** (inward yaw that reads) · `shoulder_cross_roll` **0.10 → 0.39** (half of U-cycle / ADS cant 0.785)
- **Path** — same `apply_shoulder_crossover` → `PoseOffset` → `pose_basis` as ADS/hip cant. No second viewmodel system
- **Not** — a capsule/eye slide · a mesh mirror · `scale.x = −1` / mirrored kit boxes. Kit boxes stay authored positive; ejection stays gun-right
- Intact: #59 travel · #82 DEVICE · #81 host · #79 land sway. Do **not** claim PreferredHand / new-profile onboard shipped
- Live hip / `shoulder_cross` / left tilt **superseded #98** (after #94 first +0.08) — hip **0.2403 / −0.2128 / −0.1833**; `shoulder_cross_x` **−0.281** / `shoulder_cross_y` **0.032**; pitch/yaw/roll **0.04 / 0.10 / 0.08** (slight straighten, not chest-cross cant). hip_low Y stays #94 **−0.2788**. See Closed by #98
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust `apply_shoulder_crossover` / ViewmodelDials

## Closed by fulcrumRust #86 (2026-09-09)

- **Hypha Graphics dump** — steal Evan’s aim-offset Settings Lighting dump onto existing fulcrumRust Graphics / post / sky dials after #81 19×19 open extract. [PR #86](https://github.com/initialvisuals/fulcrumRust/pull/86) (`13865b3f`). Seat: **Hypha** owns Options Graphics / sky / post defaults. Thin Options rows only where the render path already supported the value: **FOG / FOG NEAR / FOG FAR / CAM NEAR / CAM FAR**. Persist `project.json` alongside Range `output_device`
- **Dial sheet:**

| Dump key | Value | Path |
|----------|--------|------|
| fogEnabled | true | Options **FOG** + extract `haze_max` (hideout stays **0**) |
| fogNear / fogFar | **375 / 520** | Options + `LightingFrame` haze start/range (was 16 / 48) |
| lightAmbMul | **0.11** | already `sky::AMB_MUL` |
| lightFillMul | **0.41** | already `sky::FILL_MUL` |
| lightHemiMul | **0.61** | already `sky::HEMI_MUL` |
| lightKeyMul | **2.11** | already `sky::KEY_MUL` |
| lightRimMul | **1.65** | already `sky::RIM_MUL` |
| lightMoonMul | **1.06** | already `sky::MOON_MUL` |
| exposureMul | **1.44** | already `sky::EXPOSURE_MUL` |
| sunPunch | **0.51** | existing sky disc/halo (`sun_dir.w`) |
| clouds | **0.63** | `SkyState` default (was 0; **,** / **.** still nudge) |
| skyHdri | true | already default; **/** still toggles |
| camNear / camFar | **0.05 / 2000** | Options + `perspective_rh` / post linear-Z (was 0.06 / 280) |
| adsDofTaps / adsDofRadius | **12 / 0.0048** | already **#68** |

- **Parked on purpose (no path / do not invent):** bloom **0.08** · godRays **2** · brightness / gamma **1 / 1** — no existing GPU path. **sunSize 0.62** was parked here — **#87** now rides the sky disc. Heat haze dials — Range **#71** owns those. HDRI sun black-out / blow-out **completed #87** (shared Range Tech + Hypha)
- **Ownership:** Hypha Options Graphics / sky / post defaults. Range heat / binds / ballistics / Audio DEVICE stay Range. Lab-Rat stamps. Augury chrome untouched (Hypha only fills the Graphics list)
- Intact: #55 GPU post stack · #68 ADS DoF · #71 heat haze · #81 host · #82 DEVICE · #84 H tilt. Exposure keyboard still unbound after **#78**. **,** / **.** clouds still work. **/** HDRI toggle stays. Do **not** invent bloom / god-ray / brightness / gamma paths. sunSize is **no longer parked** — see Closed by #87. Do **not** claim Range Audio DEVICE / H tilt / terrain / stamps as this PR
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` / `AESTHETIC_DIEGETIC_LOCK.md` + fulcrumRust `engine/src/sky.rs` / Options Graphics. HDRI sun disc **#87**

## Closed by fulcrumRust #85 (2026-09-09)

- **Diegetic elbow smart-labels** — Augury. Thin white analysis-knowledge-core card + **L-elbow / leader** to the world interact pin (door, loot, hatch, shaft, weapon, extract plots, Locus). [PR #85](https://github.com/initialvisuals/fulcrumRust/pull/85) (`f3d60a24`). Seat: **The Augury** owns glasses EXTRACT chrome + interact cards. Range #78 already wired `Session::extract_checking`. Not a centered HUD plate (old `-0.34, -0.268` retired)
- **`engine/src/labels.rs`** — `SmartLabel` / `CardPlan`: L-elbow leader, tip mark, quiet angular junk, curl/Locus edge tints. EXTRACT stays white mono
- **Hold-O** — paints `EXTRACT` intent on the nearest in-front hatch/shaft — elbow card, **no popup**. Release clears
- **World** — `ExtractHatch` / `ExtractShaft` interacts. Hatches stay on the **yard pad** (`-24/-24`, `18/-28`, `-28/16` + shaft `18/-12`), not GRID_ORIGIN (19×19 rim)
- **Status strip** — PLACE / clock / INSPECT / … unchanged. No second ammo HUD
- Intact: #78 hold-O intent · #81 host · #82 DEVICE · #84 H tilt · #86 Graphics dump. Do **not** claim full hatch popup / elevator / toggle / timed surface kill shipped. Do **not** claim Range Tech / Hypha / Lab-Rat work as this PR
- Detail: house `AESTHETIC_DIEGETIC_LOCK.md` / `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust `engine/src/labels.rs`

## Closed by fulcrumRust #87 (2026-09-09)

- **HDRI sun black-out / blow-out** — Goegap plate solar-region tone + soft disc; not a second sky. Same ToD sample still lights dome + plate. [PR #87](https://github.com/initialvisuals/fulcrumRust/pull/87) (`5f2577d6`). Seat: **Range Tech + Hypha** on the #86 dump base. Ledger: HDRI sun **·→X**
- **Plate solar-region tone** — sky keeps grimdark Reinhard × **0.20**; solar texels use white-point **8 × 0.55** with knee-compress so bilinear / f16 cannot spike Inf. Was: Reinhard w=1 × 0.20 everywhere (~0.21 hole)
- **Disc energy** — dump **sunSize 0.62** (parked in #86) now drives disc/halo exponents (`mix(1800, 80)`). HDRI live complements: disc **0.55 / 0.18** (was 1.8 × `(1 − hdri×0.55)` / `pow(dot, 1400)` needle)
- **Local shoulder** after exposure — core stays in ~(0.12, 0.95); shoulder asymptote **0.95** + clamp **0.96**. Global **exposureMul 1.44** / **sunPunch 0.51** unchanged
- **#86 dump dials stay** — fogNear/Far **375 / 520** · lightKeyMul **2.11** (other light*Mul stay) · exposureMul **1.44** · clouds **0.63** · sunPunch **0.51** · skyHdri **true** (/** still toggles) · camNear/Far **0.05 / 2000**. bloom / godRays still no path. brightness / gamma still no path. sunSize is **no longer parked** — it rides the sky disc
- Intact: #86 fog / cam / light*Mul / clouds · #40 Goegap plate · #24 ToD sample · **/** HDRI toggle. Do **not** invent bloom / god-rays or a second sky. Do **not** claim Range heat / Augury chrome / Lab-Rat stamps as this PR
- Smoke: `gfx=fog/375/520 cam=0.05/2000 clouds=0.63 punch=0.51 size=0.62`
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` / `AESTHETIC_DIEGETIC_LOCK.md` + fulcrumRust `engine/src/sky.rs` / `engine/src/hdri.rs`

## Closed by fulcrumRust #83 (2026-09-09)

- **Two-instance pose sync + in-pause JOIN panel** — Beabim. MP sync specialist (listen-server / two-instance sync / join panel / live-profile loot trail). Flips #34 handshake-only + "no in-game text field" + parked listen-server peer pos. [PR #83](https://github.com/initialvisuals/fulcrumRust/pull/83) (`24eaca4b`). Hypha #34 stays the UDP hub / HELLO/WELCOME / **Y**-host / `--join` foundation
- **POSE** — UDP after HELLO/WELCOME (~20 Hz): feet `xyz`, yaw, pitch, grounded, crouch. Host assigns peer ids on WELCOME and relays poses
- **Silhouette** — cheap **5-box** operator (slate) — not Mixamo / not Locus. **Not** full 3P kit honesty — 1P viewmodel ≠ 3P biped + weapons + gear (holding / locked intent; Beabim 3P gun path still **open**)
- **Grounded Y** — rides the **#81 19×19 heightfield** (Range #79 snap DNA). Packet Y ignored when grounded — no phantom `y=0` slab, no floating on a lie. Airborne hops keep networked Y
- **Stream anchors** — #81 `stream_anchors` now returns remote feet so the **9×9** window can follow a peer (coordinate only — no Transvoxel rewrite)
- **Glasses** — still `HOST` / `JOIN` / `PEER` labels only — never a second ammo HUD
- **HOLD JOIN** — Esc → **JOIN** → type `fulcrum://ip:port` / `fw://` / bare `ip:port` / `localhost` → Enter. No app restart. Title **JOIN** without `--join` opens the same sheet. `--join` / `FULCRUM_JOIN` still one-click
- Default port **7777** (`FULCRUM_PORT` override) stays
- Binds: **Y** host (alive), **I** stim, hold-**O** extract untouched
- **Still local (deliberately):** shoot / HoB / heat / brass / land feel / H tilt (#84) / audio device (#82) / Graphics dump (#86) / HDRI sun (#87) / Locus brains + yard stamps / COL / deform / scatter (#80) / Transvoxel rewrite / Augury elbow / hatch UX (#85) / world seed / ToD / drops. **No** world replication / PvEvP sim / Mixamo player body
- Intact / do not steal: **I** stim (#37) · hold-**O** extract (#78 / #85 elbow) · **−/=** zero (#78) · **P** unused (#76) · hold-**J** heat-tune (#35)
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust STEAL_MAP Net row

## Closed by fulcrumRust #88 (2026-09-09)

- **Biped foot plant / terrain follow** — Hypha. Cube stubs were pinned to y=0 (floated on pad, walked into Transvoxel hills). Steals the existing Range #79 heightfield column — not a mesher rewrite. [PR #88](https://github.com/initialvisuals/fulcrumRust/pull/88) (`78e11990`). Seat: **Hypha** owns plant / ride / Mixamo host hooks. Augury brains stay. Beabim #83 packet / handshake / HOLD join stay
- **`engine/src/plant.rs`** — samples `World::surface_height` → `TerrainHost::height_at` + `support_surface_y` (wall tops). Pelvis + left/right boot XZ. Soft follow = Mycelium `ride_spring` / foot-plant DNA at cube-stub scale — **not** Mixamo clips, **not** 2-bone IK
- **Locus** — `step` no longer writes `pos.y = 0`. Extract `tick_loci` calls `tick_on` with the heightfield; hideout / unit tests keep flat-floor `tick`
- **Soles** — sit on root Y (boot center was 0.18 → **0.11** / ~7 cm stub float fixed)
- **Dummy + #83 peers** — grounded silhouettes use `biped::plant_simple_root` (same column)
- **Thin Mixamo host hooks** — `engine/src/biped.rs`: greybox sockets Pelvis / Foot_L / Foot_R / Head + planted `BipedRoot`. Form-check solids for tests only — not a second yard enemy, not GPU skin, not Augury brains
- **Dial sheet:**

| Dial | Now | Unit | Note |
|------|-----|------|------|
| root Y | heightfield column | m | pelvis + each boot, mean of feet |
| FOLLOW | **8.5** | 1/s | Mycelium `IK_BLEND_RATE` 8, quieter for boxes |
| DEADZONE | **0.04** | m | ignore micro hunt |
| RISE_RATE | **2.2** | m/s | climb without popping through mesh |
| SINK_RATE | **6.5** | m/s | catch the column — no midair hang |
| SNAP_ERR | **1.15** | m | first plant snaps; later only a large *down* error snaps |
| LIFT_MAX | **0.14** | m | per-boot slope offset; no FBIK |
| BOOT_HALF_H | center **0.11** | m | sole on root Y (was center 0.18) |
| Mixamo sockets | Pelvis / Foot_L / Foot_R / Head | | host hooks only |

- **Ledger** — A-notes `[·] enemies walk into terrain` → **X**. STEAL_MAP biped **todo → partial** (plant + host hooks; Mixamo / player body / 2-bone IK / GPU skin still parked)
- Intact: #79 heightfield FX · #81 Transvoxel host · #83 packet / handshake / HOLD join. Mesher / LOD / stamps untouched. Do **not** claim Mixamo clip import / GPU skin / player body / 2-bone IK / mesher rewrite / Range shoot/feel/heat/binds / Lab-Rat #80 plugs / Beabim net rewrite / HDRI sun
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust `engine/src/plant.rs` / `engine/src/biped.rs`

## Closed by fulcrumRust #89 (2026-09-09)

- **Projectile feel toward CE gold** — Range Tech. Deepens visuals and feel on existing `TracerField` — trail, hit flash, punch vs scuff, flight readability — **without rewriting ballistics**. [PR #89](https://github.com/initialvisuals/fulcrumRust/pull/89) (`a3e28ec0`). Seat: **Range Tech**. Ledger: `[·] projectiles from CE (Range Tech)` → **X**. SIM-only #76 stays. Private DNA: FoW / feel-lab projectile feel + Evan’s Vector mag-dump frame. Public shelf stays feel-lab style
- **Muzzle** — long yellowish-white **rectangular slab** on the can tip (`half.z` ≫ `half.x`) + pale-yellow rim flush on the tip (not a round `splat(0.018)` + 3 petals). 4–6 orange debris sparks, life 0.07–0.17 s. Rim shares the can-tip back plane (no bleed into the receiver)
- **Flight** — hot slug head `TRACER_SLUG_LEN` **0.07** m + core **2.85 / 2.25 / 0.95** + 1–2 fading wake segments, tip-clamped. visualLength floor **max(1.5, speed×0.035)** / cap **18** m (was authored 0.55 / 10 m)
- **Impact** — 0.15 s hit-flash disc (grows 0.5→2.5, fade `1−√t`). Punch **8–12** sparks (0.22–0.40 s, 35% white). Scuff **4–6** amber (0.15–0.28 s). Marks / stuck-slug / ricochet DNA stay
- **Glyphs** — same receiver LED wells **fire pulse** red/orange on dump (`fire_glow`). Hold-R peek unchanged. Not a HUD
- **Unchanged** — SIM launch / HoB / gravity (#76) · AXIS_LOCK sim barrel **+Z** / #79 heightfield snap · HeatDials / haze (#71 blend). CE tip **0.2.8** preferred if a later cook retunes muzzle-adjacent haze — **not** a heat-card rewrite
- Intact: #67 kit-tip spawn · #76 SIM-only · #71 heat blend · #79 snap · #12/#19/#47/#59 tracer field. Do **not** claim heat-card rewrite, terrain #80, Beabim sync, profile onboard, Augury hatch/labels, Aim-offset Home debugger, kit mesh rewrite, or pixellation/grit (FoW/Hypha)
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` Visible shot feedback + `VECTOR_MAG_DUMP.md` + fulcrumRust `engine/src/tracers.rs`

## Closed by fulcrumRust #94 (2026-09-09)

- **Patch A RH hip bias** — Range Tech. RH barrel was reading left of center on a pillar. Position-only +0.08 past a first +0.04 pass — no inward yaw to fake aim. [PR #94](https://github.com/initialvisuals/fulcrumRust/pull/94) (`a3a42e4f`). Seat: **Range Tech**. Ledger: Patch A RH hip row → **X**. H travel deepened by the same +0.08 so left dest stays ~−0.041. Left hold is a slight yaw/roll straighten (not a mesh flip, not the old #84 chest-cross cant)
- **Hip X (now)** — MP9-Z hip / hip_low **0.1843** (+0.08 from 0.1043) · hip_cant **0.2193** · sprint_high **0.29**. SR-25 hip / hip_low **0.20** · hip_cant / sprint_high **0.235 / 0.30**. M24 hip / hip_low **0.205** · hip_cant / sprint_high **0.24 / 0.31**
- **H travel** — `shoulder_cross_x` **−0.145 → −0.225** (keeps dest ~**−0.041**) · `shoulder_x_min` **−0.055** unchanged · ads_keep **0.32**
- **Left hold** — pitch/yaw/roll **0.04 / 0.10 / 0.08** (slight lift / inward / straighten). Supersedes #84 chest-cross **0.08 / 0.32 / 0.39**
- **Unchanged** — ADS hold X (iron / holo / acog / sniper / cant) stay feel-lab bore-center · inspect X **0.0593** · tip spawn + `hip_honest_dir` · #89 tracers / particles · no `scale.x = −1`
- Intact: #59 travel DNA · #67 tip spawn · #84 tilt path · #89 projectiles. Live **End** tuner on these same dials **later landed #97**. Live hip / ready-Y **superseded #98**. Do **not** claim kit mesh rewrite, heat, audio, Beabim, PreferredHand onboard, or Augury Home tabs/logger as #94
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust `ViewmodelDials` / `apply_shoulder_crossover`

## Closed by fulcrumRust #97 (2026-09-09)

- **Aim-offset tuner + attachment sockets** — Range Tech. Live **End** sheet on existing `ViewmodelDials` + `AttachmentOffsets` (optic / can from authored `kit_mesh` sockets). Identity PoseOffset = live authored mounts (**#98** after the body-width + ready-Y pass; was #94 when #97 shipped). [PR #97](https://github.com/initialvisuals/fulcrumRust/pull/97) (`6908ec88` / `8ac9130b`). Seat: **Range Tech**. Ledger: Patch A tuner row → **X** (A-notes `~` / parked `·` stale). Home stays unbound — Augury (#95 tip). Not Home chrome, not hitch logger, not EffectComposer, not a second pose system
- **Binds** — **End** toggle (feel-lab Home remapped like X→Z) · Insert WEAPON ↔ ATTACH · PageDown pose / attachment target · PageUp step cycle · ↑↓ select axis · ←→ / num± nudge · Delete paste-ready JSON (feel-lab `example_smg` object + attachments)
- **Steps** — MICRO pos **0.0005** / rot **0.001** · FINE (default) **0.002** / **0.005** · MED **0.01** / **0.02** · COARSE **0.05** / **0.1**. Axis rows PX PY PZ RX RY RZ
- **Authored defaults now #98** — MP9-Z hip **0.2403 / −0.2128 / −0.1833** · ADS iron X **0.0084** (bore-center) · SR-25 / M24 hip **0.256 / −0.224 / −0.208** / **0.261 / −0.229 / −0.228**. H travel / slight straighten stay; `shoulder_cross_x` **−0.281** / `shoulder_cross_y` **0.032**. Tuner writes the same dials — #97 still live for fine polish on these #98 defaults
- **Follow** — kit boxes + muzzle tip follow live can/optic offsets. World drops stay authored identity. Glasses `AIM TUNE`
- Intact: #98 RH hip / H dials (was #94 when this PR shipped) · #67 tip spawn · #89 tracers. Do **not** claim Augury Home tabs/logger · EffectComposer · Beabim · Heat rewrite · Terrain · mesh mirror / `scale.x = −1` · PreferredHand onboard · ballistics / SIM / #76 · #89 tracers · Audio DEVICE
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust `AimTuner` / `ViewmodelDials` / `AttachmentOffsets`

## Closed by fulcrumRust #98 (2026-09-09)

- **RH hip one more body-width + ready-hip Y** — Range Tech. After #94 +0.08, RH hip needed one more gun-body width further right so the *lateral* angle matches left hold, slightly tighter. Default HIP was reading like a chest/chin shoulder-weld; dropped Y so main HIP is a ready hold, not parade-rest under the chin. [PR #98](https://github.com/initialvisuals/fulcrumRust/pull/98) (`48518709` / `5b02e2ab`). Seat: **Range Tech**. Dial-only `ViewmodelDials` hip-family + `shoulder_cross`. No new shotgun low-hip pose — `hip_low` Y stays the #94 U-cycle low stance
- **Hip (now)** — MP9-Z hip **0.2403 / −0.2128 / −0.1833** (+0.056 X = 2 × MP9 `receiver_half.x` **0.028** / polymer shell **0.056**; Y **−0.044** ready-hip drop; Z **+0.012** tighter). `hip_low` **0.2403 / −0.2788 / −0.1633** (Y stays #94 **−0.2788**; +X/+Z only). `hip_cant` **0.2753 / −0.1938 / −0.1983** (Y stays; +X/+Z only). `sprint_high` X **0.29 → 0.346** (X only). SR-25 hip **0.256 / −0.224 / −0.208**. M24 hip **0.261 / −0.229 / −0.228**
- **H travel** — `shoulder_cross_x` **−0.225 → −0.281** (keeps dest X ~**−0.041**) · `shoulder_cross_y` **−0.012 → 0.032** (keeps dest Y ~**−0.181** after the RH drop) · `shoulder_x_min` **−0.055** unchanged · ads_keep **0.32**
- **Unchanged** — ADS hold X (bore-center) · left pitch/yaw/roll **0.04 / 0.10 / 0.08** (gold vertical) · inspect X **0.0593** · tip spawn + `hip_honest_dir` · #89 tracers / particles · no `scale.x = −1`
- Intact: #94 first +0.08 · #97 End tuner (still live — authored defaults are now #98) · #59 travel DNA · #67 tip spawn · #84 tilt path · #89 projectiles. Do **not** claim mesh flip, Beabim, heat, terrain, new low-hip/shotgun pose, or PreferredHand onboard as #98
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust `ViewmodelDials` / `apply_shoulder_crossover`

## Holding / locked intent — 1P viewmodel ≠ 3P biped gun (MP honesty)

Evan lock (2026-09-09 InitialVisuals). **Holding / locked intent — not shipped.** Overnight cooks steal from `FULCRUMRUST_LAST_PASS_LOCK.md`. Goes with HANDS down the road.

- **Closed (intent):** 1P weapon viewmodel ≠ MP biped + weapons + gear. Fake / artistic posing (hip fire sold for feel, canted CQC, etc.) can stay **aggressive on the first-person viewmodel**. Other players must **not** see guns sticking through eyeballs for "artistic merit"
- **Open (path):** Beabim 3P gun / gear on the peer mesh. Do **not** claim #83 5-box silhouette is full 3P kit honesty

| Seat | Owns |
|------|------|
| **Range Tech** | 1P dials / AIM TUNE (#97 End sheet) |
| **Beabim** | 3P sync path for peer mesh honesty |
| **Lab-Rat** | Stamps stay out |

## Holding — greyscale glass + Evan asset-ask (2026-09-09)

Evan lock from Initial Visuals (2026-09-09). **Not shipped.** Overnight cooks steal from this shelf + `FULCRUMRUST_LAST_PASS_LOCK.md` — not chat scroll. Do **not** claim LPVO or glass live.

### Scope glass (when LPVO lands)

Hypha Graphics owns the glass shader **when LPVO**. Range Tech seats AIM TUNE placements first (#97 End sheet).

- Greyscale / black-and-white ramp — **not** a color ramp
- Fake curve of the glass + thickness; cut lines or flatten parts (Blender-style)
- IOR glass + ramp-driven magnify
- Bodycam optic shader: **no PiP** — glass / radial / reflect in the **scope pass**
- Live **V** iron/holo/acog + FOV stay #14/#22. Current hoods stay boxes

### Asset ask path

- Clone from Concrete Echo / aim-offset **attachment tables** first
- If missing: **ask Evan** — he has **this week** (from 2026-09-09) to model + texture; primitives stay scaffolding
- Style grows with peeks (void-spore + grit floor; authored fills in)
- Lab-Rat stamps keep **procedural grit** until the asset list lands, then bake onto authored

Do **not** invent a color glass ramp, a PiP scope, a live LPVO kit, or a replacement pack. Store `dBXpg` still **open**. Kit PBR stub stays #64. See `FULCRUMRUST_LAST_PASS_LOCK.md` Scope glass + Evan asset-ask path.

## Controller lock (Evan bind wins)

Shipped in fulcrumRust #12. Overrides soft aim-offset wheel-height where they disagreed:

- **Q / E** — **Q = peek right** (same side as inverted A) · **E = peek left**. Eye formula stays `+lean → −flat_right`. Depth **0.5 / 0.5**. #25 wall clamp / spring / yard covers stay
- **H** — viewmodel **crossover shoulder / left-corner peek** on the existing FoW H bind (travel landed #59; tilt path **landed #84**; RH hip bias + slight straighten **landed #94**; one more body-width + ready-hip Y **landed #98**). Not a capsule/eye slide, not a mesh mirror
- **End** — live aim-offset / attachment tuner (landed #97). Feel-lab Home remapped like X→Z. **Home stays unbound / Augury**. Insert WEAPON↔ATTACH · PageDown pose/attachment · PageUp step · ↑↓ axis · ←→ / num± nudge · Delete JSON. Glasses `AIM TUNE`. Authored defaults now **#98**
- **Shift then Ctrl** — slide carry (sprint + crouch rising edge) **while grounded** (#78). Midair Shift+Ctrl cannot zero `vel.y` / hover
- **Hold Ctrl + mouse up/down** — analog eye height (does **not** pitch-look)
- **Mouse wheel** — move speed (**not** height; aim-offset uses wheel for crouch height — Evan’s bind wins)
- **Space** — CE hop + one air hop + land overlay (landed #59; softener #79). Hop 12/30/1 **unchanged**. Punch **0.028** · duck **0.08** · shake **0.14** gate **13** + inertia sway. Prior FPS-first "no double-jump" / #51 single-hop-only is superseded (same way #51 superseded earlier "no jump")

## Holding steady

- Hypha: distance activation / far-guts cold landed (#23) on #16 host; extract sky sample shared with Range Tech clock (#24); **#27 binaural / positional stereo on FX landed** (partial — shot propagation later; file-slot wiring landed #54; handmade vendor landed #62); **#34 listen-server / invite stub landed** (HELLO/WELCOME / **Y** host / `--join`; **#83** Beabim pose + HOLD JOIN supersedes handshake-only + no in-game join field; world / shoot / Locus / terrain rewrite / dedicated infra still parked); **#42 Windows one-click release builder landed** (basic; quality/flag still open); **wider extract chunk radius landed (#43)** (7×7 / 3 rings / 112 m / 12 544 m²; extra far ring only); **near LOD raise landed #61** (then subdivs **32/16/4**); **first big-map landed #81** (19×19 open / 304 m / 92 416 m² · 9×9 stream · underfoot **32/16/8/4** · walls off · stamp pad stays 7×7; Beabim peer feet `stream_anchors` **landed #83** — coordinate only); **biped foot plant landed #88** (FOLLOW **8.5** / DEADZONE **0.04** / RISE **2.2** / SINK **6.5** / SNAP_ERR **1.15** / LIFT_MAX **0.14** / BOOT_HALF_H center **0.11**; Mixamo sockets Pelvis / Foot_L / Foot_R / Head host hooks only; STEAL_MAP biped **partial**; Mixamo clips / player body / 2-bone IK / GPU skin parked); **#46 Options guts landed** (Graphics/Gameplay/Controls + borderless default + persist — steal CE/Mycelium; does not dump atelier into Options); **Graphics dump landed #86** (thin Options **FOG / FOG NEAR / FOG FAR / CAM NEAR / CAM FAR** + persist `project.json` alongside Range `output_device`; extract haze **375 / 520** · cam **0.05 / 2000** · clouds **0.63** · sunPunch **0.51** · light*Mul **0.11 / 0.41 / 0.61 / 2.11 / 1.65 / 1.06** · exp **1.44** · skyHdri on; hideout `haze_max` **0**; bloom / godRays / brightness / gamma **no path** — do not invent); **HDRI sun disc landed #87** (dump **sunSize 0.62** rides the procedural disc/halo; plate solar-region tone + soft disc — not a second sky); **#55 GPU post stack landed** (AO/AA/CA/grain/DoF fullscreen wgpu; toggles change the image; smoke `post=aa`; not full HDR bloom / god-ray / contact-shadow); **colorless muzzle heat landed #66** (`heat_warp_uv` before scene sample; lattice = post input only; no world-pipeline orange card; HUD/glasses still after post); **ADS viewmodel DoF landed #68** (ADS near + far on that same pass / same Options **DOF**); **LOD-tied grit / material mips landed #60** (near **256²** Lab-Rat vendor / mid **64²** / far **16²** BC4-style 8-bit; far drops grain hashes; in-repo grit mips stay until Lab-Rat cooks more; smoke `grit_mips=256/64/16 n=196608 f=768`); Lab-Rat **#58 quiet grit greyscales** remain the vendored near packs (not the whole roughness→stamp cook); next live LOD recook / tunnel cutouts / SVG density-mask ingest; keep sit-on-surface CPU boxes as peek leftover; **scope glass** (greyscale ramp / IOR / no-PiP bodycam) **holding until LPVO** — Hypha Graphics when it lands; Range AIM TUNE placements first. Do **not** claim LPVO or glass shipped
- Beabim: **two-instance pose sync + HOLD JOIN landed #83** (UDP **POSE** ~20 Hz feet/yaw/pitch/grounded/crouch; 5-box slate silhouette; grounded Y rides #81 heightfield; `stream_anchors` follow remotes; Esc → JOIN types `fulcrum://` / `fw://` / `ip:port` / `localhost`; port **7777**). Grounded silhouettes share Hypha #88 `plant_simple_root` (packet / handshake / HOLD join stay #83). Shoot / HoB / heat / Locus / stamps / Transvoxel rewrite / audio / ToD / drops stay **local**. Live-profile loot trail still later. **Y** host / **I** stim / hold-**O** extract binds stay. **1P viewmodel ≠ 3P biped gun** — holding / locked intent (not shipped); do **not** claim #83 5-box is full 3P kit honesty; Beabim owns the 3P gun / gear sync path
- Augury: Locus Standard (#18) + Inked (#26) landed; extract plant on heightfield **landed #88** (brains still Augury); spatial CE DNA via #27; **#56 CE reverb volumes landed** (DRY / YARD / OUT AABB proxies; FX wet send only; glasses peek; two-zone stub retired); **Chamber owns spatial/reverb** (does not take file slots); **down/death stub #36 landed** (partial — death cam / teammate net stabilize / timed surface kill / full loot loop later); **#37 I-stim / Y-host bind lock**; **#41 FoW title mark landed** (vendored CE header on the #11 shell); **#45 title+HOLD analysis-core polish + Options list shell landed** (white frames / white hairline; HOLD **SYSTEM PAUSED**; Graphics/Audio/Gameplay/Controls list — Audio live #21 + **#82** DEVICE); Hypha tab guts / window / persist shipped #46 — not a second overlay; **#55 GPU post live** (HUD/glasses still after post); **#66 heat warp** sits on that stack; **#68 ADS near** sits on that stack (same Options **DOF**); **#51 dizzy-play landed** (invert look + A/D, F-only door); **#59 hop landed** (CE hop + air hop + land overlay — #51 single hop superseded; **#79** softener on the same overlay); FoW brand / menu video **when cut ready** (big-map brief); glasses polish + EXTRACT elbow card **landed #85** (hold-O paints EXTRACT on nearest in-front hatch/shaft — no popup; Range #78 wired `Session::extract_checking`); full hatch popup (elevator / toggle / timed surface kill) still **~**; next Sonderer/Monk/Oculus/crawler + stamp spawn filters (prefer rock/concrete; avoid organic)
- Lab-Rat: void-spore grimdark + density-driven concrete wear landed (#20); **#30 loud Inked void-spore hotspot landed**; **#38 shape-agnostic stamp/paint substrate landed** (channels + primitives; no new scar kinds; yard/Inked/curl stay consumers); **#39 extract-yard scale harness landed** (`apply_yard_harness`, pad ≈110 m², near-warm/far-cold; smoke `layers=`/`prims=`/`yard_m2=`); Hypha #43 `ExtractStubHost` / stamp pad stay **7×7** (`STUB_GRID = 7`; Hypha walk is **#81 19×19**); stamps stay **quiet on audio**; **quiet grit greyscales landed #58** (vendored 256² `grit_{grunge,crack,dust}.png` + `sample_channels` quiet height + `grit::rough` wear; smoke `grit=`); further roughness → stamp stays on **fulcrumRust only** — bake greyscales **down before density** (8-bit / half-res / BC4-style height packs); do **not** ship raw 4k 48-bit into the yard; atelier plugs **open** (Evan **clean** yell 2026-09-08 ~00:00 ET); PBR batch **in** (150 roughness + textures/PBR ~26 sets); slope/PBR/dirt/scatter/deform plugs **landed #80** (DISP bake-down + `Deform` / `GroundScatter` filled at `8,-6` / `-10,14`); slope COL hooks reserved on host **#81** (vertex albedo only — Hypha owns that bind); NRM/GLOSS GPU parked; Holocron rust rewrite still waits on SVG / density-mask / monolith splits (`TOOLS.md`); next wet-lab beats stay on STEAL_MAP (SVG/density-mask ingest / experiment log); **Evan asset-ask** — stamps keep **procedural grit** until the asset list lands, then bake onto authored; style grows with peeks (void-spore + grit floor). Do **not** invent a replacement pack
- Range Tech: day/night clock + sky (#24), wall-clamped lean (#25), hold-` inspect (#28), bandage use (#31) landed; **#32 reload DNA landed** (Hold-R peek / tap-R reload / double-tap SWAP); **#33 live HoB zero landed** (**#76** SIM-only — **P** unused; leftover `hob_zero` ignored; **#78** **−/=** 50/100/200 — **O** is extract intent); **#35 heat-tune dump landed** (hold-J; **I** is Augury stim #37); **#40 Goegap HDRI on extract ToD landed** (/** plate toggle; glasses `HDRI` / `PROC`); **#47 leftover feel-lab FX landed** (brass eject / graze ricochet + spent slug / richer impact geo / `casing_draw_m` **55**; **#79** sleep/ends/marks snap to extract heightfield); **#51 AXIS_LOCK landed** (cam −Z / CE +X / barrel +Z; Lab-Rat +Y separate; FX on `sim_barrel_basis`; dizzy-play invert look/strafe + F-only door); Voice/Music/FX buses (#21) carry Hypha/#27 spatial + #47 ricochet ping (**FX bus live**); **Options Audio DEVICE landed #82** (SYSTEM DEFAULT; cpal cycle; persist `output_device`; same mixer → thin cpal voice — not a second mix tree); **authored SFX file-slot wiring shipped #54**; **handmade atelier vendor landed #62** (weapon/move off CE/feel `sfx_/` into those buses; rustles / rattles / slides come over; small set, not a full pack dump; missing → procedural); shot propagation still later; one-click Windows `build.bat` **#48 stay-open + `build.log` tee landed**; quality/flag options still cooking / open (Lab-Rat mirror for pycelium later — no dials invented here); **feel medium polish landed #57** (look inertia queue **26**; ADS look **0.86** / blend **6.4**; sprint high-ready **6.2**; slide carry **10.3 / 0.98 / 1.02**; jump land punch then **0.052** — **#79** live **0.028** + sway; AXIS_LOCK stay; no materials/range geo); **Evan peek landed #59** — **crossover shoulder / left-corner peek** (H viewmodel travel; authored hip +X ~0.24 → partial left ~−0.041 X / ~−0.181 Y, cap `shoulder_x_min` −0.055; ADS **0.32**; **#94** slight straighten pitch/yaw/roll **0.04 / 0.10 / 0.08**, supersedes #84 chest-cross 0.08/0.32/0.39 — not a mesh mirror); lean flip + deepen (**Q = peek right** / **E = peek left**; depth **0.5 / 0.5**; #25 clamp/spring/yard stay); CE hop + air hop (`JUMP_FORCE` **12** / `|GRAVITY|` **30** / one air hop **unchanged**; **#79** punch **0.028** · duck **0.08 m** · shake **0.14** gate **13** + inertia sway); heat motion v77 shimmer / lattice crawl stays Range Tech spatial input / `barrel_energy` / hold-J; **live tell is Hypha colorless post UV warp landed #66** (lattice = post input only; no world-pipeline orange card); tracers live until impact (sanity **180 s**, linger **2 s**) + FX `hit`; **Patch A muzzle landed #67** — kit-tip spawn (`muzzle_tip_local`) + `hip_honest_dir` (ads=0 on aim; ads=1 SIM HoB/zero) + tip→impact streak clamp (`tracer_len` is length, not a receiver skip); hip-fire no longer behind the handguard / upper-right of the reticle; **−/=** + #59 tracers-until-impact stay; **P** unused (#76); **O** is hold extract intent (#78); #67 did **not** fight #66 and did **not** ship heat color; **ADS viewmodel DoF landed #68** — disc blur on near depth when ADS + Options **DOF** (radius **0.0048** UV-x at ads=1; taps **12**; amount `ads_factor`, skip < 0.02; hip = 0; near fade full ≤ **0.90 m**, gone by **2.20 m**; far DoF smoothstep **9 → 46 m** unchanged; breath mul **1.6 parked**); same #55 pass / same Options **DOF**; gun softens under ADS; hip + range stay sharp on that layer; #68 did **not** ship heat color (live tell is Hypha #66); **heat dial blend landed #71** — live defaults sit between old bake and the dump (haze **0.07** / size **0.83** / scaleX **0.396** / lobe **0.698**; #66 colorless path stays; no orange card redraw); **SIM-only launch landed #76** — one HoB + gravity / zero model; arcade aim-dir dead; **P** unused; leftover `hob_zero` ignored; **−/=** 50/100/200 (#78); #67 hip honesty on the single SIM model; **hold-O extract / −/= zero / grounded slide landed #78** — raid `Session::extract_checking`; **O** is **not** zero; Augury EXTRACT elbow card **landed #85** (no popup); hatch elevator / toggle / timed kill still **~**; midair Shift+Ctrl cannot float-slide; **land sway softener + heightfield FX landed #79** — same #59 hop overlay; punch **0.028** / duck **0.08** / shake **0.14** gate **13** + sway; brass/tracers/marks snap to extract heightfield; `first_hit` walls-only; AXIS_LOCK +Z unchanged; Hypha first big-map host **landed #81** (Range heat / ballistics / binds **not touched**); **Hypha Graphics dump landed #86** (Options FOG / CAM NEAR/FAR + sky / post defaults — Range heat / binds / ballistics / Audio DEVICE **not touched**); **HDRI sun disc landed #87** (shared Hypha; dump **sunSize 0.62** rides the disc; plate solar-region tone + soft disc — not a second sky); kits + FX draw-distance on the wider yard still Range; kit metal/grit PBR stub **landed #64**; store `dBXpg` still **open**; **SFX remix DNA** (pitch/speed/effects; indie underground; don’t overuse the same stem) — first ±6% fire/foot/reload jitter **landed #64**; full remix minting still **open**; Music playlist beds **landed #64**; **Options Audio DEVICE landed #82** — SYSTEM DEFAULT; A/D or arrows / Enter / click; persist `output_device`; missing pin kept, playback falls back to OS default; same #21 mixer → thin cpal voice (oneshots + Music-bed loop); UI tick on the new pick; Stream on window thread (not Sync); **H shoulder-swap tilt landed #84** — tilt path; live left hold **#94** slight straighten pitch/yaw/roll **0.04 / 0.10 / 0.08** (supersedes #84 chest-cross 0.08/0.32/0.39); travel dest ~−0.041 X / ~−0.181 Y / cap **−0.055** / ads_keep **0.32**; not a capsule/eye slide, not a mesh mirror, no `scale.x = −1`; PreferredHand / new-profile onboard stays house/Hypha parked; **Patch A RH hip bias landed #94** — first +0.08; live hip **superseded #98**; ADS X / tip spawn / `hip_honest_dir` / #89 tracers stay; **aim-offset tuner + attachment sockets landed #97** — live **End** sheet on existing ViewmodelDials + kit_mesh optic/can sockets (Insert WEAPON↔ATTACH · PageDown target · PageUp MICRO/FINE/MED/COARSE · Delete JSON; glasses `AIM TUNE`); Home stays unbound / Augury; authored defaults now **#98**; not Home chrome, not hitch logger, not EffectComposer, not a second pose system; **RH hip one more body-width + ready-hip Y landed #98** — MP9-Z hip **0.2403 / −0.2128 / −0.1833**; `shoulder_cross_x` **−0.281** / `shoulder_cross_y` **0.032**; hip_low Y stays #94 **−0.2788**; no mesh flip / new shotgun pose; **projectile feel landed #89** — Vector dump rect slab + 4–6 debris (0.07–0.17 s) + feel-lab visualLength **1.5 / 18** + core **2.85 / 2.25 / 0.95** + slug **0.07** + wake 1–2 + hit flash **0.15** s + punch **8–12** (35% white) / scuff **4–6** amber + fire-pulse glyphs on existing `TracerField`; SIM / HoB / gravity **unchanged** (#76); HeatDials **unchanged** (#71); AXIS_LOCK +Z / #79 snap stay; CE tip **0.2.8** preferred if a later cook retunes muzzle-adjacent haze — not a heat-card rewrite, not Beabim, not profile onboard; **scope glass / LPVO holding** — AIM TUNE placements first (#97); Hypha owns glass when LPVO. **Asset-ask** — clone CE / aim-offset attachment tables first; missing → ask Evan this week; primitives stay scaffolding
- Atelier: plugs **open** (Evan **clean** yell 2026-09-08 ~00:00 ET). PBR batch **in** (150 roughness + textures/PBR ~26 sets). #58 / #80 optional `FULCRUM_GRIT=` / `FULCRUM_ATELIER=` stay read-only **load** paths (downsample on load). Lab-Rat slope/PBR/dirt/scatter/deform plugs **landed #80**. Further roughness → stamp stays on fulcrumRust only — bake-down first; SVG / density-mask / experiment-log still open; do **not** ship raw 4k 48-bit PNG into the yard. Evan has **this week** (from 2026-09-09) to model + texture missing asks — clone CE / aim-offset tables first; primitives stay scaffolding

Steal from this shelf + steal map. Not chat scroll.
