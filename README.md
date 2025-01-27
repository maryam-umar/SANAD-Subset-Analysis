# Epilepsy Analysis

![Science] https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExbG9hbGpibWRwZWxtd3ZocWVtdTRoc3lyMHNuZXBmNzlzOTF0cDMxOCZlcD12MV9naWZzX3NlYXJjaCZjdD1n/QC7UQbxq89MnL9r6AN/giphy.gif

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

## **References**
1. Nevitt SJ, Tudur Smith C, Weston J, Marson AG. Lamotrigine versus carbamazepine monotherapy for epilepsy: an individual participant data review. Cochrane Database Syst Rev. 2018 Jun 28;2018(6):CD001031.
   
2. Wickham H, François R, Henry L, Müller K, Vaughan D (2023). dplyr: A Grammar of Data Manipulation. R package version 1.1.4, https://CRAN.R-project.org/package=dplyr.
   
3. Therneau T (2024). A Package for Survival Analysis in R. R package version 3.7-0, https://CRAN.R-project.org/package=survival.

4. Kassambara A, Kosinski M, Biecek P (2024). survminer: Drawing Survival Curves using 'ggplot2'. R package version 0.5.0, https://CRAN.R project.org/package=survminer.

5. H. Wickham. ggplot2: Elegant Graphics for Data Analysis. Springer-Verlag New York, 2016.
   
6. R Core Team (2024). R: A Language and Environment for Statistical Computing. R Foundation for Statistical Computing, Vienna, Austria. https://www.R-project.org/.
