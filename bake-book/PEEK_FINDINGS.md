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

## Controller lock (Evan bind wins)

Shipped in fulcrumRust #12. Overrides soft aim-offset wheel-height where they disagreed:

- **Q / E** — peek left / right
- **Shift then Ctrl** — slide carry (sprint + crouch rising edge)
- **Hold Ctrl + mouse up/down** — analog eye height (does **not** pitch-look)
- **Mouse wheel** — move speed (**not** height; aim-offset uses wheel for crouch height — Evan’s bind wins)
- No double-jump day-one

## Holding steady

- Hypha: load gate / session path
- Augury: menus / load gate unless hitch
- Lab-Rat: yard silhouette fidelity landed (#13); next wet-lab beats stay on STEAL_MAP (bake stamps / experiment log)

Steal from this shelf + steal map. Not chat scroll.
