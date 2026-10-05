# 3D NAND High-Aspect-Ratio Oxide/Polysilicon Stack Etch

## Sacrificial Polysilicon Integration, Halogen-Based Etch Chemistry, and Selectivity Engineering for Replacement-Gate 3D NAND

**A ChipFoundryServices Technical Series Publication**

---

## Overview

*3D NAND High-Aspect-Ratio Oxide/Polysilicon Stack Etch* is a focused technical treatment of the oxide/polysilicon (OPOP) sacrificial stack variant used in a subset of replacement-gate 3D NAND integration schemes. Where oxide/nitride (ON) stacks dominate industry volume and are treated extensively elsewhere, this book addresses the distinct physics, chemistry, and process engineering that arise when **polysilicon**, not silicon nitride, serves as the sacrificial layer removed and replaced with metal word lines.

This substitution is not cosmetic. Polysilicon is a semiconductor, not a dielectric; it is removed by a different wet/dry chemistry than nitride; its intrinsic etch selectivity against oxide follows a different mechanism than nitride's; and its electrical conductivity interacts with plasma charging effects at extreme aspect ratio in ways a purely dielectric stack does not. This book traces these differences from materials and chemistry fundamentals through chamber engineering, process physics, and production integration, written specifically for readers who already work with or around 3D NAND etch and need the oxide/polysilicon-specific detail that general 3D NAND treatments do not provide.

---

## Audience

This book is written for:
- **Process Engineers** developing or evaluating OPOP-based channel hole, staircase, or slit etch recipes
- **Equipment Vendors and Equipment Engineers** designing or specifying reactors and chemistries for oxide/polysilicon-selective etch
- **Process Developers** evaluating OPOP against oxide/nitride integration for a given technology node or product line
- **Industry Researchers** studying comparative 3D NAND integration schemes, selectivity mechanisms, or charging physics in semiconducting versus dielectric sacrificial stacks

This is a semi-professional industry text assuming working familiarity with 3D NAND etch fundamentals (channel hole etch, aspect-ratio-dependent etching, replacement-gate integration) at the level covered in general 3D NAND process texts. It does not re-derive that foundational material in full; it focuses specifically on where oxide/polysilicon integration diverges from the oxide/nitride baseline, and why.

---

## Table of Contents

### Front Matter
- **Preface:** Why Oxide/Polysilicon Is a Distinct Engineering Problem, Not a Drop-In Substitution

### Part I: OPOP Stack Fundamentals (Chapters 1-4)
1. Introduction: Why Oxide/Polysilicon Stacks, Industrial Context & Adoption Landscape
2. Polysilicon as a Sacrificial Material: Deposition, Grain Structure, Doping Effects
3. Halogen Chemistry for Oxide/Polysilicon Etch (Cl2, HBr, SF6, Fluorocarbon Comparison)
4. Plasma-Oxide and Plasma-Polysilicon Surface Reactions at Extreme Aspect Ratio

### Part II: Chamber & Process Engineering for OPOP Etch (Chapters 5-9)
5. Reactor Requirements Specific to Oxide/Polysilicon Selectivity Control
6. Gas Delivery and Byproduct Management for Halogen/Fluorocarbon Hybrid Chemistry
7. Pressure-Power-Bias Process Window for OPOP Channel Hole Etch
8. Chamber Materials and Conditioning Under Mixed Halogen/Fluorocarbon Exposure
9. RF and Pulsing Strategies for Oxide/Polysilicon Selectivity Modulation

### Part III: Process Physics Specific to OPOP (Chapters 10-14)
10. ARDE and Transport Physics in Oxide/Polysilicon Stacks vs. Oxide/Nitride
11. Charging and Profile Defects: The Semiconducting Sidewall Problem
12. Oxide/Polysilicon Selectivity Engineering and Averaged Selectivity Control
13. Polysilicon-Specific Staircase Etch Considerations
14. Sacrificial Polysilicon Removal and Word Line Replacement for OPOP Stacks

### Part IV: Production Integration (Chapter 15)
15. Equipment Differentiation, Vendor Landscape, and Yield Economics for OPOP Integration

### Back Matter
- **Glossary:** OPOP Etch-Specific Terminology
- **Appendix A:** Thermodynamic & Material Property Data Tables
- **Appendix B:** Material Compatibility Matrix (Chamber Components Under Mixed Chemistry)
- **Appendix C:** Standard Operating Procedures
- **Appendix D:** ARDE / Selectivity Correction Lookup Tables (Oxide/Polysilicon)
- **Appendix E:** Charging & Thermal Calculations for Semiconducting Sacrificial Stacks
- **Appendix F:** Endpoint Detection Calibration for Oxide/Polysilicon Transitions

---

## File Organization

