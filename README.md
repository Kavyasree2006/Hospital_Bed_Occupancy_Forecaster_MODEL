# 🏥 AI Powered Hospital Bed Occupancy Forecasting System Using Machine Learning

> An end-to-end machine learning project that analyzes hospital occupancy patterns, predicts future bed utilization, detects overflow risk, generates capacity planning recommendations, and provides an interactive dark-mode HTML dashboard for operational decision support.

![Python](https://img.shields.io/badge/Python-3.12-blue.svg)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-purple.svg)
![Scikit--learn](https://img.shields.io/badge/Scikit--learn-ML-orange.svg)
![Random Forest](https://img.shields.io/badge/Best%20Model-Tuned%20Random%20Forest-green.svg)
![Dashboard](https://img.shields.io/badge/Dashboard-Interactive%20HTML-teal.svg)
![Status](https://img.shields.io/badge/Status-Completed-success.svg)

---

# 📌 Project Overview

The **AI Powered Hospital Bed Occupancy Forecasting System** is a healthcare analytics and forecasting project designed to support hospital capacity planning.

The system uses a synthetic hospital operations dataset to study:

- Hospital bed occupancy
- Patient admissions and discharges
- Emergency and ICU admissions
- Department-level utilization
- Seasonal occupancy patterns
- Holiday and special event effects
- Staff availability
- Future occupancy risk

The project combines **Data Analytics**, **Machine Learning**, **Forecasting**, **Overflow Risk Detection**, **Capacity Planning**, and an **Interactive Dashboard** into one complete workflow.

Unlike a simple EDA project, this system not only analyzes historical occupancy patterns but also predicts future hospital utilization and generates actionable recommendations for hospital administrators.

---

# 🚀 Features

## 🛏️ Hospital Occupancy Analysis

Analyzes hospital bed utilization using key operational fields such as:

- Total Hospital Beds
- Beds Occupied
- Occupancy Rate (%)
- Daily Admissions
- Daily Discharges
- Emergency Admissions
- ICU Admissions
- Staff Availability
- Average Length of Stay

---

## 📊 Exploratory Data Analysis

The project performs detailed EDA to identify hospital operation patterns.

EDA includes:

- Occupancy rate distribution
- Department-wise occupancy comparison
- Admission and discharge trends
- Seasonal occupancy fluctuations
- Holiday and special event analysis
- Correlation analysis
- Trend reports

---

## 🏥 Department Utilization Analysis

Department-wise occupancy trends were analyzed to understand which departments experience higher bed pressure.

Top department occupancy results:

| Department | Mean Occupancy Rate (%) |
|---|---:|
| Maternity | 80.731972 |
| Cardiology | 79.967361 |
| General Medicine | 79.929567 |
| ICU | 79.917551 |
| Emergency | 79.875909 |
| Surgery | 79.848595 |
| Pediatrics | 79.648041 |
| Orthopedics | 79.337928 |

Highest average occupancy:

```text
Maternity: 80.73%
```

Lowest average occupancy:

```text
Orthopedics: 79.34%
```

---

## 🍂 Seasonal Pattern Analysis

Seasonal occupancy analysis was performed to detect fluctuations in hospital demand.

| Season | Mean Occupancy Rate (%) | Min | Max | Std |
|---|---:|---:|---:|---:|
| Autumn | 80.052701 | 64.48 | 95.00 | 8.861978 |
| Winter | 80.019262 | 64.65 | 95.00 | 8.799558 |
| Summer | 79.999828 | 64.62 | 95.00 | 8.948450 |
| Spring | 79.544254 | 64.58 | 95.00 | 8.994486 |

Autumn showed the highest average seasonal occupancy.

---

## 🔄 Admission and Discharge Trend Analysis

The system analyzes daily admissions and discharges to understand patient flow.

A new feature was created:

```text
net_bed_change = Daily Admissions - Daily Discharges
```

This feature helps identify whether hospital bed pressure is increasing or decreasing.

- Positive net bed change means admissions are higher than discharges.
- Negative net bed change means discharges are higher than admissions.
- High positive net bed change may indicate rising occupancy pressure.

---

## 🤖 Machine Learning Forecasting

Multiple regression models were trained to predict:

```text
Occupancy Rate (%)
```

Models trained:

- Random Forest Regressor
- XGBoost Regressor
- Gradient Boosting Regressor
- Tuned Random Forest
- Tuned Gradient Boosting
- Tuned XGBoost

The best-performing model was:

```text
Tuned Random Forest
```

---

## ⚠️ Overflow Risk Detection

The project detects future capacity risk using threshold-based rules.

| Occupancy Rate | Risk Level |
|---|---|
| Below 70% | Low |
| 70% to below 85% | Moderate |
| 85% to below 95% | High |
| 95% and above | Critical |

Alerts are generated automatically when predicted occupancy crosses high-risk or critical-risk thresholds.

---

## 📈 7-Day Occupancy Forecast

The selected model generated a 7-day hospital occupancy forecast.

| Forecast Date | Predicted Occupancy Rate (%) | Capacity Status |
|---|---:|---|
| 2039-03-02 | 70.76 | Moderate Utilization |
| 2039-03-03 | 76.94 | Moderate Utilization |
| 2039-03-04 | 72.83 | Moderate Utilization |
| 2039-03-05 | 67.50 | Low Utilization |
| 2039-03-06 | 88.46 | High Utilization |
| 2039-03-07 | 78.33 | Moderate Utilization |
| 2039-03-08 | 88.40 | High Utilization |

Forecast summary:

| Metric | Value |
|---|---:|
| Average Forecast Occupancy (%) | 77.60 |
| Highest Forecast Occupancy (%) | 88.46 |
| Lowest Forecast Occupancy (%) | 67.50 |
| Highest Occupancy Date | 2039-03-06 |
| Most Common Capacity Status | Moderate Utilization |

---

## 🚨 Capacity Alerts

High-risk forecast days:

| Date | Occupancy Rate (%) | Risk Level | Alert |
|---|---:|---|---|
| 2039-03-06 | 88.46 | High | Prepare additional beds and staff |
| 2039-03-08 | 88.40 | High | Prepare additional beds and staff |

No critical-risk days were detected in the 7-day forecast.

---

## 🧭 Capacity Planning Recommendations

The system generates recommendations based on predicted occupancy risk.

### Low Utilization

```text
Capacity is stable. Continue routine monitoring and normal staffing levels.
```

### Moderate Utilization

```text
Maintain regular operations, monitor admissions and discharges, and keep backup staffing ready.
```

### High Utilization

```text
Prepare additional beds, increase staff coverage, monitor emergency admissions closely, and speed up discharge planning.
```

### Critical Utilization

```text
Activate emergency capacity plan, open overflow beds, increase ICU and emergency staff, postpone non-urgent admissions if needed, and review discharge readiness.
```

---

# 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Python | Programming language |
| Google Colab | Development environment |
| Mockaroo | Synthetic dataset generation |
| Pandas | Data processing and analysis |
| NumPy | Numerical operations |
| Matplotlib | Data visualization |
| Seaborn | Statistical visualization |
| Scikit-learn | Machine learning models and evaluation |
| XGBoost | Advanced boosting model |
| Joblib | Model serialization |
| HTML | Dashboard structure |
| CSS | Dashboard styling and dark mode |
| JavaScript | Dashboard interactivity |

---

# 📂 Project Structure

```text
hospital_occupancy_forecasting/
│
├── hospital_occupancy_7000.csv
├── hospital_train_dataset.csv
├── hospital_test_dataset.csv
├── seven_day_occupancy_forecast.csv
├── occupancy_forecast_alert_report.csv
├── capacity_planning_recommendations.csv
├── best_occupancy_forecasting_model.pkl
├── model_features.pkl
│
├── dashboard/
│   └── hospital_occupancy_interactive_dashboard.html
│
├── notebooks/
│   └── hospital_occupancy_forecasting.ipynb
│
├── reports/
│   └── final_project_documentation.md
│
└── README.md
```

---

# 📊 Dataset

The dataset was created using Mockaroo and contains synthetic hospital operations data.

Original dataset fields:

- Date
- Day of Week
- Month
- Season
- Total Hospital Beds
- Beds Occupied
- Occupancy Rate (%)
- Daily Admissions
- Daily Discharges
- Emergency Admissions
- ICU Admissions
- Department
- Public Holiday Indicator
- Special Event Indicator
- Staff Availability
- Average Length of Stay

Final combined dataset size:

```text
Approximately 6,944 records
```

---

# 🔄 Project Workflow

```text
Synthetic Hospital Dataset
        │
        ▼
Mockaroo Data Generation
        │
        ▼
CSV Export and Combination
        │
        ▼
Data Cleaning and Validation
        │
        ▼
Exploratory Data Analysis
        │
        ▼
Department and Seasonal Analysis
        │
        ▼
Feature Engineering
        │
        ▼
Train-Test Split
        │
        ▼
Machine Learning Model Training
        │
        ▼
Model Tuning and Evaluation
        │
        ▼
Tuned Random Forest Best Model
        │
        ▼
7-Day Occupancy Forecast
        │
        ▼
Overflow Risk Detection
        │
        ▼
Capacity Planning Recommendations
        │
        ▼
Interactive HTML Dashboard
```

---

# 📈 Feature Engineering

Engineered forecasting features include:

- Year
- Month Number
- Day
- Day of Year
- Week of Year
- Quarter
- Is Weekend
- Holiday Flag
- Special Event Flag
- Department Encoded
- Season Encoded
- Day of Week Encoded
- net_bed_change
- Lag Occupancy 1 Day
- Lag Occupancy 7 Days
- Rolling Occupancy 7 Days
- Rolling Admissions 7 Days

The final model used:

```text
25 input features
```

---

# 🧪 Train-Test Split

The dataset was sorted by date and split using an 80/20 split.

```text
X_train: (5555, 25)
y_train: (5555,)
X_test: (1389, 25)
y_test: (1389,)
```

This split preserves chronological order and supports forecasting evaluation.

---

# 🤖 Machine Learning Models

The following models were evaluated:

- Random Forest Regressor
- XGBoost Regressor
- Gradient Boosting Regressor
- Tuned Random Forest
- Tuned Gradient Boosting
- Tuned XGBoost

### Best Model

```text
Tuned Random Forest
```

### Model Performance

| Model | MAE | MSE | RMSE | R2 Score |
|---|---:|---:|---:|---:|
| Tuned Random Forest | 0.342179 | 0.232500 | 0.482182 | 0.997074 |
| Random Forest Regressor | 0.355484 | 0.245242 | 0.495219 | 0.996914 |
| Tuned Gradient Boosting | 0.426326 | 0.302186 | 0.549714 | 0.996197 |
| Tuned XGBoost | 0.465052 | 0.354678 | 0.595548 | 0.995536 |
| XGBoost Regressor | 0.585308 | 0.565292 | 0.751859 | 0.992886 |
| Gradient Boosting Regressor | 0.964290 | 1.589400 | 1.260714 | 0.979997 |

The **Tuned Random Forest** model achieved the lowest RMSE and highest R2 Score.

---

# 📊 Correlation Insights

Important correlations:

| Variables | Correlation |
|---|---:|
| Total Hospital Beds and Beds Occupied | 0.905666 |
| Beds Occupied and Occupancy Rate (%) | 0.406245 |
| Daily Admissions and Daily Discharges | 0.960989 |
| Daily Admissions and Emergency Admissions | 0.847505 |
| Daily Admissions and ICU Admissions | 0.698717 |

These results show that patient movement features are important for understanding hospital operational load.

---

# 💻 Interactive HTML Dashboard

An interactive dashboard was created using **HTML, CSS, and JavaScript**.

Dashboard file:

```text
hospital_occupancy_interactive_dashboard.html
```

The dashboard includes:

- Dark mode interface
- Light/dark mode toggle
- 7-day exact forecast view
- 14-day and 30-day projected forecast views
- Department filter
- High-risk and critical-risk threshold sliders
- Occupancy trend visualization
- Model performance visualization
- Department utilization section
- Forecast table
- Overflow alerts
- Capacity planning recommendations
- CSV export button

The dashboard uses actual project outputs, including:

- Tuned Random Forest model results
- 7-day forecast values
- Department occupancy values
- Overflow risk levels
- Capacity planning recommendations

---

# 📷 Dashboard Screenshots

Add screenshots after uploading the dashboard images to GitHub.

## Dashboard Overview

<img width="1366" height="768" alt="Screenshot (272)" src="https://github.com/user-attachments/assets/992023a4-f339-4888-9ef7-d6d81168eb85" />


## Forecast Trend

<img width="1366" height="768" alt="Screenshot (273)" src="https://github.com/user-attachments/assets/0fd2398c-4d62-468d-bf15-475093f068d0" />

## Overflow Alerts

<img width="1366" height="768" alt="Screenshot (274)" src="https://github.com/user-attachments/assets/9d28e9b6-6510-496d-ab7e-4e83467dfb41" />

## Capacity Planning

<img width="1366" height="768" alt="Screenshot (275)" src="https://github.com/user-attachments/assets/9276b3d0-1672-47e3-be96-a8bd59b31b2d" />

---

# 📦 Installation and Usage

Clone the repository:

```bash
git clone https://github.com/your-username/hospital-occupancy-forecasting.git
```

Move into the project folder:

```bash
cd hospital-occupancy-forecasting
```

Install dependencies:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost joblib
```

Run the notebook in Google Colab or Jupyter Notebook.

To open the dashboard:

```text
Open hospital_occupancy_interactive_dashboard.html in a web browser.
```

---

# 📁 Output Files

| File | Description |
|---|---|
| hospital_occupancy_7000.csv | Final combined synthetic dataset |
| hospital_train_dataset.csv | Training dataset |
| hospital_test_dataset.csv | Testing dataset |
| seven_day_occupancy_forecast.csv | 7-day forecast results |
| occupancy_forecast_alert_report.csv | Forecast alerts and risk levels |
| capacity_planning_recommendations.csv | Capacity recommendations |
| best_occupancy_forecasting_model.pkl | Saved trained model |
| model_features.pkl | Saved model feature list |
| hospital_occupancy_interactive_dashboard.html | Interactive dashboard |

---

# 🎯 Key Findings

- The **Tuned Random Forest** model performed best with an RMSE of **0.482182** and R2 Score of **0.997074**.
- The average 7-day forecast occupancy was **77.6%**.
- The highest predicted occupancy was **88.46%** on **2039-03-06**.
- Two high-risk days were detected: **2039-03-06** and **2039-03-08**.
- No critical-risk days were detected.
- Maternity had the highest average department occupancy at **80.73%**.
- Autumn showed the highest seasonal occupancy at **80.05%**.
- The dashboard provides an interactive way to monitor forecast trends, alerts, and recommendations.

---

# 🚀 Future Enhancements

- Connect dashboard to live hospital data.
- Add real-time bed management updates.
- Deploy dashboard as a web application.
- Add hospital department-level forecasting.
- Add ICU-specific risk forecasting.
- Add patient admission prediction.
- Integrate automated email or SMS alerts.
- Add database support for historical records.
- Use advanced time-series models such as Prophet, LSTM, or Temporal Fusion Transformer.
- Add explainable AI for model interpretation.

---

# 🎓 Learning Outcomes

Through this project, the following concepts were implemented:

- Synthetic data generation
- Data preprocessing
- Exploratory data analysis
- Feature engineering
- Regression-based forecasting
- Model tuning and optimization
- Forecast evaluation metrics
- Overflow risk detection
- Capacity planning logic
- Interactive dashboard development
- Healthcare analytics decision support

---

# 👩‍💻 Author

**K. Kavya Sree**

---

# ✅ Project Status

```text
Completed
```

