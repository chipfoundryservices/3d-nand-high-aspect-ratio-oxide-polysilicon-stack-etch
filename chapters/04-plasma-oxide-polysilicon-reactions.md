# Chapter 4: Plasma-Oxide and Plasma-Polysilicon Surface Reactions at Extreme Aspect Ratio

## Executive Summary

This chapter completes Part I by developing the molecular-level surface reaction mechanisms driving OPOP channel hole etch, for both the halogen-chemistry polysilicon reaction and the fluorocarbon-chemistry oxide reaction, and — the focus unique to this chapter — how both mechanisms behave once transport limitations at extreme aspect ratio (established generally in 3D NAND literature) are taken into account. This chapter builds the surface-kinetics foundation for Chapter 10's quantitative OPOP-vs-ON transport comparison and Chapter 11's charging-physics treatment.

---

## Part 1: Oxide Surface Reactions — Consistent With General 3D NAND Literature

### 1.1 Why Oxide Reaction Mechanisms Transfer Directly From ON Treatment

Because the oxide layers in an OPOP stack are chemically identical in composition and general deposition method to the oxide layers in an ON stack (both commonly PECVD SiO2, per general 3D NAND literature), the fluorocarbon-chemistry oxide etch mechanism — ion-assisted fluorination of a thin surface reaction layer, forming volatile SiF4 and CO/CO2 byproducts, with sidewall polymer formation providing anisotropy — transfers directly from general 3D NAND literature's established treatment without OPOP-specific modification. This chapter does not re-derive that mechanism in full; readers requiring the complete oxide reaction mechanism derivation should consult general 3D NAND etch literature's treatment, which applies unchanged to OPOP's oxide layers.

### 1.2 Where Oxide Reaction Behavior Does Diverge in an OPOP Context

The one place oxide reaction behavior in an OPOP stack genuinely diverges from an ON stack's is at layer transitions (Chapter 3, Part 3): because the adjacent sacrificial layer in an OPOP stack is polysilicon rather than nitride, any cross-chemistry interaction effects at the oxide/polysilicon interface (residual halogen species affecting fluorocarbon polymer formation quality near the transition, or vice versa, Chapter 3, Section 3.3) represent a genuinely new consideration without an ON-stack analog, since ON stacks never require this specific fluorocarbon/halogen chemistry-family boundary at their oxide/nitride interfaces.

---

## Part 2: Polysilicon Surface Reaction Mechanism

### 2.1 The Chlorine/Bromine Reaction Sequence

Building on Chapter 3's chemistry development, the polysilicon surface reaction proceeds through a sequence well-characterized in logic gate etch literature:

1. Cl or Br atoms (and some molecular Cl2/HBr) adsorb onto the polysilicon surface
2. Ion bombardment creates a damaged, halogenated surface layer (a direct mechanistic analog to the fluorinated reaction layer general 3D NAND literature describes for oxide/nitride, but with chlorine or bromine as the halogenating species and silicon's covalent network, rather than an oxide or nitride network, as the substrate)
3. Sufficient halogenation of a given surface silicon atom permits desorption as volatile SiCl4 or SiBr4 (or mixed SiClxBry species in blended chemistry, Chapter 3, Section 2.4)

### 2.2 Why Polysilicon's Reaction Layer Differs From Oxide's or Nitride's

Unlike oxide's SiOxFy reaction layer or nitride's analogous fluorinated reaction layer (both general 3D NAND literature constructs), polysilicon's halogenated reaction layer forms on a covalent, elemental silicon network rather than a silicon-oxygen or silicon-nitrogen compound network. This structural distinction means polysilicon's reaction layer formation and consumption kinetics are governed by Si-Si bond breaking and subsequent Si-halogen bond formation, rather than the Si-O or Si-N bond disruption relevant to oxide and nitride — a different, though related, bond-breaking energetics problem, directly connected to Chapter 2's doping-dependent reactivity discussion (dopant atoms altering the Si network's electronic structure and therefore its Si-Si bond energetics).

### 2.3 Grain-Structure Interaction With Reaction Layer Formation

