# Ballistics spine (arc A + model stash)

House contract for leftover vs visual honesty (2026-09-10). **Beabim leftover/net half SHIPPED** via fulcrumRust [#160](https://github.com/initialvisuals/fulcrumRust/pull/160) (`e0803dc1967418fef7bdd7e04a31c2a3b2f681ed`). Range Tech loft DNA + AIM TUNE stash chrome still **open** (tip [#161](https://github.com/initialvisuals/fulcrumRust/pull/161) CONFLICTING — do **not** claim shipped; do **not** invent a merge). Steal from this sheet + fulcrumRust [`docs/BALLISTICS_A_DIAL_SHEET.md`](https://github.com/initialvisuals/fulcrumRust/blob/main/docs/BALLISTICS_A_DIAL_SHEET.md) — not chat. Do **not** invent powder numbers, sample dt, or drag coeffs. Clerk owns this sheet.

## Problem (tip — leftover/net closed by #160)

Was: PVP leftover hit is **hitscan** (straight eye ray · **500 m** · look dir · flat `SMG_PELLET`) while visual `KIND_SHOT` tracers are **ballistic** (look dir + kit gravity, **no HoB/zero loft on the wire**). Sniper range: HP tags on the look-line while the victim sees the pellet drop short.

**#160** closed the leftover/net half: HOST leftover + `KIND_SHOT.dir` share the launch loft. Range tracer visual DNA is still open.

## Locked direction

- **Not** hitscan as the primary feel (cheap / shitty).
- **A** — Physical bullets do colliding. HOST one shared launch solve (seed + loft + gravity samples) drives leftover **and** peer streak. Client predicts visual only; HOST leftover is truth.
- Fairness for later MOA / bloom / spread: same shared HOST solve — **no** separate hitscan cheat path once powder locks.
- Milsim north star: Tarkov / Arma / DayZ fly projectiles (arc sampled in short steps; hit where the sim is).

Default cook is **A**.

## Model stash (internal leftover)

Do **not** throw away the hitscan model. Stash / restore:

| Model | Meaning | Status |
|-------|---------|--------|
| `ballistic_A` | Arc-sample leftover (locked cook). Default | **Live #160** |
| `hitscan` | Straight look-line eye ray | Stashed — `FULCRUM_LEFTOVER` / `project.json` `leftover_hit` / `Session::set_leftover_hit_model` |

Quick revert. Extra debug is OK on the internal build; strip later. Range wires AIM TUNE / debugger chrome later — leftover/net switch already ships.

## What shipped (#160 · Beabim leftover/net)

Canonical numbers live on fulcrumRust [`docs/BALLISTICS_A_DIAL_SHEET.md`](https://github.com/initialvisuals/fulcrumRust/blob/main/docs/BALLISTICS_A_DIAL_SHEET.md). Overnight cooks steal from that sheet — not every `.rs`.

| Dial | Lock |
|------|------|
| Default leftover | **`ballistic_A`** — arc samples + `feel::step_ballistic` (same `vel.y -= g·dt` as peer streak) |
| Hitscan stash | `FULCRUM_LEFTOVER` / `project.json` `leftover_hit` / `Session::set_leftover_hit_model` → `hitscan` restores look-line eye ray |
| `KIND_SHOT.dir` | HOST launch loft from `muzzle_and_launch` / `hip_honest` / MOA — **not** look-dir. No KIND bump. Unused byte **3** stays |
| Leftover origin | eye **1.60 m**, centered (#147 held). Re-solve loft from leftover eye via `solve_ballistic_launch` + kit zero — do **not** reuse 1P muzzle HoB pitch (flies over crown) |
| Max / pellet | **500 m** / flat `SMG_PELLET` **14** held |
| Arc chord | `HEAD_HALF_H + HURT_SKIN` (**0.17 m**) — not a parked powder dt |
| Shared helpers | `feel::solve_ballistic_launch` · `feel::step_ballistic` · `biped::leftover_launch_dir` |

CREDITS Beabim Shipped line + STEAL_MAP Net/ballistics claim already planted in #160. House shelf only.

## Still open

- **Range Tech** — consume #160 loft DNA + AIM TUNE leftover stash chrome. Tip **#161** CONFLICTING. Do **not** claim shipped.
- **Powder A/B/C** (rifle falloff) until Evan picks.
- Tracer visual DNA. Hypha STREAM. Augury. Hub protect. `KIND_LOOT_WORLD`. Locus yard **80 m**.

## Parked

- **Powder A/B/C** (rifle falloff) until Evan picks. Do not invent powder ids or numbers.
- **Invented sample dt / drag coeffs.** Do not park fake step or Cd on this sheet. Arc chord **0.17 m** is leftover hurt metres, not a powder dt.
- **Options B/C** (loft-straight / arcade straighten) — interim only if yelled. Default cook stays **A**.

## Seat map

| Seat | Owns |
|------|------|
| **Beabim** | `KIND_SHOT` / leftover wire · HOST shared solve · fairness seed — **shipped #160** |
| **Range Tech** | `muzzle_and_launch` loft/zero · tracer DNA · model stash UI in AIM TUNE / debugger — **still open** (consume #160 loft DNA; tip #161 CONFLICTING) |
| **Hypha / Lab-Rat / Augury** | Off |
| **Clerk** | This sheet |

See `PEEK_FINDINGS.md` Closed by #160 + Holding / locked intent — Range #161 / powder parked. Overnight cooks steal from this sheet + fulcrumRust `docs/BALLISTICS_A_DIAL_SHEET.md`.
