# 📊 Mathematics & ADVANCED statistics

This repository contains four projects, each exploring a different set of concepts using real-world style datasets.

## 📁 Projects

| # | Project | Focus Area | Notebook |
|---|---------|-----------|----------|
| 1 | [Expectation Decider](#1-expectation-decider) | Probability & Bayes' Theorem | `firstprojecttt.ipynb` |
| 2 | [Derivable Judgement](#2-derivable-judgement) | Hypothesis Testing | `Derivable_judgement.ipynb` |
| 3 | [Spread Locator](#3-spread-locator) | Probability Distributions | `Spread_Locator.ipynb` |
| 4 | [Calculative Foundation](#4-calculative-foundation) | Linear Algebra | `Calculative_Foundation.ipynb` |

---

## 1. Expectation Decider
### Probability Analysis of Student Exam Success Factors

**Overview:** Analyzes factors influencing a student's success in a competitive mathematics exam, including empirical/theoretical probability, random variables, contingency tables, conditional probability, independence testing, Venn diagrams, and Bayes' Theorem.

**Dataset:** `student_dataset.csv` — 200 students, fields: `student_id`, `study_hours`, `attendance`, `group_discussion`, previous test scores, `final_exam_pass`

**Concepts Covered**
1. Basics of Probability — P(Event) = favorable outcomes / total outcomes
2. Empirical vs Theoretical Probability — real-data probability vs binomial-model probability
3. Random Variables & Probability Distribution — binomial distribution of pass counts, mean & variance
4. Venn Diagram — overlap between high study-hours and high attendance students
5. Contingency Table & Joint/Marginal/Conditional Probability — group discussion vs exam outcome
6. Independence Testing — checking whether group discussion and passing are independent events
7. Bayes' Theorem — updating probability of passing given high attendance

**Tech Stack:** Python, pandas, matplotlib, matplotlib-venn, math (`comb`)

**Key Findings**
- Study hours and attendance both positively relate to passing the exam
- Group discussion participation raises the conditional probability of passing — dependent, not independent
- Study habits and attendance overlap significantly but not perfectly (Venn diagram)
- Bayes' Theorem shows high attendance raises the probability of passing from a 50% prior to ~58.3% posterior
- No single factor guarantees success — study hours, attendance, prior scores, and participation together compound into better outcomes

---

## 2. Derivable Judgement
### Hypothesis Testing & Statistical Inference on Public Health Data

**Overview:** Applies statistical hypothesis testing to a public health dataset to determine which lifestyle and demographic factors (smoking, exercise, age) significantly relate to health outcomes like diabetes and BMI.

**Dataset:** `public_health_dataset.csv` — fields include `age`, `weight`, `bmi`, `smoking_status`, `exercise_frequency`, `diabetes`, `age_group`

**Tasks Covered**
1. Hypothesis Formulation — smoking vs diabetes, exercise frequency vs BMI (H₀ / H₁)
2. Confidence Intervals — 95% CI for age and weight
3. One-Sample T-Test — testing if average BMI differs from 25
4. Z-Test — testing if sample mean age differs from population mean
5. Independent T-Test — comparing BMI between smokers and non-smokers
6. Chi-Square Test — relationship between smoking status and diabetes
7. ANOVA — comparing BMI across multiple age groups
8. Correlation & Covariance — relationship between age and BMI
9. Visualizations — age distribution, BMI by smoking status, correlation heatmap

**Tech Stack:** Python, pandas, numpy, scipy (`stats`), seaborn, matplotlib

**Key Takeaways**
- Statistical tests determine whether observed differences are significant or due to chance
- Smoking status and diabetes show a testable relationship via chi-square
- BMI varies significantly across age groups, confirmed through ANOVA
- Confidence intervals quantify the reliability of estimated population parameters

---

## 3. Spread Locator
### Probability Distribution Analysis on Transaction Data

**Overview:** Analyzes customer transaction data using probability distributions and statistical transformations to understand spending behavior — how often customers transact, how amounts are spread, and which values are unusually large.

**Dataset:** `spread_locator_dataset.csv` — customer transaction records with `customer_id`, `transaction_date`, `transaction_status`, `transaction_count`, `transaction_amount`

**Tasks Covered**
1. Bernoulli & Binomial Distribution — probability of transaction success and fixed weekly transaction counts
2. Poisson Distribution — modeling daily transaction frequency using average rate (λ)
3. Log-Normal & Power Law — fitting transaction amounts; detecting heavy-tail (Pareto) spending behavior
4. Q-Q Plot — testing whether transaction amounts are normally distributed
5. Box-Cox Transformation — normalizing skewed data for better statistical modeling
6. Z-Score & Probability — identifying outliers and high-value transaction probability
7. PDF & CDF — visualizing concentration and cumulative probability
8. Final Conclusion — distribution fit summary and business insights

**Tech Stack:** Python, pandas, numpy, scipy (`stats`), statsmodels, seaborn, matplotlib

**Key Takeaways**
- Transaction amounts are skewed — log-normal and power law fit better than normal
- A small number of high-value transactions drive a large share of revenue (80-20 rule)
- Poisson distribution reasonably models daily transaction frequency
- Box-Cox transformation improves symmetry for downstream modeling
- High-value transactions are rare but important to flag (spending or fraud signals)

---

## 4. Calculative Foundation
### Linear Algebra Analysis on Student Performance Dataset

**Overview:** Applies core linear algebra concepts to a student performance dataset. Each student's subject scores are treated as a vector, and the project explores vectors, matrices, eigenvalues, decompositions, and dimensionality reduction — the foundations behind techniques like PCA and LDA.

**Dataset:** `student_performance.csv` — 200 students, columns: `Student_ID`, `Math`, `Science`, `English`, `History`, `Computer`, `Average_Score`, `Category` (Above Average / Below Average)

**Concepts Covered**
- **Part A — Vectors:** score vectors, L1/L2 norms, dot product & angle, cross product, projection
- **Part B — Matrix Operations:** matrix formation, addition, multiplication, transpose, determinant, inverse
- **Part C — Geometry:** line (1D), plane (2D), hyperplane (5D), dimensionality visualization
- **Part D — Eigen & Decomposition:** eigenvalues/eigenvectors of covariance matrix, LU decomposition, SVD
- **Part E — Dimensionality Reduction:** PCA (unsupervised, 5D→2D), LDA (supervised class separation)

**Tech Stack:** Python, pandas, numpy, scipy, scikit-learn, matplotlib

**Key Takeaways**
- Real data can be represented and manipulated using pure linear algebra
- Eigen-decomposition and SVD reveal underlying data structure
- PCA finds patterns without labels; LDA maximizes class separation
- These techniques underpin modern machine learning models

---

## 🚀 How to Run Any Project
```bash
pip install pandas numpy scipy scikit-learn statsmodels seaborn matplotlib matplotlib-venn
```
Place the corresponding dataset CSV next to its notebook, then run cell by cell in Jupyter.

## 🛠️ Overall Tech Stack
Python · pandas · numpy · scipy · scikit-learn · statsmodels · seaborn · matplotlib · matplotlib-venn
