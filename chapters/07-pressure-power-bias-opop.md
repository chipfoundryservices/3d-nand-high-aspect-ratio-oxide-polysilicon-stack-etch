# Chapter 7: Pressure-Power-Bias Process Window for OPOP Channel Hole Etch

## Executive Summary

This chapter integrates Chapters 5-6's reactor and gas delivery requirements into a unified pressure-power-bias process window specific to OPOP channel hole etch. Building on the general phase-space boundary framework established in 3D NAND literature (insufficient/excessive ion energy, insufficient source power, excessive/insufficient pressure), we show that OPOP's dual-chemistry structure effectively requires characterizing and maintaining *two distinct but connected* process windows — one for oxide layers, one for polysilicon layers — within a single recipe, and examine how these two windows' boundaries differ and interact.

---

## Part 1: Why OPOP Requires Two Process Windows, Not One

### 1.1 The General Framework, Applied to Two Chemistry Regimes

General 3D NAND literature's phase-space boundary framework (insufficient ion energy risking slow etch/early etch-stop; excessive ion energy risking mask erosion/selectivity loss; insufficient source power risking inadequate flux; excessive/insufficient pressure affecting Knudsen transport efficiency and plasma stability) applies independently to each layer type's etch interval within an OPOP recipe, since each interval operates under its own chemistry (fluorocarbon or halogen, Chapter 3) with its own transport parameters (Chapter 4, Section 4.2) and its own mask-erosion and selectivity sensitivities (Chapter 5, Part 2).

### 1.2 Why the Two Windows Are Not Independent

Despite requiring separate characterization, the two process windows are not fully independent, for several reasons developed throughout this chapter: both must operate within the same reactor's achievable pressure, power, and bias range (a hardware constraint shared across both windows); both must transition between each other rapidly and reliably (Chapter 5, Part 3's chemistry-switching requirement, which favors process windows that are not too dissimilar in their pressure/power operating point, to minimize re-stabilization time); and both interact through the shared mask erosion budget (a single hard mask, per general 3D NAND literature's Chapter-2-equivalent treatment, must survive exposure to *both* process windows across the full stack depth, not just one).

---

## Part 2: Mapping the Oxide-Layer Process Window Within OPOP

### 2.1 Why This Window Resembles the General ON-Stack Window

Because oxide chemistry and surface mechanism (Chapter 4, Part 1) transfer directly from general 3D NAND literature, the oxide-layer process window within an OPOP recipe closely resembles the general ON-stack bulk-etch process window already established in that literature: moderate pressure (several to tens of mTorr), source power sufficient for adequate flux at the current etch depth, and bias power moderated to balance ion-assisted etching against mask erosion and sidewall polymer protection.

### 2.2 Where OPOP-Specific Adjustment Is Still Required

Despite this general similarity, the oxide-layer window within OPOP may require adjustment from a pure ON-stack baseline for two reasons: first, mask erosion budget must now be shared with the polysilicon-layer window's own erosion contribution (Section 1.2), potentially requiring somewhat more conservative bias power settings during oxide-layer etch than an ON-only process would use, to preserve adequate mask margin for the full combined stack; second, any cross-chemistry interaction effects at layer transitions (Chapter 4, Section 5.1) may necessitate minor pressure or power adjustment near transition boundaries specifically, distinct from the steady-state, mid-layer oxide etch conditions.

---

## Part 3: Mapping the Polysilicon-Layer Process Window

### 3.1 Pressure Considerations Specific to Halogen Chemistry

Halogen chemistry (Cl2, HBr) plasma behavior and achievable plasma density at a given pressure differ from fluorocarbon chemistry's, reflecting the different electron-impact dissociation and ionization cross-sections of Cl2 and HBr relative to CxFy species (a general plasma chemistry consideration, requiring species-specific characterization rather than direct transfer from fluorocarbon-chemistry-calibrated pressure targets). Chapter 6, Section 4.2's molecular size/mass comparison provides a starting hypothesis for how Knudsen-regime transport pressure sensitivity might differ, but actual polysilicon-layer pressure targets require independent characterization.

### 3.2 Bias Power Considerations Specific to Polysilicon's Selectivity Contrast

Chapter 5, Part 2 established that OPOP's larger intrinsic selectivity contrast demands finer bias power control resolution. Within the polysilicon-layer process window specifically, this translates into a bias power range that must be held within a narrower *relative* margin (as a fraction of the window's total usable range) than the oxide-layer window typically requires, directly reflecting the quantitative control-resolution argument developed in Chapter 5, Part 5.

