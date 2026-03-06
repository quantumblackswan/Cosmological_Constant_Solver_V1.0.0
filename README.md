# Cosmological Constant Solver V1.0.0

**Holographic Resolution of the Hubble Tension: A Six-Dataset,
First-Principles Determination of the Cosmological Constant
from Galaxy Rotation Curves to the CMB Power Spectrum**

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.18894022.svg)](https://doi.org/10.5281/zenodo.18894022)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![ORCID](https://img.shields.io/badge/ORCID-0009--0007--7286--3373-green)](https://orcid.org/0009-0007-7286-3373)

---

## Author

**Kevin Henry Miller**  
Founder and President, Q-Bond Network DeSCI DAO, LLC  
965 Garnet Drive, Acworth, Georgia 30101, USA  
✉ Kevin@qbondnetwork.com  
🔗 ORCID: [0009-0007-7286-3373](https://orcid.org/0009-0007-7286-3373)  
📦 Zenodo: [10.5281/zenodo.18894022](https://doi.org/10.5281/zenodo.18894022)

---

## Overview

This repository contains the complete manuscript, supplementary information,
figures, and analysis code for the paper submitted to *Nature Astronomy*
(March 2026).

### What this paper solves

The **Hubble tension** — a 4–6σ discrepancy between CMB-inferred
H₀ ≈ 67 km/s/Mpc (Planck) and distance-ladder H₀ ≈ 73 km/s/Mpc (SH0ES) —
is one of the most prominent open problems in cosmology.

This work:

1. **Derives Λ from first principles** via the Cohen–Kaplan–Nelson holographic
   UV–IR collapse bound. The derivation is a theorem with zero free parameters:
   ρ_crit/ρ_P = (3/8π)(l_P/r_H)² — explaining the notorious 10¹²² cosmological
   constant problem as a wrong degree-of-freedom counting (volume vs. surface).

2. **Fits six independent datasets simultaneously** across six orders of magnitude
   in physical scale, using a single open-source pipeline:
   | Dataset | Points |
   |---------|--------|
   | Pantheon+SH0ES Type Ia supernovae | 1,701 |
   | DES-SN5YR distance moduli | 1,820 |
   | DESI DR2 BAO measurements | 12 |
   | SPT-3G TT/TE/EE CMB bandpowers | 196 |
   | ACT DR6 TT/TE/EE CMB bandpowers | 122 |
   | SPARC galaxy rotation curves | 175 |
   | **Total** | **3,851** |

3. **Produces the result:**
   - Λ = (1.117 ± 0.022) × 10⁻⁵² m⁻²
   - H₀ = 68.09 ± 0.50 km/s/Mpc
   - Ω_m = 0.3101 ± 0.0048
   - χ²/dof = 0.9662 across 3,851 data points

---

## Repository Structure

```
Cosmological_Constant_Solver_V1.0.0/
├── README.md                      ← this file
├── LICENSE                        ← MIT License
├── CITATION.cff                   ← machine-readable citation
├── CHANGELOG.md                   ← version history
├── CONTRIBUTORS.md                ← contributor list
├── .gitignore                     ← LaTeX/Python ignores
│
├── main_manuscript.tex            ← LaTeX source (Nature Astronomy format)
├── main_manuscript.pdf            ← compiled manuscript (17 pages)
│
├── supplementary_information.tex  ← LaTeX source for SI
├── supplementary_information.pdf  ← compiled SI (10 pages)
│
├── cover_letter.txt               ← cover letter to editors
├── submission_checklist.md        ← submission requirements
├── README_submission.md           ← compile instructions
│
└── figures/
    ├── make_all_figures.py        ← generates Figs 1, 3, 4
    ├── fig1_h0_comparison.pdf     ← H₀ comparison (6 probes)
    ├── fig2_corner_mcmc.pdf       ← 9-param MCMC corner plot
    ├── fig3_crossscale.pdf        ← cross-scale residuals
    └── fig4_lambda_stability.pdf  ← Λ stability v4→v9
```

---

## Quick Start

```bash
# Clone
git clone https://github.com/KevinHenryMiller/Cosmological_Constant_Solver_V1.0.0.git
cd Cosmological_Constant_Solver_V1.0.0

# Generate figures (requires numpy, matplotlib)
pip install numpy matplotlib scipy
python figures/make_all_figures.py

# Compile manuscript (requires LaTeX: MiKTeX or TeX Live)
pdflatex main_manuscript.tex
pdflatex main_manuscript.tex          # second pass for references

# Compile supplementary information
pdflatex supplementary_information.tex
pdflatex supplementary_information.tex
```

---

## Key Results

| Parameter | Value | Dataset |
|-----------|-------|---------|
| Λ | (1.117 ± 0.022) × 10⁻⁵² m⁻² | Joint 6-dataset |
| H₀ | 68.09 ± 0.50 km/s/Mpc | Joint 6-dataset |
| Ω_m | 0.3101 ± 0.0048 | Joint 6-dataset |
| χ²/dof | 0.9662 | 3,851 data points |
| ΔBIC vs holographic DE | +57.9 | Decisive rejection |

MCMC: 64 walkers × 600 steps, 50.67 GPU-hours on RunPod A100s.

---

## Ten Falsifiable Predictions

1. DESI Year-5 BAO will find H₀_eff = 68.0–68.5 km/s/Mpc
2. Euclid WL will measure Ω_m = 0.310 ± 0.002
3. Simons Observatory Nₑff constraint will rule out early dark energy at > 3σ
4. ACT DR7 H₀ will be ≤ 68.5 km/s/Mpc
5. JWST Cepheid re-calibration will lower SH0ES H₀ by ≥ 2 km/s/Mpc
6. Einstein Telescope will confirm GW H₀ = 68 ± 1 km/s/Mpc
7. SPT-3G final power spectra will confirm lens amplitude consistent with Planck
8. DESI Year-5 will find w = −1.000 ± 0.020 (no dark energy dynamics)
9. SPARC-II extensions will maintain RAR with scatter < 0.05 dex
10. Holographic dark energy (Li 2004) will remain disfavoured at ΔBIC > 50

---

## Citation

If you use this work, please cite:

```bibtex
@article{Miller2026HubbleTension,
  author       = {Miller, Kevin Henry},
  title        = {Holographic Resolution of the Hubble Tension: A Six-Dataset,
                  First-Principles Determination of the Cosmological Constant
                  from Galaxy Rotation Curves to the CMB Power Spectrum},
  journal      = {Nature Astronomy (submitted)},
  year         = {2026},
  month        = {March},
  doi          = {10.5281/zenodo.18894022},
  url          = {https://doi.org/10.5281/zenodo.18894022},
  note         = {Zenodo preprint v1.0.0},
  orcid        = {0009-0007-7286-3373},
}
```

Or use the [CITATION.cff](CITATION.cff) file for GitHub's "Cite this repository" button.

---

## License

Code: [MIT License](LICENSE) — © 2026 Kevin Henry Miller, Q-Bond Network DeSCI DAO, LLC  
Manuscript text: CC-BY 4.0 — free to share with attribution

---

## Acknowledgements

This work used:
- IBM Quantum Platform (ibm_marrakesh, 887+ jobs)
- RunPod A100 GPUs (50.67 GPU-hours MCMC)
- Pantheon+, DES, DESI, SPT-3G, ACT, and SPARC public data releases
- emcee (Foreman-Mackey et al.), candl, getdist, astropy, numpy, scipy, matplotlib

---

*Submitted to Nature Astronomy, March 2026*  
*© 2026 Kevin Henry Miller, Q-Bond Network DeSCI DAO, LLC*
