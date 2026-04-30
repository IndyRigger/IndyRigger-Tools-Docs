# Installation
![Maya](https://img.shields.io/badge/Maya-2022%2B-blue?style=flat-square&logo=autodesk) ![Python](https://img.shields.io/badge/Python-3.7%2B-yellow?style=flat-square&logo=python) ![UI](https://img.shields.io/badge/UI-PySide2%2F6-brightgreen?style=flat-square) ![OS](https://img.shields.io/badge/OS-Windows%20%7C%20macOS%20%7C%20Linux-0078D6?style=flat-square) [![License](https://img.shields.io/badge/License-CC%20BY--NC%204.0-lightgrey?style=flat-square)](https://creativecommons.org/licenses/by-nc/4.0/) ![Indy](https://img.shields.io/badge/Tool-IndyRigger-F04141?style=flat-square)

## Requirements

| Category | Specification |
| :--- | :--- |
| **Maya Version** | 2022–2025+ (Tested) |
| **Python** | 3.7+ |
| **UI Framework** | PySide2 (Maya 2022–2024), PySide6 (Maya 2025+) |
| **OS** | Windows, macOS, Linux |
| **License** | CC BY-NC 4.0 |

<br>

## Install Methods

**Method 1: Drag & Drop (Recommended, Quick Setup)**

1. Unzip the package  
2. Move folder to: *Documents/maya/scripts*  
3. Launch Maya  
4. Drag **install.mel** into the viewport  
5. A shelf button will be created automatically

<p align="center">
  <img src="./assets/images/IDR-maya-rig-tools-Install-File.gif" alt="How to install IDR Maya Tools">
</p>

<br>

**Method 2: Manual Install**
Windows · macOS · Linux

1. Copy folder to: 
   *~/maya/scripts/IDR_[ToolsName]_v2026.1*
2. Open Script Editor (Python) and run:

```python
import os
import sys

home_dir = os.path.expanduser("~")

paths = [
    os.path.join(home_dir, "Documents", "maya", "scripts", "IDR_[ToolsName]_v2026.1", "scripts"),
    os.path.join(home_dir, "maya", "scripts", "IDR_[ToolsName]_v2026.1", "scripts"),
]

for path in paths:
    if os.path.exists(path):
        sys.path.insert(0, path)
        break

import IDR_[ToolsName]
IDR_[ToolsName].show()
```
<br>
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