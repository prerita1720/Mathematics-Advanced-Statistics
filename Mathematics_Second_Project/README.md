# Inferential Statistics on Public Health Data

A data analysis project applying inferential statistics — hypothesis testing, confidence intervals, z-test, t-tests, chi-square test, ANOVA, correlation, and covariance — to a public health dataset, in order to evaluate which factors are significantly linked to health outcomes like Diabetes and BMI.

## 📌 Project Objective

To apply inferential statistical techniques to a health dataset containing demographic, lifestyle, and diagnostic information, and derive statistically-backed judgements about which factors significantly affect disease occurrence — rather than relying on raw data patterns alone.

## 📁 Repository Structure

```
.
├── Derivable_judgement.ipynb       # Full practical notebook (Part B — all tests, code + markdown)
├── public_health_dataset.csv       # Dataset used for analysis
├── Theory_Notes.pdf                # Part A — theoretical short notes (definitions)
└── README.md                       # This file
```

## 📊 Dataset

The dataset contains health records of individuals across different regions, with the following fields:

| Field | Description |
|---|---|
| `record_id` | Unique identifier for each record |
| `age_group` | Age category (18-25, 26-35, 36-45, 46-60, 60+) |
| `age` | Age of the individual |
| `weight` | Weight of the individual |
| `gender` | Male / Female / Other |
| `region` | North / South / East / West |
| `smoking_status` | Smoker / Non-Smoker / Former Smoker |
| `exercise_frequency` | Daily / Weekly / Rarely / Never |
| `bmi` | Body Mass Index |
| `blood_pressure` | Systolic blood pressure (mmHg) |
| `diabetes` | Diabetes diagnosis (True/False) |
| `hypertension` | Hypertension diagnosis (True/False) |

## ✅ Tasks Covered

**Part A (Theory_Notes.pdf):** Inferential statistics, hypothesis testing and its components, confidence intervals, critical values, p-values, Type I & Type II errors, and descriptions of z-test, t-test, chi-square test, ANOVA, covariance, and correlation.

**Part B (Notebook — `Derivable_judgement.ipynb`):**
1. **Hypothesis 1:** Smoking status vs Diabetes prevalence (contingency table)
2. **Hypothesis 2:** Exercise frequency vs BMI (group comparison)
3. **Confidence Intervals** — 95% CI for age and weight
4. **One-Sample T-test** — testing if mean BMI differs from the clinical threshold of 25
5. **Z-test** — testing if mean age differs from an assumed population mean of 40
6. **Independent T-test** — BMI comparison between Smokers and Non-Smokers
7. **Chi-Square Test** — Smoking status vs Diabetes (test of independence)
8. **ANOVA** — BMI differences across five age groups
9. **Correlation** — Age vs BMI relationship
10. **Covariance** — Age vs BMI relationship
11. **Visualizations** — Age distribution, BMI by smoking status, correlation heatmap

## 📈 Key Results Summary

| Test | Statistic | p-value | Decision |
|---|---|---|---|
| One-Sample T-test (BMI vs 25) | t ≈ 13.04 | ≈ 0.000 | **Reject H₀** — mean BMI significantly differs from 25 |
| Z-test (Age vs 40) | z ≈ 14.18 | ≈ 0.000 | **Reject H₀** — mean age significantly differs from 40 |
| Independent T-test (BMI: Smokers vs Non-Smokers) | t ≈ -0.56 | ≈ 0.577 | **Fail to reject H₀** — no significant BMI difference |
| Chi-Square (Smoking vs Diabetes) | χ² ≈ 13.77 | ≈ 0.001 | **Reject H₀** — smoking and diabetes are significantly related |
| ANOVA (BMI across Age Groups) | F ≈ 2.27 | ≈ 0.059 | **Fail to reject H₀** (borderline) — no significant difference at α = 0.05 |
| Correlation (Age vs BMI) | r ≈ 0.047 | — | Negligible linear relationship |
| Covariance (Age vs BMI) | 7.11 | — | Weak positive, direction only (not standardized) |

## 🔑 Key Takeaways

- **Smoking status is significantly associated with diabetes prevalence** (chi-square test), supporting smoking as a relevant risk factor.
- **Average BMI and average age both differ significantly from reference values** (25 and 40 respectively), indicating this population skews measurably away from those baselines.
- **BMI does not differ significantly between smokers and non-smokers**, and the difference in BMI across age groups is borderline, not statistically significant at the 0.05 level — showing that not every visible pattern in the data holds up under formal testing.
- **Age and BMI show almost no linear correlation**, meaning BMI in this dataset is not meaningfully driven by age alone.

## 🎥 Video Walkthrough

📺https://drive.google.com/file/d/1MuaorTPEO5fQjJTP5kKFJtmcP-Lro9jM/view?usp=drive_link

## ▶️ How to Run

```bash
pip install pandas numpy matplotlib seaborn scipy jupyter
jupyter notebook Derivable_judgement.ipynb
```

## 🧑‍💻 Author

Prerita morashiya
