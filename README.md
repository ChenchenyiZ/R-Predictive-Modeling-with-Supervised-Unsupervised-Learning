# R-Predictive-Modeling-with-Supervised-Unsupervised-Learning
Project Title: Predicting Team Performance in NCAA Basketball 2025

Course: STAT 4194 - Advanced Statistical Modeling

Author: Chenchenyi Zhu

Date: March 2025

# 🏀 Overview

This project analyzes NCAA March Madness 2025 team performance using both unsupervised clustering (K-means, PCA) and supervised learning (LASSO, Ridge, XGBoost, Random Forest). Key findings reveal how offensive/defensive efficiency, player height, and seed rankings drive team success.

🔗 Dataset: NCAA Basketball March Madness 2025 (Custom dataset with 68 teams, 151 features)

# 🔍 Key Insights
## 🎯 Top Performance Drivers
Seed Ranking (#1 predictor in XGBoost/Random Forest)

Offensive Efficiency (+0.66 coefficient in Ridge regression)

Defensive Efficiency (-0.50 coefficient)

Average Height (+1.15 impact in Ridge)

## 📊 Model Performance

| Model           | RMSE  | Key Features Used               |
|-----------------|-------|----------------------------------|
| **XGBoost**     | 3.15  | Seed, Offensive/Defensive Stats  |
| **Ridge**       | 4.31  | Height, Experience               |
| **Random Forest**| 0.19* | Seed (80% variance explained)    |

*Mean squared residuals (scaled data)

# 🛠️ Methodology
## 1. Data Preprocessing
Subset to 68 teams in 2025 postseason

Focused on 6 key variables:

r
c("Seed", "Raw.Offensive.Efficiency", "Raw.Defensive.Efficiency", 
  "AvgHeight", "Experience", "Net.Rating")
Scaled/normalized data for clustering

## 2. Unsupervised Learning
K-means (k=4) clustered teams into:

Elite: Low seed, high offense (e.g., Duke, Houston)

Strugglers: High seed, weak offense (e.g., Alabama State)

PCA showed PC1 explains 49.7% variance (offensive stats dominate)

## 3. Supervised Learning
Best Model: XGBoost (RMSE=3.15)

Seed importance: 22.7 (Node Purity)

Ridge Regression identified height/experience as secondary factors

# 🏆 Actionable Takeaways
For Teams: Prioritize offensive drills (+0.38 pts per efficiency unit in LASSO) and recruit taller players.

For Analysts: Seed rankings are 80% predictive of Net Rating—use as baseline for bracket predictions.

Limitations: Experience showed low impact in XGBoost; focus on real-time stats over tenure.

# 🔧 Tools Used
R Libraries: xgboost, glmnet, factoextra, randomForest

Clustering: K-means (k=4), PCA

Regularization: LASSO (α=1), Ridge (α=0)

Tags: #SportsAnalytics #MarchMadness #XGBoost #NCAA #R

Note: Dataset sourced from Kaggle with custom preprocessing for 2025 season.
