# Survival analysis: time to re-arrest after prison

Challenge of the Semillero de Analítica de Datos (Universidad EIA), 2026-1. Complete survival analysis with `lifelines` on the `rossi` dataset (432 people followed 52 weeks after leaving prison).

## What I did
- Kaplan-Meier and log-rank test by financial aid
- Exponential and Weibull models, hazard and cumulative hazard
- Cox proportional hazards model and check of the assumptions

## Main results
- 74% of the people are not arrested in the 52 weeks.
- Log-rank p-value 0.050: weak evidence that financial aid reduces recidivism.
- Weibull (rho = 1.37, the risk grows over time) fits better than the exponential (AIC 1397 vs 1406).
- Cox: previous convictions increase the risk, age and financial aid reduce it (concordance 0.64). `age` and `wexp` do not meet the proportional hazards assumption.

The same tools are used for customer churn, time to default in credit risk and lapse of insurance policies.

## How to run

```
pip install lifelines pandas numpy matplotlib seaborn
jupyter notebook survival_analysis_rossi.ipynb
```

---
Alejandro Lezcano Osorio | Universidad EIA (Colombia) and Rennes School of Business (France)
