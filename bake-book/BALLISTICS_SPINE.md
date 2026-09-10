# Ballistics spine (arc A + model stash)

House contract for leftover vs visual honesty (2026-09-10). Tip order **#160 → #161** complete. **Beabim leftover/net half SHIPPED** via fulcrumRust [#160](https://github.com/initialvisuals/fulcrumRust/pull/160) (`e0803dc1967418fef7bdd7e04a31c2a3b2f681ed`). **Range Tech loft DNA + AIM TUNE leftover stash SHIPPED** via fulcrumRust [#161](https://github.com/initialvisuals/fulcrumRust/pull/161) (merge `4f47875376683f922c99adc7d7eb45a0736dc8a1`). Steal from this sheet + fulcrumRust [`docs/BALLISTICS_A_DIAL_SHEET.md`](https://github.com/initialvisuals/fulcrumRust/blob/main/docs/BALLISTICS_A_DIAL_SHEET.md) — not chat. Do **not** invent powder numbers, sample dt, or drag coeffs. Clerk owns this sheet.

## Problem (tip — leftover/net closed by #160 · Range closed by #161)

Was: PVP leftover hit is **hitscan** (straight eye ray · **500 m** · look dir · flat `SMG_PELLET`) while visual `KIND_SHOT` tracers are **ballistic** (look dir + kit gravity, **no HoB/zero loft on the wire**). Sniper range: HP tags on the look-line while the victim sees the pellet drop short.

**#160** closed the leftover/net half: HOST leftover + `KIND_SHOT.dir` share the launch loft. **#161** closed the Range half: 1P loft DNA + tracer streak + AIM TUNE **MODEL** write the same `leftover_hit` stash.

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
| `hitscan` | Straight look-line eye ray | Stashed — `FULCRUM_LEFTOVER` / `project.json` `leftover_hit` / `Session::set_leftover_hit_model` / Range AIM TUNE **MODEL** (**#161**) |

Quick revert. Extra debug is OK on the internal build; strip later. Range AIM TUNE **MODEL** + TELE/PERF `LEFTOVER` read/write this same key — no second `ballistic_model` persist.

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

## What shipped (#161 · Range loft DNA + AIM TUNE stash)

Range Tech. Consumes Beabim leftover/net (**#160**). Does **not** fork KIND_SHOT / leftover collide / HOST shared solve. Steal the Range section on fulcrumRust [`docs/BALLISTICS_A_DIAL_SHEET.md`](https://github.com/initialvisuals/fulcrumRust/blob/main/docs/BALLISTICS_A_DIAL_SHEET.md) — not chat.

| Piece | Path | Notes |
|-------|------|-------|
| 1P loft DNA | `muzzle_and_launch` + `hip_honest_dir` + MOA | Same body Beabim publishes as `KIND_SHOT.dir`. No `NetShot.loft`, no 48-byte KIND, no unused-byte model flag. |
| Tracer streak | `TracerField` + `feel::step_ballistic` | Local + peer streaks follow the lofted `ShotEvent` (dir / speed / gravity). Hitscan leftover stash does **not** flatten the streak. |
| AIM TUNE MODEL | End · INS cycle WEAPON → ATTACH → MODEL | Writes Beabim `leftover_hit` (`hitscan` / `ballistic_A`). Persist that key. No `ballistic_model`. |
| Debugger | TELE / PERF `LEFTOVER` line | Reads the same enum. Not a new Augury tab. |

CREDITS Range Shipped line + STEAL_MAP ballistics / AIM TUNE claim already planted in #161. House shelf only.

## Still open

- **Powder A/B/C** (rifle falloff) until Evan picks.
- Hypha STREAM. Augury chrome. Hub protect. `KIND_LOOT_WORLD`. Locus yard **80 m**.

## Parked

- **Powder A/B/C** (rifle falloff) until Evan picks. Do not invent powder ids or numbers.
- **Invented sample dt / drag coeffs.** Do not park fake step or Cd on this sheet. Arc chord **0.17 m** is leftover hurt metres, not a powder dt.
- **Options B/C** (loft-straight / arcade straighten) — interim only if yelled. Default cook stays **A**.

## Seat map

| Seat | Owns |
|------|------|
| **Beabim** | `KIND_SHOT` / leftover wire · HOST shared solve · fairness seed — **shipped #160** |
| **Range Tech** | `muzzle_and_launch` loft/zero · tracer DNA · model stash UI in AIM TUNE / debugger — **shipped #161** (consume #160 loft DNA) |
| **Hypha / Lab-Rat / Augury** | Off |
| **Clerk** | This sheet |

See `PEEK_FINDINGS.md` Closed by #160 + Closed by #161 + Holding / locked intent — powder parked. Overnight cooks steal from this sheet + fulcrumRust `docs/BALLISTICS_A_DIAL_SHEET.md`.
