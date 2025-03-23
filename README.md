# COMP8230_assignment1
# 🚗 Stress Detection for Truck Drivers Using HRV and Machine Learning  

## 📌 Project Overview  
This project focuses on detecting **stress in truck drivers using heart rate variability (HRV) data** and **machine learning models**. The system processes **real-time HRV signals from wearable devices**, extracts key stress-related features, and classifies stress levels (**No Stress, Interruption, Time Pressure**) to improve driver safety and fleet management.

## 📂 Dataset  
We used the **SWELL HRV Dataset** and other HRV datasets to conduct experiments.  
- **Primary Dataset:** [SWELL HRV Dataset](https://www.kaggle.com/datasets/qiriro/swell-heart-rate-variability-hrv)  
- **Target Variable Categories:** `"No Stress"`, `"Interruption"`, `"Time Pressure"`  

The features used (**HR, RMSSD, pNN50, TP, VLF**) were selected based on:  
✅ **Spearman Correlation Analysis** – Feature importance was determined using correlation with `"condition"` (stress state).  
✅ **Validation from Scientific Literature** – Research studies confirm these HRV metrics strongly correlate with stress (Schmidt et al., 2018).  

## 🛠️ Approach  
1. **Baseline Measurement (ECG, EDA, Respiration)**
   - One-time calibration to establish an individual stress threshold.
2. **Real-time HRV Monitoring**
   - Continuous stress tracking using smartwatches (Apple Watch, Garmin).
3. **Data Processing & Feature Extraction**
   - Filters noise and extracts **HRV-related stress markers**.
4. **Machine Learning Classification**
   - Models used: **Logistic Regression, Random Forest (RF), XGBoost**.
5. **Real-time Stress Detection Application**
   - Displays stress predictions, probability scores, and driver alerts.
6. **Fleet Management Integration (Optional)**
   - Identifies high-risk drivers and suggests interventions.

## 🏆 Results  
| **Model**         | **Accuracy (%)** | **F1-Score** | **Precision** | **Recall** |  
|------------------|----------------|------------|------------|---------|  
| Logistic Regression  | **62.13%**       | **58.0%**   | **61.0%**   | **62.0%**  |  
| Random Forest       | **72.50%**       | **70.0%**   | **74.0%**   | **72.0%**  |  
| XGBoost            | **90.0%**       | **89.0%**   | **90.0%**   | **90.0%**  | 

👉 **View full results and code in the Jupyter Notebook:** [Assignment1.ipynb](./Assignment1.ipynb)  


