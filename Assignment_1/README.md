[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/gplg9GEB)
# Assignment1

## Introduction
This assignment is part of the DTU course **46765 – Machine Learning for Energy Systems**. The goal is to apply various machine learning methods to support **wind power forecasting and market bidding** in the **day-ahead electricity market**.

Specifically, the assignment involves:
- Data preprocessing and feature engineering using real-world data from the **EnergyDataDK** platform.  
- Developing **linear, non-linear, weighted, and regularized regression models** to predict next-day wind power.  
- Implementing **unsupervised learning** to cluster data and train local models.  
- Extension of the analysis with **decision-focused learning** to optimize bidding strategies.  
- Evaluating model performance based on both **forecast accuracy and market revenue**.

The report is attached to the repository, namely ```Assignment_1_report.pdf ``` 

## File Structure

```bash
├── data/
│   ├── RawData_20200101-20241231/
│   ├── ProcessedData/
│   ├── final_data.csv
│   ├── final_data_train.csv
│   └── final_data_test.csv
│
├── 0_preprocessing.ipynb
├── 1b_feature_engineering.ipynb
├── 1c_linear_regression.ipynb
├── 1c-f_retrained.ipynb
├── 1d_non_linear_regression.ipynb
├── 1e_weighted_regression.ipynb
├── 1f_regularized_regression.ipynb
├── 1g_results.ipynb
├── 1h_unsupervised_learning.ipynb
├── 2_decision_focused_learning.ipynb
│
├── requirements.txt
├── Assignment_1_report.pdf  
└── README.md

```


## Notebook Overview

| File | Description |
|------|--------------|
| **0_preprocessing.ipynb** | Loads merged raw data, performs gap handling, ensures hourly resolution and splits in train and test data sets. |
| **1b_feature_engineering.ipynb** | Investigates feature importance and performs relevant feature engineering |
| **1c_linear_regression.ipynb** | Establishes the **baseline linear regression model**, comparing closed-form and optimization-based implementations. Evaluates predictive accuracy and computational efficiency. |
| **1d_non_linear_regression.ipynb** | Introduces **feature transformations** to capture non-linear relationships and compares their performance against the baseline model. |
| **1e_weighted_regression.ipynb** | Implements **locally weighted regression** to assign more importance to nearby data points, improving local prediction accuracy. |
| **1f_regularized_regression.ipynb** | Applies **L1 (Lasso)** and **L2 (Ridge)** regularization to prevent overfitting. Explores effects of regularization on model coefficients and performance. |
| **1c-f_retrained.ipynb** | Applies all of the prior techniques but included retraining of the models with past test data, demonstrating improved performance |
| **1g_results.ipynb** | Used to summarize and visualize results from sripts 1c-f |
| **1h_unsupervised_learning.ipynb** | Clusters data (e.g., via K-means) and trains separate regression models for each cluster to evaluate performance improvements. |
| **2_decision_focused_learning.ipynb** | Formulates and implements a **decision-focused learning** framework to directly optimize revenue-oriented bidding strategies. |
| **requirements.txt** | Lists all Python dependencies needed to reproduce the results. |

## Data Description

- **Source:** [EnergyDataDK](https://www.energydata.dk/)  
- **Scope:**  
  - Wind power production (Snorrebakken wind farm, Bornholm, DK2)  
  - Weather and climate data from nearby stations  
  - Day-ahead and balancing market prices  

## Setup Instructions

To ensure reproducibility, create a **virtual environment** and install dependencies:

```bash
# Clone repository
git clone https://github.com/DTU-ML4ES-2025/assignment-1-awesome
cd assignment-1-awesome

# Create and activate virtual environment
python -m venv venv
source venv/bin/activate   # on Mac/Linux
venv\Scripts\activate      # on Windows

# Install dependencies
pip install -r requirements.txt
```

## Usage

1. Run notebooks sequentially:
   - `0_preprocessing.ipynb` → `1b_feature_engineering.ipynb` → `1c_...` etc.
2. The processed datasets are automatically generated.
3. Final model results and revenue calculations are visualized in `1g_results_and_revenue.ipynb` and '2_decision_focused_learning.ipynb'

## Authors

Group members names and participation details are listed in the project report.
