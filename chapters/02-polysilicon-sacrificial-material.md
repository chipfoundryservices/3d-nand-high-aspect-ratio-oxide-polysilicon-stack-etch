# Chapter 2: Polysilicon as a Sacrificial Material — Deposition, Grain Structure, Doping Effects

## Executive Summary

This chapter develops polysilicon's materials science as a sacrificial layer in detail, the direct counterpart to how a general oxide/nitride treatment would develop PECVD nitride's properties. We examine polysilicon deposition methods and their process-rate tradeoffs, the grain structure that results and its etch-rate and stress consequences, dopant incorporation and its effect on both etch chemistry response and electrical behavior (directly relevant to Chapter 11's charging physics), and how these properties collectively diverge from — and in some respects exceed in complexity — the PECVD nitride properties a general 3D NAND reader is already familiar with.

---

## Part 1: Deposition Methods and Process Tradeoffs

### 1.1 LPCVD and PECVD Polysilicon

Polysilicon for OPOP sacrificial stacks is deposited by either low-pressure chemical vapor deposition (LPCVD, typically silane-based, at higher temperature and lower pressure than PECVD) or PECVD (plasma-assisted, lower temperature, higher throughput but generally lower film quality in specific respects relevant to this chapter).

| Attribute | LPCVD Polysilicon | PECVD Polysilicon |
|---|---|---|
| Typical deposition temperature | 580-650°C | 300-450°C |
| Film density/quality | Higher, more consistent grain structure | More variable, process-condition-dependent |
| Deposition rate / throughput | Lower | Higher |
| Thermal budget consumed | Higher (relevant to co-deposited oxide and overall thermal budget planning) | Lower |
| Typical choice for OPOP stacks | Favored where thermal budget permits, for grain structure consistency | Used where throughput or thermal budget constraints favor it |

### 1.2 Why Deposition Method Choice Interacts With Total Stack Thermal Budget

Because an OPOP stack comprises many alternating oxide/polysilicon layer pairs (directly analogous to the layer-pair-count scaling established in general 3D NAND literature for ON stacks), and because LPCVD's higher process temperature is sustained across many sequential deposition cycles, cumulative thermal budget consumed by LPCVD polysilicon deposition can become a first-order process integration concern at high layer counts, potentially affecting other temperature-sensitive aspects of the stack or requiring deliberate thermal budget allocation planning across the full deposition sequence — a consideration with a loose analogy to PECVD nitride's own cumulative deposition time concern in ON stacks (general 3D NAND literature), but driven by thermal budget rather than pure deposition time.

### 1.3 Precursor Chemistry

LPCVD polysilicon typically uses silane (SiH4) pyrolysis; PECVD variants may use silane or disilane (Si2H6) with plasma assistance. Dopant incorporation (Part 3) is typically achieved either in-situ (adding a dopant precursor gas, such as phosphine PH3 or diborane B2H6, during deposition) or via a separate post-deposition implant/anneal step — a choice with direct consequences for the grain structure and doping uniformity discussed in Parts 2-3.

---

## Part 2: Grain Structure and Its Etch Consequences

### 2.1 Why Polysilicon Is Polycrystalline, and Why This Matters

Unlike PECVD nitride, which is amorphous (lacking long-range crystalline order, Chapter 2 of the general ON treatment), as-deposited polysilicon is polycrystalline: composed of many individual crystalline grains with random or process-influenced crystallographic orientation, separated by grain boundaries. This structural difference — amorphous sacrificial material (nitride) versus polycrystalline sacrificial material (polysilicon) — is a direct, materials-level consequence of the sacrificial material choice made in Chapter 1, and it propagates into etch behavior in ways with no direct ON analog.

### 2.2 Grain Size and Etch Rate Variation

Individual grains, with their differing crystallographic orientation relative to the etch direction, can present measurably different etch rates to an anisotropic plasma etch process — a phenomenon well-documented in logic/planar polysilicon gate etch literature, where crystallographic orientation-dependent etch rate variation is a recognized, characterized effect. Grain boundaries themselves, as regions of disrupted atomic bonding and often elevated impurity/dopant segregation (Section 3.3), can etch at yet another distinct rate from either adjacent grain's bulk behavior.

**Consequence for OPOP channel hole etch:** because a channel hole's sidewall at any given polysilicon layer passes through multiple grains and grain boundaries (grain size is typically tens to a few hundred nanometers, comparable to or smaller than channel hole diameter), local etch rate and local sidewall roughness within a single polysilicon layer are not perfectly uniform at the microscopic scale, in a way PECVD nitride's amorphous structure does not produce. This grain-driven microscopic roughness is a distinct contributor to sidewall quality concerns, additive to (and mechanistically distinct from) the general aspect-ratio-driven profile defects (bowing, twisting, necking) that general 3D NAND literature already establishes for both ON and OPOP stacks alike.

### 2.3 Grain Size Control Through Deposition Conditions

Deposition temperature, pressure, and precursor chemistry (Part 1) directly influence resulting grain size and orientation distribution: higher deposition temperature generally favors larger grain size (more complete crystallization during growth), while lower temperature deposition can produce smaller grains or, at sufficiently low temperature, amorphous or microcrystalline silicon that only crystallizes into larger grains during a subsequent thermal anneal step. Process integration teams tune these deposition conditions deliberately, balancing Section 2.2's etch-uniformity consequences against Part 1's thermal budget and throughput considerations, and against the stress consequences developed in Part 4.

---

## Part 3: Doping Effects

### 3.1 Why Polysilicon Sacrificial Layers Are Often Doped

Unlike nitride, which has no meaningful "doping" concept in this context, polysilicon's semiconducting nature means dopant incorporation (typically phosphorus for n-type or boron for p-type) is a deliberate, consequential process choice, affecting both electrical conductivity (directly relevant to Chapter 11's charging physics) and etch chemistry response.

