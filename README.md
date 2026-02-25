# Causal Inference: Low Income and HbA1c Levels (NHANES)

This project estimates the causal effect of low income (Income-to-Poverty Ratio < 1.0) on glycemic control (HbA1c levels) using nationally representative data from the NHANES 2011–2012 survey. Two independent causal inference methods — propensity score matching (PSM) and inverse probability of treatment weighting (IPTW) — are applied to remove demographic confounding and estimate a defensible average treatment effect.

## Objectives

- Estimate the causal impact of poverty on HbA1c levels after adjusting for demographic confounders
- Demonstrate valid causal structure: low income plausibly affects diet quality, healthcare access, medication adherence, and stress — all of which influence blood glucose
- Validate covariate balance using standardized mean differences (love plot)
- Deliver honest, interpretable results with real-world relevance for health equity and diabetes prevention policy

## Tools and Methods

- Python (pandas, numpy, scikit-learn, seaborn, scipy)
- Logistic regression for propensity score estimation
- Propensity Score Matching (1:1 nearest neighbor, without replacement)
- IPTW with stabilized weights and 1st/99th percentile trimming
- Bootstrapped 95% confidence intervals on ATE estimates
- Love plot for covariate balance assessment before and after matching

## Dataset

- NHANES 2011–2012 (Demographics, Diabetes Questionnaire, Lab Results)
- Publicly available from CDC: https://www.cdc.gov/nchs/nhanes/

## Results

| Method | ATE on HbA1c | 95% CI |
|--------|-------------|--------|
| Propensity Score Matching | -0.009 | (-0.152, 0.134) |
| IPTW (Stabilized) | 0.019 | (-0.078, 0.120) |

## Key Insight

After adjusting for demographic confounders (age, gender, race, education), no statistically significant difference in HbA1c was found between low-income and higher-income individuals — both CIs include zero. This suggests the raw disparity observed between income groups is largely attributable to demographic factors rather than income status itself. The finding highlights the critical importance of causal methods: without adjustment, a spurious association driven by confounding could be mistaken for a direct effect of poverty on glycemic health.
