# Checkpoint peek findings (fulcrumRust)


Parked from Evan’s first full `main` peek (2026-09-07). Growth yard + curl read OK. Same-day feel dump **landed #59**. Hypha ring-mip texture LOD **landed #60**. Hypha near LOD raise **landed #61**. Range Tech handmade atelier SFX vendor **landed #62**. Range Tech music playlist + kit metal/grit PBR stub + ±6% remix jitter **landed #64**. Hypha colorless muzzle heat **landed #66**. Range Tech Patch A muzzle **landed #67**. Range Tech ADS viewmodel DoF **landed #68**. Range Tech heat dial blend **landed #71**. Range Tech heat CE tip **0.2.8 landed #129**. Range Tech SIM-only launch **landed #76**. Range Tech hold-O extract / −/= zero / grounded slide **landed #78**. Range Tech land sway softener + heightfield-grounded FX **landed #79**. Hypha first big-map 19×19 open extract + slope COL **landed #81**. Range Tech Options Audio output DEVICE / cpal cycle **landed #82**. Range Tech dirt-impact Hit pool + world FX mono fold **landed #134**. Range Tech H shoulder-swap tilt **landed #84**. Beabim two-instance pose sync + in-pause JOIN **landed #83**. Hypha Graphics dump **landed #86**. Augury elbow smart-labels **landed #85**. Range Tech + Hypha HDRI sun black-out / blow-out **landed #87**. Hypha biped foot plant / terrain follow **landed #88**. Lab-Rat slope/PBR/dirt/scatter/deform plugs **landed #80**. Lab-Rat Blender UV dials **landed #101**. Hypha Transvoxel UV consume **landed #112**. Lab-Rat Patch A subtract crawl pad network **landed #114**. Lab-Rat probe consume **landed #127**. Lab-Rat sandbox pedon **landed #130**. Lab-Rat extract player spawn loci **landed #132**. Range Tech projectile feel **landed #89**. Range Tech Patch A RH hip bias **landed #94**. Range Tech aim-offset tuner + attachment sockets **landed #97**. Range Tech AIM TUNE live-save **landed #103**. Range Tech AIM TUNE PX travel **landed #138**. Augury CE Home debugger **landed #110**. Augury Home LOGS COPY + tracker toggles **landed #121**. Augury Home occlusion + 3D probes + COLL/PERF/SPWN **landed #125**. Augury Home binds lock + spawn probes + denser STREAM **landed #128**. Hypha stream hitch amortize **landed #108**. Hypha worker STREAM extract+paint **landed #123**. Hypha play STREAM 11×11 + warm resident hold **landed #137**. Hypha 4× world + pend coalesce **landed #142**. Range Tech RH hip one more body-width + ready-hip Y **landed #98**. Range Tech low-hip shotgun stance **landed #99**. Range Tech canted 45° Greyzone CQC ADS **landed #100**. Range Tech U-cycle hold springs **landed #109**. Range Tech kit handling / ergo / MOA **landed #113**. Augury hatch/elevator glasses UX **landed #115**. Beabim invite leftover + peer names + gun pose **landed #91**. Beabim live-profile loot trail **landed #102**. Beabim world/sim leftover **landed #119**. Hypha PreferredHand + new-profile onboard **landed #116**. Augury door/extract cancel chrome **landed #120**. Beabim no-pause live sim + shared extract handshake **landed #122**. Beabim PVP leftover **landed #133**. Beabim HOST session board + no-127 invite seed **landed #139**. Beabim PVP honesty **landed #141**. Beabim leftover ray **landed #147**. Range Tech wound feel / 1P screen-react **landed #143**. Hypha landmark AABB ride **landed #136**. Hypha landmark ride hop **landed #149**. Hypha 3P biped / PeerBody **landed #131**. Hypha 3P torso lean match **landed #145**. Lab-Rat stamp / building / terrain PBR polish **landed #144**. Hypha pixellation / warp strength floor **landed #90**. **1P viewmodel ≠ 3P biped gun** (MP honesty) is **partial shipped #91** (peer biped hip gun stub; full 3P kit honesty / hands / gear sync still open) (Evan 2026-09-09). **Scope glass** (when LPVO) + **Evan asset-ask path** are **holding / not shipped** (Evan 2026-09-09). Overnight cooks steal from this shelf. Evan **clean** yell 2026-09-08 ~00:00 ET — atelier plugs **open**.

## Patch A checkpoint (fulcrumRust #72)

