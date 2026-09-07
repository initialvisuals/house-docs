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
