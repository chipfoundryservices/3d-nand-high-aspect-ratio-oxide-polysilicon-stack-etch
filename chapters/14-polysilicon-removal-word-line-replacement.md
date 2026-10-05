# Chapter 14: Sacrificial Polysilicon Removal and Word Line Replacement for OPOP Stacks

## Executive Summary

This chapter completes Part III by addressing the final major etch-adjacent process this book covers: converting an OPOP stack's sacrificial polysilicon into the final metal-gate word line structure. This proceeds through the same general slit-etch-and-replacement architecture established in 3D NAND literature, but with sacrificial removal chemistry fundamentally different from hot phosphoric acid — the near-universal ON-stack choice — since phosphoric acid does not remove polysilicon at a useful rate. We develop the TMAH-based and halogen-based removal chemistry alternatives, their lateral-access and selectivity characteristics, and the resulting structural-support-during-removal considerations specific to OPOP.

---

## Part 1: Why Hot Phosphoric Acid Does Not Transfer to Polysilicon Removal

### 1.1 The Chemistry Mismatch

Hot phosphoric acid's exceptional selectivity for nitride removal over oxide (general 3D NAND literature's >100:1 figure) is specifically a consequence of H3PO4's chemical attack mechanism on Si-N bonding, which does not similarly attack polysilicon's Si-Si covalent network at a comparable rate. Applying hot phosphoric acid to an OPOP stack would, at best, proceed extremely slowly against polysilicon while potentially posing its own, separate compatibility concerns with surrounding structures — it is simply the wrong chemistry for this materials system, not a slower or less-selective version of the same general-purpose removal tool.

### 1.2 Why This Necessitates an Entirely Separate Removal Process Development Track

Because OPOP removal chemistry cannot inherit ON's mature, extensively characterized hot phosphoric acid process, OPOP process developers must independently develop, characterize, and qualify a distinct removal chemistry from first principles (or from adjacent, non-3D-NAND process heritage, Section 2 below) — a substantial process development investment with no shortcut available from the dominant ON approach's existing knowledge base, directly reinforcing Chapter 1's observation that OPOP integration carries real engineering cost precisely at this step.

---

## Part 2: TMAH-Based Wet Removal

### 2.1 Chemistry and Mechanism

