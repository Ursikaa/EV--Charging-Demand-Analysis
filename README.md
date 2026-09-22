# EV Charging Demand Analysis and Prediction

## 📌 Project Overview

This project focuses on analyzing electric vehicle (EV) charging session data and predicting charging demand using Python and Machine Learning techniques.

The project was completed as part of the YuvaIntern internship program. The analysis covers data cleaning, exploratory data analysis (EDA), feature engineering, visualization, and machine learning-based demand prediction using a Random Forest Regression model.

## 🎯 Objectives

- Analyze EV charging session data.
- Clean and preprocess the dataset.
- Identify patterns and trends in charging demand.
- Study demand variations by hour, day, month, location, and charger type.
- Identify important factors affecting charging demand.
- Build a machine learning model to predict demand.
- Evaluate model performance using MAE, RMSE, and R² score.
- Generate useful insights for EV charging management.

## 📊 Dataset

The dataset contains EV charging session records with information related to:

- User ID
- Charger ID
- Charger Company
- Location
- Charger Type
- Start Date and Time
- End Date and Time
- Charging Duration
- Charging Demand

The original dataset contained 72,856 records.

After removing duplicate records, invalid negative-duration records, and extreme duration outliers, the final dataset contained approximately 68,904 usable records.

## 🧹 Data Preprocessing

The following preprocessing steps were performed:

1. Checked the dataset structure and data types.
2. Checked for missing values.
3. Removed 13 duplicate records.
4. Converted date-time columns into proper datetime format.
5. Created additional time-based features:
   - Start Hour
   - Start Day of Week
   - Start Month
6. Removed 17 records with negative charging duration.
7. Detected duration outliers using the IQR method.
8. Removed extreme duration values above the calculated upper bound of 445 minutes.
9. Checked the cleaned dataset again for missing and invalid values.

## 📈 Exploratory Data Analysis

Several visualizations were created to understand the dataset, including:

- Demand distribution
- Average demand by hour
- Average demand by day of week
- Average demand by month
- Location-wise demand analysis
- Charger type analysis
- Charger company analysis
- Duration vs Demand scatter plot
- Demand boxplot
- Duration boxplot
- Correlation heatmap

### Key EDA Findings

- Average charging demand was approximately 16.08 units.
- Median demand was approximately 13.52 units.
- Demand showed a noticeable time-based pattern.
- The highest average demand occurred around 11 PM.
- The lowest average demand occurred around 10 AM.
- Charger Type 1 showed higher average demand than Charger Type 0.
- Charging duration showed a strong positive relationship with demand.
- Location-wise demand varied considerably.
- Monthly and day-of-week variations were comparatively small.

## 🤖 Machine Learning

A Random Forest Regression model was used to predict charging demand.

### Features Used

- Charger Type
- Charger Company
- Duration
- Start Hour
- Start Month

### Target Variable

- Demand

The dataset was divided into training and testing sets using an approximately 80:20 split.

## 📊 Model Performance

| Metric | Random Forest |
|---|---:|
| MAE | 3.3779 |
| RMSE | 5.8427 |
| R² Score | 0.7469 |

### Interpretation

The Random Forest model achieved an R² score of approximately 0.747, indicating that the selected features explain a substantial portion of the variation in charging demand.

The MAE of approximately 3.38 means that the model's predictions differ from actual demand by about 3.38 units on average.

## ⭐ Feature Importance

The Random Forest model identified the following feature importance values:

| Feature | Importance |
|---|---:|
| Duration | 0.7712 |
| Charger Type | 0.0929 |
| Start Hour | 0.0657 |
| Start Month | 0.0563 |
| Charger Company | 0.0139 |

Charging Duration was the most influential feature, contributing approximately 77% of the model's feature importance.

## 🔍 Residual Analysis

Residual analysis was performed by comparing actual demand with predicted demand.

The mean residual was close to zero, indicating very little overall prediction bias. However, prediction errors increased for some high-demand sessions, showing that the model had more difficulty predicting extreme demand values.

## 💡 Key Insights

1. Charging duration is the strongest predictor of charging demand.
2. Higher-duration charging sessions generally correspond to higher demand.
3. Charger type has a noticeable influence on demand.
4. Charging demand varies throughout the day.
5. High-demand sessions are more difficult for the model to predict accurately.
6. Charger company has relatively low predictive importance compared with duration and charger type.

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook
- GitHub

## 📁 Project Files

- EV_Charging_Analysis.ipynb – Complete analysis and machine learning workflow.
- ChargingRecords.csv – Original dataset.
- Cleaned_ChargingRecords.csv – Cleaned dataset.
- RandomForest_Predictions.csv – Model prediction results.

## 🚀 Future Scope

The project can be extended by:

- Testing additional machine learning algorithms.
- Performing hyperparameter tuning.
- Adding more time-based and location-based features.
- Developing an interactive EV charging demand dashboard.
- Using advanced forecasting techniques for future demand prediction.
- Deploying the trained model as a web application or API.

## 👩‍💻 Internship Project

*Internship Organization:* YuvaIntern  
*University:* Uttarakhand Technical University  
*Project:* EV Charging Demand Analysis and Prediction  
*Domain:* Data Science and Machine Learning
