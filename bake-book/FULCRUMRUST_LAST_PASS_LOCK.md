# fulcrumRust — last-pass lock (Evan dump 2026-09-06 evening)

Canonical feel / systems answers. Steal map + seats update from this sheet.

## Day-one kit
- **SMG** basic 20-round mag
- **4 mags** + one in the gun
- **Knife**
- **Bandage**
- Find other weapons on enemies / in boxes / loose in world

## First playable flow
1. **Loading screens** cover bake/hitch — player never sees hitching except true CPU/geo overload
2. Small **interior hideout** (drawers, tables, lights, pickups, door) — geometry mostly authored
3. World **finalized before** hideout spawn (rigidize-on-start)
4. Door → transition → **Forever Winter–style extraction test map** (PoC playground for loop + controller feel)

## World bake (Hypha)
- Prefer proving **hub + extract linked by tunnel** early if it doesn’t block the window; otherwise one medium Forever Winter instance is fine day-one
- Near-spawn **mycelium growth PoCs**: 2D stamp, 3D organic form, ground creeper (gas/freeze/burn curl later)

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
- **M** = map
- **Z** = drop bag
- **X** = prone
- **Ctrl** + **mouse wheel** = variable crouch height (aim-offset)
- Leans: prefer **aim-offset** lean; CE wall-camera DNA where needed
- Canted hold + high/low ready from aim-offset
- **H** = shoulder swap (FoW habit); help remaps off H
- Variable walk; **hold Shift** = sprint; power slide
- Double jump later as equipment/skill/power — not day-one default

## Heat / ADS
- Heat tell: **both** (diegetic barrel + glasses readout)
- ADS/hip: **both**, weighted by enemy/context

## Props / audio / growth
- Destructible crates, boxes, cabinets with drawers from FoW
- Audio files from all repos + generated fills for gaps
- Living mycelium growth-enemy (gas/freeze/burn curl; sprint-grow) = Lab-Rat DNA hosted on extraction map

## Control DNA resolution
- FoW control scheme + aim-offset feel; agents resolve overlap

## Still soft / seat-owned timing
- Exact day-one world: single medium instance vs hub+tunnel+extract (Hypha chooses if Evan didn’t hard-pick)
- Growth PoCs after window exists

Source chat: Initial Visuals Group Chat, 2026-09-06.
