# Disease-Prediction-using-Ensemble-Models

**Project Overview**

Developed an automated machine learning pipeline to classify and predict patient medical conditions (such as Pneumonia and Diabetes). The project focuses on leveraging ensemble learning strategies to mitigate the bias and variance of individual algorithms, aiming to create a stable and consensus-driven diagnostic tool.
#
**Dataset Used**

**Source:** Medical Condition Prediction Dataset sourced via the Kaggle API (marius2303/medical-condition-prediction-dataset).  
**Format:** CSV (medical_conditions_dataset.csv).  
#
**Features & Target Variable**

**Target Variable:** condition (The specific disease to be predicted).  
**Predictive Features:** A mix of 8 demographic, lifestyle, and biometric indicators.  
1. Numerical: age, bmi, blood_pressure, glucose_levels.  
2. Categorical: gender, smoking_status.
3. Identifiers: id, full_name.
#
**Technology Stack**

1. **Language:** Python 3.11.  
2. **Data Processing:** pandas, numpy.  
3. **Machine Learning:** scikit-learn (Random Forest, Gradient Boosting, Support Vector Classifier, Voting Classifier), xgboost.  
4. **Preprocessing:** SimpleImputer (handling missing data), LabelEncoder (categorical transformation).  
5. **Visualization:** matplotlib.pyplot, ConfusionMatrixDisplay.
#
**Project Workflow & Outcomes**

**Data Engineering Pipeline:** Built a robust preprocessing framework that utilized mean imputation to handle NaN values in critical biometric columns (like BMI and glucose) and applied label encoding to transform text-based categorical data into a machine-readable format.  

**Multi-Model Training Stack:** Trained a diverse array of classifiers simultaneously using an 80/20 train-test split, including a Random Forest (100 estimators), Gradient Boosting, XGBoost, and a Support Vector Machine (SVM) configured for probability outputs.  

**Hybrid Ensemble Implementation:** Integrated the individual models into a VotingClassifier utilizing a 'soft' voting strategy, allowing the system to average predicted probabilities to reach a final diagnostic consensus.  

**Evaluation & Visual Diagnostics:** Achieved peak standalone accuracies with the SVM (60.85%) and Gradient Boosting (60.55%) models. Programmatically generated a feature importance chart from the Random Forest model to isolate the most critical symptoms, and plotted confusion matrices to analyze model precision regarding false positives and negatives.
#
**Output**

<img width="567" height="496" alt="image" src="https://github.com/user-attachments/assets/7a21f695-017b-4352-9339-2d03770b2b84" />
<img width="515" height="455" alt="image" src="https://github.com/user-attachments/assets/a6c3cd6f-e9ad-426a-8d4b-739685902318" />