### 3.3 Why Polysilicon's Grain/Doping Dependence Adds Window Variability

Chapter 2 established that polysilicon's etch rate depends on grain structure and doping level, properties fixed at deposition but potentially varying somewhat within-wafer or lot-to-lot depending on deposition process control (Chapter 2, Section 2.3, Section 3.2). This means the polysilicon-layer process window's practically achievable margins (Section 3.2) must be characterized with some allowance for this materials-driven variability, a consideration with no direct equivalent in oxide's amorphous, materials-property-invariant process window (general 3D NAND literature's oxide treatment).

---

## Part 4: Window Transition Dynamics

### 4.1 Why Minimizing Pressure/Power Discontinuity at Transitions Is Favorable

Chapter 5, Section 3.3 and Chapter 6, Section 2.2 both flagged that chemistry transitions require re-stabilization time, and that this time depends partly on how different the two chemistry groups' operating conditions are. A process window design that deliberately minimizes unnecessary pressure or power discontinuity between the oxide-layer and polysilicon-layer windows (choosing, where process performance allows, similar pressure and power set points for both, even if each window's chemistry-specific optimum might differ slightly) can reduce transition re-stabilization time at some cost to each individual window's narrow optimality — a direct tradeoff between per-layer process optimization and total transition overhead (Chapter 3, Section 5; Chapter 5, Part 6), requiring explicit evaluation during recipe development rather than assuming either extreme (fully independent per-layer optimization, or fully matched conditions across both windows) is automatically correct.

### 4.2 A Representative Process Window Comparison Table

| Variable | Oxide-Layer Window (Within OPOP) | Polysilicon-Layer Window (Within OPOP) | Key Driver of Difference |
|---|---|---|---|
| Pressure | Moderate (several-tens of mTorr range, general 3D NAND baseline) | Potentially distinct, halogen-chemistry-specific (Section 3.1) | Species-specific plasma dissociation/ionization behavior |
| Source power | Sufficient for flux at current depth (general framework) | Similar framework, halogen-species-specific flux targets | Chemistry-specific transport parameters (Chapter 4, Section 4.2) |
| Bias power range | Moderate, mask-erosion-budget-shared (Section 2.2) | Narrower relative margin due to selectivity contrast (Section 3.2) | OPOP's larger intrinsic selectivity contrast (Chapter 5, Part 5) |
| Materials-driven variability | Minimal (amorphous oxide, general literature) | Present (grain/doping variability, Section 3.3) | Polysilicon's polycrystalline, dopable nature (Chapter 2) |

---

## Part 5: Thermal Considerations Specific to the Dual-Window System

### 5.1 Why Chuck/Wafer Temperature Must Satisfy Both Windows Simultaneously

General 3D NAND literature establishes wafer/chuck temperature as an implicit fourth process variable, emerging from plasma heating and chuck cooling capacity rather than being independently settable. For OPOP, this implicit temperature variable must satisfy both the oxide-layer window's temperature sensitivity (polymer deposition rate, byproduct volatility, general literature's framework) and the polysilicon-layer window's distinct temperature sensitivities (halogenated reaction layer kinetics, Chapter 4, Section 2.1-2.2, and SiBr4 volatility management if HBr chemistry is used, Chapter 6, Part 3) simultaneously, within whatever single temperature trajectory the chuck cooling system and recipe thermal management actually produce across a continuous, chemistry-switching etch sequence.

### 5.2 Why This May Favor a Narrower Overall Temperature Operating Band

