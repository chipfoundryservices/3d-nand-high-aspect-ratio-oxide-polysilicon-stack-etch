# Chapter 10: ARDE and Transport Physics in Oxide/Polysilicon Stacks vs. Oxide/Nitride

## Executive Summary

This chapter develops the quantitative comparison this book has anticipated since Chapter 1's preview table: how aspect-ratio-dependent etching (ARDE) actually plays out differently in OPOP stacks relative to the ON baseline established in general 3D NAND literature. We apply the general Knudsen transport probability and ion trajectory attenuation framework (established generally, with its mathematical structure fully derived in general 3D NAND literature) to OPOP's halogen-chemistry polysilicon layers, using the materials and chemistry foundation from Chapters 2-4, and identify where OPOP's transport behavior genuinely diverges from the ON case versus where the general framework transfers with only parameter substitution.

---

## Part 1: Applying the General Transport Framework to Halogen Species

### 1.1 The General Framework, Restated

General 3D NAND literature derives a Knudsen transport probability $K(AR,\gamma) \approx \frac{1}{1+\frac{3}{8}AR\cdot\frac{\gamma}{1-\gamma/2}}$ relating transport probability to aspect ratio and species-specific sidewall sticking/reaction probability $\gamma$, alongside an ion trajectory transmission fraction $f_{ion}(AR)$ depending on angular ion distribution and aspect ratio. Both expressions are general — they do not assume any specific chemistry — and apply to halogen species transport exactly as to fluorocarbon species, provided the correct species-specific $\gamma$ values are used.

### 1.2 Why Halogen Species $\gamma$ Values Require Independent Characterization

