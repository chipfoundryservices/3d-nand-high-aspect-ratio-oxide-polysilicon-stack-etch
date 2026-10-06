# Appendix C: Standard Operating Procedures

This appendix consolidates representative SOP outlines for OPOP's three major etch-adjacent processes, illustrating how this book's chapter content maps onto an actual production procedure structure. These outlines are illustrative, process-flow-level summaries, not a substitute for tool-specific, fully validated production SOPs.

---

## C.1 OPOP Channel Hole Etch SOP Outline

**Scope:** Full-stack OPOP channel hole etch, from hard mask open through breakthrough/overetch, per Chapters 2-12.

1. **Incoming wafer verification.** Confirm stack deposition completion, incoming wafer bow against specification, and polysilicon doping-level/grain-structure characterization consistency (Chapter 2) prior to loading.
2. **Chamber readiness check.** Confirm combined-exposure chamber conditioning state (Chapter 8) and cumulative dual-chemistry transition count since last clean within qualified range.
3. **Mask open step.** Execute mask-open recipe under fluorocarbon chemistry (oxide-layer-equivalent conditions, per Chapter 7, Part 2).
4. **Bulk etch sequence — oxide layer.** Execute oxide-layer bulk etch recipe (fluorocarbon chemistry, Chapter 7, Part 2 process window).
5. **Chemistry transition.** Execute lockstep gas, bias, and pulsing-parameter transition to polysilicon-layer conditions (Chapter 5, Part 3; Chapter 9, Part 4).
6. **Bulk etch sequence — polysilicon layer.** Execute polysilicon-layer bulk etch recipe (halogen chemistry, Chapter 7, Part 3 process window), targeting near-balanced selectivity per Chapter 12, Part 2.
7. **Repeat steps 4-6** for each layer pair until full stack depth is reached.
8. **Breakthrough/overetch step.** Transition to high stop-layer-selectivity chemistry (Chapter 12, Part 4), monitor endpoint signal (Appendix F) to determine step termination.
9. **Post-etch inspection.** Sample-based cross-sectional CD/profile measurement, with particular attention to charging-related twisting severity (Chapter 11) and grain-boundary-correlated sidewall roughness (Chapter 2, Part 6).
10. **Chamber state update.** Log cumulative transition count and combined-exposure cycle count; schedule combined-exposure-calibrated clean per Chapter 8's cadence framework.

## C.2 OPOP Staircase Trim-Etch Cycle SOP Outline

**Scope:** Single trim-etch cycle within the full OPOP staircase formation sequence, per Chapter 13.

1. **Cycle readiness check.** Confirm mask remaining thickness against the OPOP-specific combined-exposure budget (Chapter 13, Section 2.3).
2. **Mask trim step.** Execute controlled lateral trim per the qualified trim-rate-consistency recipe, verified under combined-exposure conditions (Chapter 13, Part 2).
3. **Chemistry-appropriate vertical etch step.** Execute single-layer-pair vertical etch using fluorocarbon (oxide) or halogen (polysilicon) chemistry as appropriate to the current layer type.
4. **In-line metrology checkpoint** (at OPOP-adjusted frequency, Chapter 13, Section 5.2, given higher illustrative cumulative error relative to ON).
5. **Drift/variance diagnostic.** Distinguish materials-driven variance (polysilicon-layer-correlated) from equipment drift (Chapter 13, Section 5.3) before applying correction.
6. **Repeat** steps 1-5 for the full layer-pair count.

## C.3 OPOP Sacrificial Removal and Word Line Replacement SOP Outline

**Scope:** Full replacement sequence from slit etch through completed metal fill, per Chapter 14.

1. **Slit etch.** Execute trench etch to full stack depth using stop-layer-selective chemistry (Chapter 14, Part 1).
2. **Pre-removal inspection.** Verify slit clearing and dimensional specification.
3. **Sacrificial polysilicon removal.** Execute TMAH-based wet process or halogen-based hybrid process (Chapter 14, Part 2-3) for the qualified duration, including overetch margin per the diffusion-limited lateral removal model (Chapter 14, Part 6); verify complete removal across full block width.
4. **Minimum-support-interval tracking.** Log elapsed time in the unsupported structural interval (Chapter 14, Part 5), referencing the OPOP-specific removal duration characterization rather than assuming ON's hot-phosphoric-acid timing benchmark applies.
5. **Pre-fill surface treatment.** Apply OPOP-specific surface preparation if required (Chapter 14, Section 4.2) to address any TMAH/halogen-removal-specific surface termination differing from hot-phosphoric-acid-exposed ON surfaces.
6. **Barrier/metal fill.** Execute ALD TiN barrier deposition followed by CVD tungsten fill (general 3D NAND literature's framework, materials-choice-independent per Chapter 14, Section 4.1).
7. **Post-fill inspection.** Verify void-free fill, particularly at the lateral extremity farthest from the slit; measure word line resistance uniformity.
8. **Structural integrity verification.** Confirm no block tilting, sagging, or wafer-level warpage interaction occurred during the unsupported interval.

---

*These outlines summarize the process flow logic developed across Chapters 2-14; actual production SOPs include additional tool-specific parameter values, safety procedures, and documentation requirements beyond this book's scope.*
