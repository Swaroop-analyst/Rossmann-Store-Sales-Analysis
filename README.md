# 🏪 Rossmann Store Sales Analysis — CRISP-DM (EDA-Focused Project)

## 📌 Project Overview
This project follows the **CRISP-DM (Cross-Industry Standard Process for Data Mining)** framework to perform a **structured exploratory and diagnostic data analysis (EDA)** on Rossmann store sales data.

The objective is to **understand historical sales behavior and key business drivers** such as promotions, customer traffic, seasonality, and store characteristics, and translate these findings into **actionable business outcomes**.

> ⚠️ Scope: This project is strictly **EDA-only**. No predictive modeling, forecasting, or machine learning outcomes are used.

---

## 1️⃣ Business Understanding

### Business Problem
Retail organizations operate multiple stores with varying performance. Without structured analysis, it is difficult to understand:
- Why sales fluctuate over time
- How promotions influence revenue
- Why some stores consistently outperform others

### Business Objectives
- Analyze historical daily sales patterns
- Understand the impact of promotions and holidays
- Examine customer behavior and store-level variability
- Support retail decision-making using data insights

### Business Success Criteria
- Clear identification of sales drivers
- Business-interpretable insights
- Transparent and reproducible analysis

---

## 2️⃣ Data Understanding

### Dataset Description
The dataset contains historical daily sales records for Rossmann stores, including:
- Store ID
- Date
- Sales
- Customer count
- Promotion indicator
- State and school holidays
- Store type and assortment

### Exploratory Analysis Performed
- Dataset structure and size validation
- Date parsing and time-based exploration
- Missing value analysis
- Summary statistics of sales and customers
- Visualization of sales trends and distributions

### Key Data Observations
- Sales values vary significantly across stores
- Customer count and sales show a strong positive relationship
- Promotional days tend to record higher sales
- Sales exhibit clear weekly and seasonal patterns

---

## 3️⃣ Data Preparation

### Preparation Steps
- Conversion of date column to datetime format
- Extraction of time-based features (year, month, week, day indicators)
- Handling missing values
- Filtering of closed or invalid store records
- Creation of derived features to support analysis

### Outcome
A clean, analysis-ready dataset suitable for:
- Retail performance analysis
- Promotion effectiveness studies
- Management reporting and dashboards

---

## 4️⃣ Modeling (Not Used for Outcomes)

> 🚫 No predictive modeling used

Although experimental modeling code exists in the notebook, **model outputs are not used for insights or conclusions**.

📊 Model Performance Summary
<img width="934" height="422" alt="image" src="https://github.com/user-attachments/assets/5834cf1e-807a-4081-abe1-5eeeb8c650c8" />

🔎Interpretation
Stacking outperforms all other models, showing the value of combining multiple learners.

Random Forest is a solid single‑model choice, but stacking reduces RMSE by ~10%.

AdaBoost struggles compared to Random Forest, likely due to sensitivity to variance in sales data.

Decision Tree alone is not sufficient — ensemble methods clearly improve predictive accuracy.

## 5️⃣ Evaluation & Key Insights

### Promotion Impact
- Promotional periods are associated with higher average daily sales
- Promotion effectiveness varies across stores
- Promotions influence both customer footfall and revenue

### Customer Behavior
- A strong positive relationship exists between number of customers and sales
- Stores with consistent customer traffic demonstrate more stable sales patterns

### Seasonality & Time Patterns
- Sales follow weekly cycles, with certain weekdays outperforming others
- Seasonal peaks are observed during specific months and holiday periods
- Some stores show end-of-month sales effects

### Store-Level Variability
- Sales distribution across stores is highly skewed
- Store type and assortment influence baseline sales levels
- Not all stores respond equally to promotions and holidays

---

## 6️⃣ Business Outcomes & Practical Implications

### Operational Outcomes
- Promotion strategies should be tailored by store type
- Staffing and inventory planning can align with high-sales weekdays and peak seasons
- Stores with persistently low customer traffic can be flagged for operational review

### Strategic Outcomes
- Improved evaluation of promotion effectiveness
- Better store-level benchmarking and comparison
- Strong historical baseline for management decision-making

### Analytical Outcomes
- Key sales drivers identified through descriptive analysis
- Dataset well-understood and analysis-ready
- Foundation for future advanced analytics (optional)

📑 Assignment Summary – Rossmann Sales Prediction
🏆 Best Performing Model
Stacking Ensemble delivered the most accurate forecasts.

RMSE: 1196.40

MAE: 821.33

This demonstrates the power of combining multiple models to reduce error and improve reliability.

🔑 Key Features Driving Sales (Random Forest Importance)
Customers: 0.911 → Strongest predictor of sales volume.

Recency: 0.044 → Recent purchase behavior influences demand.

Promo: 0.027 → Promotional campaigns boost short‑term sales.

DayOfWeek: 0.014 → Weekly shopping patterns affect store traffic.

SchoolHoliday: 0.004 → Minor impact, but relevant for family‑oriented purchases.

⚙️ Data Preprocessing
Original dataset shape: (978,389 × 8 features)

Final dataset shape: (978,389 × 7 features) after cleaning and feature selection.

Training set size: 684,872 samples

Test set size: 293,517 samples

📊 Model Performance Ranking

<img width="906" height="316" alt="image" src="https://github.com/user-attachments/assets/11854347-7590-490c-a780-47fe8a886c0a" />


## 🧰 Tech Stack
- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Jupyter Notebook

---

## 📁 Repository Structure
```
Rossmann-Sales-Analysis/
├── notebooks/
│   └── Rossman sales updated.ipynb
├── README.md
└── requirements.txt
```

---