### 3.2 Doping Effects on Etch Rate

Dopant incorporation measurably affects polysilicon's plasma etch rate in halogen chemistry (Chapter 3), a well-established effect from logic polysilicon gate etch literature: heavily doped polysilicon generally etches faster than lightly doped or undoped polysilicon in chlorine-based chemistry, attributed to dopant-induced changes in the Si network's electronic structure and bond energetics affecting the chemisorption and reaction steps underlying the etch mechanism (developed further in Chapter 4). This means a given OPOP stack's etch rate and achievable selectivity against oxide (Chapter 12) depend not only on polysilicon being present, but on its specific as-deposited doping level — a tunable, deliberately engineered process parameter with no direct ON analog, since nitride's etch rate in general 3D NAND literature is not similarly tunable via an equivalent doping mechanism.

### 3.3 Dopant Segregation at Grain Boundaries

Dopant atoms frequently segregate preferentially to grain boundaries during deposition and any subsequent thermal processing, producing locally elevated dopant concentration at boundaries relative to grain interiors. Combined with Section 2.2's grain-boundary etch rate distinction, this means grain boundaries in doped polysilicon can etch at a rate reflecting both their structural disruption and their locally elevated doping — two compounding, not easily separable, contributions to the same observed grain-boundary-correlated etch rate variation.

### 3.4 Doping and Electrical Conductivity

Section 3.1's doping choice directly sets polysilicon's bulk electrical conductivity, which is the materials-level root of Chapter 11's central charging-physics distinction between OPOP and ON stacks: a more heavily doped (more conductive) polysilicon sacrificial layer provides a more effective charge dissipation pathway along the sidewall during plasma etch than a lightly doped (more resistive) polysilicon layer would, meaning the degree of charging mitigation OPOP's semiconducting nature provides (previewed in Chapter 1, Section 6.1's comparison table) is itself a tunable function of deposition-stage doping choice, not a fixed, inherent property of "polysilicon" as an undifferentiated material category.

---

## Part 4: Stress Behavior

### 4.1 Why Polysilicon Stress Differs Mechanistically From Nitride Stress

PECVD nitride's intrinsic stress (general 3D NAND literature) arises primarily from the amorphous network's bond angle and bond length distribution as influenced by deposition plasma conditions. Polysilicon's intrinsic stress arises from a different set of mechanisms specific to its polycrystalline structure: grain boundary volume and structure, any volume change associated with post-deposition crystallization (if deposited amorphous and later annealed, Section 2.3), and dopant-induced lattice strain (Section 3.2's doping effects extending into mechanical, not just electrical/chemical, consequences).

