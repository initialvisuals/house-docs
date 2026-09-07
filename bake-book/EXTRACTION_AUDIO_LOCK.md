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

## Voice / Music / FX buses (fulcrumRust #21 + #54)
Range Tech feel-lab Settings **Audio** DNA — **not a DAW**. File-slot wiring shipped **partial** via #54 (`sfx.slots[id]`): `mixer.play(Slot::*)` loads `assets/sfx/<id>.wav` (or `FULCRUM_SFX` override dir) onto the **same** #21 FX bus. Options Audio FX dial scales the buffer. Missing / bad file → existing procedural fallback. Placeholders only — real CE / aim-offset packs + feel polish still next. `.ogg` names reserved; decode WAV-only this beat.

Range Tech owns weapon / move file slots on this bus. Augury (**Chamber**) keeps spatial / reverb (#27). Not a second mixer.

### Gains
- Three buses into a **master**: **Voice** / **Music** / **FX**
- Clamp **0–2** (`VOL_MIN` / `VOL_MAX`); default **1.00 / 100%** (`VOL_DEFAULT`)
- Effective play gain = `master * bus` (feel-lab contract)
- Keyboard / list nudge **0.05** (`VOL_STEP`) — A/D or ←/→; Esc back
- Dials live on title + pause **Options** three-row sheet; persist across Deploy

### Day-one routes
| Bus | Owns |
|-----|------|
| **FX** | weapon fire / dry / reload / cycle / pickup / putdown / Locus / swipe / wrap / ricochet / footstep / slide / jump / land |
| **Voice** | UI confirm (title / pause / Options) |
| **Music** | hideout / extract ambient bed stub |

### Hard checks
- Fire SFX (SMG `playFire`) **respect the FX bus** — FX `0` is silent; half FX is quieter
- File preferred when present; missing / bad file → procedural fallback
- Sample rate stub **22050** for procedural cues (placeholder WAVs also ~22.05 kHz 16-bit mono)
- Code: fulcrumRust `engine/src/audio.rs` + Options sheet in `engine/src/menu.rs` + `assets/sfx/`

## Day-one binaural / positional stereo on FX (fulcrumRust #27)
Hypha + Augury CE FoW spatial DNA on the **same** Voice / Music / FX tree — **not a fourth bus / second mixer**.

### Spatial render path
- Listener pose follows the leaned camera basis (#25) via CE `updateListener` DNA
- HRTF-ish pan on FX: equal-power **ILD** + Woodworth **ITD** + exponential distance (CE `PannerNode`)
- World-posed FX emitters: **gunshots** (muzzle), **Locus slash** (Standard + Inked), **drops** (putdown / pickup)
- On-body FX: knife **swipe** · bandage **`wrap`** (fulcrumRust #31 — cloth rustle stub, not a heal chime)
- Voice stays centered; Music stays the ambient bed
- `Slot::Locus` / `Slot::Swipe` / `Slot::Wrap` ride FX

### Reverb zone stub
- **Hideout** — tight / drier
- **Extract** — industrial yard
- CE convolver DNA, not a send rack

### Hard checks
- Smoke: `audio=100% zone=EXTRACT spatial=1.00` after Standard + Inked dumps + Z/F; FX `0` still silences fire
- File-slot **wiring** shipped #54 (placeholders; feel polish / real packs still cooking); shot propagation still later
- Code: fulcrumRust `engine/src/audio.rs` + session pose hooks in `engine/src/session.rs`

Source: https://github.com/initialvisuals/fulcrumRust/blob/main/docs/STEAL_MAP.md
PRs: https://github.com/initialvisuals/fulcrumRust/pull/21 · https://github.com/initialvisuals/fulcrumRust/pull/27 · https://github.com/initialvisuals/fulcrumRust/pull/31 · https://github.com/initialvisuals/fulcrumRust/pull/54
