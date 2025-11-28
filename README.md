**Analysis of Treatment Delay (42 Days) and Survival Outcomes in Salivary Gland Cancer**

This project explores the impact of delays in cancer therapy ( Treatment start > 42 days post diagnosis) on the survival outcomes compared to patients who receive timely treatment

**Hypothesis:** Patients who receive delayed treatment (Delay > 42 days) will have worse Overall Survival (OS) and Cancer-Specific Survival (CSS) outcomes compared to patients who receive timely treatment.

**Plan to Test Hypothesis:**
1. **Cox Proportional Hazards (Cox PH) Model:** Used to estimate the unadjusted hazard ratio for Overall Survival (OS) across the full follow-up period.
2. **Landmark Analysis (LMA):** Used to assess the long-term, sustained effect of the delay grouping by analyzing Overall Survival only among patients who survived past the 42-day treatment landmark.
3. **Fine-Gray Competing Risks Regression (FGR):** Used to specifically model the instantaneous risk (subdistribution hazard) of Cancer-Specific Death (Cause 1) and the Competing Event (Other Death, Cause 2). This provides an assessment of the effect of treatment with competing mortality risks.

The data used in this project originates from the Surveillance, Epidemiology, and End Results (SEER) Program database. This database contains cancer incidency and survival data from population based cancer registries. 

The raw dataset was specifically filtered using the SEER Stat software to include only patients diagnosed with Salivary Gland Cancer (ICD-O-3 codes C07.9 - C08.9) who were diagnosed at the M0 stage. Key information contained within the data includes: `Survival months`, `Time from diagnosis to treatment in days recode`, `Vital status recode`, and `SEER cause-specific death classification`. This data was claned to create variables showing time to event (`Survival_Months`), categorical exposure  (`Delay_Group`), and the competing risk status  (`Competing_Risk_Status`). The data was obtained from the National Cancer Institute (NCI) SEER website.

# Data Citation

National Cancer Institute. Surveillance, Epidemiology, and End Results (SEER) Program SEER 18 registry data (1975–2020), Released April 2023. Available at: https://seer.cancer.gov/data/
