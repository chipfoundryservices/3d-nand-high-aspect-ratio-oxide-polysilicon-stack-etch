# Glossary: OPOP Etch-Specific Terminology

Terms are defined as used throughout this book, with emphasis on terminology specific to oxide/polysilicon (OPOP) integration. For general 3D NAND architectural terminology (string, block, word line, channel hole, staircase, slit) not specific to OPOP, readers should consult general 3D NAND etch literature's glossary, which this book's terminology is fully consistent with.

---

**Afterglow** — The interval following source power reduction in a pulsed plasma, during which electron temperature decays rapidly while ion and radical populations persist longer. Relevant to both general 3D NAND charging mitigation and OPOP's polysilicon-sidewall charge-dissipation interaction. See Chapter 9, Part 2-3; Chapter 11.

**ARDE (Aspect Ratio Dependent Etching)** — Etch rate decline with increasing feature aspect ratio. This book develops a comparative treatment between oxide/nitride (ON) and oxide/polysilicon (OPOP) transport behavior. See Chapter 10.

**Averaged Selectivity ($S_{avg}$)** — The time-averaged, full-depth etch rate ratio between two materials across a complete channel hole etch, as distinct from instantaneous single-layer selectivity. For OPOP, $S_{avg}=\bar{R}_{ox}/\bar{R}_{poly}$. See Chapter 12.

**Bond Energy (Si-Si, Si-O, Si-N, Si-F, Si-Cl, Si-Br)** — The energy required to break a given chemical bond, used throughout this book as the first-principles basis for comparing oxide, nitride, and polysilicon etch reactivity. See Chapter 4, Part 6.

**Charging (Differential Charging)** — Net positive charge accumulation at the bottom of an extreme-aspect-ratio feature, from the imbalance between directionally-constrained ion flux and more isotropic electron flux. This book develops how polysilicon's semiconducting nature partially, intermittently mitigates this mechanism relative to a fully dielectric sidewall. See Chapter 11.

**Combined-Exposure Testing** — Accelerated materials testing protocol specific to OPOP, characterizing chamber material and consumable component behavior under alternating fluorocarbon and halogen chemistry exposure, as distinct from single-chemistry-family qualification. See Chapter 8, Part 5.

**Dual Process Window** — The characterization finding that OPOP channel hole etch requires two independently mapped pressure-power-bias process windows (one per layer type), connected through shared reactor hardware constraints and transition dynamics. See Chapter 7.

**Grain Boundary** — The interface between adjacent crystalline grains in polycrystalline polysilicon, presenting structurally disrupted, often dopant-segregated material with distinct etch rate from grain interiors. See Chapter 2, Part 2.

**Halogen Chemistry** — Chlorine (Cl2) and hydrogen bromide (HBr) based plasma etch chemistry, the conventional choice for polysilicon etch, used in OPOP channel hole etch for polysilicon-layer intervals in place of fluorocarbon chemistry. See Chapter 3.

**HBr (Hydrogen Bromide)** — A halogen etch gas providing gentler, more profile-controllable polysilicon etch than Cl2 alone, at the cost of SiBr4 byproduct's lower volatility. See Chapter 3, Section 2.2; Chapter 6, Part 3.

**Intrinsic Selectivity Contrast** — The etch rate ratio between two materials under a given chemistry absent any deliberate suppression, used to describe OPOP's larger oxide/polysilicon contrast relative to ON's oxide/nitride contrast. See Chapter 1, Chapter 12, Part 1.

**ON (Oxide/Nitride)** — The dominant 3D NAND sacrificial stack approach, using silicon nitride as the sacrificial layer, treated throughout this book as the comparative baseline. (Developed in full in general 3D NAND etch literature; referenced here comparatively.)

**OPOP (Oxide-Polysilicon-Oxide-Polysilicon)** — The sacrificial stack variant using polysilicon rather than nitride as the sacrificial layer removed and replaced with metal word lines. The subject of this book.

**Oxyhalide Passivation Layer** — The thin silicon oxyhalide/oxychloride film forming on polysilicon sidewalls during halogen-chemistry etch, providing sidewall protection analogous in function, but chemically distinct, from fluorocarbon polymer passivation. See Chapter 4, Section 3.2.

**RC Time Constant (Charging Context)** — The characteristic time for accumulated sidewall charge to dissipate through a semiconducting polysilicon layer's bulk conductivity, a quantity this book estimates illustratively for polysilicon sidewalls. See Chapter 11, Part 5.

**Sequential Chemical Attack Synergy** — A combined-exposure degradation mechanism in which prior exposure to one chemistry family alters a surface's vulnerability to subsequent exposure to the other, requiring dedicated testing to characterize. See Chapter 8, Section 1.2.

**SiBr4** — The primary silicon bromide etch byproduct of HBr-chemistry polysilicon etch, notable for its markedly lower volatility (boiling point 153°C) relative to SiF4 or SiCl4, requiring dedicated thermal management. See Chapter 3, Section 4.2; Chapter 6, Part 3.

**Transport Probability ($K(AR,\gamma)$)** — The Knudsen-regime probability that a gas molecule entering a feature's top opening reaches the bottom without sidewall consumption, as a function of aspect ratio and species-specific sticking probability $\gamma$. This book treats halogen-species $\gamma$ values as carrying wider characterization uncertainty than fluorocarbon-species values. See Chapter 10, Part 1-2.

**$\gamma$ (Sidewall Sticking/Reaction Probability)** — The probability that a neutral species is consumed (reacts or sticks) at each sidewall collision within a feature, a key species-specific parameter in the Knudsen transport framework. See Chapter 10.
