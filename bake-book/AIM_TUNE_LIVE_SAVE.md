# AIM TUNE LIVE persist — house pointer

Range Tech. **Landed** fulcrumRust [#167](https://github.com/initialvisuals/fulcrumRust/pull/167) (2026-09-10, merge `aef44571`) + two-exe persist [#169](https://github.com/initialvisuals/fulcrumRust/pull/169) (2026-09-10, merge `ea342444`). Per-kit pull follow-up on **#103**. Schema keys unchanged. Two-instance path + flush is **no longer a soft follow**.

**Canonical dial sheet:** fulcrumRust [`docs/AIM_TUNE_LIVE_SAVE.md`](https://github.com/initialvisuals/fulcrumRust/blob/main/docs/AIM_TUNE_LIVE_SAVE.md) (merge tip `ea342444`). Steal from that sheet — do **not** duplicate or invent numbers here. House seat: [`HOLD_POSE_SPINE.md`](HOLD_POSE_SPINE.md) already-shipped siblings + [`FULCRUMRUST_LAST_PASS_LOCK.md`](FULCRUMRUST_LAST_PASS_LOCK.md).

CREDITS + STEAL_MAP already claimed in-PR — house shelf only.

## Landed lock (stolen, not invented)

Hideout and raid share one Hypha `project.json` (`FULCRUM_SETTINGS` if set, else cwd). Not a second raid file. Path is resolved **absolute**. Per-kit keys were already `aim_tune.example_smg` / `example_rifle` / `example_sniper` (MP9-Z / SR-25 / M24). The #167 hole was load / pull, not the key names: a new session seeds `FeelSheet` from authored defaults, and `pull_aim` used to replace the whole persist blob — one LIVE flush rewrote the other kits back to authored.

| Dial | Value | Notes |
|------|-------|-------|
| Schema | #103 | `aim_live` + `aim_tune.*`. No new keys. |
| Path | same file | Hideout and raid. `FULCRUM_SETTINGS` if set, else cwd `project.json`. Resolved **absolute**. |
| Kit keys | `example_smg` / `example_rifle` / `example_sniper` | MP9-Z / SR-25 / M24. |
| Pose / attach | unchanged | `hip` … `inspect` + `attachments.optic` / `canted` / `can`. |
| Pull | per-kit | Authored (untouched) kits on the live sheet keep persisted peeks. |
| Flush | absorb undirty | LIVE / Options write re-reads disk kits this instance has not changed since load. |
| Apply | Deploy / restart / `apply_aim_settings` | Snaps `hold_blend` so the seated gun matches the dial. |
| LIVE off | stub | Still does not write `aim_tune`. Leftover stash is not gated. |

End PX ±0.50 (#159), Options `look_mul` (#163), and Beabim leftover stash stay. PreferredHand / powder / Options hip Chest/Low are other seats.

## Northstar (Evan 2026-09-10)

AIM TUNE LIVE = **authoring only**. Bake peeks into kit DNA for all players when banks feel right — **not** a per-player profile.

Do **not** invent a player-profile persist path. Do **not** claim the bake-into-kit-DNA cook shipped. #103 / #167 / #169 stay the atelier LIVE persist (absolute path · per-kit pull · flush absorb · `project.json.lock`).

## Two-instance (HOST + peer) — landed #169

Lab-Rat / Evan: two exes can show different AIM TUNE peeks. Two holes, not a net pose — both **landed #169** (Range CLEAN). Not a soft follow.

1. **Path split.** Default persist is **cwd** `project.json` (absolute-resolved). `build-and-run.bat` cds to the repo, so two bats share one file. Double-click `target\release\app.exe` (cwd = that folder) writes a **different** file. Same-machine HOST/peer that must share peeks: set **`FULCRUM_SETTINGS`** to one absolute path on both, or launch both from the same folder. Each exe may keep its own file if you want split Range dials.
2. **Flush race.** AIM TUNE is local Range, not KIND_POSE. A LIVE / Options / debugger save used to last-writer the whole `aim_tune` blob. After apply, the peer sheet is last-loaded peeks (not authored), so `pull_aim` alone still rewrote HOST's kits. Flush now keeps disk peeks for kits this instance has not End-nudged since load (`aim_epoch`). Same-kit last writer wins. `project.json.lock` serializes the read-merge-write. Instances do **not** hot-reload the other window — relaunch or a later undirty flush picks the file up.

See `PEEK_FINDINGS.md` Closed by #167 + Closed by #169 + `FULCRUMRUST_LAST_PASS_LOCK.md`.
