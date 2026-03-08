# Asteroid Risk Assessment & Orbital Dynamics Analysis

## Overview

This project focuses on analyzing asteroid data to identify **Potentially Hazardous Asteroids (PHA)** using machine learning classification models. Developed as part of **Math 748 (Numerical Analysis)** at San Francisco State University.

The dataset contains **670,000+ asteroid records** with 45 features including orbital properties (eccentricity, semi-major axis, inclination, MOID) and physical characteristics (absolute magnitude H, diameter).

---

## Key Results

| Model | Accuracy | Macro Avg Precision | Macro Avg Recall | Macro Avg F1 |
|-------|:---:|:---:|:---:|:---:|
| KNN | 0.97 | 0.57 | 0.88 | 0.66 |
| **Random Forest** | **1.00** | **0.99** | **1.00** | **0.99** |
| Gradient Boosting | 1.00 | 0.97 | 1.00 | 0.99 |

Random Forest and Gradient Boosting both achieved near-perfect classification performance after SMOTE balancing.

---

## Methodology

1. **Data Preparation** — Cleaned dataset, handled missing values with median imputation, encoded categorical targets
2. **Exploratory Analysis** — Pairplots and correlation heatmaps to understand feature relationships
3. **Class Balancing** — Applied SMOTE to address severe class imbalance (655K vs 1.4K samples)
4. **Feature Selection** — Selected 6 key orbital features: H, diameter, eccentricity, semi-major axis, inclination, MOID
5. **Model Training** — Compared KNN, Random Forest, and Gradient Boosting classifiers
6. **Feature Importance** — MOID (Minimum Orbit Intersection Distance) identified as the most important predictor

---

## Key Findings

- **MOID** is the strongest predictor of asteroid hazard classification (importance: 0.60)
- **Class imbalance** was the primary challenge — only 0.2% of asteroids are classified as potentially hazardous
- SMOTE oversampling dramatically improved minority class detection
- Random Forest achieved the best overall balance of precision and recall

---

## Tech Stack

- **Python** — Pandas, NumPy, Scikit-learn
- **Visualization** — Matplotlib, Seaborn
- **Models** — KNN, Random Forest, Gradient Boosting
- **Techniques** — SMOTE, Feature Importance Analysis, Correlation Analysis

## Course

**Math 748 — Numerical Analysis** | San Francisco State University | Professor Tao He

## Author

**Pooja Chavanpatil** — MS in Statistical Data Science, San Francisco State University
