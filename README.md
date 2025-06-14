# Sales_forecasting_XGBoost
This project performs time-series forecasting on sales data using the XGBoost Regressor. It visualizes sales trends, generates lag features, and trains a machine learning model to predict future sales based on historical data.

## 📊 Visualization
1.The first step is to visualize the sales trend over time, which helps understand seasonality, trends, and anomalies.
2.A line plot is generated using matplotlib to show how sales evolved over time.

## 🧠 Model Building – XGBoost Regressor
The forecasting is done using XGBoost, a gradient boosting framework.
🛠 Steps:
1.Create lag features – previous n days of sales are used to predict the next day’s sales. (lag = 5)
2.Handle missing values caused by lagging.
3.Split data into training and testing without shuffling (to preserve time order).
4.Train the model using XGBRegressor.
5.Evaluate using RMSE (Root Mean Squared Error).

## 📈 Performance
RMSE: 737.00
1.Average Sales: 1837.00
2.Relative RMSE ≈ 40% of average → indicates room for improvement.

## ✅ Output Plots

1.Actual vs Predicted Sales plot is generated for visual evaluation of prediction performance.

2.Prediction lines follow the trend but may miss some peaks or drops.

## 🚀 How to Improve Accuracy
Here are several ways to improve the model performance:

✅ Feature Engineering

1.Include more lag features (e.g., 7, 14, 30-day lags).

2.Add rolling averages or exponential moving averages.

3.Include day of the week, month, or is_weekend as features.

4.Incorporate promotion/discount information (if available).

5.Include seasonal decomposition components.

✅ Model Enhancements
1.Use Hyperparameter Tuning with GridSearchCV or Optuna to optimize max_depth, n_estimators, learning_rate.

2.Try other models like:

LSTM or Prophet for capturing time-series seasonality.

LightGBM or CatBoost for structured boosting.

Use stacking ensemble to combine predictions from multiple models.

✅ Data Improvements

1.Remove outliers or smooth sudden spikes using rolling medians.

2.Ensure stationarity by differencing or using log/sqrt transforms.

✅ Validation

1.Use TimeSeriesSplit instead of simple train-test split for better evaluation.

2.Try cross-validation on time slices.










