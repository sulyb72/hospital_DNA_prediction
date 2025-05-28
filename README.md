# Hospital DNA (Did Not Attend) Prediction

This project explores the prediction of outpatient non-attendance (DNA) in the UK using synthetic data inspired by NHS statistics. We developed and evaluated multiple machine learning models to understand which patient and service factors best predict missed appointments.

---

## Folder Structure

```
hospital_DNA_prediction/
│
├── hosp-epis-stat-outp-all-firs-atte.csv      # All outpatient first attendance activity
├── hosp-epis-stat-outp-eth-imd-dec.csv        # Attendance by ethnicity and deprivation
├── hosp-epis-stat-outp-main-spec-t.csv        # Attendance by specialty type
├── predictive_analysis.ipynb                  # Jupyter Notebook with full modelling pipeline
└── .gitattributes                              # Git config file
```

---

## Project Overview

- **Data Processing**: Cleaned and combined multiple NHS datasets across age, gender, ethnicity, and specialty.
- **Synthetic Labeling**: Created realistic DNA rates using rule-based logic incorporating known risk factors.
- **Modelling**: Trained Linear Regression, Random Forest, Gradient Boosting, and XGBoost models.
- **Evaluation**: Compared models using MAE and R² via standard splits and cross-validation.
- **Interpretation**: Used permutation importance, SHAP values, and partial dependence plots to interpret feature influence.

---

## Key Insights

- **Top Model**: Linear Regression delivered the best MAE and R², suggesting that the problem is well-approximated by a linear combination of features.
- **Mental Illness Specialty**: Patients in the `Adult Mental Illness` specialty showed a significantly higher likelihood of non-attendance and appeared as a key predictor across tree-based models.
- **Other Drivers**: Ethnicity and age groups were also consistently relevant predictors, especially in younger and minoritized populations.

---

## Conclusion

Adult Mental Illness is a strong but not exclusive predictor of hospital DNA risk. Predictive accuracy benefits most from including a diverse range of demographic and service-level features. This supports a multifaceted approach for improving outpatient attendance, especially in mental health services.