Living A-feedback checkpoint — **not** a replacement for `STEAL_MAP` or `MILESTONE_01_PLAYABLE`. Repo-root [`patch notes A.txt`](https://github.com/initialvisuals/fulcrumRust/blob/main/patch%20notes%20A.txt) ([#72](https://github.com/initialvisuals/fulcrumRust/pull/72)). Marks: `X` done / on main · `~` partial / in progress / shallow first pass · `*` next / ready for a careful cook when greenlit · `·` parked / not started. Seats: Range Tech | Hypha | Lab-Rat | The Augury | Evan | house. Overnight cooks and seats read open A asks from that file; do **not** invent PR numbers. Do **not** copy the ledger here. Range Tech dump-dial blend is **landed #71** (`X` on the house shelf — A-notes `~` for that row is stale; **DNA / not live**). Live HeatDials are **#129** CE tip 0.2.8 (`X` on the house shelf). Range Tech sim-default / single model is **landed #76** (`X` on the house shelf). Range Tech hold-O extract intent / **−/=** zero / grounded slide is **landed #78** (`X` on the house shelf). Augury glasses polish + EXTRACT elbow card is **landed #85** (`X` on the house shelf). Augury hatch/elevator glasses UX is **landed #115** (`X` on the house shelf — hatch toggle + shaft ride **X**; timed surface kill stays `~`). Augury door/extract cancel chrome is **landed #120** (`X` on the house shelf — door / extract cancel **X**; timed surface kill stays `~`). Range Tech land overlay soften + heightfield ground FX is **landed #79** (`X` on the house shelf — hop 12/30/1 **unchanged**; same #59 overlay, not a second land system). Hypha first big-map 19×19 open extract + chunk stream + slope COL is **landed #81** (`X` on the house shelf — vertex albedo only). Lab-Rat slope/PBR/dirt/scatter/deform plugs **landed #80** (`X` on the house shelf — DISP bake-down + deform/scatter filled; NRM-GLOSS still parked; SVG / density-mask / experiment-log still open). Lab-Rat Blender UV dials **landed #101** (`X` on the house shelf — scale/offset/rotate on stamp/PBR/grit; identity default; texture tiles only, never geo / never Transvoxel shrink). Hypha Transvoxel UV consume **landed #112** (`X` on the house shelf — `promote_for_uv` + TerrainHost wear/COL honor; texture-only, never remesh / never chunk shrink). Lab-Rat Patch A subtract crawl pad network **landed #114** (`X` on the house shelf for the enterable pad network — full underground / live voxel collide still `[~]`). Beabim two-instance pose sync + HOLD JOIN is **landed #83** (`X` on the house shelf — peer feet / `stream_anchors` follow remotes; terrain rewrite / audio stay local; shoot / Locus leftover **later landed #119**). Beabim invite leftover + peer names + gun pose is **landed #91** (`X` on the house shelf — INVITE leftover / fade-in names / biped hip gun stub; full 3P kit honesty stay open; shoot leftover **later landed #119**). Beabim live-profile loot trail is **landed #102** (`X` on the house shelf — KIND_LOOT host-relayed Z/F; hairline `{NAME} DROP/TAKE KIT`; starting kits stay local; shoot / Locus leftover / death bag **later landed #119**). Beabim world/sim leftover is **landed #119** (`X` on the house shelf — KIND_SHOT / KIND_LOCUS / KIND_BODY on the #83/#91/#102 UDP leftover; peer shot muzzle = biped hip stub; joiner plants soles only; Range feel / HoB / heat / brass / knife-rally / joiner slash / stabilize / stamps / hatch stay local). Beabim no-pause live sim + KIND_RAID shared instance is **landed #122** (`X` on the house shelf — Esc HOLD / Options / JOIN mute the local pawn only; raid keeps ticking; focus loss / alt-tab releases grab, does not HOLD or freeze; KIND_RAID leftover = Augury `GATE_SECS` **2.20**; honors `Cancelled`; solo `net=off` uses the #120 countdown; glasses HOLD % stay Augury). Beabim PVP leftover is **landed #133** (`X` on the house shelf — KIND_PVP default **off**; hide names when on; KIND_BRASS host-relay; leftover eye **1.60** / head **1.62**; rim respawn **1.20 s** from `World.player_spawns`; ragdoll hook-only until #131 PeerBody (**later landed #131**); do **not** claim Range / Hypha / Lab-Rat / Augury shipped this). Beabim HOST session board / no-127 invite is **landed #139** (`X` on the house shelf — title HOST PVP **OFF/ON** radio before Deploy/enter; settings lock; `FULCRUM_PVP` / `--pvp` still seed peeks that skip the board; Home / JOIN / glasses / `fulcrum.invite` prefer LAN — no 127 seed; typed `--join 127` still works; KIND_PVP default-off + solo `net=off` held; do **not** claim Range / Hypha / Lab-Rat / Augury shipped this). Beabim PVP honesty is **landed #141** (`X` on the house shelf — `PeerBody::hurtboxes()` leftover · hurt skin **0.06** + swept AABB + **4** substeps · KIND_PVP Hit/Sync/WELCOME remaining HP/AR · unique rim pads host **0** / rotate / occupancy **16 m**; eye **1.60** / downs **1.20 s** held; Range eject dials untouched; do **not** claim Range / Hypha / Lab-Rat / Augury shipped this). Beabim leftover ray is **landed #147** (`X` on the house shelf — `LEFTOVER_HIT_M` / `first_leftover_hit` **500 m** was 80 · flat `SMG_PELLET` **14** · Locus yard keeps own 80 · Range falloff parked · eye PeerBody + hurt skin/sweep held; do **not** invent dials; do **not** claim Range / Hypha / Lab-Rat / Augury shipped this). Range Tech wound feel / 1P screen-react is **landed #143** (`X` on the house shelf — suppress-near soft short blur · armour jostle + soft blur no red · HP stronger jostle + blur + red fade · envelope `--===--------` · never full-strength blur · 1P local; Hypha `post.wound` [blur, red]; hooks Beabim KIND_PVP Hit not Sync; Death/Slain stays Augury; do **not** invent dials). Range Tech Options Audio output DEVICE / cpal cycle is **landed #82** (`X` on the house shelf — A-notes already `X` from #82; bus dials unchanged). Range Tech dirt-impact Hit pool + world FX mono fold is **landed #134** (`X` on the house shelf — `Slot::HIT_POOL` distant dirt trio + `DecodeFold::WorldMono` on `Bus::Fx`; Music/Voice keep stereo; Augury spatial stays). Range Tech H shoulder-swap tilt is **landed #84** (`X` on the house shelf — travel dest ~−0.041 / cap **−0.055** / ads_keep **0.32**; live left hold **#94** slight straighten pitch/yaw/roll **0.04 / 0.10 / 0.08**, supersedes #84 chest-cross 0.08/0.32/0.39; not a mesh mirror. PreferredHand / new-profile onboard **later landed #116**). Hypha Graphics dump is **landed #86** (`X` on the house shelf — thin Options **FOG / FOG NEAR / FOG FAR / CAM NEAR / CAM FAR** + sky / post defaults; persist `project.json` alongside Range `output_device`; hideout `haze_max` **0**; bloom / godRays / brightness / gamma stay parked / no path). Range Tech + Hypha HDRI sun black-out / blow-out is **landed #87** (`X` on the house shelf — dump **sunSize 0.62** now rides the procedural disc/halo; plate solar-region tone + soft disc; #86 fog / punch / exp / cam stay; bloom / godRays still no path). Hypha biped foot plant / terrain follow is **landed #88** (`X` on the house shelf — A-notes `[·] enemies walk into terrain` → **X**; STEAL_MAP biped **todo → partial** — plant + host hooks; Mixamo clips / player body / 2-bone IK / GPU skin still parked). Hypha landmark AABB ride is **landed #136** (`X` on the house shelf — `RIDE_STEP` **0.50** · `RIDE_SKIN` **0.06** · `SUPPORT_STEP` **0.25** unchanged; `ride_surface_y` = max(heightfield, AABB top under footprint); walls-as-floor only in the ride band; Locus hurtboxes stay walls; peers `plant_simple_root_on` same column; hop onto / land **later landed #149** vertical before XZ — no extra hop dial; 3 m compounds stay walls; #88 FOLLOW/DEADZONE stay; STREAM / Lab-Rat stamps untouched; do **not** invent A-note PRs; do **not** claim Range / Beabim / Lab-Rat / Augury shipped this). Hypha landmark ride hop is **landed #149** (`X` on the house shelf — vertical before XZ; same #136 band; Space hop ~0.20 m first frame enters `RIDE_STEP`; walk/stand ride unchanged; 3 m compounds stay walls at ground / on the hop frame; do **not** invent dials; do **not** claim Range / Beabim / Lab-Rat / Augury shipped this). Hypha 3P biped / PeerBody is **landed #131** (`X` on the house shelf — `EYE_Y` **1.60** · `HEAD_H` **1.62** · `HEAD_HALF_H` **0.11** · XZ **0** left-offset killed; crouch squat **0.62** · ragdoll flop **0.55 s** · pose lean unused byte 2; lean match **later landed #145** torso peek **0.5 m** · hinge **0.55** · feet planted; Mixamo clips / player body / 2-bone IK / GPU skin still parked; do **not** invent A-note PRs; do **not** claim Range / Beabim / Lab-Rat / Augury shipped this). Hypha 3P torso lean match is **landed #145** (`X` on the house shelf — `LEAN_LATERAL` **0.5** · `LEAN_HINGE_Y` **0.55** · `LEAN_ANGLE` **0.52** · `LEAN_SMOOTH` **9.5** · pelvis/spine/chest; Range `lean_offset` read only; do **not** invent A-note PRs; do **not** claim Range / Beabim / Lab-Rat / Augury shipped this). Range Tech projectiles from CE / feel-lab visualLength + Vector dump flash is **landed #89** (`X` on the house shelf — A-notes `[·] projectiles from CE (Range Tech)` → **X**; SIM / HoB / gravity stay #76; HeatDials **later landed #129** CE tip 0.2.8 (#71 blend DNA); AXIS_LOCK +Z / #79 snap unchanged). Range Tech Patch A RH hip bias is **landed #94** (`X` on the house shelf — first +0.08; live hip / ready-Y **superseded #98**). Range Tech aim-offset tuner + attachment sockets is **landed #97** (`X` on the house shelf — A-notes ledger `~` / parked `·` for this cook is stale). Live **End** sheet on existing `ViewmodelDials` + `kit_mesh` optic/can sockets; Home debugger **later landed #110**. Range Tech AIM TUNE live-save is **landed #103** (`X` on the house shelf — End→Hypha `project.json`; STEAL_MAP live-save **in**; `aim_live` default **true**; partial merge keeps authored **#98 / #99 / #100**; #97 End / Delete dump stay; RECORD toggle stub — no bind). Range Tech AIM TUNE PX travel is **landed #138** (`X` on the house shelf — leftover +0.226 from `−shoulder_cross_x + shoulder_x_min` is **not** an End +X cap; `shoulder_x_max` **±0.50**; H still floors at `shoulder_x_min` only; authored hip **+0.2403** / H dest **~−0.041** / #103 live-save / `hold_spring` / ADS blend untouched). Augury CE Home debugger is **landed #110** (`X` on the house shelf — Augury #95 tip / * next tabs+logger stale). Native overlay: **Home** toggle · LOGS / TELE / CHEAT · hitch WARN >33 ms / HITCH >100 ms. End stays Range AIM TUNE (#97/#103). Augury Home LOGS COPY + tracker toggles is **landed #121** (`X` on the house shelf — LOGS follow-up peek after Home LOGS). **Enter** COPY · ring **800** · `[sssss.mmm]` · Insert/Delete tracks · `log_*` persist default on · medium edge events. #110 stays the tabs+logger foundation. Augury Home occlusion + 3D probes + COLL/PERF/SPWN is **landed #125** (`X` on the house shelf — Patch A * occlusion / * CE 3D cursor/probe rows stale). Tabs **LOGS / TELE / COLL / PERF / SPWN / CHEAT**. **P** drop look-at probe · Enter copies `fulcrum.probes` JSON (cap **32**). Soft Enter COPY debounce **0.45s**. Augury Home binds lock + spawn + denser STREAM is **landed #128** (`X` on the house shelf — Home cycles off→tabs→off · arrows/Enter · Ins pages · no WASD/Space; `name:ground`; `kind:spawn` via SPWN+P; denser WALK/STREAM hang tags). Lab-Rat extract player spawn loci **later landed #132** (bake consume into `World.player_spawns` — #128 stays the writer). Lab-Rat probe consume **landed #127** (house shelf — `FULCRUM_PROBES` / cwd `fulcrum.probes` → `probes.rs` → `apply_to_layers` at bake; kind routing terrain sit · wall lip · hole/overhang Subtract; `probes=off` if missing; not a second mesher). Range tip/optic probe JSON stay **·**. Lab-Rat sandbox pedon **landed #130** (house shelf — off-stream CHANNELS leftover slab; tap **F** rebake; not Home chrome / not #114 pad crawl / not Hypha STREAM remesh). Lab-Rat extract player spawn loci **landed #132** (`X` on the house shelf — 8 rim pads; #132 shipped Chebyshev **144 m** on the #81 19×19; live rim **288 m** via **#142** `probes::rim_radius_m()` → `World.player_spawns`; Home **P** + SPWN `kind:spawn` override within **48 m** XZ else append; Beabim pool / knock-off **later landed #133**). Lab-Rat stamp / building / terrain PBR polish **landed #144** (`X` on the house shelf — rocks 3-lobe shade/face/chip · buildings Concrete grade + face UVs · default `pbr=vendor` 256² COL · five thumbs + concrete NRM; texture+UV only; chunk **16 m** held; Hypha STREAM/geo untouched; do **not** invent dials). Hatch toggle + shaft ride **landed #115** (`X`); timed surface kill stays `~`. Hypha Patch A stream hitch amortize is **landed #108** (`X` on the house shelf — cook=1/2 · prefetch=5 m · splash-pumped load-in; residual soft LOD pop / live octree still parked). Hypha worker STREAM extract+paint deepen is **landed #123** (`X` on the house shelf — play worker extract+paint · `defer=worker/paint/gpu` · skip far mask-only remesh; #108 cook=1/2 · cook_ms 8/16 · prefetch=5 m stay). Hypha play STREAM 11×11 + warm resident hold is **landed #137** (`X` on the house shelf — `STREAM_RINGS` **5** / **11×11** · prefetch=5+heading · hold=2/12; #108/#123 hitch layers stay). Hypha 4× world + pend coalesce is **landed #142** (`X` on the house shelf — 37×37 / 592 m / 350 464 m² · rings 18 · STREAM held 11×11 · `coalesce=2/2` · rim **288 m**; #81 stays the prior 8× / 19×19 fact; do **not** claim STREAM_RINGS bumped). Range Tech RH hip one more body-width + ready-hip Y is **landed #98** (`X` on the house shelf — MP9-Z hip **0.2403 / −0.2128 / −0.1833**; `shoulder_cross_x` **−0.281** / `shoulder_cross_y` **0.032** keeps H dest ~−0.041 X / ~−0.181 Y; left pitch/yaw/roll **0.04 / 0.10 / 0.08** unchanged. #97 End tuner still live — ready-hip / H defaults stay #98). Range Tech low-hip shotgun stance is **landed #99** (`X` on the house shelf — U-cycle `hip_low`; MP9-Z **0.2403 / −0.3528 / −0.1513** / pitch **0.145**; glasses **LOW HIP**; RMB from LowHip = iron ADS. Ready hip / hip_cant / H stay #98). Range Tech canted 45° Greyzone CQC ADS is **landed #100** (`X` on the house shelf — `ads_cant` MP9-Z **0.0423 / −0.148 / −0.136** / pitch/yaw/roll **0.024 / 0.11 / 0.785**; U+RMB / hold-Mouse5 @ 60° CQC; glasses **CANT 45** / **CANT ADS**. hip_low stays #99. Not a canted-holo mesh / IOR glass). Range Tech U-cycle hold springs is **landed #109** (`X` on the house shelf — STEAL_MAP pose-ease → **in**; `hold_spring` **7.0**; glasses still snap CHEST / LOW HIP / CANT 45; viewmodel eases; first-U seed-before-cycle). Range Tech kit handling / ergo / MOA is **landed #113** (`X` on the house shelf — A-notes `·` / parked handling row stale; STEAL_MAP handling → **in**; `HandlingStats` / `FeelSheet::handling`; ADS `blend_speed` **6.4** × kit ergo — not a fixed stub; `hold_spring` **7.0** stays sibling). House mastery row stays parked. Hypha PreferredHand + new-profile onboard is **landed #116** (`X` on the house shelf — A-notes already `[X]` PreferredHand onboard / `[~]` persistent+live profile stash stub; do not invent A-note PRs). Hypha pixellation / warp strength floor is **landed #90** (`X` on the house shelf — STEAL_MAP Augury pixellation **todo → partial**; A-notes has no pixellation/warp ledger row — none invented). Hypha owns the post dial (`warp_strength` default **0.01**); Augury owns the aesthetic note only.
## Vector mag dump (Range Tech — landed #89)

Evan aim-offset / Vector feel reference. **Live steal landed #89** (Range Tech). Rect slab + debris + slug/wake + punch/scuff flash + fire-pulse glyphs sit on existing `TracerField`. Artistic auth frame stays `VECTOR_MAG_DUMP.md` (local light / optic still reference-only unless already on the feel sheet). Hypha pixellation / floor warp **landed #90** (post dial `warp_strength` **0.01**; Augury aesthetic note only — do not claim Augury shipped the dial). Do **not** reopen orange heat cards or invent bloom / godRays. Intact siblings: #67 tip spawn · #76 SIM · #71 heat DNA · **#129** CE tip live · #79 heightfield.

## Holding — first big-map leftovers (Evan 2026-09-08 / landed #81 · live #142)

**Host landed #81** (prior 8× 19×19). Live extents **#142** 37×37. Peer feet stream anchors **landed #83**. Lab-Rat slope/PBR/dirt/scatter/deform plugs **landed #80**. Stamp / building / terrain PBR polish **landed #144** (default `pbr=vendor`). Do **not** claim NRM/GLOSS GPU / whole roughness→stamp / world replication / Range heat.

Live shelf: #16 host + #23 far-cold + **#142 37×37 / 592 m / 350 464 m²** (prior **#81 19×19 / 304 m / 92 416 m²**) + **#137 11×11** stream (`STREAM_RINGS` 5 · hold=2/12 · coalesce=2/2) + rim **288 m** + underfoot **32/16/8/4** + #60 grit mips + #39/#43 stamp pad **7×7** / yard ≈ **110 m²**. Walls **off**. Do **not** claim STREAM_RINGS bumped.

- **Hypha** host: drop walls · ~8× · chunk stream · local-player distance load **landed #81**. Graphics dump **landed #86** (Options FOG / CAM NEAR/FAR + sky / post defaults; hideout stays unfogged). HDRI sun disc **landed #87** (shared Range Tech + Hypha; dump **sunSize 0.62** rides the disc). Beabim peer feet + `stream_anchors` follow remotes **landed #83** (coordinate only — Transvoxel rewrite / terrain sync still parked). Biped foot plant / terrain follow **landed #88** (samples #79/#81 column; FOLLOW **8.5** / DEADZONE **0.04** / RISE **2.2** / SINK **6.5** / SNAP_ERR **1.15** / LIFT_MAX **0.14** / BOOT_HALF_H center **0.11**; mesher untouched). Landmark AABB ride **landed #136** (`RIDE_STEP` **0.50** · `RIDE_SKIN` **0.06** · `SUPPORT_STEP` **0.25** unchanged; `ride_surface_y` = max(heightfield, AABB top); walls-as-floor only in the ride band; Locus hurtboxes stay walls; peers `plant_simple_root_on` same column; hop onto / land **later landed #149** vertical before XZ — no extra hop dial; 3 m compounds stay walls; #88 FOLLOW/DEADZONE stay; STREAM / Lab-Rat stamps untouched). 3P biped / PeerBody **landed #131** (`EYE_Y` **1.60** · `HEAD_H` **1.62** · `HEAD_HALF_H` **0.11** · XZ **0** left-offset killed; crouch squat **0.62** · ragdoll flop **0.55 s** · pose lean unused byte 2; lean match **later landed #145** torso peek **0.5 m** · hinge **0.55** · feet planted; Mixamo clips / player body / 2-bone IK / GPU skin parked). 3P torso lean match **landed #145** (`LEAN_LATERAL` **0.5** · `LEAN_HINGE_Y` **0.55** · `LEAN_ANGLE` **0.52** · `LEAN_SMOOTH` **9.5** · pelvis/spine/chest; Range `lean_offset` read only). Pixellation / floor-warp **landed #90** (`warp_strength` default **0.01**; Options Graphics **WARP** after CAM FAR; `GFX_LEN` 12→13; fog/cam/#86 rows keep indices; mix toward CE PIXEL SCALE **2**; Augury aesthetic only — do not steal into Range). Stream hitch amortize **landed #108** (cook=1/2 · prefetch=5 m · splash-pumped load-in; hitch *visibility* stays #110 / #121 / **#128**). Worker STREAM extract+paint **landed #123** (`defer=worker/paint/gpu` · skip far mask-only remesh; hitch thread never `sample_channels` on play Transvoxel extract). Play STREAM 11×11 + warm resident hold **landed #137** (`STREAM_RINGS` **5** / leading edge 80 m · prefetch=5+heading · hold=2/12; #108/#123 hitch layers stay). 4× world + pend coalesce **landed #142** (37×37 / 592 m / 350 464 m² · rings 18 · `coalesce=2/2` · rim **288 m** — not a STREAM radius bump). Transvoxel UV consume **landed #112** (`promote_for_uv` + TerrainHost wear/COL honor; texture-only, never remesh). PreferredHand + new-profile onboard **landed #116** (Right default · NEW PROFILE gate · `project.json` permanent vs live · death clears live · extract→stash stub · H seats Range crossover, no mesh flip). Residual soft LOD pop inside a cell / live octree / far-4 horizon parked
- **Beabim** MP: two-instance UDP **POSE** + HOLD JOIN panel **landed #83**. Invite leftover + visible peer names + gun pose **landed #91** (INVITE sheet / `fulcrum.invite` / fade-in **HOST** / **P{id}** / 3-box biped hip gun stub). Live-profile loot trail **landed #102** (KIND_LOOT host-relayed Z/F; hairline `{NAME} DROP/TAKE KIT`). World/sim leftover **landed #119** (KIND_SHOT / KIND_LOCUS / KIND_BODY on the #83/#91/#102 UDP leftover). No-pause + KIND_RAID shared instance **landed #122** (Esc HOLD / Options / JOIN mute the local pawn only; raid keeps ticking; focus loss / alt-tab does not HOLD or freeze; leftover = `GATE_SECS` **2.20**; honors `Cancelled`; glasses stay Augury #120). PVP leftover **landed #133** (KIND_PVP default **off** · hide names · KIND_BRASS · eye **1.60**/1.62 · rim respawn **1.20 s**). HOST session board + no-127 invite **landed #139** (title HOST PVP radio pre-enter · settings lock · LAN bind prefer — no 127 seed). PVP honesty **landed #141** (`PeerBody::hurtboxes()` leftover · HP/AR Sync · unique pads host **0** / **16 m**). Leftover ray **landed #147** (`LEFTOVER_HIT_M` / `first_leftover_hit` **500 m** was 80 · flat `SMG_PELLET` **14** · Locus yard keeps own 80). Extract spawn pool / knock-off **landed #133** (Lab-Rat loci **#132**; Beabim consumes `World.player_spawns`; unique rotate **later landed #141**). Hypha 3P PeerBody flop **later landed #131** (Beabim leftover volumes **later landed #141**). Grounded silhouettes share Hypha #88 `plant_simple_root` (packet / handshake / HOLD join stay #83; #91 gun Y rides the same snap). Range feel / HoB / heat / brass / 1P hip / AIM TUNE / knife-rally / joiner slash / stabilize dummy / stamps / hatch / audio / ToD stay **local**. **1P ≠ 3P** (**partial shipped #91** — peer gun stub; #119 peer shot muzzle = biped hip, not 1P cant) — do **not** claim Mixamo / full 3P kit honesty / hands / gear sync- **Lab-Rat** stamps: slope COL hooks (`pbr=tint`) **landed #81** vertex albedo only (Hypha owns that bind). Slope/PBR/dirt/scatter/deform plugs **landed #80** — `classify_slope` + DISP bake-down + `Deform` / `GroundScatter` filled at #81 XZ (`8,-6` / `-10,14`). Blender UV dials **landed #101** — scale X/Y · offset X/Y · rotate (CCW about +Y) on stamp/PBR/grit; identity default keeps today's yard; `FULCRUM_UV`; texture tiles only, never geo / never Transvoxel shrink. Hypha #112 `lod_mips::promote_for_uv` + TerrainHost wear/COL honor the same `uv::xform` on Transvoxel skin. Subtract crawl pad network **landed #114** — shallow mouth→pocket Subtract under the pad (`CRAWL_DROP` **0.38** m; glasses `CRAWL  SUBTRACT`). Full guts / live voxel collide still `[~]`. Probe consume **landed #127** — `fulcrum.probes` → `apply_to_layers` at bake (not a second mesher). Sandbox pedon **landed #130** — off-stream leftover CHANNELS slab; tap **F** rebake; `StampField::layers` / `stream_rev` stay cold. Extract player spawn loci **landed #132** — 8 rim pads facing center → `World.player_spawns` (#132 shipped Chebyshev **144 m** on the 19×19; live rim **288 m** via **#142** `probes::rim_radius_m()`); Home **P** + SPWN `kind:spawn` override within **48 m** XZ else append; #128 stays the Augury writer; Beabim pool / knock-off **later landed #133**. Pad crawl stays **#114**. STREAM remesh stays Hypha **#123**. Stamp pad stays **7×7**. Stamp / building / terrain PBR polish **landed #144** — rocks 3-lobe shade/face/chip · buildings Concrete + face UVs · default `pbr=vendor` 256² COL (tighter tiles / grit on building faces) · five thumbs + concrete NRM. Texture+UV only; chunk **16 m** held. NRM/GLOSS GPU parked. Evan **clean** yelled 2026-09-08 ~00:00 ET — atelier plugs **open**. Atelier **150 roughness + textures/PBR ~26 sets landed**. #58/#60/#80/#101/#112/#144 stay the live yard plugs. Holocron rust rewrite still waits on SVG / density-mask / monolith splits — see `TOOLS.md`
- **Range Tech**: kits + FX draw-distance on the wider yard; kit metal/grit PBR stub **landed #64**; store `dBXpg` still **open**; Music playlist beds **landed #64**; ADS viewmodel DoF **landed #68**; heat dial blend **landed #71**; **CE tip 0.2.8 lock landed #129** (past #71 blend; #66 path; #89 untouched); land sway + heightfield FX **landed #79**; Options Audio DEVICE **landed #82**; dirt Hit pool + world FX mono fold **landed #134** (`Slot::HIT_POOL` distant dirt trio; `DecodeFold::WorldMono` on `Bus::Fx`; Music/UI keep stereo); H shoulder-swap tilt **landed #84**. Patch A RH hip bias **landed #94** (first +0.08; live hip **superseded #98**). Aim-offset tuner + attachment sockets **landed #97** (live **End** sheet / glasses `AIM TUNE`; Home debugger **later landed #110**; authored defaults now **#98**). **AIM TUNE live-save landed #103** (Hypha `project.json`; `aim_live` default **true**; partial merge keeps #98/#99/#100; #97 End stays). **AIM TUNE PX travel landed #138** (`shoulder_x_max` **±0.50**; leftover +0.226 must not cap End +X; H still `shoulder_x_min` only). **Wound feel / 1P screen-react landed #143** (suppress-near / armour / HP; Hypha `post.wound` [blur, red]; hooks KIND_PVP Hit not Sync; Death/Slain **later landed #146**). **Canted optic + AIM TUNE ATTACH landed #150** (1P silhouette; ATTACH OPTIC→CANTED→CAN; live-save `attachments.canted`; rail roll **−0.785**; `ads_cant` held). RH hip one more body-width + ready-hip Y **landed #98** (hip **0.2403 / −0.2128 / −0.1833**; `shoulder_cross_x` **−0.281**). Low-hip shotgun stance **landed #99** (`hip_low` MP9-Z **0.2403 / −0.3528 / −0.1513** / pitch **0.145**; glasses **LOW HIP**; LowHip ADS still irons). Canted 45° Greyzone CQC ADS **landed #100** (`ads_cant` MP9-Z **0.0423 / −0.148 / −0.136** / yaw **0.11**; U+RMB / Mouse5 @ 60° CQC; glasses **CANT 45** / **CANT ADS**). U-cycle hold springs **landed #109** (`hold_spring` **7.0**; STEAL_MAP pose-ease → **in**; glasses snap; viewmodel eases). Kit handling / ergo / MOA **landed #113** (`HandlingStats` / `FeelSheet::handling`; ADS blend **6.4** × kit ergo; handling → recoil `1/handling`; hip MOA after `hip_honest_dir`; ADS × **0.22**; `hold_spring` **7.0** stays sibling). HDRI sun disc **landed #87** (shared Hypha; dump **sunSize 0.62** rides the disc). Projectile feel **landed #89** (rect slab + debris + slug/wake + punch/scuff flash + fire-pulse glyphs — Vector mag dump live steal; artistic frame still `VECTOR_MAG_DUMP.md`). Heat cards / ballistics / binds **not touched** by #81. Heat / binds / ballistics / Audio DEVICE **not touched** by #86 / #87. #89 did **not** retune HeatDials / SIM / AXIS_LOCK +Z / #79 snap. Live HeatDials are **#129**
- **Augury**: FoW brand / menu video **when cut ready**. Chrome **not touched** by #81 / #86 / **#90**. Death/Slain **landed #146** (PvE envelope · Slain plate · PRESS SPACE; PVP down does not play Slain). Elbow smart-labels **landed #85** (EXTRACT elbow card, no popup). Hatch toggle + shaft ride **landed #115** (hold-F OPEN/CLOSED + RIDE/EXIT; hold-O `EXTRACT  OPEN|CLOSED|SHAFT`; no modal popup; timed surface kill still **~**). Door / extract cancel chrome **landed #120** (**F** arms `GATE_SECS` **2.20**; OPEN hatch arms extract-out; walk-away cancels; timed surface kill still **~**; KIND_RAID leftover **later landed #122** — Beabim; timer = `GATE_SECS` **2.20**; glasses stay Augury). CE Home debugger **landed #110** (**Home** toggle · LOGS / TELE / CHEAT · hitch logger; End stays AIM TUNE; glasses `DEBUG`). Home LOGS COPY + tracker toggles **landed #121** (**Enter** COPY · ring **800** · timestamps · Insert/Delete tracks · `log_*` persist default on · medium edge events). Home occlusion + 3D probes + COLL/PERF/SPWN **landed #125** (**P** look-at probe · Enter `fulcrum.probes` · tabs COLL/PERF/SPWN · chrome fills under glyphs · soft Enter debounce **0.45s**; Lab-Rat consume **later landed #127**; Range tip/optic consume stay **·**). Home binds lock + spawn + denser STREAM **landed #128** (Home cycles off→tabs→off · arrows/Enter · Ins pages · no WASD/Space; `name:ground`; `kind:spawn` via SPWN+P; denser WALK/STREAM hang tags — not hitch *fix*). FoW pixellation aesthetic note only — Hypha owns the post dial **#90**

Do **not** claim NRM/GLOSS GPU, whole roughness→stamp, full world replication / terrain sync, Range heat, `dBXpg`, full metal-tech kits, menu video, Mixamo clip import / GPU skin / player body, 2-bone IK, mesher rewrite, **LPVO**, or **scope glass** shipped. 8× open extract + wall drop + chunk stream + slope COL **are** shipped #81. Next ~4× area + pend coalesce **are** shipped #142 (37×37 · STREAM held 11×11 · `coalesce=2/2` · rim 288 m — not a STREAM_RINGS bump). Lab-Rat slope/PBR/dirt/scatter/deform plugs **are** shipped #80. Lab-Rat Blender UV dials **are** shipped #101 (texture tiles only — never geo / never Transvoxel shrink). Hypha Transvoxel UV consume **is** shipped #112 (texture-only — never remesh / never chunk shrink). Lab-Rat stamp / building / terrain PBR polish **is** shipped #144 (rocks 3-lobe shade/face/chip · buildings Concrete + face UVs · default `pbr=vendor` 256² COL · five thumbs + concrete NRM — muddy terrain / shitty buildings closed; texture+UV only; chunk 16 m held; not STREAM / remesh / NRM-GLOSS GPU). Lab-Rat subtract crawl pad network **is** shipped #114 (shallow enterable network — not full guts / live voxel collide / tunnel sim). Peer feet stream anchors + HOLD JOIN **are** shipped #83 (pose presence). Invite leftover + peer names + biped hip gun stub **are** shipped #91 (not full 3P kit honesty). Live-profile loot trail **is** shipped #102 (KIND_LOOT; not Range feel / hatch / PreferredHand). World/sim leftover **is** shipped #119 (KIND_SHOT / KIND_LOCUS / KIND_BODY; peer shot muzzle = biped hip stub; joiner plants soles only — not Range feel / knife-rally / joiner slash / stabilize / stamps / hatch / full PvEvP / dedicated infra). No-pause live sim + KIND_RAID shared instance **is** shipped #122 (mute local pawn only; leftover = `GATE_SECS` **2.20**; honors `Cancelled` — not glasses HOLD % rewrite / Range feel / Mixamo / full PvEvP). PVP leftover **is** shipped #133 (KIND_PVP default off · hide names · KIND_BRASS · eye 1.60/1.62 · rim respawn 1.20 s — not Range eject retune / not Hypha #131 (later landed separately) / not Lab-Rat stamps / not Augury Home / not server browser). HOST session board / no-127 invite **is** shipped #139 (title HOST PVP radio pre-enter · settings lock · LAN bind prefer — no 127 seed; typed `--join 127` still works — not Augury hatch/Home / not Range AIM TUNE / not Lab-Rat stamps / not Hypha PeerBody (later landed #131) / not server browser). PVP honesty **is** shipped #141 (`PeerBody::hurtboxes()` leftover · hurt skin **0.06** + sweep **4** · HP/AR Sync · unique pads host **0** / occupancy **16 m** — not Range eject retune / not Hypha STREAM / not Lab-Rat stamps / not Augury Home / not server browser). Leftover ray **is** shipped #147 (`LEFTOVER_HIT_M` / `first_leftover_hit` **500 m** was 80 · flat `SMG_PELLET` **14** · Locus yard keeps own 80 — not Range falloff / not Hypha STREAM / not Lab-Rat stamps / not Augury death / not server browser). Wound feel / 1P screen-react **is** shipped #143 (suppress-near soft short blur · armour jostle + soft blur no red · HP stronger jostle + blur + red fade · envelope `--===--------` · never full-strength blur · 1P local; Hypha `post.wound` [blur, red]; hooks Hit not Sync — not Beabim net damage / not #141 Sync punch / not Augury Death/Slain / not AIM TUNE / not heat lattice). Music playlist beds **are** shipped #64. Kit metal/grit PBR stub **is** shipped #64. Options Audio DEVICE **is** shipped #82. Dirt Hit pool + world FX mono fold **are** shipped #134 (`Slot::HIT_POOL` n≥3; WorldMono on Fx; Music/Voice keep stereo — not Augury spatial rewrite / not CREDITS). Hypha Graphics dump **is** shipped #86 (fog 375/520 · cam 0.05/2000 · clouds 0.63 · sunPunch 0.51 — not bloom / god-rays). HDRI sun disc **is** shipped #87 (sunSize **0.62** rides the disc). Biped plant + host hooks **are** shipped #88 (STEAL_MAP biped **partial**). Landmark AABB ride **is** shipped #136 (`RIDE_STEP` **0.50** · `RIDE_SKIN` **0.06** · `SUPPORT_STEP` **0.25** unchanged — walls-as-floor only in the ride band; Locus hurtboxes stay walls; hop onto / land **later landed #149** vertical before XZ — no extra hop dial; 3 m compounds stay walls; #88 plant / STREAM / Lab-Rat stamps untouched — do **not** claim Range / Beabim / Lab-Rat / Augury shipped this). Landmark ride hop **is** shipped #149 (vertical before XZ; same #136 band; no extra hop dial — do **not** claim Range / Beabim / Lab-Rat / Augury shipped this). 3P biped / PeerBody **is** shipped #131 (`EYE_Y` **1.60** · `HEAD_H` **1.62** centered · left-offset killed · ragdoll flop **0.55 s** — not Range AIM TUNE / not Beabim KIND_* / not Mixamo / not 2-bone IK). 3P torso lean match **is** shipped #145 (`LEAN_LATERAL` **0.5** · `LEAN_HINGE_Y` **0.55** · `LEAN_ANGLE` **0.52** · `LEAN_SMOOTH` **9.5** · pelvis/spine/chest — not a 0.14 m full-body slide / not a 1P AIM TUNE rewrite). Projectile feel **is** shipped #89 (rect slab + debris + slug/wake + punch/scuff flash + fire-pulse glyphs — not a ballistics rewrite). Heat CE tip **0.2.8 is** shipped #129 (past #71 blend; #66 colorless path; #89 untouched — no fog blob). RH hip bias **is** shipped #94 (first +0.08; live hip **superseded #98**). Aim-offset tuner + attachment sockets **is** shipped #97 (live End sheet; Home debugger **later landed #110** — End stays AIM TUNE; authored defaults now **#98**). AIM TUNE live-save **is** shipped #103 (End LIVE → Hypha `project.json`; `aim_live` default **true**; partial merge; End stays AIM TUNE — not RECORD bind / bake-permanent-defaults / UV / Beabim / heat). AIM TUNE PX travel **is** shipped #138 (`shoulder_x_max` **±0.50**; leftover +0.226 not an End cap; H still `shoulder_x_min` only; authored hip / H dest / #103 live-save / `hold_spring` / ADS blend untouched). CE Home debugger **is** shipped #110 (**Home** toggle · LOGS / TELE / CHEAT · hitch WARN/HITCH; native overlay — hitch *visibility* only; hitch *fix* **later landed #108** · worker/paint/gpu deepen **later landed #123**; binds lock + spawn + denser STREAM **later landed #128** — not CE heartbeat flags / End tuner changes). Home LOGS COPY + tracker toggles **is** shipped #121 (**Enter** COPY · ring **800** · `[sssss.mmm]` · Insert/Delete tracks · `log_*` persist default on · medium edge events — #110 stays the tabs+logger foundation; binds lock + spawn + denser STREAM **later landed #128**). Home occlusion + 3D probes + COLL/PERF/SPWN **is** shipped #125 (**P** look-at · Enter `fulcrum.probes` cap **32** · tabs COLL/PERF/SPWN · chrome occlusion — not End AIM TUNE / hitch *fix* rewrite / Range tip consume; Lab-Rat consume **later landed #127**). Home binds lock + spawn + denser STREAM **is** shipped #128 (Home cycles off→tabs→off · arrows/Enter · Ins pages · no WASD/Space; `name:ground`; `kind:spawn` via SPWN+P; denser WALK/STREAM hang tags — not hitch *fix* / Lab-Rat bake loci (**later landed #132**) / Range AIM TUNE / PVP hitboxes). Lab-Rat probe consume **is** shipped #127 (`FULCRUM_PROBES` / cwd `fulcrum.probes` → `apply_to_layers`; kind routing terrain sit · wall lip · hole/overhang Subtract; `probes=off` if missing — not a second mesher / not Home chrome / not Range tip consume). Lab-Rat sandbox pedon **is** shipped #130 (off-stream leftover CHANNELS slab; tap **F** rebake; glasses `PEDON  F  REBAKE  GEN n` — not Home chrome / not #114 pad crawl / not Hypha STREAM remesh / not Range / Beabim). Lab-Rat extract player spawn loci **are** shipped #132 (8 rim pads → `World.player_spawns`; #132 shipped **144 m** on the 19×19; live rim **288 m** via **#142**; **48 m** XZ override/add; #128 writer of `kind:spawn` — not Beabim pool / knock-off / PVP / respawn UI / biped eye / second MP KIND). Stream hitch amortize **is** shipped #108 (cook=1/2 · prefetch=5 m · splash-pumped load-in — not live octree / unconstrained Sync 9×9 dump). Worker STREAM extract+paint **is** shipped #123 (`defer=worker/paint/gpu` · skip far mask-only remesh — hitch thread never `sample_channels` on play extract; CHANNELS stay bake-time; no debugger rewrite). Play STREAM 11×11 + warm hold **is** shipped #137 (`STREAM_RINGS` **5** · prefetch=5+heading · hold=2/12 — not a new map size; #108/#123 hitch layers stay; flush/smoke still drop). 4× world + pend coalesce **is** shipped #142 (37×37 / 592 m / 350 464 m² · rings 18 · `coalesce=2/2` · rim **288 m** — STREAM held 11×11; stamp pad stays 7×7). RH hip one more body-width + ready-hip Y **is** shipped #98 (hip **0.2403 / −0.2128 / −0.1833**; `shoulder_cross_x` **−0.281** / `shoulder_cross_y` **0.032** — not a mesh mirror). Low-hip shotgun stance **is** shipped #99 (`hip_low` MP9-Z **0.2403 / −0.3528 / −0.1513** / pitch **0.145**; U-cycle glasses **LOW HIP**; RMB from LowHip = iron ADS — not chin-weld). Canted 45° Greyzone CQC ADS **is** shipped #100 (`ads_cant` MP9-Z **0.0423 / −0.148 / −0.136** / yaw **0.11**; U+RMB / hold-Mouse5 @ 60° CQC; glasses **CANT 45** / **CANT ADS** — not a canted-holo mesh / IOR glass). U-cycle hold springs **is** shipped #109 (`hold_spring` **7.0**; STEAL_MAP pose-ease → **in**; glasses still snap CHEST / LOW HIP / CANT 45; viewmodel eases — not Beabim/3P / heat / terrain / PreferredHand / ADS blend folded into `hold_spring`). Kit handling / ergo / MOA **is** shipped #113 (`HandlingStats` drives existing 1P fire/ADS dials; ADS `blend_speed` **6.4** × kit ergo; handling → recoil; hip MOA after `hip_honest_dir`; ADS × **0.22** — not house mastery / gear UI / Beabim 3P / heat rewrite / PreferredHand / Augury Home). Hatch toggle + shaft ride **is** shipped #115 (hold-F OPEN/CLOSED + shaft RIDE; no modal popup — timed surface kill still open). Door / extract cancel chrome **is** shipped #120 (**F** arms `GATE_SECS` **2.20**; OPEN quiet hatch arms extract-out; walk-away cancels — timed surface kill still open; KIND_RAID leftover **later landed #122**). PreferredHand + new-profile onboard **is** shipped #116 (Right default · NEW PROFILE gate · `project.json` permanent vs live · death clears live · extract→stash stub · H seats Range crossover, no mesh flip — not full PMC stash / character tab / world-pool death loot / Beabim net sync of PreferredHand). Pixellation / floor-warp **is** shipped #90 (Hypha post dial `warp_strength` **0.01**; Options **WARP**; STEAL_MAP Augury pixellation **partial**; Augury aesthetic only — do not steal into Range). See `TERRAIN_NORTHSTAR.md`.

## Open — texture / atelier leftovers (roughness→stamp still open)

Range Tech Evan peek feel **landed #59**. Hypha ring-mip texture LOD **landed #60**. Hypha near LOD raise **landed #61**. Range Tech handmade atelier SFX vendor **landed #62**. Range Tech music playlist + kit metal/grit PBR stub **landed #64**. Hypha colorless muzzle heat **landed #66** (sample-only `heat_warp_uv` on the #55 post stack — lattice is post input only; no world-pipeline orange card). Range Tech Patch A muzzle **landed #67** (kit-tip spawn + `hip_honest_dir` + tip→impact streak clamp — hip-fire no longer behind the handguard / upper-right of the reticle; did not fight #66). Range Tech ADS viewmodel DoF **landed #68** (ADS near + far on the same #55 pass / Options **DOF**). Range Tech heat dial blend **landed #71** (was→now→stolen on the #66 post path — haze **0.07** / size **0.83** / scaleX **0.396** / lobe **0.698**; DNA / not live). Live HeatDials **landed #129** CE tip 0.2.8 (haze **0.01** / size **0.99** / scaleX **0.28** / lobe **0.40**; #66 colorless path stays; no fog blob). Range Tech SIM-only launch **landed #76** (arcade aim-dir + **P** toggle dead; leftover `hob_zero` ignored). Range Tech hold-O extract / **−/=** zero / grounded slide **landed #78** (**O** is **not** zero; Augury EXTRACT elbow card **landed #85** — no popup. Hatch toggle + shaft ride **landed #115**; timed surface kill still **~**). Range Tech land sway softener + heightfield FX **landed #79** (punch **0.028** / duck **0.08** / shake **0.14** gate **13** + inertia sway; hop 12/30/1 **unchanged**; brass/tracers/marks snap to extract heightfield — no flat `floor_y` / pawn feet). Hypha first big-map **landed #81** (19×19 open + stream + slope COL `pbr=tint`). Live host **#142** (37×37 / 592 m / ~350k · `coalesce=2/2` · rim 288 m). Play STREAM **11×11** + warm hold **landed #137**. Hypha stream hitch amortize **landed #108** (cook=1/2 · prefetch=5 m · splash-pumped load-in). Hypha worker STREAM extract+paint **landed #123** (`defer=worker/paint/gpu` · skip far mask-only remesh). Range Tech Options Audio output DEVICE **landed #82** (SYSTEM DEFAULT via cpal `default_output_device()`; A/D or arrows / Enter / click cycle; persist `output_device`; same #21 mixer → thin cpal voice). Range Tech dirt Hit pool + world FX mono fold **landed #134** (`Slot::HIT_POOL` distant dirt trio; `DecodeFold::WorldMono` on `Bus::Fx`; Music/UI keep stereo; `hit.wav` retired leftover). Range Tech H shoulder-swap tilt **landed #84** (tilt path; live left hold **#94** slight straighten pitch/yaw/roll **0.04 / 0.10 / 0.08**, supersedes #84 chest-cross 0.08/0.32/0.39; travel dest ~−0.041 / `shoulder_x_min` **−0.055** / ads_keep **0.32**; not a mesh mirror / no `scale.x = −1`; PreferredHand onboard **later landed #116**). Range Tech Patch A RH hip bias **landed #94** (first +0.08; live hip **superseded #98**; ADS X / tip spawn / `hip_honest_dir` / #89 tracers stay). Range Tech aim-offset tuner + attachment sockets **landed #97** (**End** toggle; Insert WEAPON↔ATTACH; PageDown pose/attachment; PageUp step; Delete JSON; glasses `AIM TUNE`; Home debugger **later landed #110**; authored defaults now **#98**). Range Tech AIM TUNE live-save **landed #103** (End LIVE flush → Hypha `project.json` `aim_live` / `aim_tune.example_smg` / `example_rifle` / `example_sniper`; pose `{x,y,z,rotX,rotY,rotZ}`; attach optic/can; load on Deploy; partial merge keeps #98/#99/#100; Delete dump stays #97; RECORD stub — no bind). Range Tech AIM TUNE PX travel **landed #138** (`shoulder_x_max` **±0.50**; leftover +0.226 must not cap End +X; H still floors at `shoulder_x_min` only; authored hip **+0.2403** / H dest **~−0.041** / #103 schema / `hold_spring` / ADS blend untouched). Range Tech wound feel / 1P screen-react **landed #143** (suppress-near soft short blur · armour jostle + soft blur no red · HP stronger jostle + blur + red fade · envelope `--===--------` · never full-strength blur · 1P local; Hypha `post.wound` [blur, red]; hooks KIND_PVP Hit not Sync; Death/Slain **later landed #146**). Range Tech canted optic + AIM TUNE ATTACH **landed #150** (1P only; ACOG/SCOPE 45° offset holo; ATTACH OPTIC→CANTED→CAN; `attachments.canted`; rail **−0.785**). Range Tech RH hip one more body-width + ready-hip Y **landed #98** (MP9-Z hip **0.2403 / −0.2128 / −0.1833**; `shoulder_cross_x` **−0.281** / `shoulder_cross_y` **0.032**; left pitch/yaw/roll **0.04 / 0.10 / 0.08** unchanged). Range Tech low-hip shotgun stance **landed #99** (MP9-Z `hip_low` **0.2403 / −0.3528 / −0.1513** / pitch **0.145**; SR-25 **−0.364 / −0.176 / 0.148**; M24 **−0.369 / −0.196 / 0.146**; glasses **LOW HIP**; LowHip ADS still irons). Range Tech canted 45° Greyzone CQC ADS **landed #100** (MP9-Z `ads_cant` **0.0423 / −0.148 / −0.136** / pitch/yaw/roll **0.024 / 0.11 / 0.785**; SR-25 / M24 **0.0468 / −0.154 / −0.148**; U+RMB / hold-Mouse5 @ 60° CQC; glasses **CANT 45** / **CANT ADS**). Range Tech U-cycle hold springs **landed #109** (`hold_spring` **7.0** on the existing ADS / H / sprint exp-approach path; H `shoulder_spring` **8.0** / sprint **6.2** unchanged; glasses still snap; first-U seed-before-cycle; STEAL_MAP pose-ease → **in**; ADS `blend_speed` **6.4** stays its own dial — **#113** scales it by kit ergo). Range Tech kit handling / ergo / MOA **landed #113** (`HandlingStats` / `FeelSheet::handling`; ADS blend **6.4** × ergo — MP9 **8.00** / SR-25 **6.40** / M24 **5.12**; handling → recoil `1/handling`; hip MOA after `hip_honest_dir`; ADS × **0.22**; `hold_spring` **7.0** stays sibling). Hypha pixellation / warp strength floor **landed #90** (`PostToggles.warp_strength` default **0.01**; Options Graphics **WARP** after CAM FAR; persist `project.json` `{:.2}` → `0.01`; `pixel_warp_uv` after `heat_warp_uv`; smoke `gfx=` appends ` warp=0.01` only; existing `fog/375/520 cam=0.05/2000` substring stays; STEAL_MAP Augury pixellation **partial**; Augury aesthetic only — do not steal into Range). Hypha Graphics dump **landed #86** (Options **FOG / FOG NEAR / FOG FAR / CAM NEAR / CAM FAR** + persist `project.json`; extract haze 375/520 · cam 0.05/2000 · clouds **0.63** · sunPunch **0.51**; hideout `haze_max` **0**; bloom / godRays / brightness / gamma **no path**). Range Tech + Hypha HDRI sun disc **landed #87** (dump **sunSize 0.62** rides the procedural disc/halo; plate solar-region tone + soft disc — not a second sky). Augury elbow smart-labels **landed #85** (embodied card + L-elbow to interact pin; hold-O EXTRACT, no popup). Hatch toggle + shaft ride **landed #115** (hold-F OPEN/CLOSED + RIDE; hold-O `EXTRACT  OPEN|CLOSED|SHAFT`; no popup; timed surface kill still **~**). Door / extract cancel chrome **landed #120** (**F** arms `GATE_SECS` **2.20**; OPEN hatch arms extract-out; walk-away cancels; timed surface kill still **~**; KIND_RAID leftover **later landed #122**). Augury CE Home debugger **landed #110** (**Home** toggle · LOGS / TELE / CHEAT · hitch WARN >33 ms / HITCH >100 ms · glasses `DEBUG`; End stays AIM TUNE). Home LOGS COPY + tracker toggles **landed #121** (**Enter** COPY · ring **800** · `[sssss.mmm]` · Insert/Delete tracks · `log_*` persist default on · medium edge events). Home occlusion + 3D probes + COLL/PERF/SPWN **landed #125** (**P** look-at probe · Enter `fulcrum.probes` · tabs COLL/PERF/SPWN · chrome fills under glyphs · soft Enter debounce **0.45s**). Home binds lock + spawn + denser STREAM **landed #128** (Home cycles off→tabs→off · arrows/Enter · Ins pages · no WASD/Space; `name:ground`; `kind:spawn` via SPWN+P; denser WALK/STREAM hang tags). Hypha biped foot plant **landed #88** (heightfield column; FOLLOW **8.5** / DEADZONE **0.04** / RISE **2.2** / SINK **6.5** / SNAP_ERR **1.15** / LIFT_MAX **0.14** / BOOT_HALF_H center **0.11**; Mixamo sockets Pelvis / Foot_L / Foot_R / Head host hooks only; STEAL_MAP biped **partial**). Hypha landmark AABB ride **landed #136** (`RIDE_STEP` **0.50** · `RIDE_SKIN` **0.06** · `SUPPORT_STEP` **0.25** unchanged; `ride_surface_y` = max(heightfield, AABB top); walls-as-floor only in the ride band; Locus hurtboxes stay walls; peers `plant_simple_root_on` same column; #88 FOLLOW/DEADZONE stay; STREAM / Lab-Rat stamps untouched). Hypha 3P biped / PeerBody **landed #131** (`EYE_Y` **1.60** · `HEAD_H` **1.62** · XZ **0** left-offset killed; crouch squat **0.62** · ragdoll flop **0.55 s**). Hypha 3P torso lean match **landed #145** (`LEAN_LATERAL` **0.5** · `LEAN_HINGE_Y` **0.55** · `LEAN_ANGLE` **0.52** · `LEAN_SMOOTH` **9.5** · pelvis/spine/chest; feet planted — not the old 0.14 m full-body slide). Lab-Rat slope/PBR/dirt/scatter/deform plugs **landed #80** (`classify_slope` + DISP bake-down + deform/scatter filled; smoke `pbr=tint plugs=slope+deform+scatter`). Lab-Rat Blender UV dials **landed #101** (`engine/src/uv.rs` scale/offset/rotate; identity default; `FULCRUM_UV`; smoke `uv=1.00,1.00+0.00,0.00 r=0`). Hypha Transvoxel UV consume **landed #112** (`promote_for_uv` + TerrainHost wear/COL honor; texture-only). Lab-Rat subtract crawl pad network **landed #114** (shallow mouth→pocket Subtract; `CRAWL_DROP` **0.38** m; glasses `CRAWL  SUBTRACT`; full guts still `[~]`). Lab-Rat probe consume **landed #127** (`FULCRUM_PROBES` / cwd `fulcrum.probes` → `apply_to_layers`; `probes=off` if missing). Lab-Rat sandbox pedon **landed #130** (off-stream leftover slab; tap **F**; smoke `pedon=gen=1`). Lab-Rat extract player spawn loci **landed #132** (8 rim **144 m** → `World.player_spawns`; **48 m** override/add; Beabim pool still open). Range Tech projectile feel **landed #89** (rect slab + 4–6 debris / visualLength **1.5 / 18** / core **2.85 / 2.25 / 0.95** / slug **0.07** / wake 1–2 / hit flash **0.15** s / punch **8–12** / scuff **4–6** / fire-pulse glyphs; SIM #76 + AXIS_LOCK +Z + #79 snap unchanged; HeatDials **later landed #129**). Beabim live-profile loot trail **landed #102** (KIND_LOOT host-relayed Z/F; hairline crumbs; starting kits stay local; shoot / Locus leftover / death bag **later landed #119**). Beabim world/sim leftover **landed #119** (KIND_SHOT / KIND_LOCUS / KIND_BODY; peer shot muzzle = biped hip stub; joiner plants soles only; Range feel / HoB / heat / brass / knife-rally / joiner slash / stabilize / stamps / hatch stay local). Beabim no-pause + KIND_RAID **landed #122** (mute local pawn only; leftover = `GATE_SECS` **2.20**; honors `Cancelled`; glasses stay Augury). Beabim PVP leftover **landed #133** (KIND_PVP default off · hide names · KIND_BRASS · eye 1.60/1.62 · rim respawn). Beabim HOST session board + no-127 invite **landed #139** (title HOST PVP radio pre-enter · settings lock · LAN bind prefer — no 127 seed). Beabim PVP honesty **landed #141** (`PeerBody::hurtboxes()` leftover · HP/AR Sync · unique pads). Beabim leftover ray **landed #147** (`LEFTOVER_HIT_M` **500 m** was 80 · flat `SMG_PELLET` **14** · Locus yard keeps own 80). Further roughness→stamp still open (SVG / density-mask / experiment-log). Do **not** claim the whole roughness→stamp cook. Do **not** claim NRM-GLOSS GPU or `dBXpg` shipped.
- **Texture compression** — atelier roughness packs are **4k 48-bit PNG** (too large). Do **not** ship raw 4k 48-bit into the yard. Lab-Rat **#58 landed** the vendored near packs (256² bake-downs under loud scars). Hypha LOD-tied mips **landed #60** on Transvoxel **distance rings** (near 256² / mid 64² / far 16²; far drops grain hashes). Blender UV dials **landed #101** — tile those packs without shrinking geo. Hypha Transvoxel UV consume **landed #112** (`promote_for_uv` + wear/COL honor). In-repo grit mips stay #60 until Lab-Rat cooks more. Do **not** claim the whole roughness→stamp cook
- **Atelier** — plugs **open** (Evan **clean** yell 2026-09-08 ~00:00 ET). PBR batch **in** (150 roughness + textures/PBR ~26 sets). #58 optional `FULCRUM_GRIT=` / `FULCRUM_ATELIER=` stay read-only **load** paths. Crew may plug; bake-down first. `FULCRUM_UV` is Lab-Rat tile override, not an atelier write
- **Lab-Rat** — **#58 quiet grit greyscales landed** (vendored bake-downs + `sample_channels` quiet height + `grit::rough` wear — the near source for #60). Slope/PBR/dirt/scatter/deform plugs **landed #80** (DISP bake-down + `Deform` / `GroundScatter` filled). Blender UV dials **landed #101** (scale/offset/rotate; identity default; `FULCRUM_UV`; texture-only). Hypha Transvoxel UV consume **landed #112** (`promote_for_uv` + wear/COL honor). Stamp / building / terrain PBR polish **landed #144** (default `pbr=vendor` 256² COL · face UVs · 3-lobe rocks — muddy terrain / shitty buildings closed). Subtract crawl pad network **landed #114** (shallow enterable Subtract under the pad — not a tunnel sim). Probe consume **landed #127**. Sandbox pedon **landed #130** (off-stream leftover overlay — STREAM stays Hypha #123; pad crawl stays #114). Extract player spawn loci **landed #132** (8 rim pads; live **288 m** via **#142** → `World.player_spawns`; Beabim pool / knock-off **later landed #133**). Slope COL hooks reserved on host **#81** (vertex albedo only — Hypha owns that bind). Further roughness → stamp stays on **fulcrumRust only**; bake-down first. SVG / density-mask / experiment-log still open. Holocron rust rewrite still waits on those leftovers (`channels.rs` / stamp stacks / `feel` / `kit_mesh`) — see `TOOLS.md`
- Day-one FILE_SLOTS vendor **landed #62**. **SFX remix DNA** — creative reuse OK (pitch/speed/effects; indie underground; don’t overuse the same stem). First application **landed #64** — fire/foot/reload ±6% pitch/speed jitter on the #62 vendor; **#134** also jitters **hit**. Full remix minting still **open**. **Music** playlist beds **landed #64** (five titled beds; hideout+extract advance shuffle; Options Music dial; missing → two-tone stub; **#134** Music keeps stereo). Options **Audio** DEVICE cycle **landed #82** (SYSTEM DEFAULT; persist `output_device`; missing pin kept, playback falls back to OS default; same #21 mixer → thin cpal voice — not a second mix tree). Dirt Hit pool + world FX mono fold **landed #134** (`Slot::HIT_POOL` distant dirt trio; random n≥3; missing/bad → remaining pool then procedural grit; `DecodeFold::WorldMono` on `Bus::Fx`; Music/Voice keep stereo; retired leftover `assets/sfx/hit.wav` not loaded). Shot propagation / full CE pack dump still later — that is audio files, not the #59 feel dials

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
- **Hard check** — SMG fire SFX respect FX bus (FX `0` silent; half quieter); file-slot wiring shipped #54; handmade vendor landed #62 (missing → procedural). Dirt Hit pool + WorldMono fold **later landed #134**
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
- File-slot wiring shipped #54; handmade vendor landed #62; World FX L+R→mono on decode **later landed #134** (`DecodeFold::WorldMono` on `Bus::Fx`; Music/Voice keep stereo). Shot propagation later. Detail: house `EXTRACTION_AUDIO_LOCK.md` + fulcrumRust `engine/src/audio.rs`

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
- **Host** — title **HOST** (or **Y** while alive in hideout/extract) binds UDP and mints `fulcrum://ip:port`; `--host` arms title cursor and also listens after Deploy. **#139** title HOST opens SESSION board (PVP radio) before Deploy/enter; `--host` + title Deploy / **Y** still skip the board
- Default port **7777** (`FULCRUM_PORT` override). LAN iface if OS has one, else loopback
- **Join** — `--join fulcrum://ip:port` (also bare `host:port` and `fw://`); env `FULCRUM_JOIN`. Title **JOIN** confirms. Then no in-game text field. **#83** adds in-pause **JOIN** panel (Esc → JOIN → type invite → Enter; title JOIN without `--join` opens the same sheet). **#91** leftover INVITE sheet + `fulcrum.invite` seeds the JOIN field. **#139** prefer LAN — no 127 placeholder; typed `--join 127` still works if typed
- Glasses labels only: `HOST  ip:port`, then `JOIN` / `PEER` after HELLO/WELCOME — never a second ammo HUD. **#83** keeps those labels. **#91** glasses `HOST  fulcrum://ip:port`
- Honesty: then handshake / presence only. **#83** adds UDP **POSE** presence (~20 Hz feet/yaw/pitch). **#91** extends POSE with muzzle `xyz` + gun yaw/pitch. **#102** adds KIND_LOOT kit trail. **#119** adds KIND_SHOT / KIND_LOCUS / KIND_BODY leftover — host-authoritative shot / Locus / death bag. **#122** adds no-pause mute-local-only + KIND_RAID shared-instance leftover (`GATE_SECS` **2.20`; honors `Cancelled`); **#133** adds PVP leftover; **#139** adds HOST session board + no-127 invite seed; **no** full world replication / terrain/audio rewrite / PvEvP sim
- Solo **Deploy** unchanged (`net=off` on smoke)
- Intact / do not steal: **I** stim (#37), hold-**O** extract intent (#78), **−/=** zero (#78), **P** unused (#76), hold-**J** heat-tune (#35), T/C/R/Q/E/Z/B/V/N/U/`/F/M/1/2/3/Mouse4
- Bind: **Y** alive host only (#34). Stim is **I** while downed (#37). Seats do not fight — downed Y is a no-op for host and stim.
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust STEAL_MAP Net row (todo→partial). PVP leftover: Closed by #133. HOST session board / no-127 invite: Closed by #139. PVP honesty: Closed by #141. Leftover ray: Closed by #147

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
  3. **Hideout door** — keep **F** prompt; walk-into-door no longer auto-deploys. Must press F. **Later landed #120** — F arms `GATE_SECS` **2.20** countdown (not instant deploy); walk away cancels
  4. **Jump** — **Space** single hop shipped #51. **Superseded #59:** CE hop + one air hop + land duck / shake. Prior FPS-first "no double-jump" / single-jump-only is superseded (same way #51 superseded earlier "no jump")
- Do not unify the three forwards to "fix" FX. #12 look/move/gun + tracers and #25 wall clamp / spring / yard covers stay. Lean sign + depth live on #59
- Detail: house `AXIS_LOCK.md` + `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust `docs/AXIS.md` / `engine/src/axis.rs`

## Closed by fulcrumRust #54 (2026-09-07)

- **Authored SFX file slots** — Range Tech feel-lab `sfx.slots[id]` on the **same** #21 FX bus (not a second mixer). `mixer.play(Slot::*)` loads `assets/sfx/<id>.wav` (or `FULCRUM_SFX` override). Options Audio FX dial scales the buffer. Missing / bad file → existing procedural fallback
- **File-backed slots** — fire, dry, reload_release / insert / seat, pickup, putdown, swipe, wrap, footstep, slide, jump, land (placeholder WAVs ~22.05 kHz 16-bit mono). `.ogg` names reserved; decode WAV-only this beat
- **Move cues live** — walk rustle, sprint-crouch slide, Space hop + land. Weapon cues already on FX now prefer the file
- **Ownership** — Range Tech owns weapon/move SFX on the FX bus; Augury (Chamber) keeps spatial (#27) + authored reverb volumes (#56); Lab-Rat stamps stay quiet. Evan lock: all authored audio comes over (clothing rustles, rattles, slides)
- **#54 remains the wiring ship** — file slots on the #21 FX bus + placeholder WAVs. Day-one handmade atelier vendor **landed #62** (small set into FILE_SLOTS; not a full CE / aim-offset pack dump). Dirt Hit pool + WorldMono fold **later landed #134** (supersedes optional single-file `hit.wav`). Shot propagation still later. Do **not** claim every future authored music/SFX pack or Augury authored+CE synth mix as done. Controller feel-medium dials shipped #57 — that is not this row
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
- **#90** pixellation / floor-warp sits after that: `pixel_warp_uv(heat_warp_uv(…))`. `heat_warp_uv` body **untouched**. Mix identity UV toward CE PIXEL SCALE **2**. Default `warp_strength` **0.01** actually runs (`s <= 0.0` skip only)
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
- **Crossover shoulder / left-corner peek (H)** — authored hip +X ~**0.24** (right; live **#98** **0.2403 / −0.2128 / −0.1833** — ready hold, not chin-weld). **H** springs the **viewmodel** across the chest to a partial left (~**−0.041** X / ~**−0.181** Y, cap `shoulder_x_min` **−0.055**) — arms-limited, not a capsule/eye slide, not a full mirror, not infinite travel. Extra left probe (`shoulder_viewmodel` **0.12**) helps left-corner leans. ADS keeps **0.32** of the crossover. Viewmodel crossover on the existing H bind (FoW shoulder habit), not a new key. **#98** sits on #84 tilt path / #94 first +0.08: `shoulder_cross_x` **−0.281** / `shoulder_cross_y` **0.032**; left hold pitch/yaw/roll **0.04 / 0.10 / 0.08** (supersedes #84 chest-cross 0.08/0.32/0.39) — not a mesh mirror / no `scale.x = −1`. Live hip_low **superseded #99** (MP9-Z **0.2403 / −0.3528 / −0.1513** / pitch **0.145**; U-cycle glasses **LOW HIP**; LowHip ADS still irons). Live ads_cant **landed #100** (MP9-Z **0.0423 / −0.148 / −0.136** / yaw **0.11**; glasses **CANT 45** / **CANT ADS**)
- **Lean flip + deepen** — after #51 invert, **Q = peek right** (same side as inverted A), **E = peek left**. Eye formula stays `+lean → −flat_right`. Depth feel-lab **0.5 / 0.5** (`leanOffset` / `leanMax`), superseding #25 shallow 0.18/0.12. Wall clamp / spring / yard covers from #25 stay
- **CE hop + air hop + land overlay** — Evan supersedes #51 no-double. CE `JUMP_FORCE` **12** / `|GRAVITY|` **30**, one air hop **unchanged**. Same #59 hop — **not** a second land system. Then land duck **0.14 m** + shake **0.2** when impact > 8 + punch **0.052**. **#79** softener: punch **0.028** rad · duck **0.08 m** · shake **0.14** gate **13** (normal hop ~12 does not shake) · sway eye **0.014** / yaw **0.012** / roll **0.018** · decay **4.6**. Horizontal move must not eat `vel.y` (that was why the hop stayed shallow)
- **Heat motion (v77)** — `updateBarrelHeatCardMorph` upward shimmer / lattice crawl stays the **spatial input** (not static orange blobs). Barrel haze RGB `1.0 / lerp(0.14,0.70,h) / lerp(0.025,0.16,h²)` is feel-lab reference. **Live fulcrumRust draw is Hypha colorless post UV warp landed #66** — lattice = post input only; no world-pipeline orange card. Locked card geometry DNA stays on `heat-card-dial-sheet.md` (aim-offset v77). Live fulcrumRust defaults are the **#129** CE tip **0.2.8** lock on that sheet (#71 blend / dump stay DNA)
- **Ballistics / distant hit** — tracers live until impact (feel-lab sanity **180 s**, linger **2 s**). Every strike plays FX `hit` via `mixer.play_at(Slot::Hit, Some(world))`. **#134** dirt pool: `Slot::HIT_POOL` random among loaded n≥3 distant dirt stems; missing/bad → remaining pool, then procedural grit. Retired leftover: `assets/sfx/hit.wav` (not loaded). Graze still pings `ricochet`. Day-one FILE_SLOTS vendor **landed #62** (other slots). Shot propagation still later. **#67 Patch A** sits on top (kit-tip spawn + `hip_honest_dir` + tip streak clamp); did not fight Hypha #66 / did not ship heat color. Punch-vs-scuff visuals stay #89 — **#134** is audio only
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
- Parked: live octree / unconstrained Sync dump · tunnels · runtime carve. Live walk lock **landed #81**. Stream hitch amortize **later landed #108**
- Detail: house `TERRAIN_NORTHSTAR.md` + `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust `docs/TERRAIN.md`

## Closed by fulcrumRust #62 (2026-09-08)

- **Handmade atelier SFX vendor** — Range Tech. Small handmade set of atelier `sfx_/` CE/feel WAVs into fulcrumRust `assets/sfx/` FILE_SLOTS. [PR #62](https://github.com/initialvisuals/fulcrumRust/pull/62) (`1b949794`). #54 remains the **wiring** ship (file slots on the #21 FX bus). #62 fills those slots. Placeholders from #54 replaced
- One 22.05 kHz 16-bit mono WAV per FILE_SLOTS id. Optional single-file `hit.wav` (atelier darkBead) **superseded #134** — Hit is now a dirt pool (`Slot::HIT_POOL`; `assets/sfx/hit.wav` leftover, not loaded). Missing / bad file still → procedural fallback (Hit: remaining pool, then grit)
- Mapped (atelier main `f094157`, **read-only** — no clone / no write):
  - fire ← vector SMG last-with-tail
  - dry ← weapon_shoot_failure
  - reload_release / insert / seat ← vector mag remove / insert / cock
  - pickup / putdown ← PickupA / foley_grab
  - swipe ← locus movement_woosh_air
  - wrap ← rustling
  - footstep / slide / jump / land ← concrete steps + gear_rattle
  - hit (pool) **later landed #134** ← `distant_small_medium_impact_bullet` / `…B` / `…C` (not darkBead)
- Mixer, Options Audio FX dial, and Augury spatial / #56 reverb stay untouched. Lab-Rat stamps stay quiet
- Honesty: small handmade vendor — not a full CE / aim-offset pack dump. Shot propagation still later. Future extra FX ids / authored+CE synth mix remain open
- Atelier stays **read-only**
- Evan peek: fire SMG, dry-click empty, tap-R reload, F/Z pickup-drop, swipe, wrap, walk/slide/hop — cues should read CE/feel clothing + Vector, not tiny placeholder beeps
- Detail: house `EXTRACTION_AUDIO_LOCK.md` + `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust `assets/sfx/`

## Closed by fulcrumRust #64 (2026-09-08)

- **Music playlist beds** — Range Tech. Shuffle of five atelier `music/` titles on hideout / extract: CONCRETE_ECHO · Terraform · The Memory of The Augury · guttertrash · A Shattered Remnant From A Collapsed Distant Star. [PR #64](https://github.com/initialvisuals/fulcrumRust/pull/64). Small 8 s / 22.05 kHz / 16-bit mono loops in `assets/music/` (not the 5–11 MB MP3s). Each hideout / extract start advances the shuffle. Options Audio Music dial still scales. Missing → two-tone stub. Same #21 tree; Music stays dry dual-mono (#56). Voice / FX / Augury spatial+reverb untouched
- **Kit metal/grit PBR stub** — Range Tech. Store `dBXpg` greeble pack was **not** on the shelf — still **open**/missing. Used TRIMSHEET_MICRO (+ grey) + atelier MetalPanelRectangular / MetalCorroded 256² crops + handful of scratch / fingerprint roughness masks. Boxes stay color-only (stub PBR): albedo mix + roughness/mask on MP9-Z / SR-25 / M24. House DNA: **gold+black tech trim** hairlines, not gold-plate, not Locus veins. Crops in `assets/kit/`. Do **not** claim full metal-tech / `dBXpg` kits shipped
- **SFX remix first application** — fire / foot / reload ±6% pitch/speed jitter on the live #62 FILE_SLOTS vendor. **#134** also jitters **hit**. Mixer / Options FX / Augury spatial stay honest (FX `0` still silent). Remix DNA policy stays; full remix pack minting still **open**
- Atelier stays **read-only** (`FULCRUM_MUSIC` / `FULCRUM_KIT` / `FULCRUM_ATELIER`)
- Detail: house `EXTRACTION_AUDIO_LOCK.md` + `AESTHETIC_DIEGETIC_LOCK.md` + `FULCRUMRUST_LAST_PASS_LOCK.md`

## Closed by fulcrumRust #66 (2026-09-08)

- **Colorless muzzle heat** — Hypha. Live heat tell is **colorless post UV warp** — not an orange world-pipeline card/lobe draw. [PR #66](https://github.com/initialvisuals/fulcrumRust/pull/66) (`05dd80ad`). Same #55 fullscreen post stack; HUD / glasses still after post
- **World draw gone** — heat cards are no longer drawn through the opaque world pipeline (removed world-pass indexed draw of heat mesh). A same-pass card cannot refract the scene behind it and instead read as opaque orange
- **Lattice = post input** — existing tip-anchored heat lattice kept only as spatial input → one post field `post.heat: vec4` = center UV.xy, strength, radius
- **`heat_warp_uv`** — fullscreen post applies animated UV displacement **before** scene color sample. Warped scene color is the entire tell — no orange RGB / emissive heat-card output
- **Lattice RGB forced to zero** — this path cannot become an orange draw
- Energy cook remains Range Tech `FeelState.barrel_energy` / heat-tune hold-**J**. Live card defaults are the **#129** CE tip **0.2.8** lock on `heat-card-dial-sheet.md` (#71 blend / v77 / dump stay DNA). Hypha owns the post path
- Intact siblings: #59 v77 shimmer intent (lattice crawl stays spatial input); #67 Patch A muzzle (explicitly did not fight #66); #68 ADS viewmodel DoF on the same post stack; #55 GPU post stack; **#71 dump-dial blend** (Range Tech DNA; live **#129** CE tip; did not reopen orange cards)
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

- **Heat dial blend toward aim-offset dump** — Range Tech. Then-live `HeatDials` sat **between** the previous fulcrum bake and Evan’s later dump. **Live defaults superseded #129** CE tip 0.2.8 — this #71 blend is DNA / not live. [PR #71](https://github.com/initialvisuals/fulcrumRust/pull/71) (`117c8baa`). Seat: Range Tech owns heat dials on the Hypha **#66** colorless post path. Dump-dial blend cooking/~ → **landed/X**. No orange card redraw
- **Key now (blended):** haze_strength **0.07** (was 0.01 / stolen 0.11) · card_size **0.83** (1.01 / 0.71) · scale_x **0.396** (0.69 / 0.20) · scale_y **1.745** (1.63 / 1.86) · segs **26** (31 / 20) · wind **1.40** · friction **1.075** · feather **1.585** · lobe **0.698** (1.22 / 0.35). barrel_heat **0.05** / ground **2.0** / count **14** / masters **true** unchanged
- **Post strength + radius (still #66):** at 0.01 keep lattice amp; at 0.11 use visual × 0.11; default 0.07 lands 60% toward quieter dump; 0 still kills warp. Radius: card_size + lobe pull scale/cap from 0.65/0.18 toward 0.50/0.12; lattice bbox still anchors. WGSL `heat_warp_uv` unchanged. Overlay disc lobe stays parked (`HEAT_LOBE_DISCS = 0`)
- Intent: organic gas, less cartoony/wobbly. Tip-anchored lattice DNA stays. No second heat system. Glasses / live sheet still drive fields. v77 / aim-offset dump stay DNA on `heat-card-dial-sheet.md`
- Intact: #66 colorless path · #59 lattice crawl as spatial input · #67 Patch A · #68 ADS near. Do **not** reopen orange cards. **Live HeatDials later locked #129** CE tip 0.2.8 — this #71 blend stays DNA / prior blend, not live
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

- **Hold-O extract / −/= zero / grounded slide** — Range Tech. Patch A input/move trio on #76 SIM-only. [PR #78](https://github.com/initialvisuals/fulcrumRust/pull/78) (`e86bfa79`). Seat: **Range Tech** owns hold-O raid intent flag, **−/=** zero, grounded slide gate. **The Augury** EXTRACT elbow card **landed #85** (no popup). Hatch toggle + shaft ride **later landed #115**; door / extract cancel chrome **later landed #120**; timed surface kill still **~**
- **Hold O** — raid-only `Session::extract_checking`. **O is not zero.** Hideout is a no-op. Augury EXTRACT elbow card **landed #85** (no popup). Hatch toggle + shaft ride **later landed #115**; door / extract cancel chrome **later landed #120**; timed surface kill still **~**
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
- Intact: hop 12/30/1 · #78 hold-O / −/= / grounded slide · #76 SIM-only · **P** unused · Augury EXTRACT elbow card **landed #85** (no popup). Hatch toggle + shaft ride **later landed #115**; door / extract cancel chrome **later landed #120**; timed surface kill still **~**. Do **not** claim a second land system or full extract popup. First big-map host **landed #81** (this PR did not ship it)
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust `engine/src/feel.rs` / `engine/src/tracers.rs`

## Closed by fulcrumRust #80 (2026-09-09)

- **Slope/PBR + dirt/scatter/deform plugs** — Lab-Rat. Fills Hypha reserved `StampKind::Deform` / `GroundScatter` + `HookKind::LabRatDeform` / `LabRatScatter` at the same XZ as #81. [PR #80](https://github.com/initialvisuals/fulcrumRust/pull/80) (`2cda73bc`). Seat: **Lab-Rat**. Hypha #81 still owns vertex COL bind. NRM/GLOSS GPU parked
- **Slope/angle** — `classify_slope` tags dirt / sand / rock / concrete / organic on the stamp pad
- **PBR bake-down** — 256² greyscale DISP crops + 64² COL/NRM thumbs in `assets/stamps/` (CliffJagged / GroundClay / ConcreteWall / GroundMoss — not 4k 48-bit)
- **COL hooks Hypha can consume** — `pbr::ColHook` / `col_png` / `hypha_col_alias`. Lab-Rat does **not** own vertex COL bind
- **Stamp pad** — stays **7×7**. Hypha 37×37 walk consumes `sample_channels` only (#81 19×19 stays a prior fact)
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
- **Stream** — then **9×9** window (`STREAM_RINGS` 4) by player eyes. Play STREAM **11×11** / r=5 + warm hold **later landed #137**. Stamp pad still **7×7** / far-cold (#23 guts cold)
- **Underfoot LOD** — **32 / 16 / 8 / 4** — every adjacent step **2:1** (was 32/16/4; 16→4 was opening voxel gaps)
- **PBR** — slope COL hooks (`pbr=tint` default). Vertex albedo only. NRM/GLOSS parked
- **Lab-Rat** — `Deform` / `GroundScatter` + `LabRatDeform` / `LabRatScatter` identity reserved here. **Filled later #80** (DISP bake-down + deform/scatter stamps)
- **Seams Patch A** (dark-pad → hills): one extract density on every LOD (ChannelField vs HeightOnly disagreement fixed) · 8-subdiv bridge so 32→16→8→4 stays 2:1 Lengyel · yard flatten outer **9.2 → 20 m** so pad eases into hills. Residual soft LOD pop inside a cell / far-4 horizon still parked. Stream hitch amortize **later landed #108** (cook=1/2 · prefetch=5 m). Play STREAM radius + warm hold **later landed #137**
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
- Intact: #21 Voice/Music/FX · #54/#62 file slots · #64 playlist · #27/#56 spatial+reverb · #81 host. Dirt Hit pool + WorldMono fold **later landed #134**. Do **not** claim a second mixer, Augury spatial rewrite, or Hypha Graphics post
- Detail: house `EXTRACTION_AUDIO_LOCK.md` + `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust `engine/src/audio_out.rs`

## Closed by fulcrumRust #84 (2026-09-09)

- **H shoulder-swap tilt** — Range Tech. Preferred hand / shoulder swap reads as a real tilt across the chest, not a left-right mesh mirror. [PR #84](https://github.com/initialvisuals/fulcrumRust/pull/84) (`7d7e18f5`). Seat: **Range Tech** owns H tilt on existing ViewmodelDials / ADS cant DNA. Travel stays **#59**. PreferredHand + new-profile onboard **later landed #116**
- **Travel (unchanged)** — `shoulder_cross_x / y / z` hip +X ~**0.10** → ~**−0.041** · `shoulder_x_min` **−0.055** (arms-limited; not a full left park) · `shoulder_ads_keep` **0.32** · `shoulder_spring` **8.0** · `shoulder_viewmodel` **0.12**
- **Tilt (new)** — `shoulder_cross_pitch` **0.08** (chest-cross lift; ADS cant 0.02 / hip cant 0.0365 DNA) · `shoulder_cross_yaw` **0.16 → 0.32** (inward yaw that reads) · `shoulder_cross_roll` **0.10 → 0.39** (half of U-cycle / ADS cant 0.785)
- **Path** — same `apply_shoulder_crossover` → `PoseOffset` → `pose_basis` as ADS/hip cant. No second viewmodel system
- **Not** — a capsule/eye slide · a mesh mirror · `scale.x = −1` / mirrored kit boxes. Kit boxes stay authored positive; ejection stays gun-right
- Intact: #59 travel · #82 DEVICE · #81 host · #79 land sway. Do **not** claim PreferredHand / new-profile onboard as #84 — **later landed #116**
- Live hip / `shoulder_cross` / left tilt **superseded #98** (after #94 first +0.08) — hip **0.2403 / −0.2128 / −0.1833**; `shoulder_cross_x` **−0.281** / `shoulder_cross_y` **0.032**; pitch/yaw/roll **0.04 / 0.10 / 0.08** (slight straighten, not chest-cross cant). Live hip_low **superseded #99**. See Closed by #98 / Closed by #99
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
- Intact: #78 hold-O intent · #81 host · #82 DEVICE · #84 H tilt · #86 Graphics dump. Hatch toggle + shaft ride **later landed #115**. Door / extract cancel chrome **later landed #120**. Do **not** claim timed surface kill / extract loot loop shipped. Do **not** claim Range Tech / Hypha / Lab-Rat work as this PR
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

- **Two-instance pose sync + in-pause JOIN panel** — Beabim. MP sync specialist (listen-server / two-instance sync / join panel / live-profile loot trail / world-sim leftover). Flips #34 handshake-only + "no in-game text field" + parked listen-server peer pos. [PR #83](https://github.com/initialvisuals/fulcrumRust/pull/83) (`24eaca4b`). Hypha #34 stays the UDP hub / HELLO/WELCOME / **Y**-host / `--join` foundation
- **POSE** — UDP after HELLO/WELCOME (~20 Hz): feet `xyz`, yaw, pitch, grounded, crouch. Host assigns peer ids on WELCOME and relays poses. **#91** extends the same packet with muzzle `xyz` + gun yaw/pitch
- **Silhouette** — cheap **5-box** operator (slate) — not Mixamo / not Locus. **#91** adds a 3-box gun stub on the networked muzzle — **partial** 1P ≠ 3P (biped hip stub); full 3P kit honesty / hands / gear still **open**
- **Grounded Y** — rides the **#81 19×19 heightfield** (Range #79 snap DNA). Packet Y ignored when grounded — no phantom `y=0` slab, no floating on a lie. Airborne hops keep networked Y. **#91** gun Y rides the same #88 snap
- **Stream anchors** — #81 `stream_anchors` now returns remote feet so the play STREAM window can follow a peer (live **#137 11×11**; coordinate only — no Transvoxel rewrite)
- **Glasses** — still `HOST` / `JOIN` / `PEER` labels only — never a second ammo HUD. **#91** glasses `HOST  fulcrum://ip:port`
- **HOLD JOIN** — Esc → **JOIN** → type `fulcrum://ip:port` / `fw://` / bare `ip:port` / `localhost` → Enter. No app restart. Title **JOIN** without `--join` opens the same sheet. `--join` / `FULCRUM_JOIN` still one-click. **#91** leftover INVITE + `fulcrum.invite` seeds the field
- Default port **7777** (`FULCRUM_PORT` override) stays
- Binds: **Y** host (alive), **I** stim, hold-**O** extract untouched
- **Still local (deliberately):** HoB / heat / brass / land feel / H tilt (#84) / audio device (#82) / Graphics dump (#86) / HDRI sun (#87) / Locus brain tick on the joiner + yard stamps / COL / deform / scatter (#80) / Transvoxel rewrite / Augury elbow / hatch UX (#85) / world seed / ToD / drops (**later landed #102** kit trail) / shoot + Locus leftover + death bag (**later landed #119**). **No** full world replication / PvEvP sim / Mixamo player body
- Intact / do not steal: **I** stim (#37) · hold-**O** extract (#78 / #85 elbow) · **−/=** zero (#78) · **P** unused (#76) · hold-**J** heat-tune (#35)
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust STEAL_MAP Net row. Loot trail: Closed by #102. World/sim leftover: Closed by #119. No-pause + KIND_RAID: Closed by #122. PVP leftover: Closed by #133. HOST session board / no-127 invite: Closed by #139. PVP honesty: Closed by #141. Leftover ray: Closed by #147

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
- **Unchanged** — SIM launch / HoB / gravity (#76) · AXIS_LOCK sim barrel **+Z** / #79 heightfield snap · HeatDials / haze (#71 blend at #89 ship). CE tip **0.2.8** **later landed #129** — **not** a heat-card rewrite by #89
- Intact: #67 kit-tip spawn · #76 SIM-only · #71 heat blend DNA · #79 snap · #12/#19/#47/#59 tracer field. Do **not** claim heat-card rewrite, terrain #80, Beabim sync, profile onboard, Augury hatch/labels, Aim-offset Home debugger, kit mesh rewrite, or grit as this PR. Pixellation / floor warp **later landed #90** (Hypha post dial; Augury aesthetic only)
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` Visible shot feedback + `VECTOR_MAG_DUMP.md` + fulcrumRust `engine/src/tracers.rs`

## Closed by fulcrumRust #94 (2026-09-09)

- **Patch A RH hip bias** — Range Tech. RH barrel was reading left of center on a pillar. Position-only +0.08 past a first +0.04 pass — no inward yaw to fake aim. [PR #94](https://github.com/initialvisuals/fulcrumRust/pull/94) (`a3a42e4f`). Seat: **Range Tech**. Ledger: Patch A RH hip row → **X**. H travel deepened by the same +0.08 so left dest stays ~−0.041. Left hold is a slight yaw/roll straighten (not a mesh flip, not the old #84 chest-cross cant)
- **Hip X (now)** — MP9-Z hip / hip_low **0.1843** (+0.08 from 0.1043) · hip_cant **0.2193** · sprint_high **0.29**. SR-25 hip / hip_low **0.20** · hip_cant / sprint_high **0.235 / 0.30**. M24 hip / hip_low **0.205** · hip_cant / sprint_high **0.24 / 0.31**
- **H travel** — `shoulder_cross_x` **−0.145 → −0.225** (keeps dest ~**−0.041**) · `shoulder_x_min` **−0.055** unchanged · ads_keep **0.32**
- **Left hold** — pitch/yaw/roll **0.04 / 0.10 / 0.08** (slight lift / inward / straighten). Supersedes #84 chest-cross **0.08 / 0.32 / 0.39**
- **Unchanged** — ADS hold X (iron / holo / acog / sniper / cant) stay feel-lab bore-center · inspect X **0.0593** · tip spawn + `hip_honest_dir` · #89 tracers / particles · no `scale.x = −1`
- Intact: #59 travel DNA · #67 tip spawn · #84 tilt path · #89 projectiles. Live **End** tuner on these same dials **later landed #97**. Live hip / ready-Y **superseded #98**. Live hip_low **superseded #99**. Do **not** claim kit mesh rewrite, heat, audio, Beabim, PreferredHand onboard, or Augury Home tabs/logger as #94
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust `ViewmodelDials` / `apply_shoulder_crossover`

## Closed by fulcrumRust #97 (2026-09-09)

- **Aim-offset tuner + attachment sockets** — Range Tech. Live **End** sheet on existing `ViewmodelDials` + `AttachmentOffsets` (optic / can from authored `kit_mesh` sockets). Identity PoseOffset = live authored mounts (**#98** after the body-width + ready-Y pass; was #94 when #97 shipped). [PR #97](https://github.com/initialvisuals/fulcrumRust/pull/97) (`6908ec88` / `8ac9130b`). Seat: **Range Tech**. Ledger: Patch A tuner row → **X** (A-notes `~` / parked `·` stale). Home debugger **later landed #110** (was #95 tip / unbound at #97 ship). Not Home chrome at #97, not hitch logger at #97, not EffectComposer, not a second pose system
- **Binds** — **End** toggle (feel-lab Home remapped like X→Z) · Insert WEAPON ↔ ATTACH · PageDown pose / attachment target · PageUp step cycle · ↑↓ select axis · ←→ / num± nudge · Delete paste-ready JSON (feel-lab `example_smg` object + attachments)
- **Steps** — MICRO pos **0.0005** / rot **0.001** · FINE (default) **0.002** / **0.005** · MED **0.01** / **0.02** · COARSE **0.05** / **0.1**. Axis rows PX PY PZ RX RY RZ
- **Authored defaults now #98 / hip_low #99 / ads_cant #100** — MP9-Z hip **0.2403 / −0.2128 / −0.1833** · ADS iron X **0.0084** (bore-center) · SR-25 / M24 hip **0.256 / −0.224 / −0.208** / **0.261 / −0.229 / −0.228**. H travel / slight straighten stay; `shoulder_cross_x` **−0.281** / `shoulder_cross_y` **0.032**. Live hip_low is **#99** (MP9-Z **0.2403 / −0.3528 / −0.1513** / pitch **0.145**). Live ads_cant is **#100** (MP9-Z **0.0423 / −0.148 / −0.136** / yaw **0.11**). Tuner writes the same dials — #97 still live for fine polish
- **Follow** — kit boxes + muzzle tip follow live can/optic offsets. World drops stay authored identity. Glasses `AIM TUNE`. AIM TUNE live-save **later landed #103** (End→Hypha `project.json`; `aim_live` default **true**; partial merge)
- Intact: #98 RH hip / H dials (was #94 when this PR shipped) · #67 tip spawn · #89 tracers. Do **not** claim Augury Home tabs/logger as #97 (that is **#110**) · EffectComposer · Beabim · Heat rewrite · Terrain · mesh mirror / `scale.x = −1` · PreferredHand onboard · ballistics / SIM / #76 · #89 tracers · Audio DEVICE · live-save persist (that is **#103**)
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust `AimTuner` / `ViewmodelDials` / `AttachmentOffsets`

## Closed by fulcrumRust #101 (2026-09-09)

- **Blender UV dials on stamp/PBR/grit packs** — Lab-Rat. Stamp / PBR / grit packs share a Blender-style Mapping-node UV sheet — **scale X/Y · offset X/Y · rotate** (CCW about +Y) — so texture resolution / tile scale can change **without shrinking geometry**. [PR #101](https://github.com/initialvisuals/fulcrumRust/pull/101) (`c4e1490e` / `0ae97a0c`). Seat: **Lab-Rat**. Identity default keeps today's yard. Texture-only — **never** geo / **never** a Transvoxel chunk resize
- **`engine/src/uv.rs`** — Location (metres) → rotate → scale (UV repeats). `scale > 1` tiles smaller
- **Consume** — `GreyMap` / `HeightPack8` sample the sheet before wrap. Hypha #112 `lod_mips::promote_for_uv` (256/64/16 chain) + TerrainHost wear/COL honor the same `uv::xform` on Transvoxel skin
- **Dial sheet:**

| Dial | Default | Note |
|------|---------|------|
| scale X / Y | **1 / 1** | `scale > 1` tiles smaller |
| offset X / Y | **0 / 0** m | metres before rotate |
| rotate | **0** deg | CCW about stamp **+Y** |
| Identity | `1,1 + 0,0 r=0` | keeps today's yard |
| Override | `FULCRUM_UV=sx,sy,ox,oy,deg` | or `FULCRUM_UV_SCALE` / `_OFFSET` / `_ROTATE` |

- **Smoke** — `uv=1.00,1.00+0.00,0.00 r=0`
- **Peek** — `FULCRUM_UV=2,2 cargo run` → more grain, same geo/hills/chunks
- Intact: #58/#60 grit · #80 slope/PBR plugs · #81 host / vertex COL · stamp pad 7×7 · AXIS_LOCK stamp **+Y**. Do **not** claim NRM/GLOSS GPU · whole roughness→stamp · Transvoxel resize · atelier writes
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + `STAMP_FEEL_LOCK.md` + fulcrumRust `engine/src/uv.rs`

## Closed by fulcrumRust #103 (2026-09-09)

- **AIM TUNE live-save** — Range Tech. End AIM TUNE LIVE persist into Hypha `project.json` so Evan's peeks survive quit/relaunch. Steals Hypha Graphics/Audio persist path; does **not** take Augury Home (debugger **later landed #110**). [PR #103](https://github.com/initialvisuals/fulcrumRust/pull/103) (`74da84e3` / `e0452f82`). Seat: **Range Tech**. Ledger: STEAL_MAP live-save row → **in** (house `X`). #97 End tuner / Delete JSON dump schema stay. Home debugger **later landed #110**
- **Dials** — `aim_live` default **true** (End sheet `LIVE` / `OFF`; later RECORD toggle is a stub — no bind). `aim_tune.example_smg` / `example_rifle` / `example_sniper` — per-kit ViewmodelDials + optic/can offsets. Pose keys: `hip` `hip_low` `hip_cant` `sprint_high` `ads` `ads_cant` `ads_holo` `ads_acog` `ads_sniper_scope` `inspect` — each `{x,y,z,rotX,rotY,rotZ}`. Attach keys: `attachments.optic` `attachments.can`
- **Load / flush** — Deploy / new session (`Settings::boot` → `Session::apply_aim_settings`). Each End nudge when LIVE flushes Hypha persist path
- **Partial merge** — missing kits/poses keep authored **#98 / #99 / #100** numbers (ready-hip / low-hip / ads_cant stay those peeks until nudged)
- Intact: #97 End tuner · #98 ready-hip / H · #99 hip_low · #100 ads_cant · Delete JSON dump. Do **not** claim Augury Home tabs/logger as #103 (that is **#110**) · bake-permanent-defaults · UV (#101) · Beabim · heat rewrite · RECORD toggle bind
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust `Settings.aim_live` / `Settings.aim` / `AimTuner`


## Closed by fulcrumRust #110 (2026-09-09)

- **CE Home debugger** — Augury. Steal Concrete Echo Home debugger DNA into fulcrumRust as a native overlay (not a TS paste). Verified against CE `utils/debug.tsx` on `_CONCRETE_ECHO_` `4_15_26` (v0.2.8). [PR #110](https://github.com/initialvisuals/fulcrumRust/pull/110) (`7ff3c311`). Seat: **The Augury**. Ledger: Augury * next tabs+logger / #95 tip → **X**. Closes clerk #95 / #104 overnight hitch path (Home logger tab). Hitch *visibility* is this cook; Hypha stream hitch *fix* **later landed #108** · worker/paint/gpu deepen **later landed #123**
- **Binds** — **Home** toggle (CE). **End** stays Range AIM TUNE (#97 / #103). ←/→ cycle tabs. Up/Down scroll the ring
- **Tabs** — **LOGS** · **TELE** · **CHEAT** (CE names LOGS / TELEMETRY / CHEATS)
- **Hitch** — frame **> 33 ms** → `WARN` · frame **> 100 ms** → `HITCH`. Reason tags `FRAME` · `LOAD` (boot/deploy gate) · `STREAM` (Transvoxel remesh) · `BAKE` (extract rigidize ms) · `GATE` (HIDEOUT / DEPLOY / EXTRACT). Raw wall-clock measured **before** the 50 ms sim clamp (a 400 ms bake/stream hitch still prints `400ms`)
- **Ring** — 256 timed lines (CE ~800); 8 visible rows. Ring **800** + COPY + tracks **later landed #121**
- **Telemetry** — 1s FPS, last/max frame ms, warn/spike counts, pos, place, stream resident/cold, HP/AR
- **Cheats** — **GOD** skip `apply_player_wound` · **NOCLIP** skip walls + playable clamp · **TELEPORT** current-world spawn · **SPAWN** `Locus::standard` at look+4 m (extract; hideout stub log)
- **Persist** — `project.json` `debugger_tab` (optional; shares file with Range `aim_live` / `aim_tune` — one `persist_settings()` flush)
- **Chrome** — analysis-knowledge-core: thin white frames, fade-in white mono. Glasses `DEBUG`
- Intact: #97 End AIM TUNE · #103 LIVE persist · #85 EXTRACT elbow. Hatch toggle + shaft ride **later landed #115**. Door / extract cancel chrome **later landed #120**. Home LOGS COPY + tracker toggles **later landed #121**. Home occlusion + 3D probes **later landed #125**. Home binds lock + spawn + denser STREAM **later landed #128**. Timed surface kill still **~**. Do **not** claim Hypha stream hitch *fix* as this PR (that is **#108** · deepen **#123**) · shoot/feel · stamps/UV · MP sync · CE WEAPON/ATTACHMENT tuner (already End) · CE PERF/PHYS/RENDER/heartbeat/combat-log flags (house-docs steal later) · full CE debugger tab contract beyond this native shell
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` / `AESTHETIC_DIEGETIC_LOCK.md` + fulcrumRust `engine/src/debugger.rs`

## Closed by fulcrumRust #108 (2026-09-09)

- **Stream hitch amortize** — Hypha. Squash walk / load-in hitch on the then-#81 9×9 stream (no new map size). [PR #108](https://github.com/initialvisuals/fulcrumRust/pull/108) (`b3be2974`). Seat: **Hypha**. Ledger: Patch A stream hitch row → **X**. Hitch *visibility* stays Augury #110 / #121 (Hypha emits `STREAM` / `BAKE`, does not rebuild Home chrome). Play STREAM **11×11** + warm hold **later landed #137** — #108 stays hitch *fix* layer 1
- **Load-in** — skeleton (density + stamps + props) on frame 0; splash keeps presenting; **2** extracts / frame (`COOK_BUDGET_LOAD`) until idle; GPU upload only when the window is ready. No Sync whole **9×9** dump on one frame (Evan Windows busy cursor / hang dialogue)
- **Play tick** — **1** extract / frame (`COOK_BUDGET_PLAY`). Dirty jobs sorted underfoot-first via `TerrainHost::pump_stream`
- **5 m face prefetch** — upgrades the next already-resident neighbor to lod 0 *before* the step so the standing chunk is not remeshed mid-stride. Prefetch does **not** open a second 9×9
- **Walk inside a cell** — focus+LOD unchanged stays a no-op; stale LOD stays until the budget reaches it
- **Hitch emit** — Augury Home tags `STREAM` / `BAKE` (`r=` `cold=` `pend=`) into #110 logger
- **Smoke** — `cook=1/2 prefetch=5` next to `subdivs=32/16/8/4`
- Intact / parked: live octree parked; residual soft LOD pop inside a cell still parked; Range poses / AIM TUNE / loot · Lab-Rat UV (#101) · Beabim net · Augury Home tabs untouched. Mesher stolen (`TerrainHost` / `extract_one` / activation) — no greenfield mesher
- Worker extract+paint deepen **later landed #123** (`defer=worker/paint/gpu` · skip far mask-only remesh) — #108 cook=1/2 · prefetch=5 m stay this layer. Radius + warm hold **later landed #137**
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + `TERRAIN_NORTHSTAR.md` + fulcrumRust `docs/TERRAIN.md`

## Closed by fulcrumRust #112 (2026-09-09)

- **Transvoxel UV consume** — Hypha. Wires TerrainHost / material sample so Lab-Rat #101 stamp/PBR UV dials actually read on Transvoxel terrain — **texture only, never geo / never remesh / never chunk shrink**. [PR #112](https://github.com/initialvisuals/fulcrumRust/pull/112) (`35929282` / tip cook `b1ad2816`). Seat: **Hypha** (consume). Lab-Rat still owns the bake sheet (#101 `uv.rs` / GreyMap / HeightPack8)
- **`lod_mips::promote_for_uv` / `material_lod`** — existing 256/64/16 chain only; when `FULCRUM_UV` scale > 1 keep a finer existing pack (scale 2 → mid 64² instead of far 16²; scale 4 → near 256²)
- **TerrainHost `paint` / `stamp_wear_scale*` / `uv_skin`** — vertex wear / cracks hashes follow `uv::xform`; no remesh
- **`pbr_shelf` COL** — explicit `sample_with` + wrap; scale 2 at XZ == identity at 2× XZ
- **Untouched** — mesh / density / `CHUNK_METERS` 16 / `lod_for_world`
- **Peek** — identity looks like #101; `FULCRUM_UV=2,2 cargo run` → more grain on same hills; identity default keeps today's yard
- Intact / out of scope: Range AIM TUNE / poses · Beabim net · Augury Home · #108 stream hitch · Lab-Rat stamp bake rewrite · NRM/GLOSS GPU
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + `STAMP_FEEL_LOCK.md` + fulcrumRust `lod_mips::promote_for_uv`

## Closed by fulcrumRust #114 (2026-09-09)

- **Patch A subtract crawl pad network** — Lab-Rat. Deepens the open `[~]` tunnel / voxel subtract crawl (was a two-capsule dent under the extract) into a shallow enterable Subtract network under the pad. Same CHANNELS / stamp / growth lane. [PR #114](https://github.com/initialvisuals/fulcrumRust/pull/114) (`8fa74c03` / `28c09bd7`; merge tip `898454a0`). Seat: **Lab-Rat**. Pad stays shallow-by-default. Full underground / live voxel collide still `[~]`
- **Path** — mouth → mid → pocket → +Z spur, plus west / east branches and a bent anastomosis kink. Capsule radii **0.42–0.50** (prone-sized; was 0.24–0.28). Pocket / mouth / spur are ellipsoid chambers. Path wander via existing `density_stamp_2d`
- **Feet** — reserved Hypha splice `DensityField::stamp_height_delta` → `growth::crawl_floor_delta` so feet drop into the mouth bowl (`CRAWL_DROP` **0.38** m). Bowl stays above the Transvoxel slab (`SLAB_Y0` **−0.7**)
- **Lip** — concrete Union lip around the mouth stretches **up** (compound, not deeper guts)
- **Glasses** — stand in mouth / pocket → `CRAWL  SUBTRACT` (wins over Locus `ALERT_M` **14** m, same as plot pins). Thin leftover plate at the mouth
- **Dial sheet:**

| Dial | Value |
|------|--------|
| `CRAWL_DROP` | **0.38** m mouth bowl |
| Subtract radii | **0.42–0.50** (prone 0.42) |
| Mouth XZ | **−1.60, 8.20** |
| Pocket XZ | **0.25, 9.15** |
| `SLAB_Y0` | **−0.7** (bowl stays above) |
| Env / smoke | none new — existing `prims=` / `growth=` / `yard_m2=` still print harness cost |

- Intact / out of scope: Hypha cook/prefetch/LOD · Range feel · Beabim · Augury Home · `uv.rs`. Do **not** claim full guts / live voxel collide / tunnel sim. House world-depth stays **shallow**. Off-stream leftover slab **later landed #130** (not this pad crawl)
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + `STAMP_FEEL_LOCK.md` + fulcrumRust `docs/GROWTH_POC.md` / `docs/CHANNELS.md`

## Closed by fulcrumRust #98 (2026-09-09)

- **RH hip one more body-width + ready-hip Y** — Range Tech. After #94 +0.08, RH hip needed one more gun-body width further right so the *lateral* angle matches left hold, slightly tighter. Default HIP was reading like a chest/chin shoulder-weld; dropped Y so main HIP is a ready hold, not parade-rest under the chin. [PR #98](https://github.com/initialvisuals/fulcrumRust/pull/98) (`48518709` / `5b02e2ab`). Seat: **Range Tech**. Dial-only `ViewmodelDials` hip-family + `shoulder_cross`. #98 did **not** ship a shotgun low-hip — that U-cycle deepen **later landed #99**
- **Hip (now)** — MP9-Z hip **0.2403 / −0.2128 / −0.1833** (+0.056 X = 2 × MP9 `receiver_half.x` **0.028** / polymer shell **0.056**; Y **−0.044** ready-hip drop; Z **+0.012** tighter). `hip_cant` **0.2753 / −0.1938 / −0.1983** (Y stays; +X/+Z only). `sprint_high` X **0.29 → 0.346** (X only). SR-25 hip **0.256 / −0.224 / −0.208**. M24 hip **0.261 / −0.229 / −0.228**. Live `hip_low` **superseded #99** (was #98 **0.2403 / −0.2788 / −0.1633**)
- **H travel** — `shoulder_cross_x` **−0.225 → −0.281** (keeps dest X ~**−0.041**) · `shoulder_cross_y` **−0.012 → 0.032** (keeps dest Y ~**−0.181** after the RH drop) · `shoulder_x_min` **−0.055** unchanged · ads_keep **0.32**
- **Unchanged** — ADS hold X (bore-center) · left pitch/yaw/roll **0.04 / 0.10 / 0.08** (gold vertical) · inspect X **0.0593** · tip spawn + `hip_honest_dir` · #89 tracers / particles · no `scale.x = −1`
- Intact: #94 first +0.08 · #97 End tuner (still live — ready-hip / H defaults stay #98) · #59 travel DNA · #67 tip spawn · #84 tilt path · #89 projectiles. Live hip_low **superseded #99**. Do **not** claim mesh flip, Beabim, heat, terrain, or PreferredHand onboard as #98
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust `ViewmodelDials` / `apply_shoulder_crossover`

## Closed by fulcrumRust #99 (2026-09-09)

- **Low-hip shotgun stance (U-cycle hip_low)** — Range Tech. After #98 ready-hip Y **−0.2128**, U-cycle `hip_low` was still **−0.2788** (tiny 0.066 offset). Deepens the existing U step (Chest → LowHip → Canted; glasses **LOW HIP**) into a true shotgun low-ready. [PR #99](https://github.com/initialvisuals/fulcrumRust/pull/99) (`ed6dff0e`). Seat: **Range Tech**. Dial-only `ViewmodelDials.hip_low`. Still shootable: RMB from LowHip = iron ADS (not `ads_cant`). Not chin-weld. Greyzone 45° canted CQC ADS **later landed #100**
- **hip_low (now)** — MP9-Z **0.2403 / −0.3528 / −0.1513** (Y **−0.074** from #98 **−0.2788**; gap **0.140** vs ready **−0.2128**; Z tucked **−0.1633 → −0.1513**; pitch **0.0765 → 0.145**; X stays **0.2403**). SR-25 Y **−0.29 → −0.364** / Z **−0.188 → −0.176** / pitch **0.08 → 0.148**. M24 Y **−0.295 → −0.369** / Z **−0.208 → −0.196** / pitch **0.078 → 0.146**
- **U-cycle** — Chest (`hip`) → LowHip (`hip_low`) → Canted (`hip_cant`) → Chest. Glasses LowHip **LOW HIP** (was LOW). RMB from LowHip still irons. Viewmodel pose ease **later landed #109** (`hold_spring` **7.0**; glasses still snap)
- **Unchanged** — ready hip / hip_cant / ADS / H crossover (#98 locks stay). #97 End AIM TUNE still live for fine nudge on these same dials
- Intact: #98 ready-hip / H · #94 first +0.08 · #97 End tuner · #59 travel DNA · #67 tip spawn · #84 tilt path · #89 projectiles. Greyzone canted CQC ADS **later landed #100**. U-cycle pose ease **later landed #109**. Do **not** claim mesh mirror, Beabim, heat, or terrain as #99
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust `ViewmodelDials.hip_low` / `HomeHold::cycle`


## Closed by fulcrumRust #100 (2026-09-09)

- **Canted 45° Greyzone CQC ADS** — Range Tech. After #99, leftover `ads_cant` was a rolled hip-cant parked near iron — top optic still read as the sight. Dial-only `ViewmodelDials.ads_cant` (MP9 / SR-25 / M24) makes that target a first-class CQC aim pose. [PR #100](https://github.com/initialvisuals/fulcrumRust/pull/100) (`842b3efa`). Seat: **Range Tech**. RMB from U-cycle CANT + hold-Mouse5 both enter `ads_cant` @ 60° CQC. Glasses **CANT 45** / **CANT ADS**. ACOG/scope zoom does not follow a CQC cant. #97 End AIM TUNE still nudges `ads_cant`
- **ads_cant (now)** — MP9-Z X/Y/Z **0.0423 / −0.148 / −0.136** (was 0.034 / −0.142 / −0.172). Pitch/yaw/roll **0.024 / 0.11 / 0.785** (was 0.02 / 0.035 / 0.785; roll stays). X = iron **0.0084** + optic-root **0.048·sin45** (eye on the 45° rail, bore not under the LPVO). Z = CQC-close (holo −0.1335 lane). Yaw = inward to body (~6° / 0.11). SR-25 / M24 **0.0468 / −0.154 / −0.148** (root 0.052·sin45)
- **Binds** — Primary RMB from Chest/LowHip → seated optic ads (unchanged). **U** → CANT + RMB → `ads_cant` @ 60° CQC. hold-**Mouse5** from any hold → `ads_cant` @ 60° CQC (does not steal U-cycle). `ads_for(Canted, _)` already returned `ads_cant`
- **Unchanged** — `hip_low` stays #99 · ready-hip / hip_cant / primary ADS / H crossover stay #98. Iron ADS X **0.0084** (bore-center)
- Intact: #99 hip_low · #98 ready-hip / H · #97 End tuner · #94 first +0.08 · #59 travel DNA · #67 tip spawn · #84 tilt path · #89 projectiles. U-cycle pose ease **later landed #109**. Do **not** claim canted-holo mesh, IOR/bodycam glass, mesh flip, Beabim, heat, or terrain as #100
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust `ViewmodelDials.ads_cant` / `ads_for(Canted, _)`

## Closed by fulcrumRust #109 (2026-09-09)

- **U-cycle hold springs (Chest / LOW HIP / CANT)** — Range Tech. After #98/#99/#100 poses, U-cycle was snapping because `home_hold` fed `blend_aim` as the hip on the same frame. Eases pos+rot toward the selected HomeHold on the existing ADS / H / sprint exp-approach path (`k = 1 − e^{−rate·dt}`). [PR #109](https://github.com/initialvisuals/fulcrumRust/pull/109) (`6108cf91` / `fc30eb30`). Seat: **Range Tech**. Ledger: STEAL_MAP pose-ease row → **in** (house `X`). Glasses still snap CHEST / LOW HIP / CANT 45; the viewmodel springs. 1P viewmodel only
- **Dial sheet:**

| Lane | Dial | Rate | Role |
|------|------|------|------|
| U-cycle home (pos+rot) | `hold_spring` | **7.0** | NEW — house-medium between ADS and H |
| ADS enter / exit | `blend_speed` | **6.4** (feel-lab 8) | own dial — **#113** scales by kit `HandlingStats.ergo` (not folded into `hold_spring`) |
| H crossover | `shoulder_spring` | **8.0** | unchanged |
| Sprint high-ready | `sprint_hold` | **6.2** | unchanged |
| Inspect overlay | hardcoded | **10.0** | unchanged |

- **Seed-before-cycle** — load phases never tick FeelState, so the first U after deploy seeds `hold_blend` from the current home *before* cycle (otherwise that frame initializes onto LowHip and snaps)
- **Unchanged** — #98 ready-hip / H · #99 hip_low · #100 ads_cant · #97 End AIM TUNE · #103 LIVE persist. Inspect and sprint_high still lerp on top of the eased home. Mouse5 / RMB cant-ADS paths stay
- Intact: #98/#99/#100 poses · #97 End tuner · #103 LIVE persist · #57/#59 springs DNA. Do **not** claim Beabim / 3P, heat, terrain, PreferredHand, or ADS blend folding into `hold_spring` as #109
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust `FeelState.hold_blend` / `hold_spring` / `HomeHold::cycle`

## Closed by fulcrumRust #113 (2026-09-09)

- **Kit handling / ergo / MOA sheet** — Range Tech. Thin kit sheet `HandlingStats` / `FeelSheet::handling` drives existing 1P fire/ADS dials — not house mastery, not a gear UI, not a skills system. [PR #113](https://github.com/initialvisuals/fulcrumRust/pull/113) (`719deae6` / `421d61b8`; merge tip `b2d38414`). Seat: **Range Tech**. Ledger: STEAL_MAP handling → **in** (house `X`). Patch A ergo/handling/MOA → **X**. 1P feel only
- **Dial sheet:**

| Dial | Behavior |
|------|----------|
| **Ergo → ADS** | `blend_speed` **6.4** × kit ergo. Still the ADS spring — **not** folded into `hold_spring` **7.0** (#109). MP9-Z ergo **1.25** → ADS blend **8.00**; SR-25 **1.00** → **6.40**; M24 **0.80** → **5.12** |
| **Handling → recoil** | `1 / handling` on authored kick / pitch / yaw. `ads_recoil_mul` **0.6** stays. Handling MP9 **1.15** · SR-25 **1.00** · M24 **0.90**. Authored kick/pitch/yaw stay per-gun (MP9 1.0 / 0.012 / 0.008 · SR-25 1.15 / 0.018 / 0.010 · M24 1.75 / 0.035 / 0.012) |
| **MOA** | New hip cone (minutes) after `hip_honest_dir` (no 100 m loft miss). ADS × **0.22**. Hip MOA MP9 **4.0** · SR-25 **1.2** · M24 **0.40** |
| **Velocity / cycle** | Same `muzzle_speed` / `cyclic_rpm` / interval as `SmgFireDials` (MP9 300 / 1200 · SR-25 785 / 0.14s · M24 810 / 0.65s) |
| **Mag fill** | `ReloadKind::duration_for(mag_fill)` stub. Defaults **1.0** (authored 1.10 / 0.46 s) |

- **Unchanged** — #109 `hold_spring` **7.0** · #98 ready-hip / H · #99 hip_low · #100 ads_cant · #97 End AIM TUNE · #103 LIVE persist · #76 SIM / #67 hip honesty
- Intact: #109 hold springs · #97/#103 AIM TUNE · #57/#59 springs DNA · #67 tip / `hip_honest_dir`. Do **not** claim house mastery / gear UI / Beabim 3P / net / loot / heat rewrite / Lab-Rat / Augury Home / PreferredHand as #113
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust `HandlingStats` / `FeelSheet::handling`


## Closed by fulcrumRust #115 (2026-09-09)

- **Hatch/elevator glasses UX** — Augury. Hold-F toggle + Akira shaft ride on the #85 elbows — no modal popup. [PR #115](https://github.com/initialvisuals/fulcrumRust/pull/115) (`eb8618df` / `eb811e74`; merge tip `469d46b0`). Seat: **The Augury**. Landed on main 2026-09-09. Ledger: hatch toggle + shaft ride → **X**; timed surface kill stays **~**. STEAL_MAP / MILESTONE already claimed in-PR — house shelf only
- **`engine/src/hatch.rs`** — `HatchBoard`: quiet hatches start **CLOSED**; hold-**F** toggles OPEN/CLOSED. Loud Akira shaft: hold-**F** rides surface → cap lip → exit pad
- **Glasses** — stay Augury elbows (thin white mono, L-leader). Idle: `HATCH  HOLD F  OPEN` / `SHAFT  HOLD F  RIDE`. Holding: `HOLD F  OPEN  42%`. Hold-**O**: `EXTRACT  OPEN` / `CLOSED` / `SHAFT` — no modal popup
- **Draw** — open-well rings + ride cage on the existing Augury extra-solids path. Does **not** remesh Hypha world solids
- **F steal** — stabilize / dummy / stim / corpse / loot still steal **F**. Tap-**F** pickup still wins. Downed cancels a ride (no float)
- **World** — yard plots stay `-24/-24`, `18/-28`, `-28/16` + shaft `18/-12`
- **Dial sheet:**

| Dial | Value | Notes |
|------|-------|-------|
| `HOLD_SECS` | **1.15** | Commit toggle / ride. Same glasses `HOLD F  VERB  N%` language as stabilize (`STABILIZE_HOLD_SECS` **1.45**). Tap-F pickup still wins |
| `COOL_SECS` | **0.55** | Extra wait after release |
| `must_release` | **true after commit** | Opposite action cannot start until **F** is released. Cool-off alone was not enough to stop a hold-through loop |
| `RIDE_SECS` | **1.40** | Surface ↔ cap lerp (smoothstep). Completes with a snap to dest so we do not undershoot and re-arm |
| `SHAFT_CAP_Y` | **16.65** | Authored cap top (`+16.4` box + half 0.25) |
| `CAP_LIP_X` | **1.95** | Between tower half **1.6** and cap half **2.2** — standable, not inside collide |
| `EXIT_PAD_X` | **2.65** | Outside shaft interact half **1.9** so ride-down cannot re-arm |
| `CAP_KEEP_M` | **2.05** | Walk off the lid = free EXIT (no hold) |

- Intact: #85 EXTRACT elbow · #78 hold-O intent · #110 Home debugger · stabilize hold **1.45**. Door / extract cancel chrome **later landed #120**. Do **not** claim timed surface kill / extract loot loop · bloom / god-rays · Hypha remesh · Range / Lab-Rat / Beabim work as this PR
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` / `AESTHETIC_DIEGETIC_LOCK.md` + fulcrumRust `engine/src/hatch.rs`. STEAL_MAP / MILESTONE stay sources of truth

## Closed by fulcrumRust #90 (2026-09-09)

- **Pixellation / warp strength floor** — Hypha. CE Fulcrum lock: pixellation looked best at the lowest step above zero (~0.01 or 0.1). `0.01 < 0.1`, so the floor is **0.01**. [PR #90](https://github.com/initialvisuals/fulcrumRust/pull/90) (`54a99f10`). Seat: **Hypha** owns the post dial. **Augury** owns the aesthetic note only — do **not** claim Augury shipped the dial. Direction lock FoW pixellation influence is live via Hypha post — do **not** steal into Range
- **Dial sheet:**

| Dial | Was | Now | Note |
|------|-----|-----|------|
| `warp_strength` default | (none) | **0.01** | Lowest positive CE-like step (`0.01 < 0.1`) |
| Step | — | **0.01** | Options A/D / Enter |
| Range | — | **0.0–1.0** | **0 = off** |
| Skip | — | `s <= 0.0` only | Default **0.01** actually runs |
| Snap target | — | CE PIXEL SCALE **2** | Mix identity UV → half-res snap |
| Persist | — | `project.json` `warp_strength` | `{:.2}` → `0.01` |
| Options | missing | Graphics **WARP** (row 13) | After CAM FAR; `GFX_LEN` 12→13; fog/cam/#86 rows keep indices |
| Heat / sun / fog | — | **untouched** | #66 / #71 `heat_warp_uv` · #87 · #86 |

- **`PostToggles.warp_strength`** — default **0.01**; clamp / `nudge_warp`; persist in `project.json`
- **`PostStack`** — writes `pixel: [warp_strength, 0, 0, 0]`. New `pixel_warp_uv` after `heat_warp_uv` (heat body not edited). Mix identity UV toward CE PIXEL SCALE **2**
- **Smoke** — `gfx=` appends ` warp=0.01` only. Existing `fog/375/520 cam=0.05/2000` substring stays
- **STEAL_MAP** — Augury pixellation `todo` → **partial**. Fog / stars / proc tex still open. A-notes has no pixellation/warp ledger row — none invented
- Intact: Heat haze (#71 / #66) · HDRI sun (#87) · fog/cam dump (#86) · binds · stamps · net · bipeds. Do **not** claim bloom / godRays, Range heat rewrite, Lab-Rat stamps, Beabim MP, or Greyzone canted ADS as this PR
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` / `AESTHETIC_DIEGETIC_LOCK.md` + fulcrumRust `engine/src/post.rs` / Options Graphics **WARP**


## Closed by fulcrumRust #91 (2026-09-09)

- **Invite leftover + peer names + gun pose** — Beabim. Dial sheet after #83 so two-instance pose is usable without hand-typing addresses. Bundled visible peer names + gun/muzzle pose. Loot trail **later landed #102**. World/sim leftover **later landed #119**. [PR #91](https://github.com/initialvisuals/fulcrumRust/pull/91) (`c4d75c11`). Seat: **Beabim** owns this MP slice (listen-server / invite / pose / loot trail / world-sim leftover). Hypha #34 + Beabim #83 stay the UDP hub / HELLO/WELCOME / **Y**-host / HOLD JOIN / `stream_anchors` foundation
- **INVITE leftover** — Title **HOST** (and `--host` / Deploy) binds listen, then opens leftover **INVITE** sheet (same JOIN analysis-core chrome). Pause while hosting: **INVITE** (same list seat as JOIN). Enter copies. Glasses: `HOST  fulcrum://ip:port`. **Y** while hosting re-copies. File leftover `fulcrum.invite` (LAN + LOOP `127.0.0.1`) so second instance JOIN seeds without memorizing IP. **#139** later killed the LOOP 127 seed — prefer LAN / real bind; empty JOIN field — no 127 placeholder; typed `--join 127` still works. OS clipboard best-effort (`clip` / `pbcopy` / `wl-copy` / `xclip`) — file always works. Title JOIN / HOLD JOIN still accept `fulcrum://` / `fw://` / bare `ip:port` / `localhost`
- **Visible peer names** — HELLO + NAME after WELCOME. `FULCRUM_NAME` if set, else **HOST** / **P{id}**. Fade-in white mono over the remote head (hairline only). Does **not** steal Augury elbow cards (door / loot / hatch / EXTRACT)
- **Gun / weapon pose** — Same UDP **POSE** ~20 Hz now carries feet + look + **muzzle xyz + gun yaw/pitch**. Remote 5-box slate operator gets a 3-box gun stub on the networked muzzle. Grounded feet consume Hypha **#88** `plant_simple_root` on the #81 heightfield (coordinate only — no foot-plant / Transvoxel rewrite). Gun Y rides the same snap
- **1P ≠ 3P (partial)** — Peer gun is a **biped hip stub** (`reconstructed_gun`). Does **not** publish 1P `muzzle_world()` — no #94/#98/#99 hip / low-hip / artistic cant on the remote operator. Do **not** claim Mixamo / full 3P kit honesty / hands / gear sync
- **Still local (deliberately):** HoB / heat / brass · Range #89 CE projectiles · Range #113 handling · #94/#98/#99 1P hip · #97 AIM TUNE · Lab-Rat #80 stamps / COL / deform / scatter / UV **later landed #101** · Hypha #88 foot-plant rewrite / Transvoxel / pixellation (only `plant_simple_root` for peer feet; warp floor **later landed #90**) · Augury elbow / hatch UX (#85) · PreferredHand / new-profile onboard **later landed #116** · live-profile loot trail **later landed #102** · shoot / Locus leftover / death bag **later landed #119** · Clerk Patch A ledger restamp
- Binds: **Y** host (alive; re-copy while hosting) · **I** stim · hold-**O** extract · **U** 1P hold cycle · **End** AIM TUNE untouched
- Solo **Deploy** unchanged (`net=off` on smoke)
- Intact / do not steal: #83 packet / handshake / HOLD JOIN · #88 plant hook · #81 heightfield · Range 1P hip / AIM TUNE / projectiles
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust STEAL_MAP Net row. Loot trail: Closed by #102. World/sim leftover: Closed by #119. PVP leftover: Closed by #133. HOST session board / no-127 invite: Closed by #139. PVP honesty: Closed by #141. Leftover ray: Closed by #147

## Closed by fulcrumRust #102 (2026-09-09)

- **Live-profile loot trail** — Beabim. Dial sheet after #91 so two instances agree on a **readable loot trail** tied to live session presence — not full world/sim sync (that leftover **later landed #119**). [PR #102](https://github.com/initialvisuals/fulcrumRust/pull/102) (`6fc0d5d6`). Seat: **Beabim** owns this MP slice (listen-server / invite / pose / live-profile loot trail / world-sim leftover). Hypha #34 + Beabim #83 / #91 stay the UDP hub / HELLO/WELCOME / **Y**-host / HOLD JOIN / INVITE leftover / names / gun stub foundation
- **KIND_LOOT** — on the #91 UDP leftover. Host relays; both sides apply drop/take by `InstanceId`
- **Hairline crumbs** — reuse `plan_name_tag` (thin white mono): `{NAME} DROP/TAKE KIT` with `FULCRUM_NAME` / HOST / P{id}. **Not** Augury EXTRACT / hatch elbow cards
- **Two-instance** — Host **Z** → other instance sees the loose kit + `HOST DROP …`. Other **F** → host loses that id + `P1 TAKE …`
- **Starting kits** — stay local (each instance keeps minted loadout). Swap is DROP then TAKE
- **1P ≠ 3P (held)** — #91 peer biped hip gun stub unchanged. Pose / gun stub from #91 unchanged. Do **not** claim Mixamo / full 3P kit honesty
- **Still local (deliberately):** HoB / heat / brass / Range #89 / #113 handling · shoot / Locus leftover / death bag **later landed #119** · 1P hip / low-hip / cant / AIM TUNE / #103 live-save · Lab-Rat stamps / UV **later landed #101** · Augury hatch / EXTRACT elbows · PreferredHand **later landed #116** · full live-profile stash · mid-air drop bounce (remote sees settled rest) · knife-rally / joiner slash / stabilize dummy (`NO NET`)
- Solo **Deploy** unchanged (`net=off`) — no trail chrome
- Intact / do not steal: #83 packet / handshake / HOLD JOIN · #91 INVITE leftover / names / gun stub · #88 plant hook · Range 1P hip / AIM TUNE / projectiles / #103 live-save
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust STEAL_MAP Net row. World/sim leftover: Closed by #119. PVP leftover: Closed by #133. HOST session board / no-127 invite: Closed by #139. PVP honesty: Closed by #141. Leftover ray: Closed by #147

## Closed by fulcrumRust #119 (2026-09-09)

- **World/sim leftover — shoot / Locus / bodies** — Beabim. Dial sheet after #102 so two instances share the same raid stream — not just pose + loot crumbs. [PR #119](https://github.com/initialvisuals/fulcrumRust/pull/119) (`6562070e726c0ae69719598bdc294a1f51d2e37e`). Seat: **Beabim** owns this MP slice (listen-server / invite / pose / loot trail / world-sim leftover). Hypha #34 + Beabim #83 / #91 / #102 stay the UDP hub / HELLO/WELCOME / **Y**-host / HOLD JOIN / INVITE leftover / names / gun stub / KIND_LOOT foundation
- **KIND_SHOT** — host-relayed on the #83/#91/#102 UDP leftover (`HYPH` magic). Peer sees tracer + fire FX from **biped hip + look dir** (`reconstructed_gun`). Does **not** publish 1P `muzzle_world()` — house lock **1P≠3P** held
- **KIND_LOCUS** — ~10 Hz host leftover: slot + pos + yaw + HP + brain + ragdoll flop. HELLO dumps current yard. Joined peer **plants soles only** — does **not** tick a second Locus brain. Host hunts the nearest operator (local + remotes). Joined deploy does not mint a second yard
- **KIND_BODY** — death-bag drop/reclaim (host-relayed, one shared bag)
- **Two-instance** — share shoot events, Locus presence/ragdoll, and the death bag — not just pose + loot. Hairline leftover only — no new glasses chrome, no Augury elbow steal
- **1P ≠ 3P (held)** — peer shot muzzle = biped hip stub, not 1P cant. #91 gun stub unchanged. Do **not** claim Mixamo / full 3P kit honesty
- **Still local (deliberately):** Range feel / HoB / heat / eject dials / 1P hip / AIM TUNE (#113 handling etc.) · knife-rally HP · Locus slash HP on the joiner (host wound only if the hunted operator is the host) · teammate stabilize dummy (`NO NET`) · timed surface kill · death cam · stamps / Transvoxel / hatch elbows · PreferredHand **later landed #116** (local profile; no Beabim net sync) · full PvEvP / dedicated infra · mid-air drop bounce. KIND_BRASS leftover **later landed #133** (Range eject dials stay local)
- Solo **Deploy** unchanged (`net=off`)
- Intact / do not steal: #83 packet / handshake / HOLD JOIN · #91 INVITE leftover / names / gun stub · #102 KIND_LOOT · #88 plant hook · Range 1P hip / AIM TUNE / #113 handling / projectiles
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust STEAL_MAP Net row. No-pause + KIND_RAID: Closed by #122. PVP leftover: Closed by #133. HOST session board / no-127 invite: Closed by #139. PVP honesty: Closed by #141. Leftover ray: Closed by #147

## Closed by fulcrumRust #116 (2026-09-09)

- **PreferredHand + new-profile onboard** — Hypha. PreferredHand enum on input/profile (**Right** default if unset). Title Deploy / Host / Join gates a NEW PROFILE sheet — must pick RIGHT / LEFT before first raid. Permanent local profile in `project.json` (`profile_onboarded` + `preferred_hand`). Live raid is a session copy of permanent; death clears live. Extract→stash is a stub hook (Beabim KIND_LOOT already covers Z/F raid items). Viewmodel home seats Range H crossover: `shoulder_t` **0** = authored RH, **1** = existing left dest — **no** `scale.x = −1` / mesh flip. [PR #116](https://github.com/initialvisuals/fulcrumRust/pull/116) (`6018f8ad384cbc0bcf6e7d9c818f2d23f3d145ad` / tip `d531b27f11281f993f53ccbf8d1579a8539ad91e`). Seat: **Hypha**. Ledger: A-notes already `[X]` PreferredHand onboard / `[~]` persistent+live profile (stash stub) — do not invent A-note PRs / rewrite A-notes
- **Dial sheet:**

| Dial | Lock |
|------|------|
| **PreferredHand** | Enum on input/profile. **Right** default if unset |
| **NEW PROFILE** | Title Deploy / Host / Join gate. Must pick RIGHT / LEFT before first raid |
| **Permanent** | `project.json` `profile_onboarded` + `preferred_hand` |
| **Live** | Session copy of permanent. Death clears live |
| **Extract→stash** | Stub hook. KIND_LOOT already covers Z/F raid items. Full PMC stash / character tab later |
| **shoulder_t** | **0** = authored RH · **1** = existing left dest. No `scale.x = −1` / mesh flip |

- **Does not steal** — Range ergo / MOA / pose springs (#109/#113) · Augury hatch (#115) · Lab-Rat stamps · Beabim world/sim / loot trail (#102/#119) · root README
- Intact / do not claim: full PMC stash · character tab · world-pool death loot · Beabim net sync of PreferredHand · mesh flip · Range feel rewrite · bloom / godRays
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust `project.json` profile keys / title NEW PROFILE sheet

## Closed by fulcrumRust #120 (2026-09-09)

- **Door / extract cancellable countdown chrome** — Augury. Hideout door **F** and OPEN quiet-hatch presence arm a short cancellable glasses countdown (same HOLD % language as hatch #115) before map transition. Walk away / leave volume cancels. Stay commits. [PR #120](https://github.com/initialvisuals/fulcrumRust/pull/120) (`77f0cd67` / `4aaf40a` / `3db2e7e`; merge tip `089e0ad0`). Seat: **The Augury**. Landed on main 2026-09-09. Ledger: door / extract cancel chrome → **X**; timed surface kill stays **~**. STEAL_MAP / MILESTONE already claimed in-PR — house shelf only. In-repo dial sheet: `docs/GATE_DIAL_SHEET.md`
- **`engine/src/gate.rs`** — `GateBoard`: same HOLD % glasses language as hatch / stabilize. No modal popup
- **Door** — **F** edge arms `DOOR  DEPLOY  N%`. Walk-into-door still does **not** auto-deploy (#51). Walk away cancels. Stay + timer → `begin_deploy` → extract
- **Extract** — standing in an **OPEN** quiet hatch volume arms `EXTRACT  N%`. Hold-**F** still toggles OPEN/CLOSED. Shaft is a ride, not extract-out. Walk away / hold-F close / ride drops the count. Stay + timer → Hypha `extract_transfer_to_stash` stub, then hideout. Kit stays
- **Glasses** — stay Augury elbows (thin white mono, L-leader, analysis-core — not gold). Idle door `DOOR  F  DEPLOY`. Armed: `DOOR  DEPLOY  N%` · `EXTRACT  N%`. Hold-**O** still intent only (`OPEN` / `CLOSED` / `SHAFT`) — countdown wins while armed
- **`GateSignal`** — local leftover. Arm / frac for Beabim. No new KIND. Handshake / Esc-pause **later landed #122** (Beabim; leftover = `GATE_SECS` **2.20**; glasses stay this PR)
- **Dial sheet:**

| Dial | Value | Notes |
|------|-------|-------|
| `GATE_SECS` | **2.20** | Stay in door / OPEN hatch volume to commit |
| `COOL_SECS` | **0.55** | After cancel, do not immediately re-arm (same cool-off fairness as hatch #115 / house-docs #78) |
| Door arm | **F** edge | Walk-into-door still does **not** auto-deploy (#51). F starts the count |
| Extract arm | **OPEN** quiet hatch presence | Hold-**F** still toggles OPEN/CLOSED. Shaft is a ride, not extract-out |
| Cancel | leave volume | Walk away. Hold-**F** close / ride also drops the count |
| Commit door | still in volume | `begin_deploy` → extract |
| Commit extract | still in volume | Hypha `extract_transfer_to_stash` stub, then hideout. Kit stays |
| `GateSignal` | local leftover | Arm / frac for Beabim. No new KIND. Handshake / Esc-pause **later landed #122** |

- Intact: #115 hatch HOLD/RIDE (`HOLD_SECS` **1.15** etc.) · #85 EXTRACT elbow · #78 hold-O intent · #51 F-only door (no walk-in auto-deploy). Do **not** claim timed surface kill / extract loot loop as this PR. Beabim pause/handshake **later landed #122**. Do **not** claim Hypha PreferredHand guts · bloom / god-rays · Range / Lab-Rat work as this PR
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` / `AESTHETIC_DIEGETIC_LOCK.md` + fulcrumRust `docs/GATE_DIAL_SHEET.md` / `engine/src/gate.rs`. STEAL_MAP / MILESTONE stay sources of truth

## Closed by fulcrumRust #122 (2026-09-09)

- **No-pause live sim + shared extract handshake** — Beabim. Esc HOLD / Options / JOIN chrome **mutes the local pawn only**. Raid keeps ticking (pose / shots / Locus leftover). Focus loss / alt-tab releases grab — **does not HOLD or freeze** (no bullet bulk catch-up). Door **F** / OPEN quiet hatch presence arm the #120 glasses countdown; host then commits both peers to the same raid id + host seed (dest extract or hideout). [PR #122](https://github.com/initialvisuals/fulcrumRust/pull/122) (merge tip `cbb26d8796faa9e476e8695fb4b118486d1759b3`). Seat: **Beabim** (MP sync specialist — listen-server / pose / loot / world-sim / no-pause / shared instance). Hypha #34 + Beabim #83 / #91 / #102 / #119 stay the UDP hub / HELLO/WELCOME / **Y**-host / HOLD JOIN / INVITE leftover / names / gun stub / KIND_LOOT / KIND_SHOT / KIND_LOCUS / KIND_BODY foundation. Augury #120 still owns glasses HOLD % / `GATE_SECS` / `COOL_SECS`. In-repo dial sheet: fulcrumRust `docs/GATE_DIAL_SHEET.md` KIND_RAID row
- **No-pause** — Esc HOLD / Options / JOIN mute the local pawn only. Raid keeps ticking. Focus loss / alt-tab releases grab — does **not** HOLD or freeze. Augury HOLD list / "SYSTEM PAUSED" chrome **not restyled**
- **KIND_RAID** — host-authoritative leftover = Augury `GATE_SECS` **2.20** (house-docs #80 / fulcrumRust #120). Door **F** / OPEN quiet hatch presence arm the #120 glasses countdown; host then commits both peers to the same raid id + host seed
- **Cancel** — Augury leave-volume / `GateEvent::Cancelled` → KIND_RAID CANCEL. Inventory / death soft-cancel too. No forced transition. Augury cool-off **0.55**. Glasses HOLD % (`DOOR  DEPLOY  N%` / `EXTRACT  N%`) not rewritten
- **Solo `net=off`** — uses the #120 countdown (stay commits, walk away cancels). No invented handshake / raid id / trail
- **1P ≠ 3P (held)** — #91 peer biped hip gun stub + #119 hip-stub shot muzzle unchanged. Do **not** claim Mixamo / full 3P kit honesty
- **Still local (deliberately):** Range feel / HoB / heat / eject dials / 1P hip / AIM TUNE · knife-rally / joiner slash / stabilize dummy · stamps / Transvoxel hitch / PreferredHand · Lab-Rat stamps · Augury glasses HOLD % / hatch art / timed surface kill · full PvEvP / dedicated infra. KIND_BRASS leftover **later landed #133** (Range eject dials stay local)
- Intact / do not steal: #83/#91/#102/#119 pose / shots / loot / world-sim · #120 `GATE_SECS` **2.20** / glasses HOLD % / cool-off **0.55** · hatch HOLD art · Range AIM TUNE / 1P hip · Hypha PreferredHand / Transvoxel hitch · Lab-Rat stamps
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust `docs/GATE_DIAL_SHEET.md` KIND_RAID row / STEAL_MAP Net row. PVP leftover: Closed by #133. HOST session board / no-127 invite: Closed by #139. PVP honesty: Closed by #141. Leftover ray: Closed by #147

## Closed by fulcrumRust #121 (2026-09-09)

- **Home LOGS COPY + event tracker toggles** — Augury. Steal the rest of Concrete Echo Home LOGS after #110 so Evan can paste a walk without a firehose. Verified against CE `utils/debug.tsx` on `_CONCRETE_ECHO_` `4_15_26`: LOGS **COPY** dumps the boot ring; settings keep **separate** tracker checkboxes. Native overlay chrome, not a TS paste. [PR #121](https://github.com/initialvisuals/fulcrumRust/pull/121) (`2416ec09`). Seat: **The Augury**. Landed on main 2026-09-09. Ledger: LOGS follow-up peek after Home LOGS → **X**. STEAL_MAP / CREDITS already claimed in-PR — house shelf only. #110 stays the tabs+logger foundation
- **Bind** — **Home** LOGS. **End** AIM TUNE untouched
- **Copy** — **Enter** on LOGS copies the **full** boot→now ring (clipboard via existing leftover helper + cwd `fulcrum.logs`; `FULCRUM_LOGS` override)
- **Ring** — **800** timed lines (CE ~800). Overlay still 8 rows, Up/Down scroll
- **Timestamp** — `[sssss.mmm]` on every dump/overlay line
- **Tracks** — **STREAM** · **BAKE** · **GATE** · **PLAY**/GAMEPLAY · **INT**/INTERNAL — Insert selects, Delete toggles. Off quiets that category (not one console dump)
- **Persist** — `project.json` `log_stream` / `log_bake` / `log_gate` / `log_gameplay` / `log_internal` (default **on**) + existing `debugger_tab`
- **Hitch** — warn **> 33 ms** / spike **> 100 ms** stay. TELE **max ms** still updates when a track is off
- **Events** — medium, edge-only — BOOT / GPU / GATE / STREAM r↑ cold↓ / FIRE (burst start) / HIT / AI brain / HATCH / WOUND / DOWN / DEAD / STIM / HEAL / RELOAD / SLASH / DROP / TAKE / CHEAT / COPY. No per-frame spam
- **Chrome** — analysis-knowledge-core. Glasses `DEBUG`
- Does **not** rewrite Hypha stream hitch amortize (#108). Emits/tags richer STREAM lines Hypha already feeds. Worker `extract0`/`paint`/`gpu` emit **later landed #123**
- **Dial sheet:**

| Dial | Value | Notes |
|------|-------|-------|
| Bind | **Home** LOGS | **End** AIM TUNE untouched |
| Copy | **Enter** on LOGS | Full boot→now ring. Clipboard via existing leftover helper + cwd `fulcrum.logs`; `FULCRUM_LOGS` override |
| Ring | **800** timed lines | CE ~800. Overlay still 8 rows, Up/Down scroll |
| Timestamp | `[sssss.mmm]` | Every dump/overlay line |
| Tracks | **STREAM** · **BAKE** · **GATE** · **PLAY**/GAMEPLAY · **INT**/INTERNAL | Insert selects, Delete toggles. Off quiets that category (not one console dump) |
| Persist | `log_stream` / `log_bake` / `log_gate` / `log_gameplay` / `log_internal` | `project.json` default **on** + existing `debugger_tab` |
| Hitch | warn **> 33 ms** / spike **> 100 ms** | TELE **max ms** still updates when a track is off |
| Events | medium, edge-only | BOOT / GPU / GATE / STREAM r↑ cold↓ / FIRE / HIT / AI brain / HATCH / WOUND / DOWN / DEAD / STIM / HEAL / RELOAD / SLASH / DROP / TAKE / CHEAT / COPY. No per-frame spam |
| Chrome | analysis-knowledge-core | Glasses `DEBUG` |

- Intact / out of scope: Hypha #108 hitch amortize rewrite · End AIM TUNE · door/extract cancel · Beabim pause/MP · Range feel · stamps. #110 tabs+logger foundation stays. Home occlusion + 3D probes **later landed #125**. Home binds lock + spawn + denser STREAM **later landed #128**
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust `engine/src/debugger.rs`. STEAL_MAP / CREDITS stay sources of truth

## Closed by fulcrumRust #125 (2026-09-09)

- **Home occlusion + 3D probes + COLL/PERF/SPWN** — Augury. Steal more Concrete Echo Home debugger DNA after #110/#121. Native overlay chrome — not a TS paste. Evan greenlit Patch A (#124 ledger). [PR #125](https://github.com/initialvisuals/fulcrumRust/pull/125) (`317d58fd6788d1b9b12ef28ba211becd1c621678`). Seat: **The Augury**. Landed on main 2026-09-09. Ledger: Patch A * occlusion + * CE 3D cursor/probe JSON → **X**. STEAL_MAP / CREDITS already claimed in-PR — house shelf only. #110 stays the tabs+logger foundation; #121 stays LOGS COPY + tracks. End stays Range AIM TUNE
- **Tabs** — **LOGS** · **TELE** · **COLL** · **PERF** · **SPWN** · **CHEAT** (←/→ cycle; two-row strip). Persist `project.json` `debugger_tab` (`logger` / `telemetry` / `collision` / `perf` / `spawner` / `cheats`)
- **Drop probe** — **P** (CE **T** remapped — T is bandage). Drops a labeled look-at / surface hit in front of the player. Live look-at cursor (wall slab vs heightfield) with kind + world `Pn` labels. Cap **32**
- **Copy probes** — **Enter** on TELE / COLL / PERF copies JSON of all probes (clipboard + cwd `fulcrum.probes`; `FULCRUM_PROBES` override). Schema `fulcrum.probes.v1`: `id`, `label`, `x/y/z`, `nx/ny/nz`, `kind` (`wall` / `terrain` / `air` / `overhang` / `hole` / `spawn`), `distance`, `name`. Cwd leftover ignored like `fulcrum.logs`
- **Pop probe** — **Delete** on TELE / COLL / PERF
- **Copy logs** — **Enter** on LOGS (unchanged). Soft Enter-hold debounce **0.45s**
- **Tracks** — LOGS: Insert selects, Delete toggles STREAM / BAKE / GATE / PLAY / INT (unchanged #121)
- **Spawner** — SPWN: Up/Down select **LOCUS STD** / **LOCUS INK** / **KIT DROP**; Enter fires at look-at (hideout Locus is a stub log)
- **Collision** — COLL tab draws wall AABB wires (invisible blockers) + hole count. PERF owns 1s FPS + hitch
- **Occlusion** — fills under glyphs; overlay buffer grows (was 256 KiB / ~1820 quads; now 2 MiB and grows) so LOGS footer `ENTER COPY` is not eaten. INV/STATUS footer no longer shares y with `1200 RPM` / `HEAT v77`. HP/AR labels sit above bars (ultrawide midlines clear). Options GRAPHICS fog/cam/WARP sit above the hint. Title JOIN HOLD is its own row (`HOLD JOIN`, not `HOLD P…`). Debugger panel clamped above HP/AR
- **Chrome** — analysis-knowledge-core. Glasses `DEBUG`. Still labels only, never a second ammo HUD
- Lab-Rat consume **later landed #127**. Range tip/optic probe JSON stay **·**. Timed surface kill still **~**. Hitch *fix* deepen **later landed #123**
- **Dial sheet:**

| Dial | Value | Notes |
|------|-------|-------|
| Bind | **Home** toggle | **End** AIM TUNE untouched. Cycle lock **later landed #128** |
| Tabs | **LOGS** · **TELE** · **COLL** · **PERF** · **SPWN** · **CHEAT** | ←/→ cycle; two-row strip |
| Drop probe | **P** | CE **T** remapped — T is bandage. Look-at / surface hit. Cap **32** |
| Copy probes | **Enter** on TELE / COLL / PERF | Clipboard + cwd `fulcrum.probes`; `FULCRUM_PROBES` override |
| Pop probe | **Delete** on TELE / COLL / PERF | |
| Copy logs | **Enter** on LOGS | Unchanged. Soft Enter-hold debounce **0.45s** |
| Schema | `fulcrum.probes.v1` | `id` · `label` · `x/y/z` · `nx/ny/nz` · `kind` · `distance` · `name` |
| Kinds | `wall` / `terrain` / `air` / `overhang` / `hole` / `spawn` | Live cursor: wall slab vs heightfield |
| Spawner | **LOCUS STD** / **LOCUS INK** / **KIT DROP** | Up/Down select; Enter fires at look-at |
| Collision | wall AABB wires + hole count | Invisible blockers |
| Persist | `debugger_tab` | `logger` / `telemetry` / `collision` / `perf` / `spawner` / `cheats` |
| Chrome | analysis-knowledge-core | Fills under glyphs; growing overlay buffer; fade-in white mono. Glasses `DEBUG` |

- Intact / out of scope: Hypha hitch *fix* deepen (**later landed #123**) / STREAM refill · End AIM TUNE (Range) · Lab-Rat stamps/crawl consume of probe JSON (**later landed #127**) · Range tip/optic probe JSON · Beabim MP · timed surface kill. #110 tabs+logger foundation stays. #121 LOGS COPY + tracks stay. Home binds lock + spawn + denser STREAM **later landed #128**
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` / `AESTHETIC_DIEGETIC_LOCK.md` + fulcrumRust `engine/src/debugger.rs`. STEAL_MAP / CREDITS stay sources of truth

## Closed by fulcrumRust #123 (2026-09-09)

- **Worker STREAM extract+paint** — Hypha. Deepen of stream hitch *fix* after #108 amortize. [PR #123](https://github.com/initialvisuals/fulcrumRust/pull/123) (`b4725b8c`). Seat: **Hypha**. Rebased onto #125 + #127. Hitch *visibility* stays Augury #110 / #121 (Hypha emits into `Debugger::push_stream` — no debugger rewrite). STEAL_MAP / CREDITS already claimed in-PR — house shelf only
- **Play worker extract+paint** — hitch thread never `sample_channels` on play Transvoxel extract. Worker owns extract+paint. Tick only applies one finished mesh then leftover paint/GPU
- **`defer`** — **`worker/paint/gpu`** (alongside existing #108 cook=1/2 · cook_ms 8/16 · prefetch 5 m)
- **Far mask-only remesh skipped** when R climbs — no lod-2/3 storm on row add
- **STREAM lines** — `extract0` / `paint` / `gpu` + hitch-thread ms + r↑/cold↓ (emits into Augury #121 Home LOGS tags; Hypha emits only)
- **Load splash** stays sync. CHANNELS stay bake-time
- **Smoke** — keeps Lab-Rat `probes=off` **and** Hypha `cook_ms` / `defer`
- **Evan peek (prior dump — context this cook closed):** STREAM WARN ~62 ms while walking · HITCH **336–414 ms** · TELE MAX **17391 ms** · STREAM R↑ / COLD↓ (R 72–81 · COLD 289–280). EXTRACT pend=2 ~17s STREAM bite on hitch thread — fixed by worker path
- Intact / out of scope: Lab-Rat stamps / Range / Beabim / GATE / Augury Home chrome (#125) / PreferredHand. Residual soft LOD pop / live octree still parked. #108 cook=1/2 · prefetch=5 m stay the prior amortize layer. Denser WALK/STREAM hang tags **later landed #128** (visibility — not this hitch *fix*). Play STREAM **11×11** + warm hold **later landed #137** — #123 stays the worker/paint/gpu hitch layer
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + `TERRAIN_NORTHSTAR.md` + fulcrumRust `docs/TERRAIN.md`

## Closed by fulcrumRust #129 (2026-09-09)

- **HeatDials CE tip 0.2.8 lock** — Range Tech. Live `HeatDials` + post strength/radius are Evan’s locked CE tuner from `_CONCRETE_ECHO_` `4_15_26` `barrelHeatCanon.ts` (house-locked 2026-09-09). Past #71 dump-blend. [PR #129](https://github.com/initialvisuals/fulcrumRust/pull/129) (`54c558a`). Seat: **Range Tech** owns heat dials on the Hypha **#66** colorless post path. Cards do the look; barrel warp at enable floor; **no fog blob**. #66 path stays. #89 projectile feel untouched. Do **not** reopen orange cards
- **Key now (CE tip 0.2.8):** barrel_heat **1.0** · haze_strength **0.01** (enable-floor) · ground_strength **0.0** (flag ON, strength off) · card_size **0.99** · scale_x **0.28** · scale_y **0.86** · count **20** · segs **32** · wind **1.56** · friction **0.74** · feather **1.90** · lobe **0.40**. WAS = #71 blend. STOLEN = aim-offset dump
- **Post strength + radius (still #66):** `visual * haze`. Haze **0.01** is the enable-floor (subtle warp; #71 remap 0.01→lattice×1.35 was the fog). **0** still kills warp. Radius scale/cap **0.40 / 0.08**. Tip-weighted lattice energy + energy-weighted post UV (field on the can, not a haze cloud). WGSL `heat_warp_uv` unchanged. Overlay disc lobe stays parked (`HEAT_LOBE_DISCS = 0`)
- Intent: hotter can tip, subtle muzzle warp, no fog blob. Tip-anchored lattice DNA stays. No second heat system. Glasses / live sheet still drive fields. #71 blend / aim-offset dump stay DNA on `heat-card-dial-sheet.md`
- Intact: #66 colorless path · #59 lattice crawl as spatial input · #67 Patch A · #68 ADS near · #71 dump-blend DNA · **#89** projectile feel (untouched). Do **not** reopen orange cards
- Detail: house `heat-card-dial-sheet.md` + `FULCRUMRUST_LAST_PASS_LOCK.md`

## Closed by fulcrumRust #127 (2026-09-09)

- **Lab-Rat probe consume** — Lab-Rat. Consume seat for [#125](https://github.com/initialvisuals/fulcrumRust/pull/125) Home look-at probes. Agents (and Evan) **P**-drop hits in Home, **Enter**-copy `fulcrum.probes`, next extract bake lands stamps / crawl / CHANNELS at those metres. [PR #127](https://github.com/initialvisuals/fulcrumRust/pull/127) (`1c9217c9`). Seat: **Lab-Rat**. Not a second mesher. Not Home chrome. Not Range AIM TUNE / Hypha stream / Beabim. Range tip/optic JSON consume stays **·**. STEAL_MAP / CREDITS already claimed in-PR — house shelf only. Do **not** invent A-note PRs
- **Path** — `FULCRUM_PROBES` if set, else cwd `fulcrum.probes` → `engine/src/probes.rs` (`parse` / `channel_primitives` / `apply_to_layers`) → `stamps::apply_yard_harness` onto existing `StampField::layers` (same CHANNELS compose Hypha remeshes)
- **Kind routing** — existing CHANNELS language only:

| `kind` / `name` | Write |
|-----------------|-------|
| `terrain` (`ground`; leftover `extract` still parses) | `height_mask` (`density_stamp_2d`) + sit ellipsoid + short up capsule when `ny > 0.25` |
| `spawn` | dirt ellipsoid / sphere at the hit |
| `wall` (`blocker`) | concrete box lip offset along the normal |
| `hole` / `overhang` | shallow `ChannelOp::Subtract` ellipsoid; sequential hits connect with a subtract capsule |
| `air`, `name=hideout`, `name=locus` | skip |

- **Floor** — `growth::crawl_floor_delta` mins in `probes::floor_delta` so hole/overhang hits get the reserved shallow bowl. Subtract Y stays ≥ **−0.54** (Hypha slab −0.7). Stretch **up**, not guts. Cap **32** matches Augury
- **Default** — missing / empty / unit-test cwd → **no extra prims**. Smoke `probes=off` (or `probes=n=N` when a sheet is present)
- Intact / out of scope: Home chrome (#125 writer stays Augury) · Range tip/optic consume · Hypha STREAM/hitch (#123) · Beabim · sandbox pedon leftover (**later landed #130**) · player spawn loci bake (**later landed #132** — same sheet, `World.player_spawns`; #127 stays CHANNELS dirt sit). Not a second mesher
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust `docs/PROBES.md`

## Closed by fulcrumRust #130 (2026-09-09)

- **Lab-Rat sandbox pedon** — Lab-Rat. Stick + button on the extract yard. Tap **F** rebakes stamp / growth peek / Subtract crawl on a **separate smaller leftover slab** on a concrete table on the real pad — iterate Patch A CHANNELS without Hypha’s **37×37** STREAM remesh (stamp pad stays **7×7**). [PR #130](https://github.com/initialvisuals/fulcrumRust/pull/130) (`10a4c7b3`; tip `ef6dea41`). Seat: **Lab-Rat**. Not Home chrome. Not probe consume (#127). Not the enterable pad crawl (#114). World stays shallow-by-default. STEAL_MAP / CREDITS already claimed in-PR — house shelf only. Do **not** invent A-note PRs
- **Find it** — extract spawn, walk **+X** (right) and a little **−Z** (behind you) ~4 m. Rust stick + red button; concrete table holds the ~2 m sandbox. Off the stim vial / dummy
- **What F rebakes** — existing CHANNELS language on the pedon only (`engine/src/pedon.rs`): dirt `box_sdf` · `density_stamp_2d` height-mask · organic/creeper peek capsules · Subtract crawl mouth→pocket→spur + concrete lip
- **Seed / overlay** — extract seed xor generation. Leftover voxel columns = Lab-Rat `pedon` GPU overlay (not growth budget, not `extract_terrain`). `StampField::layers` and `TerrainHost::stream_rev` stay cold
- **Glasses** — `PEDON  F  REBAKE  GEN n`
- **Dial sheet:**

| Dial | Value |
|------|--------|
| Stick XZ | `3.90, -0.55` |
| Slab XZ | `5.20, -0.55` (table `TABLE_H` 1.02 m) |
| Button reach | 1.35 m |
| Slab | 1.90 m half-span, 0.38 m thick, 10×6×10 @ 0.18 m |
| Bind | tap **F** on the stick (does not steal hatch hold-F / kit pickup) |
| Env | none |
| Smoke | `pedon=gen=1 prims=N voxels=M` after one off-stream rebake. Extract `stream_rev` / terrain tris / harness `layers=` must not move |

- Intact / out of scope: Hypha STREAM/hitch (#123) · Range feel · Beabim net · Augury Home (glasses label only) · probe consume (#127) · enterable pad crawl (#114). Do **not** claim Hypha remesh / Range / Beabim / Augury Home chrome shipped by #130
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + `STAMP_FEEL_LOCK.md` + fulcrumRust `docs/PEDON.md`

## Closed by fulcrumRust #128 (2026-09-09)

- **Home binds lock + spawn probes + denser STREAM events** — Augury. Steal the rest of Concrete Echo Home input after #110/#121/#125 so WASD does not walk *and* cycle tabs, Space does not hop *and* copy/fire, and Enter actually confirms. Native overlay chrome — not a TS paste. [PR #128](https://github.com/initialvisuals/fulcrumRust/pull/128) (`6904d4ee38418ec1f8545b73b1e5c72105b70f14`). Seat: **The Augury**. Landed on main 2026-09-09. STEAL_MAP / CREDITS already claimed in-PR — house shelf only. #110 stays the tabs+logger foundation; #121 stays LOGS COPY + tracks; #125 stays occlusion + 3D probes + COLL/PERF/SPWN. End stays Range AIM TUNE. Dial sheet: fulcrumRust `docs/DEBUGGER.md`
- **Home** — cycle **off → LOGS → TELE → COLL → PERF → SPWN → CHEAT → off**. Not a separate unbound toggle. First press always opens **LOGS**. Last press closes
- **← / →** — cycle tabs while open. **↑ / ↓** — page options (LOGS scroll · SPWN kind · CHEAT row). **Arrows only**
- **Enter** — confirm (LOGS copy `fulcrum.logs` · TELE/COLL/PERF copy `fulcrum.probes` · SPWN fire · CHEAT toggle). **Space** stays hop. **F** stays interact
- **Insert** — tab page options (LOGS tracks · TELE/COLL/PERF **drop kind** AUTO / TERRAIN / WALL / **SPAWN** / HOLE / OVERHANG / AIR · SPWN kind · CHEAT row). End tuner still owns Insert when AIM TUNE is open
- **WASD / Space** — player move / hop. Title / HOLD still read them. They do **not** set `debug_*`
- **`name`** — surface tag: `ground` / `wall` / `hole` / `overhang` / `air` / `spawn` / `hideout` / `locus`. **Not** mesh id `extract` (that read as the EXTRACT gate). Hideout terrain stays `hideout` (Lab-Rat skip). Locus volume stays `locus` unless drop mode is **SPAWN**
- **`kind:spawn`** — easy writer: **SPWN + P**, or TELE **Insert → SPAWN → P**. Schema `fulcrum.probes.v1` fields stay — do not invent keys
- **Denser hang / STREAM tags** — event-based, not frame spam. Hypha `extract0` / `paint` / `gpu` kept. `WALK START/STOP r= cold= pend=` · `STREAM [stage] r=↑/↓ cold=↑/↓ pend= rΔ= cΔ= pendΔ= [SPIKE] [walk]` · hitch `Nms r= cold= pend= [walk]` when the last tag was STREAM/WALK. `WALK` counts as STREAM. TELE max still moves when STREAM is muted
- **Chrome** — analysis-knowledge-core. Glasses `DEBUG`. Still labels only, never a second ammo HUD
- **Dial sheet:**

| Dial | Value | Notes |
|------|-------|-------|
| **Home** | Cycle **off → LOGS → TELE → COLL → PERF → SPWN → CHEAT → off** | Not a separate unbound toggle. First press **LOGS** |
| **← / →** | Cycle tabs | Arrows only. **WASD** stays move |
| **↑ / ↓** | Page options | LOGS scroll · SPWN kind · CHEAT row |
| **Enter** | Confirm | LOGS / probes copy · SPWN fire · CHEAT. **Space** stays hop |
| **Insert** | Tab page options | Tracks / drop kind / SPWN / CHEAT. End owns Insert when AIM TUNE is open |
| **Delete** | Toggle / pop | LOGS: selected track. TELE/COLL/PERF: last probe |
| **P** | Drop look-at probe | Cap **32**. SPWN (AUTO) or Insert **SPAWN** forces `kind:spawn` |
| `name` | Surface tag | `ground` / `wall` / `hole` / `overhang` / `air` / `spawn` / `hideout` / `locus` — not mesh id `extract` |
| STREAM | Event hang tags | `WALK START/STOP` · r/cold Δ · pend spike · hitch-cause. Not frame spam |
| Chrome | analysis-knowledge-core | Glasses `DEBUG`. Title / HOLD still WASD + Space |

- Intact / out of scope: Hypha hitch *fix* (#108 / **#123** already shelved) · End AIM TUNE (Range) · Lab-Rat CHANNELS consume (already landed #127 — dirt sit) · Lab-Rat player spawn loci bake (**later landed #132**) · Range tip/optic probe JSON · PVP leftover **later landed #133** · Beabim MP · timed surface kill. #110 tabs+logger foundation stays. #121 LOGS COPY + tracks stay. #125 occlusion + probes stay
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` / `AESTHETIC_DIEGETIC_LOCK.md` + fulcrumRust `docs/DEBUGGER.md` / `engine/src/debugger.rs`. STEAL_MAP / CREDITS stay sources of truth

## Closed by fulcrumRust #132 (2026-09-09)

- **Lab-Rat extract player spawn loci** — Lab-Rat. 8 bake-time pads around the extract map **edges, facing center**. Beabim owns the runtime pool (one-person-per-spawn, knock off until reset) — **not** shipped by this PR. Lab-Rat supplies the loci. [PR #132](https://github.com/initialvisuals/fulcrumRust/pull/132) (`67a5a2bb`; merge tip `71c467ed`). Seat: **Lab-Rat**. **Not** PVP / hitboxes / respawn UI. **Not** biped eye / cam height. **Not** a second MP KIND. #128 stays the Augury Home writer of `kind:spawn`; #132 is bake consume into `World.player_spawns`. STEAL_MAP / CREDITS already claimed in-PR — house shelf only. Do **not** invent A-note PRs
- **Default rim** — no spawn sheet: 8 pads on outer-chunk centers facing extract origin. #132 shipped Chebyshev **144 m** on the #81 19×19 (`playable_half_m` 151.25). Live rim **288 m** via **#142** `probes::rim_radius_m()` / `GRID_ORIGIN` (inside `playable_half_m` 295.25). Yaw 0 = **+Z**; face center `atan2(-x, -z)`. Y from `terrain.height_at`. No CHANNELS writes at the far rim (shallow / far-cold). Solo still plants on the yard (`World.spawn` / `spawn_yaw`) so the growth PoC stays in front of you. Beabim / Lab-Rat must not hardcode 144
- **Rim bearings:**

| # | Bearing | XZ | Yaw (rad) | Looks |
|---|---------|-----|-----------|--------|
| 0 | N | `0, 144` | `π` | −Z |
| 1 | NE | `144, 144` | `−3π/4` | −X −Z |
| 2 | E | `144, 0` | `−π/2` | −X |
| 3 | SE | `144, −144` | `−π/4` | −X +Z |
| 4 | S | `0, −144` | `0` | +Z |
| 5 | SW | `−144, −144` | `π/4` | +X +Z |
| 6 | W | `−144, 0` | `π/2` | +X |
| 7 | NW | `−144, 144` | `3π/4` | +X −Z |

- **Home P + SPWN** — stolen from [#127](https://github.com/initialvisuals/fulcrumRust/pull/127) / [#128](https://github.com/initialvisuals/fulcrumRust/pull/128). Same `fulcrum.probes.v1` — no new fields. **SPWN + P** (or TELE **Insert → SPAWN → P**) writes `kind:spawn` · typically `name:ground`. Hit within **48 m** XZ of a rim pad **replaces** that pad; farther hits **append**. Facing still center (manual 3D cursor sets position). Dirt sit CHANNELS leftover when bake-warm still applies (#127)
- **Beabim / Hypha read** — `World.player_spawns: Vec<SpawnLocus>` (`pos`, `yaw`, `source` = Rim / Probe). Same World as yard `spawn` / `AuguryLocusSpawn` — do not invent a net KIND. Randomize + knock-off is Beabim (**later landed #133**)
- **Smoke** — `cargo run -- --smoke` prints `spawns=rim=8` (unit-test cwd has no sheet) or `spawns=rim=N+probe=M` when Home leftover has `kind:spawn`. `probes=off` stays the CHANNELS sheet tag
- Intact / out of scope: Beabim pool / knock-off / PVP leftover **later landed #133** · Hypha biped eye / cam · second MP KIND · Home chrome (#128 writer stays Augury) · CHANNELS dirt sit (#127) · pedon (#130) · pad crawl (#114). Do **not** claim Beabim knock-off / PVP / respawn leftover shipped by #132
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust [`docs/SPAWNS.md`](https://github.com/initialvisuals/fulcrumRust/blob/main/docs/SPAWNS.md). Live rim metres: Closed by #142
## Closed by fulcrumRust #134 (2026-09-09)

- **Dirt-impact Hit pool + world FX mono fold** — Range Tech. Wire Evan’s distant dirt trio onto bullet landings and fold stereo world FX to one emitter on load. [PR #134](https://github.com/initialvisuals/fulcrumRust/pull/134) (`50aa367c`). Seat: **Range Tech** owns mixer file slots + fold. Augury still owns spatial/reverb. Hypha still owns Options Graphics post. CREDITS plant is a separate fulcrumRust PR — house shelf only. STEAL_MAP already claimed in-PR. Do **not** invent A-note PRs
- **Slot::Hit dirt pool** — `Slot::HIT_POOL`. Random among loaded files (**n≥3**). Missing / bad file → remaining pool, then procedural grit. Call site stays `mixer.play_at(Slot::Hit, Some(world))`. Punch-vs-scuff visuals untouched. Retired leftover: `assets/sfx/hit.wav` (not loaded). Mixer WAV-only (22.05 kHz 16-bit mono); MP3s in `distant_impacts/` are source
- **Dial sheet — Hit pool filenames:**

| Slot | Stem | File (mixer) |
|------|------|--------------|
| `hit` (pool) | `distant_small_medium_impact_bullet` | `assets/sfx/distant_impacts/distant_small_medium_impact_bullet.wav` |
| `hit` (pool) | `distant_small_medium_impact_bulletB` | `assets/sfx/distant_impacts/distant_small_medium_impact_bulletB.wav` |
| `hit` (pool) | `distant_small_medium_impact_bulletC` | `assets/sfx/distant_impacts/distant_small_medium_impact_bulletC.wav` |

- **World FX mono fold** — `DecodeFold::WorldMono` on `Bus::Fx` (weapons · footsteps · impacts · reactions · env one-shots): L+R → mono on decode so one emitter can pan/HRTF. `Slot::fold_world_mono()` is `bus == Fx`. Music playlist (`Bus::Music`) **Keep stereo** (`DecodeFold::Keep`) — 2D bed. UI / Voice (`Bus::Voice`) **Keep / dual-mono** — 2D confirm ticks
- **Still apply** — FX bus + Options Audio volume. Small ±6% pitch jitter on fire / foot / reload / **hit**
- Intact / out of scope: Augury spatial/reverb (#27/#56) · punch-vs-scuff visuals (#89) · PVP leftover **later landed #133** · biped eye/cam · Lab-Rat stamps/pedon · Augury Home · CREDITS plant (separate PR). Do **not** claim Augury spatial rewrite, CREDITS, or a second mixer
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + `EXTRACTION_AUDIO_LOCK.md` + fulcrumRust `engine/src/audio.rs` / `assets/sfx/distant_impacts/`

## Closed by fulcrumRust #138 (2026-09-09)

- **AIM TUNE PX travel past leftover +0.226** — Range Tech. End WEAPON Pos X hit leftover wall ~+0.226 (`−shoulder_cross_x + shoulder_x_min` from #94/#98/#84 RH hip + H). −X stayed loose. [PR #138](https://github.com/initialvisuals/fulcrumRust/pull/138) (`aa489abd`). Seat: **Range Tech**. STEAL_MAP / CREDITS already claimed in-PR — house shelf only. Do **not** invent A-note PRs
- **Dial sheet — leftover wall vs End PX box:**

| Dial | Value | Notes |
|------|-------|-------|
| Leftover derived +X wall | **+0.226** | `−shoulder_cross_x + shoulder_x_min` = `0.281 − 0.055`. Documented, **not** an End cap |
| `shoulder_x_max` / End PX | **±0.50** | AIM TUNE PX only. `AimTuner::nudge` clamps PX; PY/PZ/rot unclamped |
| Authored MP9-Z hip X | **+0.2403** | Unchanged. Ready-hip RH |
| Authored SR-25 / M24 hip X | **+0.256 / +0.261** | Unchanged |
| H dest (default hip) | **~−0.041** | Unchanged. `apply_shoulder_crossover` still floors at `shoulder_x_min` **−0.055** only |
| `shoulder_cross_x` | **−0.281** | Unchanged |
| `shoulder_x_min` | **−0.055** | H live-pose left floor only. Not the tuner box |
| Live-save schema | #103 | `aim_tune` + `aim_live`. Untouched |
| `hold_spring` / ADS blend | **7.0** / **6.4** | Untouched |

- Intact / out of scope: authored hip / H dest · #103 live-save · `hold_spring` · ADS blend · Beabim · Hypha stream · Lab-Rat stamps · Augury Home. Do **not** claim Beabim / Hypha / Lab-Rat / Augury shipped this
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust [`docs/AIM_TUNE_X_DIAL_SHEET.md`](https://github.com/initialvisuals/fulcrumRust/blob/main/docs/AIM_TUNE_X_DIAL_SHEET.md). STEAL_MAP / CREDITS stay sources of truth

## Closed by fulcrumRust #133 (2026-09-09)

- **PVP leftover — toggle / hide names / KIND_BRASS / eye hitboxes / rim respawn** — Beabim. Dial sheet after #83 / #91 / #102 / #119 / #122 so two instances can enable **peer damage** without stealing Range feel or Hypha’s mesher. Default **off** so Braeden peeks are not accidental grief. Rebased through Range [#138](https://github.com/initialvisuals/fulcrumRust/pull/138) (`aa489abd`) — AIM TUNE PX **±0.50** stays Range. [PR #133](https://github.com/initialvisuals/fulcrumRust/pull/133) (`a950ba92`; merge tip `0d73c780`). Seat: **Beabim** owns PVP leftover / KIND_PVP / KIND_BRASS. Hypha owns eye **1.60** / head **1.62** metres (#131 consume — **later landed #131**). Lab-Rat owns `World.player_spawns` (#132). Range owns local brass eject dials (#79/#134) — do not retune. Ragdoll hooks **later landed #131** `PeerBody`. Server browser parked. CREDITS + STEAL_MAP + SPAWNS + MILESTONE already claimed in-PR — house shelf only. Do **not** invent dials. Do **not** invent A-note PRs
- **Dial sheet:**

| Dial | Value | Notes |
|------|-------|-------|
| Default | **off** | Title **HOST** session board (**later landed #139**) is the pre-enter radio. `FULCRUM_PVP=1` / `--pvp` still seed peeks that skip the board. INVITE leftover left/right still flips in-raid. Joiner cannot flip |
| Glasses | existing HOST/PEER slot | `  PVP` suffix when on. **#141** `HP n  AR n` + diegetic bars when a KIND_PVP snapshot lands. Not a second HUD. Not Augury Home |
| Names | **hidden when PVP on** | Co-op / PVP-off keeps #91 fade-in tags. Loot-trail crumbs stay. Party exception later |
| Hit origin | eye **1.60 m**, centered | Camera on eye. Not 1P `muzzle_world()`, not PreferredHand, not lean. KIND_SHOT tracers stay biped hip |
| Leftover ray | leftover at #133 used **80 m** | **Later landed #147** — `LEFTOVER_HIT_M` / `first_leftover_hit` **500 m**. Flat `SMG_PELLET` **14**. Locus yard keeps own 80 |
| Head | center **1.62 m**, half **0.11** | Consume Hypha `HEAD_H` / `HEAD_HALF_H`. Skull surrounds the eye. XZ **0** — left-offset killed |
| Torso / limbs | leftover volumes | Same leftover stubs at #133. **Later landed #141** `PeerBody::hurtboxes()` + skin **0.06** + sweep **4**. Range **2.5× head** later. Mesher stays Hypha |
| Pellet | Locus `SMG_PELLET` **14** | Armor first, then HP. Same leftover as Locus — not a Range feel rewrite |
| KIND_BRASS | (14) host-relay | 3P hip + pawn-right + look. Always on a live listen stub (not gated on PVP). Range #79/#134 eject dials stay local |
| KIND | **KIND_PVP** (13) · **KIND_BRASS** (14) | PVP: On / Off / Hit / Respawn. **#141** adds **Sync**. Hit + Sync + WELCOME carry remaining HP/AR |
| Respawn | **1.20 s** after down | Local + relay `KIND_PVP RESPAWN`. Extract net uses Lab-Rat #132 `World.player_spawns` (8 rim; live **288 m** via **#142** `probes::rim_radius_m()` — #132 shipped 144 m on the 19×19; Home SPWN+P override/append). One pad per occupant; knock-off until raid reset. **#141** unique assign/rotate (host **0**; occupancy **16 m**). Solo stays on the yard `World.spawn`. Hideout stays hideout spawn. Not the 22 s bleed bag |
| Ragdoll | hook only | `apply_peer_hit_react` / `peer_corpse_anchor` / KIND_BODY Drop. Visual flop **later landed #131** `PeerBody`. Leftover volumes **later landed #141** |

- **1P ≠ 3P (held)** — #91 peer biped hip gun stub + #119 hip-stub shot muzzle unchanged. House lock held. Do **not** claim Mixamo / full 3P kit honesty
- **No-pause / KIND_RAID (held)** — #122 unchanged. Glasses HOLD % stay Augury
- Intact / out of scope: Range 1P feel / AIM TUNE / HoB / heat / SFX / eject dials (#138 PX **±0.50** consumed, not restacked) · Lab-Rat stamps / pedon / CHANNELS · Hypha STREAM / mesher (consume height only — 3P body **later landed #131**) · Augury Home binds / hatch glasses · party name exception · Range **2.5× head** · Mixamo / full 3P kit honesty / hands / gear · server browser / dedicated infra. Do **not** claim Range / Hypha / Lab-Rat / Augury shipped this
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust [`docs/PVP_DIAL_SHEET.md`](https://github.com/initialvisuals/fulcrumRust/blob/main/docs/PVP_DIAL_SHEET.md). STEAL_MAP / CREDITS / SPAWNS / MILESTONE stay sources of truth. HOST session board / no-127 invite: Closed by #139. PVP honesty: Closed by #141. Leftover ray: Closed by #147

## Closed by fulcrumRust #139 (2026-09-09)

- **HOST session board + no-127 invite seed** — Beabim. Dial sheet leftover after #91 / #122 / #133 + house-docs #91 so title **HOST** is a pre-enter session settings board (PVP on/off radio) before Deploy — not only an in-raid INVITE flip / env flag. Home / invite surfaces stop seeding `127.0.0.1`. [PR #139](https://github.com/initialvisuals/fulcrumRust/pull/139) (`0f8ee594`; merge tip `f6f8d509`). Seat: **Beabim** owns HOST-page session board / invite LAN surface. KIND_PVP default-off + solo `net=off` held. Hitboxes / names / brass / respawn stay #133. CREDITS + PVP_DIAL_SHEET + STEAL_MAP already claimed in-PR — house shelf only. Do **not** invent dials. Do **not** invent A-note PRs
- **Dial sheet:**

| Dial | Value | Notes |
|------|-------|-------|
| HOST page | SESSION board before Deploy/enter | Title **HOST** → PVP **OFF / ON** radio → **DEPLOY** enters. Radio default **off**. Settings lock into the instance |
| Peek skip | `FULCRUM_PVP=1` / `--pvp` | Seeds peeks that skip the board (`--host` + title Deploy / **Y**). INVITE leftover left/right still flips in-raid. Joiner cannot flip |
| Invite surface | LAN / real bind | Home / JOIN / glasses / `fulcrum.invite` prefer LAN. Empty JOIN field — no 127 placeholder. Do **not** seed or show `127.0.0.1` |
| Loopback | typed leftover | Same-machine `--join fulcrum://127.0.0.1:7777` still works if typed |
| KIND_PVP | default **off** held | Hitboxes / names / brass / respawn unchanged from #133 |
| Solo | `net=off` unchanged | Title Deploy without HOST stays solo |

- **1P ≠ 3P (held)** — #91 peer biped hip gun stub + #119 hip-stub shot muzzle unchanged. House lock held. Do **not** claim Mixamo / full 3P kit honesty
- **No-pause / KIND_RAID (held)** — #122 unchanged. Glasses HOLD % stay Augury
- Intact / out of scope: Range 1P feel / AIM TUNE / HoB / heat / SFX · Lab-Rat stamps / pedon / CHANNELS · Hypha STREAM / mesher / #131 `PeerBody` (**later landed #131** — #139 did not ship it) · Augury Home binds / hatch glasses (HOST sheet steals leftover HOLD frames only) · Mixamo / full 3P kit honesty / hands / gear · server browser / dedicated infra. Do **not** claim Range / Hypha / Lab-Rat / Augury shipped this
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust [`docs/PVP_DIAL_SHEET.md`](https://github.com/initialvisuals/fulcrumRust/blob/main/docs/PVP_DIAL_SHEET.md). CREDITS / STEAL_MAP / PVP_DIAL_SHEET stay sources of truth. PVP honesty: Closed by #141. Leftover ray: Closed by #147

## Closed by fulcrumRust #136 (2026-09-09)

- **Landmark AABB ride — stand / walk / hop onto extract buildings, rocks, props without push-off** — Hypha. Heightfield `ground_y` sat under the box; collide AABBs were treated as walls; `slide_xz` / `resolve` phantom-shoved XZ. Raises local pawn `ground_y` to landmark AABB tops in a **0.50 m** ride band and plants peer soles on the same lids. [PR #136](https://github.com/initialvisuals/fulcrumRust/pull/136) (`67bfc1ec`; merge tip `07513e40`). Hop onto / land **later landed #149**: vertical before XZ so a Space hop enters the same band; no extra hop dial; 3 m compounds stay walls. Seat: **Hypha** owns landmark ride. Soft dials only — not a mesher rewrite, not STREAM, not Lab-Rat stamps. STEAL_MAP / CREDITS already claimed in-PR — house shelf only. Do **not** invent A-note PRs. Do **not** claim Range / Beabim / Lab-Rat / Augury shipped this
- **Dial sheet:**

| Dial | Value | Notes |
|------|-------|-------|
| `RIDE_STEP` | **0.50** | Feet this far below an AABB top ride as floor (not XZ shove). Rocks / lips (~0.44) step up. 0.7 m crates need a hop. 3 m compounds stay walls at ground |
| `RIDE_SKIN` | **0.06** | Planted-sole hysteresis so a top does not re-enter resolve. Camera `push_out_of_walls` skips a box the eye is standing above (hop-eye above a lid too) |
| `SUPPORT_STEP` | **0.25** | Range #79 brass / tracer / mark lip. **Not widened** — leftover FX stay on the 0.25 column |
| `ride_surface_y` | `max(heightfield, AABB top under footprint)` | Hatch / shaft `floor_y` still wins when present |
| Walls | `world_walls()` landmark solids | Walls-as-floor **only** in the ride band. Locus hurtboxes stay walls (not floors) |
| Peers | `plant_simple_root_on` | Same column when walls are passed. Airborne pose keeps packet Y |
| Capsule | `slide_xz` / `resolve` | Skip XZ push when `is_ride_top`. Side hits below the band still block |
| Hop | same band | **Later landed #149** — vertical before XZ. Space hop (~0.20 m first frame) enters `RIDE_STEP`. No extra hop dial |

- **#88 plant (held)** — FOLLOW **8.5** / DEADZONE **0.04** / RISE **2.2** / SINK **6.5** / SNAP_ERR **1.15** / LIFT_MAX **0.14** / BOOT_HALF_H center **0.11** **unchanged**. Heightfield column stays first; AABB tops raise it
- Intact / out of scope: Range 1P / AIM TUNE (`SUPPORT_STEP` **0.25** stays) · Beabim KIND_* / HOST / leftover PVP (#133) · Lab-Rat stamps / CHANNELS / pedon / spawns · Augury Home · STREAM amortize (#123) · #131 biped branch (**later landed #131**). Do **not** claim Range / Beabim / Lab-Rat / Augury shipped this
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust [`docs/LANDMARK_RIDE.md`](https://github.com/initialvisuals/fulcrumRust/blob/main/docs/LANDMARK_RIDE.md). STEAL_MAP / CREDITS stay sources of truth. Hop onto: Closed by #149

## Closed by fulcrumRust #131 (2026-09-09)

- **3P biped eye 1.60 / head 1.62, left-offset killed** — Hypha. Visual / state feedback for peer bodies. Local cam + 3P `Socket::Eye` share `EYE_Y` **1.60**; visual head center `HEAD_H` **1.62** surrounds the eye (not a crown float); XZ **0** — left-offset killed. Old 3P stub at 1.22 sat ~40 cm under cam. [PR #131](https://github.com/initialvisuals/fulcrumRust/pull/131) (`2fa1d13f`; merge tip `96507be3`). Seat: **Hypha** owns 3P peer presentation / PeerBody. Not Range 1P AIM TUNE / HoB / heat. Not Beabim KIND_* / hitboxes / loot UI (Beabim consumes death/ragdoll hooks only). STEAL_MAP / CREDITS already claimed in-PR — house shelf only. Do **not** invent A-note PRs. Do **not** invent dials. Do **not** claim Range / Beabim / Lab-Rat / Augury shipped this
- **Dial sheet:**

| Dial | Value | Notes |
|------|-------|-------|
| `EYE_Y` | **1.60** | Adult eye above feet. Local cam (`MoveDials.eye_stand`) + 3P `Socket::Eye` share this |
| `HEAD_H` | **1.62** | Visual head *center*. Surrounds the eye (eyes / forehead). Not a crown float |
| `HEAD_HALF_H` | **0.11** | ME `HEAD_HEIGHT` 0.22. Skull box contains `EYE_Y` |
| Head / eye XZ | **0** | Centered on the yaw axis. **Left-offset killed.** Not PreferredHand. H crossover stays 1P viewmodel |
| Old 3P head | 1.22 | Dead stub sat ~40 cm under cam. Reticle read *above* the skull |
| Crouch squat | **0.62** | Smooth squat matching Beabim crouch flag |
| Ragdoll flop | **0.55 s** | KIND_BODY Drop → PeerBody flop |
| Pose lean | unused byte 2 (`i8/127`) | Optional −1..1; Fulcrum sign + = peek left (E). No KIND bump |

- **Also landed:** lean tilt (visual roll + 0.14 m lateral — **later deepened #145** torso peek **0.5 m** · hinge **0.55** · feet planted) · walk/run/jump loco primitives (idle / walk ≥0.40 / run ≥4.20 / jump `!grounded`) · hit-react sockets (Flinch→Chest, Stagger→Spine) · foot plant via #88 + landmark ride kept
- **#88 plant + #136 ride (held)** — FOLLOW / DEADZONE / `RIDE_STEP` **0.50** / `RIDE_SKIN` **0.06** / `SUPPORT_STEP` **0.25** **unchanged**
- **1P ≠ 3P (held)** — #91 peer biped hip gun stub + #119 hip-stub shot muzzle unchanged. House lock held. Do **not** claim Mixamo / full 3P kit honesty
- Intact / out of scope: Range 1P AIM TUNE / HoB / heat · Beabim KIND_PVP / KIND_BRASS / HOST board (already shelved house-docs #91/#92) · hit tunneling / HP UI / unique pads **later landed #141** (consume Hypha metres — do **not** claim #131 shipped leftover) · Lab-Rat stamps / pedon / probes / spawns · Augury Home chrome · STREAM amortize / 4× world expand · Mixamo clips / full player body / 2-bone IK / GPU skin. Do **not** claim Range / Beabim / Lab-Rat / Augury shipped this
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust [`docs/BIPED_3P_DIAL_SHEET.md`](https://github.com/initialvisuals/fulcrumRust/blob/main/docs/BIPED_3P_DIAL_SHEET.md). STEAL_MAP / CREDITS stay sources of truth. Lean match: Closed by #145

## Closed by fulcrumRust #137 (2026-09-09)

- **Hypha play STREAM 11×11 + warm resident hold** — Hypha. Radius + warm-return layer on top of #108 / #123 hitch (same #81 19×19 host — not a new map size). [PR #137](https://github.com/initialvisuals/fulcrumRust/pull/137) (`4ea0c1e4`; follow-up `a26628a` hold_publish / extract0·gpu split). Seat: **Hypha**. Hitch *fix* layers stay #108 / #123 (`cook=1/2` · `cook_ms=8/16` · `defer=worker/paint/gpu`). Hitch *visibility* stays Augury #110 / #121 / #128 (Home LOGS `STREAM` still keys `resident=` / `cold=` / `pend=` — held leftovers count as resident until TTL). STEAL_MAP / CREDITS already claimed in-PR — house shelf only. Do **not** invent A-note PRs
- **Window** — `STREAM_RINGS` **5** / **11×11** (was 4 / 9×9). Leading edge **80 m**, not 64 m
- **Prefetch** — **5 m** face + **walk heading** (reverse included); one cheap lod-3 look-ahead past the hot ring. Face fire unchanged (spawn-safe)
- **Resident hold** — GPU halo `HOLD_RINGS` **2** + CPU TTL `RESIDENT_TTL_SECS` **12** (`hold=2/12`). Return walk promotes / republishes — no extract. Flush / smoke still drop (rim spawn-cold honest). Soft LOD pop OK
- **Cook / hitch (held)** — cook=1/2 · cook_ms 8/16 · defer=worker/paint/gpu. Hole-fill dirty jobs (heading side first) before LOD upgrades. Halo-exit still sets `hold_publish` so extract0 / gpu stay on separate play ticks. TELE MAX ~30 ms apply/queue
- **Smoke** — `prefetch=5+heading` `hold=2/12` `defer=worker/paint/gpu`
- Intact / out of scope: Lab-Rat 7×7 stamp pad · Range / Beabim / Augury Home chrome · #131 biped · #136 landmark ride · #123 worker amortize path (deepened, not rewritten). Residual soft LOD pop / live octree still parked. 4× world + pend coalesce **later landed #142** (STREAM held 11×11)
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + `TERRAIN_NORTHSTAR.md` + fulcrumRust `docs/TERRAIN.md`

## Closed by fulcrumRust #141 (2026-09-09)

- **PVP honesty — PeerBody leftover, HP/AR glasses, unique pads** — Beabim. Dial-sheeted leftover after [#133](https://github.com/initialvisuals/fulcrumRust/pull/133) + [#139](https://github.com/initialvisuals/fulcrumRust/pull/139) + Evan’s friend peek. Downs already worked — this cook makes the HP/AR chrome, the eye ray, and the #132 rim pool honest, and **rides Hypha `PeerBody`** for leftover volumes (not the old short 5-box). [PR #141](https://github.com/initialvisuals/fulcrumRust/pull/141) (`dc94c810`; merge tip `cb9c20a3`). Seat: **Beabim** owns PVP honesty leftover. Rides Hypha #131 `PeerBody` (hurtboxes). Lab-Rat #132 rim pads. Range eject dials untouched. CREDITS + PVP_DIAL_SHEET + STEAL/SPAWNS already claimed in-PR — house shelf only. Do **not** invent dials. Do **not** invent A-note PRs
- **Closed (HP glasses stale):** KIND_PVP Hit / **Sync** + WELCOME carry remaining HP/AR. Victim kit + both HOST/JOIN glasses (`HP n  AR n` on the existing slot) + diegetic bars read the snapshot. Armor first, then HP. Downs still arm **1.20 s**
- **Closed (hit detection / tunneling):** discrete eye ray vs 20 Hz poses and thin boxes. Hurt skin **0.06** + swept AABB + **4** substeps from last **presented PeerBody** → now. Inclusive slab (origin-inside still hits). Leaned skull is a real target; crown still misses
- **Closed (same spawn pad reuse):** WELCOME assigns a unique index (host **0**). Join + respawn **rotate** onto a free pad. Occupancy = claims + peer feet within **16 m**. Knock-off if stacked
- **Dial sheet:**

| Dial | Value | Notes |
|------|-------|-------|
| Hurt leftover | `PeerBody::hurtboxes()` | Same metres as `solids()` + hurt skin. Lean / crouch / loco / ragdoll. Not the short leftover 5-box. Mesh untouched |
| Hurt skin / sweep | **0.06 m** + **4** substeps | Swept AABB from last presented body → now. Inclusive slab. Fallback leftover boxes only before first view ticks |
| Hit origin | eye **1.60 m**, centered | Camera on eye. Not 1P cant / PreferredHand / lean. KIND_SHOT tracers stay biped hip |
| Leftover ray | leftover at #141 still **80 m** | **Later landed #147** — `LEFTOVER_HIT_M` **500 m** (was 80). Flat `SMG_PELLET` **14**. Locus yard keeps own 80 |
| Head | center **1.62 m**, half **0.11** | Hypha #131 `HEAD_H` / `HEAD_HALF_H`. XZ **0**. Crown miss held |
| Vitals | Hit / Sync + WELCOME | Remaining HP/AR. HOST/JOIN glasses + diegetic bars. Armor first |
| Unique pads | host **0** · rotate · **16 m** | WELCOME unique index. Join + respawn rotate free. Occupancy = claims + peer feet within 16 m. Knock-off if stacked |
| Respawn | **1.20 s** held | Local + relay `KIND_PVP RESPAWN` (vitals reset 100 / 40). Solo yard `World.spawn` |
| KIND | **KIND_PVP** (13) · **KIND_BRASS** (14) | PVP: On / Off / Hit / Respawn / **Sync**. Brass unchanged (#133) |
| Ragdoll | **PeerBody flop** | `apply_peer_hit_react` → flinch/stagger. `KIND_BODY` Drop → visual flop. Respawn / Take clears |

- **1P ≠ 3P (held)** — #91 peer biped hip gun stub + #119 hip-stub shot muzzle unchanged. Eye ray stays centered **1.60**. House lock held. Do **not** claim Mixamo / full 3P kit honesty
- **No-pause / KIND_RAID (held)** — #122 unchanged. Glasses HOLD % stay Augury
- **HOST board (held)** — #139 unchanged. PVP radio pre-enter · no 127 invite seed
- Intact / out of scope: Range 1P feel / AIM TUNE / HoB / heat / SFX / eject dials · wound screen-react **later landed #143** (hooks Hit not Sync) · Lab-Rat stamps / pedon / CHANNELS · Hypha STREAM / mesher (#137 11×11 + hold=2/12 stay; consume height / PeerBody metres only) · Augury Home binds / hatch glasses · Death/Slain **later landed #146** · party name exception · Range **2.5× head** · Mixamo / full 3P kit honesty / hands / gear · server browser / dedicated infra. Do **not** claim Range / Hypha / Lab-Rat / Augury shipped this
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust [`docs/PVP_DIAL_SHEET.md`](https://github.com/initialvisuals/fulcrumRust/blob/main/docs/PVP_DIAL_SHEET.md). CREDITS / STEAL_MAP / SPAWNS / PVP_DIAL_SHEET stay sources of truth. Wound feel: Closed by #143. Leftover ray: Closed by #147. Death / Slain: Closed by #146

## Closed by fulcrumRust #143 (2026-09-09)

- **1P screen-react — suppress / armour / HP feel** — Range Tech. 1P local only. Jostle + intensity envelopes on existing cam punch / land-sway / recoil-cam seats. Hypha post consumes `post.wound = [blur, red, 0, 0]`. Hooks Beabim `KIND_PVP` **Hit** (and local `apply_player_wound`) — **Sync** does not punch. Death/Slain **later landed #146**. [PR #143](https://github.com/initialvisuals/fulcrumRust/pull/143) (`ae09f5f8`). Seat: **Range Tech**. CREDITS + WOUND_FEEL_DIAL_SHEET + STEAL already claimed in-PR — house shelf only. Do **not** invent dials. Do **not** invent A-note PRs
- **Dial sheet:**

| Kind | Trigger | Jostle | Blur | Red |
|------|---------|--------|------|-----|
| **Suppress-near** | Incoming `KIND_SHOT` pass-close (not a volume hit) | none | slight, short, never full-strength | none |
| **Armour** | `take_hit` / Hit snapshot ate AR only | land-sway / recoil-cam DNA | slight | **none** |
| **HP** | any health lost (split leftover counts as HP) | stronger per hit | stronger | reddish overlay, fades |

| Dial | Suppress | Armour | HP |
|------|----------|--------|----|
| Ramp / Peak / Tail | **0.035** / **0.055** / **0.200** s | **0.045** / **0.070** / **0.420** s | **0.055** / **0.090** / **0.680** s |
| Blur / Red peak | **0.22** / **0** | **0.30** / **0** | **0.58** / **0.38** |
| Jostle pitch / yaw / roll / eye | **0** | **0.018** rad / **0.014** rad / **0.016** rad / **0.010** m | **0.032** rad / **0.024** rad / **0.026** rad / **0.016** m |
| Suppress radius / hit floor | **0.92** m / **0.16** m | — | — |

- Envelope `--===--------`: soft rise to **0.38** of peak → hard front peak → long quadratic tail. Rank suppress < armour < HP. Stronger kind replaces; same kind retriggers. Successive armour / HP punches flip jostle sign. Never full-strength blur. 1P local only
- **Post** — `Session::wound_post()` → `post.wound = [blur, red, 0, 0]`. Thin `apply_wound` at end of Hypha `fs_post`. Graphics do not gate (hit react, not Options)
- **#141 (held)** — PeerBody leftover / HP/AR Sync / unique pads unchanged. Sync still applies remaining HP/AR and does **not** punch
- Intact / out of scope: Beabim net damage / #141 Sync / PeerBody · Hypha fullscreen order (SSAO → DoF → FXAA → CA → grain) · Lab-Rat stamps / pedon / 4× · AIM TUNE / HoB / heat lattice · Augury Home / hatch / Death/Slain chrome (**later landed #146**). No Tarkov / Greyzone wording. Do **not** claim Beabim / Hypha / Lab-Rat / Augury shipped this
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust [`docs/WOUND_FEEL_DIAL_SHEET.md`](https://github.com/initialvisuals/fulcrumRust/blob/main/docs/WOUND_FEEL_DIAL_SHEET.md). CREDITS / STEAL_MAP / WOUND_FEEL_DIAL_SHEET stay sources of truth

## Closed by fulcrumRust #142 (2026-09-10)

- **Hypha 4× world scale + pend coalesce** — Hypha. Next ~4× area expand on the #81 host — **not** a STREAM radius bump. [PR #142](https://github.com/initialvisuals/fulcrumRust/pull/142) (`d1eb09df`). Seat: **Hypha**. Hitch *fix* layers stay #108 / #123. Play STREAM 11×11 + warm hold stay #137. STEAL_MAP / CREDITS already claimed in-PR — house shelf only. Do **not** invent dials. Do **not** invent A-note PRs. Do **not** claim STREAM_RINGS bumped
- **Extract** — **37×37 / 592 m / 350 464 m²** (was #81 **19×19 / 304 m / 92 416 m²**). ~4× area; linear ~1.95×. World rings **9 → 18** (`RING_COUNT = GRID / 2`). Spawn stays origin
- **Stream (held)** — **11×11** (`STREAM_RINGS` 5 / `r=5`). Prefetch **5+heading** same. Resident hold **2/12** same. Cook/hitch **1/2 · 8/16 · defer=worker/paint/gpu** same
- **Pend coalesce** — admit **2** / cap **2** (`coalesce=2/2`). Play truncates heading/hole sort so mid-drain does not admit another leading-edge storm. Home SPIKE is `pendΔ ≥ 2`. Motivated by Lab-Rat walk dump max=319.4 ms · warn=15 · spike=4 when pend jumped +8/+16/+18
- **GPU concat** — walk-forward appends new hole-fills. Full rebuild when a leftover leaves the GPU halo or a resident remeshes
- **Rim spawn** — **144 → 288 m** via `probes::rim_radius_m()` / `GRID_ORIGIN`. Inside `playable_half_m` **295.25**. Smoke `spawns=rim=8`. Beabim / Lab-Rat must not hardcode 144
- **Stamp pad** — still **7×7**. Lab-Rat CHANNELS / pedon left alone
- **Smoke** — `extract_m2=350464` `rings=18` `prefetch=5+heading` `hold=2/12` `defer=worker/paint/gpu` `coalesce=2/2` `spawns=rim=8`
- **Leftover** — if seams/empty air at the new rim or on a long sprint, bump `STREAM_RINGS` to 6 / 13×13 **before** cook/hitch. If walk SPIKEs return, lower `PEND_ADMIT` to 1 before growing the window. Flatten / shared-face density not retuned for extra rings. Far 4-cell horizon + delayed LOD pop still parked
- Intact / out of scope: Lab-Rat 7×7 stamp pad / CHANNELS / pedon · Range feel / AIM TUNE / heat · Beabim net/PVP/HOST (consume `player_spawns` only) · Augury Home chrome · STREAM_RINGS bump. #81 stays the prior 8× fact
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + `TERRAIN_NORTHSTAR.md` + fulcrumRust `docs/TERRAIN.md` / `docs/SPAWNS.md`. CREDITS / STEAL_MAP stay sources of truth

## Closed by fulcrumRust #145 (2026-09-10)

- **3P torso lean 0.5 m to match 1P peek** — Hypha. Micro deepen of #131 PeerBody lean. 1P cam `lean_offset` / leanMax is **0.5 m**; #131 3P `LEAN_LATERAL` was **0.14 m** (visual roll + full-body slide). Live lean is height-weighted torso peek **0.5 m** matching Range `MoveDials.lean_offset` / feel-lab leanMax. [PR #145](https://github.com/initialvisuals/fulcrumRust/pull/145) (`2d381f04`; merge tip `d1eb09df`). Seat: **Hypha** owns 3P lean presentation. Range 1P AIM TUNE / HoB / heat / `lean_offset` read only — do **not** rewrite. Beabim KIND_* / short leftover 5-box untouched. Lab-Rat stamps untouched. #142 4× world extent untouched. STEAL_MAP / CREDITS already claimed in-PR (#131 Shipped covers 3P lean/crouch/loco) — house shelf only. Do **not** invent A-note PRs. Do **not** invent dials. Do **not** claim Range / Beabim / Lab-Rat / Augury shipped this
- **Dial sheet:**

| Dial | Value | Notes |
|------|-------|-------|
| `LEAN_LATERAL` | **0.5** | Full-lean eye/head peek. Matches Range `lean_offset` / leanMax. Read Range — do not rewrite 1P AIM TUNE |
| `LEAN_HINGE_Y` | **0.55** | Torso lean starts at thigh top. Feet/shins/root stay on yaw axis — no full-body slide |
| `LEAN_ANGLE` | **0.52** | ME `MAX_LEAN_ANGLE` roll share (~30°). Folded into the 0.5 m eye peek so 3P does not overshoot 1P |
| `LEAN_SMOOTH` | **9.5** | ME `LEAN_BODY_SMOOTH_RATE`. Kept |
| Spine boxes | pelvis / spine / chest | One 1.05 slab could not carry 0.5 m head; hitboxes match presented volumes |

- **Held from #131:** `EYE_Y` **1.60** · `HEAD_H` **1.62** · `HEAD_HALF_H` **0.11** · XZ **0** left-offset killed (centered when not leaning) · crouch squat **0.62** · ragdoll flop **0.55 s** · pose lean unused byte 2 (`i8/127`; + = peek left / E). Walk/run/jump · hit-react · #88 plant + #136 ride stay
- Intact / out of scope: Range 1P AIM TUNE / HoB / heat / `lean_offset` (read only) · Beabim KIND_* / short leftover · Lab-Rat stamps · Augury Home · #142 4× world extent · Mixamo clips / player body / 2-bone IK / GPU skin. Do **not** claim Range / Beabim / Lab-Rat / Augury shipped this
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust [`docs/BIPED_3P_DIAL_SHEET.md`](https://github.com/initialvisuals/fulcrumRust/blob/main/docs/BIPED_3P_DIAL_SHEET.md). STEAL_MAP / CREDITS stay sources of truth

## Closed by fulcrumRust #147 (2026-09-10)

- **PVP leftover ray — 500 m sniper peek** — Beabim. Dial-sheeted leftover after [#141](https://github.com/initialvisuals/fulcrumRust/pull/141) + Evan’s sniper peek. Peers stayed visible (~700 m decal) while the wound ray died at **80 m**. Zero 50/100/200 only lofts HoB — max zero 200 was clipped by that wall. [PR #147](https://github.com/initialvisuals/fulcrumRust/pull/147) (`9a9853d4`; merge tip `0b90b2ef`). Seat: **Beabim**. CREDITS + PVP_DIAL_SHEET + STEAL already claimed in-PR — house shelf only. Do **not** invent dials. Do **not** invent A-note PRs
- **Closed (sniper peeks):** `first_leftover_hit` leftover bake **500 m** (`LEFTOVER_HIT_M`; was **80**). A sniper peek at 400+ m registers `PeerBody` when aimed. Past **500 m** the leftover clips (visuals / decal can still draw ~700)
- **Dial sheet:**

| Dial | Value | Notes |
|------|-------|-------|
| Leftover ray | **500 m** (`LEFTOVER_HIT_M`) | Was **80 m**. Flat leftover bake (MP9-Z / SR-25 / M24 share the ray) |
| Pellet | Locus `SMG_PELLET` **14** | Held. No invented falloff. Range owns rifle pellet later |
| Yard | own **80 m** helper | Locus `apply_shot` does not inherit the PVP 500 m ray |
| Hurt leftover | `PeerBody` + skin **0.06** + sweep **4** | Eye-centered + anti-tunnel from **#141** held |
| Hit origin | eye **1.60 m**, centered | Head **1.62** / half **0.11**. Crown miss + wall occlude held |

- **1P ≠ 3P (held)** — #91 hip stub + #119 hip-stub shot muzzle unchanged. Eye ray stays centered **1.60**. House lock held
- **#141 (held)** — PeerBody leftover / HP/AR Sync / unique pads unchanged
- Intact / out of scope: Range 1P feel / AIM TUNE / HoB / heat / zero / falloff · Lab-Rat stamps / pedon / CHANNELS · Hypha STREAM / mesher / 4× · Augury Home / hatch / death · Mixamo / full 3P kit honesty / server browser. Do **not** claim Range / Hypha / Lab-Rat / Augury shipped this
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust [`docs/PVP_DIAL_SHEET.md`](https://github.com/initialvisuals/fulcrumRust/blob/main/docs/PVP_DIAL_SHEET.md). CREDITS / STEAL_MAP / PVP_DIAL_SHEET stay sources of truth


## Closed by fulcrumRust #146 (2026-09-10)

- **CE Slain death flow + glasses chrome** — Augury. PvE bleed-out envelope → Slain plate → PRESS SPACE respawn. Glasses + death overlay only. No HOST radio, no hitbox math, no Range live-world jostle. [PR #146](https://github.com/initialvisuals/fulcrumRust/pull/146) (`60a88648`). Seat: **Augury**. CREDITS + DEATH_DIAL_SHEET + STEAL already claimed in-PR — house shelf only. Do **not** invent dials. Do **not** invent A-note PRs
- **Closed (death cam / Slain plate):** clock expiry plays Red → FadeBlack → Beat → Slain → Prompt. Space → existing `claim_place_spawn` / hideout / rim (#141 pads)
- **Dial sheet:**

| Phase | Default | Feel |
|-------|---------|------|
| Red | `DEATH_RED_SECS` **0.55** · wash **0.78** | Deeper red/black than hit or downed |
| FadeBlack | `DEATH_FADE_SECS` **0.70** | Red → full black |
| Beat | `DEATH_BEAT_SECS` **1.00** | Hold black |
| Slain | `SLAIN_FADE_SECS` **0.78** | `assets/images/ui/deathscreens/slain.jpg` (CE `4_15_26`) object-cover |
| Prompt | `PROMPT_FADE_SECS` **0.60** | White mono **PRESS SPACE TO RESPAWN** |
| Hit flash | **0.18** s · wash **0.20** | — |
| Downed wash | **0.48** | Stim still readable |
| Bar trail | `BAR_CATCH` **6.5** default on | `FULCRUM_BAR_DELAY=0/off` snaps. Heal / Sync-up snaps |
| Glitch floor | `GLITCH_PROMPT_FLOOR` **0.12** | Text never stays unreadable |

- **PVP** — down does **not** play Slain. Beabim 1.20s leftover auto-respawn unchanged
- Intact / out of scope: Range live hit-react (#143 jostle / world blur) · Beabim HOST / KIND_PVP / hitbox · Lab-Rat stamps · Hypha 4× / landmark. Do **not** claim Range / Hypha / Lab-Rat / Beabim shipped this
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust [`docs/DEATH_DIAL_SHEET.md`](https://github.com/initialvisuals/fulcrumRust/blob/main/docs/DEATH_DIAL_SHEET.md). CREDITS / STEAL_MAP / DEATH_DIAL_SHEET stay sources of truth

## Closed by fulcrumRust #150 (2026-09-10)

- **Canted optic silhouette + AIM TUNE ATTACH** — Range Tech. 1P viewmodel only. Magnified top-rail seats (ACOG / SCOPE) also draw a **silhouette** 45° holo/red-dot on an offset rail. Iron / holo-only seats stay solo. No IOR glass, no PiP, no second composer. `ads_cant` pose already landed #100. [PR #150](https://github.com/initialvisuals/fulcrumRust/pull/150) (`6286b262`). Seat: **Range Tech**. CREDITS + CANTED_OPTIC_DIAL_SHEET + STEAL already claimed in-PR — house shelf only. Do **not** invent dials. Do **not** invent A-note PRs
- **Closed (canted companion mesh + ATTACH socket):** magnified ACOG/SCOPE draws the offset holo. ATTACH PageDown cycles **OPTIC → CANTED → CAN**. Live-save `attachments.canted`
- **Dial sheet:**

| Kit | Allow-list | Canted companion | Canted socket | Rail roll |
|-----|------------|------------------|---------------|-----------|
| MP9-Z | Iron / Holo / **ACOG** | ACOG only | **0.0339 / 0.0339 / −0.01** | **−0.785** |
| SR-25 | Iron / Holo / **ACOG** / **SCOPE** | ACOG or SCOPE | **0.0368 / 0.0368 / −0.02** | **−0.785** |
| M24 | Iron / **SCOPE** | SCOPE only | **0.0368 / 0.0368 / +0.01** | **−0.785** |

- RH default: offset rail camera-**+X**, window rolled **−45°** about +Z so `ads_cant` roll **+0.785** brings the pane to the eye. Identity `attachments.canted` = authored (pos 0, tuner RZ adds on rail roll)
- **#100 / #103 (held)** — `ads_cant` numbers · `aim_live` + optic/can stay. PreferredHand / H untouched
- Intact / out of scope: `ads_cant` retune · PreferredHand / H · 3P peer gun · Lab-Rat stamps · Hypha STREAM · Beabim net · Augury Home / Slain · IOR / magnify shader. Do **not** claim Hypha / Beabim / Lab-Rat / Augury shipped this
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust [`docs/CANTED_OPTIC_DIAL_SHEET.md`](https://github.com/initialvisuals/fulcrumRust/blob/main/docs/CANTED_OPTIC_DIAL_SHEET.md). CREDITS / STEAL_MAP / CANTED_OPTIC_DIAL_SHEET stay sources of truth

## Closed by fulcrumRust #144 (2026-09-10)

- **Stamp / building / terrain PBR polish — muddy terrain / shitty buildings** — Lab-Rat. Texture + UV only. Extract peeks read authored grit, not muddy placeholders; compounds read poured concrete, not flat grey slabs. [PR #144](https://github.com/initialvisuals/fulcrumRust/pull/144) (`de448bc`). Seat: **Lab-Rat**. Chunk metres **16** held. Stamp pad **7×7**. Hypha STREAM / geo / remesh / 37×37 walk untouched. CREDITS + STAMP_PBR_DIAL_SHEET + STEAL already claimed in-PR — house shelf only. Do **not** invent dials. Do **not** invent A-note PRs
- **Closed (muddy terrain):** default **`pbr=vendor`** — in-repo 256² COL thumbs for all five smart materials. Dirt / sand hold grit instead of a muddy wash. Cliff sides still win rock COL (vertical plane). Atelier / `FULCRUM_PBR` still win when set
- **Closed (shitty buildings):** `Solid.grade = Concrete`. Face UVs: walls = vertical plane + NRM luma, lids = XZ. Lean covers + compounds read poured concrete (cracks / formwork), not flat grit tint `[0.16, 0.15, 0.14]`
- **Dial sheet:**

| Surface | Lock |
|---------|------|
| Rocks | Offset 3-lobe density + 4-box silhouette (shade / face / chip). `Solid.grade = Rock` |
| Buildings | `Solid.grade = Concrete`. Face UVs: walls = vertical plane + NRM luma, lids = XZ |
| Terrain COL | Default **`pbr=vendor`**. 256² COL thumbs dirt / sand / rock / concrete / organic + concrete NRM. Not 4k |
| Tiles | Concrete **3.2** · rock **3.6** · dirt **3.8** · sand **4.0** · organic **3.2**. Grit **4.6 / 2.6 / 3.4**. Same 16 m chunks |
| COL mix | `0.46 + 1.08·sample`. Terrain wear/rough still rides `lod_mips`. Building faces add NRM luma + grit. Grim clamp stays |
| Extra grit | **Building faces only** — do not put `grit_modulate` back on every Transvoxel vert |

- **Peek** — `cargo run -- --smoke` (`pbr=vendor`). `FULCRUM_UV=2,2` finer existing mips — not a remesh. Identity UV is the shipped look
- **#80 / #101 / #112 (held)** — slope/PBR plugs + Blender UV sheet + Transvoxel UV consume stay the prior layers
- Intact / out of scope: Hypha STREAM / 37×37 / hitch / landmark ride · chunk resize / remesh · GPU NRM sampler on `fs_world` · Range feel / AIM TUNE / wound · Beabim leftover ray / PVP · Augury Home / death (**later landed #146**). Do **not** claim Range / Hypha / Beabim / Augury shipped this
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust [`docs/STAMP_PBR_DIAL_SHEET.md`](https://github.com/initialvisuals/fulcrumRust/blob/main/docs/STAMP_PBR_DIAL_SHEET.md). CREDITS / STEAL_MAP / STAMP_PBR_DIAL_SHEET stay sources of truth

## Closed by fulcrumRust #149 (2026-09-10)

- **Landmark ride hop — stop hop shove off tops** — Hypha. Micro follow-up to #136 stand/walk ride. Patch A open row: hopping onto / landing on extract landmark lids (buildings, rocks, ~0.44–0.7 m crates) still XZ-shoved the pawn after #136. #136 `is_ride_top` only skips a lid once feet are in `RIDE_STEP` **0.50**; local pawn slid XZ **before** hop/gravity, so the jump frame sat at last-frame Y and resolve treated the box as a wall. Live hop applies **vertical before XZ**. A Space hop (~0.20 m first frame) enters the existing band; land plants on `ride_surface_y` and keeps `is_ride_top`. [PR #149](https://github.com/initialvisuals/fulcrumRust/pull/149) (`e940a1d0`; merge tip `ff540315`). Seat: **Hypha** owns landmark ride. Soft order only — **no extra hop dial**. STEAL_MAP / CREDITS already claimed in-PR (Hypha planted the in-PR CREDITS line; Clerk classified **micro** under Evan 2026-09-09 CREDITS major-only — no new house CREDITS plant). Do **not** invent A-note PRs. Do **not** invent dials. Do **not** claim Range / Beabim / Lab-Rat / Augury shipped this
- **Dial sheet (held from #136):**

| Dial | Value | Notes |
|------|-------|-------|
| `RIDE_STEP` | **0.50** | Same band. Rocks / lips (~0.44) step up. 0.7 m crates need a hop. 3 m compounds stay walls at ground / on the hop frame |
| `RIDE_SKIN` | **0.06** | Planted-sole hysteresis; `push_out_of_walls` skip (hop-eye above a lid too) |
| `SUPPORT_STEP` | **0.25** | Range #79 brass / tracer / mark lip. **Not widened** |
| Hop | same band | **Vertical before XZ**. Space hop (~0.20 m first frame) enters `RIDE_STEP`. Land plants on `ride_surface_y`. No extra hop dial |

- **Held from #136:** `ride_surface_y` = max(heightfield, AABB top under footprint) · walls-as-floor only in the ride band · Locus hurtboxes stay walls · peers `plant_simple_root_on` same column · `slide_xz` / `resolve` skip XZ when `is_ride_top`
- **#88 plant (held)** — FOLLOW / DEADZONE / RISE / SINK **unchanged**
- Intact / out of scope: Range 1P / AIM TUNE (`SUPPORT_STEP` **0.25** stays) · Beabim KIND_* / HOST / leftover PVP · Lab-Rat stamps / CHANNELS / pedon · Augury Home · STREAM / Transvoxel · Mixamo / player body. Walk/stand ride unchanged. Do **not** claim Range / Beabim / Lab-Rat / Augury shipped this
- Detail: house `FULCRUMRUST_LAST_PASS_LOCK.md` + fulcrumRust [`docs/LANDMARK_RIDE.md`](https://github.com/initialvisuals/fulcrumRust/blob/main/docs/LANDMARK_RIDE.md). STEAL_MAP / CREDITS stay sources of truth

## Holding / locked intent — 1P viewmodel ≠ 3P biped gun (MP honesty; partial shipped #91)

Evan lock (2026-09-09 InitialVisuals). **Partial shipped #91** — peer biped hip gun stub (`reconstructed_gun`). Full 3P kit honesty / hands / gear sync still **open**. Overnight cooks steal from `FULCRUMRUST_LAST_PASS_LOCK.md`. Goes with HANDS down the road.

- **Closed (intent):** 1P weapon viewmodel ≠ MP biped + weapons + gear. Fake / artistic posing (hip fire sold for feel, canted CQC, etc.) can stay **aggressive on the first-person viewmodel**. Other players must **not** see guns sticking through eyeballs for "artistic merit"
- **Partial (path):** Beabim **#91** landed a 3-box gun stub on the networked muzzle — biped-honest hip, not 1P `muzzle_world()`. **#119** peer shot muzzle uses that same hip stub + look dir — does **not** publish 1P cant. **#133** leftover eye ray is centered **1.60 m** (not 1P cant / PreferredHand). Hypha **#131** landed 3P peer presentation / PeerBody (`EYE_Y` **1.60** · `HEAD_H` **1.62** centered). Lean match **later landed #145** (torso peek **0.5 m** · hinge **0.55** · feet planted). **#141** leftover volumes ride `PeerBody::hurtboxes()` (eye ray stays 1.60). **#147** leftover ray **500 m** (was 80; flat `SMG_PELLET` **14**; Locus yard keeps own 80). Range **#143** 1P screen-react is local only (hooks Hit not Sync). Death/Slain Augury **later landed #146**. Range canted optic **later landed #150** (1P only). House lock **1P≠3P** held. Do **not** claim Mixamo / full 3P kit honesty. Hands / gear sync remain open

| Seat | Owns |
|------|------|
| **Range Tech** | 1P dials / AIM TUNE (#97 End sheet); #94/#98/#99 hip stay 1P-only; wound feel **#143** (1P local); canted optic **#150** (1P only) |
| **Hypha** | 3P peer presentation / PeerBody **landed #131**; lean match **#145** (torso peek **0.5 m** · hinge **0.55**); `post.wound` consume **#143** |
| **Beabim** | 3P sync path — peer gun stub **landed #91**; peer shot muzzle **#119** uses that hip stub; PVP leftover **#133** (eye ray centered 1.60; 1P≠3P held); HOST session board **#139** (PVP radio pre-enter · no 127 invite seed); PVP honesty **#141** (`PeerBody::hurtboxes()` leftover · HP/AR Sync · unique pads); leftover ray **#147** (`LEFTOVER_HIT_M` **500 m** was 80 · flat `SMG_PELLET` **14** · Locus yard keeps own 80); KIND_* / hitboxes / loot UI consume Hypha metres; #143 hooks Hit not Sync; full kit honesty still open |
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
- **H** — viewmodel **crossover shoulder / left-corner peek** on the existing FoW H bind (travel landed #59; tilt path **landed #84**; RH hip bias + slight straighten **landed #94**; one more body-width + ready-hip Y **landed #98**). Not a capsule/eye slide, not a mesh mirror. Live hip_low is **#99** shotgun low-ready (U-cycle glasses **LOW HIP**; LowHip ADS still irons). Live ads_cant is **#100** Greyzone CQC (glasses **CANT 45** / **CANT ADS**)
- **U** — unaimed-hold cycle Chest → LowHip → Canted. Glasses still snap **LOW HIP** on #99 · **CANT 45** on Canted. Viewmodel springs via `hold_spring` **7.0** (**landed #109**). **U** → CANT + RMB → `ads_cant` @ 60° CQC (**#100**). RMB from Chest/LowHip stays seated optic ads
- **Mouse5** — hold-cant ADS from any hold → `ads_cant` @ 60° CQC (**#100**). Does not steal U / RMB / melee
- **End** — live aim-offset / attachment tuner (landed #97). **AIM TUNE live-save landed #103** (End LIVE → Hypha `project.json`; `aim_live` default **true**; partial merge keeps #98/#99/#100). **AIM TUNE PX travel landed #138** (`shoulder_x_max` **±0.50**; leftover +0.226 must not cap End +X; H still `shoulder_x_min` only). **Wound feel / 1P screen-react landed #143** (suppress / armour / HP; 1P local; hooks Hit not Sync). **Canted optic + AIM TUNE ATTACH landed #150** (PageDown ATTACH OPTIC→CANTED→CAN; `attachments.canted`). Feel-lab Home remapped like X→Z. Insert WEAPON↔ATTACH · PageDown pose/attachment · PageUp step · ↑↓ axis · ←→ / num± nudge · Delete JSON. Glasses `AIM TUNE`. Ready-hip / H defaults stay **#98**; hip_low **#99**; ads_cant **#100**
- **Home** — CE debugger cycle (**landed #110**; bind lock **#128**). Cycles **off → LOGS → TELE → COLL → PERF → SPWN → CHEAT → off** (not a separate unbound toggle). **Arrows + Enter** navigate; **Insert** tabs page options. **WASD / Space** stay move / hop. Hitch WARN >33 ms / HITCH >100 ms. Glasses `DEBUG`. **End** stays AIM TUNE. LOGS COPY + tracker toggles **landed #121** — **Enter** COPY · ring **800** · `[sssss.mmm]` · Insert/Delete tracks · `log_*` persist default on · medium edge events · TELE max ms stays when tracks off. Home occlusion + 3D probes **landed #125** — **P** drop look-at probe (cap **32**) · TELE/COLL/PERF **Enter** copies `fulcrum.probes` · soft Enter debounce **0.45s**. Home binds lock + spawn + denser STREAM **landed #128** — `name:ground` · `kind:spawn` via SPWN+P · denser WALK/STREAM hang tags. Lab-Rat bake consume **later landed #127**. Lab-Rat extract player spawn loci **later landed #132**. Tap **F** on the pedon stick (**#130**) does not steal hatch hold-F / kit pickup
- **Shift then Ctrl** — slide carry (sprint + crouch rising edge) **while grounded** (#78). Midair Shift+Ctrl cannot zero `vel.y` / hover
- **Hold Ctrl + mouse up/down** — analog eye height (does **not** pitch-look)
- **Mouse wheel** — move speed (**not** height; aim-offset uses wheel for crouch height — Evan’s bind wins)
- **Space** — CE hop + one air hop + land overlay (landed #59; softener #79). Hop 12/30/1 **unchanged**. Punch **0.028** · duck **0.08** · shake **0.14** gate **13** + inertia sway. Prior FPS-first "no double-jump" / #51 single-hop-only is superseded (same way #51 superseded earlier "no jump")

## Holding steady

- Hypha: distance activation / far-guts cold landed (#23) on #16 host; extract sky sample shared with Range Tech clock (#24); **#27 binaural / positional stereo on FX landed** (partial — shot propagation later; file-slot wiring landed #54; handmade vendor landed #62); **#34 listen-server / invite stub landed** (HELLO/WELCOME / **Y** host / `--join`; **#83** Beabim pose + HOLD JOIN supersedes handshake-only + no in-game join field; **#91** INVITE leftover + peer names + gun stub; **#102** loot trail; **#119** KIND_SHOT / KIND_LOCUS / KIND_BODY leftover; **#122** no-pause mute-local-only + KIND_RAID leftover (`GATE_SECS` **2.20`); **#133** PVP leftover; **#139** HOST session board / no-127 invite; terrain rewrite / dedicated infra still parked); **#42 Windows one-click release builder landed** (basic; quality/flag still open); **wider extract chunk radius landed (#43)** (7×7 / 3 rings / 112 m / 12 544 m²; extra far ring only); **near LOD raise landed #61** (then subdivs **32/16/4**); **first big-map landed #81** (19×19 open / 304 m / 92 416 m² · 9×9 stream · underfoot **32/16/8/4** · walls off · stamp pad stays 7×7; Beabim peer feet `stream_anchors` **landed #83** — coordinate only); **stream hitch amortize landed #108** (cook=1/2 · prefetch=5 m · splash-pumped load-in; hitch *visibility* stays #110 / #121 / **#128**); **worker STREAM extract+paint landed #123** (`defer=worker/paint/gpu` · skip far mask-only remesh; hitch thread never `sample_channels` on play extract); **play STREAM 11×11 + warm hold landed #137** (`STREAM_RINGS` **5** · prefetch=5+heading · hold=2/12); **biped foot plant landed #88** (FOLLOW **8.5** / DEADZONE **0.04** / RISE **2.2** / SINK **6.5** / SNAP_ERR **1.15** / LIFT_MAX **0.14** / BOOT_HALF_H center **0.11**; Mixamo sockets Pelvis / Foot_L / Foot_R / Head host hooks only; STEAL_MAP biped **partial**; Mixamo clips / player body / 2-bone IK / GPU skin parked); **landmark AABB ride landed #136** (`RIDE_STEP` **0.50** · `RIDE_SKIN` **0.06** · `SUPPORT_STEP` **0.25** unchanged; `ride_surface_y` = max(heightfield, AABB top); walls-as-floor only in the ride band; Locus hurtboxes stay walls; peers `plant_simple_root_on` same column; #88 FOLLOW/DEADZONE stay; STREAM / Lab-Rat stamps untouched); **3P biped / PeerBody landed #131** (`EYE_Y` **1.60** · `HEAD_H` **1.62** · XZ **0** left-offset killed; crouch squat **0.62** · ragdoll flop **0.55 s** · pose lean unused byte 2; lean match **later landed #145** torso peek **0.5 m** · hinge **0.55** · feet planted; Mixamo clips / player body / 2-bone IK / GPU skin parked); **3P torso lean match landed #145** (`LEAN_LATERAL` **0.5** · `LEAN_HINGE_Y` **0.55** · `LEAN_ANGLE` **0.52** · `LEAN_SMOOTH` **9.5** · pelvis/spine/chest); **#46 Options guts landed** (Graphics/Gameplay/Controls + borderless default + persist — steal CE/Mycelium; does not dump atelier into Options); **Graphics dump landed #86** (thin Options **FOG / FOG NEAR / FOG FAR / CAM NEAR / CAM FAR** + persist `project.json` alongside Range `output_device`; extract haze **375 / 520** · cam **0.05 / 2000** · clouds **0.63** · sunPunch **0.51** · light*Mul **0.11 / 0.41 / 0.61 / 2.11 / 1.65 / 1.06** · exp **1.44** · skyHdri on; hideout `haze_max` **0**; bloom / godRays / brightness / gamma **no path** — do not invent); **HDRI sun disc landed #87** (dump **sunSize 0.62** rides the procedural disc/halo; plate solar-region tone + soft disc — not a second sky); **#55 GPU post stack landed** (AO/AA/CA/grain/DoF fullscreen wgpu; toggles change the image; smoke `post=aa`; not full HDR bloom / god-ray / contact-shadow); **colorless muzzle heat landed #66** (`heat_warp_uv` before scene sample; lattice = post input only; no world-pipeline orange card; HUD/glasses still after post); **pixellation / warp strength floor landed #90** (`PostToggles.warp_strength` default **0.01**; Options Graphics **WARP** after CAM FAR; `GFX_LEN` 12→13; fog/cam/#86 rows keep indices; `pixel_warp_uv` after `heat_warp_uv`; mix toward CE PIXEL SCALE **2**; persist `project.json` `{:.2}` → `0.01`; smoke `gfx=` appends ` warp=0.01` only; STEAL_MAP Augury pixellation **todo → partial**; Augury aesthetic only — do not steal into Range); **ADS viewmodel DoF landed #68** (ADS near + far on that same pass / same Options **DOF**); **wound consume landed #143** (`apply_wound` at end of `fs_post`; `post.wound` [blur, red]; Graphics do not gate); **LOD-tied grit / material mips landed #60** (near **256²** Lab-Rat vendor / mid **64²** / far **16²** BC4-style 8-bit; far drops grain hashes; in-repo grit mips stay until Lab-Rat cooks more; smoke `grit_mips=256/64/16 n=196608 f=768`); **Transvoxel UV consume landed #112** (`promote_for_uv` + TerrainHost wear/COL honor; texture-only, never remesh); **PreferredHand + new-profile onboard landed #116** (Right default · NEW PROFILE gate · `project.json` `profile_onboarded` + `preferred_hand` permanent vs live · death clears live · extract→stash stub · `shoulder_t` 0 = authored RH / 1 = existing left dest — no mesh flip); Lab-Rat **#58 quiet grit greyscales** remain the vendored near packs (not the whole roughness→stamp cook); next live octree / unconstrained Sync dump / tunnel cutouts / SVG density-mask ingest; keep sit-on-surface CPU boxes as peek leftover; **scope glass** (greyscale ramp / IOR / no-PiP bodycam) **holding until LPVO** — Hypha Graphics when it lands; Range AIM TUNE placements first. Do **not** claim LPVO or glass shipped
- Beabim: **two-instance pose sync + HOLD JOIN landed #83** (UDP **POSE** ~20 Hz feet/yaw/pitch/grounded/crouch; 5-box slate silhouette; grounded Y rides #81 heightfield; `stream_anchors` follow remotes; Esc → JOIN types `fulcrum://` / `fw://` / `ip:port` / `localhost`; port **7777**). **Invite leftover + peer names + gun pose landed #91** (INVITE sheet after HOST / `--host` / Deploy; pause **INVITE**; Enter copies; glasses `HOST  fulcrum://ip:port`; **Y** while hosting re-copies; file leftover `fulcrum.invite` LAN + LOOP `127.0.0.1` (**later killed #139** — prefer LAN, no 127 seed); clipboard best-effort; HELLO + NAME → `FULCRUM_NAME` else **HOST** / **P{id}**; fade-in white mono over remote head; POSE + muzzle `xyz` + gun yaw/pitch; 3-box gun stub). Grounded silhouettes share Hypha #88 `plant_simple_root` (packet / handshake / HOLD join stay #83; #91 gun Y rides the same snap). Live-profile loot trail **landed #102** (KIND_LOOT host-relayed Z/F; hairline `{NAME} DROP/TAKE KIT`; starting kits stay local). World/sim leftover **landed #119** (KIND_SHOT / KIND_LOCUS / KIND_BODY; peer shot muzzle = biped hip stub; joiner plants soles only). No-pause + KIND_RAID **landed #122** (mute local pawn only; leftover = `GATE_SECS` **2.20**; honors `Cancelled`; glasses stay Augury). PVP leftover **landed #133** (KIND_PVP default **off** · hide names · KIND_BRASS · eye **1.60**/1.62 · rim respawn **1.20 s**). HOST session board + no-127 invite **landed #139** (title HOST PVP radio pre-enter · settings lock · LAN bind prefer — no 127 seed). PVP honesty **landed #141** (`PeerBody::hurtboxes()` leftover · HP/AR Sync · unique pads host **0** / **16 m**). Leftover ray **landed #147** (`LEFTOVER_HIT_M` / `first_leftover_hit` **500 m** was 80 · flat `SMG_PELLET` **14** · Locus yard keeps own 80). Extract spawn pool / knock-off **landed #133** (Lab-Rat loci **#132**; Beabim consumes `World.player_spawns`; unique rotate **later landed #141**). Hypha 3P PeerBody flop **later landed #131** (Beabim leftover volumes **later landed #141**). Range feel / HoB / heat / eject dials / 1P hip / AIM TUNE / **#143** 1P screen-react (hooks Hit not Sync) / knife-rally / joiner slash / stabilize dummy / stamps / Transvoxel rewrite / hatch / audio / ToD stay **local**. **Y** host / **I** stim / hold-**O** extract binds stay. **1P viewmodel ≠ 3P biped gun** — **partial shipped #91** (biped hip stub); 3P presentation **later landed #131**; do **not** claim Mixamo / full 3P kit honesty / hands / gear sync- Augury: Locus Standard (#18) + Inked (#26) landed; extract plant on heightfield **landed #88** (brains still Augury); spatial CE DNA via #27; **#56 CE reverb volumes landed** (DRY / YARD / OUT AABB proxies; FX wet send only; glasses peek; two-zone stub retired); **Chamber owns spatial/reverb** (does not take file slots); **down/death stub #36 landed** (partial — teammate net stabilize / timed surface kill / full loot loop later; **Death/Slain later landed #146** — Range #143 is 1P screen-react only); **#37 I-stim / Y-host bind lock**; **#41 FoW title mark landed** (vendored CE header on the #11 shell); **#45 title+HOLD analysis-core polish + Options list shell landed** (white frames / white hairline; HOLD **SYSTEM PAUSED**; Graphics/Audio/Gameplay/Controls list — Audio live #21 + **#82** DEVICE); Hypha tab guts / window / persist shipped #46 — not a second overlay; **#55 GPU post live** (HUD/glasses still after post); **#66 heat warp** sits on that stack; **#90 pixellation / floor-warp** sits after `heat_warp_uv` (Hypha owns the post dial; Augury aesthetic note only — do not claim Augury shipped the dial); **#68 ADS near** sits on that stack (same Options **DOF**); **#51 dizzy-play landed** (invert look + A/D, F-only door); **#59 hop landed** (CE hop + air hop + land overlay — #51 single hop superseded; **#79** softener on the same overlay); FoW brand / menu video **when cut ready** (big-map brief); glasses polish + EXTRACT elbow card **landed #85** (hold-O paints EXTRACT on nearest in-front hatch/shaft — no popup; Range #78 wired `Session::extract_checking`); CE Home debugger **landed #110** (**Home** toggle · LOGS / TELE / CHEAT · hitch logger; End stays AIM TUNE; glasses `DEBUG`); Home LOGS COPY + tracker toggles **landed #121** (**Enter** COPY · ring **800** · timestamps · Insert/Delete tracks · `log_*` persist default on · medium edge events); Home occlusion + 3D probes + COLL/PERF/SPWN **landed #125** (**P** look-at · Enter `fulcrum.probes` · chrome fills under glyphs); Home binds lock + spawn + denser STREAM **landed #128** (Home cycles off→tabs→off · arrows/Enter · Ins pages · no WASD/Space; `name:ground`; `kind:spawn` via SPWN+P; denser WALK/STREAM hang tags — not hitch *fix*); Lab-Rat extract player spawn loci **later landed #132**; hatch toggle + shaft ride **landed #115**; door / extract cancel chrome **landed #120**; KIND_RAID leftover **later landed #122** (Beabim; timer = `GATE_SECS` **2.20**; glasses stay Augury); timed surface kill still **~**; CE PERF/PHYS/RENDER/heartbeat/combat-log flags still open (house-docs steal later); next Sonderer/Monk/Oculus/crawler + stamp spawn filters (prefer rock/concrete; avoid organic)
- Lab-Rat: void-spore grimdark + density-driven concrete wear landed (#20); **#30 loud Inked void-spore hotspot landed**; **#38 shape-agnostic stamp/paint substrate landed** (channels + primitives; no new scar kinds; yard/Inked/curl stay consumers); **#39 extract-yard scale harness landed** (`apply_yard_harness`, pad ≈110 m², near-warm/far-cold; smoke `layers=`/`prims=`/`yard_m2=`); Hypha #43 `ExtractStubHost` / stamp pad stay **7×7** (`STUB_GRID = 7`; Hypha walk is **#142 37×37**; #81 stays the prior 8× / 19×19 fact); stamps stay **quiet on audio**; **quiet grit greyscales landed #58** (vendored 256² `grit_{grunge,crack,dust}.png` + `sample_channels` quiet height + `grit::rough` wear; smoke `grit=`); further roughness → stamp stays on **fulcrumRust only** — bake greyscales **down before density** (8-bit / half-res / BC4-style height packs); do **not** ship raw 4k 48-bit into the yard; atelier plugs **open** (Evan **clean** yell 2026-09-08 ~00:00 ET); PBR batch **in** (150 roughness + textures/PBR ~26 sets); slope/PBR/dirt/scatter/deform plugs **landed #80** (DISP bake-down + `Deform` / `GroundScatter` filled at `8,-6` / `-10,14`); Blender UV dials **landed #101** (scale/offset/rotate; identity default; `FULCRUM_UV`; texture-only — never geo); Hypha Transvoxel UV consume **landed #112** (`promote_for_uv` + TerrainHost wear/COL honor); stamp / building / terrain PBR polish **landed #144** (rocks 3-lobe shade/face/chip · buildings Concrete + face UVs · default `pbr=vendor` 256² COL · five thumbs + concrete NRM; chunk **16 m** held; STREAM/geo untouched); subtract crawl pad network **landed #114** (shallow mouth→pocket Subtract; `CRAWL_DROP` **0.38** m; glasses `CRAWL  SUBTRACT`; full guts still `[~]`); probe consume **landed #127** (`FULCRUM_PROBES` / cwd `fulcrum.probes` → `apply_to_layers`; `probes=off` if missing; not a second mesher); sandbox pedon **landed #130** (off-stream leftover CHANNELS slab; tap **F**; glasses `PEDON  F  REBAKE  GEN n`; `StampField::layers` / `stream_rev` stay cold); extract player spawn loci **landed #132** (8 rim pads; live **288 m** via **#142** → `World.player_spawns`; **48 m** override/add; #128 writer; Beabim pool still open); slope COL hooks reserved on host **#81** (vertex albedo only — Hypha owns that bind); NRM/GLOSS GPU parked; Holocron rust rewrite still waits on SVG / density-mask / monolith splits (`TOOLS.md`); next wet-lab beats stay on STEAL_MAP (SVG/density-mask ingest / experiment log); **Evan asset-ask** — stamps keep **procedural grit** until the asset list lands, then bake onto authored; style grows with peeks (void-spore + grit floor). Do **not** invent a replacement pack
- Range Tech: day/night clock + sky (#24), wall-clamped lean (#25), hold-` inspect (#28), bandage use (#31) landed; **#32 reload DNA landed** (Hold-R peek / tap-R reload / double-tap SWAP); **#33 live HoB zero landed** (**#76** SIM-only — **P** unused; leftover `hob_zero` ignored; **#78** **−/=** 50/100/200 — **O** is extract intent); **#35 heat-tune dump landed** (hold-J; **I** is Augury stim #37); **#40 Goegap HDRI on extract ToD landed** (/** plate toggle; glasses `HDRI` / `PROC`); **#47 leftover feel-lab FX landed** (brass eject / graze ricochet + spent slug / richer impact geo / `casing_draw_m` **55**; **#79** sleep/ends/marks snap to extract heightfield); **#51 AXIS_LOCK landed** (cam −Z / CE +X / barrel +Z; Lab-Rat +Y separate; FX on `sim_barrel_basis`; dizzy-play invert look/strafe + F-only door); Voice/Music/FX buses (#21) carry Hypha/#27 spatial + #47 ricochet ping (**FX bus live**); **Options Audio DEVICE landed #82** (SYSTEM DEFAULT; cpal cycle; persist `output_device`; same mixer → thin cpal voice — not a second mix tree); **authored SFX file-slot wiring shipped #54**; **handmade atelier vendor landed #62** (weapon/move off CE/feel `sfx_/` into those buses; rustles / rattles / slides come over; small set, not a full pack dump; missing → procedural); shot propagation still later; one-click Windows `build.bat` **#48 stay-open + `build.log` tee landed**; quality/flag options still cooking / open (Lab-Rat mirror for pycelium later — no dials invented here); **feel medium polish landed #57** (look inertia queue **26**; ADS look **0.86** / blend **6.4**; sprint high-ready **6.2**; slide carry **10.3 / 0.98 / 1.02**; jump land punch then **0.052** — **#79** live **0.028** + sway; AXIS_LOCK stay; no materials/range geo); **Evan peek landed #59** — **crossover shoulder / left-corner peek** (H viewmodel travel; authored hip +X ~0.24 → partial left ~−0.041 X / ~−0.181 Y, cap `shoulder_x_min` −0.055; ADS **0.32**; **#94** slight straighten pitch/yaw/roll **0.04 / 0.10 / 0.08**, supersedes #84 chest-cross 0.08/0.32/0.39 — not a mesh mirror); lean flip + deepen (**Q = peek right** / **E = peek left**; depth **0.5 / 0.5**; #25 clamp/spring/yard stay); CE hop + air hop (`JUMP_FORCE` **12** / `|GRAVITY|` **30** / one air hop **unchanged**; **#79** punch **0.028** · duck **0.08 m** · shake **0.14** gate **13** + inertia sway); heat motion v77 shimmer / lattice crawl stays Range Tech spatial input / `barrel_energy` / hold-J; **live tell is Hypha colorless post UV warp landed #66** (lattice = post input only; no world-pipeline orange card); tracers live until impact (sanity **180 s**, linger **2 s**) + FX `hit`; **Patch A muzzle landed #67** — kit-tip spawn (`muzzle_tip_local`) + `hip_honest_dir` (ads=0 on aim; ads=1 SIM HoB/zero) + tip→impact streak clamp (`tracer_len` is length, not a receiver skip); hip-fire no longer behind the handguard / upper-right of the reticle; **−/=** + #59 tracers-until-impact stay; **P** unused (#76); **O** is hold extract intent (#78); #67 did **not** fight #66 and did **not** ship heat color; **ADS viewmodel DoF landed #68** — disc blur on near depth when ADS + Options **DOF** (radius **0.0048** UV-x at ads=1; taps **12**; amount `ads_factor`, skip < 0.02; hip = 0; near fade full ≤ **0.90 m**, gone by **2.20 m**; far DoF smoothstep **9 → 46 m** unchanged; breath mul **1.6 parked**); same #55 pass / same Options **DOF**; gun softens under ADS; hip + range stay sharp on that layer; #68 did **not** ship heat color (live tell is Hypha #66); **heat dial blend landed #71** — prior blend / DNA (haze **0.07** / size **0.83** / scaleX **0.396** / lobe **0.698**); **live HeatDials landed #129** CE tip 0.2.8 (haze **0.01** / size **0.99** / scaleX **0.28** / lobe **0.40**; #66 colorless path stays; no fog blob / no orange card redraw); **SIM-only launch landed #76** — one HoB + gravity / zero model; arcade aim-dir dead; **P** unused; leftover `hob_zero` ignored; **−/=** 50/100/200 (#78); #67 hip honesty on the single SIM model; **hold-O extract / −/= zero / grounded slide landed #78** — raid `Session::extract_checking`; **O** is **not** zero; Augury EXTRACT elbow card **landed #85** (no popup). Hatch toggle + shaft ride **later landed #115**; timed surface kill still **~**; midair Shift+Ctrl cannot float-slide; **land sway softener + heightfield FX landed #79** — same #59 hop overlay; punch **0.028** / duck **0.08** / shake **0.14** gate **13** + sway; brass/tracers/marks snap to extract heightfield; `first_hit` walls-only; AXIS_LOCK +Z unchanged; Hypha first big-map host **landed #81** (Range heat / ballistics / binds **not touched**); **Hypha Graphics dump landed #86** (Options FOG / CAM NEAR/FAR + sky / post defaults — Range heat / binds / ballistics / Audio DEVICE **not touched**); **HDRI sun disc landed #87** (shared Hypha; dump **sunSize 0.62** rides the disc; plate solar-region tone + soft disc — not a second sky); kits + FX draw-distance on the wider yard still Range; kit metal/grit PBR stub **landed #64**; store `dBXpg` still **open**; **SFX remix DNA** (pitch/speed/effects; indie underground; don’t overuse the same stem) — first ±6% fire/foot/reload jitter **landed #64**; full remix minting still **open**; Music playlist beds **landed #64**; **Options Audio DEVICE landed #82** — SYSTEM DEFAULT; A/D or arrows / Enter / click; persist `output_device`; missing pin kept, playback falls back to OS default; same #21 mixer → thin cpal voice (oneshots + Music-bed loop); UI tick on the new pick; Stream on window thread (not Sync); **H shoulder-swap tilt landed #84** — tilt path; live left hold **#94** slight straighten pitch/yaw/roll **0.04 / 0.10 / 0.08** (supersedes #84 chest-cross 0.08/0.32/0.39); travel dest ~−0.041 X / ~−0.181 Y / cap **−0.055** / ads_keep **0.32**; not a capsule/eye slide, not a mesh mirror, no `scale.x = −1`; PreferredHand / new-profile onboard **later landed #116**; **Patch A RH hip bias landed #94** — first +0.08; live hip **superseded #98**; ADS X / tip spawn / `hip_honest_dir` / #89 tracers stay; **aim-offset tuner + attachment sockets landed #97** — live **End** sheet on existing ViewmodelDials + kit_mesh optic/can sockets (Insert WEAPON↔ATTACH · PageDown target · PageUp MICRO/FINE/MED/COARSE · Delete JSON; glasses `AIM TUNE`); Home debugger **later landed #110**; authored defaults now **#98**; not Home chrome at #97, not hitch logger at #97, not EffectComposer, not a second pose system; **AIM TUNE live-save landed #103** — End LIVE flush → Hypha `project.json` (`aim_live` default **true**; `aim_tune.example_smg` / `example_rifle` / `example_sniper`; pose `{x,y,z,rotX,rotY,rotZ}`; attach optic/can; load on Deploy; partial merge keeps #98/#99/#100); #97 End / Delete dump stay; End stays AIM TUNE; RECORD toggle stub — no bind; **CE Home debugger landed #110** — **Home** toggle · LOGS / TELE / CHEAT · hitch WARN/HITCH · glasses `DEBUG`; shares `project.json` `debugger_tab` with Range `aim_live` / `aim_tune`; hitch *visibility* only; hitch *fix* **later landed #108** · worker/paint/gpu deepen **later landed #123** — not CE heartbeat flags / End tuner changes; **Home LOGS COPY + tracker toggles landed #121** — **Enter** COPY · ring **800** · timestamps · Insert/Delete tracks · `log_*` persist default on · medium edge events · TELE max ms stays when tracks off; **Home occlusion + 3D probes landed #125** — **P** drop look-at probe (CE T remapped; T is bandage) · TELE/COLL/PERF Enter `fulcrum.probes` · tabs COLL/PERF/SPWN · chrome fills under glyphs · soft Enter debounce **0.45s** · Lab-Rat consume **later landed #127**; Range tip/optic consume stay **·**; **Home binds lock + spawn + denser STREAM landed #128** — Home cycles off→tabs→off · arrows/Enter · Ins pages · no WASD/Space; `name:ground`; `kind:spawn` via SPWN+P; denser WALK/STREAM hang tags — not hitch *fix* / Lab-Rat bake loci (**later landed #132**) / Range AIM TUNE; **RH hip one more body-width + ready-hip Y landed #98** — MP9-Z hip **0.2403 / −0.2128 / −0.1833**; `shoulder_cross_x` **−0.281** / `shoulder_cross_y` **0.032**; no mesh flip; **low-hip shotgun stance landed #99** — MP9-Z `hip_low` **0.2403 / −0.3528 / −0.1513** / pitch **0.145** (gap **0.140** vs ready **−0.2128**); SR-25 **−0.364 / −0.176 / 0.148**; M24 **−0.369 / −0.196 / 0.146**; U-cycle glasses **LOW HIP**; RMB from LowHip = iron ADS (not `ads_cant`); not chin-weld; #97 End tuner still live; ready hip / hip_cant / ADS / H stay #98; **canted 45° Greyzone CQC ADS landed #100** — MP9-Z `ads_cant` **0.0423 / −0.148 / −0.136** / pitch/yaw/roll **0.024 / 0.11 / 0.785** (roll stays); SR-25 / M24 **0.0468 / −0.154 / −0.148**; U+RMB / hold-Mouse5 @ 60° CQC; glasses **CANT 45** / **CANT ADS**; hip_low stays #99; #97 End tuner still live; not a canted-holo mesh / IOR glass / mesh flip / Beabim / heat / terrain; **U-cycle hold springs landed #109** — `hold_spring` **7.0** (house-medium between ADS `blend_speed` **6.4** and H `shoulder_spring` **8.0**); same exp-approach `k = 1 − e^{−rate·dt}`; glasses still snap CHEST / LOW HIP / CANT 45; inspect / sprint_high lerp on eased home; first-U seed-before-cycle; 1P only; STEAL_MAP pose-ease → **in**; ADS blend stays its own dial — **#113** scales it by kit ergo; **kit handling / ergo / MOA landed #113** — `HandlingStats` / `FeelSheet::handling`; ADS `blend_speed` **6.4** × ergo (MP9 **8.00** / SR-25 **6.40** / M24 **5.12**); handling → recoil `1/handling`; hip MOA after `hip_honest_dir`; ADS × **0.22**; `hold_spring` **7.0** stays sibling; not house mastery / gear UI / Beabim 3P / heat / PreferredHand; **projectile feel landed #89** — Vector dump rect slab + 4–6 debris (0.07–0.17 s) + feel-lab visualLength **1.5 / 18** + core **2.85 / 2.25 / 0.95** + slug **0.07** + wake 1–2 + hit flash **0.15** s + punch **8–12** (35% white) / scuff **4–6** amber + fire-pulse glyphs on existing `TracerField`; SIM / HoB / gravity **unchanged** (#76); HeatDials **later landed #129** CE tip 0.2.8 (#71 blend DNA); AXIS_LOCK +Z / #79 snap stay; #89 did **not** retune heat — not a heat-card rewrite, not Beabim, not profile onboard; **wound feel / 1P screen-react landed #143** (suppress-near / armour / HP; envelope `--===--------`; never full-strength blur; 1P local; Hypha `post.wound` [blur, red]; hooks KIND_PVP Hit not Sync; Death/Slain **later landed #146**); **canted optic + AIM TUNE ATTACH landed #150** (1P silhouette; ATTACH OPTIC→CANTED→CAN; rail roll **−0.785**); **scope glass / LPVO holding** — AIM TUNE placements first (#97); Hypha owns glass when LPVO. **Asset-ask** — clone CE / aim-offset attachment tables first; missing → ask Evan this week; primitives stay scaffolding
- Atelier: plugs **open** (Evan **clean** yell 2026-09-08 ~00:00 ET). PBR batch **in** (150 roughness + textures/PBR ~26 sets). #58 / #80 optional `FULCRUM_GRIT=` / `FULCRUM_ATELIER=` stay read-only **load** paths (downsample on load). Lab-Rat slope/PBR/dirt/scatter/deform plugs **landed #80**. Stamp / building / terrain PBR polish **landed #144** (default `pbr=vendor` 256² COL). Further roughness → stamp stays on fulcrumRust only — bake-down first; SVG / density-mask / experiment-log still open; do **not** ship raw 4k 48-bit PNG into the yard. Evan has **this week** (from 2026-09-09) to model + texture missing asks — clone CE / aim-offset tables first; primitives stay scaffolding

Steal from this shelf + steal map. Not chat scroll.