### 4.2 Representative Stress Behavior Comparison

| Attribute | PECVD Nitride (General ON Reference) | Polysilicon (OPOP) |
|---|---|---|
| Primary stress mechanism | Amorphous network bond angle/length distribution, plasma-condition-tunable | Grain structure, crystallization volume change, dopant-induced lattice strain |
| Typical stress magnitude range | -1.2 GPa to +1.0 GPa (highly plasma-condition-tunable) | Generally lower magnitude for LPCVD; more variable for PECVD polysilicon, grain-structure-dependent |
| Primary tuning lever | Deposition plasma frequency, pressure, precursor ratio | Deposition temperature (grain size/crystallization state), dopant concentration, anneal conditions |
| Interaction with removal (Chapter 14) | Stress state irrelevant to a dielectric material's removal chemistry selectivity | Stress state can interact with removal process kinetics, since polysilicon's crystalline structure (and any associated strain) affects local chemical reactivity during removal |

### 4.3 Why This Stress Difference Is a Documented OPOP Adoption Driver

Chapter 1, Section 2.2 flagged stress management profile differences as one documented reason some manufacturers choose OPOP over ON for specific technology generations. This chapter's Section 4.1-4.2 now grounds that claim materially: because polysilicon's stress-tuning levers (deposition temperature, doping, anneal) are mechanistically distinct from nitride's (plasma deposition conditions), a manufacturer whose existing process capability or technology roadmap constraints make nitride stress tuning difficult for a specific stack height target may find polysilicon's different tuning lever set offers an easier path to acceptable net wafer bow (using the same Stoney's-equation-based bow estimation framework established in general 3D NAND stress literature, applied here to polysilicon's distinct stress magnitude and tunability characteristics) — a concrete, materials-grounded instance of Chapter 1's qualitative adoption-driver discussion.

---

## Part 5: Summary Comparison Table — Polysilicon vs. Nitride as Sacrificial Material

| Property Category | PECVD Nitride (ON) | Polysilicon (OPOP) | Chapter Reference |
|---|---|---|---|
| Structural order | Amorphous | Polycrystalline | Section 2.1 |
| Electrical character | Dielectric | Semiconducting, doping-tunable | Section 3.4 |
| Etch rate tuning levers | Chemistry (fluorocarbon C:F ratio), plasma conditions | Chemistry (halogen), doping level, grain structure | Section 3.2 |
| Microscopic sidewall uniformity | Uniform (no grain structure) | Grain/grain-boundary-driven local variation | Section 2.2 |
| Stress tuning levers | Deposition plasma conditions | Deposition temperature, doping, anneal | Section 4.2 |
| Removal chemistry dependency on material state | Minimal (hot H3PO4 selectivity largely state-independent) | Removal kinetics can depend on crystalline/strain state | Section 4.2; Chapter 14 |

---

## Part 6: A Worked Grain-Boundary Etch Rate Variation Estimate

### 6.1 Framing the Problem

To make Section 2.2's grain-boundary etch rate variation concrete, consider a simplified estimate of sidewall roughness contribution from grain structure alone. If grain boundaries etch at a rate enhancement factor $f_{gb}$ relative to grain interiors (a representative illustrative value, consistent with logic polysilicon etch literature's general finding that grain boundaries etch somewhat faster due to structural disruption and dopant segregation, Section 3.3), and grain boundary width is $w_{gb}$ relative to average grain diameter $d_g$, the area-fraction-weighted average etch rate relative to a hypothetical, boundary-free reference is:

$$R_{avg}/R_{grain} \approx 1 + \left(\frac{w_{gb}}{d_g}\right)(f_{gb}-1)$$

**Illustrative calculation:** for $d_g = 100\ nm$ (representative mid-range grain size), $w_{gb} = 3\ nm$ (representative boundary width), and $f_{gb}=1.3$ (a 30% local etch rate enhancement at boundaries, illustrative):

