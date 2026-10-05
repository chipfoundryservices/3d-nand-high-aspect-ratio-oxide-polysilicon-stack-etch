# Chapter 3: Halogen Chemistry for Oxide/Polysilicon Etch

## Executive Summary

This chapter develops the plasma chemistry OPOP channel hole etch requires, building directly on Chapter 2's materials foundation. Polysilicon etch chemistry has a mature, independent heritage from logic and planar device polysilicon gate etch, built around chlorine (Cl2) and hydrogen bromide (HBr) halogen chemistry rather than the fluorocarbon chemistry that general 3D NAND literature establishes for oxide etch at extreme aspect ratio. OPOP stack etch must reconcile these two chemistry traditions within a single, continuous channel hole etch — the central chemistry integration challenge this chapter addresses, with no direct equivalent in oxide/nitride stacks, where a single fluorocarbon-based chemistry family addresses both sacrificial and dielectric layers.

---

## Part 1: Why Polysilicon Etch Chemistry Differs From Nitride Etch Chemistry

### 1.1 The Byproduct Volatility Requirement, Revisited

As with any plasma etch chemistry choice (a principle established generally in 3D NAND and logic etch literature alike), the primary requirement is volatile byproduct formation. For polysilicon, chlorine and bromine both form volatile silicon halide byproducts (SiCl4, SiBr4, and related SiClxBry species) with sufficient vapor pressure at typical process temperatures, directly analogous in function to fluorine's role in forming volatile SiF4 from oxide or nitride (general 3D NAND literature).

### 1.2 Why Fluorine-Based Chemistry Is Not the Natural First Choice for Polysilicon

Fluorine chemistry does etch silicon (including polysilicon) readily and spontaneously, often considered "too readily" for good anisotropic process control in isolation: fluorine's spontaneous, non-ion-assisted chemical etch rate on silicon is high enough that achieving good anisotropy (direction-dependent, vertical-sidewall-preserving etch) with fluorine chemistry on polysilicon specifically is more difficult than with chlorine or bromine chemistry, where spontaneous chemical etch rate is lower and the etch is more strongly, controllably ion-assisted. This is the chemistry-mechanism-level reason logic polysilicon gate etch, over decades of process development, converged on chlorine/bromine chemistry rather than fluorine chemistry, despite fluorine's effectiveness at etching silicon-containing materials generally (as established for oxide and nitride in general 3D NAND literature).

### 1.3 The Direct Consequence for OPOP Stack Etch

Because the co-etched oxide layers in an OPOP stack require fluorocarbon chemistry for the polymer-passivation-based anisotropy mechanism general 3D NAND literature establishes, and because polysilicon etch is most effectively and controllably performed with chlorine/bromine chemistry (Section 1.2), a single channel hole etch recipe traversing an OPOP stack must deliver, in some form, both chemistry families to the same feature — the central integration problem this chapter develops.

---

## Part 2: The Halogen Chemistry Family for Polysilicon

### 2.1 Chlorine (Cl2)

Cl2 dissociates in plasma to atomic chlorine (Cl), which reacts with silicon to form volatile SiCl4 (and intermediate SiClx species) through a mechanism well-characterized in logic gate etch literature: chemisorption of Cl atoms onto the silicon surface, followed by ion-assisted desorption of the resulting chlorinated silicon species. Cl2-based chemistry generally provides good silicon etch rate with moderate-to-good selectivity against oxide (a selectivity relationship this book develops quantitatively in Chapter 12), and is a mature, widely available chemistry across essentially all etch equipment platforms given its heritage in logic device manufacturing.

### 2.2 Hydrogen Bromide (HBr)

HBr dissociates to atomic bromine (Br) and hydrogen, with bromine reacting with silicon analogously to chlorine but generally more slowly and more controllably — a property logic gate etch literature has long exploited specifically for anisotropic profile control, since HBr's comparatively gentler, more surface-reaction-rate-limited (rather than supply-limited) etch behavior tends to produce smoother, more vertical sidewalls than more aggressive Cl2 chemistry alone. HBr is frequently blended with Cl2 (Section 2.4) specifically to combine Cl2's etch rate with HBr's profile control benefit.