Tetramethylammonium hydroxide (TMAH) is a well-established silicon wet etchant, widely used in MEMS and other silicon micromachining applications for anisotropic or isotropic silicon etching depending on concentration and temperature conditions. TMAH attacks silicon through a hydroxide-mediated mechanism, producing soluble silicate species, with etch rate and oxide selectivity depending on concentration, temperature, and the presence of any added surfactants or chelating agents (a mature parameter space from TMAH's non-3D-NAND process heritage).

### 2.2 Why TMAH's Oxide Selectivity Must Be Independently Verified for This Application

While TMAH is known generally to etch silicon much faster than oxide (a favorable starting selectivity characteristic for sacrificial polysilicon removal, analogous in function to hot phosphoric acid's nitride-over-oxide selectivity), the specific selectivity ratio achievable, and its sensitivity to the specific oxide film quality present (Chapter 2's PECVD oxide discussion, general 3D NAND literature's deposition-recipe-dependent film property caution), requires independent verification for the specific OPOP stack's oxide films rather than relying on TMAH selectivity figures reported for other, non-3D-NAND silicon/oxide material systems.

### 2.3 Lateral Access Behavior

TMAH removal through slit-based lateral access faces the same general lateral diffusion-limited removal physics established in 3D NAND literature for hot phosphoric acid (removal rate slowing with increasing lateral distance from the slit, general literature's diffusion-limited model), but with TMAH-specific diffusion coefficient and reaction rate parameters requiring independent characterization rather than direct transfer from hot phosphoric acid's established values.

### 2.4 Potential Compatibility Considerations

TMAH's compatibility with other materials present in a partially-processed 3D NAND structure (any exposed metal, barrier, or other non-oxide/polysilicon material at the point removal is performed, general literature's integration-flow context) must be verified independently, since TMAH's chemistry and reactivity profile differs from hot phosphoric acid's, and a compatibility assumption transferred from the ON-stack process without verification risks an unanticipated materials interaction specific to the OPOP integration flow's particular sequence and exposed materials at this process step.

---

## Part 3: Halogen-Based Dry/Wet Hybrid Removal

### 3.1 Why a Dry or Hybrid Approach Is a Viable Alternative

Because Chapter 3 already established halogen chemistry (Cl2, HBr) as an effective polysilicon etchant for the channel hole and staircase vertical etch steps, an adapted halogen-based chemistry — potentially a dry plasma process delivered through the slit access path, or a hybrid combining dry chemical pretreatment with a wet finishing step — represents an alternative removal approach building on chemistry this book has already developed in depth, rather than requiring an entirely separate chemistry family (TMAH) to be introduced.

### 3.2 Why Dry Plasma Delivery Through a Slit Faces Line-of-Sight Limitations

Chapter 14-equivalent general literature's wet removal discussion for ON stacks (hot phosphoric acid) specifically notes that removal must proceed through narrow, non-line-of-sight horizontal cavities extending potentially hundreds of microns laterally from the slit — a geometry fundamentally incompatible with plasma/ion-based removal, which, per Chapter 4's transport physics discussion extended to this geometry, requires at least some line-of-sight or near-line-of-sight access that a fully lateral, enclosed cavity does not provide. This means a purely dry, plasma-based removal process is unlikely to achieve adequate lateral reach on its own, motivating the hybrid approach (Section 3.1) in which any dry/plasma component addresses only the slit-adjacent region while a wet chemical process (TMAH or an adapted halogen-based wet chemistry) completes removal at greater lateral distance.

### 3.3 Why This Hybrid Approach Adds Process Complexity Relative to a Single-Chemistry Wet Process

Compared to Section 2's TMAH-only approach (a single wet chemistry process, directly analogous in overall structure to ON's single-wet-chemistry hot phosphoric acid process), a dry/wet hybrid approach introduces an additional process step and transition, with its own qualification burden analogous in spirit to Chapter 3's channel hole etch chemistry-transition overhead concern, though occurring at the process-flow level (one discrete process step transitioning to another) rather than within a single, continuous etch step. Process developers should weigh this added complexity against whatever lateral-reach or selectivity advantage the hybrid approach might offer over a TMAH-only approach, a tradeoff requiring direct comparative characterization rather than an a priori assumption that either approach is universally preferable.

---

## Part 4: Metal Fill Considerations for OPOP

### 4.1 Why Metal Fill Itself Is Materials-Choice-Independent

Once sacrificial polysilicon (via either Section 2 or Section 3's removal approach) has been fully removed, the resulting empty horizontal cavities require TiN barrier and tungsten fill through the same general ALD-plus-CVD process general 3D NAND literature establishes for ON stacks — metal fill process requirements depend on cavity geometry (set by layer thickness and lateral extent, general literature's framework) and do not depend on what sacrificial material previously occupied the cavity, since by the time fill occurs, no distinction remains between an OPOP-derived and ON-derived empty cavity.

### 4.2 Why Cavity Surface Chemistry Prior to Fill May Differ

What may differ is the cavity's exposed oxide surface chemistry immediately following removal: TMAH or halogen-based removal chemistry (Section 2-3) may leave a different surface termination or residue character on the exposed oxide cavity walls than hot phosphoric acid leaves (general literature's established, well-characterized post-removal surface condition for ON stacks), potentially requiring an OPOP-specific pre-fill surface treatment or cleaning step to ensure adequate ALD nucleation and barrier layer quality — a further, specific instance of this book's recurring finding that OPOP's distinct chemistry choices propagate consequences into downstream process steps that might otherwise be assumed materials-choice-independent.

---

## Part 5: Mechanical Stability During the Unsupported Interval

### 5.1 Why the General Vulnerability Window Applies Equally

General 3D NAND literature identifies the interval between sacrificial removal and completed metal fill as the point of minimum structural integrity in the entire process flow, since the stack's oxide layers lose their horizontal mechanical support once sacrificial material is removed, relying only on the channel hole pillar array for support until fill is complete. This vulnerability is purely structural/geometric, independent of which sacrificial material was removed or which chemistry removed it — it applies to OPOP exactly as to ON.

### 5.2 Why OPOP's Removal Process Timing May Differ, With Structural Consequences

