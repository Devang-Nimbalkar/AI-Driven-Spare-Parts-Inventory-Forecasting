# AI-Driven Spare Parts Inventory Forecasting System

## Project Overview

This project was developed for NewX Services to address spare parts inventory management challenges. Service centers often face two major issues:

- Excess inventory leading to higher holding costs.
- Insufficient inventory causing spare parts unavailability.

The objective of this project is to forecast spare parts demand and provide inventory recommendations to support Just-In-Time (JIT) inventory management.

---

## Business Problem

Managing spare parts inventory across multiple service centers is challenging due to fluctuating demand patterns. Organizations need a system that can accurately predict future demand and recommend inventory actions to reduce costs while maintaining product availability.

---

## Project Objectives

- Forecast future spare parts demand using Machine Learning.
- Analyze inventory patterns across suppliers and warehouses.
- Identify inventory items that require replenishment.
- Support Just-In-Time (JIT) inventory management.
- Reduce inventory holding costs and improve inventory utilization.

---

## Dataset Information

Dataset Size:
- 91,250 Records
- 15 Features

Key Features:
- Date
- SKU_ID
- Warehouse_ID
- Supplier_ID
- Region
- Units_Sold
- Inventory_Level
- Reorder_Point
- Order_Quantity
- Supplier_Lead_Time_Days
- Unit_Cost
- Unit_Price
- Demand_Forecast

---

## Data Preprocessing

The following preprocessing steps were performed:

- Missing value analysis
- Duplicate record checking
- Date feature extraction
- Label Encoding for categorical variables
- Feature engineering

Generated Features:
- Year
- Month
- Day
- Weekday

---

## Machine Learning Model

### Demand Forecasting Model

Algorithm Used:
- Random Forest Regressor

Target Variable:
- Units_Sold

Evaluation Results:

| Metric | Value |
|----------|----------|
| MAE | 2.12 |
| MSE | 7.16 |
| R² Score | 0.913 |

### Interpretation

The model achieved an R² score of 0.913, indicating that approximately 91.3% of the demand variation is explained by the model.

The Mean Absolute Error (MAE) of 2.12 indicates that the average prediction error is approximately 2 units.

---

## Inventory Recommendation Engine

Business Logic:

- Inventory Healthy
- Reorder Soon

Recommendation Rule:

If Inventory_Level ≤ Reorder_Point

→ Reorder Soon

Else

→ Inventory Healthy

Results:

| Recommendation | Count |
|---------------|--------:|
| Inventory Healthy | 86,209 |
| Reorder Soon | 5,041 |

---

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-Learn
- Matplotlib
- Seaborn
- Google Colab
- GitHub

---

## Project Structure

```text
AI-Driven-Spare-Parts-Inventory-Forecasting/

├── data/
├── notebooks/
├── images/
├── requirements.txt
└── README.md
```

---

## Key Achievements

- Processed and analyzed 91K+ inventory records.
- Built a demand forecasting model with R² = 0.913.
- Developed an inventory recommendation engine.
- Generated actionable insights for JIT inventory management.
- Created a scalable framework for inventory optimization.

---

## Future Enhancements

- Streamlit Dashboard Integration
- Real-Time Inventory Monitoring
- Multi-Warehouse Optimization
- Advanced Time-Series Forecasting
- Automated Procurement Recommendations

---
Model File Notice

The trained Random Forest model file (.pkl) is not included in this repository due to GitHub file size limitations.

Model Performance:
- MAE: 2.12
- MSE: 7.16
- R² Score: 0.913

The complete training workflow is available in the notebook provided in this repository.

## Author

Devang Nimbalkar

Final Year AIML Engineer
