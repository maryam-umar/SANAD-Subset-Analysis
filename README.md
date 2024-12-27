# Epilepsy Analysis

This repository contains a detailed statistical analysis of an epilepsy dataset, focusing on treatment outcomes and survival analysis. The goal is to evaluate the effectiveness of different treatments and their impact on seizure remission and withdrawal rates.

## Project Overview

This project involves:
- Logistic regression to analyze the relationship between treatment types and remission probability.
- Survival analysis using Kaplan-Meier and Cox proportional hazards models.
- Gender interaction models to assess differences in treatment effects.
- Competing risk analysis to understand withdrawal causes.

## Dataset

The dataset includes variables such as:
- `treat`: Treatment type (e.g., CBZ, LTG).
- `ageyr`: Age of participants in years.
- `sex`: Gender of participants.
- `withtime`: Time to event (e.g., withdrawal).
- `censall`: Censoring indicator.
- `wdlcode`: Withdrawal code indicating the reason for withdrawal.

## Key Findings

1. **Treatment Efficacy**:
   - Lamotrigine (LTG) showed a slight advantage over Carbamazepine (CBZ) in achieving 12-month seizure remission, but the difference was not statistically significant.

2. **Gender-Specific Analysis**:
   - Women on CBZ had the lowest probability of achieving remission, but overall, no significant differences were observed between genders.

3. **Survival Analysis**:
   - LTG had consistently lower withdrawal rates and fewer adverse events compared to CBZ, indicating better tolerability.

4. **Competing Risks**:
   - Lamotrigine had a significantly lower cumulative incidence of withdrawal due to adverse effects (UAE), making it a preferable treatment option.

## Visualizations

The analysis includes:
- Bar plots for predicted probabilities.
- ROC curves to evaluate model performance.
- Kaplan-Meier survival plots.
- Forest plots for odds ratios and hazard ratios.

## Tools and Libraries

The analysis was conducted in R using the following libraries:
- `ggplot2` for data visualization.
- `survival` and `survminer` for survival analysis.
- `cmprsk` for competing risk analysis.

## Limitations

- Other variables such as age and seizure frequency were not included in the models.
- Results are specific to the dataset used and may not generalize to broader populations.

