# Data Science Project: Vaccine Adoption Prediction

## Project Overview

This data science project aims to predict the adoption of H1N1 and Seasonal vaccines using a dataset of . The project includes several stages, such as Exploratory Data Analysis (EDA), Data Preprocessing, Feature Selection, Feature Engineering, and Model Selection.

## Contributors

- Justin
- Fam

## Sections

- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Data Preprocessing](#data-preprocessing)
- [Feature Selection and Engineering](#feature-selection-and-engineering)
- [Model Selection](#model-selection)

### Exploratory Data Analysis

- Conducted basic EDA.
- Converted some features to object data type.
- Found unique values in each feature.
- Visualized the distribution of features.
- Identified NULL values.
- Visualized the distribution of NULL values.
- Checked if NULL values are missing at random using a heatmap.
- Calculated the total number of NULL values.
- Sorted NULL values in ascending order.
- Visualized NULL values.
- Found the percentage of NULL values in each feature.
- Checked for duplicate entries.
- Found unique values in each column.

### Data Preprocessing

- Conducted MNAR (Missing Not At Random) Imputation for 'employment_industry' and 'employment_occupation'.
- Removed columns with too many missing values.
- Removed rows with too many missing values.
- Performed feature encoding.
- Calculated class weights for label 1 in the H1N1 dataset.
- Imputed H1N1 and Seasonal Vaccine data using KNN with different weights.
- Encoded data without removing rows and columns.
- Imputed NULL values using KNN, Mode, MissForest, and Iterative Imputer.

### Feature Selection and Engineering

- Conducted feature selection using RFE, Chi-Square, and SelectKBest.
- Applied dimensionality reduction using PCA.
- Performed feature selection using Lasso, RandomForest, and XGBoost.
- Printed features extracted with each imputation and selection method.
- Visualized features extracted.
- Found the frequency of features extracted by each model.
- Ranked feature importance in a graph.
- Fitted each model to a baseline predictive model to calculate AUROC scores.

### Model Selection

- Trained H1N1 models using RandomForestClassifier, LogisticRegression, and XGBClassifier with different hyperparameters.
- Trained Seasonal models using RandomForestClassifier, LogisticRegression, and XGBClassifier with different hyperparameters.
- Trained H1N1 models using SVM, CatBoost, and MLP with different hyperparameters.
- Calculated AUROC scores for both H1N1 and Seasonal models.

## Dependencies

- Python 3.7+
- Libraries: pandas, numpy, scikit-learn, matplotlib, seaborn, xgboost, catboost

## Usage

1. Clone this repository.
2. Set up your Python environment.
3. Run the Jupyter notebooks in the respective sections to reproduce the analysis and models.

## License

This project is licensed under the [MIT License](LICENSE).
