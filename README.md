# Liver Disease Prediction Project

## Problem Statement
Liver disease poses a major health challenge globally, with late diagnosis often leading to severe health complications. The Indian Liver Patient Dataset (ILPD) provides various biochemical and demographic features to help identify individuals at risk. The goal of this project is to leverage machine learning models to predict the presence of liver disease, thereby aiding early detection and timely medical intervention.

## Dataset Description
- **Source**: Indian Liver Patient Dataset (ILPD)
- **Attributes**:
  - **Age**: Age of the patient.
  - **Gender**: Gender of the patient (Male/Female).
  - **Total Bilirubin**: Level of bilirubin in the blood.
  - **Direct Bilirubin**: Direct bilirubin levels.
  - **Alkaline Phosphotase**: Enzyme related to the bile duct.
  - **Alamine Aminotransferase**: Enzyme indicative of liver function.
  - **Aspartate Aminotransferase**: Enzyme that indicates liver or heart damage.
  - **Total Proteins**: Total protein levels in the blood.
  - **Albumin**: Albumin protein levels, indicating liver function.
  - **Albumin and Globulin Ratio**: Ratio indicating liver health.
  - **Target**: 1 indicates the presence of liver disease, 2 indicates absence.

## Key Insights
- **Gender Impact**: Males showed a higher occurrence of liver diseases compared to females.
- **Bilirubin Levels**:
  - Males with bilirubin levels above **20 mg/dL** require aggressive treatment.
  - Females with bilirubin levels above **15 mg/dL** need immediate medical attention.
  - Critical risk thresholds are **>30 mg/dL** for males and **>25 mg/dL** for females, beyond which survival is severely compromised without intensive care or liver transplantation.
- **Age Factor**: Older individuals exhibited higher bilirubin levels, correlating with increased liver health risks.
- **Protein Levels**: An imbalance in albumin and globulin ratios often correlated with disease presence.

## Approach
1. **Data Cleaning**:
   - Removed duplicate entries.
   - Handled missing values and ensured data consistency.

2. **Exploratory Data Analysis (EDA)**:
   - Conducted univariate analysis to understand individual feature distributions.
   - Bivariate analysis to uncover relationships between features and the target variable.
   
3. **Model Building**:
   - Implemented and compared multiple classification models including:
     - Logistic Regression
     - Random Forest Classifier
     - Gradient Boosting Classifier
     - XGBoost Classifier
   - Performed hyperparameter tuning using `GridSearchCV` and `RandomizedSearchCV` for optimal model performance.

4. **Model Evaluation**:
   - Evaluated models based on metrics such as **Accuracy**, **Precision**, **Recall**, and **F1-Score**.
   
5. **Interpretability**:
   - Identified key features influencing predictions, emphasizing the role of bilirubin levels, enzyme counts, and protein ratios.

## Conclusion
The predictive model effectively identifies individuals at risk of liver disease, enabling timely medical intervention. Elevated bilirubin levels were identified as a critical health indicator, especially among older male patients. The model emphasizes the necessity of continuous health monitoring and early medical engagement to mitigate severe outcomes. Future enhancements, including broader data integration and model fine-tuning, are encouraged to bolster predictive accuracy and reliability.

## How to Run the Project
1. **Install Dependencies**:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost ydata-profiling
```
2. **Execute the Notebook**:
Run the provided Jupyter Notebook to perform data analysis and model building:
```bash
jupyter notebook PRCP-1007-LiverPatientPred.ipynb
```

## Potential Improvements
- **Feature Engineering**: Incorporate more derived features for better model performance.
- **Model Optimization**: Experiment with ensemble techniques and deep learning models.
- **Data Collection**: Gather more diverse datasets for a robust and generalized model.
