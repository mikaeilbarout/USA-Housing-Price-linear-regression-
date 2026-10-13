# USA Housing Price Prediction

Predicting house prices with **Linear Regression (scikit-learn)** on the USA Housing dataset.

## Dataset

`USA_Housing.csv`: 5,000 houses with these features:

| Feature | Description |
|---|---|
| Avg. Area Income | Average income of residents in the area |
| Avg. Area House Age | Average age of houses in the area |
| Avg. Area Number of Rooms | Average number of rooms |
| Avg. Area Number of Bedrooms | Average number of bedrooms |
| Area Population | Population of the area |
| **Price** | House price (the target) |

The `Address` column is not used by the model.

## What the notebook does

1. **Explores the data** with a pairplot, the price distribution and a correlation heatmap
2. **Splits** the data 70/30 into training and test sets
3. **Trains** a Linear Regression model
4. **Evaluates** it with MAE, RMSE and R², and looks at the percentage error of each prediction

## Results

| Metric | Value |
|---|---|
| R² | 0.918 |
| RMSE | ~100,842 |
| MAE | ~81,258 |
| Median % error | 5.7% |

The model explains most of the variation in price, and half of its predictions are within about 6% of the real price.

## What I learned

- How to use correlation and pairplots to see which features are related to the target before training
- How to judge a regression model with several metrics instead of only one
- Why percentage error is easier to explain than RMSE when prices are large numbers

## How to run

```bash
pip install -r requirements.txt
jupyter notebook USA_Housing_Price_Etimating.ipynb
```
