# Chronic Kidney Disease (CKD) Prediction  
### Regression Analysis • Classification & Regression Trees • Random Forest • Artificial Neural Networks (ANN)
**Author:** Timothy Liu  

---

## Dataset Source

Chronic Kidney Disease (CKD) Dataset — UCI Machine Learning Repository  
🔗 https://archive.ics.uci.edu/ml/datasets/Chronic_Kidney_Disease

---

## Project Overview  
This repository contains a full end-to-end predictive analytics workflow applied to the **Chronic Kidney Disease (CKD) dataset**.  
Across three assignments, I built and compared multiple predictive modeling approaches:

1. **Linear Regression** – to understand medical risk factors affecting hemoglobin levels  
2. **Logistic Regression** – to predict CKD status  
3. **CART Classification & Regression Trees**  
4. **Random Forest (RF)**  
5. **Artificial Neural Networks (ANN)** – with 0 hidden layers & 1 hidden layer
6. **Model comparison using accuracy, sensitivity, specificity, and ROC-AUC  

This project demonstrates skills in **data preprocessing, statistical modeling, machine learning, interpretation, and model comparison**.

## Business / Healthcare Question

**Which clinical indicators best predict Chronic Kidney Disease, and how accurately can machine learning models detect CKD?**

Early identification of CKD significantly improves patient treatment outcomes.


---

## Methods & Techniques Used

### **1. Regression Analysis**
- Linear Regression (predict hemoglobin)
- Logistic Regression (predict CKD status)
- Evaluations:
  - Adjusted R²  
  - McFadden pseudo-R²  
  - ROC Curve & AUC  
- Interpretation of beta coefficients & clinical relevance  

---

### **2. Classification & Regression Trees (CART)**
- Built multiple trees with different CP and minbucket parameters  
- Pruned trees for optimal performance  
- Metrics: accuracy, sensitivity, specificity, balanced accuracy  
- Interpretable “if-else” decision paths for clinicians  

---

### **3. Random Forest**
- Tuned `mtry` using Out-Of-Bag (OOB) error  
- Accuracy ≈ **90%**  
- VarImportance plot  
- Finding: Hemoglobin + serum creatinine dominate model performance  

---

### **4. Artificial Neural Networks (ANN)**
- ANN with **0 hidden layers**  
- ANN with **1 hidden layer**  
- Scaled numerical predictors  
- Compared ANN accuracy with Random Forest  

---

## Key Insights

### **•Hemoglobin is the strongest CKD predictor**  
Lower hemoglobin levels are strongly associated with CKD due to anemia related to kidney dysfunction.

### **•Serum Creatinine is also highly predictive**  
Higher creatinine indicates reduced kidney filtration capacity.

### **•Random Forest provided the best overall classification performance**  
The ensemble model captured nonlinear clinical relationships with strong accuracy and balanced sensitivity/specificity.

### **•Logistic Regression delivered excellent interpretability and predictive power (AUC ≈ 0.98)**  
A simple but strong baseline model.

### **•Trees offer transparency**  
CART created clear rules:  
“**If hemoglobin ≥ 13 and serum creatinine < 1.3 → Not CKD**”  
perfect for medical decision-making.

---

## Skills Demonstrated

- Machine learning (RF, ANN, CART)  
- Statistical modeling (Logistic/Linear Regression)  
- Feature engineering & preprocessing  
- Tuning (cross-validation, cp, mtry, ANN structure)  
- Evaluation: accuracy, sensitivity, specificity, AUC  
- R, tidyverse, neuralnet, rpart, randomForest  
- Quarto / R Markdown reporting  
- Healthcare data interpretation

  CKD-Prediction-Models/
│
├── regression/
│   ├── Timothy_Regressions.qmd
│   └── Timothy_Regressions.pdf
│
├── trees/
│   ├── Timothy_Liu_Trees.qmd
│   └── Timothy_Liu_Trees.pdf
│
├── randomforest-ann/
│   ├── Group3_Predicting.qmd
│   └── Group3_Predicting.pdf
│
└── README.md

