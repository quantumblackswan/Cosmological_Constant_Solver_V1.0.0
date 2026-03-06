# Changelog

All notable changes to this project will be documented in this file.
Format follows [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).

---

## [1.0.0] — 2026-03-06

### Added
- Initial public release of the Cosmological Constant Solver
- `main_manuscript.tex` / `main_manuscript.pdf` — 17-page Nature Astronomy format manuscript
- `supplementary_information.tex` / `supplementary_information.pdf` — 10-page SI
- `figures/make_all_figures.py` — reproduces Figs 1, 3, 4
- `figures/fig1_h0_comparison.pdf` — H₀ comparison across 6 probes
- `figures/fig2_corner_mcmc.pdf` — 9-parameter MCMC corner plot (64w × 600s, RunPod A100)
- `figures/fig3_crossscale.pdf` — cross-scale residuals (SN, BAO, CMB)
- `figures/fig4_lambda_stability.pdf` — Λ stability v4 → v9
- `cover_letter.txt` — Nature Astronomy cover letter
- `submission_checklist.md` — full submission requirements
- `README.md`, `CITATION.cff`, `LICENSE`, `CONTRIBUTORS.md` — GitHub standard docs

### Key Results (v1.0.0)
- Λ = (1.117 ± 0.022) × 10⁻⁵² m⁻² (6-dataset joint MCMC)
- H₀ = 68.09 ± 0.50 km/s/Mpc
- Ω_m = 0.3101 ± 0.0048
- χ²/dof = 0.9662 (3,851 data points)
- ΔBIC vs holographic DE: +57.9 (decisive rejection)
- Zenodo DOI: [10.5281/zenodo.18894022](https://doi.org/10.5281/zenodo.18894022)

### Author
Kevin Henry Miller, Founder and President, Q-Bond Network DeSCI DAO, LLC  
ORCID: 0009-0007-7286-3373

---

## [Unreleased]

- Post-submission edits based on Nature Astronomy referee comments
- arXiv preprint (astro-ph.CO) — ID pending
- MCMC chain deposition to Zenodo (separate record)
