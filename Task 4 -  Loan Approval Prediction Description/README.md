# 🏦 Loan Approval Prediction

## 📌 Project Overview
This project builds a **Machine Learning pipeline** to predict whether a loan application will be **approved** or **not approved**.  
It demonstrates handling of:
- **Missing values**
- **Categorical encoding**
- **Feature scaling**
- **Imbalanced data (SMOTE)**
- **Binary classification models**

---

## 📂 Dataset
- **Source:** [Loan Approval Prediction Dataset on Kaggle](https://www.kaggle.com/datasets/architsharma01/loan-approval-prediction-dataset)  
- **Target Column:** `Loan_Status` (Approved / Not Approved)

---

## ⚙️ Workflow

### **1. Import Libraries**
- Python (NumPy, Pandas, Matplotlib, Seaborn)  
- Scikit-learn (preprocessing, models, evaluation)  
- imbalanced-learn (SMOTE for oversampling)

---

### **2. Data Exploration**
- Load dataset (`loan_approval_dataset.csv`).  
- Checked structure, data types, and missing values.  
- Analyzed target distribution (`Loan_Status`).  

---

### **3. Data Preprocessing**
- **Label Encoding** for categorical features.  
- **StandardScaler** for numerical features.  
- Splitting features (`X`) and target (`y`).  
- Train-Test split (80/20, stratified).  

---

### **4. Handling Imbalance**
- **Class distribution check** revealed imbalance.  
- Applied **SMOTE** (Synthetic Minority Oversampling Technique) to balance training data.  

---

### **5. Model Selection**
Two classification models were trained and compared:
1. **Logistic Regression** (baseline, interpretable)  
2. **Decision Tree Classifier** (rule-based, handles non-linear patterns)  

---

### **6. Evaluation**
- Metrics used: **Accuracy, Precision, Recall, F1-Score**  
- Visualized **Confusion Matrices** for both models.  

---

## 📊 Results
| Model               | Accuracy | Precision | Recall | F1-Score |
|---------------------|----------|-----------|--------|----------|
| Logistic Regression  | 93.21%   | 0.91      | 0.91   | 0.91     |
| Decision Tree        | 97.66%   | 0.97      | 0.96   | 0.97     |

---

## 🚀 Key Takeaways
- **SMOTE** helps balance imbalanced datasets and improves recall for minority class.  
- **Logistic Regression** is simple and interpretable, making it a strong baseline.  
- **Decision Trees** handle complex patterns but may overfit without tuning.  
- For production, tuning hyperparameters (GridSearchCV/RandomizedSearchCV) could further boost performance.  

---

## 🛠️ Tools & Libraries
- Python  
- Pandas, NumPy  
- Scikit-learn  
- Seaborn, Matplotlib  
- imbalanced-learn (SMOTE)  
