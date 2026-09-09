# Extraction / audio locks (fulcrumRust)

Parked from Evan + seat locks (2026-09-07).

## Stash / corpse
- **Sacred stash** — builds live in the stash, not on the corpse
- **Corpse reclaim fight** — may need to kill previous dead self for bag loot (not hard-lose, not hub-forgiving)

## Extract
- Timed surface hazard (spores / O₂ kill)
- Toggle extracts (open/close; one or many)

## Audio day-one
- **Binaural** from the start
- FX bus / gunshots get spatial first
- Shot propagation later

## Voice / Music / FX buses (fulcrumRust #21 + #54 + #62 + #64 + #82 + #134)
Range Tech feel-lab Settings **Audio** DNA — **not a DAW**. File-slot **wiring** shipped #54 (`sfx.slots[id]`): `mixer.play(Slot::*)` loads `assets/sfx/<id>.wav` (or `FULCRUM_SFX` override dir) onto the **same** #21 FX bus. Day-one handmade atelier vendor **landed #62** (one 22.05 kHz 16-bit mono WAV per FILE_SLOTS id in `assets/sfx/`). Optional single-file `hit.wav` **superseded #134** — Hit is `Slot::HIT_POOL` (`distant_small_medium_impact_bullet` / `…B` / `…C` under `assets/sfx/distant_impacts/`); retired leftover `assets/sfx/hit.wav` is not loaded. Options Audio FX dial scales the buffer. Missing / bad file → existing procedural fallback (Hit: remaining pool, then grit). Small handmade set — not a full CE / aim-offset pack dump. Shot propagation still later. `.ogg` names reserved; decode WAV-only this beat. Music playlist beds **landed #64** on the same #21 Music bus. Options **DEVICE** cycle **landed #82** — same mixer stereo render → thin cpal voice; **not** a second mix tree. World FX mono fold **landed #134** — `DecodeFold::WorldMono` on `Bus::Fx` (L+R → mono on decode); Music **Keep stereo**; Voice keep / dual-mono.

