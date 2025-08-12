# 🛍️ Customer Segmentation with K-Means & DBSCAN

## 📌 Project Overview
This project performs **customer segmentation** using the *Mall Customers Dataset*, aiming to group customers based on **income** and **spending behaviors**.  
Such segmentation enables businesses to **tailor marketing strategies** for each customer group — from luxury lovers to budget-conscious shoppers.

---

## 📂 Dataset
**Source:** [Mall Customer Segmentation Dataset – Kaggle](https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial-in-python)  

📏 **Size:** 200 customer records  
📋 **Features:**
- 🆔 `CustomerID`
- 🚻 `Gender`
- 🎂 `Age`
- 💰 `Annual Income (k$)` — in thousands of dollars
- 🛒 `Spending Score (1–100)`

💡 *In this project, we focus solely on:*  
`Annual Income (k$)` & `Spending Score (1–100)`

---

## 🔄 Workflow

### 1️⃣ Data Exploration
- 📥 Load dataset
- 🔍 Inspect data types, missing values, descriptive statistics

### 2️⃣ Preprocessing
- 📄 Copy original data
- 📏 Scale `Annual Income` & `Spending Score` using **MinMaxScaler**

### 3️⃣ Exploratory Data Analysis (EDA)
- 📊 Scatter plot of scaled features
- 📈 Histograms of feature distributions

### 4️⃣ Selecting Optimal Number of Clusters (K-Means)
- Evaluate `k` from 2 to 10 using:
  - 📉 **Elbow Method** (Inertia/WCSS)
  - 🪞 **Silhouette Score**
- 📌 Visualize both to choose optimal `k`

### 5️⃣ Final K-Means Clustering
- 🤖 Apply K-Means with optimal `k` (typically 5)
- 🏷 Assign clusters, save labels, and inspect cluster sizes

### 6️⃣ Cluster Visualization
- 🔄 Inverse transform cluster centroids to original scale
- 🎯 Plot customers & centroids for intuitive interpretation

### 7️⃣ Evaluating Cluster Quality
- 🧮 Print final **Silhouette Score** & **Inertia**
- 📊 *(Optional)*: Compute **Davies–Bouldin** & **Calinski–Harabasz** indices

### 8️⃣ Bonus — DBSCAN Clustering
- 🌐 Run DBSCAN on scaled features
- 🗂 Print cluster count (excluding noise)
- 🖼 Visualize results for comparison with K-Means

### 9️⃣ Bonus — Cluster Summaries
- 📏 Compute mean `Annual Income`, mean `Spending Score`, & counts per cluster
- 💡 Assist with business interpretation of customer segments

---

## 🏆 Results
Example findings:
- **Optimal Clusters (K-Means):** `5`
- **Silhouette Score:** `~0.56` → well-separated, compact clusters
- **Cluster Profiles:**
  - 💎 *High Income – High Spending*
  - 🛍 *Medium Income – High Spending*
  - 🐢 *Low Income – Low Spending*
- **DBSCAN:** May produce fewer clusters + noise points

---

## 🛠 Tech Stack
- 🐍 Python  
- 📊 pandas, numpy — data manipulation  
- 🎨 matplotlib, seaborn — visualization  
- 🤖 scikit-learn — clustering, scaling, evaluation metrics  

---

## 📁 Repository Structure
