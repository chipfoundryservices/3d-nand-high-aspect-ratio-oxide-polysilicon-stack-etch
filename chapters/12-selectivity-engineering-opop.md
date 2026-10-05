# Chapter 12: Oxide/Polysilicon Selectivity Engineering and Averaged Selectivity Control

## Executive Summary

This chapter develops OPOP selectivity engineering in full quantitative detail, extending the averaged-selectivity framework established generally in 3D NAND literature (time-averaged, full-depth selectivity as the practically relevant metric, distinct from instantaneous single-film selectivity) to oxide/polysilicon's larger intrinsic contrast, doping-dependent tunability (Chapter 11, Part 4's design-lever discussion), and dual-chemistry structure. We quantify the intrinsic contrast magnitude using Chapter 4's bond-energy foundation, develop the chemistry and bias-power levers available to tune it (building on Chapters 3, 5, and 9), and address the breakthrough/stop-layer selectivity requirement OPOP's removal process (Chapter 14) depends on.

---

## Part 1: Quantifying OPOP's Intrinsic Selectivity Contrast

### 1.1 Why Bond Energy Provides a Starting Quantitative Estimate

Chapter 4, Section 6.2 established that Si-Si bonds (~222-310 kJ/mol) are substantially weaker than Si-O bonds (~452 kJ/mol), directly explaining polysilicon's intrinsically faster etch rate relative to oxide under comparable ion-assisted chemical etch conditions. A simplified Arrhenius-type framework relates etch rate ratio to this bond energy difference:

$$\frac{R_{poly}}{R_{ox}} \approx \exp\left(\frac{E_{Si-O} - E_{Si-Si}}{k_B T_{eff}}\right)$$

