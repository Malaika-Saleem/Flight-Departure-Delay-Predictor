# ✈️ Flight Departure Delay Predictor

**A machine learning project that predicts flight delays using weather and time-based features. Achieved 85% accuracy on Kaggle.**

---

## 📁 Project Overview

This repository contains a complete pipeline for predicting flight departure delays using classification and regression models. The analysis is based on weather conditions, time features, and historical flight data.

**Author:** Malaika Saleem  
**ID:** 22i0509 – AIC

---

## 🧠 Project Components

### 1. Data Analysis

#### ✅ Data Composition
- **Weather Features:** Temperature, Wind Speed, Humidity, Pressure, Precipitation  
- **Time Features:** Hour of Day, Month of Year  
- **Targets:**
  - *Binary:* On-time (0) or Delayed (1)
  - *Multi-class:* No Delay, Short Delay, Moderate Delay, Long Delay
  - *Regression:* Exact delay duration in minutes

#### 🔧 Preprocessing Steps
- Converted `.docx` files to JSON format and normalized using pandas  
- Exported dataset to CSV for analysis and modeling

#### 📊 Exploratory Data Analysis (EDA)
- Temporal trends between scheduled, estimated, and actual departure times
- Seasonal distributions in temperature and humidity
- Delay correlation with precipitation, wind speed, and pressure
- Peak delays identified during specific hours and months

---

### 2. Predictive Modeling

#### 🟢 Binary Classification
- **Model:** Random Forest  
- **Target:** On-time vs. Delayed  
- **Metrics:** Accuracy, Precision, Recall, F1-Score

**Key Points:**
- High accuracy due to dominant "No Delay" class
- Moderate recall performance for identifying delays

**Suggestions:**
- Address class imbalance with SMOTE or oversampling
- Temporal validation for real-world performance

#### 🔵 Multi-class Classification
- **Model:** Random Forest  
- **Target:** Delay severity categories  
- **Metrics:** Accuracy, Class-wise F1-Scores

**Observations:**
- Accuracy decreases as delay severity increases
- Most misclassifications between adjacent delay categories

**Suggestions:**
- Boosting models for better rare class handling
- Include temporal and geographic features

#### 🔴 Regression
- **Model:** Random Forest Regressor  
- **Target:** Delay duration in minutes  
- **Metrics:** MAE, MSE

**Insights:**
- Strong for small delays, weak on extreme values

**Suggestions:**
- Add interaction features (time-of-day × weather)
- Use gradient boosting to reduce variance and improve outlier handling

---

### 3. Practical Approaches

#### 🧬 Feature Engineering
- Derived `delay_duration = actualTime - scheduledTime`
- Encoded categorical variables (e.g., terminal info)

#### 🧠 Model Selection
- **Regression:** Gradient Boosting for nonlinear patterns  
- **Classification:** Ensemble models (Random Forest)

---

### 4. Evaluation and Tuning

- **Cross-validation:** Ensures generalizable metrics  
- **Hyperparameter Tuning:** Grid/Random Search  
- **Class Imbalance:** Resampling and weighted loss functions

---

### 5. 📈 Kaggle Results

- **Binary Classification:** *[Score not specified]*  
- **Multi-class Classification:** *[Score not specified]*  
- **Regression:** *[Score not specified]*  

---

## ✅ Recommendations

### 🔧 Feature Enrichment
- Integrate real-time weather data for live predictions  
- Add categorical indicators (e.g., holidays, weekends)

### 🚀 Model Optimization
- Use **XGBoost** for improved regression/classification  
- Perform extensive **hyperparameter tuning**

### 🌐 Deployment
- Deploy models as REST APIs  
- Monitor model performance with dashboards

### 🔭 Future Work
- Explore neural networks for regression models  
- Regional/geographical delay pattern analysis

---

## 📌 Conclusion

This project showcases the power of structured flight and weather data in predicting delays. With feature engineering, ensemble models, and hyperparameter tuning, high-performing models are achievable. The foundation is set for real-time deployment and continuous improvement.

---

## 🛠️ Technologies Used

- Python
- Pandas / NumPy
- Scikit-learn
- Random Forest
- XGBoost
- Matplotlib / Seaborn

---
