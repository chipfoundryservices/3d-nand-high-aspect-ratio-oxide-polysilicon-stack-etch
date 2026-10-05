# Chapter 5: Reactor Requirements Specific to Oxide/Polysilicon Selectivity Control

## Executive Summary

Part I established that OPOP channel hole etch requires two mechanistically distinct chemistry and surface reaction systems operating within the same feature. This chapter opens Part II by establishing what this dual-chemistry requirement demands of reactor architecture, building on the general source/bias decoupling rationale established in 3D NAND literature (ICP with separate wafer bias, or dual-frequency CCP) and identifying where OPOP's specific selectivity control and chemistry-switching requirements impose additional, OPOP-specific reactor capability beyond that general baseline.

---

## Part 1: Why General 3D NAND Reactor Architecture Is a Necessary but Insufficient Starting Point

### 1.1 What Transfers Directly

The fundamental argument for high-density, source/bias-decoupled plasma architecture (ICP with independently controlled wafer bias, or dual/multi-frequency CCP), established generally in 3D NAND literature for extreme-aspect-ratio dielectric etch, applies to OPOP channel hole etch without modification: both oxide and polysilicon layers, at the aspect ratios 3D NAND channel hole etch operates at, require independently tunable ion flux (source power) and ion energy (bias power) for the same transport and surface-activation reasons general literature establishes. A reactor architecture inadequate for extreme-AR ON stack etch would be equally inadequate for OPOP stack etch on these general grounds alone.

### 1.2 What Does Not Transfer: Chemistry-Switching Capability

What general 3D NAND reactor treatment does not address, because ON stacks do not require it, is the capability to execute rapid, repeated, full chemistry-family switches (fluorocarbon to halogen and back, Chapter 3, Part 3) at every layer transition throughout a single continuous etch process. This capability — encompassing gas delivery system design (Chapter 6), purge/stabilization speed, and process control sequencing — is an OPOP-specific reactor requirement with no direct general-3D-NAND equivalent, and is this chapter's central new contribution beyond the general architectural baseline.

---

## Part 2: Selectivity Control as a First-Order Reactor Design Driver

### 2.1 Why OPOP's Larger Intrinsic Selectivity Contrast Changes Reactor Requirements

Chapter 1, Section 6.1 previewed that oxide/polysilicon's intrinsic selectivity contrast against oxide is generally larger than oxide/nitride's. Chapter 12 develops this quantitatively, but the reactor-architecture consequence can be stated directly here: achieving a desired, controlled selectivity target (whether near-balanced for profile-protective bulk etch, or deliberately high for stop-layer protection, following the same general selectivity-target framework 3D NAND literature establishes) from a larger intrinsic starting contrast requires correspondingly more capable, more precisely controllable selectivity-suppressing or selectivity-enhancing mechanisms — placing a higher premium on fine-grained ion energy and chemistry control than an ON stack's more moderate intrinsic contrast demands.

### 2.2 Why This Favors Maximal Source/Bias Independence

Because selectivity control in both the ON and OPOP cases is substantially mediated through ion-energy-dependent mechanisms (ion-assisted damage layer formation and polymer/passivation layer clearing, established generally and extended for polysilicon's oxyhalide passivation mechanism in Chapter 4, Section 3.2), and because OPOP's larger intrinsic contrast demands finer selectivity control margin (Section 2.1), OPOP reactor selection favors architectures offering the most complete, least-compromised source/bias independence — generally pointing toward ICP with separately biased wafer electrodes, or the most capable dual/multi-frequency CCP configurations, rather than architectures offering only partial flux/energy decoupling that might be acceptable for a lower-selectivity-contrast ON process.

### 2.3 Why Polysilicon's Doping and Grain Structure Add a Further Control Dimension

Chapter 2 established that polysilicon's etch rate depends on doping level and grain structure, properties that are fixed by the time etch begins (set during deposition, Chapter 2, Parts 1-3) but that nonetheless mean a given reactor's selectivity-control settings must be characterized against the *specific* polysilicon film properties in use, not against a generic "polysilicon" material assumption — directly analogous to, but a further compounding factor beyond, the deposition-recipe-dependent film property characterization general 3D NAND literature already establishes as necessary for PECVD oxide and nitride films.

---

## Part 3: Reactor Requirements for Rapid Chemistry Switching

### 3.1 Why Switching Speed Is a Reactor-Level, Not Purely Recipe-Level, Capability

Chapter 3, Section 5's worked transition-overhead calculation showed that per-transition purge/stabilization time compounds significantly across a full-stack OPOP etch. Reducing this overhead is partly a recipe design question (Chapter 3, Section 3.3's partial chemistry overlap approaches) but is equally, and perhaps more fundamentally, a reactor hardware question: how quickly can the gas delivery system (Chapter 6) actually transition delivered gas composition from one chemistry family to another, how quickly does chamber pressure and plasma condition re-stabilize after such a transition, and how reliably can process control systems execute this transition repeatedly, hundreds of times, within a single continuous etch process without cumulative drift or error.