Chapter 6, Section 4.1 flagged that halogen species transport parameters cannot be assumed equivalent to fluorocarbon species values. This chapter addresses the comparison directly: Cl and Br atoms, and their SiCl4/SiBr4 reaction products, interact with chamber and feature sidewalls through different physisorption/chemisorption energetics than F and CFx species (Chapter 4, Section 6's bond energy data providing partial grounding), and no general 3D NAND literature source characterizes these values directly, since that literature's treatment is fluorocarbon-chemistry-specific.

### 1.3 A Reasoned Estimate, Pending Direct Characterization

In the absence of directly published halogen-species $\gamma$ values for this specific application, this chapter offers a reasoned, hypothesis-level estimate for illustrative purposes, grounded in two considerations: first, Chapter 4, Section 3.1-3.2 established that polysilicon's halogen chemistry is deliberately chosen (over fluorine) specifically because it is *less* aggressively, spontaneously reactive toward silicon than fluorine is — suggesting halogen species sidewall sticking probability may be somewhat *lower* than fluorine's own sticking probability on an oxide or nitride surface, all else equal; second, SiBr4's larger molecular size (Chapter 3, Appendix A data) relative to SiCl4 or SiF4 suggests comparatively higher geometric collision cross-section, a competing consideration that could favor higher effective sticking probability. These two considerations point in different directions, and this chapter treats the net halogen-species $\gamma$ value as genuinely uncertain pending direct experimental characterization — a limitation this book states explicitly rather than presenting an unfounded, falsely precise estimate.

---

## Part 2: Illustrative Comparative ARDE Table

### 2.1 Framing the Comparison

Given Section 1.3's acknowledged uncertainty, this section presents an illustrative comparison using a *range* of plausible halogen-species $\gamma$ values bracketing general 3D NAND literature's fluorocarbon-species reference values, rather than a single, falsely precise point estimate, directly extending the general transport probability table structure established in that literature's own appendix-level reference tables.

### 2.2 Illustrative Transport Probability Comparison at AR=55 (128-Layer-Pair-Equivalent Single-Tier Target)

| Species Category | Illustrative $\gamma$ Range | $K(55,\gamma)$ Range |
|---|---|---|
| Fluorocarbon (oxide layers, general 3D NAND literature reference value) | 0.25-0.30 | 0.145-0.129 (using Chapter 10-equivalent general literature's formula) |
| Halogen (polysilicon layers, this chapter's bracketed estimate) | 0.15-0.35 (deliberately wide bracket per Section 1.3's uncertainty) | 0.202-0.113 |

### 2.3 Why This Wide Bracket Is the Honest, Useful Output of This Analysis

The halogen-species bracket in Section 2.2 overlaps substantially with, and extends somewhat on both sides of, the fluorocarbon reference range — meaning this chapter's analysis cannot responsibly claim halogen species transport at extreme aspect ratio is definitively more or less favorable than fluorocarbon species transport without further characterization. This is itself a useful and important finding: it tells process developers and researchers that OPOP's polysilicon-layer transport behavior at extreme aspect ratio is not safely assumed to mirror ON-stack nitride-layer behavior, in either direction, and that dedicated characterization (per Section 1.2's recommendation) is a necessary, not optional, step before OPOP processes can be confidently extrapolated to new, higher-aspect-ratio generations using purely analytical means.

---

## Part 3: Ion Trajectory Attenuation — Why This Component Transfers More Directly

### 3.1 Why Ion Trajectory Physics Is Less Chemistry-Dependent

Unlike Knudsen-regime neutral transport (Part 1-2, strongly species-specific via $\gamma$), ion trajectory attenuation ($f_{ion}(AR)$, general 3D NAND literature's error-function model) depends primarily on sheath physics, ion angular distribution, and feature geometry — factors that are substantially less sensitive to which specific ion species (Ar+, Cl+, Br+, or F+/CFx+) is involved, compared to neutral transport's strong species-dependence via sticking probability. This means the general $f_{ion}(AR)$ framework and its associated illustrative values (general literature's reference table) transfer to OPOP's polysilicon-layer ion trajectory behavior with substantially less uncertainty than the neutral transport comparison in Parts 1-2 required.

### 3.2 Why Ion Mass Differences Still Warrant a Minor Caveat

Chapter 5's general sheath voltage framework ($J \propto V_s^{3/2}/\sqrt{M}$-type scaling, general literature's Child-Langmuir-like relationship) does depend on ion mass $M$, meaning heavier halogen-derived ions (Cl+, Br+, or ionized SiCl4/SiBr4 fragments) versus lighter fluorocarbon-derived ions could produce modestly different sheath acceleration behavior at identical applied bias power — a second-order effect relative to Part 1-2's neutral transport uncertainty, but one that should be incorporated into full reactor-specific characterization (Chapter 7's dual-process-window framework) rather than assumed negligible without verification.

---

## Part 4: Combined Rate Model Applied to OPOP's Dual-Chemistry Structure

### 4.1 Extending the General Combined Rate Expression

General 3D NAND literature's combined rate expression, $R_{etch}(AR) \approx k \cdot \Gamma_{n,0} \cdot K(AR,\gamma) \cdot f(\Gamma_{i,0}\cdot f_{ion}(AR), E_i)$, applies independently within each layer type's etch interval, using that layer type's own chemistry-specific $\Gamma_{n,0}$, $\gamma$, and reaction-rate parameters $k$ and $f$. For OPOP, this means two independently parameterized versions of this same general expression — one for oxide intervals (using general literature's established fluorocarbon parameters), one for polysilicon intervals (using Part 1-2's halogen-chemistry parameters, bracketed per Section 2.2's uncertainty) — rather than the single, consistently-parameterized expression a general ON-stack treatment would use throughout.

### 4.2 Why Total Stack Etch Behavior Requires Combining Both Models Depth-wise

Total channel hole etch time and depth-dependent rate behavior across a full OPOP stack is the layer-by-layer composition of these two independently parameterized rate models, applied sequentially as the etch front transits alternating oxide and polysilicon layers at progressively increasing aspect ratio — directly analogous in structure to how general 3D NAND literature's single-chemistry-family model is applied across an ON stack's alternating oxide/nitride layers, but now requiring two distinct parameter sets rather than one consistent set with only blend-ratio variation.

### 4.3 Why This Compounds the Uncertainty Discussed in Section 2.3

Because Section 2.2-2.3 established genuine uncertainty in the halogen-species transport parameters, and because this uncertainty propagates through every polysilicon-layer interval's contribution to total stack etch time and depth-dependent behavior (Section 4.2), OPOP process developers should expect correspondingly wider uncertainty bands in predicted total etch time and depth-dependent profile behavior than an equivalent ON-stack prediction would carry, using purely analytical extrapolation methods — reinforcing, from the transport-physics side, Chapter 1's broader observation that OPOP integration carries a less mature, less extensively characterized technical foundation than the dominant ON approach.

---

## Part 5: Qualitative ARDE Severity Comparison, Pending Full Characterization

### 5.1 What Can Be Stated With Reasonable Confidence

Despite Section 2.3's acknowledged quantitative uncertainty, several qualitative conclusions can be stated with reasonable confidence, grounded in mechanisms established in Chapters 2-4 rather than requiring the uncertain $\gamma$ value itself:

- OPOP's dual-chemistry structure introduces additional, layer-type-specific transport characterization burden beyond what a single-chemistry ON stack requires (Section 4.3), independent of whether halogen or fluorocarbon transport proves more or less favorable in absolute terms.
- Polysilicon's grain-structure and doping-dependent reactivity (Chapter 2) introduces materials-driven etch rate variability with no ON-stack transport-model analog, meaning even a well-characterized mean $\gamma$ value for polysilicon layers would still carry additional variance beyond what oxide's materials-invariant transport behavior exhibits.
- The ion trajectory attenuation component (Part 3) is less uncertain than the neutral transport component (Parts 1-2), meaning profile-defect mechanisms primarily driven by ion trajectory behavior (Chapter 11's bowing/twisting treatment) can be analyzed with somewhat more confidence by direct extension of general 3D NAND literature's framework than etch-rate predictions primarily driven by neutral transport can.

### 5.2 Why This Chapter Models Honest Uncertainty Rather Than Resolving It by Assumption

This chapter has deliberately avoided resolving Section 1.3's halogen-species transport parameter uncertainty through unfounded assumption, instead presenting a bracketed range and explaining the reasoning and limitations behind it. This reflects a core principle this book maintains throughout: OPOP's technical literature base is genuinely less mature than ON's, and a credible, professionally useful treatment of this topic must represent that immaturity honestly, pointing toward the specific characterization work (Section 1.2, Section 1.3) a reader would need to perform or commission to resolve it for their own specific reactor and chemistry combination, rather than presenting a confident-sounding but unsupported numerical claim.

---

## Part 6: A Worked Sensitivity Analysis Across the Uncertainty Bracket

### 6.1 Why Sensitivity Analysis Is the Right Tool for This Uncertainty

Given Section 2.3's acknowledged wide $\gamma$ bracket, the appropriate analytical response is not to pick a single point value and proceed as if certain, but to perform sensitivity analysis across the full bracket, identifying which downstream process decisions are robust across the entire plausible range and which are sensitive enough to the specific value that characterization must be completed before those decisions can be made with confidence.

### 6.2 Illustrative Sensitivity Calculation

Using Section 2.2's bracketed $K(55,\gamma)$ range of 0.113-0.202 for polysilicon layers, consider the combined-stack relative etch rate implication (extending Chapter 10-equivalent general literature's combined illustrative model) at this single aspect ratio:

| Parameter | Low End of Bracket ($\gamma=0.35$) | High End of Bracket ($\gamma=0.15$) | Ratio (High/Low) |
|---|---|---|---|
| $K(55,\gamma)$ for polysilicon layers | 0.113 | 0.202 | 1.79× |
| Illustrative polysilicon-layer etch time contribution (relative) | Longer (slower transport-limited rate) | Shorter (faster transport-limited rate) | ~1.79× difference |

### 6.3 Interpreting the Sensitivity

A roughly 1.8x difference in polysilicon-layer transport-limited etch rate between the bracket's two ends is a substantial swing — large enough that total stack etch time predictions, mask erosion budget calculations (Chapter 7, Part 6, which depend on per-layer-type etch duration), and etch-stop risk margin assessments (extending general 3D NAND literature's etch-stop framework) could each shift meaningfully depending on where within this bracket the true, characterized value actually falls. This is the quantitative demonstration of why Section 1.2's recommended direct characterization is not an optional refinement but a precondition for confident OPOP process economics and risk assessment at the aspect ratios modern 3D NAND generations require.

### 6.4 Which Decisions Are Robust Regardless of Where in the Bracket the True Value Falls

Despite Section 6.3's sensitivity, certain qualitative conclusions from Part 5.1 remain valid across the *entire* bracket: dual-chemistry transition overhead (Chapter 3, Chapter 5) is present and significant regardless of the specific $\gamma$ value; polysilicon's materials-driven variability (Chapter 2) adds variance beyond any single characterized mean value; and the general architectural requirement for source/bias-decoupled reactors with fine selectivity control (Chapter 5) holds regardless of exactly how transport-limited polysilicon-layer etch proves to be. Distinguishing bracket-sensitive conclusions (Section 6.3) from bracket-robust conclusions (this section) is itself a useful output of this sensitivity analysis, helping process developers prioritize which uncertainties must be resolved before proceeding versus which engineering decisions can proceed with confidence today.

---

## Part 7: Research Priorities for Resolving This Chapter's Open Questions

### 7.1 A Prioritized List

Given this chapter's identified uncertainties, the following characterization work would most directly resolve the open questions raised:

1. **Direct measurement of Cl/Br/SiCl4/SiBr4 sidewall sticking probability** in representative extreme-AR test structures, using methods analogous to those general 3D NAND literature describes for characterizing fluorocarbon species $\gamma$ values (e.g., comparing blanket-film and patterned-structure etch rates across a range of test aspect ratios to extract transport probability empirically).
2. **Ion mass-dependent sheath acceleration characterization** (Section 3.2's minor caveat) across the specific ion species mix present in Cl2/HBr/SF6-blended plasmas, to quantify whether this second-order effect meaningfully affects practical process window prediction.
3. **Grain-structure and doping-level-resolved etch rate characterization** (extending Chapter 2's materials treatment into the transport-physics domain) to separate materials-driven variance from pure transport-physics variance in observed polysilicon-layer etch rate data.
4. **Direct comparative test structure studies** etching matched ON and OPOP stacks under equivalent reactor and aspect ratio conditions, to validate or correct this chapter's qualitative, mechanism-grounded comparative claims (Part 5.1) against direct empirical comparison.

### 7.2 Why This Book Documents Open Questions Rather Than Only Settled Answers

Consistent with this book's stated audience (industry researchers among its primary readers, per the Preface), this chapter's explicit identification of open, uncharacterized questions is intended as a genuine contribution in its own right — a research agenda, not merely a gap to be apologized for. Readers in a position to perform or commission the characterization work outlined in Section 7.1 are positioned to make a documented, citable contribution to a technical area this book has shown to be genuinely less mature than the dominant ON approach's extensively characterized literature base.

---

## Summary and Forward Look

OPOP channel hole etch ARDE behavior extends the general Knudsen transport probability and ion trajectory attenuation framework established in 3D NAND literature, but requires independent, currently less-characterized parameters for halogen-species neutral transport specifically, while ion trajectory attenuation transfers with comparatively less uncertainty. The combined rate model for a full OPOP stack requires two independently parameterized versions of the general rate expression, compounding transport parameter uncertainty across the many polysilicon-layer intervals a full stack etch traverses, and reinforcing this book's broader finding that OPOP's technical and characterization maturity lags the dominant ON approach.

The next chapter addresses a related but distinct physics question this chapter's ion trajectory discussion has set up: how charging behaves differently in OPOP stacks given polysilicon's semiconducting nature, extending Chapter 2, Section 3.4's materials-level observation into the full profile-defect-mechanism treatment this book's analysis has been building toward.
