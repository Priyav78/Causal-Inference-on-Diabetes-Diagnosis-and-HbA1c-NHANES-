# Causal Inference on Diabetes and HbA1c using NHANES Data

This project estimates the causal effect of diabetes diagnosis on glycemic control (HbA1c levels) using nationally representative data from the NHANES survey. We apply advanced causal inference methods—including propensity score matching (PSM), inverse probability of treatment weighting (IPTW), and regression adjustment—to reduce bias and estimate counterfactual outcomes.

## Objectives

- Quantify the impact of diabetes diagnosis on HbA1c levels
- Control for confounding using demographic and clinical covariates
- Demonstrate the importance of causal vs. correlational analysis in public health data
- Deliver interpretable results with real-world relevance for clinical decision-making and health equity

## Tools and Methods

- Python (pandas, statsmodels, sklearn)
- Propensity Score Modeling
- IPTW (Inverse Probability of Treatment Weighting)
- Average Treatment Effect (ATE) Estimation
- Visualization of covariate balance and treatment effects

## Dataset

- NHANES 2017-2020 datasets (DEMO, DIQ, GHB files)
- Publicly available from CDC: https://www.cdc.gov/nchs/nhanes/

## Key Insight

Causal methods revealed a statistically significant difference in HbA1c levels attributable to diabetes diagnosis status—highlighting gaps in metabolic health and treatment outcomes across population groups.