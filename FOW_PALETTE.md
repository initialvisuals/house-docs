# FoW palette — internal cheat sheet

Craftsman kit (~90% of project color). Prefix `FOW_` is **color-only**.

- Greys: `FOW_Black` / `FOW_White` at the ends; mid ladder `FOW_Grey_NN` (index rises with lightness).
- Chromatics: short taste names (`FOW_Blood`, `FOW_Foliage`, `FOW_Brass`…).

Machine file lives in fulcrumRust: `assets/trims_utility/fow_palette.json` (`fow_palette/v1`). Named grids: fulcrumRust `assets/trims_utility/readable/`. Scheme: `FOW_PALETTE_SCHEME.md`.
Optional Rust const stub: `assets/trims_utility/fow_color_consts.rs.snippet`.

Plates: `TRIMSHEET_MICRO.png`, `TRIMSHEET_MICRO_GREY.png`, `foliage_colors.png`. Named grids: `assets/trims_utility/readable/`.

## Greys

| Id | Hex | RGB |
|----|-----|-----|
| `FOW_Black` | `#000000` | 0, 0, 0 |
| `FOW_Grey_01` | `#0A0A0A` | 10, 10, 10 |
| `FOW_Grey_02` | `#171717` | 23, 23, 23 |
| `FOW_Grey_03` | `#1A1A1A` | 26, 26, 26 |
| `FOW_Grey_04` | `#1F1F1F` | 31, 31, 31 |
| `FOW_Grey_05` | `#2B2B2B` | 43, 43, 43 |
| `FOW_Grey_06` | `#404040` | 64, 64, 64 |
| `FOW_Grey_07` | `#575757` | 87, 87, 87 |
| `FOW_Grey_08` | `#6B6B6B` | 107, 107, 107 |
| `FOW_Grey_09` | `#7F7F7F` | 127, 127, 127 |
| `FOW_Grey_10` | `#808080` | 128, 128, 128 |
| `FOW_Grey_11` | `#949494` | 148, 148, 148 |
| `FOW_Grey_12` | `#A8A8A8` | 168, 168, 168 |
| `FOW_Grey_13` | `#BABABA` | 186, 186, 186 |
| `FOW_Grey_14` | `#C3C3C3` | 195, 195, 195 |
| `FOW_Grey_15` | `#D4D4D4` | 212, 212, 212 |
| `FOW_Grey_16` | `#D6D6D6` | 214, 214, 214 |
| `FOW_Grey_17` | `#E6E6E6` | 230, 230, 230 |
| `FOW_White` | `#FFFFFF` | 255, 255, 255 |

## Chromatics

| Id | Hex | RGB | Plates |
|----|-----|-----|--------|
| `FOW_Amber` | `#E39500` | 227, 149, 0 | micro |
| `FOW_Bark` | `#75533A` | 117, 83, 58 | micro |
| `FOW_BlackBlood` | `#470000` | 71, 0, 0 | micro |
| `FOW_Blood` | `#E00000` | 224, 0, 0 | micro |
| `FOW_Bone` | `#FFEBAF` | 255, 235, 175 | micro |
| `FOW_Brass` | `#FFA700` | 255, 167, 0 | micro |
| `FOW_Canopy` | `#203319` | 32, 51, 25 | foliage |
| `FOW_Chartreuse` | `#B5E61D` | 181, 230, 29 | micro, foliage |
| `FOW_Clay` | `#A17250` | 161, 114, 80 | micro |
| `FOW_Cream` | `#EFE4B0` | 239, 228, 176 | micro, foliage |
| `FOW_Crimson` | `#A30000` | 163, 0, 0 | micro |
| `FOW_DeepCanopy` | `#0D2911` | 13, 41, 17 | foliage |
| `FOW_DriedBlood` | `#610000` | 97, 0, 0 | micro |
| `FOW_Driftwood` | `#4D4132` | 77, 65, 50 | foliage |
| `FOW_Fern` | `#648246` | 100, 130, 70 | foliage |
| `FOW_FernDark` | `#526B3A` | 82, 107, 58 | foliage |
| `FOW_Foliage` | `#84AB5C` | 132, 171, 92 | foliage |
| `FOW_FoliageLight` | `#A3D472` | 163, 212, 114 | foliage |
| `FOW_Frost` | `#99D9EA` | 153, 217, 234 | micro |
| `FOW_Gold` | `#FFC90E` | 255, 201, 14 | micro, foliage |
| `FOW_Grape` | `#5C165C` | 92, 22, 92 | micro |
| `FOW_Ice` | `#72BEE0` | 114, 190, 224 | micro |
| `FOW_InkGreen` | `#081408` | 8, 20, 8 | foliage |
| `FOW_Lavender` | `#A57ABA` | 165, 122, 186 | micro |
| `FOW_Leaf` | `#22B14C` | 34, 177, 76 | micro, foliage |
| `FOW_Lilac` | `#A369A6` | 163, 105, 166 | micro |
| `FOW_Maroon` | `#800000` | 128, 0, 0 | micro |
| `FOW_Mint` | `#99E099` | 153, 224, 153 | micro |
| `FOW_Moss` | `#688F8D` | 104, 143, 141 | micro |
| `FOW_Mud` | `#332F1D` | 51, 47, 29 | foliage |
| `FOW_Mulberry` | `#732A71` | 115, 42, 113 | micro |
| `FOW_NightMoss` | `#050D05` | 5, 13, 5 | foliage |
| `FOW_Olive` | `#55594B` | 85, 89, 75 | foliage |
| `FOW_Orange` | `#FF7F27` | 255, 127, 39 | micro, foliage |
| `FOW_Orchid` | `#944A8F` | 148, 74, 143 | micro |
| `FOW_Pine` | `#0B3818` | 11, 56, 24 | foliage |
| `FOW_Plum` | `#420A41` | 66, 10, 65 | micro |
| `FOW_PlumDark` | `#290329` | 41, 3, 41 | micro |
| `FOW_Sage` | `#405949` | 64, 89, 73 | foliage |
| `FOW_Sand` | `#D49669` | 212, 150, 105 | micro |
| `FOW_Seaweed` | `#61B095` | 97, 176, 149 | micro |
| `FOW_Sky` | `#7092BE` | 112, 146, 190 | micro |
| `FOW_Soil` | `#29231D` | 41, 35, 29 | micro, foliage |
| `FOW_Spring` | `#65FFA9` | 101, 255, 169 | micro |
| `FOW_SteelBlue` | `#7089BA` | 112, 137, 186 | micro |
| `FOW_Umber` | `#4D412A` | 77, 65, 42 | foliage |
| `FOW_Void` | `#0F010F` | 15, 1, 15 | micro |
| `FOW_Walnut` | `#40392C` | 64, 57, 44 | foliage |
