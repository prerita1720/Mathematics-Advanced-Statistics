# 📊 Spread Locator — Statistical Distribution Analysis on Transaction Data

## 📌 Project Overview
**Spread Locator** is a data analysis project that studies how customer transaction data is *spread* across different statistical distributions. The goal is to understand transaction behavior, detect skewness, identify outliers/high-value transactions, and check how well the data fits standard probability models (Bernoulli, Binomial, Poisson, Log-Normal, Power Law, and Normal distributions).

The project is split into two parts:
- **Part A — Theoretical Foundation:** Conceptual Q&A covering statistical distributions, Q-Q plots, PDF/CDF, Z-scores, Box-Cox transform, etc.
- **Part B — Data Analysis & Testing:** Hands-on Python analysis applying these concepts to a real transaction dataset.

---

## 📁 Repository Contents
| File | Description |
|---|---|
| `Spread_Locator.ipynb` | Jupyter Notebook containing the full data analysis (Part B) |
| `spread_locator_dataset.csv` | Transaction dataset used for analysis |
| `Part_A_Theoretical_Foundation.pdf` | Theory notes on distributions, Q-Q plots, PDF/CDF, etc. |
| `README.md` | Project documentation (this file) |

---

## 🗂️ Dataset Description
The dataset (`spread_locator_dataset.csv`) contains **220 transaction records** with the following columns:

| Column | Description |
|---|---|
| `transaction_id` | Unique ID for each transaction |
| `customer_id` | Unique ID for each customer |
| `transaction_amount` | Amount of the transaction |
| `transaction_date` | Date of transaction |
| `transaction_count` | Number of transactions by that customer |
| `region` | Region of the transaction (North/South/East/etc.) |
| `transaction_status` | Success or Fail |

---

## 🔬 Tasks & Methodology

### Task 1 — Bernoulli & Binomial Distribution
Converted transaction status into binary (Success = 1, Fail = 0) and calculated the probability of success. Used the Binomial distribution to estimate the probability of a customer completing exactly 5 transactions.

### Task 2 — Poisson Distribution
Calculated the average number of transactions per day (λ) and used the Poisson distribution to estimate the probability of a specific number of transactions occurring on a given day.

### Task 3 — Log-Normal & Power Law Distribution
Fit Log-Normal and Power Law distributions to transaction amounts to model the right-skewed, heavy-tailed nature of financial data (few large transactions, many small ones — Pareto/80-20 principle).

### Task 4 — Q-Q Plot
Used a Quantile-Quantile plot to visually check whether transaction amounts follow a normal distribution.

### Task 5 — Box-Cox Transformation
Applied a Box-Cox transformation to reduce skewness in transaction amounts and make the data more suitable for statistical modeling.

### Task 6 — Z-Score & Probability
Computed Z-scores to identify how far individual transactions deviate from the mean, and calculated the probability of transactions exceeding ₹5000 (useful for outlier/fraud detection).

### Task 7 — PDF & CDF
Plotted the Probability Density Function and Cumulative Distribution Function of transaction amounts to visualize concentration and cumulative probability.

---

## ✅ Key Findings
- Transaction amount data is **skewed**, not normally distributed.
- **Log-Normal** and **Power Law** distributions fit the data better than a Normal distribution.
- A small number of **high-value transactions** contribute disproportionately to total revenue (Pareto principle).
- **Poisson distribution** reasonably models daily transaction frequency.
- **Box-Cox transformation** improves symmetry, making the data more analysis/ML-ready.

---

## 🛠️ Tech Stack
- **Python 3**
- `pandas`, `numpy` — data handling
- `matplotlib`, `seaborn` — visualization
- `scipy.stats` — distribution fitting & statistical tests
- `statsmodels` — Q-Q plots

---

## ▶️ How to Run
1. Clone/download this repository.
2. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn scipy statsmodels
   ```
3. Open `Spread_Locator.ipynb` in Jupyter Notebook / JupyterLab / VS Code.
4. Run all cells sequentially — the notebook loads the CSV, cleans it, and runs through Tasks 1–8.

---

## 📚 Theoretical Foundation
See `Part_A_Theoretical_Foundation.pdf` for concept explanations on:
statistical distributions, Q-Q plots, discrete vs continuous distributions, Bernoulli, Binomial, Log-Normal, Power Law, Box-Cox, Poisson, Z-score, and PDF vs CDF.

---

## 🙋 Author
PRERITA MORASHIYA
