Airline Passenger Demand Forecasting Using ARIMA 
Abstract 
In this project, a comprehensive time series analysis was performed on monthly airline passenger 
data collected over several years. The objective was to analyze long-term growth trends, seasonal 
patterns, and random variations in passenger demand. The study involved visual inspection of the 
t
ime series, stationarity testing using the Augmented Dickey-Fuller (ADF) test, differencing 
techniques, autocorrelation and partial autocorrelation analysis (ACF & PACF), and ARIMA model 
development. The results revealed a strong upward trend, clear yearly seasonality, and non
stationarity in the original series. After applying appropriate differencing, the data became stationary 
and suitable for ARIMA modeling. This analysis enables accurate forecasting of future passenger 
demand for effective airline resource planning. 
Problem Statement 
Airline passenger demand is influenced by various time-dependent factors such as economic growth, 
seasonal travel trends, holidays, and tourism patterns. Without analyzing the time series structure, 
forecasting models may generate inaccurate predictions, leading to inefficient aircraft utilization and 
operational losses. 
The goal of this project is to analyze airline passenger data to: 
• Identify long-term growth trends 
• Detect seasonal patterns 
• Measure temporal dependence 
• Test stationarity conditions 
• Develop reliable ARIMA forecasting models 
Table of Contents 
1. Dataset Loading and Preprocessing 
2. Time Series Visualization 
3. Stationarity Testing and Differencing 
4. Autocorrelation Function (ACF) Analysis 
5. Partial Autocorrelation Function (PACF) Analysis 
6. ARIMA Model Development 
7. Model Evaluation and Forecasting 
8. Interpretation of Results 
9. Summary 
10. References 
Dataset Loading and Preprocessing 
The airline passenger dataset was loaded using the Pandas library. The Month column was converted 
into datetime format and set as the time index to enable time series operations. The frequency of 
the dataset was set to monthly to ensure consistency. 
Key preprocessing steps: 
• Converted Month column to datetime format 
• Set Month as time index 
• Assigned monthly frequency 
• Checked for missing values 
These steps ensured the dataset was properly structured for ARIMA modeling. 
Time Series Visualization 
A time series plot was generated to observe passenger demand over time. 
Observations: 
• A steady increase in passenger numbers over years 
• Clear seasonal peaks during specific months 
• Repetitive yearly patterns 
• Minor short-term fluctuations 
The visualization confirmed the presence of both trend and seasonality in the data. 
Stationarity Testing and Differencing 
To verify whether the time series was stationary, the Augmented Dickey-Fuller (ADF) test was 
applied. 
Initial Results: 
• ADF Statistic ≈ −1.35 
• p-value ≈ 0.60 
Since the p-value was greater than 0.05, the null hypothesis of non-stationarity could not be 
rejected. 
To make the series stationary, first-order differencing was applied. 
After Differencing: 
• Trend was removed 
• Mean and variance became stable 
• Series became suitable for modeling 
This step was essential for ARIMA implementation. 
Autocorrelation Function (ACF) Analysis 
The ACF plot was used to examine the correlation between passenger values and their past 
observations. 
Findings: 
• High correlation at early lags 
• Gradual decay pattern 
• Periodic spikes at seasonal intervals 
These patterns indicated strong temporal dependence and seasonal behavior in the dataset. 
Partial Autocorrelation Function (PACF) Analysis 
PACF analysis was performed to measure direct relationships between current and lagged values. 
Observations: 
• Significant spikes at initial lags 
• Rapid decline after certain lags 
• Limited influence beyond early lags 
These results helped in selecting appropriate autoregressive (AR) parameters for the ARIMA model. 
ARIMA Model Development 
Based on ACF and PACF analysis, an ARIMA(2,1,2) model was selected for forecasting. 
Model Components: 
• p = 2 (Auto-Regressive terms) 
• d = 1 (Differencing order) 
• q = 2 (Moving Average terms) 
The model was trained using 80% of the dataset, while the remaining 20% was reserved for testing. 
Model Evaluation and Forecasting 
Model performance was evaluated using statistical accuracy measures. 
Evaluation Metrics: 
• Mean Absolute Error (MAE) 
• Root Mean Squared Error (RMSE) 
Results indicated satisfactory predictive accuracy. 
The trained model was used to forecast passenger demand for the next 24 months. 
Forecast Analysis: 
• Continued upward trend 
• Recurring seasonal patterns 
• Stable long-term growth 
These forecasts assist airlines in capacity planning and scheduling. 
Interpretation of Results 
The analysis confirmed that airline passenger demand exhibits: 
• Strong upward growth trend 
• Clear yearly seasonality 
• High temporal dependence 
• Initial non-stationarity 
After differencing, the dataset satisfied stationarity conditions, enabling effective ARIMA modeling. 
The forecasting results were consistent with historical patterns, validating the reliability of the model. 
Summary 
This project successfully analyzed airline passenger data using time series techniques and ARIMA 
modeling. The dataset was found to be non-stationary due to trend and seasonality. Through 
differencing and correlation analysis, a suitable ARIMA model was developed and evaluated. The 
forecasting results provide valuable insights for airline management in optimizing resources and 
improving operational efficiency. 
