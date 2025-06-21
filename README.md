# Stroke Risk Classification using Machine Learning

This project explores various machine learning models to predict stroke risk based on a set of clinical-like symptoms and features. The analysis includes performance evaluation, feature analysis, and visual explanations.

We aim to:
- Explore the data distribution and feature-target relationships
- Train and compare multiple classification models
- Investigate feature importance and separation in 2D space (PCA)
- Evaluate robustness using Stratified K-Fold cross-validation

---

## Dataset

- Source: [Kaggle Stroke Prediction Dataset](https://www.kaggle.com/datasets/mahatiratusher/stroke-risk-prediction-dataset)
- Features: Demographics, health conditions, and lifestyle choices. 16 in total.
- Target used: `At Risk (Binary)` (1 = risk stroke, 0 = no risk) . Another Target exist but not used: (At Risk in %) for regression.

---

## Models Trained
- Logistic Regression
- Decision Tree
- Random Forest
- XGBoost

Each model was evaluated using **AUC** and **F1-score** metrics with cross-validation and tested on a held-out set.

---

## Final Model Comparison (Cross-Validation)

| Model               | AUC (Mean ± Std)   | F1 Score (Mean ± Std) |
|--------------------|--------------------|------------------------|
| Logistic Regression| 1.00000 ± 0.00000  | 0.99838 ± 0.00050      |
| Decision Tree      | 0.86868 ± 0.00208  | 0.90767 ± 0.00109      |
| Random Forest      | 0.98997 ± 0.00043  | 0.95853 ± 0.00104      |
| XGBoost            | 0.99983 ± 0.00003  | 0.99607 ± 0.00033      |

✅ Final results were confirmed with a test set.

---

## Key Insights
- found that**Age** is a dominant feature (correlation ≈ +0.6), leading to nearly perfect linear separation in logistic models.
- PCA visualizations with and without **Age** showed its critical role in the data structure.
- All models performed well, with **XGBoost and Logistic Regression** achieving near-perfect results.
- No signs of data leakage found.
- Further improvements can be achieved by:
  - Balancing the dataset (e.g., SMOTE)
  - Tuning hyperparameters
  - Using more data or domain-specific features
  - Use dataset that better reflects real world cases

---

## 🚀 Check It Out ⛦

You can explore the notebook on **Kaggle** here:  
🔗 [Kaggle Notebook Link](https://www.kaggle.com/code/ellezee/stroke-risk-classification-using-machine-learning)

