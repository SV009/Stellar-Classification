# Stellar Classification Analysis

A machine learning-based approach to classify celestial objects—stars, galaxies, and quasars—using Sloan Digital Sky Survey (SDSS) data.
This project implements supervised learning (Random Forest, AdaBoost, KNN, Decision Tree) and unsupervised clustering (K-Means) to enable accurate and interpretable classification.
The Random Forest model achieved the highest accuracy of 98%, supported by balanced precision, recall, and F1-scores.

---

## Project Overview

Stellar classification is a critical step in astronomy for understanding the composition, structure, and evolution of celestial bodies.
This project applies machine learning techniques to 100,000 observations from SDSS (via Kaggle) to classify objects into:

Star

Galaxy

Quasar (QSO)

Beyond classification, the project also explores unsupervised clustering to identify natural groupings and data separability.

---
## Dataset
Source: Kaggle – Stellar Classification Dataset (SDSS17)

Size: 100,000 observations, 18 attributes (17 features + 1 class label)

Attributes: Spectral features, positional coordinates (right ascension, declination), redshift, photometric data

Classes: Star, Galaxy, Quasar

---

## Exploratory Data Analysis (EDA)

Key insights from EDA:

Spatial Distribution: Stars are clustered locally, galaxies form a dense central cluster, quasars are more scattered.

Redshift Patterns:

Stars → near zero redshift (close to Earth)

Galaxies → lower redshift (relatively closer)

Quasars → higher redshift (distant, fast-moving)

Correlation Analysis: Certain spectral features exhibit strong correlations with object classification.

---
## Methodology

### 1. Data Preprocessing

Renamed columns for clarity

Checked for missing/duplicate entries

Standardized numerical features (StandardScaler) for distance-based algorithms

### 2. Supervised Models

K-Nearest Neighbors (KNN)

Decision Tree Classifier

Random Forest Classifier

AdaBoost Classifier

### 3. Unsupervised Model

K-Means clustering with k = 3 (Elbow method)

### 4. Evaluation Metrics

Accuracy

Precision, Recall, F1-Score

Cross-validation scores for model reliability


---

## Results 

### Supervised Learning Models

| Model             | Accuracy   | Precision (Macro Avg) | Recall (Macro Avg) | F1-Score (Macro Avg) | Notes                               |
| ----------------- | ---------- | --------------------- | ------------------ | -------------------- | ----------------------------------- |
| **Random Forest** | **98.00%** | 0.98                  | 0.98               | 0.98                 | Best overall performance            |
| AdaBoost          | 98.00%     | 0.98                  | 0.98               | 0.98                 | High performance across all classes |
| Decision Tree     | 96.65%     | 0.97                  | 0.95               | 0.96                 | Highly interpretable                |
| KNN               | 96.07%     | 0.96                  | 0.96               | 0.96                 | Good with scaling                   |


### Unsupervised Learning (K-Means)

| Metric         | Score      | Notes                                  |
| -------------- | ---------- | -------------------------------------- |
| SSE            | -487102.98 | Lower value indicates tighter clusters |
| Purity Score\* | \~94.1%    | Indicates reasonable separation        |

*Calculated by mapping cluster labels to true classes for reference.
---
## Key Insights
Random Forest and AdaBoost provided the best classification results, achieving perfect or near-perfect metrics for Stars.

Decision Tree offers excellent interpretability with competitive accuracy.

KNN performs well when features are scaled.

K-Means clustering suggests that spatial and certain spectral features can reasonably separate object classes, though with some overlap.


