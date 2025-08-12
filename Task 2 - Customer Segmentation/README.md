# ​​ Customer Segmentation with K-Means & DBSCAN

##  Project Overview
This project performs **customer segmentation** using the *Mall Customers Dataset*, aiming to group customers based on income and spending behaviors. This allows businesses to tailor marketing strategies for each customer segment.

---

##  Dataset
**Source:** [Mall Customer Segmentation Dataset – Kaggle](https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial-in-python)  
Includes 200 customer records with features:
- `CustomerID`
- `Gender`
- `Age`
- `Annual Income (k$)` — in thousands of dollars
- `Spending Score (1–100)`

*Usage note:* In this project, we focus solely on `Annual Income (k$)` and `Spending Score (1–100)`.

---

##  Workflow

### 1. Data Exploration
- Load dataset
- Inspect data types, missing values, descriptive statistics

### 2. Preprocessing
- Copy original data
- Scale `Annual Income` and `Spending Score` using **MinMaxScaler**

### 3. Exploratory Data Analysis (EDA)
- Scatter plot of scaled features
- Histograms of feature distributions

### 4. Selecting Optimal Number of Clusters (K-Means)
- Evaluate `k` from 2 to 10 using:
  - **Elbow Method** (Inertia/WCSS)
  - **Silhouette Score**
- Visualize both to choose optimal `k`

### 5. Final K-Means Clustering
- Apply K-Means with optimal `k` (typically 5)
- Assign clusters, save labels, and inspect cluster sizes

### 6. Cluster Visualization
- Inverse transform cluster centroids to the original scale
- Plot customers and centroids in original features for intuitive interpretation

### 7. Evaluating Cluster Quality
- Print final **Silhouette Score** and **Inertia**
- Optional: compute **Davies–Bouldin** and **Calinski–Harabasz** indices for deeper evaluation

### 8. Bonus — DBSCAN Clustering
- Run DBSCAN on scaled features
- Print cluster count excluding noise
- Visualize results for comparison with K-Means

### 9. Bonus — Cluster Summaries
- Compute mean `Annual Income`, mean `Spending Score`, and counts per cluster
- Assist with business interpretation of customer segments

---

##  Results
Example outcomes:
- **Optimal Clusters (K-Means):** 5
- **Silhouette Score:** ~0.56 — indicates well-separated, compact clusters
- **Cluster Profiles:** e.g., “High Income – High Spending”, “Low Income – Low Spending”
- **DBSCAN:** May produce different structure, including noise points

---

##  Tech Stack
- Python
- pandas, numpy — data manipulation  
- matplotlib, seaborn — visualization  
- scikit-learn — clustering, scaling, evaluation metrics  

---

##  Repository Structure
