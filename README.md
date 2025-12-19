# CreditRiskAnalysis

## Overview
This project implements an end-to-end **Credit Risk Analysis framework** aligned with banking and regulatory practices. The objective is to quantify credit risk by modeling **Probability of Default (PD)** using Logistic Regression and estimating **Loss Given Default (LGD)**, **Exposure at Default (EAD)**, and **Expected Credit Loss (ECL)** using Basel-style methodologies.

The project is designed for academic, portfolio, and interview purposes and follows an industry-recognized credit risk workflow.

---

## Business Objective
- Identify borrowers with higher default risk
- Quantify expected losses at both customer and portfolio level
- Demonstrate regulatory-aligned credit risk metrics (PD, LGD, EAD, ECL)

---

## Dataset
- **Source:** Kaggle – Credit Risk Dataset  
- **Link:** https://www.kaggle.com/datasets/laotse/credit-risk-dataset  
- **Target Variable:** `loan_status`  
  - `0` → Non-default  
  - `1` → Default  

---

## Project Workflow
1. Data loading and initial inspection  
2. Exploratory Data Analysis (EDA)  
3. Missing value treatment  
4. Categorical variable encoding  
5. Train–test split and feature scaling  
6. PD modeling using Logistic Regression  
7. LGD estimation using rule-based assumptions  
8. EAD approximation using loan exposure  
9. ECL calculation using Basel formula  
10. Portfolio-level risk analysis  

---

## Key Credit Risk Components

### Probability of Default (PD)
- Modeled using **Logistic Regression**
- Outputs the probability that a borrower will default
- Evaluated using **ROC-AUC**

### Loss Given Default (LGD)
- Estimated using **rule-based segmentation**
- Assumed based on loan grade:
  - Grade A–B: 30%
  - Grade C–D: 45%
  - Grade E–G: 60%

### Exposure at Default (EAD)
- Approximated using **outstanding loan amount**
- Represents total exposure at the time of default

### Expected Credit Loss (ECL)
Calculated using the standard Basel-style formula:

ECL = PD × LGD × EAD

This provides borrower-level and portfolio-level expected loss.

---

## Technologies Used
- Python
- Pandas, NumPy
- Scikit-learn
- Matplotlib, Seaborn
- Jupyter Notebook

---

## Key Outputs
- Probability of Default (PD) scores for borrowers
- Expected Credit Loss (ECL) per loan
- Total portfolio EAD and ECL
- Risk distribution visualization

---

## Use Cases
- Credit Risk Analyst portfolios
- Banking and NBFC interview projects
- Academic demonstrations of Basel-style credit risk modeling
- Risk quantification and decision-support analysis

---

## Disclaimer
LGD and EAD are estimated using assumptions due to the absence of recovery and exposure timing data. This approach is standard for academic and interview-oriented credit risk projects.

