# Maternal Health Risk Prediction using Machine Learning

This project applies machine learning techniques to predict maternal health risk levels (High, Mid, Low) using physiological indicators. The goal is to assist in early detection of high-risk pregnancies, which can help improve maternal and neonatal health outcomes.

> Developed as part of CS550 coursework at San Francisco Bay University.

---

## Objectives
- Classify maternal health risk levels into **High, Mid, and Low** categories  
- Explore dataset distributions and feature correlations  
- Train and compare multiple machine learning models  
- Apply hyperparameter tuning to improve accuracy  
- Identify influential health indicators for interpretability  

---

## Dataset
- **Source:** UCI Machine Learning Repository  
- **Size:** 1,014 records  
- **Shape:** (1014, 7)  
- **Target variable:** `RiskLevel` (High, Mid, Low)  
- **Features:**  
  - `Age` – Age of the pregnant woman (years)  
  - `SystolicBP` – Upper blood pressure (mmHg)  
  - `DiastolicBP` – Lower blood pressure (mmHg)  
  - `BS` – Blood sugar level (mmol/L)  
  - `BodyTemp` – Body temperature (°C)  
  - `HeartRate` – Heart rate (beats/min)  

> Dataset contained **no missing values**.

---

## Workflow
1. **Data Collection** – Obtained dataset from UCI ML Repository  
2. **Data Preprocessing** – Outlier handling, label encoding, feature scaling  
3. **Exploratory Data Analysis (EDA)** – Feature distributions, correlation heatmap, risk-level analysis  
4. **Model Training** – Trained Decision Tree, KNN, SVM, Random Forest, XGBoost  
5. **Hyperparameter Tuning** – Applied GridSearchCV on Random Forest and XGBoost  
6. **Evaluation** – Accuracy scores, classification reports, confusion matrices, feature importance  

---

## Methods & Tools
- **Python Libraries:** pandas, numpy, matplotlib, seaborn, scikit-learn, xgboost  
- **Models:** Decision Tree, KNN, SVM, Random Forest, XGBoost  
- **Evaluation Metrics:** Accuracy, classification report, confusion matrix, feature importance  
- **Optimization:** GridSearchCV (cross-validation)  

---

## Key Findings
- Majority of women in the dataset were between **20–40 years**, with most pregnancies classified as **Low Risk**.  
- Strong correlation observed between **SystolicBP and DiastolicBP (0.79)**.  
- Higher **age (26–48)** and elevated **heart rate** were linked with higher risk.  
- Removing **DiastolicBP** reduced model performance, highlighting its importance.  

---

## Model Performance
| Model           | Accuracy (Initial) | Accuracy (Tuned) |
|-----------------|---------------------|------------------|
| Random Forest   | 0.8274              | 0.8286           |
| XGBoost         | 0.8249              | **0.8311**       |
| Decision Tree   | 0.8151              | -                |
| KNN             | Moderate            | -                |
| SVM             | Moderate            | -                |

- **XGBoost (tuned)** achieved the highest accuracy (83.11%).  
- Random Forest followed closely with 82.86%.  
- Decision Tree was competitive but less stable due to higher variance.  

---

## Repository Contents
- `CS550_Midterm_tanha_Notebook.ipynb` → Full notebook (EDA, preprocessing, model training, evaluation)  
- `CS550_Midterm_tanha_PPT.pdf` → Final presentation slides  
- `Maternal Health Risk Data Set.csv` → Dataset used for training and evaluation
- `CS550_Midterm_tanha_video` → Video description of the project

---

