# Car Selling Price Prediction with XGBoost Regression

## About Dataset

This dataset contains information about used cars.
This data can be used for a lot of purposes such as price prediction to exemplify the use of linear regression in Machine Learning.
The columns in the given dataset are as follows:

name
year
selling_price
km_driven
fuel
seller_type
transmission
Owner

This dataset contains information about used cars listed on different websites
This data can be used for a lot of purposes such as price prediction to exemplify the use of linear regression in Machine Learning.

In this code, we use XGBoost regression to predict the selling prices of cars based on various features such as mileage, engine power, fuel type, and brand. The dataset used in this analysis is obtained from a CSV file named 'Car details v3.csv'.

## Preprocessing Data

The first step in our analysis is to preprocess the data to make it suitable for regression. We begin by correcting the format of the mileage column, which can be in either 'km/kg' or 'kmpl' format. We convert both formats to 'kmpl' format for consistency. We then extract the brand information from the 'name' column, which contains the car model name. We also remove unnecessary characters from the 'engine' and 'max_power' columns. Finally, we one-hot encode categorical variables such as fuel type, seller type, transmission, owner, and brand using the pd.get_dummies function from the pandas library.
## Splitting Data

After preprocessing the data, we split it into a training set and a test set using the train_test_split function from the sklearn library. We use 75% of the data for training and 25% for testing.
## Fitting XGBoost Regression Model

We then fit an XGBoost regression model on the training set using the xgb.XGBRegressor function from the xgboost library. We use the default hyperparameters for this function, with the exception of colsample_bytree, learning_rate, max_depth, and n_estimators, which are set to 0.8, 0.1, 6, and 1000, respectively.
## Evaluating Model Performance

After fitting the model, we use it to predict the selling prices of cars in the test set. We then evaluate the model's performance using mean absolute error and R-squared scores. We use the mean_absolute_error and r2_score functions from the sklearn library to calculate these scores.
## Feature Importance

Finally, we plot the feature importance using the xgb.plot_importance function from the xgboost library. This plot shows the relative importance of each feature in the model. We use this plot to gain insights into which features are most important for predicting car selling prices.
Overall, this code provides an example of how to use XGBoost regression for car selling price prediction and demonstrates the importance of data preprocessing and feature selection in developing an accurate and interpretable model.

![download (6)](https://user-images.githubusercontent.com/75095471/218686548-dcf01eae-7a24-4ca7-a702-c7108c541cc0.png)
