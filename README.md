# 🎢 Theme Park Logistics: Predicting Crowd Flow and Wait Times

## Executive Summary
This project analyzes simulated operational theme park data to understand how external factors (time of day, day of the week) impact attraction wait times. The goal is to optimize guest routing and predict operational bottlenecks.

** Key Finding: ** Wait times predictably peak at 2:00 PM, with weekends adding an average of 20+ minutes to the baseline wait of high-demand attractions
## 🛠 Methodology
* **Data Generation:** Simulated operational data for Seven Dwarfs Mine Train, mimicking the structure of the TouringPlans historical dataset, including random operational downtime (`-999` anomaly flags).
* **Data Engineering:** Cleaned missing values, extracted datetime features, and normalized wait times for statistical accuracy.
* **Predictive Modeling:** Built a Random Forest Regressor to forecast wait times based on chronological features.

## 📊 Exploratory Data Analysis
`![Crowd Flow Chart](crowd_flow_chart.png)`)

As shown in the chart above, the standard operational day follows a distinct bell curve, requiring maximum staffing allocations between 1:00 PM and 4:00 PM.

## 🤖 Machine Learning Prediction
I deployed a `RandomForestRegressor` to predict future wait times. 
* **Model Accuracy (MAE):** The model predicts wait times with a Mean Absolute Error of ~8.5 minutes, allowing for highly accurate, near-real-time resource allocation.

## 💻 How to Run This Project
1. Clone the repository.
2. Open the `Disney_Logistics_Analysis.ipynb` notebook in Jupyter or Google Colab.
3. Run the cells sequentially to generate the simulated data and train the model.