### 3.2 Gas Panel and Valve Architecture Implications

Rapid, repeated chemistry-family switching favors gas panel architectures with dedicated, independently valved delivery lines for the fluorocarbon chemistry group and the halogen chemistry group (rather than a single shared delivery path requiring full purge between every use of each chemistry group), minimizing the physical gas-line volume that must be cleared at each transition and thereby directly reducing the purge/stabilization time Chapter 3's calculation depends on. This is a concrete, reactor-hardware-level design choice with no equivalent requirement in ON-stack-only tool platforms, where a single, shared fluorocarbon-chemistry gas delivery path suffices throughout.

### 3.3 Chamber Volume and Pressure Stabilization Speed

Chapter 6 (general 3D NAND literature's treatment, extended for OPOP in the next chapter of this book) establishes chamber residence time as a function of chamber volume, pressure, and flow rate. For OPOP's repeated chemistry-switching requirement, chamber volume specifically becomes a double-edged design parameter: a smaller chamber volume favors faster pressure/composition re-stabilization after each chemistry switch (reducing Section 3.1's transition overhead), but, per general 3D NAND literature's residence time tradeoffs, must still support adequate residence time for whichever chemistry is currently active to properly supply the extreme-aspect-ratio transport problem each layer's etch faces independently.

### 3.4 Process Control System Sequencing Requirements

Beyond physical gas delivery hardware, the process control system orchestrating a full OPOP channel hole etch recipe must reliably sequence through potentially hundreds of chemistry-family transitions (one per layer pair, per Chapter 3's transition-count discussion) with consistent, repeatable timing and parameter accuracy at every single transition — a software/control-system reliability and precision requirement considerably more demanding than the handful of major recipe-step transitions a general ON-stack channel hole etch recipe requires, and a capability not all legacy or ON-optimized tool control systems may support without modification or upgrade.

---

## Part 4: Reactor Platform Comparison for OPOP Suitability

### 4.1 Summary Comparison Table

| Reactor Capability | Baseline Requirement (shared with ON, general 3D NAND literature) | OPOP-Specific Additional Requirement |
|---|---|---|
| Source/bias power independence | Required for extreme-AR flux/energy control | Favored toward maximal independence given larger selectivity contrast (Section 2.2) |
| Plasma density regime | High-density ($10^{11}$-$10^{12}\ \text{cm}^{-3}$ class) | Unchanged from general baseline |
| Gas delivery architecture | Single-chemistry-family delivery path sufficient | Dedicated, independently valved paths per chemistry family favored (Section 3.2) |
| Chamber volume optimization target | Residence time vs. plasma density tradeoff (general literature) | Additional consideration: transition re-stabilization speed (Section 3.3) |
| Process control sequencing capability | Handful of major recipe steps | Hundreds of reliable, repeatable chemistry-family transitions (Section 3.4) |
| Pulsing capability | Favored for profile/charging control (general literature) | Additionally relevant for selectivity modulation (Chapter 9) |

### 4.2 Why Not Every ON-Qualified Platform Is Automatically OPOP-Ready

Section 4.1's rightmost column makes explicit why Chapter 1, Section 4.3's observation — that OPOP process development frequently requires either dedicated OPOP-capable equipment or adaptation of ON-qualified platforms — is a direct, mechanistically grounded conclusion rather than an incidental industry pattern: a reactor platform qualified and optimized purely for ON stack etch may lack the dedicated chemistry-family gas delivery architecture (Section 3.2) and process control sequencing capability (Section 3.4) that OPOP's chemistry-switching requirement imposes, even if its core plasma source architecture (Section 2.2's selectivity-control requirement) is otherwise perfectly adequate. Chapter 15 returns to this equipment qualification gap with full economic and vendor-landscape treatment.

---

## Part 5: Quantifying the Selectivity Control Margin Requirement

### 5.1 Why Larger Intrinsic Contrast Demands Proportionally Finer Control Resolution

Using the general sheath-voltage/ion-energy framework established in 3D NAND literature (sheath voltage $V_s$ setting ion energy, which mediates selectivity-relevant mechanisms per Chapter 4), consider the practical consequence of needing to suppress or enhance a larger intrinsic selectivity contrast within the same achievable bias power adjustment range a reactor provides. If a reactor's bias power control resolution provides, for illustration, control over $V_s$ in increments corresponding to roughly 2% selectivity change per control step for an ON-stack process (a representative, illustrative figure), the same absolute control resolution applied to OPOP's larger intrinsic contrast (Chapter 1's preview, Chapter 12's full quantitative treatment) would correspond to a *larger* absolute selectivity swing per control step, when expressed relative to OPOP's wider overall contrast range — effectively coarser *relative* control resolution unless the reactor's bias power control granularity is specifically improved to compensate.

### 5.2 Illustrative Implication

**Illustrative comparison:** suppose an ON-stack process requires holding averaged selectivity within $\pm 10\%$ of a target near 1.0 (general 3D NAND literature's near-balanced bulk-etch target), achievable with a reactor providing bias power control resolution corresponding to roughly $\pm 2\%$ selectivity change per adjustment step — ample margin for the required control precision. If an equivalent OPOP process's intrinsic contrast is, illustratively, twice as large (Chapter 12 develops the actual magnitude), achieving the same relative $\pm 10\%$ selectivity control band around whatever target point is chosen requires either twice the absolute bias power control resolution, or acceptance of a proportionally wider relative control margin than the ON case tolerates — a direct, quantitative reason Section 2.2's "favored toward maximal source/bias independence" recommendation is not merely a qualitative preference but reflects a genuine control-resolution requirement gap between the two stack types.

### 5.3 Why This Argues for Reactor Investment, Not Just Recipe Tuning

Because bias power control resolution is fundamentally a reactor hardware/RF generator capability (Chapter 9 develops the specific RF system requirements further), Section 5.2's illustrative gap cannot be fully closed through recipe tuning alone on a reactor with inherently coarser control resolution — it requires either accepting a wider selectivity control band for OPOP processes (with corresponding yield/margin consequences, echoing the margin discussion found throughout general 3D NAND process control literature) or investing in reactor/RF hardware with finer control resolution specifically to support OPOP's larger intrinsic contrast range. This is a direct, concrete instance of the equipment differentiation theme Chapter 15 develops at full economic scale.

---

## Part 6: A Worked Gas Panel Architecture Timing Comparison

### 6.1 Shared vs. Dedicated Delivery Path Timing

Extending Chapter 3, Section 5's transition overhead calculation, consider the specific contribution of gas panel architecture choice (Section 3.2) to per-transition purge time. A shared delivery path (single gas line serving both chemistry families sequentially) must fully purge residual halogen species before fluorocarbon chemistry flows, and vice versa, with purge time scaling with shared-line internal volume. A dedicated-path architecture (separate lines per chemistry family, converging only at a point very close to the chamber inlet) requires purging only the much smaller shared final segment.

### 6.2 Illustrative Calculation

**Shared path illustrative case:** shared line volume $V_{line} = 50\ \text{cm}^3$, purge flow rate $Q_{purge}=500\ sccm$, requiring illustratively 5 full volume exchanges for adequate clearing confidence:

$$t_{purge,shared} \approx \frac{5 \times V_{line}}{Q_{purge}} \times \text{(unit conversion factor)} \approx 3\text{-}4\ s \text{ (order of magnitude, consistent with Chapter 3's illustrative 3s per-transition estimate)}$$

**Dedicated path illustrative case:** shared final segment volume reduced to $V_{line,shared}=8\ \text{cm}^3$ (dedicated lines up to a point close to the chamber inlet, per Section 3.2's architecture):

$$t_{purge,dedicated} \approx \frac{5\times8}{500} \times \text{(unit conversion factor)} \approx 0.5\text{-}0.6\ s$$

### 6.3 Reapplying This to the Full-Stack Transition Overhead Total

Applying this illustrative roughly 6x reduction in per-transition purge time to Chapter 3, Section 5.2's full 256-transition, 128-layer-pair calculation:

$$t_{overhead,total,dedicated} \approx 256 \times 0.55\ s \approx 141\ s \approx 2.3\ \text{minutes} \quad (\text{vs. the shared-path estimate of} \approx 12.8\ \text{minutes})$$

This illustrative comparison makes concrete why Section 3.2's dedicated gas panel architecture recommendation is not a minor convenience but a substantial, quantifiable total process time lever — reducing cumulative transition overhead by roughly an order of magnitude in this illustrative scenario, directly addressing the throughput economics concern Chapter 3 raised and Chapter 15 develops into full production economic treatment.

---

## Summary and Forward Look

OPOP reactor requirements build on the general 3D NAND extreme-aspect-ratio reactor architecture baseline (source/bias-decoupled, high-density plasma sources) but add two OPOP-specific demands: finer-grained selectivity control capability, justified by oxide/polysilicon's larger intrinsic selectivity contrast relative to oxide/nitride, and rapid, repeatable chemistry-family switching capability, justified by the dual-chemistry-system requirement Chapter 3 and Chapter 4 established. These additional demands manifest concretely in gas panel/valve architecture, chamber volume optimization, and process control sequencing capability, together explaining why not every ON-optimized platform transfers directly to OPOP use without modification or dedicated qualification.

The next chapter develops gas delivery and byproduct management in full detail for this hybrid chemistry system, extending general 3D NAND gas distribution principles to address the dual-chemistry-family delivery and byproduct removal requirements this chapter has identified at the reactor-architecture level.
