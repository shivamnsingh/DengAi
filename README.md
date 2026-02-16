🦟 DengAI – Dengue Fever Case Prediction

A machine learning project to predict weekly dengue fever cases using environmental and climate data for:

San Juan, Puerto Rico

Iquitos, Peru

Built with a focus on performance, structured modeling, and time-aware validation.

📌 Overview

Dengue fever outbreaks are strongly influenced by climate conditions such as temperature, humidity, and rainfall.

This project builds city-specific regression models to forecast weekly case counts using historical environmental data.

Instead of combining both cities into a single model, each location is modeled independently due to major climatic differences.

🛠 Tech Stack

Data Processing: Polars, NumPy

Visualization: Matplotlib, Seaborn

Machine Learning: Scikit-Learn

Model Used: Linear Regression

Scaling: StandardScaler

⚙️ Approach
1. Data Preparation

Merged features and labels using city, year, and weekofyear

Handled missing values using forward and backward fill

Split dataset into:

sj_df (San Juan)

iq_df (Iquitos)

2. Exploratory Data Analysis

Generated correlation matrices for both cities

Identified key environmental drivers influencing dengue cases

Observed differing feature importance across cities

3. Feature Engineering

Selected high-correlation predictors

Applied StandardScaler to normalize features

4. Modeling

Built separate Linear Regression models per city

Used time-aware split (shuffle=False) to avoid data leakage

Evaluated using Mean Squared Error (MSE)

📊 Sample Output
City	Year	Week	Actual	Predicted
San Juan	2008	17	5	27.65
Iquitos	2010	25	4	6.99


🚀 Installation
git clone https://github.com/your-username/dengue-prediction.git
cd dengue-prediction
pip install -r requirements.txt


Run the notebook or main script to reproduce results.

🔮 Future Improvements

Time-series cross-validation

Lag-based climate features

Random Forest / XGBoost models

Hyperparameter tuning

📜 Note

This project was developed for the DengAI competition and is intended for educational purposes only.
