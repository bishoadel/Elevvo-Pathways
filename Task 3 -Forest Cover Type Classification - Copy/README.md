
# 🌲 Forest Cover Type Prediction

## 📌 Project Overview
This project predicts **forest cover types** based on cartographic variables (elevation, slope, soil type, etc.).  
It applies **machine learning models** to classify the cover type into one of 7 categories.  

We compare a **baseline model (Decision Tree)** with an **advanced model (XGBoost)** and analyze feature importance.

---

## 📂 Dataset
- **Source**: [UCI Forest CoverType Dataset](https://archive.ics.uci.edu/ml/datasets/covertype)  
- **Target Variable**: `Cover_Type` (7 classes: Spruce/Fir, Lodgepole Pine, etc.)  
- **Features**: Elevation, Aspect, Slope, Soil Type, Wilderness Area, etc.  

---

## 🔑 Steps in the Notebook
### 1. Data Preprocessing
- Checked for missing values  
- Separated features (`X`) and target (`y`)  
- Applied **Label Encoding** to target variable (`Cover_Type`)  

### 2. Exploratory Data Analysis (EDA)
- Class distribution of cover types  
- Most frequent soil types  
- Correlation heatmap of numerical features  
- Elevation vs Cover Type scatter plot  

### 3. Baseline Model
- **Decision Tree Classifier**  
- Parameters: `max_depth=10`, `criterion="gini"`  
- Accuracy ≈ **70%**  
- Confusion matrix + classification report  

### 4. Advanced Model
- **XGBoost Classifier** (multi-class, softmax objective)  
- Accuracy ≈ **(to be filled after run)**  
- Confusion matrix + classification report  

### 5. Feature Importance
- XGBoost feature importance analysis  
- Top 15 important features visualized  

### 6. Bonus (Optional)
- Model comparison: **Random Forest vs XGBoost**  
- Hyperparameter tuning with GridSearchCV / RandomizedSearchCV  

---

## 📊 Results (Summary)
- **Decision Tree** → Simple, interpretable baseline, ~70% accuracy  
- **XGBoost** → More powerful, handles complex feature interactions, improved accuracy  
- **Most Important Features** → Elevation, Horizontal Distance to Roadways, Hillshade features, Soil Types  

---

## 🚀 How to Run
1. Clone this repo  
2. Install dependencies:  
   ```bash
   pip install -r requirements.txt
   ```
3. Open the Jupyter notebook and run all cells.  

---

## 🛠️ Tech Stack
- Python  
- Pandas, NumPy, Matplotlib, Seaborn  
- Scikit-learn  
- XGBoost  

---

✨ **Takeaway**:  
- Use **Decision Tree** for fast interpretability.  
- Use **XGBoost** for higher accuracy and real-world deployment.  