### 2.3 Sulfur Hexafluoride (SF6) as a Polysilicon Etch Modifier

Unlike its role in general 3D NAND oxide/nitride chemistry (where SF6 serves as a carbon-free fluorine source boosting overall etch rate, per general 3D NAND literature), SF6's role in halogen-based polysilicon chemistry is somewhat different: small SF6 additions can be used to modulate etch rate and profile in Cl2/HBr-based polysilicon recipes, exploiting fluorine's generally higher silicon etch rate to fine-tune overall etch rate without abandoning the primarily halogen-based, profile-controlled chemistry foundation. This is a secondary, modifying role rather than SF6 serving as the primary etchant species, in contrast to its more central role in general 3D NAND dielectric etch recipes.

### 2.4 Representative Chlorine/Bromine Blending Strategy

| Chemistry Blend | Etch Rate Character | Profile Character | Typical Application Within OPOP Etch |
|---|---|---|---|
| Cl2-dominant | Higher | More aggressive, requires careful ion energy control for verticality | Bulk polysilicon layer clearing where rate is prioritized |
| HBr-dominant | Lower | Smoother, more inherently anisotropic | Profile-critical portions, polysilicon layers near select-gate or other CD-sensitive regions |
| Cl2/HBr blend | Intermediate, tunable | Intermediate, tunable via blend ratio | General bulk etch, balancing rate and profile needs |
| Cl2/HBr + SF6 modifier | Fine-tuned via SF6 fraction | Minimal change if SF6 fraction kept small | Fine process window adjustment without full chemistry re-qualification |

---

## Part 3: Hybrid Chemistry Integration With Fluorocarbon Oxide Etch

### 3.1 Why Simple Sequential Chemistry Switching Is the Starting Point

The most straightforward approach to OPOP channel hole etch chemistry integration is sequential chemistry switching: etch each oxide layer with fluorocarbon chemistry (per general 3D NAND literature's established approach), then switch to halogen chemistry for each polysilicon layer, repeating across the full stack depth — directly analogous in structure to how a single continuous ON stack etch chemistry blend handles oxide/nitride transitions, but requiring an actual, discrete chemistry *family* switch (not just a blend ratio adjustment) at every single layer transition given fluorocarbon and halogen chemistry's fundamentally different character.

### 3.2 Why This Sequential Approach Introduces Challenges With No ON Analog

Because an ON stack's single fluorocarbon chemistry family can be blended and ratio-adjusted continuously across oxide/nitride transitions (general 3D NAND literature's multi-step recipe approach, varying blend ratio and power/pressure but remaining within one chemistry family throughout), while an OPOP stack's chemistry must switch between fundamentally different chemistry families at every layer transition, OPOP recipes face additional challenges:

**Chamber/gas-line purge requirements between chemistry family switches.** Residual fluorocarbon-chemistry byproducts or adsorbed species must be adequately cleared before halogen chemistry begins (and vice versa) to avoid cross-contamination effects on the subsequent layer's etch behavior — a purge/stabilization requirement at every single layer transition, far more frequent than the comparatively gentler blend-ratio transitions an ON stack recipe requires.

**Transition-induced profile defects at every layer boundary.** The necking defect mechanism established in general 3D NAND literature (polymer-flux/clearing-rate mismatch at recipe transitions) has a direct, likely more severe analog at every single OPOP layer transition, since the chemistry discontinuity is more fundamental (full chemistry family switch, not merely blend ratio adjustment) than a typical ON-stack recipe step transition.

**Total process time penalty from transition overhead.** Each chemistry switch's purge/stabilization interval (Section 3.2's first point) adds cumulative overhead that scales with layer count, directly analogous to — but generally more severe than — the general 3D NAND throughput scaling concerns already established for channel hole etch at high layer count.