Because Section 2.3 and Section 3's removal processes may proceed at different rates, and require different total process time, than hot phosphoric acid's well-characterized ON-stack removal rate, the *duration* of this structurally vulnerable interval for an OPOP stack may differ from an equivalent ON stack's duration — longer if OPOP's removal chemistry proves slower (extending the vulnerability window and its associated risk, general literature's framework applied with an OPOP-specific duration), or shorter if it proves faster. This duration difference, not the vulnerability mechanism itself, is where OPOP-specific characterization (Section 2-3) feeds back into the general structural risk assessment general literature establishes.

### 5.3 Why This Reinforces the Removal Chemistry Characterization Priority

Because Section 5.2 shows that removal process speed directly determines structural vulnerability window duration, and because this window represents (per general literature) the highest structural-failure-risk interval in the entire process flow, achieving a removal chemistry and process (Section 2 or 3) that proceeds at least as quickly as, and ideally faster than, hot phosphoric acid's ON-stack benchmark should be treated as a high-priority characterization and optimization target, not merely a secondary consideration behind selectivity or surface-quality concerns (Section 2.2, Section 4.2) alone.

---

## Part 6: A Worked Lateral Removal Time Comparison

### 6.1 Applying the General Diffusion-Limited Model to TMAH Removal

General 3D NAND literature's diffusion-limited lateral removal model, $x(t)\approx\sqrt{2D_{eff}t}$, applies to TMAH removal using a TMAH-specific effective diffusion coefficient $D_{eff,TMAH}$, which must be characterized independently from hot phosphoric acid's own $D_{eff}$ value (general literature's illustrative reference figure).

### 6.2 Illustrative Comparison

**Illustrative hot phosphoric acid reference** (general 3D NAND literature's illustrative calculation): clearing a 3µm block half-width in approximately 90 seconds, using $D_{eff}\approx5\times10^{-10}\ \text{cm}^2/\text{s}$.

**Illustrative TMAH comparison:** suppose TMAH's effective diffusion/reaction coefficient through the narrow polysilicon-cavity geometry is characterized at $D_{eff,TMAH}\approx3\times10^{-10}\ \text{cm}^2/\text{s}$ (illustratively somewhat lower, reflecting TMAH's generally more viscous aqueous solution character and different molecular size relative to phosphoric acid, a plausible but not yet empirically confirmed directional hypothesis consistent with this book's recurring caution about assumed-equivalent transport parameters):

$$t_{TMAH} = \frac{x^2}{2D_{eff,TMAH}} = \frac{(3\times10^{-4})^2}{2\times3\times10^{-10}} = \frac{9\times10^{-8}}{6\times10^{-10}} = 150\ s$$

### 6.3 Interpreting This Illustrative Result

This illustrative comparison suggests TMAH removal, under this particular illustrative parameter assumption, could take roughly 67% longer than hot phosphoric acid removal for the same lateral clearing distance — directly relevant to Section 5.2's structural vulnerability window duration concern, since a longer removal process time directly extends the interval during which the stack lacks horizontal mechanical support. This illustrative result should motivate, rather than substitute for, direct experimental characterization of TMAH's actual effective diffusion coefficient in this specific application, precisely because Section 5.3 identified removal speed as a high-priority characterization target given its direct structural-risk consequence.

### 6.4 Why Halogen-Based Hybrid Removal's Comparable Timing Is Even Less Certain

Because Section 3's halogen-based hybrid approach combines a dry/plasma component (addressing only slit-adjacent regions, Section 3.2) with a wet finishing step, its total effective removal time for a given lateral clearing distance depends on the combination of two distinct process steps' individual timing, each requiring its own characterization, making a confident illustrative estimate for this approach less reliable than even the single-chemistry TMAH estimate in Section 6.2 — a further specific instance of this book's general finding that OPOP's less mature process characterization base extends to this removal step as thoroughly as to the transport physics (Chapter 10) and selectivity (Chapter 12) questions addressed earlier.

---

## Part 7: Chemistry Approach Comparison Summary

| Dimension | Hot H3PO4 (ON Reference) | TMAH (OPOP Candidate) | Halogen-Based Hybrid (OPOP Candidate) |
|---|---|---|---|
| Process type | Single-step wet | Single-step wet | Multi-step dry+wet hybrid |
| Target material compatibility | Mature, extensively characterized for nitride | Established for silicon generally; OPOP-specific selectivity requires verification (Section 2.2) | Builds on Chapter 3's halogen chemistry; lateral reach limited for dry component alone (Section 3.2) |
| Illustrative lateral removal time (3µm half-width) | ~90s (general literature reference) | ~150s (Section 6.2, illustrative) | Not confidently estimable without further characterization (Section 6.4) |
| Process complexity | Low (single chemistry) | Low (single chemistry) | Higher (two-step transition, Section 3.3) |
| Compatibility verification burden | Minimal (mature, well-characterized) | Required (Section 2.4) | Required for both component steps |
| Post-removal surface condition for metal fill | Well-characterized | Requires verification (Section 4.2) | Requires verification (Section 4.2) |

---

## Summary and Forward Look

OPOP sacrificial removal requires an entirely distinct chemistry and process development track from ON's mature hot phosphoric acid approach, with TMAH-based wet removal and halogen-based dry/wet hybrid removal representing the two primary candidate approaches, each requiring independent selectivity, lateral-access, and compatibility characterization rather than inheriting ON's established process knowledge. Metal fill itself is materials-choice-independent once removal is complete, though OPOP's distinct removal chemistry may necessitate additional pre-fill surface treatment. The general structural vulnerability window between removal and fill applies equally to OPOP, with removal process speed — a function of the specific OPOP removal chemistry's characterized rate — directly determining this window's duration and associated structural risk.

With Part III's complete OPOP-specific process physics treatment now established — comparative transport physics (Chapter 10), charging (Chapter 11), selectivity (Chapter 12), staircase (Chapter 13), and removal/replacement (this chapter) — Part IV concludes this book by addressing the equipment, vendor, and production economics landscape this extensive technical divergence from the ON baseline ultimately produces.
