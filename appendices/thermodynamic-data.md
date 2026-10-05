# Appendix A: Thermodynamic & Material Property Data Tables

This appendix consolidates material and thermodynamic property data referenced throughout the main text. Values are representative/illustrative, drawn from general materials science and plasma processing literature; production process characterization should rely on fab- and tool-specific measured data, consistent with this book's repeated caution against treating generic values as production-ready specifications.

---

## A.1 Core OPOP Stack Material Properties

| Property | SiO2 (PECVD) | Polysilicon (LPCVD) | Polysilicon (PECVD) |
|---|---|---|---|
| Density (g/cm³) | 2.1-2.2 | ~2.30-2.33 (near bulk Si density) | More variable, process-dependent |
| Deposition temperature | N/A (oxide-specific process) | 580-650°C | 300-450°C |
| Structural order | Amorphous | Polycrystalline | Polycrystalline (grain size generally smaller than LPCVD) |
| Typical intrinsic stress | -300 to +300 MPa | Generally lower magnitude, grain-structure dependent | More variable |
| Doping range (as deposited or implanted) | N/A (dielectric) | $10^{18}$-$10^{21}\ \text{cm}^{-3}$ class, process dependent | Similar range |

## A.2 Bond Energy Reference Table

| Bond | Approximate Bond Energy (kJ/mol) | Relevance |
|---|---|---|
| Si-O (in SiO2) | ~452 | Oxide network strength |
| Si-N (in Si3N4) | ~335 | Nitride reference (ON comparison) |
| Si-Si (polysilicon network) | ~222-310 | Polysilicon network strength; central to this book's reactivity comparisons |
| Si-F | ~565 | Fluorination product; explains fluorine's excessive silicon reactivity |
| Si-Cl | ~381 | Chlorination product |
| Si-Br | ~310 | Bromination product |

## A.3 Halogen and Fluorocarbon Species Reference

| Species | Formula | Molecular Weight (g/mol) | Role |
|---|---|---|---|
| Chlorine | Cl2 | 70.9 | Primary polysilicon etchant |
| Hydrogen bromide | HBr | 80.9 | Profile-controlling polysilicon etchant |
| Sulfur hexafluoride | SF6 | 146.1 | Polysilicon etch rate modifier (OPOP context, distinct from its general 3D NAND oxide-chemistry role) |
| Octafluorocyclobutane | C4F8 | 200.0 | Oxide-layer polymer-forming chemistry |
| Hexafluorobutadiene | C4F6 | 162.0 | Oxide-layer maximum-passivation chemistry |

## A.4 Byproduct Volatility Reference

| Byproduct | Source | Boiling/Sublimation Point | Volatility Category |
|---|---|---|---|
| SiF4 | Fluorine + Si (oxide layers) | -86°C | Highest |
| SiCl4 | Chlorine + Si (polysilicon layers) | 57.6°C | Moderate |
| SiBr4 | Bromine + Si (polysilicon layers) | 153°C | Lowest in this comparison; requires dedicated thermal management |
| CO/CO2 | Fluorocarbon polymer oxidation | -192°C / -78.5°C | Highest |
| HCl, HBr (unreacted) | Halogen chemistry byproducts | Gas at room temperature | High |

## A.5 Physical Constants Used in This Book's Worked Examples

| Constant | Symbol | Value |
|---|---|---|
| Vacuum permittivity | $\epsilon_0$ | 8.85×10⁻¹² F/m |
| Elementary charge | $e$ | 1.602×10⁻¹⁹ C |
| Boltzmann constant | $k_B$ | 1.381×10⁻²³ J/K |
| Gas constant | $R$ | 8.314 J/(mol·K) |
| Representative heavily-doped polysilicon resistivity | $\rho$ | ~1×10⁻³ Ω·cm (illustrative) |

---

*Note on data provenance: these values are representative, order-of-magnitude-correct figures drawn from general materials science, plasma processing, and logic polysilicon etch literature, intended to support this book's worked examples. As Chapter 10 and Chapter 12 both emphasize, halogen-species transport and reaction parameters specific to extreme-aspect-ratio OPOP channel hole etch carry wider characterization uncertainty than the equivalent, more extensively published fluorocarbon-chemistry values, and direct experimental characterization is recommended before relying on these figures for production process design.*
