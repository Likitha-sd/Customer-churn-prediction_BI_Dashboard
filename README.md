# Customer-churn-prediction_BI_Dashboard

## 📌 Overview
This project builds a machine learning pipeline to predict **customer churn** using the Telco Customer dataset (7,043 records, 21 features). The goal is to identify customers likely to leave and provide interpretable insights into the drivers of churn.

---

## 📊 Dataset
- **Source**: Telco Customer Churn dataset
- **Size**: 7,043 rows × 21 columns
- **Target**: `Churn` (Yes/No)
- **Features**: Demographics, service subscriptions, contract type, billing method, monthly charges, and tenure.

---

## ⚙️ Methodology
1. **Data Preprocessing**
   - Removed `customerID` column
   - Encoded categorical variables using Label Encoding and One-Hot Encoding
   - Scaled numerical features (`tenure`, `MonthlyCharges`, `SeniorCitizen`)
   - Engineered `Tenure_Group` feature for grouped analysis

2. **Model Training**
   - Split dataset into train/test (80/20, stratified)
   - Trained **XGBoost Classifier** with tuned hyperparameters
   - Evaluated using **AUC-ROC, precision, recall, F1-score**

3. **Explainability**
   - Applied **SHAP** for global and local feature importance
   - Generated summary plots and force plots to highlight churn drivers

---

## 📈 Results
- **AUC-ROC**: 0.83
- **Accuracy**: ~79%
- **Precision/Recall (Churn class)**: Precision = 0.62, Recall = 0.52
- Key churn drivers: Contract type, tenure, internet service, monthly charges

---

## 🚀 Usage
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/churn-prediction.git
   cd churn-prediction
