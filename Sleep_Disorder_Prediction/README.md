# Sleep Disorder and Stress Level Prediction

## 📌 Project Overview
This project focuses on analyzing lifestyle and health parameters—such as sleep duration, quality of sleep, physical activity levels, stress levels, and BMI categories—to predict the presence of sleep disorders (`None`, `Insomnia`, or `Sleep Apnea`). 

By leveraging predictive modeling, this project aims to highlight the critical lifestyle factors affecting sleep health and provide an automated system for early anomaly detection.

---

## 📊 Dataset Description
The dataset used for this project is the **Sleep Health and Lifestyle Dataset** sourced from Kaggle. It contains 374 rows and 13 columns, covering a comprehensive set of variables:
- **Demographics:** Gender, Age, Occupation
- **Sleep Metrics:** Sleep Duration (hours), Quality of Sleep (scale 1-10)
- **Lifestyle Features:** Physical Activity Level (minutes/day), Stress Level (scale 1-10), Daily Steps
- **Health Indicators:** BMI Category, Blood Pressure (Systolic/Diastolic), Heart Rate
- **Target Variable:** Sleep Disorder (`None`, `Insomnia`, `Sleep Apnea`)

---

## 🛠️ Methodology & Pipeline

### 1. Data Cleaning & Feature Engineering
- Handled missing values in the target feature by mapping unclassified entries to `None`.
- Split the composite `Blood Pressure` string column into two distinct numerical features: `Systolic_BP` and `Diastolic_BP`.
- Removed redundant columns like `Person ID` to ensure optimal performance.

### 2. Categorical Encoding
- Encoded the categorical target variable using `LabelEncoder`.
- Applied One-Hot Encoding (`pd.get_dummies`) to nominal categorical variables like `Gender`, `Occupation`, and `BMI Category` to make them machine-readable.

### 3. Model Training & Evaluation
- Partitioned the dataset into an **80% Training set** and a **20% Testing set** using standard stratification rules.
- Performed Feature Scaling using `StandardScaler` to uniformize numerical feature scales.
- Trained a robust **Random Forest Classifier** to model nonlinear feature relationships effectively.

---

## 🏆 Key Results
The Random Forest model achieved highly stable metrics on the unseen test partition:

- **Overall Model Accuracy:** `88.00%`
- **Class-wise Performance (F1-Scores):**
  - `None` (Healthy Sleep): **0.97** (High precision and recall)
  - `Insomnia`: **0.76**
  - `Sleep Apnea`: **0.76**

### Confusion Matrix Insights
The confusion matrix demonstrates that the model rarely confuses healthy individuals with those suffering from sleep conditions, proving its high diagnostic reliability for baseline screenings.

---

## 📂 Project Directory Structure
```text
Sleep_Disorder_Prediction/
├── dataset.csv                   # Cleaned lifestyle dataset
├── sleep_disorder_analysis.ipynb # Complete Jupyter Notebook with EDA and Model
└── README.md                     # Comprehensive project documentation