Chapter 2, Section 2.2 established that grain boundaries present structurally disrupted, often dopant-segregated silicon, with measurably different etch rate than grain interiors. At the surface-reaction-mechanism level developed in this chapter, this translates to grain boundaries presenting a different (generally more readily disrupted, Chapter 2, Section 2.2) Si-Si bond network for the halogenation reaction sequence (Section 2.1) to act on, directly explaining at the mechanistic level why grain boundaries etch measurably faster — the halogenation and ion-assisted desorption steps proceed more readily on the already-structurally-disrupted boundary network than on well-ordered grain interior lattice.

---

## Part 3: Why Spontaneous (Non-Ion-Assisted) Chemical Etch Rate Matters More for Polysilicon

### 3.1 The Anisotropy Challenge Specific to Silicon

Chapter 3, Section 1.2 flagged that fluorine's high spontaneous chemical etch rate on silicon makes fluorine chemistry less suitable for anisotropic polysilicon etch than for oxide/nitride etch, where spontaneous chemical etch rate is comparatively more moderate. This chapter now grounds that claim mechanistically: silicon's covalent network (Section 2.2) presents a chemically more reactive, more readily attacked bonding structure toward halogens generally than oxide's or nitride's compound networks do, meaning *any* halogen chemistry choice for polysilicon etch (not only fluorine) must contend with comparatively higher spontaneous, non-ion-assisted chemical etch rate than the oxide/nitride case — chlorine and bromine chemistry are chosen specifically because they offer the *least* severe version of this general silicon-reactivity challenge among viable halogen options, not because they eliminate it entirely.

### 3.2 Consequence for Sidewall Protection Strategy

Because polysilicon's spontaneous chemical etch rate (even with the comparatively favorable Cl2/HBr chemistry choice) remains higher, relative to its ion-assisted rate, than oxide's or nitride's fluorocarbon-chemistry spontaneous rate, polysilicon etch anisotropy relies more heavily on sidewall passivation mechanisms distinct from — though loosely analogous to — the fluorocarbon polymer mechanism general 3D NAND literature establishes for oxide/nitride. In halogen chemistry, sidewall protection commonly relies on a thin silicon oxyhalide or oxychloride passivation layer (formed from trace oxygen, intentionally added or present as a background species, reacting with the halogenated silicon surface) rather than a carbon-based polymer — a mechanistically distinct passivation chemistry from the fluorocarbon case, requiring its own characterization and control rather than being a direct analog to Chapter 3's fluorocarbon polymer discussion.

### 3.3 Why This Passivation Mechanism Difference Matters for OPOP Recipe Design

Because polysilicon's sidewall passivation mechanism (Section 3.2) is chemically distinct from oxide's fluorocarbon polymer mechanism, a single OPOP channel hole etch recipe must sustain *two* distinct, non-interchangeable passivation chemistries — one for each material — rather than a single passivation mechanism serving both layer types as general 3D NAND fluorocarbon chemistry does for an ON stack's oxide and nitride alike. This is a second, chemistry-mechanism-level restatement of Chapter 3's core integration challenge, now grounded specifically in why the two materials cannot share a single anisotropy-enabling mechanism even if a chemistry blend could nominally etch both.

---

## Part 4: Transport Limitations at Extreme Aspect Ratio

### 4.1 Why General 3D NAND Transport Physics Applies, With Modification

