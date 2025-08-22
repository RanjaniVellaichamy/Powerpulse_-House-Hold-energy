# Powerpulse_-House-Hold-energy
The goal of this project is to develop a machine learning model that can predict household energy consumption based on historical data. 

📌 Project Overview

PowerPulse is a machine learning project designed to forecast household energy consumption using time-series data. It helps:

🏠 Households → Monitor energy usage, reduce electricity bills, and encourage energy-efficient habits.

🔌 Energy Providers → Predict demand for better load management and pricing strategies.

🔍 Anomaly Detection → Identify irregular usage patterns that may indicate faults or unauthorized usage.

🌍 Environmental Impact → Reduce carbon footprint by promoting sustainable energy usage.

⚡ Smart Grid Integration → Enable predictive analytics for real-time optimization.

⚙️** Workflow**

🔹 1. Data Understanding & Exploration

Load .txt dataset into Pandas.

Perform Exploratory Data Analysis (EDA).

Handle missing values and detect anomalies.

🔹 2. Data Preprocessing

Combine Date and Time → datetime.

Resample per-minute data into hourly averages.

Create new features:

hour, day, month, weekday, is_weekend.

Normalize numeric features where required.

🔹 3. Feature Engineering

Shift Global_active_power to create target (next-hour prediction).

Select input features:

Global_active_power, Global_reactive_power, Voltage, hour, is_weekend.

🔹 4. Modeling

Train-Test split (shuffle=False to preserve time order).

Model used: RandomForestRegressor (100 trees, random_state=42).

Predict next-hour household power consumption.

🔹 5. Evaluation Metrics

MAE (Mean Absolute Error): Average prediction error magnitude.

RMSE (Root Mean Squared Error): Penalizes large deviations.

R² (Coefficient of Determination): Measures explained variance.

🔹 6. Visualization & Insights

Actual vs Predicted energy usage plot.

Feature importance ranking.

Time-series trends and patterns.

📊 Results

MAE: Low average error in predictions.

RMSE: Shows model effectively handles peaks/spikes.

R²: Indicates strong explanatory power.

Feature Importance: hour and Global_active_power were most influential.

