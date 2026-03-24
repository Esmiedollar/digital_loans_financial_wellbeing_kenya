# Promise or Peril? County-Level Evidence on Digital Loans and Financial Well-Being in Kenya Using Machine Learning

## Overview

This repository contains the complete Python code and Google Colab 
notebook supporting the MSc thesis submitted in partial fulfilment 
of the requirements for the degree of Master of Science in 
Mathematical Sciences and Risk Analytics at Strathmore University, 
Nairobi, Kenya (2026).

**Author:** Esmie Awonteme Abaaluk  
**Submission Year:** 2026  
**GitHub:** [Esmiedollar](https://github.com/Esmiedollar)

---

## Thesis Abstract

The rapid expansion of digital lending in Kenya has transformed 
access to credit, yet its implications for household financial 
well-being remain contested. This study investigates whether 
digital loans represent promise or peril for Kenyan households 
using a rigorous risk analytics framework. Using nationally 
representative FinAccess survey data, the study models the 
probability of household financial distress as a function of 
digital loan usage and socioeconomic characteristics. A binary 
classification framework is adopted, beginning with 
survey-weighted logistic regression, followed by Random Forest 
and Gradient Boosting ensemble machine learning models. Model 
performance is evaluated using AUC ROC and Brier Score metrics. 
Predicted probabilities are aggregated to generate county-level 
financial vulnerability maps across all 47 Kenyan counties. SHAP 
explainability analysis is used to interpret model predictions. 
The findings confirm that digital loan usage is significantly 
associated with financial distress, with this association mediated 
by underlying socioeconomic characteristics including income, 
employment status, education, and health status.

---

## Repository Structure
```
digital_loans_financial_wellbeing_kenya/
│
├── python_code_Esmie.ipynb        ← Main analysis notebook
└── README.md
```

---

## Notebook Contents

The single notebook `python_code_Esmie.ipynb` contains the 
complete end-to-end analysis, structured in the following 
sections:

| Section | Description |
|---------|-------------|
| 1. Data Preprocessing | Data cleaning, Winsorization of Monthly Income and Age at 1st and 99th percentiles, handling missing values, and feature engineering |
| 2. Descriptive Statistics | Survey-weighted descriptive statistics, weighted distributions of Age, Monthly Income, Educational Level, Main Source of Income, and Digital Loan Usage |
| 3. Logistic Regression | Survey-weighted logistic regression, coefficient table, odds ratios, marginal effects analysis, and predicted probability plots |
| 4. Random Forest | Random Forest classifier with hyperparameter tuning, classification report, confusion matrix, AUC ROC, and Brier Score |
| 5. Gradient Boosting | Gradient Boosting classifier with hyperparameter tuning, classification report, confusion matrix, AUC ROC, and Brier Score |
| 6. Class Imbalance Handling | Retraining of all three models using `class_weight='balanced'` for Logistic Regression and Random Forest, and SMOTE pipeline for Gradient Boosting |
| 7. Target Leakage Robustness Check | Robustness checks re-estimating all models after excluding `Bad credit history` and `Negative listing by CRB` |
| 8. SHAP Explainability | SHAP feature importance bar plot, beeswarm summary plot, and dependence plots for Monthly Income, Age, and Negative Listing by CRB |
| 9. County-Level Choropleth Mapping | County-level choropleth maps of Default Rate, Mean Monthly Income, Digital Loan Users Percentage, and Percentage Overcame Financial Problems across Kenya's 47 counties |

---

## Direct Link to Notebook

The full analysis notebook can be accessed directly here:

[python_code_Esmie.ipynb](https://github.com/Esmiedollar/digital_loans_financial_wellbeing_kenya/blob/main/python_code_Esmie.ipynb)

---

## Data

This study uses data from the **Kenya FinAccess Household Surveys 
(2021 and 2024 waves)**, conducted by the Kenya National Bureau 
of Statistics (KNBS) in collaboration with the Central Bank of 
Kenya and the Financial Sector Deepening (FSD) Kenya Trust.

The raw data is **not included** in this repository due to data 
licensing and privacy restrictions. The dataset is publicly 
available and can be accessed directly from:

- [Kenya National Bureau of Statistics (KNBS)](https://www.knbs.or.ke)
- [FSD Kenya FinAccess Survey](https://fsdkenya.org/publication/finaccess/)

---

## Requirements

The analysis was conducted in **Google Colab** using Python 3. 
The following libraries are required to run the notebook:
```
pandas
numpy
scipy
statsmodels
scikit-learn
imbalanced-learn
shap
matplotlib
seaborn
geopandas
folium
```

To install all dependencies at once, run the following in 
Google Colab or your terminal:
```bash
pip install pandas numpy scipy statsmodels scikit-learn imbalanced-learn shap matplotlib seaborn geopandas folium
```

---

## How to Run

1. Clone this repository:
```bash
git clone https://github.com/Esmiedollar/digital_loans_financial_wellbeing_kenya.git
```

2. Download the FinAccess survey data from KNBS or FSD Kenya 
and place it in the same directory as the notebook.

3. Open `python_code_Esmie.ipynb` in Google Colab or Jupyter 
Notebook and run the cells sequentially from top to bottom.

---

## Key Findings

- Digital loan usage is significantly associated with household 
financial distress in Kenya (χ² = 105.74, p < 0.001), with this 
association mediated by underlying socioeconomic characteristics.
- Monthly Income, Chronic Disease, and Age are the three most 
influential predictors of financial recovery as identified by 
SHAP analysis.
- Gradient Boosting achieved the highest AUC ROC (0.68) in the 
baseline specification, while Logistic Regression achieved the 
highest minority class recall (0.60) after class imbalance 
correction.
- Financial vulnerability is geographically concentrated in 
northern and eastern ASAL counties, which simultaneously exhibit 
the lowest incomes, highest default rates, and lowest digital 
loan penetration.
- Loan purpose critically moderates the relationship between 
digital credit and financial recovery: productive loans are 
associated with recovery, while consumptive loans are associated 
with continued financial distress.

---

## Citation

If you use any part of this code or analysis in your own work, 
please cite:
```
Abaaluk, E.A. (2026). Promise or Peril? County-Level Evidence 
on Digital Loans and Financial Well-Being in Kenya Using Machine 
Learning. MSc Thesis, Strathmore Institute of Mathematical 
Sciences, Strathmore University, Nairobi, Kenya.
```

---

## License

This repository is made available for academic and research 
purposes. The code is released under the MIT License. The data 
is subject to the terms and conditions of the Kenya National 
Bureau of Statistics and FSD Kenya — please refer to their 
respective data use policies before using the raw survey data.

---

## Contact

**Esmie Awonteme Abaaluk**  
MSc Mathematical Sciences and Risk Analytics (2026)  
Strathmore Institute of Mathematical Sciences  
Strathmore University, Nairobi, Kenya  
GitHub: [Esmiedollar](https://github.com/Esmiedollar)  
Email: eabaaluk@gmail.com