General 3D NAND literature establishes that both ion trajectory narrowing (a geometric, chemistry-independent effect) and Knudsen-regime neutral transport (a chemistry-dependent effect, varying with each species' effective sidewall sticking/reaction probability) attenuate flux reaching the bottom of an extreme-aspect-ratio feature. This general transport framework applies to OPOP stacks as much as to ON stacks — the feature geometry and underlying gas transport physics do not care which specific sacrificial material is present. What changes for OPOP, developed fully in Chapter 10, is the *specific* sticking/reaction probability values for the halogen species (Cl, Br, SiCl4, SiBr4) relevant to polysilicon layers, which differ from the fluorocarbon species values relevant to oxide and nitride layers in the general ON treatment.

### 4.2 Why Halogen Species Transport May Differ From Fluorocarbon Species Transport

Chlorine and bromine atoms, and their silicon halide reaction products, have different molecular size, mass, and surface reactivity than fluorine and fluorocarbon radical species — differences that directly affect both the mean free path (and therefore Knudsen regime behavior at a given pressure) and the effective sidewall sticking probability $\gamma$ in the transport probability framework general 3D NAND literature establishes. Without characterizing these halogen-specific transport parameters directly (a task Chapter 10 undertakes comparatively against the established fluorocarbon-species values), it is not safe to assume halogen chemistry transport behavior at extreme aspect ratio mirrors fluorocarbon chemistry transport behavior merely because both operate within the same general Knudsen-regime framework.

### 4.3 Why Chemistry-Switching Compounds the Transport Problem

Because OPOP channel hole etch requires switching between fluorocarbon and halogen chemistry at every layer transition (Chapter 3, Part 3), and because each chemistry's transport attenuation behavior at a given depth is distinct (Section 4.2), the *effective* flux conditions realized at the bottom of a deep OPOP feature are not merely attenuated versions of a single, consistent top-opening chemistry condition (as in the simpler ON case, where one chemistry family persists with blend-ratio variation throughout) — they reflect whichever chemistry is currently active, each attenuated according to its own distinct transport parameters, adding a further layer of complexity Chapter 10 must address beyond what a direct ON-stack transport treatment alone would require.

---

## Part 5: Reaction Layer Behavior at Oxide/Polysilicon Transitions

### 5.1 Why the Transition Is More Discontinuous Than an Oxide/Nitride Transition

General 3D NAND literature (Chapter 4-equivalent treatment for ON stacks) notes that the etch front's reaction layer carries some brief compositional memory across an oxide/nitride transition, since both materials share the same fluorocarbon-chemistry reaction layer framework (SiOxFy-like layers in both cases, differing mainly in the non-silicon species involved — oxygen versus nitrogen). An oxide/polysilicon transition is more discontinuous: the reaction layer composition must transition between a fluorinated oxide reaction layer and a halogenated silicon reaction layer, chemically distinct frameworks (Section 1.1 vs. Section 2.1) rather than variations within a single, shared fluorocarbon-chemistry framework.

### 5.2 Consequence for Endpoint Detection and Transition Timing

This more discontinuous transition character (Section 5.1) means endpoint/transition detection signals at OPOP oxide/polysilicon boundaries (developed fully in Appendix F) are likely to show more pronounced, more readily detectable signal changes than the comparatively subtler oxide/nitride transition signals general 3D NAND literature describes — a potential advantage for per-layer transition timing control (useful given Chapter 3, Section 5's transition-overhead concerns), though this must be weighed against the purge/stabilization overhead (Chapter 3, Part 3) that the same chemistry discontinuity imposes.

---

## Part 6: Bond Energy Comparison and Its Reactivity Consequence

### 6.1 Representative Bond Energies

| Bond | Approximate Bond Energy (kJ/mol) | Relevance |
|---|---|---|
| Si-O (in SiO2) | ~452 | Oxide network strength; relevant to Section 1.1's fluorocarbon mechanism |
| Si-N (in Si3N4) | ~335 (general 3D NAND literature reference) | Nitride network strength, included for comparison |
| Si-Si (polysilicon network) | ~222-310 (range reflects crystalline environment/strain dependence) | Polysilicon network strength; central to Section 2.2's reactivity discussion |
| Si-Cl | ~381 | Chlorination product bond strength |
| Si-Br | ~310 | Bromination product bond strength |
| Si-F | ~565 | Fluorination product bond strength (strongest in this comparison set) |

### 6.2 Why the Si-Si Network Is More Readily Disrupted Than Si-O

The comparison in Section 6.1 makes Section 3.1's reactivity claim quantitative: Si-Si bonds (~222-310 kJ/mol) are substantially weaker than Si-O bonds (~452 kJ/mol), meaning less energy input (whether from spontaneous chemical attack or ion-assisted damage, Chapter 4 Part 1-2's mechanisms) is required to disrupt the silicon network sufficiently to permit halogenation and subsequent volatile byproduct formation. This bond-energy gap is the first-principles, quantitative grounding for every qualitative reactivity claim this chapter and Chapter 2 have made about polysilicon etching "more readily" than oxide — it is not an empirical rule of thumb but a direct consequence of comparative bond energetics.

### 6.3 Why Si-F Bond Strength Explains Fluorine's Excessive Reactivity Toward Silicon

Section 6.1's data also explains Section 1.2 and Section 3.1's claim that fluorine is poorly suited to anisotropic polysilicon etch: Si-F bonds (~565 kJ/mol) are the strongest bond in this entire comparison set, meaning fluorination of silicon is thermodynamically highly favorable — favorable enough to proceed spontaneously, without requiring the ion-assistance that provides directional, anisotropic control. Chlorine and bromine's weaker Si-Cl (~381 kJ/mol) and Si-Br (~310 kJ/mol) bond strengths make silicon halogenation with these species *less* thermodynamically overdetermined, requiring more ion-assistance to proceed at a useful rate and thereby naturally favoring the more directional, controllable etch behavior Section 1.2 and Chapter 3 identified as the reason logic polysilicon etch converged on chlorine/bromine chemistry rather than fluorine.

---

## Part 7: Mechanism Contribution Comparison — Oxide vs. Polysilicon

### 7.1 Side-by-Side Mechanism Table

| Aspect | Oxide (Fluorocarbon Chemistry) | Polysilicon (Halogen Chemistry) |
|---|---|---|
| Dominant reactive species | F, CFx | Cl, Br |
| Reaction layer substrate | SiO2 network (Si-O bonds, ~452 kJ/mol) | Si-Si network (~222-310 kJ/mol) |
| Primary byproduct | SiF4, CO/CO2 | SiCl4, SiBr4 |
| Sidewall passivation mechanism | Carbon-based fluorocarbon polymer | Silicon oxyhalide passivation layer |
| Spontaneous (non-ion-assisted) etch rate relative to ion-assisted rate | Moderate | Higher (Section 3.1), requiring careful chemistry choice to manage |
| Grain/microstructure dependence | None (amorphous network) | Significant (polycrystalline, Chapter 2 Part 2) |
| Doping dependence | None (dielectric, no doping concept) | Significant (Chapter 2, Section 3.2) |

### 7.2 Why This Table Is the Chapter's Central Takeaway

This side-by-side comparison crystallizes this chapter's purpose: oxide and polysilicon etch within the same OPOP channel hole are not two variations of a single underlying mechanism, but two genuinely distinct reaction systems, differing in reactive species, substrate bond energetics, byproducts, passivation chemistry, and — unique to polysilicon — microstructure and doping dependence. Every subsequent Part II and Part III chapter's OPOP-specific content traces back to one or more rows of this table, making it a useful reference point to revisit when working through the chamber engineering and process physics chapters that follow.

---

## Summary and Forward Look

OPOP channel hole etch surface chemistry comprises two mechanistically distinct reaction systems operating in the same feature: oxide's fluorocarbon-chemistry reaction mechanism, transferring directly from general 3D NAND literature, and polysilicon's halogen-chemistry reaction mechanism, built on a covalent Si-Si network's distinct bond-breaking energetics, grain-structure-dependent reactivity, and a chemically distinct (oxyhalide-based rather than carbon-polymer-based) sidewall passivation mechanism. These two systems do not merely coexist — their chemistry-specific transport attenuation behavior at extreme aspect ratio, and the discontinuous reaction-layer transition between them at every layer boundary, together determine the realized etch conditions at depth in ways this chapter has established qualitatively and Chapter 10 develops quantitatively.

With Part I's materials, chemistry, and surface mechanism foundation complete, Part II now turns to the chamber and process engineering this chemistry system demands: reactor requirements, gas delivery, process window mapping, chamber materials, and RF/pulsing strategies, each addressed specifically for the hybrid halogen/fluorocarbon chemistry and dual-mechanism surface reaction system this chapter has established.
