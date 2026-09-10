# AIM TUNE LIVE persist — house pointer

Range Tech. **Landed** fulcrumRust [#167](https://github.com/initialvisuals/fulcrumRust/pull/167) (2026-09-10, merge `aef44571`). Per-kit pull follow-up on **#103**. Schema keys unchanged.

**Canonical dial sheet:** fulcrumRust [`docs/AIM_TUNE_LIVE_SAVE.md`](https://github.com/initialvisuals/fulcrumRust/blob/main/docs/AIM_TUNE_LIVE_SAVE.md) (merge tip `aef44571`). Steal from that sheet — do **not** duplicate or invent numbers here. House seat: [`HOLD_POSE_SPINE.md`](HOLD_POSE_SPINE.md) already-shipped siblings + [`FULCRUMRUST_LAST_PASS_LOCK.md`](FULCRUMRUST_LAST_PASS_LOCK.md).

CREDITS + STEAL_MAP already claimed in-PR — house shelf only.

## Landed lock (stolen, not invented)

Hideout and raid share one Hypha `project.json` (`FULCRUM_SETTINGS` or cwd). Not a second raid file. Per-kit keys were already `aim_tune.example_smg` / `example_rifle` / `example_sniper` (MP9-Z / SR-25 / M24). The hole was load / pull, not the key names: a new session seeds `FeelSheet` from authored defaults, and `pull_aim` used to replace the whole persist blob — one LIVE flush rewrote the other kits back to authored.

| Dial | Value | Notes |
|------|-------|-------|
| Schema | #103 | `aim_live` + `aim_tune.*`. No new keys. |
| Path | same file | Hideout and raid. `FULCRUM_SETTINGS` or cwd `project.json`. |
| Kit keys | `example_smg` / `example_rifle` / `example_sniper` | MP9-Z / SR-25 / M24. |
| Pose / attach | unchanged | `hip` … `inspect` + `attachments.optic` / `canted` / `can`. |
| Pull | per-kit | Authored (untouched) kits on the live sheet keep persisted peeks. |
| Apply | Deploy / restart / `apply_aim_settings` | Snaps `hold_blend` so the seated gun matches the dial. |
| LIVE off | stub | Still does not write `aim_tune`. Leftover stash is not gated. |

End PX ±0.50 (#159), Options `look_mul` (#163), and Beabim leftover stash stay. PreferredHand / powder / Options hip Chest/Low are other seats.

## Soft follow (not in the dial sheet)

Two-instance shared `project.json` / flush race — **soft follow**. Not in the #167 dial sheet. Do **not** invent a race fix. Shelf the landed tip only.

See `PEEK_FINDINGS.md` Closed by #167 + `FULCRUMRUST_LAST_PASS_LOCK.md`.
