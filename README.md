# 🦠 Disease Burden Analysis — Cameroon vs Sub-Saharan Africa
### Malaria, HIV/AIDS & Tuberculosis: trends, comparisons, and SDG 3 tracking

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/YOUR_USERNAME/cameroon-disease-burden-analysis/blob/main/cameroon_disease_burden.ipynb)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Data: World Bank](https://img.shields.io/badge/Data-World%20Bank%20Open%20Data-blue.svg)](https://data.worldbank.org)

---

## Overview

Sub-Saharan Africa carries a disproportionate share of the global burden of malaria, HIV/AIDS, and tuberculosis. This project uses **World Bank Open Data** to analyse Cameroon's disease burden trajectory from 2000 to 2022, benchmark it against the Sub-Saharan Africa regional average, and surface insights relevant to health governance, SDG 3 monitoring, and evidence-based advocacy.

The analysis goes beyond charting: it constructs a **Normalised Disease Burden Index (NDBI)** across six burden dimensions, explores correlations between health spending and disease outcomes, and produces an SDG 3 target scorecard with current trajectory status.

---

## Indicators covered

| Disease | Indicator | Code |
|---------|-----------|------|
| Malaria | Incidence per 1,000 at risk | SH.MLR.INCD.P3 |
| Malaria | Deaths per 100,000 | SH.MLR.MORT.P3 |
| Malaria | ITN usage, children (%) | SH.MLR.NETS.ZS |
| HIV | Prevalence, adults 15-49 (%) | SH.DYN.AIDS.ZS |
| HIV | ART coverage (%) | SH.HIV.ARTC.ZS |
| HIV | New infections per 1,000 | SH.HIV.INCD.ZS |
| TB | Incidence per 100,000 | SH.TBS.INCD |
| TB | Treatment success rate (%) | SH.TBS.CURE.ZS |
| TB | Mortality excl. HIV (per 100k) | SH.TBS.MORT |
| System | Health expenditure per capita (USD) | SH.XPD.CHEX.PC.CD |
| System | Physicians per 1,000 | SH.MED.PHYS.ZS |

---

## What this project demonstrates

| Skill | Detail |
|-------|--------|
| **Live API integration** | 11 indicators fetched directly from World Bank API via `wbgapi` |
| **Time-series analysis** | 22-year trend analysis with Cameroon vs SSA comparison |
| **Index construction** | Normalised Disease Burden Index across 6 burden dimensions |
| **Correlation analysis** | Pearson r heatmap — all 11 indicators, 2000–2022 |
| **Policy framing** | SDG 3 target scorecard with on-track / below-target status |
| **Excel export** | 5-sheet workbook: latest indicators, SDG scorecard, time series |

---

## Visualisations

7 publication-quality charts:
1. 6-panel overview grid — all key indicators, Cameroon vs SSA
2–4. Disease deep-dives — Malaria, HIV, TB (shaded area trend lines)
5. **Radar/spider chart** — Normalised Disease Burden Index
6. Pearson r correlation heatmap — all 11 indicators
7. SDG 3 scorecard table (colour-coded green/red by status)

---

## Normalised Disease Burden Index

```
NDBI = mean of normalised scores across:
  ├── Malaria Incidence
  ├── Malaria Deaths
  ├── HIV Prevalence
  ├── New HIV Infections
  ├── TB Incidence
  └── TB Mortality
```

Higher score = higher relative burden. Allows cross-disease comparison on a common scale.

---

## SDG 3 target tracking

| Indicator | 2030 Target | Status |
|-----------|------------|--------|
| ART Coverage | 95% (UNAIDS 95-95-95) | Monitor |
| TB Incidence | <10 per 100k | Below target |
| TB Treatment Success | 90% (WHO End TB) | Monitor |

---

## Quick start

```bash
pip install wbgapi pandas matplotlib seaborn openpyxl xlsxwriter
jupyter notebook cameroon_disease_burden.ipynb
```

---

## Planned extensions

- Sub-national analysis using DHS and MICS survey data
- ARIMA / Prophet forecasting to project 2030 indicator values
- Governance overlay — disease burden vs transparency indices
- Streamlit deployment for ministry and NGO use

---

**Author:** Pantouin Adjinsala · University Lecturer & Civic Tech Contributor, AfricTivistes CitizenLab Cameroon  
**Data:** World Bank Open Data (CC BY 4.0) · WHO Global Health Observatory  
**Part of:** [AI for Social Good portfolio](https://github.com/P-Adjinsala/padjinsala)
