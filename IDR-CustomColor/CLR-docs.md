# IDR CustomColor v2026.1
![Maya](https://img.shields.io/badge/Maya-2022%20--%202025-blue?style=flat-square&logo=autodesk) ![Python](https://img.shields.io/badge/Python-3.7%2B-yellow?style=flat-square&logo=python) ![OS](https://img.shields.io/badge/OS-Windows%20%7C%20macOS%20%7C%20Linux-brightgreen?style=flat-square) [![License](https://img.shields.io/badge/License-CC%20BY--NC%204.0-lightgrey?style=flat-square)](https://creativecommons.org/licenses/by-nc/4.0/)

<br>

![UI Overview](./images/CLR_UI_Overview.gif)

A color management tool for Autodesk Maya, designed to help Riggers and Animators assign colors quickly, accurately, and consistently.

<br>

## Requirements

| Category | Specification |
| :--- | :--- |
| **Maya Version** | 2022, 2023, 2024, 2025+ |
| **Language** | Python 3.7+ |
| **UI Framework** | PySide2 (2022-2024), PySide6 (2025+) |
| **OS Support** | Windows, macOS, Linux |
| **License** | [CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/) |

<br>

## Installation

**Method 1: Drag & Drop (Recommended)**

1. Unzip the package
2. Place the folder (e.g., *Documents/maya/scripts*)
3. Open Maya
4. Drag **install.mel** into the Viewport
5. Shelf button is created automatically

![How to install IDR Maya Tools](../assets/images/IDR-maya-rig-tools-Install-File.gif)

<br>

**Method 2: Manual Install**
Windows · macOS · Linux

1. Copy folder to: *~/maya/scripts/IDR_CustomColor_v2026.1*
2. Open Script Editor (Python) and run:

```python
import os
import sys

home_dir = os.path.expanduser("~")

paths = [
    os.path.join(home_dir, "Documents", "maya", "scripts", "IDR_CustomColor_v2026.1", "scripts"),
    os.path.join(home_dir, "maya", "scripts", "IDR_CustomColor_v2026.1", "scripts"),
]

for path in paths:
    if os.path.exists(path):
        sys.path.insert(0, path)
        break

import IDR_CustomColor
IDR_CustomColor.show()
```

<br>
<br>

# **🔴 Color System & ACES**

💡 Before starting, the tool includes 115 preset colors: 31 Maya Index Colors and 84 ACES colors. This ensures accurate viewport color matching across all modes.

![*The current color mode is displayed on the right side of the input field.*](./images/CLR_ACES_Explan.gif)

## What is ACES?

The ACES values in this tool are not true ACEScg. They are sampled directly from Maya to ensure a 100% match with viewport colors. This can be considered "Fake ACES," focused on visual accuracy.

The tool provides three color modes: **Index**, **ACES**, and **RGB**.

> <small>⚠️ Custom colors (Eyedropper or HEX) use standard RGB only and may not match exactly in the viewport.
> 💡 For more details on RGB, Maya Index Color, and ACEScg, see the Terminology section below.</small>

<br>
<br>

# **🔴 Color Palette**

## 115 Preset Colors

![*Select an object in Maya → Click a color button or press **Apply***](./images/CLR_115_Preset_Colors.gif)

Browse and apply from 115 preset colors divided into:

- **Main Palette** (11 signature colors)
- **More Colors** (104 extended colors)

<br>

## Color Input

![*Enter a color value → Right-click to switch mode (HEX / RGB / HSV / ACEScg) → Press Enter*](./images/CLR_Color_Input.gif)

Enter the desired color value in HEX / RGB / HSV / ACEScg format.

- **Right-click** input field to switch color mode
- **Smart paste**: auto-detects format on paste

<br>

## Current Color

![*Left-click the **Current Color** button to open the Maya Color Editor.*](./images/CLR_Current_Color.gif)

Displays the active color. Left-click to open the Maya Color Editor and select additional colors.

<br>

## Brightness

![*Set → Apply*](./images/CLR_Brightness.gif)

Adjust brightness before applying (no hue shift).

> <small>💡 0 = black · 50 = original · 100 = bright</small>

<br>

## Eyedropper

![*Click → Hover to preview → Left-click to pick (Esc / right-click to cancel)*](./images/CLR_Eyedropper.gif)

Pick any color from anywhere on screen. Features an 11×11 zoom preview grid with HEX readout in the color bar.

> <small>💡 Multi-monitor support with zoom preview</small>

<br>
<br>

# 🔴 Favorite Presets

![CLR_Favorite_Presets_01.gif](./images/CLR_Favorite_Presets_01.gif)

Store and reuse colors with 12 slots. Supports RGB, ACES, and Maya Index, with custom names and drag & drop.

- **Save**: Click an empty slot to store current color
- **Sort**: Move filled slots to the front
- **Blend**: Generate gradients between slots
- **Rename**: Name appears on hover
- **Auto Save**: Saved & restored automatically
File: `resources/presets/favorites.json`

> <small>💡 Share the JSON for team use</small>

## Built-in Palette Files

In addition to personal slots, the tool includes 8 ready-made palette files curated for rigging work:

| Palette | Description |
| --- | --- |
| Color Pastel 1 | Soft pastel tones |
| Rigging Controls 1 | Standard rig colors |
| Rigging Controls 2 | Extended rig colors |
| Toon – Lips Eyes Hair | Toon character features |
| Toon – Skin | Skin tones for toon rigs |
| Toon – Nature | Nature-themed toon colors |
| Toon – Sky | Sky and atmosphere tones |
| zIDR Code | IDR internal color code set |

![*Right-click a slot → **Load** to apply instantly.*](./images/CLR_Favorite_Presets_02.gif)

> <small>💡 User-saved palettes appear automatically in the menu.</small>

<br>
<br>

# 🔴 Viewport & Outliner

![CLR_ViewportOutliner.gif](./images/CLR_ViewportOutliner.gif)

Choose whether color is applied to the Viewport (shape node), Outliner (transform node), or both.

- **Viewport**: Colors the shape node in the Maya scene
- **Outliner**: Colors the transform in the Outliner panel

<br>
<br>

# 🔴 Apply Color

## Apply & Reset

![*Select → Choose color → Click **Apply** · Select → Click **Reset***](./images/CLR_AppleReset.gif)

- **Apply**: Applies selected color to objects (Viewport / Outliner)
- **Reset**: Restores color to default (disables override)

<br>

## Random Color

![*Select → Right-click Apply Button → Click **Random***](./images/CLR__Random_Color.gif)

Assign random colors from 11 presets (no repeats if ≤11 objects).

> <small>💡 Auto reshuffle when exceeded</small>

<br>

## Rainbow Color

![*Select → Right-click Apply Button → Click **Rainbow***](./images/CLR__Rainbow_Color.gif)

Distribute colors in sequence across objects.

> <small>💡 Auto interpolate if fewer objects than presets</small>

<br>

## Fade Dark / Light

![*Select → Right-click Apply Button → Click **Fade Dark / Light***](./images/CLR_Fade_Dark_Light.gif)

Fade color across selection (dark or light direction).

> <small>💡 Dark: progressively darker · Light: progressively brighter/desaturated</small>

<br>

## Display Type

![*Select → Right-click Apply Button → Display Type*](./images/CLR_Display_Type.gif)

Set viewport display mode: **Normal / Template / Reference**

<br>
<br>

# 🔴 Create Material

![*Select → Choose color → **Create Material** → Pick shader*](./images/CLR_Create_Material.gif)

Create and assign a material directly from the current color.

> <small>💡 Supports: lambert / blinn / surfaceShader / standardSurface</small>

<br>
<br>

---

# 🔴 Troubleshooting

- **Viewport color mismatch**: RGB colors (HEX / Eyedropper) may differ in ACES mode. Use the ACES palette for accurate results.
- **Apply not working**: Ensure objects are selected and Viewport/Outliner checkbox is enabled. Locked or connected attributes are skipped.
- **Favorite slots reset**: Check that `favorites.json` exists in the presets folder.
- **Tool not opening / duplicate window**: Only one instance is allowed. Re-run the script to refocus or reopen.
- **Eyedropper not working**: Press Esc to cancel, or click the Maya viewport to refocus and try again.

<br>

# 🔴 Terminology

- **RGB / HEX / HSV**: Standard color formats. RGB uses 3 channels, HEX is #RRGGBB, HSV represents Hue, Saturation, Value.
- **Maya Index Color**: Legacy system with 31 fixed color IDs predefined in Maya.
- **ACEScg**: Wide color space used in VFX. In this tool, values are sampled from Maya ("Fake ACES") to match viewport colors visually.
- **Linear sRGB**: All RGB values are automatically converted before applying (no manual step required).
- **Override Color**: Applies color without a material using Maya override attributes. Reset disables this.
- **Viewport / Outliner**: Viewport applies to Shape Node (object color), Outliner applies to Transform Node (name color).
- **Shape Node / Transform Node**: Shape = geometry data, Transform = position/rotation/scale.
- **Shader / Material**: Creates and assigns a material from the selected color (Lambert, Blinn, etc.).
- **Undo Chunk**: Groups all actions so changes undo together in one Ctrl+Z.

<br>

## Get the Tools
Visit the official store for advanced scripts and premium rigging assets.

[![Gumroad](https://img.shields.io/badge/Gumroad-IndyRigger-black?style=flat-square&logo=gumroad)](https://indyrigger.gumroad.com/)

<br>

## Support This Project
If you find these tools helpful, consider supporting further development.

[![Buy Me A Coffee](https://img.shields.io/badge/Support-Buy%20Me%20A%20Coffee-orange?style=flat-square&logo=buy-me-a-coffee)](https://buymeacoffee.com/indyrigger)

<br>

## Connect & Contact
Follow for the latest updates, tutorials, and more rigging content.

[![Facebook](https://img.shields.io/badge/Facebook-IndyRigger-blue?style=flat-square&logo=facebook)](https://www.facebook.com/indyrigger) [![YouTube](https://img.shields.io/badge/YouTube-IndyRigger-red?style=flat-square&logo=youtube)](https://www.youtube.com/indyrigger) [![Email](https://img.shields.io/badge/Email-rigger.indy@gmail.com-white?style=flat-square&logo=gmail)](mailto:rigger.indy@gmail.com)

<br>
<br>

<p align="center">
© 2026 Indy Rigger • Some rights reserved.
</p>