# Hideout hub (FoW pre-raid friend hub)

House contract for the FoW pre-raid friend hub (2026-09-10). Soft leftover **landed #153** (Beabim). Floorplan metres stay **pending Evan tip** — do **not** invent hall / wing / ceiling numbers. Steal from this sheet + fulcrumRust [`docs/MP_WEAPON_DIAL_SHEET.md`](https://github.com/initialvisuals/fulcrumRust/blob/main/docs/MP_WEAPON_DIAL_SHEET.md), not chat. Clerk owns this sheet.

## Intent

Pre-raid hub to fuck around with friends before extract. Stash + loadouts. Port more from aim-offset into a long range hall **once metres land**.

## Soft rules (LOCKED · Beabim leftover landed #153)

Hideout is a friend sandbox. Raid stays raid.

| Lock | Detail | Status |
|------|--------|--------|
| **No-loot downs** | In hideout: downs / hits do **not** drop a kit or seat a `KIND_BODY` bag. **Z** throw stays a player drop | **Landed #153** |
| **15 s protect** | `HUB_PROTECT_SECS` **15**. Both peers arm on a hub soft-down (`KIND_PVP` unused bytes **22–23** `protect_ms`). Leftover ray + Hit apply gated until the window ends. Not `PVP_RESPAWN_SECS` **1.20** | **Landed #153** |
| **Hideout PeerBodies** | Starting-room remotes draw the same `locus_solids` + held-clone path as extract (was extract-only upload) | **Landed #153** |
| **Crisp flash** | Hit feedback: crisp red → black flash → fade back to normal. **Not** Slain. **Not** death climb | **Pending** — Augury/Range chrome. #153 leftover is net/session gate + timer + no-loot only |
| **Raid is normal** | Outside hideout / in world raid: loot, death, #143 wound feel, Beabim PvP. Extract keeps leftover ray + **1.20 s** leftover. No hub protect | **Landed #153** (raid skip) |
| **Raid shader** | Raid may still use damage shader feedback (wound feel). That is not this hideout crisp | Held — Range #143 |

Do **not** invent a second protect window. **15 s** is the locked protect. Do **not** fold hideout crisp into Augury Death / Slain. Do **not** fold it into Range #143 raid wound feel — reuse that DNA for the flash envelope only (chrome still pending).

## Volume (PENDING metres — do not invent)

Evan wants a larger / taller / wider compound — **T or H with an L**, plus a long shooting-range hall.

Lab-Rat cooks Concrete grade + face UVs (**#144** shelf) **when Evan tips**:

- hall length
- wing width
- ceiling height

Until that tip: **no hall / wing / ceiling numbers on this sheet.** Shape words only. Do **not** invent floorplan metres.

## Visible bipeds + held kit (landed #153)

Show **PeerBody** bipeds in the hideout starting room. **Beabim** leftover **landed #153** — same boxes + authored `kit_boxes` clone on `GUN_HOLD_LOCAL` `(0.18, 1.05, 0.28)` via `presented_local` so lean/peek rides the torso. House lock **1P viewmodel ≠ 3P biped gun** held. Hands / gear / Mixamo still open.

## Seat map

| Seat | Owns |
|------|------|
| **Lab-Rat** | T·H·L + range hall boxes **when metres tip**; Concrete / UV off the **#144** shelf |
| **Range Tech** | aim-offset range toys **after metres**; crisp flash dial sheet (reuse #143 wound DNA, **not** Slain); Music already on hideout (**#64**) |
| **Beabim** | Hideout PeerBody + no-loot + **15 s** protect + held 3P kit clone **landed #153**. Dial `docs/MP_WEAPON_DIAL_SHEET.md` |
| **Augury** | Crisp overlay chrome **if needed** (still pending); soft-rim desert stays **separate** (**#151**) |
| **Hypha** | landmark ride / STREAM cover the bigger floor **when volume lands**; stay **off** volume sculpt. PeerBody box table already #131 / #145 |
| **Clerk** | This sheet |

## Explicitly parked

- **Crisp red→black flash chrome** — Augury/Range. Not the #153 leftover.
- **Powder A/B/C** until Evan locks. Do not invent powder ids or dials.
- **Invented floorplan metres.** Hall length / wing width / ceiling height wait on Evan tip.
- **Bigger progression / faction systems.** Not this hub sheet.
- Hands / gear / Mixamo / PreferredHand 3P / End tuner sockets on the remote kit.

See `PEEK_FINDINGS.md` Closed by #153 + Holding / locked intent — hideout hub (metres pending). Overnight cooks steal from this sheet + fulcrumRust `docs/MP_WEAPON_DIAL_SHEET.md`.
