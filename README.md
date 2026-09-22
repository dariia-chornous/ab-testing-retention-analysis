# 🎮 A/B Testing & Retention Analysis — Cookie Cats

> A data-driven evaluation of a product change in a mobile game, focused on user retention and evidence-based product decision-making.

## 📌 Project Overview

Cookie Cats is a mobile game in which players periodically encounter progression gates.

In this A/B test, the first gate was moved from level 30 (`gate_30`) to level 40 (`gate_40`). The goal of the analysis was to evaluate whether this product change affected user retention 1 and 7 days after installing the game.

The project covers the full statistical analysis workflow — from hypothesis formulation and sample size estimation to statistical significance testing and interpretation of the results for product decision-making.

## 📈 Key Findings

| Metric | gate_30 (Control) | gate_40 (Treatment) |
|---|---:|---:|
| 7-Day Retention | **19.0%** | **18.2%** |
| 95% CI | [0.187, 0.194] | [0.178, 0.186] |
| p-value (z-test) | **0.002** | — |
| χ² | **9.959** | — |

Moving the gate from level 30 to level 40 resulted in a statistically significant decrease in 7-day retention.

Although the absolute difference was relatively small, the statistical evidence indicates that the change negatively affected longer-term user retention.

## 💡 Business Recommendation

Based on the analysis, moving the progression gate from level 30 to level 40 should not be implemented without further validation.

Recommended next steps:

- retain the current gate placement while additional testing is conducted;
- investigate potential reasons for lower 7-day retention in the treatment group;
- run additional experiments before rolling out the change to all users;
- continue monitoring retention as a key metric when evaluating progression-related product changes.

The analysis demonstrates how statistical testing can support product decisions and reduce the risk of implementing changes that negatively affect user engagement.

## 🔬 Analysis & Methodology

### Sample Size

Estimated the minimum required sample size at approximately **24,638 users per group**, using:

- statistical power: 80%
- significance level: α = 0.05

### Statistical Testing

The analysis included:

- **Two-proportion z-test** — to evaluate whether the difference in 7-day retention between the two groups was statistically significant;
- **Chi-square (χ²) test** — to test the relationship between game version and user retention;
- **95% confidence intervals** — to estimate the range of plausible retention values for the control and treatment groups.

## 🛠️ Tools & Stack

| Task | Tools |
|---|---|
| Data Processing | Python, Pandas |
| Statistical Analysis | SciPy, Statsmodels |
| Data Visualization | Matplotlib, Seaborn |
| Analysis Environment | Jupyter Notebook |

## 📁 Project Structure

```text
ab-testing-retention-analysis/
├── ab_testing_analysis.ipynb
├── data/
│   └── cookie_cats.csv
├── .gitignore
└── README.md
```

## 🚀 How to Run

```bash
git clone https://github.com/dariia-chornous/ab-testing-retention-analysis.git
cd ab-testing-retention-analysis
pip install pandas scipy statsmodels matplotlib seaborn
jupyter notebook ab_testing_analysis.ipynb
```
---
*Dataset: Cookie Cats — Kaggle*
