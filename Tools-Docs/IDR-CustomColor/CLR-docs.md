# IDR CustomColor v2026.1
![Maya](https://img.shields.io/badge/Maya-2022%2B-blue?style=flat-square&logo=autodesk) ![Python](https://img.shields.io/badge/Python-3.7%2B-yellow?style=flat-square&logo=python) ![UI](https://img.shields.io/badge/UI-PySide2-brightgreen?style=flat-square) ![OS](https://img.shields.io/badge/OS-Windows%20%7C%20macOS%20%7C%20Linux-0078D6?style=flat-square) [![License](https://img.shields.io/badge/License-CC%20BY--NC%204.0-lightgrey?style=flat-square)](https://creativecommons.org/licenses/by-nc/4.0/) ![Indy](https://img.shields.io/badge/Tool-IndyRigger-F04141?style=flat-square)

<br>

<p align="center">
  <img src="./images/CLR_UI_Overview.gif" alt="UI Overview">
</p>

A powerful toolkit for fast, consistent coloring in Maya. Includes 115 preset colors (Index & ACES) with accurate viewport matching, plus HEX/RGB/HSV/ACEScg input and Eyedropper. Random, Rainbow, Fade, Blend, and 12 Favorites enable quick multi-object coloring.

<br>

## Installation Guide

👉 **[Install Tools](../Install-Tools.md)**

<br>

## Color System & ACES**

💡 Before starting, the tool includes 115 preset colors: 31 Maya Index Colors and 84 ACES colors. This ensures accurate viewport color matching across all modes.

<p align="center">
  <img src="./images/CLR_ACES_Explan.gif" alt="ACES Mode">
</p>

## What is ACES?

The ACES values in this tool are not true ACEScg. They are sampled directly from Maya to ensure a 100% match with viewport colors. This can be considered "Fake ACES," focused on visual accuracy.

The tool provides three color modes: **Index**, **ACES**, and **RGB**.

> <small>⚠️ Custom colors (Eyedropper or HEX) use standard RGB only and may not match exactly in the viewport.<br>
> 💡 For more details on RGB, Maya Index Color, and ACEScg, see the Terminology section below.</small>

<br>
<br>

## 115 Preset Colors

<p align="center">
  <img src="./images/CLR_115_Preset_Colors.gif" alt="Preset Colors">
</p>

Browse and apply from 115 preset colors divided into:

- **Main Palette** (11 signature colors)
- **More Colors** (104 extended colors)

<br>
<br>

## Color Input

<p align="center">
  <img src="./images/CLR_Color_Input.gif" alt="Color Input">
</p>

Enter the desired color value in HEX / RGB / HSV / ACEScg format.

- **Right-click** input field to switch color mode
- **Smart paste**: auto-detects format on paste

<br>
<br>

## Current Color

<p align="center">
  <img src="./images/CLR_Current_Color.gif" alt="Current Color">
</p>

Displays the active color. Left-click to open the Maya Color Editor and select additional colors.

<br>
<br>

## Brightness

<p align="center">
  <img src="./images/CLR_Brightness.gif" alt="Brightness">
</p>

Adjust brightness before applying (no hue shift).

> <small>💡 0 = black · 50 = original · 100 = bright</small>

<br>
<br>

## Eyedropper

<p align="center">
  <img src="./images/CLR_Eyedropper.gif" alt="Eyedropper">
</p>

Pick any color from anywhere on screen. Features an 11×11 zoom preview grid with HEX readout in the color bar.

> <small>💡 Multi-monitor support with zoom preview</small>

<br>
<br>

## Favorite Presets

<p align="center">
  <img src="./images/CLR_Favorite_Presets_01.gif" alt="Favorites">
</p>

Store and reuse colors with 12 slots. Supports RGB, ACES, and Maya Index, with custom names and drag & drop.

- **Save**: Click an empty slot to store current color
- **Sort**: Move filled slots to the front
- **Blend**: Generate gradients between slots
- **Rename**: Name appears on hover
- **Auto Save**: Saved & restored automatically
File: `resources/presets/favorites.json`

> <small>💡 Share the JSON for team use</small>

<br>
<br>

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

<p align="center">
  <img src="./images/CLR_Favorite_Presets_02.gif" alt="Load Palette">
</p>

> <small>💡 User-saved palettes appear automatically in the menu.</small>

<br>
<br>

## Viewport & Outliner

<p align="center">
  <img src="./images/CLR_ViewportOutliner.gif" alt="Viewport & Outliner">
</p>

Choose whether color is applied to the Viewport (shape node), Outliner (transform node), or both.

- **Viewport**: Colors the shape node in the Maya scene
- **Outliner**: Colors the transform in the Outliner panel

<br>
<br>


## Apply & Reset

<p align="center">
  <img src="./images/CLR_AppleReset.gif" alt="Apply & Reset">
</p>

- **Apply**: Applies selected color to objects (Viewport / Outliner)
- **Reset**: Restores color to default (disables override)

<br>
<br>

## Random Color

<p align="center">
  <img src="./images/CLR__Random_Color.gif" alt="Random Color">
</p>

Assign random colors from 11 presets (no repeats if ≤11 objects).

> <small>💡 Auto reshuffle when exceeded</small>

<br>
<br>

## Rainbow Color

<p align="center">
  <img src="./images/CLR__Rainbow_Color.gif" alt="Rainbow Color">
</p>

Distribute colors in sequence across objects.

> <small>💡 Auto interpolate if fewer objects than presets</small>

<br>
<br>

## Fade Dark / Light

<p align="center">
  <img src="./images/CLR_Fade_Dark_Light.gif" alt="Fade Color">
</p>

Fade color across selection (dark or light direction).

> <small>💡 Dark: progressively darker · Light: progressively brighter/desaturated</small>

<br>
<br>

## Display Type

<p align="center">
  <img src="./images/CLR_Display_Type.gif" alt="Display Type">
</p>

Set viewport display mode: **Normal / Template / Reference**

<br>
<br>

## Create Material

<p align="center">
  <img src="./images/CLR_Create_Material.gif" alt="Create Material">
</p>

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

[![Facebook](https://img.shields.io/badge/Facebook-IndyRigger-blue?style=flat-square&logo=facebook)](https://www.facebook.com/indyrigger) [![YouTube](https://img.shields.io/badge/YouTube-IndyRigger-red?style=flat-square&logo=youtube)](https://www.youtube.com/indyrigger) [![Email](https://img.shields.io/badge/Email-rigger.indy@gmail.com-eeeeee?style=flat-square&logo=gmail&labelColor=333333)](mailto:rigger.indy@gmail.com)

<br>
<br>

<p align="center">
© 2026 Indy Rigger • Some rights reserved.
</p>