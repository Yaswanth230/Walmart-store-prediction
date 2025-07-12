Capstone Project – Walmart Sales Forecasting

Table of Contents
Problem Statement


Project Objective


Data Description


Data Preprocessing Steps and Inspiration


Choosing the Algorithm for the Project


Motivation and Reasons for Choosing the Algorithm


Assumptions


Model Evaluation and Techniques


Inferences from the Project


Future Possibilities of the Project


Conclusion


References
Problem Statement
Walmart is facing challenges in accurately forecasting weekly sales across its stores, particularly during major holiday periods. Accurate predictions are crucial to optimize inventory, staffing, and overall operational efficiency, ultimately improving customer satisfaction and financial outcomes.

Project Objective
The objective of this project is to build a robust model to forecast weekly sales for each store and department in Walmart’s dataset. This will help in better planning and resource allocation to reduce overstock or stockouts, and to handle holiday season demand effectively.

Data Description
The dataset used is the Walmart Store Sales Forecasting Dataset, containing historical data on weekly sales from various Walmart stores.
Key columns include:
Store: Store number identifier.


Dept: Department number.


Date: Week-ending date.


Weekly_Sales: Sales amount for the given week.


Holiday_Flag: Indicates whether the week includes a holiday (1 = holiday week, 0 = non-holiday).


Temperature, Fuel_Price, CPI, Unemployment: External variables potentially affecting sales.


The dataset contains no missing values or duplicates after initial inspection.

Data Preprocessing Steps and Inspiration
The preprocessing steps included:
Date conversion: Converted date columns to datetime format for time-series analysis.


Sorting: Sorted data by store, department, and date to maintain temporal order.


Feature engineering: Created new features such as 'Year', 'Month', and 'Week' from the date.


Outlier detection: Checked for extreme sales values and corrected where necessary.


Seasonal decomposition: Used seasonal_decompose to analyze trend, seasonality, and residual components of weekly sales.


Scaling: Normalized numerical features to improve model convergence.



Choosing the Algorithm for the Project
For this forecasting task, we selected time-series decomposition and regression-based models (e.g., XGBoost Regressor), along with exploratory use of ARIMA for stationarity checks.
Reasons for selection:
Ability to handle seasonal trends.


Good performance on tabular data with multiple explanatory variables.


Scalability to handle multiple store-department combinations.



Motivation and Reasons for Choosing the Algorithm
XGBoost: Well-suited for large, structured datasets and can handle non-linear relationships effectively.


Decomposition analysis: Provided insight into trend and seasonal patterns, which are crucial for retail sales.


ARIMA (exploratory): Useful to validate time-series properties, though not used as the final model due to multivariate complexity.



Assumptions
Historical sales patterns are representative of future sales.


External variables (temperature, CPI, etc.) continue to influence sales similarly.


Holiday effect remains consistent year-over-year.


No major external disruptions (e.g., new competitor entry, extreme weather events).



Model Evaluation and Techniques
Techniques used:
Train-test split: Split the data based on date to simulate future prediction.


Cross-validation: Used time-based cross-validation to ensure no data leakage.


Error metrics: Evaluated using RMSE and MAPE to measure accuracy.


Evaluation results:
RMSE: Provided a measure of error magnitude.


MAPE: Helped understand relative error as a percentage.


The model achieved a relatively low RMSE and MAPE, indicating good predictive power on unseen data.

Inferences from the Project
Trend analysis: Overall upward trend with seasonal dips and spikes during holidays.


Holiday impact: Significant increases in sales during major holidays like Thanksgiving and Christmas.


External factors: Moderate influence of fuel price and CPI on sales.



Future Possibilities of the Project
Incorporating additional features such as local economic indicators, competitor data, or promotions.


Deploying a dynamic forecasting system updated weekly.


Using deep learning models (e.g., LSTM) for further improvements in sequence modeling.



Conclusion
The developed model successfully forecasts weekly Walmart sales with reasonable accuracy, helping improve planning and resource allocation. The analysis also provided insights into seasonal trends and the effect of external variables, supporting data-driven decision-making.
References
data set from intellpaat
I did all my own reference from pervious lectures

