# 📊 Consumer Credit Risk Portfolio Analysis

A data analytics project investigating borrower credit behaviour and identifying key drivers of financial distress using a large-scale credit dataset.

This project combines **data analysis, statistical modelling, and risk segmentation** to quantify default risk and support data-driven credit decision-making.

---

## 🔗 Interactive Dashboard (Tableau Public)

Explore the interactive version here:  
👉 https://public.tableau.com/views/ConsumerCreditRiskPortfolioAnalysis/Dashboard1

---

## 📂 Dataset

Dataset: **Give Me Some Credit**

- **Total Borrowers:** 150,000  
- **Target Variable:** `SeriousDlqin2yrs`

| Value | Meaning |
|------|--------|
| 0 | No serious delinquency |
| 1 | Serious delinquency within 2 years |

---

## 🎯 Project Objectives

- Understand borrower behaviour patterns  
- Identify key drivers of default risk  
- Quantify impact of financial indicators  
- Segment borrowers based on risk  
- Enable data-driven credit decisions  

---

## 🛠️ Tools & Technologies

- Python (Pandas, NumPy)  
- Scikit-learn (Logistic Regression)  
- Stats-based interpretation (Odds Ratios)  
- Tableau Public (Dashboard)  

---

## ⚙️ Methodology

---

### 1. Data Cleaning

- Removed extreme outliers using 99th percentile capping  
- Handled missing values:
  - `MonthlyIncome` → median imputation  
  - `NumberOfDependents` → median imputation  
- Validated distributions and ensured data consistency  

---

### 2. Feature Engineering

#### Age Groups
- 20–30, 30–40, 40–50, 50–60, 60–70, 70+

#### Credit Utilisation Bands
- Low, Medium, High, Very High  

#### Risk Segmentation (Rule-Based)
- Created composite **risk score** using:
  - Utilisation  
  - Debt ratio  
  - Delinquency  
- Segmented borrowers into:
  - Low Risk  
  - Medium Risk  
  - High Risk  

---

### 3. Risk Profiling (Descriptive Analysis)

- Analysed default rates across:
  - Age groups  
  - Utilisation bands  
  - Delinquency levels  

---

### 4. Logistic Regression (Risk Modelling)

Built a logistic regression model to quantify default risk:

- Applied **feature encoding and scaling**
- Removed engineered leakage features (`risk_segment`, `risk_score`)
- Evaluated using **ROC-AUC**

#### 📊 Model Performance
- **ROC-AUC:** 0.84 → strong predictive power  

---

### 5. Key Risk Drivers (Model-Based)

Using odds ratios from the model:

- **Delinquency (30–59 days past due)** → ~**3.4× higher default risk**  
- **Credit Utilisation** → ~**2.3× higher risk**  
- **Delinquency flag** → ~**1.6× higher risk**  

👉 Behavioural variables significantly outperform demographic variables  

---

### 6. Credit Strategy Simulation

Simulated approval strategies using risk segmentation:

- Excluding high-risk borrowers:
  - Reduced default rate from **6.68% → ~3.6%**  
  - Maintained ~66% approval rate  

⚠️ *Note: This is a simulation-based scenario, not real deployment*

---

## 📊 Key Insights

1. **Default risk is behaviour-driven, not demographic-driven**  
   Delinquency and utilisation are significantly stronger predictors than age.

2. **Delinquency is the strongest predictor of default**  
   Borrowers with past delinquencies have ~**3.4× higher default risk**.

3. **High credit utilisation signals financial stress**  
   Borrowers with high utilisation exhibit ~**2.3× higher risk**.

4. **Risk segmentation effectively separates borrower behaviour**  
   High-risk borrowers show substantially higher default rates than low-risk groups.

5. **Portfolio risk is concentrated, not evenly distributed**  
   A small segment of borrowers contributes disproportionately to defaults.

---

## 💡 Business Recommendations

1. **Implement risk-based approval policies**  
   Use borrower risk segmentation to filter high-risk applicants and reduce portfolio defaults.

2. **Monitor credit utilisation proactively**  
   High utilisation should trigger risk alerts or credit limit controls.

3. **Apply stricter checks for delinquent borrowers**  
   Past delinquency is the strongest signal of future default.

4. **Adopt balanced credit strategies**  
   Avoid extreme rejection policies; focus on optimising approval vs risk trade-off.

5. **Incorporate model-driven risk scoring**  
   Use predicted default probabilities to enhance credit decision systems beyond rule-based segmentation.

---

## 📈 Business Impact

- Identified **6.68% portfolio default rate**  
- Quantified key risk drivers using statistical modelling  
- Demonstrated potential **~46% reduction in default rates (simulation)**  
- Enabled structured, data-driven credit risk assessment  

---

## 🚀 Conclusion

This project demonstrates an end-to-end credit risk analytics workflow:

- Data cleaning and feature engineering  
- Behavioural risk analysis  
- Statistical modelling using logistic regression  
- Risk quantification using odds ratios  
- Scenario-based decision simulation  
- Dashboard-driven storytelling  

---

## 👨‍💻 Author
**Ishita Kukreti**
