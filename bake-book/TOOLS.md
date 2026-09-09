# Tools (Evan gift 2026-09-08)

Atelier `tools_for_ai_and_dev/`. Not a fulcrumRust ship. Steal the idea — do not clone atelier into extract.

## Holocron

- **`Holocron_Visualizer.py`** — tree nested-rectangle viewer (Plotly treemap) over a file base. Line-count heat. Prints top monoliths. Writes `holocron_py.html`.
- **`Analyze-Holocron.ps1`** — text-only sibling. Top-N monolith candidates (default 20).

**Why:** cut down monolithic files — agent context windows, avoid overwrite loss.

**Seat:** Slope/PBR plugs **landed #80**. Lab-Rat owns a rust-friendly rewrite still waiting on SVG / density-mask / monolith splits. Useful later for `channels.rs` / stamp stacks / `feel` / `kit_mesh`. Do **not** claim the rewrite shipped.

See `ATELIER_PORTFOLIO_STEAL.md`.
