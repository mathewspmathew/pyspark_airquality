# 🏭 Prediction of Air Quality (CO) and Segmentation into Categories  

## 📌 Overview  
This project focuses on **predicting air quality** using the [UCI Air Quality Dataset](https://archive.ics.uci.edu/dataset/360/air+quality).  
Specifically analyze **Carbon Monoxide (CO) levels**, perform regression to predict pollutant concentrations, and apply classification to segment air quality into actionable categories.  

---

## 📊 Dataset  
- **Source**: UCI Machine Learning Repository  
- **Description**: The dataset contains hourly averaged responses from a chemical multisensor device deployed in an Italian city, along with meteorological data.  
- **Features**: Temperature, humidity, sensor readings (e.g., NOx, NMHC, etc.)  
- **Target**: `CO_GT` (true hourly averaged CO concentration in mg/m³)  

---

## 🔧 Steps Performed  

### 1. Data Cleaning  
- Removed placeholder values (`-200`) and missing data.  
- Dropped irrelevant/duplicate columns.  

### 2. Regression (Predicting CO concentration)  
- **Linear Regression** (with StandardScaler for feature normalization).  
- **Random Forest Regressor** (nonlinear model for better handling of sensor data).  
- Compared performance using **RMSE (Root Mean Squared Error)**.  

### 3. Classification (Segmenting Air Quality)  
- Converted continuous CO values into 4 AQI-based categories:  
  - `0` → Good (0–1 mg/m³)  
  - `1` → Moderate (1–2 mg/m³)  
  - `2` → Unhealthy (2–9 mg/m³)  
  - `3` → Hazardous (>9 mg/m³)  
- Trained **RandomForestClassifier** to predict these categories directly from sensor features.  
- Evaluated with **Accuracy Score**.  

---

## 📈 Results  
- **Regression**:  
  - Linear Regression RMSE: ~ *0.4908*  
  - Random Forest RMSE: ~ *0.4842*  
- **Classification**:  
  - Random Forest Classifier Accuracy: ~ *0.845*  

---

## 📂 How to Run  
1. Clone this repo or open the Colab notebook.  
2. Upload the UCI dataset file.  
3. Run cells step by step:  
   - Daling & Regression  
   - Classificatata Cleaning  
   - Feature Scion & Evaluation  