```
3d-nand-high-aspect-ratio-oxide-polysilicon-stack-etch/
├── README.md
├── PREFACE.md
├── INDEX.md
├── chapters/
│   ├── 01-opop-industrial-context.md
│   ├── 02-polysilicon-sacrificial-material.md
│   ├── 03-halogen-chemistry.md
│   ├── 04-plasma-oxide-polysilicon-reactions.md
│   ├── 05-reactor-requirements-selectivity.md
│   ├── 06-gas-delivery-hybrid-chemistry.md
│   ├── 07-pressure-power-bias-opop.md
│   ├── 08-chamber-materials-mixed-chemistry.md
│   ├── 09-rf-pulsing-selectivity-modulation.md
│   ├── 10-arde-opop-vs-on.md
│   ├── 11-charging-semiconducting-sidewall.md
│   ├── 12-selectivity-engineering-opop.md
│   ├── 13-staircase-opop.md
│   ├── 14-polysilicon-removal-word-line-replacement.md
│   └── 15-equipment-vendor-yield-economics.md
├── appendices/
│   ├── glossary.md
│   ├── thermodynamic-data.md
│   ├── material-compatibility.md
│   ├── standard-procedures.md
│   ├── correction-tables.md
│   ├── charging-thermal-calculations.md
│   └── endpoint-detection.md
```

---

## Key Technical Themes

### 1. **Polysilicon Is Semiconducting, Not Dielectric — This Changes Everything Downstream**
Every chamber charging, selectivity, and removal-chemistry decision in this book traces back to one structural fact: the sacrificial layer conducts, however modestly, rather than insulating. This affects differential charging at extreme aspect ratio, sidewall-to-bulk charge dissipation pathways, and removal chemistry selection, none of which transfer unchanged from an oxide/nitride baseline.

### 2. **Larger Intrinsic Selectivity Contrast, Different Control Problem**
Oxide/polysilicon's intrinsic etch rate contrast is generally larger than oxide/nitride's, meaning the "suppress nitride's faster chemical etch rate" selectivity-engineering problem familiar from ON stacks becomes a "suppress polysilicon's substantially faster chemical and physical etch rate" problem of different magnitude and different chemistry sensitivity.

### 3. **Halogen Chemistry, Not Pure Fluorocarbon**
Polysilicon etch is conventionally halogen-chemistry territory (Cl2, HBr) in planar and logic applications. Oxide/polysilicon stack etch must reconcile this halogen chemistry with the fluorocarbon-based, polymer-passivation-dependent anisotropy mechanism that extreme-aspect-ratio dielectric etch depends on — a chemistry integration problem with no equivalent in oxide/nitride stacks.

### 4. **Sacrificial Removal Is a Different Unit Operation Entirely**
Hot phosphoric acid, the industry-standard sacrificial nitride removal chemistry, does not remove polysilicon. OPOP integration requires a distinct removal chemistry (commonly TMAH-based or halogen-based) with its own lateral-access, selectivity, and structural-support-during-removal characteristics.

### 5. **Equipment and Vendor Differentiation**
Because OPOP is a minority integration path relative to oxide/nitride, equipment and chemistry qualification for OPOP-specific requirements represents a distinct vendor and tool-qualification landscape, with direct consequences for which equipment platforms and chemistries a fab or process developer can access.

---

## Constraints & Scope

### In Scope
- Oxide/polysilicon (OPOP) sacrificial stacks in replacement-gate 3D NAND, as an alternative to oxide/nitride (ON)
- Channel hole, staircase, and slit/word-line-replacement etch as applied specifically to OPOP stacks
- Halogen (Cl2, HBr) and fluorocarbon hybrid chemistry for oxide/polysilicon selective etch
- Polysilicon-specific sacrificial removal chemistry and process integration
- Charging and profile-defect physics specific to a semiconducting sacrificial layer

### Out of Scope
- Oxide/nitride (ON) stack etch in general (treated in other series volumes; referenced here only comparatively)
- Front-end CMOS logic polysilicon gate etch (a related but distinct application with different stack context)
- Deposition process detail for polysilicon or oxide films beyond what is needed to explain etch-relevant properties
- 2D/planar NAND flash processes
- Charge-trap (ONO) stack deposition detail, except where needed to frame the channel hole etch target

---

## Development Status

**Status:** In Development (chapters authored sequentially; see INDEX.md for current status)

**Version:** 0.1 (Manuscript Development Phase)

---

## Attribution & License

This book is authored by **ChipFoundryServices** and distributed under the **Creative Commons Attribution 4.0 International (CC-BY-4.0)** license.

**Academic citations welcome.** Please cite as:

> ChipFoundryServices. (2026). *3D NAND High-Aspect-Ratio Oxide/Polysilicon Stack Etch — Sacrificial Polysilicon Integration, Halogen-Based Etch Chemistry, and Selectivity Engineering for Replacement-Gate 3D NAND*. GitHub. https://github.com/chipfoundryservices/3d-nand-high-aspect-ratio-oxide-polysilicon-stack-etch

---

[Begin Reading →](INDEX.md)