where $T_{eff}$ is an effective reaction temperature reflecting the ion-assisted activation process (not simply wafer temperature, but a parameter encompassing the ion-energy-driven activation this book's surface reaction chapters have described), and $E_{Si-O}$, $E_{Si-Si}$ are the respective bond energies.

### 1.2 Illustrative Calculation

Using representative values $E_{Si-O}=452\ kJ/mol$, $E_{Si-Si}=270\ kJ/mol$ (mid-range of Chapter 4's cited range), and an illustrative effective temperature $T_{eff}\approx 2000\ K$ (a representative order-of-magnitude value for ion-assisted plasma surface reactions, substantially above wafer thermal temperature, reflecting the non-thermal, ion-energy-driven activation process):

$$\frac{R_{poly}}{R_{ox}} \approx \exp\left(\frac{(452-270)\times10^3}{8.314\times2000}\right) = \exp\left(\frac{182000}{16628}\right) = \exp(10.95) \approx 5.7\times10^4$$

### 1.3 Why This Figure Should Be Treated as Illustrative, Not Predictive

This illustrative calculation produces an extremely large ratio, considerably larger than the general selectivity ratios (commonly in the few-to-tens-of-1 range) actually observed in production halogen-chemistry polysilicon etch against oxide — a direct signal that the simplified Arrhenius framework, while useful for illustrating *why* a large intrinsic contrast should be expected directionally, substantially overstates its magnitude by neglecting the many other rate-limiting factors (ion flux availability, Chapter 10's transport limitations, passivation layer effects, Chapter 4, Section 3.2) that moderate the realized etch rate ratio well below what bond-energy differences alone would predict. This chapter uses this calculation specifically to establish the *qualitative, mechanistic* expectation of a large intrinsic contrast, consistent with Chapter 1's preview and Chapter 4's bond-energy discussion, while deferring to empirically measured selectivity values (Section 1.4) for any quantitative process design purpose.

### 1.4 Representative Empirically-Grounded Selectivity Range

Based on general logic polysilicon gate etch literature's reported oxide/polysilicon selectivity in chlorine/bromine chemistry (typically cited in ranges from roughly 5:1 to 50:1 depending on specific chemistry, bias conditions, and oxide quality), and acknowledging this figure's origin in planar logic applications rather than extreme-AR 3D NAND channel hole etch specifically, this chapter treats 5:1-50:1 as a representative starting bracket for OPOP bulk etch intrinsic selectivity, substantially larger than the near-1:1 (general 3D NAND literature's ON stack) target but far more moderate than Section 1.2's bond-energy-only estimate — reinforcing why direct selectivity measurement under actual extreme-AR OPOP process conditions remains necessary (consistent with Chapter 10's research-agenda framing) rather than relying on either the bond-energy estimate or the planar-logic reference value alone.

---

## Part 2: Suppressing the Intrinsic Contrast for Balanced Bulk Etch

### 2.1 Why Near-Balanced Selectivity Remains the Bulk-Etch Target

Chapter 2, Section 2.1's stepped-sidewall-defect concern (general 3D NAND literature's rationale for near-1:1 bulk-etch selectivity target) applies to OPOP exactly as to ON: a strongly imbalanced bulk etch, with polysilicon etching dramatically faster than oxide at every layer transition, would produce a severely stepped sidewall profile, directly degrading the smooth-sidewall requirement for downstream ONO deposition (general literature's acceptance criteria, unchanged for OPOP per Chapter 1, Section 3.1's structural-equivalence observation).

### 2.2 Chemistry-Based Suppression Levers

Chapter 3's chemistry discussion provides the primary suppression lever: HBr's comparatively gentler, more controllable etch character (Chapter 3, Section 2.2) relative to more aggressive Cl2 chemistry can be weighted more heavily specifically to reduce polysilicon's intrinsic rate advantage, while SF6's modifying role (Chapter 3, Section 2.3) can independently fine-tune overall rate without primarily affecting the oxide/polysilicon ratio — together providing a chemistry-blend-based suppression toolkit analogous in function, though different in specific species, to general 3D NAND literature's fluorocarbon-chemistry-based nitride suppression toolkit.

### 2.3 Bias-Power-Based Suppression (Chapter 9 Revisited)

Chapter 9, Part 2 established bias power as a direct selectivity-modulation lever, since oxide's and polysilicon's differential ion-energy sensitivity (Chapter 4, Section 6's bond-energy-grounded reasoning) means adjusting bias power shifts the realized etch rate ratio. For bulk-etch balanced-selectivity targeting specifically, this suggests operating at a bias power point that minimizes, rather than maximizes, polysilicon's ion-assisted rate advantage over oxide — a specific, quantifiable operating point distinct from whatever bias power might otherwise be chosen purely for profile or throughput reasons, requiring the dual-objective optimization Chapter 7 and Chapter 9 both flagged as necessary for OPOP recipe development.

### 2.4 Doping-Level-Based Suppression (Chapter 11 Revisited)

Chapter 11, Part 4 and Part 6 established doping level as a design lever trading charging mitigation against etch rate (and therefore selectivity). For a process prioritizing bulk-etch selectivity balance over charging mitigation, lighter polysilicon doping (reduced intrinsic etch rate, Chapter 2, Section 3.2) directly narrows the intrinsic contrast Section 1 quantified, at the cost of forfeiting some of Chapter 11's charging-mitigation benefit — a second, independent instance of the general tradeoff structure this book has shown doping level to sit within.

### 2.5 Why These Three Levers Must Be Jointly, Not Independently, Optimized

Because chemistry blend (Section 2.2), bias power (Section 2.3), and doping level (Section 2.4, though fixed at deposition rather than tunable during etch) jointly determine realized selectivity, and because each lever carries its own secondary consequences (chemistry blend affecting profile and transition overhead, Chapter 3; bias power affecting mask erosion and charging, Chapters 5, 7, 11; doping level affecting charging mitigation, Chapter 11), OPOP bulk-etch selectivity targeting is a genuinely multi-variable optimization problem, more heavily constrained than general 3D NAND literature's ON-stack equivalent, which primarily relies on chemistry blend alone (doping not being an available lever for nitride, and bias power's selectivity role being comparatively less central given ON's more moderate intrinsic contrast, Chapter 5, Part 5's control-resolution argument).

---

## Part 3: Averaged Selectivity Across Depth

### 3.1 Extending the General Averaged-Selectivity Framework

General 3D NAND literature's $S_{avg} = \bar{R}_{ox}/\bar{R}_{nit}$ framework (time-averaged etch rate ratio across full stack depth, the practically relevant metric distinct from instantaneous single-layer selectivity) extends directly to OPOP as $S_{avg,OPOP} = \bar{R}_{ox}/\bar{R}_{poly}$, computed across the full depth-dependent etch rate behavior Chapter 10 developed for both layer types independently.

### 3.2 Why OPOP's Depth-Dependent Selectivity Drift May Differ in Magnitude From ON's

Chapter 10, Section 2.3's uncertainty bracket for halogen-species transport parameters means the depth-dependent selectivity drift mechanism general literature identifies (transport attenuation acting with different magnitude on the two materials, shifting $S_{avg}$ from its shallow-feature value as depth increases) carries correspondingly wider uncertainty for OPOP than for the well-characterized ON case. This is a direct, practical consequence of Chapter 10's broader transport-characterization gap, now specifically affecting selectivity prediction rather than only etch-rate prediction.

### 3.3 Why Full-Depth Selectivity Characterization Is Even More Essential for OPOP Than for ON

General 3D NAND literature already establishes full-depth selectivity characterization as necessary (rather than relying on shallow-feature measurements) because of the depth-dependent drift mechanism. Given Section 3.2's wider OPOP-specific uncertainty, this necessity is amplified for OPOP: a shallow-feature-only selectivity characterization risks an even larger, less predictable error when extrapolated to full production stack depth than the equivalent ON-stack extrapolation would carry, reinforcing yet again this book's recurring finding that OPOP process development requires more extensive, more depth-complete empirical characterization than the comparatively better-understood ON baseline.

---

## Part 4: Breakthrough/Stop-Layer Selectivity for OPOP

### 4.1 Why High, Not Balanced, Selectivity Is Required at the Bottom Interface

Consistent with general 3D NAND literature's framework (Section 2.1's bulk-etch target does not apply to the final breakthrough step), the OPOP channel hole etch's final overetch/breakthrough step must achieve deliberately high selectivity of the etch toward whatever sacrificial material remains at the bottom-most layer relative to the underlying stop-layer material, protecting the stop layer during the overetch margin needed for full-wafer clearing.

### 4.2 Why This Step May Be Comparatively Easier for OPOP, Chemistry-Wise

Because Section 1's analysis establishes that oxide/polysilicon's intrinsic contrast is already large before any deliberate suppression (Section 2) is applied, achieving high selectivity *specifically against polysilicon* at the breakthrough step (if the stop layer itself is not polysilicon) may require comparatively less aggressive chemistry adjustment from the bulk-etch baseline than general 3D NAND literature's ON-stack breakthrough step requires relative to its own near-1:1 bulk baseline — essentially, OPOP's bulk-etch suppression work (Section 2) can be partially or fully relaxed at the breakthrough step to recover much of Section 1's large intrinsic contrast "for free," whereas ON's breakthrough step must actively engineer additional selectivity beyond its more moderate intrinsic baseline.

### 4.3 Why This Advantage Is Conditional on Stop-Layer Material Choice

Section 4.2's comparative ease is conditional on the stop-layer material not itself being polysilicon or another material with etch behavior similar to polysilicon's — if the bottom stop-layer or source contact structure (general 3D NAND literature's architectural framework) is itself silicon-based, the favorable intrinsic contrast Section 4.2 describes would not apply, and breakthrough selectivity engineering would instead require the same active, deliberate chemistry adjustment general ON-stack literature's breakthrough step requires. This conditionality should be verified against the specific stack and stop-layer design in question before assuming Section 4.2's advantage applies.

---

## Part 5: A Worked Selectivity Suppression Margin Calculation

### 5.1 Framing the Problem

Suppose process characterization establishes, via Section 1.4's empirical bracket, an unsuppressed intrinsic selectivity $S_{intrinsic}\approx 15{:}1$ (polysilicon etching 15x faster than oxide) at a candidate baseline chemistry and bias condition, and the bulk-etch target per Section 2.1 is $S_{avg}\approx 1.0\pm0.2$ (near-balanced, with modest tolerance).

### 5.2 Required Suppression Factor

$$\text{Required suppression factor} = \frac{S_{intrinsic}}{S_{target}} = \frac{15}{1.0} = 15\times$$

This means the combined effect of chemistry blend adjustment (Section 2.2), bias power tuning (Section 2.3), and any doping-level contribution already fixed at deposition (Section 2.4) must together reduce the realized polysilicon-to-oxide rate ratio by a factor of 15 from the unsuppressed intrinsic baseline to reach the near-balanced target.

### 5.3 Illustrative Allocation Across the Three Levers

| Lever | Illustrative Suppression Contribution | Rationale |
|---|---|---|
| Chemistry blend (HBr-weighting, Section 2.2) | ~4x | Primary, most readily adjustable lever; general polysilicon etch literature supports this general order-of-magnitude contribution from chemistry alone |
| Bias power tuning (Section 2.3) | ~2.5x | Secondary, finer-grained lever per Chapter 9's selectivity-modulation role |
| Doping level (fixed at deposition, Section 2.4) | ~1.5x | Contributes a fixed baseline shift (lighter doping already somewhat reducing intrinsic rate), not dynamically adjustable during etch |

$$\text{Combined suppression} \approx 4\times2.5\times1.5 = 15\times \quad \checkmark$$

### 5.4 Why This Allocation Exercise Is Useful Even Though the Specific Numbers Are Illustrative

This illustrative allocation demonstrates the practical planning value of Section 2.5's multi-lever optimization framing: rather than attempting to achieve a 15x suppression factor from a single lever alone (which Chapter 5's control-resolution argument suggests may exceed what bias power alone can reliably achieve, and which Chapter 3's chemistry-blend limits may similarly constrain for chemistry alone), distributing the required suppression across multiple, independently-characterized levers reduces the precision and range demanded of any single lever, directly informing how a process developer should structure their own characterization and optimization work when faced with a measured intrinsic selectivity value from Section 1.4's bracket.

### 5.5 Why Doping Level's Fixed Contribution Interacts With Chapter 11's Tradeoff

Because Section 5.3 treats doping level's suppression contribution as fixed at deposition (not dynamically adjustable during etch, unlike chemistry and bias power), the specific doping level chosen per Chapter 11's charging-mitigation tradeoff directly determines how much suppression burden the remaining two, dynamically-adjustable levers (chemistry, bias power) must provide. A process developer choosing heavier doping for stronger charging mitigation (Chapter 11, Part 6) correspondingly increases the intrinsic contrast those two remaining levers must suppress, tightening the demands on chemistry blend and bias power precision — a direct, quantitative linkage between Chapter 11's charging chapter and this chapter's selectivity chapter that process developers must resolve jointly, not sequentially, when finalizing an OPOP recipe.

---

## Summary and Forward Look

OPOP's intrinsic oxide/polysilicon selectivity contrast is substantially larger than oxide/nitride's, grounded mechanistically in the Si-Si versus Si-O bond energy difference (though empirically moderated well below naive bond-energy-only estimates), requiring active chemistry, bias-power, and doping-level-based suppression to achieve the near-balanced selectivity target bulk channel hole etch requires for sidewall-quality reasons. This larger intrinsic contrast, conversely, can work favorably at the breakthrough/stop-layer step, potentially easing high-selectivity achievement relative to ON's more moderate intrinsic baseline, conditional on stop-layer material choice. Full-depth selectivity characterization is even more essential for OPOP than for the already-selectivity-characterization-dependent ON case, given the wider transport-parameter uncertainty Chapter 10 identified.

The next chapter turns to staircase etch considerations specific to polysilicon sacrificial layers, extending the general trim-etch cycling framework and compounding-error analysis established in 3D NAND literature to address where OPOP's materials and chemistry differences (Chapters 2-4) specifically affect staircase formation.