Because both chemistry-specific temperature sensitivities (Section 5.1) must be satisfied by the same physical wafer temperature at any given moment (temperature cannot be instantaneously and independently set per chemistry the way gas composition can via Section 1 and Chapter 6's dual-delivery-path architecture), OPOP recipes may need to operate within a narrower overall temperature band than either chemistry's individually-optimal temperature range alone would suggest, a further concrete instance of the general "two windows, shared hardware constraints" theme this chapter has developed throughout.

---

## Part 6: A Worked Shared Mask Erosion Budget Calculation

### 6.1 Framing the Problem

Chapter 2 (general 3D NAND literature's hard-mask-budget framework) establishes that total mask thickness deposited must survive erosion across the full channel hole etch duration. For OPOP, this total erosion budget is now the sum of erosion occurring during oxide-layer intervals and erosion occurring during polysilicon-layer intervals — Section 2.2's "shared erosion budget" claim made quantitative.

### 6.2 Illustrative Calculation

Suppose a given mask material erodes at rate $E_{ox} = 0.8\ nm/min$ during oxide-layer etch intervals (under the oxide-layer process window's bias power conditions) and at rate $E_{poly} = 1.1\ nm/min$ during polysilicon-layer etch intervals (illustratively higher, reflecting Section 3.2's narrower, potentially less erosion-conservative bias power margin requirement for polysilicon's selectivity control). For a 128-layer-pair stack with illustrative per-layer etch times of 1.5 minutes (oxide) and 1.2 minutes (polysilicon):

$$\text{Total erosion} = N_{layers} \times (E_{ox} \times t_{ox} + E_{poly} \times t_{poly})$$
$$= 128 \times (0.8 \times 1.5 + 1.1 \times 1.2) = 128 \times (1.2 + 1.32) = 128 \times 2.52 = 322.6\ nm$$

### 6.3 Interpreting the Result and Comparing to a Hypothetical ON-Only Equivalent

If an equivalent ON-stack process (general 3D NAND literature baseline) erodes mask only at the oxide-layer-comparable rate throughout (since nitride etch, per general literature, does not impose the same selectivity-driven bias power constraint OPOP's polysilicon layers do), illustratively at $E_{nitride}\approx 0.85\ nm/min$ for a comparable per-layer etch time:

$$\text{Total erosion}_{ON} = 128 \times (0.8\times1.5 + 0.85\times1.5) \approx 128\times2.475 \approx 316.8\ nm$$

This illustrative comparison shows the two totals are not drastically different in this particular example, but the composition differs meaningfully: OPOP's total is driven by two different erosion rates at two different per-layer durations, meaning the mask budget calculation itself requires the two-window characterization this chapter has emphasized, rather than a single-rate estimate that would risk under- or over-stating the true combined erosion if either layer type's rate or duration differs more substantially from the other than this illustrative example assumes. A process developer relying on a single, oxide-only erosion rate measurement to budget mask thickness for a full OPOP stack risks a meaningful underestimate if polysilicon-layer erosion rate, as in this illustration, runs appreciably higher.

### 6.4 Why This Argues for Independent Erosion Characterization

This worked example is a direct, quantitative justification for Section 1.2's claim that both process windows share a mask erosion budget constraint requiring joint consideration: mask thickness deposition targets for OPOP stacks must be set using independently measured $E_{ox}$ and $E_{poly}$ values combined according to each layer type's actual proportion of total etch time, not estimated from either rate alone or assumed equal to a general ON-stack reference value.

---

## Part 7: Illustrative Combined Process Window Visualization (Descriptive)

### 7.1 Describing the Two-Window Relationship

Because this book's format does not include graphical figures, the two-window relationship developed in Parts 2-4 can be described as follows: imagine a pressure-power-bias phase space (as established generally in 3D NAND literature) containing two distinct, possibly overlapping acceptable regions — one for oxide-layer conditions, one for polysilicon-layer conditions — connected by a transition path the recipe must traverse at every layer boundary. The oxide-layer region's shape and boundaries closely resemble the general ON-stack region (Section 2.1), while the polysilicon-layer region's shape reflects halogen chemistry's distinct pressure sensitivity (Section 3.1) and narrower bias power margin (Section 3.2).

### 7.2 Why Region Overlap or Proximity Is a Favorable Design Target

Per Section 4.1's transition-minimization argument, a favorable OPOP process window design seeks pressure and power set points where these two regions are as close together (ideally overlapping in pressure and power, differing primarily in bias power fine-tuning and gas chemistry) as each region's individual performance requirements allow — minimizing the "distance" the recipe must traverse at each transition, and thereby minimizing both re-stabilization time (Section 4.1) and the risk of transition-induced profile defects (Chapter 3, Section 3.2's necking-defect-analog concern) that a larger window-to-window discontinuity would risk.

---

## Summary and Forward Look

OPOP channel hole etch requires characterizing two distinct pressure-power-bias process windows — one for oxide layers, closely resembling the general ON-stack baseline with modest mask-erosion-budget-sharing adjustment, and one for polysilicon layers, requiring independent halogen-chemistry-specific characterization and accommodating both a narrower selectivity-control margin and materials-driven (grain/doping) variability. These two windows are connected through shared reactor hardware constraints, transition re-stabilization dynamics that favor minimizing window discontinuity, and a single shared wafer temperature trajectory that must satisfy both windows' thermal sensitivities simultaneously.

The next chapter examines the chamber materials and conditioning behavior underlying both of these process windows, addressing how mixed halogen/fluorocarbon exposure affects chamber wall materials, consumable component lifetime, and conditioning/seasoning behavior differently than the fluorocarbon-only exposure general 3D NAND literature addresses.