Range Tech owns Voice / Music / FX mixer + authored file-slot SFX (#21 + #54 + #62) + playlist beds / remix jitter (#64) + Options **DEVICE** (#82) + Hit pool + decode fold (#134). Augury (**Chamber**) owns spatial path (#27 HRTF/ITD) + authored CE reverb volumes + FX wet send (#56). Not a second mixer. Hypha keeps Options Graphics post.

### Gains
- Three buses into a **master**: **Voice** / **Music** / **FX**
- Clamp **0–2** (`VOL_MIN` / `VOL_MAX`); default **1.00 / 100%** (`VOL_DEFAULT`)
- Effective play gain = `master * bus` (feel-lab contract)
- Keyboard / list nudge **0.05** (`VOL_STEP`) — A/D or ←/→; Esc back
- Dials live on title + pause **Options** Audio sheet; persist across Deploy
- **DEVICE** row **landed #82** (cursor 0, above Voice / Music / FX). Cycle A/D or arrows; Enter / click also steps (same DNA as Graphics **WINDOW**). Default **SYSTEM DEFAULT** via cpal `default_output_device()` (Windows / OS default). Persist `output_device` in `project.json` (empty / `default` / `system` = OS default). Named pin kept if the device is missing; playback falls back to OS default. Bus dials unchanged (0–2 / 100%)
- Route: same #21 mixer stereo render → thin cpal voice (oneshots + Music-bed loop). UI tick plays on the newly selected device. Code: `engine/src/audio_out.rs` (Stream on window thread — not Sync)

### Day-one routes
| Bus | Owns |
|-----|------|
| **FX** | weapon fire / dry / reload / cycle / pickup / putdown / Locus / swipe / wrap / ricochet / footstep / slide / jump / land / **hit** (pool #134) |
| **Voice** | UI confirm (title / pause / Options) |
| **Music** | hideout / extract playlist **landed #64** — CONCRETE_ECHO · Terraform · The Memory of The Augury · guttertrash · A Shattered Remnant From A Collapsed Distant Star; Options Music dial still scales; missing → two-tone stub |

### Hard checks
- Fire SFX (SMG `playFire`) **respect the FX bus** — FX `0` is silent; half FX is quieter
- File preferred when present; missing / bad file → procedural fallback (Hit: remaining `HIT_POOL`, then grit)
- Sample rate stub **22050** for procedural cues (atelier vendor WAVs also ~22.05 kHz 16-bit mono)
- Code: fulcrumRust `engine/src/audio.rs` + `engine/src/audio_out.rs` + Options sheet in `engine/src/menu.rs` + `assets/sfx/`

## Day-one binaural / positional stereo on FX (fulcrumRust #27)
Hypha + Augury CE FoW spatial DNA on the **same** Voice / Music / FX tree — **not a fourth bus / second mixer**.

### Spatial render path
- Listener pose follows the leaned camera basis (#25) via CE `updateListener` DNA
- HRTF-ish pan on FX: equal-power **ILD** + Woodworth **ITD** + exponential distance (CE `PannerNode`)
- World-posed FX emitters: **gunshots** (muzzle), **Locus slash** (Standard + Inked), **drops** (putdown / pickup)
- On-body FX: knife **swipe** · bandage **`wrap`** (fulcrumRust #31 — cloth rustle stub, not a heal chime)
- Voice stays centered; Music stays the ambient bed
- `Slot::Locus` / `Slot::Swipe` / `Slot::Wrap` ride FX

### Authored CE reverb volumes (fulcrumRust #56)
Upgrades the #27 phase-only two-zone stub (hideout dry vs extract industrial) to authored AABB proxy volumes on extract. Listener XZ inside → that zone; first hit wins; miss → outdoor fallback.

| Volume | Glasses | Feel |
|--------|---------|------|
| Hideout interior | **DRY** | tight / drier |
| Extract yard pad | **YARD** | industrial yard |
| Open extract | **OUT** | wetter / longer tail |

- **FX wet send only.** Voice / Music stay dry dual-mono. Same #21 bus tree — not a second mixer. #54 file slots still render through that FX wet send.
- Listener follows the camera (#27 `updateListener`). **No extra bind.** Walk off the yard pad to hear outdoor.
- Glasses peek `DRY` / `YARD` / `OUT` — labels only, never a second ammo HUD.
- CE convolver DNA, not a send rack. **The Augury** owns volumes + FX wet send. Range Tech keeps mixer + file slots + DEVICE + fold. Hypha keeps Options Graphics post.

### Hard checks
- Smoke: `audio=100% zone=EXTRACT spatial=1.00 sfx=file/13` after Standard + Inked dumps + Z/F; FX `0` still silences fire
- File-slot **wiring** shipped #54; day-one handmade vendor **landed #62** (atelier WAVs in `assets/sfx/`; missing / bad file → procedural); DEVICE cycle **landed #82**; dirt Hit pool + WorldMono fold **landed #134**; shot propagation still later
- Code: fulcrumRust `engine/src/audio.rs` + session pose hooks in `engine/src/session.rs`

## SFX remix DNA (Evan 2026-09-08 ~00:00 ET)

Range Tech. Creative reuse **OK** — pitch / speed / effects to mint new one-shots from existing packs. Indie underground vibe. Do **not** overuse the same stem. #54 wiring + #62 handmade vendor stay the live FILE_SLOTS fill. Remix is how more one-shots get minted without a full pack dump. Same #21 FX bus — not a second mixer. Voice / Music stay dry dual-mono (#56).

First application **landed #64** — fire / foot / reload ±6% pitch/speed jitter on the live #62 vendor. **#134** also jitters **hit**. Mixer / Options FX / Augury spatial stay honest (FX `0` still silent). Remix DNA policy stays; full remix pack minting still **open**.

## Music beds (landed #64)

Shuffle of five atelier `music/` titles on hideout / extract beds: **CONCRETE_ECHO** · **Terraform** · **The Memory of The Augury** · **guttertrash** · **A Shattered Remnant From A Collapsed Distant Star**. Small 8 s / 22.05 kHz / 16-bit mono loops in fulcrumRust `assets/music/` (not the 5–11 MB MP3s). Each hideout / extract start advances the shuffle. Options Audio Music dial still scales the bed. Missing file → old two-tone stub. Same #21 Voice / Music / FX tree — not a fourth bus. Music stays dry dual-mono (#56). **#134** Music **Keep stereo** (`DecodeFold::Keep`) — 2D bed. Voice / FX / Augury spatial+reverb untouched. Overrides: `FULCRUM_MUSIC` / `FULCRUM_ATELIER` read-only. Playback rides the #82 DEVICE pick (thin cpal voice).

## Options Audio DEVICE (landed #82)

Range Tech. Explicit host-output pick on the Options **Audio** pane. Audio still follows the OS default unless cycled. Same #21 mixer — **not** a second mix tree. Augury keeps spatial/reverb. Hypha keeps Options Graphics post.

| Dial | Lock |
|------|------|
| **Row** | `DEVICE` (cursor 0, above Voice / Music / FX) |
| **Default** | **SYSTEM DEFAULT** — cpal `default_output_device()` (Windows / OS default) |
| **Cycle** | A/D or arrows; Enter / click also steps (same DNA as Graphics **WINDOW**) |
| **Persist** | `output_device` in `project.json` (empty / `default` / `system` = OS default) |
| **Missing pick** | Keep the pin; playback falls back to OS default |
| **Route** | Same #21 mixer stereo render → thin cpal voice (oneshots + Music-bed loop) |
| **Hear it** | UI tick plays on the newly selected device |
| **Code** | `engine/src/audio_out.rs` — cpal enumerate + stream. Stream on window thread (`Stream` is not Sync) |

Source: https://github.com/initialvisuals/fulcrumRust/blob/main/docs/STEAL_MAP.md
PRs: https://github.com/initialvisuals/fulcrumRust/pull/21 · https://github.com/initialvisuals/fulcrumRust/pull/27 · https://github.com/initialvisuals/fulcrumRust/pull/31 · https://github.com/initialvisuals/fulcrumRust/pull/54 · https://github.com/initialvisuals/fulcrumRust/pull/56 · https://github.com/initialvisuals/fulcrumRust/pull/62 · https://github.com/initialvisuals/fulcrumRust/pull/64 · https://github.com/initialvisuals/fulcrumRust/pull/82 · https://github.com/initialvisuals/fulcrumRust/pull/134
