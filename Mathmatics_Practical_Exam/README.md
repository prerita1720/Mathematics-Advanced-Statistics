 
## Mathematics & Advanced Statistics — Loan Default Risk Analysis

## Overview
This project applies statistics, probability, and linear algebra to a loan
applications dataset (~5,000 records) to evaluate customer loan default risk.
It combines theoretical explanations of core statistical concepts with a
hands-on Python analysis of the data.

## Problem Statement
Given a dataset of loan applicants with fields such as income, credit score,
and loan amount, the goal is to:
1. Explain key statistical concepts in theory.
2. Apply Python-based statistical & probability analysis to evaluate loan
   default risk.

## Dataset
**File:** `loan_applications.csv`
**Records:** ~5,000
**Fields:**
| Column | Description |
|---|---|
| Customer_ID | Unique identifier for each customer |
| Age | Customer's age |
| Income | Customer's annual income |
| Loan_Amount | Loan amount applied for |
| Credit_Score | Customer's credit score (300–850) |
| Loan_Term | Loan repayment term, in months |
| Default_Status | Whether the customer defaulted (Yes/No) |

> **Note:** The original `loan_applications.csv` file was not supplied with
> the exam brief — only the schema was described. A synthetic dataset with
> the same structure and realistic relationships (e.g., lower credit score →
> higher default probability) was generated so every task could be completed
> end-to-end. If the real dataset becomes available, the same code can be
> re-run against it with no changes required.

## Project Structure
```
├── README.md                          # This file
├── loan_applications.csv              # Dataset (synthetic, see note above)
├── analysis.py                        # Full Part B analysis as a Python script
├── Practical_Exam_Set_C.ipynb         # Same analysis as an executed Jupyter notebook
└── Practical_Exam_Set_C_Report.docx   # Final report: theory answers + outputs + insights
```

## Part A — Theory
Short-answer explanations of eight core concepts, each tied to an example
from the dataset:
1. Mean, Median, Mode
2. Standard Deviation vs. Variance
3. Random Variable
4. Conditional Probability
5. Bayes' Theorem
6. Empirical vs. Theoretical Probability
7. Poisson Distribution
8. Eigenvalues and Eigenvectors

Full answers are in `Practical_Exam_Set_C_Report.docx`.

## Part B — Practical (Python)
Implemented in `analysis.py` / `Practical_Exam_Set_C.ipynb` using
**pandas**, **numpy**, **matplotlib**, and **scipy**.

**Step 1 — Central Tendency & Dispersion**
- Mean, median, mode of Income
- Range, variance, standard deviation of Loan_Amount

**Step 2 — Probability & Events**
- Overall probability of loan default
- Contingency table: Credit_Score range vs. Default_Status
- Conditional probability: P(Default | Credit_Score < 600)

**Step 3 — Distributions & Visualization**
- Histogram of Credit_Score with a fitted Gaussian curve
- Skewness and kurtosis of Loan_Amount
- Q-Q plot of Income vs. a normal distribution

**Step 4 — Linear Algebra Application**
- Dot product between customer vectors [Income, Loan_Amount]
- L2 norm of a customer's financial vector
- Angle between two customers' vectors

## Key Insights
1. Overall default rate is **≈38.5%**.
2. Customers with **Credit_Score < 600 default ≈67%** of the time — nearly
   double the baseline rate, making credit score a strong risk signal.
3. **Loan_Amount is right-skewed** (skewness ≈ 1.66, excess kurtosis ≈ 4.38),
   so median/IQR are more reliable summaries than mean/std alone.
4. **Credit_Score is approximately normally distributed**, supporting the
   use of z-score-based risk thresholds.
5. **Income deviates from normality in the tails** (per the Q-Q plot),
   suggesting a log-transform may help in downstream models.

## How to Run
```bash
pip install numpy pandas matplotlib scipy
python analysis.py
```
This regenerates all statistics and saves the two plots
(`fig1_histogram_credit_score.png`, `fig2_qqplot_income.png`) plus a full
text log (`outputs.txt`).

Alternatively, open `Practical_Exam_Set_C.ipynb` in Jupyter to view the
analysis with outputs and plots already rendered inline.

## Deliverables (as required by the exam)
- [x] Python file / Jupyter notebook with all calculations
- [x] PDF/Word report with theory answers, Part B outputs, and 5 insights

