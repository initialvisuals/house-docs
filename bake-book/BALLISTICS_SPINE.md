# Ballistics spine (arc A + model stash)

House contract for leftover vs visual honesty (2026-09-10). **Holding / locked intent — not shipped.** Steal from this sheet, not chat. Do **not** invent powder numbers, sample dt, or drag coeffs. No code. Clerk owns this sheet.

## Problem (tip)

PVP leftover hit is **hitscan** (straight eye ray · **500 m** · look dir · flat `SMG_PELLET`). Visual `KIND_SHOT` tracers are **ballistic** (look dir + kit gravity, **no HoB/zero loft on the wire**).

Sniper range: HP tags on the look-line while the victim sees the pellet drop short.

## Locked direction

- **Not** hitscan as the primary feel (cheap / shitty).
- **A** — Physical bullets do colliding. HOST one shared launch solve (seed + loft + gravity samples) drives leftover **and** peer streak. Client predicts visual only; HOST leftover is truth.
- Fairness for later MOA / bloom / spread: same shared HOST solve — **no** separate hitscan cheat path once powder locks.
- Milsim north star: Tarkov / Arma / DayZ fly projectiles (arc sampled in short steps; hit where the sim is).

Default cook is **A**.

## Model stash (internal leftover)

Do **not** throw away the current hitscan model. Stash / restore in AIM TUNE / debugger:

| Model | Meaning |
|-------|---------|
| `hitscan` | Current tip — leftover eye ray |
| `ballistic_A` | Arc-sample leftover (locked cook) |

Quick revert. Extra debug is OK on the internal build; strip later.

## Parked

- **Powder A/B/C** (rifle falloff) until Evan picks. Do not invent powder ids or numbers.
- **Invented sample dt / drag coeffs.** Do not park fake step or Cd on this sheet.
- **Options B/C** (loft-straight / arcade straighten) — interim only if yelled. Default cook stays **A**.

## Seat map (ownership — no implementation yet)

| Seat | Owns |
|------|------|
| **Beabim** | `KIND_SHOT` / leftover wire · HOST shared solve · fairness seed |
| **Range Tech** | `muzzle_and_launch` loft/zero · tracer DNA · model stash UI in AIM TUNE / debugger |
| **Hypha / Lab-Rat / Augury** | Off |
| **Clerk** | This sheet |

## Explicitly parked

- Hitscan as primary leftover feel.
- Deleting the current hitscan model. Stash it; do not erase the revert path.
- Powder A/B/C + invented sample dt / drag until Evan locks.
- Options B/C as the default cook.
- No code on this cook. Seats steal intent from here when a cook is greenlit.

See `PEEK_FINDINGS.md` Holding / locked intent — ballistics spine. Overnight cooks steal from this sheet.
