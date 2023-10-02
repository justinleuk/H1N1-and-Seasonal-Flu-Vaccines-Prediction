# Predicting Flu Vaccination Probability for Public Health Optimization

## Introduction

Mass vaccination is considered one of the most effective public health measures to control infectious diseases during an outbreak. However, vaccination rates can vary widely across different populations, and vaccine hesitancy is a growing concern that can hinder vaccination rates. This project aims to answer key questions:

1. How likely are individuals of different age groups to get vaccinated to assist public health officials in optimal vaccination allocation and distribution?
2. What is the receptiveness of vaccination from individuals of varying income levels for effective public health intervention strategies?

To address these questions, we analyze and model a dataset from the National 2009 H1N1 Flu Survey to predict the probability of flu vaccination of individuals during a pandemic, with the goal of optimizing vaccination allocation and distribution.

## Dataset Overview

- Dataset Size: 26,707 data samples
- Features: 35 categorical features, including individuals' social, economic, and demographic backgrounds, as well as opinions on illness risks and vaccine effectiveness.

Based on the dataset's descriptive statistics, the overall vaccination rate for the H1N1 and seasonal flu is 21.2% and 46.6%, respectively. This indicates a heavily imbalanced distribution of H1N1 vaccination, which could lead to overfitting of the model. Examining vaccination rates by age group, individuals aged 65 and above have the highest vaccination rates at 11.7% and 34.8% for H1N1 and seasonal vaccines, respectively. Moreover, the seasonal vaccination rate has a balanced distribution across different income levels. However, the H1N1 vaccination rate is imbalanced across income levels, with the highest percentage of unvaccinated individuals at 76.9% for the below $75,000, above poverty income level group.

These statistics suggest that age group and income level are important factors affecting vaccination rates, which can be used to identify priority groups and improve accessibility to vaccines.

## Project Sections

### Exploratory Data Analysis (EDA)

- Basic EDA
- Convert to object
- Find unique values in each feature
- Visualize the distribution
- Finding total null values
- Sort null values in ascending order
- Visualize the null values
- Finding the percentage of null in each feature
- Check if the dataset contains duplicates
- Visualize unique values in each column
- Check if null values are missing at random using a heatmap

### Preprocessing

- MNAR Imputation for employment_industry and employment_occupation
- Remove columns with too many missing values
- Remove rows with too many missing values
- Feature encoding
- Correlation matrix for all features
- Split the dataset for single output
- Calculate class weight for label 1 in the H1N1 dataset
- H1N1 and Seasonal Vaccine Imputation using KNN with different weights
- Encoding (try without removing rows and columns)
- Null Imputation using KNN, Mode, MissForest, and Iterative Imputer

### Feature Selection and Engineering

- Feature selection using RFE, Chi Square, and SelectKBest
- Dimensionality Reduction using PCA
- Feature Selection using Lasso, RandomForest, and XGBoost
- Print features extracted with each imputation method and feature selection method
- Visualize features extracted
- Find the frequency of features extracted by each model
- Rank the feature importance in a graph
- Fit each model to a baseline predictive model to see the AUROC score

### Model Selection

For H1N1:
- Model training using RandomForestClassifier, LogisticRegression, XGBClassifier, SVM, CatBoost, and MLP with different hyperparameters
- Calculate AUROC for H1N1 model

For Seasonal:
- Model training using RandomForestClassifier, LogisticRegression, XGBClassifier, SVM, CatBoost, and MLP with different hyperparameters
- Calculate AUROC for Seasonal model

## Contributors

- Justin
- Fam

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
