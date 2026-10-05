# Chapter 11: Charging and Profile Defects — The Semiconducting Sidewall Problem

## Executive Summary

This chapter develops the physics this book has flagged since Chapter 1's preview table and Chapter 2, Section 3.4's materials-level grounding: how differential charging at extreme aspect ratio behaves differently when the sacrificial sidewall is semiconducting (polysilicon) rather than fully dielectric (nitride, general 3D NAND literature's treatment). We extend the general charging mechanism (ion flux depositing net positive charge at a feature's bottom, faster than comparatively isotropic electron flux can neutralize it, general literature's established framework) to account for polysilicon's doping-dependent conductivity providing a partial charge dissipation pathway, and examine how this changes bowing, twisting, and necking defect severity relative to the ON baseline.

---

## Part 1: The General Charging Mechanism, Revisited

### 1.1 Why Charging Occurs at Extreme Aspect Ratio

General 3D NAND literature establishes that in a fully dielectric feature, ions arriving at the bottom of an extreme-aspect-ratio hole deposit net positive charge there, since dielectric sidewalls and bottom surfaces have no bulk conduction pathway to redistribute or neutralize this charge, while electrons' more isotropic angular distribution means they reach the bottom of a deep, narrow feature in systematically smaller quantity than directionally-constrained ions do. This imbalance accumulates into a local positive charge concentration that deflects subsequently arriving ions, producing the self-reinforcing trajectory distortion general literature identifies as a primary driver of twisting and, in some regimes, bowing.

### 1.2 Why This Mechanism Assumes a Fully Insulating Sidewall

The general mechanism's self-reinforcing character (Section 1.1) depends on accumulated charge *remaining* localized at the point of deposition long enough to meaningfully deflect subsequent ion trajectories — a direct consequence of the sidewall's insulating nature preventing charge from redistributing or dissipating elsewhere. This chapter's central question is what changes when this insulating-sidewall assumption no longer holds.

---

## Part 2: How a Semiconducting Sidewall Changes the Picture

### 2.1 Partial Charge Dissipation via Bulk Conduction

At any depth where the channel hole sidewall is currently polysilicon (a sacrificial layer interval, as opposed to an oxide layer interval, Chapter 1's structural framework), accumulated charge at or near that sidewall location has, in principle, a conduction pathway through the polysilicon's own bulk material — a pathway entirely absent for a dielectric nitride or oxide sidewall. Chapter 2, Section 3.4 established that this conduction pathway's effectiveness depends directly on the polysilicon's doping-set conductivity: more heavily doped layers provide a more effective dissipation pathway, lightly doped layers provide a correspondingly weaker one.

### 2.2 Why Dissipation Is "Partial," Not Complete

Several factors limit how completely this conduction pathway neutralizes accumulated charge, even for well-doped polysilicon:

**Finite conductivity, not superconductivity.** Even heavily doped polysilicon has finite resistivity, meaning charge dissipation proceeds at a finite rate (an RC-type time constant, Section 2.3) rather than instantaneously — if the charging accumulation rate (set by ion flux, general literature's framework) exceeds the dissipation rate this finite conductivity provides, net charge accumulation can still occur despite the available pathway.

**Spatially localized conduction only at polysilicon-layer depths.** The conduction pathway Section 2.1 describes exists only where the sidewall is currently polysilicon. At oxide-layer depths within the same feature, the sidewall remains fully insulating, meaning charge accumulated at or migrating toward an oxide-layer depth has no equivalent dissipation pathway — the mitigation this chapter describes is depth-dependent and intermittent along the feature's length, not a uniform, continuous benefit throughout the full stack depth.

**Native oxide/oxyhalide surface layer resistance.** Chapter 4, Section 3.2 established that polysilicon's own sidewall passivation mechanism relies on a thin silicon oxyhalide layer, which, being itself a thin dielectric or near-dielectric film, interposes some additional resistance between the plasma-exposed surface and the bulk conducting polysilicon beneath it — meaning the conduction pathway Section 2.1 describes is not a direct, unimpeded connection to bulk polysilicon conductivity, but one moderated by this thin surface passivation layer's own, generally much higher, resistance.

### 2.3 A Simplified RC Time Constant Framing

The charge dissipation process described in Section 2.1-2.2 can be framed, to a first approximation, as an RC (resistance-capacitance) discharge problem: accumulated surface charge (capacitive, at the oxyhalide/plasma interface) discharges through the series combination of the oxyhalide layer's resistance and the bulk polysilicon's resistance (itself dependent on doping level, Chapter 2, Section 3.2) to whatever reference potential the bulk polysilicon layer, connected through the rest of the not-yet-removed sacrificial stack, effectively presents. A faster RC time constant (lower combined resistance, higher doping) favors more effective, more complete charge dissipation within the timescale relevant to ongoing ion trajectory deflection; a slower time constant provides correspondingly less protective benefit.

---

## Part 3: Consequences for Bowing, Twisting, and Necking

### 3.1 Twisting: Likely Reduced Severity at Polysilicon-Layer Depths

Because general 3D NAND literature identifies charging as a primary twisting amplification mechanism (self-reinforcing lateral trajectory deflection accumulating with depth), and because Section 2's partial dissipation pathway specifically reduces peak accumulated charge at polysilicon-layer depths (to a degree set by doping level and the Section 2.3 RC time constant), twisting accumulation *rate* may be measurably reduced during polysilicon-layer intervals relative to an equivalent-depth oxide-layer interval within the same feature — a depth-dependent, intermittent mitigation rather than a uniform reduction throughout the full stack.

### 3.2 Why This Does Not Simply "Solve" Twisting for OPOP Stacks

Despite Section 3.1's partial mitigation during polysilicon intervals, oxide-layer intervals within the same OPOP stack retain the full, unmitigated charging mechanism general literature describes, meaning twisting accumulated during oxide-layer intervals compounds with whatever twisting (reduced but non-zero, per Section 2.2's "partial" qualifier) occurs during polysilicon intervals. Total accumulated twist by the bottom of a full OPOP stack therefore reflects this alternating, depth-dependent mitigation pattern — plausibly somewhat less severe than an equivalent all-dielectric-sidewall accumulation would produce, but not reduced to the degree a naive "polysilicon solves charging" assumption might suggest.

### 3.3 Bowing: A More Mechanistically Complex Interaction

Chapter 11-equivalent general literature's bowing mechanism (scattered-ion sidewall attack coinciding with locally thinned polymer/passivation protection) interacts with Section 2's partial charge dissipation in a less straightforward way than twisting does, because bowing's charging-related contribution (general literature notes this interaction without fully resolving its magnitude even for the simpler ON case) is itself a less dominant, less well-isolated mechanism relative to the scattered-ion/passivation-thinning contribution. This chapter does not claim a confident, quantified bowing-severity comparison between ON and OPOP stacks; it notes the mechanism exists and plausibly differs, consistent with Chapter 10's broader finding that OPOP's characterization base is less mature than ON's, flagging this as a further specific item for the research agenda Chapter 10, Part 7 outlined.

### 3.4 Necking: Primarily Governed by a Different Mechanism, Likely Less Charging-Sensitive

Because general literature's necking mechanism is primarily a recipe-transition polymer-flux-mismatch effect (Chapter 3, Part 3's chemistry-switching-induced analog for OPOP) rather than a charging-driven mechanism, Section 2's semiconducting-sidewall charge dissipation is not expected to materially affect necking severity one way or the other — necking in OPOP stacks is more directly addressed through the chemistry-transition timing and lockstep pulsing-parameter switching strategies developed in Chapters 3, 5, and 9, rather than through any charging-related consideration this chapter addresses.

---

## Part 4: Doping Level as a Deliberate Charging-Mitigation Design Lever

### 4.1 Why Doping Level Choice Involves a Genuine Tradeoff

Chapter 2, Section 3.2 established that doping level affects etch rate (heavier doping, faster etch) and Section 3.4 established that it affects charge dissipation effectiveness (heavier doping, more effective dissipation per this chapter's Section 2 analysis). A process developer choosing polysilicon doping level for charging-mitigation purposes must therefore weigh this benefit against doping's simultaneous etch-rate consequence, which itself affects selectivity (Chapter 12), process window (Chapter 7), and mask erosion budget (Chapter 7, Part 6) — doping level is not a free, independently optimizable charging-mitigation lever, but one that interacts with essentially every other process parameter this book has developed.

### 4.2 Why This Represents a Genuine OPOP-Specific Design Decision

This doping-level tradeoff (Section 4.1) has no direct ON-stack analog, since nitride's dielectric, non-dopable nature removes this entire design dimension from ON-stack process development. OPOP process developers specifically must make a deliberate, documented doping-level choice weighing charging mitigation against etch rate/selectivity consequences, a decision point unique to this integration path and a further concrete instance of the broader divergence this book has traced from Chapter 1 onward.

---

## Part 5: A Worked RC Discharge Time Constant Estimate

### 5.1 Setting Up the Estimate

Extending Section 2.3's RC framing quantitatively, consider a simplified estimate of discharge time constant for a representative doped polysilicon layer. The characteristic RC time constant for charge dissipation through a resistive path is:

$$\tau_{RC} \approx R \cdot C$$

where $R$ is the effective resistance of the oxyhalide-layer-plus-bulk-polysilicon conduction path, and $C$ is the effective capacitance of the charged surface region.

### 5.2 Illustrative Resistance Estimate

For a representative heavily doped polysilicon layer (resistivity $\rho \approx 1\times10^{-3}\ \Omega\cdot\text{cm}$, a representative value for heavily phosphorus-doped polysilicon) with a conduction path length comparable to the layer thickness (~30nm, Chapter 2-equivalent general stack geometry reference) and a cross-sectional area comparable to the local charged surface patch (illustratively $\sim 10^{-12}\ \text{cm}^2$, representing a small, localized charge accumulation region at the nanometer scale):

$$R \approx \rho \frac{L}{A} \approx 1\times10^{-3} \times \frac{30\times10^{-7}\ \text{cm}}{10^{-12}\ \text{cm}^2} \approx 3\times10^{3}\ \Omega$$

### 5.3 Illustrative Capacitance Estimate

Using a simplified parallel-plate approximation for the thin oxyhalide passivation layer (thickness $d\approx 2nm$, dielectric constant $\kappa\approx 4$, representative of a thin silicon oxide-like passivation film) over the same illustrative area:

$$C \approx \frac{\kappa\epsilon_0 A}{d} \approx \frac{4\times8.85\times10^{-12}\times10^{-16}\ \text{m}^2}{2\times10^{-9}\ \text{m}} \approx 1.77\times10^{-18}\ \text{F}$$

(area converted to $10^{-16}\ \text{m}^2$ from the illustrative $10^{-12}\ \text{cm}^2$ figure above)

### 5.4 Combining Into an Illustrative Time Constant

$$\tau_{RC} \approx R\times C \approx 3\times10^{3}\ \Omega \times 1.77\times10^{-18}\ \text{F} \approx 5.3\times10^{-15}\ \text{s}$$

### 5.5 Interpreting This Result Against Relevant Process Timescales

This illustrative time constant (on the order of femtoseconds) is extraordinarily short relative to any plasma process timescale relevant to this book (RF periods in the nanosecond range, pulsing periods in the microsecond-to-millisecond range, Chapter 9's general framework) — suggesting that, *if* this simplified estimate's assumptions hold (heavily doped polysilicon, thin oxyhalide layer, and the particular localized-area assumption used), charge dissipation through a well-doped polysilicon sidewall could in principle be fast enough to essentially eliminate meaningful charge accumulation at polysilicon-layer depths, a considerably more optimistic conclusion than Section 2.2's qualitative "partial" framing alone might suggest.

### 5.6 Why This Optimistic Result Must Be Treated With Substantial Caution

This result should not be read as a confident, quantitative claim, for several reasons consistent with Chapter 10's broader honesty about this book's characterization limits: the illustrative resistivity, area, and oxyhalide thickness values are representative estimates, not measured quantities for any specific process; the simplified parallel-plate capacitance and single-path resistance model neglects the true three-dimensional geometry of charge accumulation and conduction at a feature sidewall; and most importantly, the relevant comparison is not simply whether $\tau_{RC}$ is short in absolute terms, but whether it is short *relative to the ongoing ion flux arrival rate* that continuously redeposits charge — a dynamic balance problem (charge continuously arriving while continuously dissipating) rather than a simple one-time discharge problem, which this simplified static RC estimate does not fully capture. The genuinely correct conclusion from this section is that the *order of magnitude* suggests dissipation could plausibly be fast relative to many relevant process timescales for sufficiently well-doped material, strongly motivating the direct experimental characterization (comparing measured OPOP and ON twisting severity at matched aspect ratio and process conditions) that Chapter 10, Part 7's research agenda already called for, rather than resolving the question analytically.

---

## Part 6: Doping Level as a Design Point — Illustrative Tradeoff Table

| Doping Level (Illustrative) | Charge Dissipation Effectiveness (Section 2, Part 5) | Etch Rate Consequence (Chapter 2, Section 3.2) | Net Process Implication |
|---|---|---|---|
| Heavily doped ($>10^{20}\ \text{cm}^{-3}$ class) | Most effective dissipation; fastest illustrative $\tau_{RC}$ | Fastest etch rate; largest intrinsic selectivity contrast vs. oxide (Chapter 12) | Best charging mitigation, but demands the most careful selectivity control (Chapter 5, Chapter 9) |
| Moderately doped | Intermediate dissipation effectiveness | Intermediate etch rate | Balanced tradeoff; likely starting point for initial process development absent strong charging or selectivity constraints |
| Lightly doped / near-intrinsic | Weakest dissipation; charging behavior approaches ON-stack-like severity | Slowest etch rate; smallest intrinsic selectivity contrast vs. oxide | Minimal charging benefit; may ease selectivity control burden at the cost of forfeiting this chapter's central OPOP-specific charging advantage |

This table makes Section 4.1's tradeoff concrete: there is no doping level that simultaneously maximizes charging mitigation and minimizes selectivity control burden, and process developers must choose a deliberate point along this spectrum informed by which concern — charging-driven profile defects or selectivity control precision — poses the greater yield risk for their specific stack height, aspect ratio, and reactor capability (Chapter 5).

---

## Summary and Forward Look

Polysilicon's semiconducting nature provides a partial, depth-dependent, doping-level-dependent charge dissipation pathway absent in oxide/nitride stacks' fully dielectric sacrificial layers, likely reducing twisting accumulation rate specifically during polysilicon-layer intervals while leaving oxide-layer intervals' charging behavior unchanged from the general ON-stack mechanism. This mitigation is partial, not complete — limited by finite conductivity, intermittent depth-dependent availability, and the thin oxyhalide passivation layer's own interposed resistance — and its practical magnitude for bowing specifically remains an open, insufficiently characterized question per this book's honest treatment of its own technical maturity limits. Doping level emerges as a genuine, OPOP-specific process design lever for charging mitigation, trading directly against etch rate and selectivity consequences with no equivalent decision point in ON-stack process development.

The next chapter develops oxide/polysilicon selectivity engineering in full quantitative detail, building on this chapter's doping-level discussion and Chapter 4's bond-energy foundation to establish how averaged selectivity is actually achieved and controlled across OPOP's dual-chemistry, alternating-layer structure.
