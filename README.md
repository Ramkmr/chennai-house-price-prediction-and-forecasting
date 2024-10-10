Time Series forecasting with SARIMAX and XGBoost: Chennai House price prediction and forecasting

Project Overview:

1. Data Preprocessing
The raw dataset is first cleaned and preprocessed. This includes:

Filling missing values with relevant imputation methods.
Correcting misspellings in categorical data (e.g., fixing incorrect values in the SALE_COND column).
Dropping irrelevant columns and handling duplicates.
Filling missing dates and dealing with extra records using custom logic.
Removing outliers and handling the remaining missing data using forward fill.

2. Feature Engineering
Key features are extracted to enhance model performance:

Encoding categorical features like SALE_COND, AREA, etc.
Aggregating area-based rankings.
Deriving additional features relevant to the time series and predictive models.

3. Time Series Forecasting (SARIMAX)
The SARIMAX (Seasonal ARIMA with eXogenous variables) model is used for time series forecasting. Key steps:

Hyperparameter tuning for SARIMA (p, d, q, P, D, Q, S).
Residual analysis and error metrics for evaluating the model's performance.
Forecasting future trends based on historical data.

4. XGBoost Model for Prediction
The XGBoost model is trained on temporal and non-temporal features:

Cross-validation using TimeSeriesSplit.
Predictions using the result of time series forecasting as part of the feature set.
Calculation of performance metrics such as R² and Mean Absolute Error (MAE).
Installation and Setup
Clone the repository:

bash
Copy code
git clone <repository-url>
Install dependencies:

bash
Copy code
pip install -r requirements.txt
Add your data into the data/ folder (raw dataset as raw_data.csv).

Run the Jupyter notebooks sequentially to understand each step of the pipeline:

Start with 1_data_preprocessing.ipynb for cleaning the raw dataset.
Proceed with 2_feature_engineering.ipynb to extract features.
Continue to 3_time_series_forecasting.ipynb to train the SARIMAX model.
Finish with 4_xgboost_model_training.ipynb to train and evaluate the XGBoost model.

Future Enhancements

Web Application: A user interface (UI) can be built for real-time forecasting and predictions using the trained models.

Azure Integration: Deployment of the models using Azure services to enable scalable and accessible forecasting.

<meta name="google-site-verification" content="sUrPFZwBbkptQfWmzCniDt_pZduLICBlL28o3fFXFOw" />
