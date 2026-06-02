# Cenozoic Silicate Weathering and Carbon Isotope Dynamics
## EMSC2010 — Individual Data Analysis Project | u8163685 | ANU 2026

---

## Research Question

How does the statistical relationship between seawater ⁸⁷Sr/⁸⁶Sr (silicate 
weathering proxy) and benthic δ¹³C vary across the full Cenozoic, with the 
PETM excursion removed, and within the Oligocene–Mid-Miocene interval (34–15 Ma)?

---

## Analytical Approach

This project runs **three complete Bayesian linear regression models** using PyMC:

| Model | Dataset | Purpose |
|-------|---------|---------|
| Model 1 | Full Cenozoic (0–66 Ma, n=67) | Long-term baseline relationship |
| Model 2 | PETM-exempt (54–58 Ma removed, n=62) | Robustness / sensitivity check |
| Model 3 | Oligocene–Mid-Miocene (34–15 Ma, n=20) | Focused positive-coupling interval |

A **posterior comparison figure** plots all three β posteriors on the same axis, 
directly visualising how the Sr–δ¹³C coupling evolves across Cenozoic time intervals.

---

## Repository Structure
EMSC2010_Induvidual_Project_u8163685/
├── README.md
├── data/
│   └── EMSC2010_Data_Package_u8163685.xlsx   ← all datasets and results
├── notebooks/
│   └── EMSC2010_A3_FINAL_v3_u8163685.ipynb   ← main analysis notebook
└── figures/                                   ← saved automatically on run
## How to Run

Click the badge below to open the notebook directly in Google Colab:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sameer15200/EMSC2010_Induvidual_Project_u8163685/blob/main/notebooks/EMSC2010_A3_FINAL_v3_u8163685.ipynb)

1. Run the first cell to install PyMC and ArviZ
2. Run all remaining cells in order
3. The four MCMC sampling cells each take ~2–4 minutes

---

## Data Sources

- **δ¹³C:** Westerhold et al. (2020) CENOGRID — *Science* 369:1383 
  [doi:10.1594/PANGAEA.917660](https://doi.org/10.1594/PANGAEA.917660)
- **⁸⁷Sr/⁸⁶Sr:** McArthur et al. (2020) — *Geological Time Scale 2020*, Elsevier

---

## Key Results

*(Updated after running the notebook)*

| Model | β mean | 94% HDI | P(β>0) |
|-------|--------|---------|--------|
| Full Cenozoic | — | — | — |
| PETM-exempt | — | — | — |
| Oligocene–Miocene | — | — | — |
