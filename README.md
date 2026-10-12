# CSET485 - AI and Society: Assignment #1
## Predictive Modeling, Stress-Testing, and Algorithmic Fairness on COMPAS

**Student Name:** Parth Bhatia  
**Enrollment No.:** S24BCAU0210  
**Course:** CSET485 - AI and Society  
**Dataset:** COMPAS Recidivism Risk Score Dataset (Assigned by roll number last digit: **0**)  
**Train-Test Split Seed:** **210** (`random_state=210`, 70% train / 30% test)  

---

## Repository Overview
This repository contains the complete reproducible code, cleaned dataset, and analytical figures for **Assignment #1** in CSET485 (AI and Society). The assignment audits the COMPAS pretrial risk assessment tool for predictive accuracy, subgroup stability, omitted-variable bias, adversarial vulnerabilities, and mathematical fairness trade-offs.

### Repository Files
- **`CSET485_Assignment1_S24BCAU0210.ipynb`**: Complete, self-contained Jupyter notebook computing all baseline models (OLS on decile score, Logistic Regression on two-year recidivism), the 4 stress-tests (Simpson's Paradox, Omitted Variable Bias, Adversarial Subsets, Fairness Sweep), and metric tables.
- **`compas-scores-two-years.csv`**: Raw benchmark dataset from ProPublica.
- **`compas_cleaned_S24BCAU0210.csv`**: Preprocessed, filtered dataset (6,172 valid cases) with engineered features.
- **`fairness_tradeoff.png`**: Demographic Parity vs Equalized Odds trade-off curve across decision thresholds $t \in [0.05, 0.95]$.
- **`fairness_vs_threshold.png`**: Evolution of DP, EO, and PP metric ratios across thresholds.

---

## Reproducibility & Execution
1. Clone this repository:
   ```bash
   git clone https://github.com/PARTH7759-BEAST/CSET485_Assignment1_S24BCAU0210.git
   cd CSET485_Assignment1_S24BCAU0210
   ```
2. Install dependencies:
   ```bash
   pip install numpy pandas scipy scikit-learn statsmodels matplotlib
   ```
3. Run the notebook:
   ```bash
   jupyter notebook CSET485_Assignment1_S24BCAU0210.ipynb
   ```
All models, coefficients, p-values, odds ratios, and fairness metrics are deterministically produced using random seed `210`.

---
**Author:** Parth Bhatia (S24BCAU0210)  
**Institution:** CSET485 - AI and Society  