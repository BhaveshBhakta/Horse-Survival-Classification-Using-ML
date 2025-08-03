## Horse Survival Classification

### Project Overview

This project aims to predict the **survival outcome of horses** based on a variety of clinical attributes. By analyzing features such as rectal temperature, pulse, respiratory rate, and other diagnostic indicators, the goal is to develop a machine learning model that can assist veterinarians in making critical decisions about treatment and prognosis.

-----

### Technical Highlights

  * **Dataset**: [Kaggle - Horse Survival Dataset](https://www.kaggle.com/datasets/yasserh/horse-survival-dataset)
  * **Size**: 299 entries, 28 columns
  * **Key Features**:
      * `surgery`, `age`, `rectal_temp`, `pulse`, `respiratory_rate`, `pain`, `abdomo_appearance`, `abdomo_protein`, `surgical_lesion`, and other diagnostic measurements.
  * **Approach**:
      * Data Cleaning: Dropped `hospital_number` as it's a unique identifier. A significant number of columns have missing values, which were handled by filling numerical columns with the mean and categorical columns with the mode.
      * Exploratory Data Analysis: Checked data shape, size, info, descriptive statistics, and unique values for each column.
      * Label Encoding: Applied to all columns, including numerical ones, and the target variable.
      * Classification Task: The target variable `cp_data` (cp\_data in the provided notebook's code, but the descriptive stats refer to `outcome`). The code's objective is to predict `cp_data`, which seems to be a binary variable (0 or 1) based on the code's output. The project title "Survival Classification" suggests the target should be `outcome` which has 3 classes. This discrepancy is noted, but the README follows the code's objective.
      * Models Used:
          * Logistic Regression, Ridge Classifier, SVC, Random Forest, XGBoost, AdaBoost, Gradient Boosting, Bagging, Decision Tree.
  * **Best Accuracy**:
      * 85.0% with Gradient Boosting Classifier.
      * 83.3% with Random Forest Classifier.
      * 81.7% with XGBoost Classifier, AdaBoost Classifier, and Bagging Classifier.

-----

### Purpose and Applications

  * Assist veterinarians in **predicting horse survival outcomes**, especially in cases of colic and other severe conditions.
  * Provide a data-driven tool for prognosis and treatment planning.
  * Contribute to veterinary medicine research by identifying key indicators of survival.
  * Serve as a supplementary tool for decision-making in equine critical care.

-----

### Installation

Clone the repository:

```bash
git clone https://github.com/BhaveshBhakta/Horse-Survival-Classification-Using-ML.git
cd Horse-Survival-Classification-Using-ML
```

Install the necessary libraries:

```bash
pip install pandas numpy seaborn matplotlib scikit-learn imbalanced-learn xgboost
```

-----

### Collaboration

We welcome contributions to improve the project. You can help by:

  * Re-evaluating the target variable to ensure it aligns with the project's title ("Survival Classification") and performing multi-class classification on the `outcome` column.
  * Exploring more advanced methods for handling the large number of missing values (e.g., K-Nearest Neighbors imputation) instead of simple mean/mode imputation.
  * Performing comprehensive hyperparameter tuning and cross-validation for all models.
  * Adding explainability (e.g., SHAP or LIME) to understand which clinical signs are the most significant predictors of survival.
