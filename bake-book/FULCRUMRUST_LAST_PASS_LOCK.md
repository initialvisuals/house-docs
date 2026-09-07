# fulcrumRust — last-pass lock (Evan dump 2026-09-06 evening)

Canonical feel / systems answers. Steal map + seats update from this sheet.

## Day-one kit
- **SMG** basic 20-round mag
- **4 mags** + one in the gun
- **Knife**
- **Bandage**
- Find other weapons on enemies / in boxes / loose in world

## MP9-Z kit + attachments (fulcrumRust #14)
- Day-one viewmodel is the **feel-lab MP9-Z silhouette** (procedural boxes), not the brick SMG
- Mag chrome stays diegetic on the **MP9-Z receiver rail** (20 LEDs + stick plaque); Hold-R peek unchanged
- **V** — cycle optic iron / holo / acog (ADS pose + FOV follow)
- **N** — toggle .45 suppressor; muzzle / flash / tracer spawn move to can tip
- FOV lock: hip **90** · iron ADS **60** · holo ADS **60** · acog ADS **25**
- Ballistics / HoB / recoil / 20-rd + 4 mags stay on the feel sheet (attachments do not invent new gameplay mags)

## First playable flow
1. **Loading screens** cover bake/hitch — player never sees hitching except true CPU/geo overload
2. Small **interior hideout** (drawers, tables, lights, pickups, door) — geometry mostly authored
3. World **finalized before** hideout spawn (rigidize-on-start)
4. Door → transition → **Forever Winter–style extraction test map** (PoC playground for loop + controller feel)

## World bake (Hypha)
- Prefer proving **hub + extract linked by tunnel** early if it doesn’t block the window; otherwise one medium Forever Winter instance is fine day-one
- Near-spawn **mycelium growth PoCs**: 2D stamp, 3D organic form, ground creeper (gas/freeze/burn curl later)
- **Smart material stamps** (Lab-Rat #15): dirt/sand/rock/concrete/organic on 8 m cells + sit-on-surface structures; Hypha owns real `VoxelHost` + meshed stamped cells

## Downed / revive
- Teammate **stabilize**, then heal with **items** (no magic heal)
- Equipment required — or take off the downed body
- **Self-revive** via revive stim on person
- Slash a downed **Locus Standard** (or similar) → **critical revive rally**

## Inventory / HUD
- MyceliumEngine **slot system** (stub OK)
- **Tab** = inventory / status (includes health)
- Health + armour **bottom-left**
- Ammo peek: hold **Numpad 0** or hold **R**; double-tap **R** = emergency quick mag; press **R** = normal reload
- Hold **`~`** = inspect weapon
- **B** = fire mode
- **V** = cycle optic (iron / holo / acog)
- **N** = toggle .45 suppressor
- **M** = map
- **Z** = drop bag
- **X** = prone
- Canted hold + high/low ready from aim-offset
- **H** = shoulder swap (FoW habit); help remaps off H

## Axes + controller lock (fulcrumRust #12)
- World is **Y-up**; `yaw = 0` looks **+Z** (hideout door / extract yard)
- Mouse-right **increases** yaw; WASD is camera-relative on that yaw
- SMG long axis is **look** (not +X); mag dots along the bore
- **Q / E** — peek left / right (wall-clamped; feel-lab +lean = left)
- **Shift then Ctrl** — slide carry (sprint + crouch rising edge)
- **Hold Ctrl + mouse up/down** — analog eye height; does **not** pitch-look
- **Mouse wheel** — move speed (**not** height). Aim-offset uses wheel for crouch height; **Evan’s bind wins**
- Variable walk; **hold Shift** = sprint; power slide via the Shift→Ctrl rising edge above
- Double jump later as equipment/skill/power — not day-one default
- Glasses may show `SLIDE` / `SPD` / `HT` / stamp material labels only — never a second ammo HUD

## Heat / ADS
- Heat tell: **both** (diegetic barrel + glasses readout)
- ADS/hip: **both**, weighted by enemy/context

## Visible shot feedback (fulcrumRust #12)
- LMB spends a round → muzzle flash + ballistic tracer + spark burst + hit mark (feel-lab language)
- Tracer speed / gravity / length from the SMG feel sheet

## Props / audio / growth
- Destructible crates, boxes, cabinets with drawers from FoW
- Audio files from all repos + generated fills for gaps
- Living mycelium growth-enemy (gas/freeze/burn curl; sprint-grow) = Lab-Rat DNA hosted on extraction map

## Control DNA resolution
- **Locked** by fulcrumRust #12: FoW scheme + aim-offset feel with Evan bind overrides above. No remaining soft overlap on lean / height / wheel.

## Still soft / seat-owned timing
- Exact day-one world: single medium instance vs hub+tunnel+extract (Hypha chooses if Evan didn’t hard-pick)
- Growth PoCs after window exists

Source chat: Initial Visuals Group Chat, 2026-09-06. Controller axis lock: fulcrumRust PR #12 (2026-09-07).
MP9-Z kit: fulcrumRust PR #14 (2026-09-07).
Smart stamps: fulcrumRust PR #15 (2026-09-07).
