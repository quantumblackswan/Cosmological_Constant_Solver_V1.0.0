# Nature Astronomy Submission Checklist

**Paper:** Holographic Resolution of the Hubble Tension: A Six-Dataset,
First-Principles Determination of the Cosmological Constant
from Galaxy Rotation Curves to the CMB Power Spectrum

**Author:** Kevin Henry Miller | Kevin@qbondnetwork.com | ORCID: 0009-0007-7286-3373

**Date:** March 3, 2026

---

## Manuscript Requirements

- [x] **Format:** Single-column, 12pt, double-spaced (article class, setspace)
- [x] **Length:** ~6,200 words main text + Methods (~800 words) — within Nature Astronomy limit (6,000 words main + Methods)
  - Action: if word count too high, trim Introduction (target ~500 words) and Discussion (~350 words)
- [x] **Abstract:** 200 words (count with `texcount`)
- [x] **Line numbers:** Enabled via `lineno` package (required for peer review)
- [x] **Title:** ≤ 150 characters
- [x] **Author list:** Single author, affiliation, email, ORCID
- [x] **Methods section:** Present, at end of main text, not included in word count
- [x] **Data availability statement:** Present
- [x] **Code availability statement:** Present
- [x] **Author contributions:** Present
- [x] **Competing interests:** Declared ("no competing interests")
- [x] **References:** Numbered [1]–[N], Nature format (Author, journal, vol, page, year)
- [x] **SI:** Separate file, sections labeled S1, S2..., tables S1, S2..., figures S1, S2...

---

## Figures

| Figure | File | Status |
|--------|------|--------|
| Fig 1: H0 comparison across probes | `fig1_h0_comparison.pdf` | ⬜ GENERATE |
| Fig 2: MCMC 9-parameter corner plot | `fig2_corner_mcmc.pdf` | ⬜ COPY from `fig48_mcmc_v9_corner.png` |
| Fig 3: Cross-scale residuals | `fig3_crossscale.pdf` | ⬜ GENERATE |
| Fig 4: Lambda stability vs version | `fig4_lambda_stability.pdf` | ⬜ GENERATE |

**Figure generation scripts to write:**
- `figures/make_fig1_h0_comparison.py` — horizontal bar chart of H0 measurements
- `figures/make_fig3_crossscale.py` — three-panel residual plot
- `figures/make_fig4_stability.py` — Lambda vs N_data stability plot

**Nature Astronomy figure requirements:**
- Min 300 dpi at final print size
- PDF or EPS preferred for line art; TIFF for photos
- Max width: 89mm (single column) or 183mm (double column)
- Font size ≥ 7pt in figure
- Axes labels in sentence case
- No box-and-whisker plots with hidden data

---

## Supplementary Figures

| Figure | Status |
|--------|--------|
| Fig S1: Per-dataset chi2/N vs redshift | ⬜ GENERATE |
| Fig S2: MCMC walker traces | ⬜ GENERATE |
| Fig S3: Representative SPARC fits | ⬜ GENERATE |
| Fig S4: Neutrino mass chi2 scan | ⬜ GENERATE |

---

## File Inventory for Submission Portal

```
main_manuscript.tex               ← Main manuscript LaTeX source
main_manuscript.pdf               ← Compiled PDF (compile command below)
supplementary_information.tex     ← SI LaTeX source
supplementary_information.pdf     ← Compiled SI PDF
cover_letter.txt                  ← Cover letter to editor
references.bib                    ← BibTeX bibliography (create or use inline \thebibliography)
figures/
  fig1_h0_comparison.pdf          ← Figure 1
  fig2_corner_mcmc.pdf            ← Figure 2 (copy of fig48_mcmc_v9_corner.png)
  fig3_crossscale.pdf             ← Figure 3
  fig4_lambda_stability.pdf       ← Figure 4
```

---

## Compile Instructions

```powershell
cd "C:\Users\CCRN4\OneDrive\Desktop\TQS\TQS\HUBBLE_TENSION_NATURE_ASTRONOMY"
pdflatex -interaction=nonstopmode main_manuscript.tex
pdflatex -interaction=nonstopmode main_manuscript.tex
pdflatex -interaction=nonstopmode supplementary_information.tex
pdflatex -interaction=nonstopmode supplementary_information.tex
```

(Two pdflatex passes needed for correct cross-references and line numbers.)

If bibliography issues arise (no .bib file present), the inline `\thebibliography`
environment in the .tex file takes precedence.

---

## Submission Portal

**URL:** https://mts.nature.com/cgi-bin/main.plex (Nature Manuscript Tracking System)

**Steps:**
1. Create account or log in at https://mts.nature.com
2. Select Journal: **Nature Astronomy**
3. Article Type: **Article**
4. Upload files in order:
   - Manuscript (main_manuscript.pdf and .tex)
   - Supplementary Information (supplementary_information.pdf)
   - Cover letter (cover_letter.txt or paste text)
   - Individual figure files
5. Enter metadata:
   - Title (copy from manuscript)
   - Abstract (copy from manuscript, plain text, ≤200 words)
   - Keywords: cosmological constant, Hubble tension, holographic principle, dark energy, CMB
   - Subject area: Cosmology
6. Suggest reviewers (4 suggested in cover letter)
7. Review and submit

---

## Post-Submission

- [ ] Upload preprint to arXiv (astro-ph.CO)
- [ ] Deposit MCMC chain + code to Zenodo (get DOI before arXiv submission)
- [ ] Update Zenodo DOI in manuscript before final submission
- [ ] Tweet/post to astronomy community

---

## Word Count Targets

| Section | Target | Status |
|---------|--------|--------|
| Abstract | ≤200 words | ⬜ COUNT |
| Introduction | ~600 words | ⬜ COUNT |
| Theory | ~500 words | ⬜ COUNT |
| Data & Methods | ~600 words | ⬜ COUNT |
| Results | ~700 words | ⬜ COUNT |
| Discussion | ~400 words | ⬜ COUNT |
| Conclusion | ~200 words | ⬜ COUNT |
| Methods section | ~800 words | ⬜ COUNT |
| Total main text | ≤6,000 words | ⬜ COUNT |

Run word count: `texcount -sum main_manuscript.tex` (if texcount installed)

---

*Checklist version: 1.0 — March 3, 2026*
