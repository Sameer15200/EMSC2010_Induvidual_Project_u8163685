# Cenozoic Silicate Weathering and Carbon Isotope Dynamics
## EMSC2010 — Individual Data Analysis Project | u8163685 | ANU 2026

---

## Research Question

How does the statistical relationship between seawater ⁸⁷Sr/⁸⁶Sr (silicate
weathering proxy) and benthic δ¹³C vary across the full Cenozoic, with the
PETM excursion removed, and within the Oligocene–Mid-Miocene interval (34–15 Ma)?

---

## Open in Colab

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Sameer15200/EMSC2010_Induvidual_Project_u8163685/blob/main/notebooks/EMSC2010_FINAL_COMPLETE_u8163685.ipynb)

> If the GitHub notebook preview shows an error, use the Colab link above directly.

---

## Analytical Approach

This project runs **three complete Bayesian linear regression models** using PyMC,
comparing how the ⁸⁷Sr/⁸⁶Sr–δ¹³C relationship changes across Cenozoic time intervals:

| Model | Dataset | Purpose |
|-------|---------|---------|
| Model 1 | Full Cenozoic (0–66 Ma, n=67) | Long-term baseline relationship |
| Model 2 | PETM-exempt (54–58 Ma removed, n=62) | Robustness / sensitivity check |
| Model 3 | Oligocene–Mid-Miocene (34–15 Ma, n=20) | Focused positive-coupling interval |

A **posterior comparison figure** plots all three β posteriors on the same axis,
directly visualising how the Sr–δ¹³C coupling evolves across Cenozoic time intervals.

---

## Key Results

| Model | Pearson r | β mean | 94% HDI | P(β<0) | ΔWAIC | Verdict |
|-------|-----------|--------|---------|--------|-------|---------|
| Full Cenozoic | −0.514 (p<0.001) | −0.507 | [−0.712, −0.304] | 100% | +9.0 | Strong evidence |
| PETM-exempt | −0.513 (p<0.001) | −0.503 | [−0.710, −0.301] | 100% | +8.2 | Meaningful evidence |
| Oligocene–Miocene | +0.214 (ns) | +0.202 | [−0.45, +0.85] | ~25% | −0.6 | No evidence |

**Core finding:** The ⁸⁷Sr/⁸⁶Sr–δ¹³C relationship is **time-dependent and
non-stationary**. A strong negative coupling dominates the full Cenozoic record
(β = −0.507, P(β<0) = 100%), driven by the Neogene divergence between rising
⁸⁷Sr/⁸⁶Sr and declining δ¹³C after the Mid-Miocene Carbon Optimum (~15 Ma).
This result is robust to PETM removal (β barely changes). Within the
Oligocene–Mid-Miocene interval (34–15 Ma), the relationship shifts toward
positive (β = +0.202), consistent with theoretical predictions of simultaneous
Himalayan uplift and Antarctic glaciation driving both proxies upward together —
but this signal is statistically uncertain at 1 Myr resolution.

---

## Repository Structure
EMSC2010_Induvidual_Project_u8163685/
├── README.md
├── data/
│   └── EMSC2010_Data_Package_u8163685.xlsx   ← all datasets and results
├── notebooks/
│   └── EMSC2010_FINAL_COMPLETE_u8163685.ipynb ← main analysis notebook
└── figures/                                   ← saved automatically on run

---

## How to Run

1. Click the **Open in Colab** badge above
2. Run the first cell to install PyMC and ArviZ (~2 min)
3. Run all remaining cells in order from top to bottom
4. The four MCMC sampling cells each take ~2–4 minutes
5. All figures save automatically to `figures/`

> Note: `progressbar=False` is set in all `pm.sample()` calls so the notebook
> renders correctly in GitHub without widget metadata errors.

---

## Data Sources

- **δ¹³C:** Westerhold et al. (2020) CENOGRID — *Science* 369:1383
  [doi:10.1594/PANGAEA.917660](https://doi.org/10.1594/PANGAEA.917660)
- **⁸⁷Sr/⁸⁶Sr:** McArthur et al. (2020) — *Geological Time Scale 2020*, Elsevier

---

## References

- Caves, J.K., et al. (2016). Cenozoic carbon cycle imbalances and a variable
  weathering feedback. *Earth and Planetary Science Letters*, 450, 152–163.
- McArthur, J.M., et al. (2020). Strontium Isotope Stratigraphy. In:
  *Geological Time Scale 2020*. Elsevier, pp. 211–238.
- Westerhold, T., et al. (2020). An astronomically dated record of Earth's
  climate over the last 66 Ma. *Science*, 369(6509), 1383–1387.
- Salvatier, J., et al. (2016). PyMC3. *PeerJ Computer Science*, 2, e55.
- Kumar, R., et al. (2019). ArviZ. *JOSS*, 4(33), 1143.

---

## Student

u8163685 | Australian National University | EMSC2010 2026
