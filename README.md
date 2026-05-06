# Customer Churn Prediction — SQL + ML Pipeline

## Business Problem
Telecom companies lose revenue when customers cancel their subscriptions (churn).
This project predicts which customers are likely to churn so the business can take 
proactive retention action.

## What Makes This Project Different
All feature engineering is done in SQL — not pandas. This mirrors the real 
industry workflow where data analysts build feature tables in SQL before 
handing off to ML engineers.

## Dataset
- Source: IBM Telco Customer Churn (via Kaggle)
- Rows: 7,043 customers
- Columns: 21 features

## SQL Feature Engineering
Features created entirely in SQL using SQLite:
- tenure_group: Segmented customers into new / mid / loyal
- charge_tier: Categorized monthly charges into low / medium / high
- service_count: Counted total number of services per customer
- churn_label: Converted Yes/No to 1/0

## Model Results
| Model | ROC-AUC |
|-------|---------|
| Logistic Regression | 0.XX |
| Random Forest | 0.XX |

## Key SQL Insights Found
- Month-to-month contract customers churn at ~42% vs 11% for yearly contracts
- New customers (tenure under 12 months) have the highest churn rate
- High charge tier customers churn more despite using more services

## Tech Stack
SQLite · Python · pandas · scikit-learn · matplotlib · Google Colab

## Project Structure
- data/ — raw and engineered datasets
- notebooks/ — full Jupyter notebook with all code
- outputs/ — ROC curve, confusion matrix, feature importance charts
