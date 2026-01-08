[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/Gs8vJRhw)

# Assignment2

This assignment, part of **46765 – Machine Learning for Energy Systems**, applies supervised and reinforcement learning methods to operate a **Battery Energy Storage System (BESS)** using DK2 hourly electricity prices.

The assignment implements two modelling approaches:

- **Logistic Regression (Supervised Learning)**
- **Markov Decision Process + Value Iteration (Reinforcement Learning)**

A **perfect-foresight solution** is used as a benchmark for evaluating both models.


## File Structure

```bash
├── data/
│   └── Price.xlsx
│
├── 1_logistic_regression.ipynb
├── 2_reinforcement_learning.ipynb
├── 3_model_comparison.ipynb
│
├── report.pdf
├── requirements.txt
└── README.md
``` 

## Notebook Overview

| File | Description |
|------|-------------|
| **1_logistic_regression.ipynb** | Computes the Gurobi reference solution, constructs charge/discharge labels, trains a Logistic Regression model with time-series CV, tunes the decision threshold, and evaluates test-set profit. |
| **2_reinforcement_learning.ipynb** | Defines an MDP with discrete SOC and price bins, builds transition and reward matrices, runs value iteration, performs grid search over bins/γ, and tests the resulting policy. |
| **3_model_comparison.ipynb** | Compares Logistic Regression, RL policy, and the optimal benchmark through SOC trajectories, actions, hourly profit, and cumulative revenue. |

## Setup Instructions

```bash
git clone https://github.com/DTU-ML4ES-2025/assignment-2-awesome
cd assignment-2-awesome

python -m venv venv
source venv/bin/activate       # Mac/Linux
venv\Scripts\activate          # Windows

pip install -r requirements.txt
```

## Usage

Run the notebooks in the following order:
```md
1. `1_logistic_regression.ipynb`
2. `2_reinforcement_learning.ipynb`
3. `3_model_comparison.ipynb`
```

## Authors

Group member names and contributions are listed in the project report.