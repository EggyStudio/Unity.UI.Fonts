# Unity Essentials

This module is part of the Unity Essentials ecosystem and follows the same lightweight, editor-first approach.
Unity Essentials is a lightweight, modular set of editor utilities and helpers that streamline Unity development. It focuses on clean, dependency-free tools that work well together.

All utilities are under the `UnityEssentials` namespace.

```csharp
using UnityEssentials;
```

## Installation

Install the Unity Essentials entry package via Unity's Package Manager, then install modules from the Tools menu.

- Add the entry package (via Git URL)
    - Window → Package Manager
    - "+" → "Add package from git URL…"
    - Paste: `https://github.com/EggyStudio/UnityEssentials.git`

- Install or update Unity Essentials packages
    - Tools → Install & Update UnityEssentials
    - Install all or select individual modules; run again anytime to update

---

# UI Fonts

> Quick overview: UI font families for TextMeshPro, with SDF font assets for Cascadia Mono, Rajdhani and Verily Serif Mono.

This module bundles four font families for UI and HUD text, as TTF and OTF files under `Resources`, with ready-made TextMeshPro SDF font assets for three of them.

## Features
- Fonts included
  - Cascadia Mono, with `Cascadia Mono SDF.asset`
  - Inter, variable fonts in regular and italic, without a font asset
  - Rajdhani in Light, Regular, Medium, SemiBold and Bold, with an SDF asset for each and Shadow SDF assets for Medium, SemiBold and Bold
  - Verily Serif Mono, with `Verily Serif Mono SDF.asset` and `Verily Serif Mono SDF Outline.asset`

## Requirements
- Unity 6000.0 or later
- TextMeshPro, which Unity includes

## Usage

### 1) Use a provided font asset
- Assign one of the `SDF.asset` files to the Font Asset field of a TextMeshPro component
- The assets sit under `Resources`, so `Resources.Load<TMP_FontAsset>("Rajdhani/Rajdhani-Regular SDF")` loads one by path

### 2) Create a font asset for Inter
- Project window, right-click `Resources/Inter/Inter.ttf`, then Create → TextMeshPro → Font Asset
- Or use Window → TextMeshPro → Font Asset Creator, then Save
- Set fallback fonts on a font asset for characters its family does not cover

## Notes and Limitations
- Licensing
  - Each font is distributed under its own license, given in `THIRD-PARTY-NOTICES.md`, and Inter's and Cascadia Mono's SIL Open Font License is also in their folder's `OFL.txt`
- Coverage and glyph sets vary by family
- `Cascadia Mono SDF.asset` was generated from an earlier build of the same Cascadia Mono version, so regenerate it from `Cascadia Mono.ttf` if glyphs render wrong

## Files in This Package
- `Resources/*`, the family folders Cascadia Mono, Inter, Rajdhani and Verily Serif Mono
  - Example: `Resources/Cascadia Mono/Cascadia Mono.ttf`, `Resources/Cascadia Mono/Cascadia Mono SDF.asset`
- `LICENSE.txt`, the MPL 2.0 for the package, and `THIRD-PARTY-NOTICES.md`, the licenses of the fonts

## Tags
unity, ui, text, font, tmp, textmeshpro
