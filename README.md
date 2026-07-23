# Dynamic Supply Chain Risk Monitoring with Real-Time Predictions and Geospatial Heatmaps

## Overview

This project develops a scalable big data analytics pipeline to predict late delivery risks in e-commerce supply chains using Apache Spark. By combining distributed data processing, machine learning, and geospatial visualization, the system enables proactive identification of delivery delays at both the order and regional levels.

The project was completed as part of **IST 718 - Big Data Analytics**.

---

## Problem Statement

Supply chain disruptions and delayed deliveries significantly impact customer satisfaction and operational efficiency. Traditional reporting methods identify delays only after they occur.

This project addresses this challenge by:

- Predicting whether an order will be delivered late
- Identifying high-risk geographic regions
- Visualizing regional delivery risks using interactive heatmaps
- Supporting proactive logistics planning through predictive analytics

---

## Dataset

**Dataset:** DataCo Smart Supply Chain for Big Data Analysis

- Approximately **180,000** records
- **53 original features**
- Data includes:
  - Customer information
  - Order details
  - Shipping information
  - Product categories
  - Geographic locations
  - Financial metrics

After preprocessing, **34 features** were retained for modeling.

---

## Project Workflow

```
Data Ingestion
        ↓
Data Cleaning
        ↓
Feature Engineering
        ↓
Train / Validation / Test Split
        ↓
Machine Learning Models
        ↓
Model Evaluation
        ↓
Regional Risk Aggregation
        ↓
Interactive Geospatial Heatmap
```

---

## Technologies Used

- Apache Spark
- PySpark
- Spark MLlib
- Python
- Pandas
- Folium
- Matplotlib
- Jupyter Notebook

---

## Feature Engineering

The preprocessing pipeline included:

- Removing identifiers and leakage-prone variables
- Handling missing values
- Encoding categorical variables
- Extracting temporal features:
  - Order Day of Week
  - Month
  - Day
  - Hour
- Creating shipping delay features
- Preparing data for distributed machine learning

---

## Machine Learning Models

The following classification models were evaluated:

- Logistic Regression
- Decision Tree
- Random Forest
- Gradient Boosting Trees (GBT)
- Multi-Layer Perceptron (Simple)
- Multi-Layer Perceptron (One Hidden Layer)
- Multi-Layer Perceptron (Deep)

---

## Best Performing Model

### Tuned Gradient Boosting Trees (GBT)

| Metric | Score |
|---------|-------|
| AUC | **0.8618** |
| Accuracy | **0.7670** |
| Precision | **0.8710** |
| Recall | **0.6725** |
| F1 Score | **0.7590** |

The tuned Gradient Boosting Trees model achieved the highest overall predictive performance and was selected as the final model.

---

## Geospatial Visualization

Predicted late delivery probabilities were aggregated by geographic region and visualized using **Folium**.

The interactive heatmap:

- Displays regional delivery risk
- Uses color-coded markers:
  - 🟢 Low Risk
  - 🟡 Medium Risk
  - 🔴 High Risk
- Provides interactive tooltips containing:
  - Region
  - Risk Level
  - Average Late Delivery Probability

---

## Key Findings

- More than **54%** of orders experienced late delivery.
- First Class shipping unexpectedly showed the highest late delivery rate.
- Standard Class had the lowest late delivery rate.
- Geographic delivery risks varied across regions.
- Shipping-related variables were stronger predictors than financial variables.
- Order country, shipping mode, order status, geographic coordinates, and shipping schedule were among the most important features.
---
##  Results

<img width="1024" height="390" alt="image" src="https://github.com/user-attachments/assets/8e7f5961-b4b4-49d4-9231-a0e866db8ef3" />
<img width="1189" height="490" alt="image" src="https://github.com/user-attachments/assets/f7cedc1a-7681-44b5-a914-c4c3e9cb01ef" />
<img width="1389" height="975" alt="image" src="https://github.com/user-attachments/assets/0e5a5149-fa2e-48f5-ae16-856abc1aabd8" />
<img width="1389" height="490" alt="image" src="https://github.com/user-attachments/assets/b16d7bcb-4451-4836-afff-335e9c17c253" />

---

## Authors

- Isha Prakash Kadam
- Swetha Narasimhan
- Arun Prasadh Senthil


---

## References

DataCo Smart Supply Chain for Big Data Analysis, Mendeley Data (Version 5, 2020)

https://data.mendeley.com/datasets/8gx2fvg2k6/5

---

## License

This project was developed for academic purposes as part of the IST 718 Big Data Analytics course.
