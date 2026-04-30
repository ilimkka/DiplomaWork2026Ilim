# Forecasting Labor Market Indicators in Kyrgyzstan Using Machine Learning

## Project Overview
This project forecasts Kyrgyzstan’s unemployment rate up to the year 2028 by combining machine learning (ML) techniques with time-series econometrics. It utilizes historical macroeconomic data (2000–2023) to build a predictive engine capable of modeling various economic scenarios.

## Methodology
The project follows a hybrid forecasting pipeline:
1.  **Data Preparation:** Cleaning raw World Bank data and handling specific economic indicators (Remittances, Gold prices, etc.).
2.  **Feature Importance:** Using Gradient Boosting, Random Forest, and XGBoost to identify the most significant macroeconomic predictors (Agri-Employment and Remittances were found to be key).
3.  **Stationarity Testing:** Augmented Dickey-Fuller (ADF) tests to determine the integration order for ARIMA modeling.
4.  **AutoARIMA Projection:** Forecasting the features themselves to create inputs for future scenarios.
5.  **ML Forecasting:** Using a Gradient Boosting Regressor trained on historical lags to predict the final unemployment rate.

## Key Scenarios
*   **Base (Inertial):** Persistence of current dynamics. Projected unemployment: ~3.54% by 2028.
*   **Deflationary:** Optimistic scenario with stable currency and cooling prices.
*   **Stagflationary Crisis:** Simulates economic shocks leading to a structural collapse (~6.56% unemployment by 2028).

## Repository Structure
*   `Finished_labor_data.csv`: Cleaned and transposed dataset used for modeling.
*   `DiplomaWorkMain.ipynb`: Complete technical implementation (Data cleaning -> ML Models -> Visualization).
*   `requirements.txt`: List of required Python libraries.

## Usage
Open the Jupyter Notebook and run the cells sequentially. The notebook is divided into parts: Data Preparation, Feature Importance, ARIMA Forecasting, and final ML Scenario building.
