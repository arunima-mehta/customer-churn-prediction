# Customer Churn Prediction & Retention Strategy

## Project Overview 
Built a production-ready ML system to identify at-risk customers and enable targeted retention strategies. The pipeline handles data extraction, preprocessing, model training with experiment tracking, and delivers insights through interactive dashboards.
Business Impact: Proactively identify 26.5% of customers at risk of churning, enabling data-driven retention campaigns worth potential millions in saved revenue.

## Key Features

- **SQL-Based ETL:** Automated data extraction from SQL Server views
- **Multi-Model Training:** Compared 5 algorithms (LightGBM, XGBoost, Random Forest, Logistic Regression, KNN)
- **SMOTE Balancing:** Handled 73:27 class imbalance for improved minority class detection
- **MLflow Tracking:** Logged 10+ experiments with metrics, parameters, and LIME explanations
- **Power BI Dashboard:** Interactive visualizations for business stakeholders
- **DVC Integration:** Data version control for reproducibility

## Tech Stack

- Languages: **Python 3.8+, SQL (T-SQL), DAX**
- ML Frameworks: **Scikit-learn, XGBoost, LightGBM**
- Data Processing: **Pandas, NumPy, imbalanced-learn**
- Experiment Tracking: **MLflow**
- Visualization: **Power BI, Matplotlib, Seaborn**
- Explainability: **LIME**
- Database: **SQL Server**
- Version Control: **DVC, Git**

## 📊 Model Performance

### Algorithms Evaluated

| Model | Dataset | Precision (Churn) | Recall (Churn) | F1 Score (Churn) |
|-------|---------|-------------------|----------------|------------------|
| Logistic Regression | Imbalanced | 0.65 | 0.58 | 0.61 |
| Random Forest | Imbalanced | 0.78 | 0.49 | 0.60 |
| **LightGBM** | **Balanced** | **0.88** | **0.92** | **0.90** |
| XGBoost | Balanced | 0.85 | 0.89 | 0.87 |
| KNN | Balanced | 0.82 | 0.85 | 0.83 |

### Final Model: LightGBM

## Key Insights

### Churn Risk Factors

1. **Contract Type**: Month-to-month contracts show 42% churn vs 11% for long-term
2. **Payment Method**: Electronic check users churn at 45% rate
3. **Tenure**: Customers with <12 months tenure are 3x more likely to churn
4. **Service Usage**: Fiber optic users without online security show higher churn
5. **Support Tickets**: Customers with 3+ tech support calls in last month at high risk

### Business Recommendations

- Incentivize contract upgrades (month-to-month → annual)
- Promote autopay/credit card payment methods
- Enhanced onboarding for new customers (<6 months)
- Bundle security services with fiber optic plans
- Proactive outreach for customers with multiple support tickets

### **Dashboard Features:**
- Real-time churn rate monitoring
- Customer segmentation by risk level
- Revenue impact analysis
- Drill-down by demographics and services
- Exportable customer lists for retention campaigns

## Experiment Tracking (MLflow)

All experiments are logged with:
- Model hyperparameters
- Training/validation metrics (Precision, Recall, F1, AUC-ROC)
- Feature importance scores
- LIME explanations for interpretability
- Model artifacts (.pkl files)

