# fulcrumRust — last-pass lock (Evan dump 2026-09-06 evening)

Canonical feel / systems answers. Steal map + seats update from this sheet.

## Where to read (2026-09-08)

fulcrumRust owns the port docs: `docs/STEAL_MAP.md`, `docs/AXIS.md`, `docs/TERRAIN.md`, `docs/MILESTONE_01_PLAYABLE.md`, `docs/CHANNELS.md`, plus `STAMPS.md` / `GROWTH_POC.md`. Patch A feedback checkpoint is repo-root `patch notes A.txt` (#72) — `X` / `~` / `*` / `·` ledger + seat owners; not a replacement for STEAL_MAP or MILESTONE. House-docs bake-book is the **dial shelf** — readable enough for seats without reading every `.rs`. Steal from the shelf + steal map. Not chat scroll.

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
- **G** cycles MP9-Z → SR-25 → M24; **4 / 5 / 6** seat directly; **U** stays unaimed-hold cycle; **1 / 2 / 3** stay Lab-Rat curl
- Mag chrome stays diegetic on the seated kit — well count **is** mag size (MP9-Z **20** / SR-25 **20** / M24 **5**); Hold-R peek / tap-R reload / double-tap SWAP (fulcrumRust #32); leftover discarded; no HUD ammo counter
- **V** — cycle optic on the seated kit’s allow-list (SMG iron/holo/acog; SR-25 + scope; M24 iron/scope); ADS pose + FOV follow
- **N** — toggle .45 suppressor / can mounts; muzzle / flash / tracer spawn follow the kit tip (`kit_mesh::muzzle_tip_local` — front of the forward-most heat-tagged box; birdcage / can). `muzzle_socket_local` stays the authored fallback. Landed #67
- FOV lock: hip **90** · iron ADS **60** · holo ADS **60** · acog ADS **25**
- Per-kit ballistics (`FeelSheet::fire`): MP9-Z AUTO ~1200 rpm / 300 m/s / kick 1.0 · SR-25 SEMI 0.14 s / 785 m/s / kick 1.15 · M24 bolt 0.65 s / 810 m/s / kick 1.75; HoB / muzzle / heat τ on the feel sheet (attachments do not invent new gameplay mags). Live zero via **− / =** 50/100/200 wrap (fulcrumRust #78; was **O** #33). Launch is **SIM only** — HoB + gravity / zero; leftover `hob_zero` ignored; **P** unused (fulcrumRust #76). Hip honesty via `hip_honest_dir` (ads=0 on aim; ads=1 keeps the SIM solve — landed #67)

## First playable flow
1. **Loading screens** cover bake/hitch — player never sees hitching except true CPU/geo overload
2. Small **interior hideout** (drawers, tables, lights, pickups, door) — geometry mostly authored
3. World **finalized before** hideout spawn (rigidize-on-start)
4. Door (**F** only — no walk-in auto-deploy, #51) → transition → **Forever Winter–style extraction test map** (PoC playground for loop + controller feel)

## World bake (Hypha)
- Prefer proving **hub + extract linked by tunnel** early if it doesn’t block the window; otherwise one medium Forever Winter instance is fine day-one
- Near-spawn **void-spore growth PoCs**: denser 2D webbing, hellish mushroom, spore-tipped creeper (curl **1 / 2 / 3** live)
- **Smart material stamps** (Lab-Rat #15 + #20): dirt/sand/rock/concrete/organic on 8 m cells, grimdark luma + sit-on-surface (void-spore bloom / brutalist mass) + density-driven concrete wear
- **Transvoxel consume channels** (Lab-Rat #17): `sample_channels` / `fill_chunk_samples` — density `> 0` solid; Hypha owns mesher / LOD / tables
- **Shape-agnostic stamp/paint substrate** (Lab-Rat #38): any authored shape → density + material; ChannelOp Union/Subtract/Paint/Replace; paint writes real / UX stubbed; mesh→voxel convert. Yard/Inked/curl stay consumers. Lab-Rat writes; Hypha remeshes
- **Extract-yard scale harness** (Lab-Rat #39): stay on the extract yard; `apply_yard_harness` via `StampField::layers`; pad ≈ **110 m²**; near-warm / far-cold (`guts_cold` **140**); smoke `layers=` `prims=` `yard_m2=`
- **Quiet grit greyscales** (Lab-Rat #58): vendored 256² luma in `assets/stamps/` (`grit_grunge` / `grit_crack` / `grit_dust`); `grit.rs` tiled world-XZ (stamp +Y); `sample_channels` quiet height under loud scars; `grit::rough` wear; `FULCRUM_GRIT=` / `FULCRUM_ATELIER=` stay read-only **load** paths. Live yard plugs until Lab-Rat cooks more. Smoke `grit=`. Near source for Hypha #60 mips
- **LOD-tied grit / material mips** (Hypha #60): `lod_mips.rs` BC4-class 8-bit height/rough on Transvoxel rings — near **256²** (#58 vendor) / mid **64²** / far **16²**; far drops grain hashes; `sample_channels` + `stamp_wear_scale` pick the ring from world XZ; in-repo `grit_*.png` until more grit cooks. Smoke `grit_mips=256/64/16 n=196608 f=768`
- **Wider extract chunk radius** (Hypha #43): `TerrainHost` **5×5 → 7×7**; **3 Chebyshev rings / 112 m span / 12 544 m²** (was 2 rings / 80 m / 6 400 m²); extra **far** ring only. Far-cold still `lod >= 2` + Locus `ACTIVATE_M` **24** / `SLEEP_M` **32**. Lab-Rat `STUB_GRID = 7`. Near LOD raise **shipped #61**
- **Near LOD raise** (Hypha #61): then bake-once Transvoxel subdivs **32/16/4** (was 16/8/4). Grid stayed #43 **7×7**. Near step **2:1**. **#81** live underfoot **32/16/8/4**. Grit mips stay **256² / 64² / 16²** (#60). Live recook / tunnels / runtime carve still parked
- **First big-map** (Hypha #81): **landed**. Live host **19×19 / 304 m / 92 416 m²** + **9×9** player-eye stream (`STREAM_RINGS` 4) + underfoot **32/16/8/4**. Walls **off**. Stamp pad still **7×7** / far-cold. Slope COL hooks (`pbr=tint` default) — vertex albedo only; NRM/GLOSS parked. Lab-Rat `Deform` / `GroundScatter` identity reserved — **no stamp bake**. Listen-server peer pos still parked. #79 land sway + heightfield FX kept. Range heat / ballistics / binds / Augury chrome **not touched**. See `TERRAIN_NORTHSTAR.md`
- **Transvoxel extract host** (Hypha #16): crates.io `transvoxel` 2.0; live underfoot **32/16/8/4** (#81; was #61 32/16/4) + transition faces; `TerrainHost` implements `VoxelHost`; verts grade from Lab-Rat tint + wear; grimdark haze; slope COL tint default #81
- **Distance activation / far-guts cold** (Hypha #23): shared Locus `ACTIVATE_M` **24** / `SLEEP_M` **32**; far stamp guts + growth/Locus upload stay cold (~19× cheaper far mean)

## Downed / revive
- HP→0 **downs** (prone crawl + thin bleed) — not menu death. Bleed-out ~`BLEED_SECS` **22.0**; extra hits while downed shave `BLEED_HIT_SECS` **6.0**. Clock expiry → `DEAD` + dark bag. Shipped Augury #36; death cam / teammate net / full loot loop still parked.
- Teammate **stabilize**, then heal with **items** (no magic heal) — hold **F** (`STABILIZE_HOLD_SECS` **1.45**); self while downed, or yard dummy when standing nearby (`REACH_M` **1.85**). Glasses `STAB STUB  NO NET` / `SELF-STAB STUB`. Solo placeholder — no fake net. Teammate net stabilize still parked.
- Equipment required — or take off the downed body
- **Self-revive** via revive stim on person — **I** while downed (`STIM_REVIVE_HP` **35**); day-one kit `stim: 1`; yard vial `YARD_STIM` **(3.55, 0, 3.20)** in front of dummy `YARD_DUMMY` **(3.55, 0, 4.55)** (`[F] PICK UP STIM`). Not a standing heal. Alive **I** is a no-op (no consume). **Y** is Hypha listen-server host (#34), alive only — does **not** stim. Downed Y is a no-op for both host and stim.
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
- **Y** = listen-server host while alive (Hypha #34). Does **not** stim. Downed **Y** is a no-op (no host, no stim)
- **V** = cycle optic on seated kit allow-list
- **N** = toggle .45 suppressor / can mounts
- **M** = map
- **/** = Goegap plate on/off (fulcrumRust #40). Does **not** steal **M**
- **Z** = drop held kit as world bag (fulcrumRust #19); **F** = pickup / swap. Hideout door is **F** only (#51 — walk-into-door does not auto-deploy). **F** tap near death bag = light corpse-reclaim stub; hold **F** = stabilize stub (self / yard dummy) or `[F] PICK UP STIM` when applicable — shipped stub (fulcrumRust #36)
- **Space** = CE hop + one air hop + land overlay (same #59 hop — **not** a second land system). `JUMP_FORCE` **12** / `|GRAVITY|` **30** / one air hop **unchanged**. **#79** softener: punch **0.028** rad · duck **0.08 m** · shake **0.14** gate **13** (normal hop ~12 does not shake) · sway eye **0.014** / yaw **0.012** / roll **0.018** · decay **4.6**. Horizontal move must not eat `vel.y`. Landed #59; softener #79. Prior FPS-first **"no double-jump"** / single-hop-only (#51) is superseded (same way #51 superseded earlier "no jump")
- **[ / ]** = extract clock ±30 min (fulcrumRust #24); **K** = dawn/noon/dusk/night snap; **L** = live cycle
- **− / =** = step live zero 50 / 100 / 200 m wrap (fulcrumRust #78). Exposure keyboard unbound (no second pair; sky `nudge_exposure` may still exist). **, / .** = cloud cover (extract only; hideout unfogged)
- **O** (hold) = raid extract-check intent (`Session::extract_checking`; fulcrumRust #78). **Not** zero. Hideout is a no-op. Augury still owns popup / glasses EXTRACT / hatch chrome (~). **P** unused after #76 (no arcade↔sim; no new bind)
- **X** = prone
- Canted hold + high/low ready from aim-offset
- **H** = viewmodel **crossover shoulder / left-corner peek** on the existing FoW H bind (landed #59). Authored hip +X ~**0.10** (right); springs across the chest to a partial left (~**−0.041**, cap `shoulder_x_min` **−0.055**). ADS keeps **0.32**. Extra left probe `shoulder_viewmodel` **0.12**. Not a capsule/eye slide, not a full mirror, not infinite travel. Help remaps off H

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
- Hideout door **F** only (#51) — walk-into-door no longer auto-deploys. Must press F
- **Space** — CE hop + one air hop + land overlay (landed #59; softener #79). `JUMP_FORCE` **12** / `|GRAVITY|` **30** / one air hop **unchanged**; punch **0.028** rad · duck **0.08 m** · shake **0.14** gate **13** · sway eye **0.014** / yaw **0.012** / roll **0.018** · decay **4.6**. Horizontal move must not eat `vel.y`. Same #59 hop — **not** a second land system. Prior FPS-first "no double-jump" / #51 single-jump-only is superseded
- Glasses may show `SLIDE` / `SPD` / `HT` / stamp material / `LOCUS  STANDARD|INKED  <brain>` / `INK HOTSPOT` / `INSPECT` / `RELOAD` / `SWAP` / `BANDAGE` / `EMPTY` / `Z{n}  SIM` / `HEAT TUNE` / `HOST` / `JOIN` / `PEER` / `DOWNED` / `DEAD` / `STIM` / `NO STIM` / `RALLY` / `NEED STAB` / `STAB STUB  NO NET` / `HDRI` / `PROC` (ToD strip, fulcrumRust #40) / `DRY` / `YARD` / `OUT` (reverb volumes #56) labels only — never a second ammo/health HUD

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
3. **Hideout door** — keep **F** prompt; walk-into-door no longer auto-deploys. Must press F
4. **Jump** — **landed #59**; softener **#79**. CE `JUMP_FORCE` **12** / `|GRAVITY|` **30**, one air hop **unchanged**. Same #59 hop overlay — **not** a second land system. Punch **0.028** rad · duck **0.08 m** · shake **0.14** gate **13** (normal hop ~12 does not shake) · sway eye **0.014** / yaw **0.012** / roll **0.018** · decay **4.6**. Horizontal move must not eat `vel.y`. Prior FPS-first **"no double-jump"** / single-jump-only (#51) is superseded (same way #51 superseded earlier "no jump")

## Heat / ADS
- Heat tell: **both** (diegetic barrel + glasses readout). **Live draw (landed #66):** colorless post UV warp — lattice is post input only; no world-pipeline orange card/lobe. Glasses `HEAT TUNE` (#35) stays the readout
- ADS/hip: **both**, weighted by enemy/context
- Heat-tune dump (fulcrumRust #35): hold **J** climbs the same `barrel_energy` cook with recoil / camera punch skipped; glasses `HEAT TUNE` only — see Heat-tune dump section. Range Tech owns cook / heat dials / hold-J. Live defaults are the **#71 blend** (v77 / dump stay DNA). Hypha owns the post path (#66)
- Heat cards look: v77 `updateBarrelHeatCardMorph` upward shimmer / lattice crawl stays the **spatial input** (landed #59). Barrel haze RGB `1.0 / lerp(0.14,0.70,h) / lerp(0.025,0.16,h²)` is feel-lab reference — **live fulcrumRust draw is colorless warp (#66)**. Live card defaults are the **#71 blend** on `heat-card-dial-sheet.md` (v77 / later dump stay DNA). Lattice vertex RGB forced to zero so this path cannot become an orange draw. Dump-dial blend cooking/~ → **landed/X** (#71)
- ADS viewmodel DoF (landed #68): disc blur on near depth when ADS + Options **DOF**. Radius **0.0048** UV-x at ads=1 · taps **12** · amount `ads_factor` (skip < 0.02; hip = 0) · near fade full ≤ **0.90 m**, gone by **2.20 m** · far DoF smoothstep **9 → 46 m** unchanged (#55) · breath mul **1.6 parked**. Same #55 pass / same Options **DOF** as #66 heat warp. See ADS viewmodel DoF section

## Visible shot feedback (fulcrumRust #12 + #19 + #59 + #67)
- LMB spends a round → muzzle flash + ballistic tracer + spark burst + hit mark (feel-lab language)
- Tracer speed / gravity / length from the SMG feel sheet. **#59:** tracers live until impact (feel-lab sanity **180 s**, linger **2 s**). Every strike plays FX `hit` (optional `hit.wav` if present; else procedural 780 Hz grit + 220→90). Graze still pings `ricochet`
- **#67 Patch A:** spawn + flash sit on the kit heat-box front (`kit_mesh::muzzle_tip_local`), not the feel-lab socket center (`muzzle_local` z=−0.405). Hip launch uses `hip_honest_dir` (ads=0 stays on **aim**; ads=1 keeps the SIM HoB/zero solve) so the 100 m HoB loft from a right-low hip muzzle is not a close-range up+right miss. Streak is feel-lab tip→impact: `tracer_len` is length again (not a 0.55 m receiver skip); back of the streak clamped to the tip. Distant speed scale kept once the slug is past the gun. Did **not** fight Hypha #66 / did **not** ship heat color. Lab-Rat terrain untouched
- FX draw-distance (hide-not-despawn, fulcrumRust #19 + #47): `muzzle_draw_m` **28** (clamp 8–80) · `spark_draw_m` **55** (clamp 8–200) · `casing_draw_m` **55** (clamp 8–200 via `live_casing`) · `decal_draw_m` **700** (clamp 50–2000) — walking back restores; they do not fill forever

## Props / audio / growth
- Destructible crates, boxes, cabinets with drawers from FoW
- Audio files from all repos + generated fills for gaps
- Living mycelium growth-enemy (gas/freeze/burn curl; sprint-grow) = Lab-Rat DNA hosted on extraction map

## Control DNA resolution
- **Locked** by fulcrumRust #12 + #51 + #59 + **#66** + **#67** + **#71** + **#76** + **#78** + **#79**: FoW scheme + aim-offset feel with Evan bind overrides above. #51 dizzy-play is the live look / strafe / door. **#59** landed Q/E flip + deepen, CE hop + air hop + land overlay, H viewmodel crossover, heat v77 look (spatial input), tracers-until-impact + FX `hit`. **#66** landed the live heat tell as colorless post UV warp (Hypha; lattice = post input only). **#67 Patch A** sits on top of **−/=** zero (#78; was **O** #33) + #76 SIM-only + #59 tracers: kit-tip spawn + hip aim-dir honesty + tip→impact streak clamp (did not fight #66). **#71** landed the Range Tech dump-dial blend on that #66 path (cooking/~ → landed/X). **#78** landed hold-**O** extract intent (Augury popup later), **−/=** zero 50/100/200, grounded slide gate (no midair float-slide). **#79** softened the same #59 land overlay (punch **0.028** · duck **0.08** · shake **0.14** gate **13** + inertia sway; hop 12/30/1 **unchanged**) and snapped brass / tracer ends / marks to extract heightfield / wall support (`first_hit` walls-only; AXIS_LOCK +Z unchanged). No remaining soft overlap on height / wheel. Lean / hop / H / hip-fire muzzle no longer cooking. Orange world heat cards are **not** the live path.
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
- Title + pause **Options** open the Augury shell (#45); Hypha Graphics/Gameplay/Controls panes live (#46); **Audio** still Range Tech #21 three-row Voice/Music/FX sheet; **A/D** or **←/→** nudge **0.05**; Esc Hypha pane / Audio → Options → title/pause; dials persist across Deploy
- Routes: **FX** = fire / dry / reload / cycle / pickup / putdown / Locus / swipe / wrap / ricochet / footstep / slide / jump / land; **Voice** = UI confirm; **Music** = hideout / extract playlist **landed #64** (five titled beds; hideout+extract advance shuffle; Options Music dial; missing → two-tone stub)
- Hard check: SMG fire SFX respect FX (FX `0` silent). File preferred when present; missing → procedural. See `EXTRACTION_AUDIO_LOCK.md` + `engine/src/audio.rs`
- File-slot **wiring** shipped #54. Day-one handmade vendor **IN** via #62 (small set, not a full CE / aim-offset pack dump). Range Tech owns weapon/move SFX on this bus. Shot propagation still later. Controller feel-medium dials shipped #57 — that is not this row. See Authored SFX file slots (#54 + #62).

## Day-one binaural / positional stereo on FX (fulcrumRust #27 + #56)
- Hypha + Augury CE FoW spatial DNA rides the **same** #21 Voice / Music / FX tree — **not a fourth bus**
- Listener follows the leaned camera basis (#25); HRTF-ish pan = equal-power ILD + Woodworth ITD + exponential distance
- World-posed FX: gunshots (muzzle), Locus slash (Standard + Inked), drops (putdown / pickup), ricochet ping at graze skip (#47); on-body FX: swipe / bandage `wrap` (#31); Voice centered; Music ambient bed
- **Reverb volumes shipped #56** (two-zone stub retired): hideout interior **DRY** · extract yard pad **YARD** · open extract **OUT** (wetter / longer tail). Authored AABB proxies; first XZ hit wins; miss → outdoor. **FX wet send only** — Voice / Music stay dry dual-mono. Glasses peek `DRY` / `YARD` / `OUT`. Listener follows camera. No extra bind. Walk off the yard pad to hear outdoor
- `Slot::Locus` / `Slot::Wrap` / `Slot::Ricochet` (#47) ride FX; file-slot **wiring** shipped #54; day-one handmade vendor **landed #62**; shot propagation still later. Augury (**Chamber**) owns spatial + authored volumes + FX wet send; Range Tech owns mixer + file slots on the same bus
- Smoke: `zone=EXTRACT spatial=1.00 sfx=file/13`; FX `0` still silences fire
- See `EXTRACTION_AUDIO_LOCK.md` + fulcrumRust `engine/src/audio.rs`

## Transvoxel extract host (fulcrumRust #16)
- Flat-world bake-once isosurface via crates.io **`transvoxel` 2.0** (Lengyel); **not** a globe
- Distance LOD: live underfoot **32 / 16 / 8 / 4** + transition faces (**#81**; was #61 32/16/4). Every adjacent step **2:1**. Stamp-pad radius stays #43
- Live grid **19×19 / 304 m / 92 416 m²** + **9×9** stream (Hypha #81). Stamp pad still **7×7** / 112 m / 12 544 m² (#43; far-cold)
- `TerrainHost` consumes Lab-Rat `sample_channels` + `density_stamp_2d` / `WearStamp`; skin = `VoxelMaterial::tint` + #81 slope COL (`pbr=tint` default)
- Extract atmosphere: ashen/slate/brutalist vertex paint, void-spore stamp tints, cheap distance haze; hideout unfogged. Walls **off**
- Parked: live LOD recook · tunnels · runtime carve · listen-server peer stream · NRM/GLOSS GPU. Near LOD raise **shipped #61**. First big-map **landed #81**. Texture mips / compression **shipped #60** on the same **distance rings** (near 256² / mid 64² / far 16²; far softer). In-repo grit mips stay until Lab-Rat cooks more — see Texture LOD compress. See `TERRAIN_NORTHSTAR.md` + fulcrumRust `docs/TERRAIN.md`


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
- Parked: live LOD recook · tunnels · runtime carve. Live walk lock **landed #81**
- See `TERRAIN_NORTHSTAR.md` + fulcrumRust `docs/TERRAIN.md`

## First big-map open extract (Hypha — landed #81)

Evan lock. **Shipped** [fulcrumRust #81](https://github.com/initialvisuals/fulcrumRust/pull/81) (2026-09-09, `73dc8fe4`). **Hypha** owns host / stream / slope COL. Lab-Rat deform/scatter identity hooks reserved only — **no stamp bake**. Stamp pad still **7×7** / far-cold. #79 land sway + heightfield FX kept. Range heat / ballistics / binds / Augury chrome **not touched**.

| Dial | Lock |
|------|------|
| **Extract** | **19×19 / 304 m / 92 416 m²** (~8× old 7×7) |
| **Walls** | **Off** — open horizon, soft XZ clamp |
| **Stream** | **9×9** window (`STREAM_RINGS` 4) by player eyes |
| **Underfoot** | **32 / 16 / 8 / 4** — every adjacent step **2:1** (was 32/16/4) |
| **Stamp pad** | Still **7×7** / far-cold (#23 guts cold) |
| **PBR** | Slope COL hooks (`pbr=tint` default). Vertex albedo only. NRM/GLOSS parked |
| **Lab-Rat** | `Deform` / `GroundScatter` + `LabRatDeform` / `LabRatScatter` identity reserved. **No stamp bake** |
| **Seams** | One extract density on every LOD · 8-subdiv bridge (32→16→8→4 stays 2:1 Lengyel) · yard flatten outer **9.2 → 20 m**. Residual LOD pop inside a chunk / far-4 horizon parked |
| **Smoke** | `subdivs=32/16/8/4` `extract_m2=92416` `resident=` `stream_cold=` `pbr=` |

| Beat | Lock |
|------|------|
| **1. Higher res** | Already **#61** (32/16/4). **#81** keeps **32/16/8/4**. Further res stays Hypha |
| **2. Drop walls** | **Landed #81** |
| **3. ~8× extend** | **Landed #81** — 19×19 / 304 m / 92 416 m² |
| **4. Chunks** | **Landed #81** — 9×9 stream |
| **5. Scatter / PBR / deform** | Still reserved / Lab-Rat open — identity hooks only. **No stamp bake** |
| **6. Slope materials** | **Landed #81** — COL tint default; NRM/GLOSS parked |
| **7. Distance load** | **Landed #81** — local-player stream. Listen-server peer pos still parked |

See `TERRAIN_NORTHSTAR.md` + `PEEK_FINDINGS.md` Closed by #81.

## Extract day/night clock + procedural sky (fulcrumRust #24)
- Feel-lab Settings **Lighting** DNA on extract only; hideout stays authored interior / unfogged (ToD does not leak inside)
- Default clock **06:21** (`TOD_DEFAULT` 6.35); sun path rise ~6:05 / set ~19:42; noon elev **56°**
- Dials: **[ / ]** ±30 min · **K** dawn→noon→dusk→night · **L** live cycle (`LIVE_HOURS_PER_SEC` 0.25) · **, / .** clouds (step 0.10) · **/** Goegap plate on/off (#40; does not steal **M**). **#78:** **− / =** step zero (was exposure). Exposure keyboard unbound — no second pair; sky `nudge_exposure` may still exist (leftover mul **1.44**)
- **No XOR sky** — one ToD sample drives ambient / key / fill / fog + procedural dome; dual color-aware lights. #40 plate rides the same sample.
- Grimdark: `EXTRACT_SKY_LUMA` **0.20** crushes noon to ashen (house aesthetic lock); Day HDRI shipped #40 (Goegap 4k; missing file stays procedural)
- Glasses on extract: `HH:MM  BAND  EXP x.xx  HDRI|PROC` labels only — never a second ammo HUD
- See `AESTHETIC_DIEGETIC_LOCK.md` + fulcrumRust `engine/src/sky.rs` / `engine/src/hdri.rs`

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

## Crossover shoulder / left-corner peek (fulcrumRust #59)

Evan lock. **Landed** [fulcrumRust #59](https://github.com/initialvisuals/fulcrumRust/pull/59). Range Tech. Quiet influence — house words: **crossover shoulder / left-corner peek** (no franchise name-drop in shelf / READMEs / public copy).

| Dial | Lock |
|------|------|
| **Authored hip** | +X ~**0.10** (right) |
| **H hold** | Springs the **viewmodel** across the chest to a partial left (~**−0.041**, cap `shoulder_x_min` **−0.055**) |
| **Not** | A capsule / eye slide. Full mirror. Infinite travel |
| **Left probe** | `shoulder_viewmodel` **0.12** — helps left-corner leans |
| **ADS** | Keeps **0.32** of the crossover |
| **H** | Existing FoW shoulder habit — viewmodel crossover, not a new key |
| **Seat** | Range Tech. Same #59 feel PR as lean flip / hop / heat look / distant hit |

See `PEEK_FINDINGS.md` Closed by #59 + `AESTHETIC_DIEGETIC_LOCK.md`.

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
- **O** — then cycled those presets. **#78:** hold extract-check intent (`Session::extract_checking`). **Not** zero. Hideout is a no-op. Augury popup / glasses / hatch chrome still **~**
- **P** — unused after #76 (no new bind). `FeelSheet::toggle_hob_zero` + session **P** apply gone; **P** no longer sets an input edge. Then #33 arcade (aim-dir) ↔ sim (HoB + ballistic zero)
- Honesty: changing zero preset changes muzzle **launch dir** only (not muzzle position). **#76:** one SIM model (`solve_ballistic_launch` — not a precomputed bake). Sim aims up to meet sight zero. Arcade aim-dir return in `muzzle_and_launch` is dead
- **#67 sits on top** — does not replace **−/=**. `hip_honest_dir` blends aim → solved by existing ADS↔hip weight: ads=0 stays on aim; ads=1 keeps this SIM solve. **−/=** still changes the zero; it bites when aimed. **O** / **P** do not. Not a new cone. Per-kit recoil / `yaw_walk` stay (MP9-Z kick 1.0 · SR-25 1.15 · M24 1.75)
- Toast: `ZERO  {n} M` (age **1.2s**, `Slot::Cycle`). `LAUNCH  ARCADE` / `LAUNCH  SIM` gone with **P**
- Glasses status strip (labels only, never a second ammo HUD): `Z{zero_dist_m:.0}  SIM` e.g. `Z100  SIM` — never `ARCADE`
- Intact / do not steal: **[ / ]** stay ToD clock; exposure keyboard unbound (no second pair); **9 / 0** left free; does not steal **T** / **C** / **R** / **Q** / **E** / **Z** / **B** / **V** / **N** / **U** / **`** / **F** / **X** / **H** / **1** / **2** / **3** / **G** / **Mouse4**; tip→impact tracers / muzzle / sparks stay; reload / knife / bandage / lean / inspect / ToD stay seated

## Patch A muzzle tip + honest hip fire (Range Tech — landed #67)

Evan lock. **Shipped** [fulcrumRust #67](https://github.com/initialvisuals/fulcrumRust/pull/67) (2026-09-08, `258b90fb`). **Range Tech** owns it. Focused ballistics / tracers / muzzle slice — no new systems, no heat-card color, no Lab-Rat terrain, no fight with Hypha #66 (colorless post warp **landed #66**). **−/=** HoB zero (#78; was **O** #33) + **#76 SIM-only** and #59 tracers-until-impact + FX `hit` stay; Patch A sits on top. **P** unused. **O** is hold extract intent (#78).

| Dial | Was | Now |
|------|-----|-----|
| **Spawn origin** | Feel-lab socket center (`muzzle_local` z=−0.405, flash-hider middle) | Front face of the forward-most **heat-tagged kit box** (birdcage / can) via `kit_mesh::muzzle_tip_local` (same DNA the viewmodel already draws). `muzzle_socket_local` stays the authored fallback |
| **Hip launch** | SIM 100 m HoB from a right-low hip muzzle → close-range **up + right** of the reticle | `hip_honest_dir`: ads=0 stays on **aim**; ads=1 keeps the SIM HoB/zero solve. Existing ADS↔hip weight. Not a new cone. **−/=** still changes the zero; it bites when aimed. **O** is extract intent (#78). **P** unused (#76) |
| **Streak** | `tracer_len` (0.55 m) used as a **receiver skip**; then a 10 m box drawn backward through the gun | Spawn **on the tip**. `tracer_len` is length again. Back of the streak clamped to the tip (feel-lab tip→impact). Distant speed scale kept once the slug is past the gun |

Do **not** claim `dBXpg` / full metal-tech kits / Lab-Rat stamp bake shipped. First big-map host **landed #81**. Heat tell is Hypha #66 colorless post warp — this PR did not fight #66 and did not ship heat color. Music playlist beds **are** shipped #64. Kit metal/grit PBR stub **is** shipped #64.

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

Evan lock. **Shipped** [fulcrumRust #78](https://github.com/initialvisuals/fulcrumRust/pull/78) (2026-09-09, `e86bfa79`). **Range Tech** owns hold-O raid intent, **−/=** zero, grounded slide gate. **The Augury** owns extract popup / glasses EXTRACT / hatch chrome — still **~** (not landed by #78). No heat / ballistics rewrite / Lab-Rat terrain. Ledger: hatch / elevator / extract popup stays `~` (hold-O check wired).

| Dial | Was | Now |
|------|-----|-----|
| **O** | cycle live zero 50 → 100 → 200 m (#33; stayed after #76) | **hold** raid extract-check intent (`Session::extract_checking`). **Not** zero. Hideout is a no-op. Augury popup later |
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

**#78** hold-O / −/= zero / grounded slide stays. **#76** SIM-only stays. Do **not** claim a second land system or Augury extract popup. First big-map host **landed #81** (this PR did not ship it). Lab-Rat stamp bake still **open**.

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
| **Siblings** | #59 v77 shimmer intent (lattice crawl stays spatial input). #67 Patch A (explicitly did not fight #66). #68 ADS near on the same stack. #55 GPU post stack. **#71 dump-dial blend** (Range Tech; did not reopen orange cards) |

Do **not** invent new Graphics sliders or claim full Mycelium bloom/god-ray heat. Do **not** flip `dBXpg` / Lab-Rat stamp bake to shipped. First big-map host **landed #81**. Do **not** reopen orange cards.

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

Intent: organic gas, less cartoony/wobbly. Tip-anchored lattice DNA stays. No second heat system. Do **not** reopen orange cards.

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

## Listen-server + invite stub (fulcrumRust #34)
- Thin `std::net` UDP hub in `engine/src/net.rs` (MyceliumEngine had no portable net crate)
- Title **HOST** / **JOIN**; in-game **Y** while alive arms listen-server; `--host` / `--join fulcrum://ip:port` (also bare `host:port` and `fw://`); env `FULCRUM_JOIN`
- Default port **7777** (`FULCRUM_PORT` override). LAN iface if OS has one, else loopback
- Glasses labels only: `HOST  ip:port`, then `JOIN` / `PEER` after HELLO/WELCOME — never a second ammo HUD
- Honesty: handshake / presence only — both machines still sim locally; **no** world replication / shoot/Locus/terrain/audio rewrite / PvEvP sim
- Solo **Deploy** unchanged (`net=off` on smoke)
- Does **not** steal **I** stim (#37), hold-**O** extract intent (#78), **−/=** zero (#78), **P** unused (#76), hold-**J** heat-tune (#35), or T/C/R/Q/E/Z/B/V/N/U/`/F/M/1/2/3/Mouse4
- Bind: **Y** alive host only (#34). Stim is **I** while downed (#37). Seats do not fight — downed Y is a no-op for host and stim.

## Down / death stub (fulcrumRust #36 + #37 bind)
- HP→0 **downs** (prone crawl + thin bleed) — not menu death. Glasses `DOWNED`. Bleed-out ~`BLEED_SECS` **22.0**; extra hits while downed shave `BLEED_HIT_SECS` **6.0**. Clock expiry → `DEAD` + dark bag.
- Constants (`engine/src/down.rs`): `BLEED_SECS` **22.0** · `BLEED_HIT_SECS` **6.0** · `STABILIZE_HOLD_SECS` **1.45** · `STIM_REVIVE_HP` **35** · `RALLY_HP` **45** / `RALLY_ARMOR` **20** / `RALLY_LOW_HP` **25** · `REACH_M` **1.85**
- Yard props: dummy `YARD_DUMMY` **(3.55, 0, 4.55)** · stim vial `YARD_STIM` **(3.55, 0, 3.20)** (in front of dummy)
- **I** while downed = stim self-revive (day-one kit `stim: 1`; yard vial `[F] PICK UP STIM`). Not a standing heal. Empty → glasses `NO STIM`. Success → `STIM` and stand at 35 HP. Alive **I** is a no-op (no consume).
- **Y** while alive = Hypha listen-server host stub (#34). Does **not** stim. Downed **Y** is a no-op for both host and stim.
- Hold **F** = stabilize stub (self while downed, or yard dummy when standing nearby). Glasses: `STAB STUB  NO NET` / `SELF-STAB STUB`. Prompt: `HOLD F  SELF-STAB STUB`. Solo placeholder — no fake net. **F** tap near bag = light corpse-reclaim stub (hold for stab; tap on bag — shipped stub).
- **T** bandage (+40 HP, Range Tech #31) unchanged as heal item. While downed and **not** stabilized: glasses `NEED STAB` (no consume). After stabilize: T stands you up with the heal chunk. Prompt: `STABILIZED  T HEAL / I STIM / SLASH RALLY`
- **Mouse4 / C** knife slash on a **downed or dying** Locus while you are downed or low (≤25 HP) → `RALLY` burst (+45 HP / +20 armor, stands if downed)
- Bleed-out ~22s → `DEAD` + dark bag; a new bleed-out **replaces** previous bag; **F** tap on bag = light corpse-reclaim stub (`DEAD  BAG STUB` / `CORPSE RECLAIM STUB`)
- Glasses/toasts labels only (never a second ammo/health HUD): `DOWNED` · `DEAD` · `STIM` · `NO STIM` · `STIM  PICKUP` · `STAB STUB  NO NET` · `RALLY` · `NEED STAB` · `DEAD  BAG STUB` · `CORPSE RECLAIM STUB` · prompts like `HOLD F  SELF-STAB STUB` / `[F] PICK UP STIM` / `STABILIZED  T HEAL / I STIM / SLASH RALLY`
- Intact / do not steal: **T** stays bandage · knife Mouse4/C · lean Q/E · inspect ` · reload R · kits G/4/5/6 · curl 1/2/3 · ToD **[ ]**/K/L/,/. · −/= zero (#78) · hold-O extract intent (#78) · P unused (#76) · hold-J heat-tune · listen-server title HOST/JOIN + `--host` / `--join` stay. **I** is stim (does not steal Y host). **Y** is host alive-only (does not steal I stim).
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
| **Consumers stay** | sit-on-surface ellipsoids; wear ribbons (prefer capsule for new work); Inked hotspot; yard plots + curl **1 / 2 / 3** (CPU boxes; #39 also writes `primitive_from_density_2d` into `layers`); Hypha StampSlots empty until fed |
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

Atelier roughness packs are **4k 48-bit PNG** — too large for extract. Do **not** ship raw 4k 48-bit into the yard. Quiet grit greyscales **landed #58** (vendored bake-downs + `sample_channels` quiet height + `grit::rough` wear). Hypha ring-mip texture LOD **shipped #60**. Atelier **150 roughness + textures/PBR ~26 sets landed**. Evan **clean** yell 2026-09-08 ~00:00 ET — plugs **open**. Whole roughness→stamp cook is **not** done.

| Seat | Lock |
|------|------|
| **Lab-Rat** | Bake greyscales **down before density** — 8-bit / half-res / BC4-style height packs. Quiet grit under loud scars. Wire on **fulcrumRust only**. **#58 landed** first in-repo 256² set — the near source for #60. Grit / slope / PBR plugs **open**. See Quiet grit greyscales |
| **Hypha** | LOD-tied mips / compression **shipped #60** on Transvoxel **distance rings**. Near **256²** (Lab-Rat vendor) · mid **64²** box mip · far **16²** box mip (cheaper / softer; far drops grain hashes). In-repo `assets/stamps/grit_*.png` until Lab-Rat cooks more. Smoke `grit_mips=256/64/16 n=196608 f=768` |
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
| **Still open** | SVG / density-mask ingest · experiment log · further roughness→stamp (PBR batch in; grit / slope / PBR plugs **open**). Hypha ring-mips **landed #60**. Atelier plugs **open** (2026-09-08 clean) |
| **Out of scope** | Range Tech controller · Augury Locus · Hypha Transvoxel tables |

See `STAMP_FEEL_LOCK.md` + fulcrumRust `docs/STAMPS.md` / `docs/CHANNELS.md`.

## Goegap HDRI on extract ToD (fulcrumRust #40)

Range Tech day plate on the #24 extract clock. Hideout stays authored interior / unfogged.

- Asset: Poly Haven **Goegap** 4k Radiance RGBE (~22MB, CC0 / Greg Zaal). `engine/build.rs` fetches **one** file at build time into `engine/assets/hdris/` (not a submodule, not the atelier texture dump). Atelier raw is fallback. Missing file → procedural dome (honest).
- Feel: Radiance RGBE decode → equirect sky/env (`engine/src/hdri.rs`). Same ToD sample still drives ambient / key / fill / fog / dome — **no XOR sky**. Plate yaw tracks the clock sun. Night fades the day plate back to the procedural dome (stars stay).
- Grimdark: `EXTRACT_SKY_LUMA` **0.20** keeps noon ashen
- **/** toggles Goegap plate on/off — does **not** steal **M** (map). Existing ToD dials: **[ / ]** · **K** · **L** · **, / .**. **#78:** **− / =** is zero (was exposure). Exposure keyboard unbound (no second pair)
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
| **Live tab** | **Audio** still opens Range Tech #21 Voice/Music/FX mixer (persists). Graphics/Gameplay/Controls filled #46 (no longer disabled `HYPHA` placeholders) |
| **Confirm** | Confirm on a Hypha tab opens that pane (#46). Audio still #21 |
| **Esc** | Hypha pane / Audio → Options → title/pause |
| **Mark** | #41 seat stands: `MARK_MAX_W` **1.70** / `MARK_MAX_H` **0.40** / `MARK_CENTER_Y` **0.58** |

See `AESTHETIC_DIEGETIC_LOCK.md`. Hypha window / tab guts / persist shipped #46. GPU post stack live #55 (toggles change the image; not full HDR bloom / god-ray). **#66** colorless heat warp and **#68** ADS near sit on that same pass / same Options **DOF**.

## Menus / settings ownership (Evan dump 2026-09-07; Augury shell #45; Hypha guts #46; GPU post #55; colorless heat #66; ADS near #68)

Augury shell polish shipped #45 (title + HOLD chrome + Options list shell + logo seat). Hypha Graphics/Gameplay/Controls guts + window mode + persist shipped #46. GPU post stack live **#55** — toggles change the image (AO/AA/CA/grain/DoF). **#66** colorless muzzle heat and **#68** ADS near DoF sit on that same pass. Honest: not the full Mycelium HDR bloom / god-ray / contact-shadow chain. Logo/title mark #41 still stands.

| Seat | Owns |
|------|------|
| **Augury** | Title + HOLD analysis-core chrome (#45). Options list shell. Logo/title mark #41. Layout/colors/buttons remain Augury |
| **Hypha** | Graphics / Gameplay / Controls tab guts + window mode + persist — **shipped #46**. GPU post stack **#55** (AO/AA/CA(+strength)/grain/DoF) — toggles change the image; HUD/glasses still after post. **#66** colorless muzzle heat (`heat_warp_uv` before scene sample; lattice = post input only). **#68** ADS near + far on that same Options **DOF** flag. Borderless default; windowed 1280×720; exclusive (borderless fallback). Persist `project.json` / `FULCRUM_SETTINGS`. **Not** packed into Range Tech ToD / Goegap / HDRI uniforms. Steal from CE/Mycelium. Does **not** dump atelier into Options Graphics. LOD-tied texture mips hook Transvoxel distance rings — see Texture LOD compress |
| **Range Tech** | Audio mixer stays #21 Voice/Music/FX (untouched by #46). Owns `barrel_energy` / heat dials / heat-tune hold-J. Live heat defaults are the **#71 blend** (v77 / dump stay DNA). ADS viewmodel DoF dials **landed #68** on Hypha’s #55 pass (same Options **DOF**). Hypha owns the #66 colorless heat post path |
| **Input** | FoW OG input manager also in scope (steal into fulcrumRust) — still cooking |

Esc Hypha pane / Audio → Options → title/pause. Still no second ammo HUD. See `AESTHETIC_DIEGETIC_LOCK.md`. Existing #12–#68 sections stay (including #66 colorless heat).

## Hypha Options guts (fulcrumRust #46)

Filled the disabled `HYPHA` stub tabs on Augury’s #45 Options list. Not a second settings overlay. Title / HOLD / Options chrome + FoW logo seat stay Augury.

| Dial | Lock |
|------|------|
| **Window** | Live via winit. **Borderless** = default launch. **Windowed** = decorated 1280×720. **Exclusive** = exclusive video mode when OS/GPU expose one, else borderless fallback. Also `--windowed` / `FULCRUM_WINDOW` (`borderless` / `windowed` / `exclusive`) |
| **Post** | Live GPU passes **#55**. AO, AA, CA (+ strength default **0.35**, step **0.05**, range **0–1**), film grain, DoF persist via #46 `project.json` / `FULCRUM_SETTINGS` and change the image. **#66** colorless muzzle heat (`heat_warp_uv` before scene sample; lattice = post input only — no world-pipeline orange card). **#68** ADS near + far on that same Options **DOF** flag — no second composer, no new Graphics sliders. Must **not** pack into Range Tech ToD / Goegap / HDRI uniforms. HUD/glasses still after post. Honest: not full HDR bloom / god-ray / contact-shadow |
| **Graphics hint** | `POST LIVE · AA ON · WINDOW LIVE · A/D NUDGE` |
| **Gameplay** | Glasses labels toggle + crosshair toggle (real — drop quads when off). Hint: `SHOOT FEEL STAYS · ENTER TOGGLE` |
| **Controls** | Look scale on feel-lab sens: `LOOK_MUL` default **1.0**, min **0.25**, max **2.0**, step **0.05**; Invert Y toggle. Binds stay README. Hint: `LOOK SITS ON FEEL-LAB SENS · BINDS IN README` |
| **Audio** | Untouched — Range Tech #21 Voice/Music/FX mixer |
| **Persist** | `project.json` in cwd, or `FULCRUM_SETTINGS=/path/to.json` |
| **Esc** | Hypha pane / Audio → Options → title or HOLD (same stack as #45) |

See `AESTHETIC_DIEGETIC_LOCK.md`. No second ammo HUD. Does not dump atelier into Options Graphics. GPU stack that made toggles change the image is #55. Colorless heat warp on that stack is #66. ADS near layer on that stack is #68.

## Hypha GPU post stack (fulcrumRust #55)

Follows #46 Settings Graphics toggles. Flags already persisted via `project.json` / `FULCRUM_SETTINGS` and previously no-op'd. #55 wires a real fullscreen wgpu stack so toggles change the image. #46 remains guts/persist. **#66** colorless muzzle heat and **#68** ADS near DoF sit on this same pass — #55 stays the GPU stack land.

- Scene color + sampleable depth, then one fullscreen pass (Mycelium `POST_PASS_ORDER` compressed):
  - **Heat** — `#66` `heat_warp_uv` **before** scene color sample (center UV / strength / radius from the tip lattice). Colorless UV displacement only — no orange RGB / emissive heat-card output
  - **AO** — depth hemisphere SSAO (8 taps; Mycelium `ssao.rs` DNA, no G-buffer)
  - **AA** — luma-edge FXAA (Mycelium `fxaa.rs`; TAA later)
  - **CA** — radial R/B offset; strength slider already in Options
  - **Grain** — hashed film grain last so FXAA does not eat it
  - **DoF** — then far-field blur only (viewmodel stayed sharp). **#68** adds ADS near on the same pass / same Options **DOF** flag (ADS near + far). Far stays smoothstep **9 → 46 m**
- HUD / glasses still draw on the swapchain after post
- Not packed into Range Tech ToD / Goegap lighting params
- Smoke: `post=aa` (default AA on); keeps #54 `sfx=file/`
- Headless naga parse/validate of the post WGSL
- Honest: toggles change the image. Not the full Mycelium HDR bloom / god-ray / contact-shadow chain
- Stay out: Atelier, Range Tech bat/HDRI ToD/shoot feel/FX file slots, Augury title mark/HOLD/reverb

See `AESTHETIC_DIEGETIC_LOCK.md` + Colorless muzzle heat (#66) + ADS viewmodel DoF (#68).

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
- **Richer impact geo** — punch vs scuff + `IMPACT_HOLE_VARIANTS` **10** + rim chips + stuck-slug plug (brass SMG / steel DMR+bolt). Rides existing spark/mark path — not a rebuild. **#79:** tracer ends + marks snap to that column; cheap slope normal so marks sit flush. `first_hit` is **walls-only** — no phantom y=0 slab. Ground belongs to the heightfield
- Audio: FX bus routes now include ricochet (with fire/dry/reload/cycle/pickup/putdown/Locus/swipe/wrap)
- Intact / do not steal: tracers / muzzle flash / #19 draw-distance stay; kits / lean / ToD+HDRI / knife / bandage / reload / heat-tune / Locus / Transvoxel / listen-server unchanged. Mag chrome stays diegetic — no second ammo HUD
- #51 AXIS_LOCK: FX long/thin axis is **sim barrel +Z** (`axis::sim_barrel_basis`) — not camera/viewmodel −Z, not CE +X. Brass toss stays camera-right; brass long axis is barrel +Z. Do not rotate Lab-Rat stamps to fix sideways plugs. See `AXIS_LOCK.md`
- See fulcrumRust `engine/src/tracers.rs` + `engine/src/feel.rs` (`FxDrawDials`) + `engine/src/kit_mesh.rs` (`ejectionPort`) + `engine/src/axis.rs` + STEAL_MAP FX rows

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
| ADS look / blend | 1.0 FOV-only / 8 | **0.86** / **6.4** (extra weight only while aiming) |
| Sprint high-ready | 9 | **6.2** |
| Slide carry | 9.6 / 0.88 / 1.2 | **10.3 / 0.98 / 1.02** |
| Jump land punch | none | then **0.052** rad overlay (does not write `pitch`). **#79** live **0.028** + inertia sway |

Binds stay #12 + #51 invert look/strafe + F-only door. **#59** landed Q/E flip + CE hop + H crossover. Hypha #55 GPU post and Augury #56 DRY/YARD/OUT reverb volumes kept.

Day-one handmade SFX vendor **landed #62** — that is audio files, not these controller dials. See Authored SFX file slots (#54 + #62).

See `AESTHETIC_DIEGETIC_LOCK.md`. Steal from this shelf + steal map — not chat scroll.

## Evan peek feel (Range Tech — landed #59)

Evan lock. **Shipped** [fulcrumRust #59](https://github.com/initialvisuals/fulcrumRust/pull/59) (2026-09-07, `6359ae97`). **Range Tech** owns it. Quiet influence — house words: **crossover shoulder / left-corner peek**. `AXIS_LOCK` three spaces stay. #51 invert look/strafe + F-only door stay. #57 medium dials stay. #58 grit stays. #56 reverb volumes stay. Kits / ToD / SFX FILE_SLOTS / Options post stay.

| Cue | Lock |
|-----|------|
| **H crossover** | Authored hip +X ~**0.10** (right). Viewmodel springs to partial left (~**−0.041**, cap `shoulder_x_min` **−0.055**). Extra left probe `shoulder_viewmodel` **0.12**. ADS keeps **0.32**. Arms-limited — not a capsule/eye slide, not a full mirror, not infinite travel. Existing H bind, not a new key |
| **Lean flip + deepen** | **Q = peek right** (same side as inverted A) · **E = peek left**. Eye formula stays `+lean → −flat_right`. Depth **0.5 / 0.5** (`leanOffset` / `leanMax`), superseding #25 0.18/0.12. Wall clamp / spring / yard covers stay |
| **Hop** | CE `JUMP_FORCE` **12** / `|GRAVITY|` **30**, one air hop **unchanged**. Same #59 hop overlay — **not** a second land system. **#79** softener: punch **0.028** rad · duck **0.08 m** · shake **0.14** gate **13** (normal hop ~12 does not shake) · sway eye **0.014** / yaw **0.012** / roll **0.018** · decay **4.6**. Horizontal move must not eat `vel.y` |
| **Heat look (v77)** | `updateBarrelHeatCardMorph` upward shimmer / lattice crawl stays the **spatial input** (not static orange blobs). Barrel haze RGB `1.0 / lerp(0.14,0.70,h) / lerp(0.025,0.16,h²)` is feel-lab reference. **Live draw is Hypha colorless post UV warp (#66)** — lattice = post input only; no world-pipeline orange card. Live card defaults are the **#71 blend** on `heat-card-dial-sheet.md` (v77 / dump stay DNA) |
| **Ballistics / distant hit** | Tracers live until impact (sanity **180 s**, linger **2 s**). Every strike plays FX `hit` (optional `hit.wav`; else procedural 780 Hz grit + 220→90). Graze still pings `ricochet`. Day-one FILE_SLOTS vendor **landed #62** (optional `hit.wav`; missing → procedural). Shot propagation still later. **#67 Patch A sits on top:** kit-tip spawn + `hip_honest_dir` + tip→impact streak clamp. Did not fight Hypha #66 / did not ship heat color |

## Authored SFX vs spatial split (day-one FILE_SLOTS vendor landed #62)

Initial Visuals Group Chat 2026-09-07. File-slot **wiring** shipped #54. Day-one handmade atelier vendor **landed #62** — small set into FILE_SLOTS, not a full CE / aim-offset pack dump. #21 FX bus is **live**. Authored audio (rustles / rattles / slides) comes over that bus. Mixer / Options Audio FX / Augury spatial+#56 reverb stay untouched. Controller feel-medium dials shipped #57 — that is not this row.

| Seat | Owns |
|------|------|
| **Range Tech** | Weapon / move SFX **file slots** off CE / FoW packs into the live #21 Voice / Music / FX buses. Not a fourth bus. Wiring shipped #54. Day-one handmade vendor landed #62. Remix first ±6% fire/foot/reload jitter **landed #64**; full remix minting still **open**. Music playlist beds **landed #64**. |
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

Shuffle of five atelier `music/` titles on hideout / extract beds: **CONCRETE_ECHO** · **Terraform** · **The Memory of The Augury** · **guttertrash** · **A Shattered Remnant From A Collapsed Distant Star**. Small 8 s / 22.05 kHz / 16-bit mono loops in fulcrumRust `assets/music/` (not the 5–11 MB MP3s). Each hideout / extract start advances the shuffle. Options Audio Music dial still scales the bed. Missing file → old two-tone stub. Same #21 Voice / Music / FX tree — not a fourth bus. Music stays dry dual-mono (#56). Voice / FX / Augury spatial+reverb untouched. Overrides: `FULCRUM_MUSIC` / `FULCRUM_ATELIER` read-only. See `EXTRACTION_AUDIO_LOCK.md`.

## Kit metal/grit PBR stub (landed #64)

Range Tech. Store `dBXpg` greeble pack was **not** on the shelf — still **open**/missing. Used what was: brand/TRIMSHEET_MICRO (+ grey); atelier textures/PBR MetalPanelRectangular / MetalCorroded (256² crops); handful of scratch / fingerprint roughness masks from the 150-roughness pack. Boxes stay color-only (stub PBR): albedo mix + roughness/mask on MP9-Z / SR-25 / M24. House DNA: **gold+black tech trim** hairlines, not gold-plate, not Locus veins. Crops vendored in fulcrumRust `assets/kit/`. Atelier read-only (`FULCRUM_KIT` / `FULCRUM_ATELIER`). Do **not** claim full metal-tech / `dBXpg` kits shipped — only this stub. See `AESTHETIC_DIEGETIC_LOCK.md`.

## Still soft / seat-owned timing
- Exact day-one world: single medium instance vs hub+tunnel+extract (Hypha chooses if Evan didn’t hard-pick)
- Near LOD raise **shipped #61** (then subdivs **32/16/4**). Live underfoot **#81 32/16/8/4**. Stamp pad stays Hypha #43 **7×7**. Live LOD recook / tunnels / runtime carve / listen-server peer stream still parked
- First big-map host **landed #81**. Live walk is **19×19 / 304 m / 92 416 m²** + **9×9** stream. Stamp pad still **7×7**. Slope COL tint default; NRM/GLOSS parked. Lab-Rat deform/scatter identity reserved — **no stamp bake**. Continues on fulcrumRust
- Menus / settings: Augury title+HOLD chrome + Options shell shipped #45; Hypha Graphics/Gameplay/Controls + window + persist shipped #46; GPU post stack shipped **#55** (AO/AA/CA/grain/DoF; smoke `post=aa`; not full bloom/god-ray); **colorless muzzle heat landed #66** (sample-only UV warp; no new Graphics sliders); **ADS viewmodel DoF landed #68** (ADS near + far on the same Options **DOF**); **heat dial blend landed #71** (Range Tech; dump-dial cooking/~ → landed/X; #66 path stays)
- One-click Windows `build.bat` **landed as Hypha #42 + Range Tech #48** (always pause + `build.log` tee); quality/flag options still cooking / open (Lab-Rat mirror for pycelium later — no dials invented here)
- Embodied feel pass: Range Tech medium dials **landed #57** (look inertia queue **26**; ADS **0.86** / **6.4**; sprint high-ready **6.2**; slide **10.3 / 0.98 / 1.02**; land punch then **0.052** rad overlay — **#79** live punch **0.028** + inertia sway; AXIS_LOCK stay; no materials / range geo)
- Evan peek feel **landed #59**: H viewmodel crossover (hip +X ~0.10 → partial left ~−0.041, cap `shoulder_x_min` −0.055; ADS **0.32**); lean flip + deepen (**Q = peek right** / **E = peek left**; depth **0.5 / 0.5**); CE hop + air hop (`JUMP_FORCE` **12** / `|GRAVITY|` **30** / one air hop **unchanged**); **#79** land softener punch **0.028** · duck **0.08 m** · shake **0.14** gate **13** + inertia sway; heat motion v77 shimmer stays Range Tech spatial input / `barrel_energy` / hold-J; **live tell is Hypha colorless post UV warp landed #66** (lattice = post input only; no world-pipeline orange card); tracers live until impact + FX `hit`. Day-one handmade SFX vendor **landed #62**. **Patch A muzzle landed #67** — kit-tip spawn (`muzzle_tip_local`) + `hip_honest_dir` + tip→impact streak clamp. **−/=** zero + #59 tracers-until-impact stay; **P** unused (#76); **O** is hold extract intent (#78). #67 did **not** fight #66 and did **not** ship heat color. **ADS viewmodel DoF landed #68** — ADS near + far on the same #55 pass / same Options **DOF** (radius **0.0048**; taps **12**; near fade 0.90→2.20 m; breath mul **1.6 parked**). #68 did **not** ship heat color (live tell is Hypha #66). **Heat dial blend landed #71** — dump-dial cooking/~ → landed/X; live defaults sit between old bake and the dump (haze **0.07** / size **0.83** / scaleX **0.396** / lobe **0.698**); #66 colorless path stays; no orange card redraw. **SIM-only launch landed #76** — one HoB + gravity / zero model; arcade aim-dir dead; leftover `hob_zero` ignored; **P** unused; **−/=** 50/100/200 (#78); #67 hip honesty on the single SIM model. **Hold-O extract / −/= zero / grounded slide landed #78** — raid `Session::extract_checking`; **O** is **not** zero; Augury popup / glasses / hatch chrome still **~**; midair Shift+Ctrl cannot float-slide. **Land sway softener + heightfield FX landed #79** — same #59 hop overlay (**not** a second land system); punch **0.028** / duck **0.08** / shake **0.14** gate **13** + sway eye/yaw/roll + decay **4.6**; brass / tracers / marks snap to extract heightfield / wall support; `first_hit` walls-only; AXIS_LOCK +Z unchanged. Lab-Rat terrain untouched. Music playlist beds **landed #64**. Kit metal/grit PBR stub **landed #64**. Store `dBXpg` still **open**. First big-map host **landed #81**. Shot propagation still later
- Texture compression (2026-09-07): atelier roughness packs are **4k 48-bit PNG** — too large. Do **not** ship raw 4k 48-bit into the yard. Lab-Rat **#58 quiet grit greyscales landed** (vendored 256² bake-downs + `sample_channels` quiet height + `grit::rough` wear — the near source). Hypha LOD-tied mips **shipped #60** on Transvoxel **distance rings** (near 256² / mid 64² / far 16²; far softer). Do **not** claim the whole roughness→stamp cook. Near LOD raise **shipped #61**; live underfoot **#81 32/16/8/4**; grit mips stay. First big-map host **landed #81**. See `STAMP_FEEL_LOCK.md` + `TERRAIN_NORTHSTAR.md`
- Atelier: plugs **open** (Evan **clean** yell 2026-09-08 ~00:00 ET). PBR batch **in** (150 roughness + textures/PBR ~26 sets). #58 `FULCRUM_GRIT=` / `FULCRUM_ATELIER=` stay read-only **load** paths. Further Lab-Rat roughness → stamp stays on **fulcrumRust only** — bake-down first; grit / slope / PBR **open**. Range Tech kit metal/grit PBR stub **landed #64**; store `dBXpg` still **open**. Music playlist beds **landed #64**. Augury FoW brand / menu video **when cut ready**
- **SFX remix DNA** (2026-09-08 ~00:00 ET): creative reuse OK — pitch / speed / effects to mint new one-shots from existing packs; indie underground vibe; don’t overuse the same stem. #62 vendor stays the live FILE_SLOTS fill. First ±6% fire/foot/reload jitter **landed #64**; full remix minting still **open**
- Holocron (Evan gift 2026-09-08): atelier `Holocron_Visualizer.py` + `Analyze-Holocron.ps1` — tree nested-rectangle viewer for file bases. Cut down monoliths (agent context; overwrite loss). Lab-Rat rust-friendly rewrite **after** slope/PBR. Later: `channels.rs` / stamp stacks / `feel` / `kit_mesh`. See `TOOLS.md`. Do **not** claim rewrite shipped
- Growth PoCs after window exists
- Shot propagation on the spatial FX path (binaural day-one landed #27; reverb volumes landed #56; file-slot wiring landed #54; handmade vendor landed #62)
- Authored SFX vs spatial split: Range Tech file-slot **wiring** shipped #54; day-one handmade vendor **landed #62** (small set, not a full pack dump). **SFX remix DNA** first ±6% fire/foot/reload jitter **landed #64**; full remix minting still **open**. Music playlist beds **landed #64**. Shot propagation still later. Augury (Chamber) keeps spatial/reverb DNA (**volumes shipped #56**); Lab-Rat stamps stay quiet on audio (Initial Visuals Group Chat 2026-09-07)

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
Extract day/night clock + procedural sky: fulcrumRust PR #24 (2026-09-07). **−/=** exposure **superseded #78** — keyboard unbound; **−/=** is zero.
Wall-clamped Q/E lean polish: fulcrumRust PR #25 (2026-09-07).
Locus Inked on yard: fulcrumRust PR #26 (2026-09-07).
Day-one binaural / positional stereo on FX: fulcrumRust PR #27 (2026-09-07).
CE reverb volumes (DRY / YARD / OUT, FX wet send): fulcrumRust PR #56 (2026-09-07) — The Augury.
Hold-` inspect pose: fulcrumRust PR #28 (2026-09-07).
Lab-Rat Inked void-spore hotspot: fulcrumRust PR #30 (2026-09-07).
Bandage use stub: fulcrumRust PR #31 (2026-09-07).
Mag reload DNA: fulcrumRust PR #32 (2026-09-07).
Live HoB zero / launch dials: fulcrumRust PR #33 (2026-09-07). Dual-path arcade↔sim **superseded #76** — **P** unused. Zero bind **superseded #78** — **−/=** 50/100/200; **O** is hold extract intent.
Listen-server + invite stub: fulcrumRust PR #34 (2026-09-07).
Heat-tune dump (hold-J): fulcrumRust PR #35 (2026-09-07).
Down / death stub: fulcrumRust PR #36 (2026-09-07).
Augury I-stim / Y-host bind: fulcrumRust PR #37 (2026-09-07).
Shape-agnostic stamp/paint substrate: fulcrumRust PR #38 (2026-09-07).
Extract-yard scale harness: fulcrumRust PR #39 (2026-09-07).
Quiet grit greyscales (vendored 256² + sample_channels quiet height + grit::rough wear): fulcrumRust PR #58 (2026-09-07) — **landed**. Atelier read-only. Near source for Hypha #60 ring-mips.
Goegap day plate on extract ToD: fulcrumRust PR #40 (2026-09-07). **−/=** exposure **superseded #78**.
FoW title mark on the #11 shell: fulcrumRust PR #41 (2026-09-07).
Windows one-click release builder: fulcrumRust PR #42 (2026-09-07).
Windows builder stay-open + `build.log` tee: fulcrumRust PR #48 (2026-09-07).
Yard expand A/B (wider chunk radius first): clerk lock, Initial Visuals Group Chat (2026-09-07) — **shipped** Hypha #43.
Wider extract chunk radius (7×7 / 3 rings / 112 m / 12 544 m²): fulcrumRust PR #43 (2026-09-07).
Title + HOLD analysis-core polish: fulcrumRust PR #45 (2026-09-07).
Hypha Options Graphics/Gameplay/Controls guts: fulcrumRust PR #46 (2026-09-07).
Leftover feel-lab FX (brass / ricochet / impact variety / casing_draw_m): fulcrumRust PR #47 (2026-09-07). Ground snap **superseded #79** — heightfield / wall support; `first_hit` walls-only.
AXIS_LOCK + dizzy-play: fulcrumRust PR #51 (2026-09-07) — see `AXIS_LOCK.md`.
Hypha GPU post stack (AO/AA/CA/grain/DoF): fulcrumRust PR #55 (2026-09-07). **#66** colorless muzzle heat and **#68** ADS near sit on the same pass / same Options **DOF**.
Menus / settings ownership: Evan dump (2026-09-07) — Augury shell shipped #45; Hypha guts shipped #46; GPU post stack shipped #55; colorless heat shipped #66; ADS near DoF shipped #68.
Embodied feel pass (aim-offset × CE/FoW medium dials, Range Tech): fulcrumRust PR #57 (2026-09-07) — **landed**.
Evan peek feel (lean flip + deepen, CE hop + air hop, heat v77 look, H crossover, tracers-until-impact + FX `hit`): fulcrumRust PR #59 (2026-09-07) — **landed**. See `PEEK_FINDINGS.md` Closed by #59.
Hypha colorless muzzle heat (sample-only `heat_warp_uv`; lattice = post input only; no world-pipeline orange card): fulcrumRust PR #66 (2026-09-08) — **landed**. Range Tech keeps `barrel_energy` / heat dials / hold-J. Live defaults are the **#71 blend**. See `PEEK_FINDINGS.md` Closed by #66.
Range Tech Patch A muzzle (kit-tip spawn + `hip_honest_dir` + tip→impact streak clamp): fulcrumRust PR #67 (2026-09-08) — **landed**. Sits on **−/=** zero (#78; was **O** #33) + #76 SIM-only + #59 tracers-until-impact; does not replace them. Did not fight Hypha #66 / did not ship heat color. Lab-Rat terrain untouched. See `PEEK_FINDINGS.md` Closed by #67.
Range Tech ADS viewmodel DoF (ADS near + far on #55 stack; radius **0.0048** / taps **12** / near fade 0.90→2.20 m; breath mul **1.6 parked**): fulcrumRust PR #68 (2026-09-08) — **landed**. Same Options **DOF** / `project.json` `depth_of_field`. See `PEEK_FINDINGS.md` Closed by #68.
Range Tech heat dial blend toward aim-offset dump (was→now→stolen on the #66 post path; haze **0.07** / size **0.83** / scaleX **0.396** / lobe **0.698**; dump-dial cooking/~ → landed/X): fulcrumRust PR #71 (2026-09-08) — **landed**. #66 architecture stays; no orange card redraw. Glasses / live sheet still drive fields. See `PEEK_FINDINGS.md` Closed by #71 + `heat-card-dial-sheet.md`.
Range Tech SIM-only launch (one HoB + gravity / zero model; arcade aim-dir dead; leftover `hob_zero` ignored; **P** unused; #67 hip honesty + per-kit recoil/`yaw_walk` stay): fulcrumRust PR #76 (2026-09-09) — **landed**. Not a precomputed bake. Zero distance is **−/=** after #78 (was **O**). See `PEEK_FINDINGS.md` Closed by #76.
Range Tech hold-O extract / −/= zero / grounded slide: fulcrumRust PR #78 (2026-09-09) — **landed**. Hold-**O** raid intent (`Session::extract_checking`); **O** is **not** zero; **−/=** step 50/100/200; exposure keyboard unbound; midair Shift+Ctrl cannot float-slide. Augury extract popup / glasses / hatch chrome still **~**. #76 SIM-only + **P** unused + #67 hip honesty stay. See `PEEK_FINDINGS.md` Closed by #78.
Range Tech land sway softener + heightfield-grounded FX: fulcrumRust PR #79 (2026-09-09) — **landed**. Same #59 hop overlay — **not** a second land system. Punch **0.028** · duck **0.08** · shake **0.14** gate **13** + sway eye **0.014** / yaw **0.012** / roll **0.018** · decay **4.6**. Hop 12/30/1 **unchanged**. Brass / tracer ends / marks snap to extract `World::surface_height` / wall support; `first_hit` walls-only; no flat `floor_y` / pawn feet / phantom y=0. AXIS_LOCK sim barrel **+Z** unchanged. See `PEEK_FINDINGS.md` Closed by #79.
Texture LOD compress + atelier read-only: clerk lock, Initial Visuals (2026-09-07). Lab-Rat **#58 quiet grit greyscales landed** (vendored bake-downs); Hypha ring-mip texture LOD **shipped #60** (256/64/16; far softer; atelier read-only). Further roughness→stamp still open. Quiet influence — no franchise name-drop. See `PEEK_FINDINGS.md` Closed by #60 / `STAMP_FEEL_LOCK.md` / `TERRAIN_NORTHSTAR.md`.
LOD-tied grit / material mips (near 256² / mid 64² / far 16² BC4-style; far drops grain hashes; atelier read-only): fulcrumRust PR #60 (2026-09-07) — **landed**. Hypha. See `PEEK_FINDINGS.md` Closed by #60.
Near LOD raise (16/8/4 → 32/16/4; grid/radius stay #43; grit mips stay #60): fulcrumRust PR #61 (2026-09-08) — **landed**. Hypha. See `PEEK_FINDINGS.md` Closed by #61.
Authored SFX vs spatial split (Range Tech file slots / Augury Chamber spatial / Lab-Rat quiet stamps): Initial Visuals Group Chat (2026-09-07) — wiring shipped #54; day-one handmade vendor landed #62; shot propagation still later.
Authored SFX file slots: fulcrumRust PR #54 (2026-09-07) — wiring. Handmade atelier vendor: fulcrumRust PR #62 (2026-09-08) — **landed**. Small set, not a full CE / aim-offset pack dump.
First big-map (drop walls · ~8× extend · chunked Transvoxel · slope COL · local-player stream): Evan dump (2026-09-08) / Hypha **#81 landed**. Stamp pad still 7×7. Scatter/deform identity reserved — **no stamp bake**. NRM/GLOSS + listen-server peer pos parked. Lab-Rat grit-slope-PBR plugs **open** / Range Tech kits+FX draw + `dBXpg` still **open**; kit PBR stub + music playlist **landed #64** / Augury FoW brand+menu video **when cut ready**. Atelier PBR batch **in** (150 roughness + textures/PBR ~26 sets). See `TERRAIN_NORTHSTAR.md` + `PEEK_FINDINGS.md` Closed by #81.
Hypha 19×19 open extract + chunk stream + slope COL hooks: fulcrumRust PR #81 (2026-09-09) — **landed**. `73dc8fe4`. Underfoot **32/16/8/4**. Smoke `subdivs=32/16/8/4` `extract_m2=92416` `resident=` `stream_cold=` `pbr=`. Do **not** claim Lab-Rat stamp bake / NRM-GLOSS GPU / listen peer stream / Range heat. See `PEEK_FINDINGS.md` Closed by #81.
Atelier clean yell + SFX remix DNA + Music playlist beds: Evan dump (2026-09-08 ~00:00 ET) — plugs **open** (was read-only). Lab-Rat grit/slope/PBR · Range Tech `dBXpg` still **open**. Music playlist + kit metal/grit PBR stub **landed #64**. Remix first ±6% jitter **landed #64**; full remix minting still **open**. Augury FoW brand/menu video when cut ready · Hypha big-map continues on fulcrumRust. Do **not** claim Lab-Rat stamp bake / NRM-GLOSS / `dBXpg` / menu video shipped. 8× open extract **is** shipped #81. See `ATELIER_PORTFOLIO_STEAL.md` + `EXTRACTION_AUDIO_LOCK.md` + `PEEK_FINDINGS.md` Closed by #81.
Range Tech music playlist + kit metal/grit PBR stub + ±6% FX remix jitter: fulcrumRust PR #64 (2026-09-08) — **landed**. Five titled beds; stub PBR on MP9-Z / SR-25 / M24; store `dBXpg` still missing. See `EXTRACTION_AUDIO_LOCK.md` + `PEEK_FINDINGS.md` Closed by #64.
Holocron viewer gift (atelier `tools_for_ai_and_dev/Holocron_Visualizer.py` + `Analyze-Holocron.ps1`): Evan dump (2026-09-08) — tree nested-rectangle file-base viewer; cut monoliths (agent context; overwrite loss). Lab-Rat rust rewrite after slope/PBR. See `TOOLS.md`.
