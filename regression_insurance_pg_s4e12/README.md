# Project Description - Regression with an Insurance Dataset

Kaggle competition: [Regression with an Insurance Dataset](https://www.kaggle.com/competitions/playground-series-s4e12). 

The dataset for this competition (both train and test) was generated from a deep learning model trained on the [Insurance Premium Prediction](https://www.kaggle.com/datasets/schran/insurance-premium-prediction) dataset. Feature distributions are close to, but not exactly the same, as the original.

## Data

**Files**

- train.csv - the training dataset; Premium Amount is the continuous target
- test.csv - the test dataset; your objective is to predict target Premium Amount for each row
- sample_submission.csv - a sample submission file in the correct format

**Evaluation:**  Root Mean Squared Logarithmic Error (RMSLE).

**Description of variablesn**

- `Age` -> Age of the insured individual (Numerical)
- `Gender` -> Gender of the insured individual (Categorical: Male, Female)
- `Annual Income` -> Annual income of the insured individual (Numerical, skewed)
- `Marital Status` -> Marital status of the insured individual (Categorical: Single, Married, Divorced)
- `Number of Dependents` -> Number of dependents (Numerical, with missing values)
- `Education Level` -> Highest education level attained (Categorical: High School, Bachelor's, Master's, PhD)
- `Occupation` -> Occupation of the insured individual (Categorical: Employed, Self-Employed, Unemployed)
- `Health Score` -> A score representing the health status (Numerical, skewed)
- `Location` -> Type of location (Categorical: Urban, Suburban, Rural)
- `Policy Type` -> Type of insurance policy (Categorical: Basic, Comprehensive, Premium)
- `Previous Claims` -> Number of previous claims made (Numerical, with outliers)
- `Vehicle Age` -> Age of the vehicle insured (Numerical)
- `Credit Score` -> Credit score of the insured individual (Numerical, with missing values)
- `Insurance Duration` -> Duration of the insurance policy (Numerical, in years)
- `Premium Amount` -> Target variable representing the insurance premium amount (Numerical, skewed)
- `Policy Start Date` -> Start date of the insurance policy (Text, improperly formatted)
- `Customer Feedback` -> Short feedback comments from customers (Text)
- `Smoking Status` -> Smoking status of the insured individual (Categorical: Yes, No)
- `Exercise Frequency` -> Frequency of exercise (Categorical: Daily, Weekly, Monthly, Rarely)
- `Property Type` -> Type of property owned (Categorical: House, Apartment, Condo)

## Goal

The objective of this challenge is to predict insurance premiums based on various factors.

## Libraries Used

*os*, *warnings*, *pandas*, *matplotlib*, *numpy*, *seaborn*, *scipy*, *sklearn*, *phik*, *lightgbm*, *catboost*, *optuna*, *autogluon*

## Conclusion

As a result of this competition, it was possible to get into the top 15%. For the best result, missing values ​​were considered as separate categories, since it turned out that they are related to the target. The best result was achieved in a combination of stacking, weighted prediction and AutoGluon. To create meta data, predictions on Ridge, CatBoostRegressor, LGBMRegressor and MLPRegressor were used. Ridge was used as a meta model. Then a weighted prediction was used, where meta predictions used weights of 0.6, and AutoGluon predictions used a weight of 0.4.

В результате этого соревнования удалось попасть в топ-15%. Для лучшего результата пропущенные значения рассматривались как отдельные категории, так как оказалось, что они связаны с таргетом. Лучший результат был достигнут в сочетании стекинга, весового предсказания и AutoGluon. Для создания метаданных использовались предсказания на Ridge, CatBoostRegressor, LGBMRegressor и MLPRegressor. В качестве метамодели использовался Ridge. Затем применил весовое предсказание, где метапредсказаниям присудил вес 0.6, а предсказаниям AutoGluon вес 0.4.