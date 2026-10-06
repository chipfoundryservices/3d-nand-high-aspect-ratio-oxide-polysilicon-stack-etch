# Appendix D: ARDE / Selectivity Correction Lookup Tables (Oxide/Polysilicon)

This appendix consolidates the aspect-ratio-indexed and selectivity-related illustrative values developed in Chapters 10-12, presented in lookup-table form. As Chapter 10 emphasizes, halogen-species values in this appendix carry wider characterization uncertainty than the fluorocarbon-species values; brackets are given where this book's analysis identified genuine uncertainty rather than a single point estimate.

---

## D.1 Transport Probability Comparison — Fluorocarbon (Oxide) vs. Halogen (Polysilicon, Bracketed)

Derived from Chapter 10, Part 1-2's modified Clausing model

| Aspect Ratio | Oxide (Fluorocarbon, $\gamma=0.25$-$0.30$) | Polysilicon (Halogen, Bracketed $\gamma=0.15$-$0.35$) |
|---|---|---|
| 20 | 0.290-0.335 (illustrative) | 0.279-0.421 (wide bracket) |
| 40 | 0.170-0.200 | 0.169-0.264 |
| 55 | 0.129-0.145 | 0.113-0.202 |
| 80 | 0.090-0.102 | 0.0844-0.143 |

## D.2 Illustrative Sensitivity Table — Combined Stack Rate Impact of Halogen $\gamma$ Uncertainty

Derived from Chapter 10, Part 6

| Parameter | Low End ($\gamma=0.35$) | High End ($\gamma=0.15$) | Ratio |
|---|---|---|---|
| $K(55,\gamma)$ for polysilicon layers | 0.113 | 0.202 | 1.79× |

## D.3 Intrinsic Selectivity Contrast Reference

Derived from Chapter 12, Part 1

| Basis | Illustrative Oxide/Polysilicon Ratio |
|---|---|
| Bond-energy-only Arrhenius estimate (Chapter 12, Section 1.2) | ~$5.7\times10^4$ (illustrative upper-bound, not production-representative) |
| Logic polysilicon gate etch literature reference range (Chapter 12, Section 1.4) | 5:1 to 50:1 |

## D.4 Illustrative Selectivity Suppression Lever Allocation

Derived from Chapter 12, Part 5, for an illustrative 15:1 required suppression factor

| Lever | Illustrative Contribution |
|---|---|
| Chemistry blend (HBr-weighting) | ~4× |
| Bias power tuning | ~2.5× |
| Doping level (fixed baseline) | ~1.5× |

## D.5 Staircase Cumulative Error Comparison

Derived from Chapter 13, Part 3, for an illustrative 128-layer-pair stack

| Stack Type | Illustrative Cumulative Random Error |
|---|---|
| ON (equivalent, single error source) | ~32 nm |
| OPOP (oxide + polysilicon materials-driven variance) | ~38.9 nm |

## D.6 Lateral Removal Time Comparison

Derived from Chapter 14, Part 6, for an illustrative 3µm block half-width

| Removal Chemistry | Illustrative Clearing Time |
|---|---|
| Hot H3PO4 (ON reference) | ~90 s |
| TMAH (OPOP candidate, illustrative) | ~150 s |

---

*These tables are derived directly from the simplified, illustrative models presented in Chapters 10-14. Production process characterization requires empirical measurement of the equivalent quantities on the specific reactor, chemistry, and stack combination in use, per this book's repeated caution against treating illustrative values as production-ready specifications.*
