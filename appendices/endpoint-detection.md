# Appendix F: Endpoint Detection Calibration for Oxide/Polysilicon Transitions

This appendix develops endpoint detection methodology specific to OPOP's oxide/polysilicon layer transitions, extending the general multi-layer stack endpoint detection framework established in 3D NAND literature and referenced throughout this book (Chapter 4, Section 5.2; Chapter 12, Section 4.3).

---

## F.1 Why Endpoint Detection Matters Specifically at OPOP's Chemistry Transitions

General 3D NAND literature establishes endpoint detection as necessary for the final breakthrough/overetch step, bounding overetch duration against stop-layer damage. For OPOP, an additional endpoint detection application arises at every oxide/polysilicon layer transition within the bulk etch itself: because Chapter 4, Section 5.2 established that OPOP's reaction-layer transition is more discontinuous than ON's oxide/nitride transition, the resulting optical emission or electrical signal change at each OPOP transition is likely more pronounced and more readily detectable, offering a potential tool for precise per-layer transition timing control — directly relevant to minimizing the necking-defect-analog risk Chapter 3, Section 3.2 and Chapter 11, Section 3.4 both flagged.

## F.2 Optical Emission Spectroscopy for OPOP Transitions

**Representative monitored species/wavelengths relevant to OPOP's dual-chemistry system:**

| Species | Approx. Wavelength | Relevance |
|---|---|---|
| SiCl (chlorine-chemistry polysilicon etch byproduct signal) | ~280 nm (representative) | Polysilicon-layer-specific signal, rises when polysilicon etch is active |
| SiBr (bromine-chemistry byproduct signal) | ~290 nm (representative) | Polysilicon-layer-specific signal when HBr chemistry is weighted |
| SiF (oxide-layer fluorine chemistry byproduct signal) | ~440 nm (general 3D NAND literature reference) | Oxide-layer-specific signal |
| CN/N2 (fluorocarbon/oxide chemistry byproduct) | ~337-391 nm | Secondary oxide-layer chemistry indicator |

**Why the transition signal should be more pronounced for OPOP:** because the monitored species themselves change character entirely at an OPOP layer transition (fluorine-chemistry signals dropping to near-zero as halogen-chemistry signals rise, and vice versa, rather than general 3D NAND literature's more subtle shift within a single, continuous fluorocarbon-chemistry-species framework), the signal-to-noise ratio for detecting the transition itself should be favorable, consistent with Chapter 4, Section 5.2's qualitative prediction.

## F.3 Calibration Procedure, Extended for Dual-Chemistry Transitions

1. Run a representative, fully-characterized wafer (known-good clearing and transition behavior from destructive cross-section verification) while recording OES data continuously, including through multiple oxide-to-polysilicon and polysilicon-to-oxide transitions.
2. Identify the specific wavelength(s) and signal transition pattern most clearly, reproducibly marking each transition type (oxide-to-polysilicon versus polysilicon-to-oxide, which may show distinct signatures given the directional asymmetry Chapter 6, Section 2.2 flagged).
3. Establish per-transition-type trigger thresholds, since oxide-to-polysilicon and polysilicon-to-oxide transitions may require independently calibrated detection criteria rather than a single, symmetric threshold.
4. Validate across a statistically meaningful sample of production-representative wafers, specifically verifying consistency across both transition directions and across the full stack depth (given Chapter 10's transport-parameter uncertainty, verifying that transition detection reliability does not degrade differently with depth for the two chemistry families).

## F.4 Using Transition Detection for Lockstep Parameter Switching Verification

Chapter 5, Section 3.4 and Chapter 9, Part 4 both recommend lockstep switching of gas chemistry, bias power, and pulsing parameters at each layer transition. Reliable, per-transition endpoint/transition detection (Section F.2-F.3) provides a direct verification tool for confirming this lockstep switching is actually occurring with correct timing in production — detecting a transition signal substantially earlier or later than the commanded parameter switch would indicate a process control sequencing error (Chapter 5, Section 3.4's reliability concern) worth investigating, distinct from a genuine process drift issue.

## F.5 Breakthrough/Stop-Layer Endpoint for OPOP

Consistent with Chapter 12, Part 4's finding that OPOP's final breakthrough step may benefit from the already-large intrinsic oxide/polysilicon contrast (if the stop layer is not itself silicon-based), the breakthrough endpoint signal — marking transition from the final sacrificial layer to the stop-layer material — should be calibrated using the general procedure in Section F.3, with particular attention to Chapter 12, Section 4.3's conditionality: if the stop layer is itself polysilicon or another silicon-based material, the endpoint signal contrast may be considerably more subtle than a stop layer with a more distinct composition, requiring correspondingly more careful calibration.

## F.6 Calibration Maintenance Under Combined-Exposure Chamber Drift

Because Chapter 8 established that OPOP chambers experience combined-exposure conditioning and drift behavior distinct from single-chemistry-family ON chambers, endpoint detection trigger thresholds calibrated per Section F.3 must be periodically reverified against current combined-exposure chamber state (Chapter 8, Part 4's two-track chamber matching framework), rather than assuming a single-chemistry-family drift characterization adequately captures OPOP's combined-exposure drift behavior.

---

*This appendix summarizes endpoint detection methodology specific to OPOP's dual-chemistry transitions. Specific wavelength selection, threshold values, and calibration procedures are tool- and process-specific and must be established through the empirical procedure outlined in Section F.3 for each production reactor and recipe combination.*