$$R_{avg}/R_{grain} \approx 1 + (0.03)(0.3) = 1.009$$

This illustrative result suggests that, at this representative grain size and boundary enhancement factor, the *area-averaged* etch rate deviation from grain-boundary effects alone is modest (under 1%). However, the *local, pointwise* sidewall roughness this produces — individual boundary locations etching measurably faster than surrounding grain interior at any given instant — is a distinct concern from the area-averaged rate, since it is local roughness, not average rate, that determines final sidewall smoothness relevant to downstream ONO-equivalent deposition quality (per general 3D NAND literature's sidewall-quality acceptance criteria). Smaller grain size (larger grain-boundary area fraction per unit sidewall area) would proportionally increase both the area-averaged deviation and, more importantly for sidewall quality, the spatial frequency of local roughness features, directly motivating the grain-size control discussed in Section 2.3 as a genuine etch-uniformity, not merely cosmetic, process lever.

### 6.2 Why Grain Size Targets Involve a Genuine Tradeoff

Smaller average grain size reduces the characteristic length scale of grain-boundary-driven roughness (favorable for sidewall smoothness, Section 6.1) but increases total grain boundary area fraction (unfavorable, since more total boundary-driven etch rate deviation accumulates). Conversely, larger grain size reduces total boundary area fraction but produces coarser, more spatially extended roughness features when boundaries do occur. This is a genuine engineering tradeoff without a universally "correct" grain size target — the optimal choice depends on the specific sidewall roughness specification and the deposition process's achievable grain size control range, requiring empirical characterization specific to a given fab's deposition capability rather than a value this book can specify universally.

---

## Part 7: Representative Polysilicon-Specific Defect Modes

### 7.1 Defect Modes With No Direct ON Analog

Beyond the general aspect-ratio-driven profile defects (bowing, twisting, necking, taper) that apply to both ON and OPOP stacks alike (per general 3D NAND literature, revisited comparatively in Chapter 10), polysilicon's distinct materials properties introduce defect modes specific to OPOP integration:

| Defect Mode | Root Cause | Chapter Reference |
|---|---|---|
| Grain-boundary-correlated sidewall micro-roughness | Section 2.2, Section 6.1's grain/boundary etch rate variation | This chapter; Chapter 11 (interaction with charging) |
| Doping-non-uniformity-driven etch rate drift | Within-wafer or within-layer dopant concentration variation (Section 3.2) propagating into etch rate variation | This chapter; Chapter 12 (selectivity consequence) |
| Stress-state-dependent removal rate variation | Section 4.2's observation that polysilicon removal kinetics can depend on crystalline/strain state | Chapter 14 |
| Grain-structure-dependent charging dissipation variation | Local variation in effective conductivity (Section 3.4) producing non-uniform charge dissipation along a single sidewall | Chapter 11 |

### 7.2 Why These Defect Modes Require OPOP-Specific Characterization

Because none of Section 7.1's defect modes have a direct equivalent in ON stack characterization (general 3D NAND literature's defect taxonomy, developed for an amorphous, electrically inert sacrificial material, has no natural category for grain-boundary or doping-driven effects), OPOP process qualification requires its own, dedicated defect characterization and metrology approach beyond simply applying an ON-developed defect inspection checklist unchanged. This is a direct, practical consequence of this chapter's materials science discussion, and a theme Chapter 15 returns to when discussing OPOP-specific equipment and process qualification investment.

---

## Summary and Forward Look

Polysilicon's materials science as a sacrificial layer diverges from PECVD nitride's at essentially every level this chapter examined: it is deposited by different methods with different thermal budget consequences, it is polycrystalline rather than amorphous (introducing grain and grain-boundary-driven etch rate and sidewall uniformity effects with no nitride analog), it is deliberately doped with direct consequences for both etch rate and electrical conductivity, and its stress behavior arises from and is tuned through mechanistically distinct levers. Each of these differences propagates into the chemistry, chamber, and process physics chapters that follow, beginning with the next chapter's development of the halogen-based etch chemistry that polysilicon's materials properties specifically call for, and how that chemistry must be integrated with the fluorocarbon chemistry the co-etched oxide layers require.
