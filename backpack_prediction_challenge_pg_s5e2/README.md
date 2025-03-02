# Project Description - Backpack Prediction Challenge

Kaggle competition: [Backpack Prediction Challenge](https://www.kaggle.com/competitions/playground-series-s5e2/overview). 

The dataset for this competition (both train and test) was generated from a deep learning model trained on the [Student Bag Price Prediction Dataset](https://www.kaggle.com/datasets/schran/insurance-premium-prediction) dataset. Feature distributions are close to, but not exactly the same, as the original.

## Data

**Files**

- train.csv - the training dataset; Price is the target
- train_extra.csv - a whole lot more training data!
- test.csv - the test dataset; your objective is to predict the Price for each row
- sample_submission.csv - a sample submission file in the correct format

**Evaluation:**  Root Mean Squared Error (RMSE).

**Description of variablesn**

- `Brand` -> The brand of the bag (Categorical: Under Armour, Adidas, Nike, Puma, Jansport)
- `Material` -> The primary material used (Categorical: Polyester, Leather, Nylon, Canvas)
- `Size` -> The size of the bag (Categorical: Medium, Large, Small)
- `Compartments` -> The number of compartments in the bag (Categorical: 1 to 10)
- `Laptop Compartment` -> Whether the bag has a laptop compartment (Categorical: Yes, No)
- `Waterproof` -> Whether the bag is waterproof (Categorical: Yes, No)
- `Style` -> The style of the bag (Categorical: Messenger, Tote, Backpack)
- `Color` -> The color of the bag (Categorical: Pink, Gray, Blue, Red, Black, Green)
- `Weight Capacity (kg)` -> The maximum weight the bag can hold (Numerical)
- `Price` -> The price of the bag in USD (Numerical)

## Goal

The objective of this challenge is to predict the price of backpacks given various attributes.

## Libraries Used

*os*, *warnings*, *itertools*, *pandas*, *matplotlib*, *numpy*, *seaborn*, *scipy*, *sklearn*, *phik*, *lightgbm*, *optuna*, *cuml*,  *cudf*

## Conclusion

As a result of this competition, it was possible to get into the top 3%. Due to the peculiarities of the data (the target has no obvious relationship) due to the fact that this data set was synthesized based on a synthetic data set, and the target (price) was chosen randomly. In this case, it was necessary to generate a signal in order to get a good result. Therefore, it was necessary to resort to creating a large number of features (191) and train one model (LGBMRegressor hyperparameters were determined using optuna).

В результате этого соревнования удалось попасть в топ-3% лучших.  Из-за особенностей данных (цель не имеет явной взаимосвязи) в связи с тем, что данный набор данных был синтезирован на основе синтетического набора данных, а цель (цена) выбиралась случайным образом. В таком случае необходимо было сформировать сигнал для того, чтобы получить хороший результат. Поэтому пришлось прибегнуть к созданию большого количества признаков (191) и обучить одну модель (LGBMRegressor гиперпараметры определялись при помощи optuna).