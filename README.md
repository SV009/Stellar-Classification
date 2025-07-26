🌌 Stellar Classification Analysis

A machine learning-based classification system for astronomical objects using Sloan Digital Sky Survey (SDSS) data. This project applies supervised models (Random Forest, AdaBoost, KNN, Decision Tree) and unsupervised K-Means clustering to classify stars, galaxies, and quasars. Random Forest achieved the highest test accuracy of 98%, supported by strong F1-scores and robustness. Includes EDA, model comparison, and visualizations for scientific and practical insights in astrophysical data mining.

---

📌 Project Overview

This project aims to classify celestial objects—stars, galaxies, and quasars—based on their spectral and positional data using machine learning. The dataset, sourced from SDSS via Kaggle, includes 100,000 observations with 18 attributes.

---

🔍 Exploratory Data Analysis (EDA)

- Visualized class distribution using scatter plots of astronomical coordinates
- Analyzed redshift vs. plate ID across classes
- Explored feature relationships via correlation heatmaps and pairwise plots

---

🔧 Machine Learning Models

✅ Supervised Learning
- **Random Forest Classifier** – Best performance (98% test accuracy)
- **AdaBoost Classifier**
- **K-Nearest Neighbors (KNN)**
- **Decision Tree Classifier**

Each model was fine-tuned using Grid Search or Randomized Search and evaluated using precision, recall, and F1-score.

🔄 Unsupervised Learning
- **K-Means Clustering**
  - Applied with k=3 (based on elbow method)
  - Visualized cluster separation using key spatial and spectral features

---

🏆 Results Summary

| Model         | Accuracy | Notes                                 |
|---------------|----------|----------------------------------------|
| Random Forest | 98.00%   | Best overall performance               |
| AdaBoost      | 97.30%   | High scores across classes             |
| KNN           | 96.07%   | Good with proper scaling               |
| Decision Tree | 96.65%   | Highly interpretable                   |
| K-Means       | 94.1%*   | Purity score – useful for EDA          |

---