### 3.3 Why Some Degree of Chemistry Overlap or Blending May Be Preferable

Given Section 3.2's challenges with purely sequential, discrete chemistry switching, some OPOP process development approaches instead explore partial chemistry overlap — maintaining some fluorocarbon component present even during polysilicon-layer etch (to pre-condition the chemistry for the upcoming oxide layer transition and potentially reduce switch-transition severity) or maintaining some halogen component present during oxide-layer etch (for the symmetric reason) — trading some reduction in each individual layer's etch optimality for reduced transition-induced defect risk and reduced cumulative purge overhead. This approach requires careful characterization of cross-chemistry interaction effects (e.g., does residual Cl2/HBr affect fluorocarbon polymer formation quality on the oxide sidewall, a question with no direct ON-stack analog to draw on) rather than simply importing general 3D NAND multi-step recipe design practice unchanged.

### 3.4 Why Chemistry Compatibility With Chamber Hardware Must Be Verified Independently

Because halogen chemistry (Cl2, HBr) and fluorocarbon chemistry interact differently with chamber materials (developed fully in Chapter 8), equipment and process teams cannot assume that a chamber qualified for general 3D NAND fluorocarbon-only ON etch is automatically suitable for the mixed halogen/fluorocarbon exposure OPOP etch requires — chamber material compatibility (Chapter 8) and gas delivery/byproduct handling (Chapter 6) must be independently verified for this hybrid chemistry exposure, a qualification requirement with no equivalent in single-chemistry-family ON processing.

---

## Part 4: Byproduct Comparison

### 4.1 Halogen-Based Polysilicon Etch Byproducts

| Byproduct | Source | Volatility | Relevance |
|---|---|---|---|
| SiCl4 | Si + Cl (chlorine chemistry) | Boiling point 57.6°C — volatile but closer to typical process/wall temperatures than fluorine-based byproducts | Primary chlorine-chemistry byproduct; some redeposition risk at cooler chamber surfaces, addressed in Chapter 8 |
| SiBr4 | Si + Br (bromine chemistry) | Boiling point 153°C — notably less volatile than SiCl4 or SiF4 | Requires more careful thermal management of chamber surfaces to avoid redeposition, a distinct consideration from general 3D NAND fluorocarbon chemistry's byproduct volatility profile |
| HCl, HBr (unreacted/recombined) | Hydrogen from HBr dissociation recombining with halogen | Volatile gases | Generally unproblematic, readily pumped |

### 4.2 Why SiBr4's Lower Volatility Matters

Unlike SiF4 (boiling point -86°C) or even SiCl4 (57.6°C), SiBr4's considerably higher boiling point (153°C) means standard process and chamber wall temperatures, adequate for fluorocarbon or chlorine chemistry byproduct removal, may be insufficient to prevent some SiBr4 redeposition on cooler chamber surfaces — a chamber thermal management consideration specific to HBr-containing chemistry blends, directly relevant to Chapter 8's chamber material and conditioning discussion, and with a structural analogy (though different specific chemistry and temperature regime) to the AlCl3 residue management challenge documented in other etch chemistry systems within this book series.

---

## Part 5: A Worked Transition Overhead Estimate

### 5.1 Framing the Calculation

To quantify Section 3.2's cumulative transition overhead concern, consider a representative 128-layer-pair OPOP stack (256 individual layer transitions across the full stack, directly analogous to the layer-pair counting convention established in general 3D NAND literature), with each chemistry-family transition requiring a purge/stabilization interval before the next layer's etch can proceed with confidence in its chemistry state.

### 5.2 Illustrative Calculation

