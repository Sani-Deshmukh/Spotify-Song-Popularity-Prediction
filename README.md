# CS 155 Mini Project 1: Random Forest + AdaBoost for Song Popularity

This repository contains a **Random Forest + AdaBoost** ensemble for predicting song popularity, as part of Caltech CS/CNS/EE 155. We focus on **data preprocessing, feature engineering**, and **ensemble methods** to achieve robust AUC-ROC performance.

---

## Key Details

1. **Data Preprocessing**  
   - **One-Hot Encoding** for categorical features (e.g., time signature, mode, key).  
   - **Normalization** via `StandardScaler` for numeric features (e.g., tempo, loudness).  
   - **Feature Engineering** to capture relationships (e.g., `energy * loudness`).

2. **Model Architecture**: **Random Forest with AdaBoost**  
   - **Base Estimator**: Random Forest Classifier.  
     - Tunable hyperparameters (e.g., `n_estimators`, `max_depth`, `min_samples_split`).  
   - **AdaBoost**: Improves upon the base estimator by focusing on misclassified samples from previous iterations.  
     - Key hyperparameters:
       - `n_estimators`: Total number of boosting rounds (e.g., 50, 100).  
       - `learning_rate`: Shrinks contribution of each classifier (e.g., 0.1–1.0).  
       - `random_state`: Ensures reproducibility.

3. **Evaluation & Metric**  
   - **Primary Metric**: AUC (Area Under the ROC Curve) to handle class imbalance effectively.  
   - **Cross-Validation**: 5-fold or similar for hyperparameter tuning.  
   - **Optional**: Additional metrics (e.g., precision, recall, confusion matrix) to analyze performance thoroughly.

4. **Why Random Forest + AdaBoost?**  
   - **Random Forest**: Ensemble of decision trees, reduces variance.  
   - **AdaBoost**: Sequentially re-weights samples to improve weak learners and can boost performance.  
   - **Combined**: Achieves strong performance and handles overfitting better than single classifiers.

---
#Results and Metrics 
![image](https://github.com/user-attachments/assets/1251be38-891d-464e-b63e-27cee8eeeddd)

![image](https://github.com/user-attachments/assets/8ab30acd-26bb-4041-a4dd-45697b6f1064)



