# Appendix E: Charging & Thermal Calculations for Semiconducting Sacrificial Stacks

This appendix consolidates the worked charging and thermal calculation methods developed in Chapters 6, 8, and 11, presented as reusable calculation templates for process characterization.

---

## E.1 RC Discharge Time Constant for Semiconducting Polysilicon Sidewall

**Method** (Chapter 11, Part 5):

$$\tau_{RC} \approx R\cdot C, \qquad R\approx\rho\frac{L}{A}, \qquad C\approx\frac{\kappa\epsilon_0 A}{d}$$

**Worked template:**

| Input | Symbol | Example Value |
|---|---|---|
| Polysilicon resistivity (heavily doped) | $\rho$ | $1\times10^{-3}\ \Omega\cdot\text{cm}$ |
| Conduction path length (layer thickness) | $L$ | 30 nm |
| Charged surface patch area | $A$ | $10^{-12}\ \text{cm}^2$ |
| Oxyhalide layer thickness | $d$ | 2 nm |
| Oxyhalide dielectric constant | $\kappa$ | 4 |
| **Result: Resistance** | $R$ | **~3×10³ Ω** |
| **Result: Capacitance** | $C$ | **~1.77×10⁻¹⁸ F** |
| **Result: Time constant** | $\tau_{RC}$ | **~5.3×10⁻¹⁵ s (illustrative; treat with caution per Chapter 11, Section 5.6)** |

To use: substitute characterized doping-dependent resistivity and measured oxyhalide thickness; compare resulting $\tau_{RC}$ against relevant process timescales (RF period, pulsing period) to assess whether charge dissipation is plausibly fast relative to ongoing ion flux arrival — treating this as a dynamic balance problem, not a one-time discharge, per Chapter 11, Section 5.6's caution.

## E.2 SiBr4 Condensation Margin Estimate

**Method** (Chapter 6, Part 5):

Compare chamber wall/exhaust path temperature against SiBr4's boiling point (153°C), accounting for the Clausius-Clapeyron-driven steep vapor pressure drop near the boiling point.

**Worked template:**

| Species | Boiling Point | Representative Unheated Wall Temp | Margin |
|---|---|---|---|
| SiF4 | -86°C | 40-60°C | >120°C (no risk) |
| SiCl4 | 57.6°C | 40-60°C | Near/below boiling point (modest risk) |
| SiBr4 | 153°C | 40-60°C | ~90-110°C below boiling point (high risk without dedicated heating) |

To use: measure actual chamber wall and exhaust path temperatures at locations of interest; compare against this table to identify locations requiring dedicated thermal management per Chapter 6, Section 3.3.

## E.3 Gas Panel Architecture Purge Time Comparison

**Method** (Chapter 5, Part 6):

$$t_{purge} \approx \frac{n\times V_{line}}{Q_{purge}}\times(\text{unit conversion factor})$$

**Worked template:**

| Architecture | Line Volume | Illustrative Purge Time |
|---|---|---|
| Shared delivery path | 50 cm³ | ~3-4 s |
| Dedicated delivery paths (shared final segment only) | 8 cm³ | ~0.5-0.6 s |

To use: measure actual gas line volumes for your specific gas panel configuration; apply this method to estimate per-transition purge time and total cumulative overhead across a full stack's layer-pair count (Chapter 3, Section 5.2).

## E.4 Selectivity Suppression Factor Allocation

**Method** (Chapter 12, Part 5):

$$\text{Required suppression} = \frac{S_{intrinsic}}{S_{target}}$$

Allocate across chemistry blend, bias power, and doping level levers such that their product equals the required suppression factor.

**Worked template:**

| Input | Symbol | Example Value |
|---|---|---|
| Measured intrinsic selectivity | $S_{intrinsic}$ | 15:1 |
| Target bulk-etch selectivity | $S_{target}$ | 1.0 |
| **Result: Required suppression** | — | **15×** |

To use: substitute your own measured $S_{intrinsic}$ (Appendix D.3's reference range as a starting estimate) and target; allocate the resulting suppression factor across your characterized lever contributions following the structure in Chapter 12, Part 5.

## E.5 Lateral Diffusion-Limited Removal Time

**Method** (Chapter 14, Part 6):

$$t = \frac{x^2}{2D_{eff}}$$

**Worked template:**

| Input | Symbol | Example Value |
|---|---|---|
| Lateral clearing distance (block half-width) | $x$ | 3 µm |
| Effective diffusion coefficient (chemistry-specific) | $D_{eff}$ | Characterize per chemistry; illustrative TMAH value $3\times10^{-10}\ \text{cm}^2/\text{s}$ |
| **Result: Clearing time** | $t$ | **~150 s (illustrative)** |

To use: substitute your characterized $D_{eff}$ for the specific removal chemistry in use; apply to estimate structural vulnerability window duration per Chapter 14, Section 5.2-5.3.

---

*All templates in this appendix reproduce calculation methods developed in their referenced main-text chapters. Users should substitute characterized, tool-specific input values rather than relying on illustrative example values for actual process decisions.*
