# Causal Inference: Effect of Low Income on HbA1c Levels (NHANES)

This project estimates the causal effect of low income (Income-to-Poverty Ratio < 1.0) on glycemic control (HbA1c levels) using nationally representative data from the NHANES 2011–2012 survey. Two independent causal inference methods — propensity score matching (PSM) and inverse probability of treatment weighting (IPTW) — are applied to remove demographic confounding and estimate a defensible average treatment effect.

## Objectives

- Quantify the causal impact of poverty on HbA1c levels after adjusting for demographic confounders
- Demonstrate valid causal structure: low income plausibly affects diet quality, healthcare access, medication adherence, and stress — all of which influence blood glucose
- Validate covariate balance using standardized mean differences (love plot)
- Deliver interpretable results with real-world relevance for health equity and diabetes prevention policy

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

## Key Insight

After adjusting for age, gender, race, and education through two independent causal methods, low-income individuals exhibit meaningfully higher HbA1c levels than demographically comparable higher-income individuals. The consistency of the ATE estimate across PSM and IPTW strengthens confidence in the finding and supports targeting low-income populations in diabetes prevention and early screening programs.
