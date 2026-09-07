# fulcrumRust — last-pass lock (Evan dump 2026-09-06 evening)

Canonical feel / systems answers. Steal map + seats update from this sheet.

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
- **G** cycles MP9-Z → SR-25 → M24; **4 / 5 / 6** seat directly; **U** stays unaimed-hold cycle; **1 / 2 / 3** stay Lab-Rat curl
- Mag chrome stays diegetic on the seated kit — well count **is** mag size (MP9-Z **20** / SR-25 **20** / M24 **5**); Hold-R peek / tap-R reload / double-tap SWAP (fulcrumRust #32); leftover discarded; no HUD ammo counter
- **V** — cycle optic on the seated kit’s allow-list (SMG iron/holo/acog; SR-25 + scope; M24 iron/scope); ADS pose + FOV follow
- **N** — toggle .45 suppressor / can mounts; muzzle / flash / tracer spawn follow can tip when mounted
- FOV lock: hip **90** · iron ADS **60** · holo ADS **60** · acog ADS **25**
- Per-kit ballistics (`FeelSheet::fire`): MP9-Z AUTO ~1200 rpm / 300 m/s / kick 1.0 · SR-25 SEMI 0.14 s / 785 m/s / kick 1.15 · M24 bolt 0.65 s / 810 m/s / kick 1.75; HoB / muzzle / heat τ on the feel sheet (attachments do not invent new gameplay mags). Live zero + arcade↔sim via **O** / **P** (fulcrumRust #33)

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
- **Wider extract chunk radius** (Hypha #43): `TerrainHost` **5×5 → 7×7**; **3 Chebyshev rings / 112 m span / 12 544 m²** (was 2 rings / 80 m / 6 400 m²); extra **far** ring only. Near LOD 16/8/4 unchanged. Far-cold still `lod >= 2` + Locus `ACTIVATE_M` **24** / `SLEEP_M` **32**. Lab-Rat `STUB_GRID = 7`. Next expand A/B = **near LOD later**
- **Transvoxel extract host** (Hypha #16): crates.io `transvoxel` 2.0; distance LOD 16/8/4 + transition faces; `TerrainHost` implements `VoxelHost`; verts grade from Lab-Rat tint + wear; grimdark haze
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
- **Space** = single hop (fulcrumRust #51). No double-jump. Earlier "no jump" lock is superseded
- **[ / ]** = extract clock ±30 min (fulcrumRust #24); **K** = dawn/noon/dusk/night snap; **L** = live cycle
- **− / =** = exposure; **, / .** = cloud cover (extract only; hideout unfogged)
- **O** = cycle live zero presets 50 → 100 → 200 m (fulcrumRust #33); **P** = arcade ↔ sim launch (`hob_zero`)
- **X** = prone
- Canted hold + high/low ready from aim-offset
- **H** = shoulder swap (FoW habit); help remaps off H

## Axes + controller lock (fulcrumRust #12 + #51 AXIS_LOCK)
- Three spaces — do **not** unify. Camera/viewmodel local **−Z**; CE FBX **+X** (`rotY − π/2`); sim barrel / FX **+Z**. Lab-Rat stamps stay **+Y** (not this lock). Detail: `AXIS_LOCK.md` + fulcrumRust `docs/AXIS.md`
- World is **Y-up**; pawn `yaw = 0` looks **+Z** (hideout door / extract yard) — same *vector* as arcade sim barrel when the bore matches look; **not** camera-local −Z
- Evan dizzy-play (#51): **subtract** mouse X (invert horizontal); **invert A/D** including slide A/D bias. WASD otherwise camera-relative on that yaw. Q/E lean signs stay +lean = left (#25) — do not invert lean to "fix" FX
- SMG long axis is **look** / sim barrel +Z (not camera −Z, not CE +X); mag dots along the bore
- **Q / E** — peek left / right (wall-clamped; feel-lab +lean = left; #25 spring + viewmodel pad + yard covers)
- **Shift then Ctrl** — slide carry (sprint + crouch rising edge)
- **Hold Ctrl + mouse up/down** — analog eye height; does **not** pitch-look
- **Mouse wheel** — move speed (**not** height). Aim-offset uses wheel for crouch height; **Evan’s bind wins**
- Variable walk; **hold Shift** = sprint; power slide via the Shift→Ctrl rising edge above
- Hideout door **F** only (#51) — walk-into-door no longer auto-deploys. Must press F
- **Space** single hop (FoW/aim-offset, #51). No double-jump. Earlier "no jump" lock is superseded; day-one is single jump, not zero jump
- Glasses may show `SLIDE` / `SPD` / `HT` / stamp material / `LOCUS  STANDARD|INKED  <brain>` / `INK HOTSPOT` / `INSPECT` / `RELOAD` / `SWAP` / `BANDAGE` / `EMPTY` / `Z{n}  SIM|ARCADE` / `HEAT TUNE` / `HOST` / `JOIN` / `PEER` / `DOWNED` / `DEAD` / `STIM` / `NO STIM` / `RALLY` / `NEED STAB` / `STAB STUB  NO NET` / `HDRI` / `PROC` (ToD strip, fulcrumRust #40) labels only — never a second ammo/health HUD

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
2. **Invert A/D strafe** — including slide A/D bias. Q/E lean signs stay #25 (+lean = left)
3. **Hideout door** — keep **F** prompt; walk-into-door no longer auto-deploys. Must press F
4. **Jump** — **Space** single hop (FoW/aim-offset). No double-jump. Earlier "no jump" lock is superseded; day-one is single jump, not zero jump

## Heat / ADS
- Heat tell: **both** (diegetic barrel + glasses readout)
- ADS/hip: **both**, weighted by enemy/context
- Heat-tune dump (fulcrumRust #35): hold **J** climbs the same `barrel_energy` cook with recoil / camera punch skipped; glasses `HEAT TUNE` only — see Heat-tune dump section

## Visible shot feedback (fulcrumRust #12 + #19)
- LMB spends a round → muzzle flash + ballistic tracer + spark burst + hit mark (feel-lab language)
- Tracer speed / gravity / length from the SMG feel sheet
- FX draw-distance (hide-not-despawn, fulcrumRust #19 + #47): `muzzle_draw_m` **28** (clamp 8–80) · `spark_draw_m` **55** (clamp 8–200) · `casing_draw_m` **55** (clamp 8–200 via `live_casing`) · `decal_draw_m` **700** (clamp 50–2000) — walking back restores; they do not fill forever

## Props / audio / growth
- Destructible crates, boxes, cabinets with drawers from FoW
- Audio files from all repos + generated fills for gaps
- Living mycelium growth-enemy (gas/freeze/burn curl; sprint-grow) = Lab-Rat DNA hosted on extraction map

## Control DNA resolution
- **Locked** by fulcrumRust #12 + #51: FoW scheme + aim-offset feel with Evan bind overrides above. #51 dizzy-play is the live look / strafe / door / jump. No remaining soft overlap on lean / height / wheel.
- **/** = Goegap plate on/off (fulcrumRust #40). Does **not** steal **M** (map).
- **Embodied feel pass** (Evan dump 2026-09-07) is still **cooking** — Range Tech owns. Transpose aim-offset guns / attachments / controller into fulcrumRust (outside materials and range geometry); sweet medium vs CE / FoW OG controller + action audio cues. Do **not** claim this pass shipped. See section below.

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
- Feel-lab Settings **Audio** DNA — **not a DAW**; file-slot **wiring** shipped **partial** via #54 (placeholders; feel polish / real packs still cooking)
- Buses **Voice / Music / FX** into a **master**; gains clamp **0–2**, default **1.00 / 100%**; effective = `master * bus`
- Title + pause **Options** open the Augury shell (#45); Hypha Graphics/Gameplay/Controls panes live (#46); **Audio** still Range Tech #21 three-row Voice/Music/FX sheet; **A/D** or **←/→** nudge **0.05**; Esc Hypha pane / Audio → Options → title/pause; dials persist across Deploy
- Routes: **FX** = fire / dry / reload / cycle / pickup / putdown / Locus / swipe / wrap / ricochet / footstep / slide / jump / land; **Voice** = UI confirm; **Music** = hideout / extract ambient bed stub
- Hard check: SMG fire SFX respect FX (FX `0` silent). File preferred when present; missing → procedural. See `EXTRACTION_AUDIO_LOCK.md` + `engine/src/audio.rs`
- File-slot **wiring** shipped #54 (partial). Range Tech owns weapon/move SFX on this bus. Do **not** claim feel polish or CE packs as done. See Authored SFX file slots (#54).

## Day-one binaural / positional stereo on FX (fulcrumRust #27)
- Hypha + Augury CE FoW spatial DNA rides the **same** #21 Voice / Music / FX tree — **not a fourth bus**
- Listener follows the leaned camera basis (#25); HRTF-ish pan = equal-power ILD + Woodworth ITD + exponential distance
- World-posed FX: gunshots (muzzle), Locus slash (Standard + Inked), drops (putdown / pickup), ricochet ping at graze skip (#47); on-body FX: swipe / bandage `wrap` (#31); Voice centered; Music ambient bed
- Reverb zone stub: hideout (tight / drier) vs extract (industrial yard) — CE convolver DNA, not a send rack
- `Slot::Locus` / `Slot::Wrap` / `Slot::Ricochet` (#47) ride FX; file-slot **wiring** shipped #54; shot propagation still later. Augury (**Chamber**) **keeps** this spatial/reverb DNA; Range Tech owns file slots on the same bus (placeholders; feel polish still cooking)
- Smoke: `zone=EXTRACT spatial=1.00`; FX `0` still silences fire
- See `EXTRACTION_AUDIO_LOCK.md` + fulcrumRust `engine/src/audio.rs`

## Transvoxel extract host (fulcrumRust #16)
- Flat-world bake-once isosurface via crates.io **`transvoxel` 2.0** (Lengyel); **not** a globe
- Distance LOD: center subdiv **16** · ring-1 **8** · outer **4** + transition faces. Near LOD **unchanged** by #43
- Grid **7×7** / 3 Chebyshev rings / 112 m / 12 544 m² (Hypha #43; extra far ring only)
- `TerrainHost` consumes Lab-Rat `sample_channels` + `density_stamp_2d` / `WearStamp`; skin = `VoxelMaterial::tint` (no second paint story)
- Extract atmosphere: ashen/slate/brutalist vertex paint, void-spore stamp tints, cheap distance haze; hideout unfogged
- Parked: live LOD recook · tunnels · runtime carve. Next expand A/B = **near LOD later**. See `TERRAIN_NORTHSTAR.md` + fulcrumRust `docs/TERRAIN.md`


## Distance activation / far-guts cold (fulcrumRust #23)
- Shared Augury Locus dials: `ACTIVATE_M` **24** / `SLEEP_M` **32** (CE labyrinth DNA; `activation.rs`)
- Bake rings match Transvoxel LOD; far rings skip stamp-structure / wear consume; far plates stay out of extract bake (collide boxes land); brutalist compounds stay on horizon
- Growth + Locus GPU uploads skip past `ACTIVATE_M`; near yard unchanged; reuses #16 `TerrainHost`
- Smoke: `near_chunk=862` · `far_chunk=45` · `guts_warm=17` · `guts_cold=140` · `terrain_tris=3168`
- See `TERRAIN_NORTHSTAR.md` / `LOCUS_AI_LOCK.md` + fulcrumRust `docs/TERRAIN.md`

## Wider extract chunk radius (fulcrumRust #43)
- Hypha; `TerrainHost` grid **5×5 → 7×7** (smallest honest odd widen): one extra **far** ring only
- Playable extract: **3 Chebyshev rings / 112 m span / 12 544 m²** (was 2 rings / 80 m / 6 400 m²)
- Near LOD unchanged: center subdiv **16** · ring-1 **8** · outer **4**. Do **not** raise near LOD — **next expand A/B = near LOD later**
- Far-cold still maps `lod >= 2` → heightfield-only + shares Locus `ACTIVATE_M` **24** / `SLEEP_M` **32**
- Lab-Rat `ExtractStubHost` stays aligned (`STUB_GRID = 7`); near yard pad `yard_m2` ≈ **110** unchanged
- Smoke prints `rings=` / `extract_m2=` next to `near_chunk` / `far_chunk` / `yard_m2`:
  `near_chunk=858 far_chunk=39 guts_warm=75 guts_cold=216 rings=3 extract_m2=12544 yard_m2=110 locus_hp=24 terrain_tris=4034 lods=3`
  Far mean chunk ~**22×** cheaper than near; extra far ring added cold guts; yard pad + Locus stay
- Stay out of Atelier / HDRI / title mark. No new named scars
- See `TERRAIN_NORTHSTAR.md` / `STAMP_FEEL_LOCK.md` + fulcrumRust `docs/TERRAIN.md`

## Extract day/night clock + procedural sky (fulcrumRust #24)
- Feel-lab Settings **Lighting** DNA on extract only; hideout stays authored interior / unfogged (ToD does not leak inside)
- Default clock **06:21** (`TOD_DEFAULT` 6.35); sun path rise ~6:05 / set ~19:42; noon elev **56°**
- Dials: **[ / ]** ±30 min · **K** dawn→noon→dusk→night · **L** live cycle (`LIVE_HOURS_PER_SEC` 0.25) · **− / =** exposure (default mul **1.44**, step 0.08) · **, / .** clouds (step 0.10) · **/** Goegap plate on/off (#40; does not steal **M**)
- **No XOR sky** — one ToD sample drives ambient / key / fill / fog + procedural dome; dual color-aware lights. #40 plate rides the same sample.
- Grimdark: `EXTRACT_SKY_LUMA` **0.20** crushes noon to ashen (house aesthetic lock); Day HDRI shipped #40 (Goegap 4k; missing file stays procedural)
- Glasses on extract: `HH:MM  BAND  EXP x.xx  HDRI|PROC` labels only — never a second ammo HUD
- See `AESTHETIC_DIEGETIC_LOCK.md` + fulcrumRust `engine/src/sky.rs` / `engine/src/hdri.rs`

## Wall-clamped Q/E lean polish (fulcrumRust #25)
- Range Tech aim-offset / Engine #3 polish on existing #12 lean — no controller rebuild
- Sign lock: **Q** = left / +lean · **E** = right / −lean (do not invert)
- MoveDials: `lean_offset` **0.18** · `lean_roll` **0.12** · `lean_spring` **8.0** · `lean_skin` **0.08** · `lean_viewmodel` **0.16**
- Spring enter/exit, then hard ceiling after the spring so walking into a wall cannot push past clearance; release still springs out (no snap)
- Camera probe uses those MoveDials (no hardcoded 0.18 / 0.12)
- Viewmodel pad (`lean_viewmodel` **0.16**): E peeks stop the gun leading side at geometry (0.18 m camera travel is shorter than the capsule)
- Origin already inside a wall: `probe_clearance` reports 0 clearance
- Yard: two collide covers at extract yard mouth (`YARD_LEAN_COVERS`) on the Transvoxel pad; stay off plots / Locus / spawn
- Untouched: kits / drop / audio / heat / ToD / Locus / Transvoxel; slide / Ctrl+mouse height / wheel speed stay
- See fulcrumRust `engine/src/feel.rs` + `engine/src/player.rs`

## Mag reload DNA (fulcrumRust #32)
- Scheme: **Hold R** (~200 ms) = peek chrome only (does not start reload; release after a hold is not a tap). **Tap R** = short press, reload on RELEASE when `in_mag < capacity` AND reserves > 0 (NOT empty-only). **Double-tap R** (~300 ms from first tap) = emergency SWAP
- Dials (`engine/src/kit.rs` + `session.rs`): `RELOAD_PEEK_HOLD_SEC` **0.20** · `RELOAD_DOUBLE_TAP_SEC` **0.30** · `RELOAD_BASIC_SEC` **1.10** (basic mag-out pose stub) · `RELOAD_EMERGENCY_SEC` **0.46** (faster slap, same 1-reserve cost)
- Leftover rounds discarded on both paths (reserve is whole mags, not pocketed partials). Emergency’s higher-cost feel is dumping a half-stick
- Glasses labels only: `RELOAD` (basic) / `SWAP` (emergency) — never a numeric ammo HUD
- Intact / do not steal: knife, bandage, lean, inspect, ToD, kits
- Viewmodel: `reload_t` mag-out dip; inspect overlay still wins over reload dip

## Live HoB zero / launch dials (fulcrumRust #33)
- Per-kit rpm / recoil / HoB sheet was already authored (#22); this PR makes zero distance + arcade↔sim **live**
- Constants: `ZERO_PRESETS_M` **[50.0, 100.0, 200.0]** m; default `zero_dist_m` **100**; default `hob_zero` **true** (SIM)
- **O** — cycle live zero presets 50 → 100 → 200 → 50 (HoB solve). Shared across MP9-Z / SR-25 / M24 so G-swap does not hide the solve (`FeelSheet::cycle_zero`)
- **P** — arcade (aim-dir launch) ↔ sim (height-over-bore + ballistic zero) via `hob_zero` (`FeelSheet::toggle_hob_zero`). Shared launch mode across kits
- Honesty: changing zero preset changes muzzle **launch dir** only (not muzzle position); arcade vs sim launch dirs differ; sim aims up to meet sight zero; arcade launches along aim
- Toast: `ZERO  {n} M` / `LAUNCH  ARCADE` / `LAUNCH  SIM` (age **1.2s**, `Slot::Cycle`)
- Glasses status strip (labels only, never a second ammo HUD): `Z{zero_dist_m:.0}  SIM|ARCADE` e.g. `Z100  SIM`
- Intact / do not steal: **[ / ]** stay ToD clock; **− / =** stay exposure; **9 / 0** left free; does not steal **T** / **C** / **R** / **Q** / **E** / **Z** / **B** / **V** / **N** / **U** / **`** / **F** / **X** / **H** / **1** / **2** / **3** / **G** / **Mouse4**; tip→impact tracers / muzzle / sparks stay; reload / knife / bandage / lean / inspect / ToD stay seated

## Heat-tune dump (fulcrumRust #35)
- Bind: hold **J** = heat-tune dump. **I** is no longer free — I is Augury stim (#37).
- Feel: sustained AUTO on the seated kit (`FeelState::try_heat_tune` / `fire_shot(..., heat_tune: true)`); uses kit `auto_interval_sec` while tuning (ignores SEMI hold gate)
- Recoil impulse + camera punch skipped; leftover LMB punch stomped while J is down (`recoil_punch` / `recoil_rot` / `cam_recoil_p` / `cam_recoil_y` zeroed) so the gun stays still
- Same cook path: `FeelState.barrel_energy` still climbs so tip cards + lobe go live for live dialing (no second heat cook)
- Ammo dial cheat: mag **still spends** while holding; **release refills** the seated mag via `DayOneKit::refill_mag` (tops stick to `smg_mag_size`, does **not** spend a reserve)
- Glasses: `HEAT TUNE` label only (amber-ish overlay) — never a second ammo HUD; must not count mag rounds
- Intact / do not steal: ToD **[ ]**/K/L/−/=/,/. · lean Q/E · inspect ` · reload R · knife Mouse4/C · bandage T · O/P zero/launch · I stim · Y host · O/P/T/C/R/Q/E/Z/B/V/N/U/`/F/X/H/G/I/Y/1/2/3/Mouse4
- Tests that define the lock: `heat_tune_climbs_energy_without_camera_punch`, `heat_tune_does_not_fight_tod_lean_inspect_reload_knife_bandage_zero`, `heat_tune_glasses_do_not_count_mag`, `j_is_heat_tune_hold_without_stealing_binds`

## Listen-server + invite stub (fulcrumRust #34)
- Thin `std::net` UDP hub in `engine/src/net.rs` (MyceliumEngine had no portable net crate)
- Title **HOST** / **JOIN**; in-game **Y** while alive arms listen-server; `--host` / `--join fulcrum://ip:port` (also bare `host:port` and `fw://`); env `FULCRUM_JOIN`
- Default port **7777** (`FULCRUM_PORT` override). LAN iface if OS has one, else loopback
- Glasses labels only: `HOST  ip:port`, then `JOIN` / `PEER` after HELLO/WELCOME — never a second ammo HUD
- Honesty: handshake / presence only — both machines still sim locally; **no** world replication / shoot/Locus/terrain/audio rewrite / PvEvP sim
- Solo **Deploy** unchanged (`net=off` on smoke)
- Does **not** steal **I** stim (#37), **O**/**P** HoB zero (#33), hold-**J** heat-tune (#35), or T/C/R/Q/E/Z/B/V/N/U/`/F/M/1/2/3/Mouse4
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
- Intact / do not steal: **T** stays bandage · knife Mouse4/C · lean Q/E · inspect ` · reload R · kits G/4/5/6 · curl 1/2/3 · ToD **[ ]**/K/L/−/=/,/. · O/P zero/launch · hold-J heat-tune · listen-server title HOST/JOIN + `--host` / `--join` stay. **I** is stim (does not steal Y host). **Y** is host alive-only (does not steal I stim).
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

Stay **on the extract yard** as a scale/perf harness for the #38 stamp/paint substrate. Not a bigger world map. No Standard / Monk one-off scars. HDRI stays Range Tech.

| Dial | Lock |
|------|------|
| **Pad** | `growth::yard_bounds` ≈ **110 m²** (baseline before harness ≈ **54 m²**); flatten disk tracks it so plots stay playable |
| **`apply_yard_harness`** | Anonymous SDF lattice + larger paint brushes + 2D-mask convert of the three existing plots through `StampField::layers` — not a fourth named plot |
| **Near / far** | Near yard stays warm (`bake_guts_warm`). Far guts stay cold (Hypha #23). Harness primitives are near-warm only; smoke fails if a layer center is far. `guts_cold` stayed **140** |
| **Smoke** | `growth=544 curled=580 stamps=100 structs=55 wears=117 content=173 layers=43 prims=216 yard_m2=110` · `guts_warm=75 guts_cold=140 near_chunk=858 far_chunk=45 terrain_tris=3182`. Baseline: `layers=0 prims≈content yard_m2≈54 guts_warm=32`. Far cheapness holds (`far_chunk < near_chunk`). Growth GPU boxes still under 620 |

See `STAMP_FEEL_LOCK.md` / `TERRAIN_NORTHSTAR.md` + fulcrumRust `docs/CHANNELS.md`.

## Goegap HDRI on extract ToD (fulcrumRust #40)

Range Tech day plate on the #24 extract clock. Hideout stays authored interior / unfogged.

- Asset: Poly Haven **Goegap** 4k Radiance RGBE (~22MB, CC0 / Greg Zaal). `engine/build.rs` fetches **one** file at build time into `engine/assets/hdris/` (not a submodule, not the atelier texture dump). Atelier raw is fallback. Missing file → procedural dome (honest).
- Feel: Radiance RGBE decode → equirect sky/env (`engine/src/hdri.rs`). Same ToD sample still drives ambient / key / fill / fog / dome — **no XOR sky**. Plate yaw tracks the clock sun. Night fades the day plate back to the procedural dome (stars stay).
- Grimdark: `EXTRACT_SKY_LUMA` **0.20** keeps noon ashen
- **/** toggles Goegap plate on/off — does **not** steal **M** (map). Existing ToD dials unchanged: **[ / ]** · **K** · **L** · **− / =** · **, / .**
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

See `AESTHETIC_DIEGETIC_LOCK.md`. Hypha window / post stubs / tab guts shipped #46. GPU post shaders still open.

## Menus / settings ownership (Evan dump 2026-09-07; Augury shell #45; Hypha guts #46)

Augury shell polish shipped #45 (title + HOLD chrome + Options list shell + logo seat). Hypha Graphics/Gameplay/Controls guts + window mode + post stubs + persist shipped #46. **Do not claim GPU post passes (SSAO/FXAA/CA/grain/DoF shaders) done** — toggles persist as live-read stubs and no-op safely. Logo/title mark #41 still stands.

| Seat | Owns |
|------|------|
| **Augury** | Title + HOLD analysis-core chrome (#45). Options list shell. Logo/title mark #41. Layout/colors/buttons remain Augury |
| **Hypha** | Graphics / Gameplay / Controls tab guts + window mode + post stubs + persist — **shipped #46**. Borderless default; windowed 1280×720; exclusive (borderless fallback). Post AO/AA/CA(+strength)/grain/DoF persist and no-op until GPU passes — **not** packed into Range Tech ToD / Goegap / HDRI uniforms. Steal from CE/Mycelium. **No atelier push** |
| **Range Tech** | Audio mixer stays #21 Voice/Music/FX (untouched by #46) |
| **Input** | FoW OG input manager also in scope (steal into fulcrumRust) — still cooking |

Esc Hypha pane / Audio → Options → title/pause. Still no second ammo HUD. See `AESTHETIC_DIEGETIC_LOCK.md`. Existing #12–#46 sections stay.

## Hypha Options guts (fulcrumRust #46)

Filled the disabled `HYPHA` stub tabs on Augury’s #45 Options list. Not a second settings overlay. Title / HOLD / Options chrome + FoW logo seat stay Augury.

| Dial | Lock |
|------|------|
| **Window** | Live via winit. **Borderless** = default launch. **Windowed** = decorated 1280×720. **Exclusive** = exclusive video mode when OS/GPU expose one, else borderless fallback. Also `--windowed` / `FULCRUM_WINDOW` (`borderless` / `windowed` / `exclusive`) |
| **Post stubs** | AO, AA, CA (+ strength default **0.35**, step **0.05**, range **0–1**), film grain, DoF persist and are live-read stubs until GPU passes — **no-op safely**. Must **not** pack into Range Tech ToD / Goegap / HDRI uniforms. GPU shaders still open |
| **Graphics hint** | `POST STUB UNTIL GPU · WINDOW LIVE · A/D NUDGE` |
| **Gameplay** | Glasses labels toggle + crosshair toggle (real — drop quads when off). Hint: `SHOOT FEEL STAYS · ENTER TOGGLE` |
| **Controls** | Look scale on feel-lab sens: `LOOK_MUL` default **1.0**, min **0.25**, max **2.0**, step **0.05**; Invert Y toggle. Binds stay README. Hint: `LOOK SITS ON FEEL-LAB SENS · BINDS IN README` |
| **Audio** | Untouched — Range Tech #21 Voice/Music/FX mixer |
| **Persist** | `project.json` in cwd, or `FULCRUM_SETTINGS=/path/to.json` |
| **Esc** | Hypha pane / Audio → Options → title or HOLD (same stack as #45) |

See `AESTHETIC_DIEGETIC_LOCK.md`. No second ammo HUD. No atelier push.

## Leftover feel-lab FX (fulcrumRust #47)

Range Tech leftover feel-lab stack on the same #12/#19 `TracerField`. Tip already had tracers + muzzle + spark/mark + FX draw-distance — those stay. Not a rebuild.

- **FxDrawDials** (updated #19 row): `muzzle_draw_m` **28** (clamp 8–80) · `spark_draw_m` **55** (clamp 8–200) · `casing_draw_m` **55** NEW (clamp 8–200 via `live_casing`) — hide-not-despawn XZ lane for brass + spent slugs · `decal_draw_m` **700** (clamp 50–2000)
- **Brass eject** — live fire from seated kit `ejectionPort`: `MP9Z_EJECT` **(0.036, −0.014, 0.018)** · `SR25_EJECT` **(0.038, 0.008, 0.018)** · `M24_EJECT` **(0.03, 0.018, 0.055)**. Camera-right toss; `CASING_GRAVITY` **12**; bounce then sleep; `CASING_FADE` **6** s; `MAX_CASINGS` **48**. Hide-not-despawn via `casing_draw_m` **55**. Hold-**J** heat-tune dump (#35) skips brass so the lattice stays still
- **Ricochet / spent slug** — feel-lab `trySpawnSpentSlugBounce` — **NOT** a bounce table. `SLUG_CHANCE` **1/16**; `SLUG_GRAZE_MAX` |n·vhat| ≤ **0.52** (dead-on still punches). Reflect incoming vel, keep 8–18% (`SLUG_KEEP_MIN`/`MAX` **0.08–0.18**); `SLUG_SPEED_MIN`/`MAX` **2.2–16**. Spent-slug visual `MAX_SLUGS` **24**; scuff mark instead of punch plug. Optional FX bus `Slot::Ricochet` ping at skip point
- **Richer impact geo** — punch vs scuff + `IMPACT_HOLE_VARIANTS` **10** + rim chips + stuck-slug plug (brass SMG / steel DMR+bolt). Rides existing spark/mark path — not a rebuild
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

## Embodied feel pass (Range Tech — cooking, not shipped)

Evan dump 2026-09-07. **Not shipped** — do not claim the feel pass as done. **Range Tech** owns it.

| Lock | Detail |
|------|--------|
| **Steal** | Aim-offset **looks/feels correct** for guns, attachments, controller — **transpose** that work into fulcrumRust |
| **Out of scope** | Materials and range geometry |
| **Sweet medium** | Concrete Echo / FoW OG also has a great controller + **action audio cues**. Find a medium between aim-offset and CE/FoW for **embodied feel** |
| **Binds stay** | #12 Evan-bind lock (Q/E lean, Ctrl+mouse height, wheel speed) + #51 dizzy-play (invert look/strafe, F-only door, Space hop) is not this pass |

See `AESTHETIC_DIEGETIC_LOCK.md`. Steal from this shelf + steal map — not chat scroll.

## Authored SFX vs spatial split (wiring shipped partial #54)

Initial Visuals Group Chat 2026-09-07. File-slot **wiring** shipped **partial** via #54 — do **not** claim feel polish or real CE / aim-offset packs as done. #21 FX bus is **live**. Authored audio (rustles / rattles / slides) comes over that bus (placeholders today).

| Seat | Owns |
|------|------|
| **Range Tech** | Weapon / move SFX **file slots** off CE / FoW packs into the live #21 Voice / Music / FX buses. Not a fourth bus. Wiring + placeholders shipped #54. |
| **Augury (Chamber)** | Keeps spatial / reverb DNA (#27). Does not take the file slots. |
| **Lab-Rat** | Stamps stay **quiet on audio** |

#21 Audio tab + #27 spatial path stay. Shot propagation still later. Feel polish / real packs still cooking. See `AESTHETIC_DIEGETIC_LOCK.md` + `EXTRACTION_AUDIO_LOCK.md`.

## Authored SFX file slots (fulcrumRust #54)

Range Tech feel-lab `sfx.slots[id]` on the **same** #21 FX bus — **not** a second mixer. Status **PARTIAL**: wiring + placeholder WAVs shipped; real CE / aim-offset packs + feel polish still next. Shot propagation still later. `.ogg` names reserved; decode WAV-only this beat.

| Dial | Lock |
|------|------|
| **Load** | `mixer.play(Slot::*)` loads `assets/sfx/<id>.wav` (or `FULCRUM_SFX` override dir) |
| **Fallback** | Missing / bad file → existing procedural tone |
| **FX gain** | Options Audio FX dial scales the buffer; FX `0` still silent |
| **File-backed slots** | fire · dry · reload_release / insert / seat · pickup · putdown · swipe · wrap · footstep · slide · jump · land |
| **Reserved (synth until file)** | cycle · locus · ricochet |
| **Placeholders** | ~22.05 kHz 16-bit mono WAVs in `assets/sfx/` — not the real rustle packs |
| **Move cues live** | walk rustle (`footstep`) · sprint-crouch slide · Space hop + land |
| **Weapon cues** | already on FX; now prefer the file |
| **Ownership** | Range Tech file slots / Augury Chamber spatial+reverb / Lab-Rat quiet stamps |
| **Left alone** | AXIS_LOCK · Locus brains · terrain/stamps · Options Graphics |

See `EXTRACTION_AUDIO_LOCK.md` + fulcrumRust `assets/sfx/README.md`.

## Still soft / seat-owned timing
- Exact day-one world: single medium instance vs hub+tunnel+extract (Hypha chooses if Evan didn’t hard-pick)
- Next yard expand A/B = **near LOD later** (wider chunk radius shipped Hypha #43: 7×7 / 3 rings / 112 m / 12 544 m²; near subdiv stays 16/8/4)
- Menus / settings: Augury title+HOLD chrome + Options shell shipped #45; Hypha Graphics/Gameplay/Controls + window + persist shipped #46; GPU post passes (SSAO/FXAA/CA/grain/DoF actual shaders) still cooking — **not done**
- One-click Windows `build.bat` **landed as Hypha #42 + Range Tech #48** (always pause + `build.log` tee); quality/flag options still cooking / open (Lab-Rat mirror for pycelium later — no dials invented here)
- Embodied feel pass: Range Tech transposes aim-offset guns / attachments / controller into fulcrumRust (outside materials / range geometry); sweet medium vs CE / FoW OG controller + action audio cues (Evan dump 2026-09-07) — **not done**
- Growth PoCs after window exists
- Shot propagation on the spatial FX path (binaural day-one landed #27; file-slot wiring landed #54)
- Authored SFX vs spatial split: Range Tech file-slot **wiring** shipped #54 (placeholders); feel polish / real CE packs / shot propagation still open. Augury (Chamber) keeps spatial/reverb DNA; Lab-Rat stamps stay quiet on audio (Initial Visuals Group Chat 2026-09-07)

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
Extract day/night clock + procedural sky: fulcrumRust PR #24 (2026-09-07).
Wall-clamped Q/E lean polish: fulcrumRust PR #25 (2026-09-07).
Locus Inked on yard: fulcrumRust PR #26 (2026-09-07).
Day-one binaural / positional stereo on FX: fulcrumRust PR #27 (2026-09-07).
Hold-` inspect pose: fulcrumRust PR #28 (2026-09-07).
Lab-Rat Inked void-spore hotspot: fulcrumRust PR #30 (2026-09-07).
Bandage use stub: fulcrumRust PR #31 (2026-09-07).
Mag reload DNA: fulcrumRust PR #32 (2026-09-07).
Live HoB zero / arcade↔sim launch: fulcrumRust PR #33 (2026-09-07).
Listen-server + invite stub: fulcrumRust PR #34 (2026-09-07).
Heat-tune dump (hold-J): fulcrumRust PR #35 (2026-09-07).
Down / death stub: fulcrumRust PR #36 (2026-09-07).
Augury I-stim / Y-host bind: fulcrumRust PR #37 (2026-09-07).
Shape-agnostic stamp/paint substrate: fulcrumRust PR #38 (2026-09-07).
Extract-yard scale harness: fulcrumRust PR #39 (2026-09-07).
Goegap day plate on extract ToD: fulcrumRust PR #40 (2026-09-07).
FoW title mark on the #11 shell: fulcrumRust PR #41 (2026-09-07).
Windows one-click release builder: fulcrumRust PR #42 (2026-09-07).
Windows builder stay-open + `build.log` tee: fulcrumRust PR #48 (2026-09-07).
Yard expand A/B (wider chunk radius first): clerk lock, Initial Visuals Group Chat (2026-09-07) — **shipped** Hypha #43.
Wider extract chunk radius (7×7 / 3 rings / 112 m / 12 544 m²): fulcrumRust PR #43 (2026-09-07).
Title + HOLD analysis-core polish: fulcrumRust PR #45 (2026-09-07).
Hypha Options Graphics/Gameplay/Controls guts: fulcrumRust PR #46 (2026-09-07).
Leftover feel-lab FX (brass / ricochet / impact variety / casing_draw_m): fulcrumRust PR #47 (2026-09-07).
AXIS_LOCK + dizzy-play: fulcrumRust PR #51 (2026-09-07) — see `AXIS_LOCK.md`.
Menus / settings ownership: Evan dump (2026-09-07) — Augury shell shipped #45; Hypha guts shipped #46; GPU post shaders still open.
Embodied feel pass (aim-offset × CE/FoW, Range Tech): Evan dump (2026-09-07) — cooking, not shipped.
Authored SFX vs spatial split (Range Tech file slots / Augury Chamber spatial / Lab-Rat quiet stamps): Initial Visuals Group Chat (2026-09-07) — wiring shipped partial #54; feel polish / real packs still cooking.
Authored SFX file slots: fulcrumRust PR #54 (2026-09-07) — wiring + placeholders; feel polish still next.