**Assumptions:** each chemistry transition (oxide-to-polysilicon or polysilicon-to-oxide) requires an illustrative 3-second purge/stabilization interval (a representative value reflecting gas line and chamber residence time considerations analogous to, but likely somewhat longer than, general 3D NAND literature's chamber residence time estimates, given the more complete chemistry family change involved here relative to a within-family blend ratio adjustment).

$$t_{overhead,total} = N_{transitions} \times t_{purge} = 256 \times 3\ s = 768\ s \approx 12.8\ \text{minutes}$$

### 5.3 Interpreting the Result

A 12.8-minute cumulative transition overhead, added to the underlying bulk etch time at each individual layer (itself subject to the same general aspect-ratio-dependent etch rate falloff established in general 3D NAND literature, developed comparatively for OPOP in Chapter 10), represents a potentially significant fraction of total channel hole etch process time, particularly at the shallower, less aspect-ratio-constrained portions of the etch where per-layer bulk etch time itself may be comparatively short. This illustrative calculation is the quantitative grounding for Section 3.3's motivation to explore partial chemistry overlap approaches: even a modest, few-second per-transition purge requirement compounds, at high layer count, into a throughput penalty large enough to justify the additional process characterization complexity that reduced-transition-overhead approaches require.

### 5.4 Why This Overhead Has No Direct ON-Stack Equivalent at This Magnitude

While general 3D NAND ON stack etch also requires some brief stabilization at major recipe step transitions (per general literature's multi-step recipe discussion), those transitions are comparatively infrequent (a handful of major steps per full channel hole etch — mask open, bulk etch, breakthrough) rather than occurring at every single one of 256 individual layer boundaries. This frequency difference — a handful of transitions versus hundreds — is the direct, quantitative reason OPOP's chemistry transition overhead is treated in this book as a first-order process economics concern (Chapter 15 returns to this with full economic framing) rather than a minor, easily-absorbed process detail.

---

## Part 6: Thermodynamic Comparison of Etch Chemistry Byproducts

### 6.1 Side-by-Side Volatility Comparison Across Chemistry Systems

| Byproduct | Source Chemistry | Boiling/Sublimation Point | Relative Volatility Ranking |
|---|---|---|---|
| SiF4 | Fluorine (oxide/nitride etch, general 3D NAND literature) | -86°C | Highest |
| SiCl4 | Chlorine (polysilicon etch) | 57.6°C | Moderate |
| SiBr4 | Bromine (polysilicon etch) | 153°C | Lowest among this comparison set |
| CO/CO2 | Fluorocarbon polymer oxidation (general 3D NAND literature) | -192°C / -78.5°C | Highest |

### 6.2 Why This Ranking Matters for Chamber Design (Preview of Chapter 8)

This volatility ranking directly previews Chapter 8's chamber material and thermal management discussion: a chamber handling only fluorocarbon-chemistry byproducts (general ON-stack processing) operates with a comparatively generous volatility margin at typical process and wall temperatures, while an OPOP chamber handling the full byproduct set in this table — particularly SiBr4, with its markedly higher boiling point — must be more deliberately engineered for byproduct removal and redeposition avoidance, a direct, quantitative consequence of this chapter's chemistry choice that Chapter 8 develops into specific chamber material and thermal design requirements.

---

## Summary and Forward Look

OPOP channel hole etch chemistry must reconcile two historically distinct chemistry traditions: chlorine/bromine-based halogen chemistry, mature from decades of logic polysilicon gate etch development, for the sacrificial polysilicon layers; and fluorocarbon polymer-passivation chemistry, established in general 3D NAND literature, for the co-etched oxide layers. This reconciliation can proceed via discrete sequential chemistry switching (simpler conceptually, but introducing purge overhead and transition-defect risk at every layer boundary) or partial chemistry overlap (reducing transition severity at the cost of requiring characterized cross-chemistry interaction understanding), and must additionally account for halogen chemistry's distinct byproduct volatility profile, particularly HBr-chemistry's less volatile SiBr4 byproduct, relative to the fluorine-based byproducts general 3D NAND chemistry produces.

The next chapter develops the surface reaction mechanisms this chemistry drives at the molecular level, for both oxide and polysilicon, and specifically how these mechanisms behave at the extreme aspect ratios OPOP channel hole etch, like its ON counterpart, must operate at.
