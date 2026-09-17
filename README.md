# 🛒 SmartCart — AI/ML Customer Segmentation

An unsupervised Machine Learning project designed to segment e-commerce customers into distinct behavioral groups. By analyzing spending habits, income, and purchase frequency, this project helps marketing teams design targeted campaigns and personalized recommendations.

---

## 📌 Problem Statement
E-commerce platforms have diverse customer bases. Applying a "one-size-fits-all" marketing strategy is inefficient. SmartCart uses AI clustering algorithms to discover hidden customer personas from raw purchasing data.

---

## 🤖 ML Models & Algorithms Used

Since this is an **unsupervised learning** task, we do not use Accuracy or F1-Score. Instead, we use clustering evaluation metrics.

### 1. Principal Component Analysis (PCA)
- Used for **Dimensionality Reduction**.
- Condensed multiple behavioral features into 3 principal components to allow for 3D visualization and faster clustering.

### 2. K-Means Clustering
- Evaluated optimal clusters ($K$) using the **Elbow Method (WCSS)** and **Silhouette Score**.
- Selected $K=4$ based on optimal silhouette scores.

### 3. Agglomerative Hierarchical Clustering
- Used **Ward's Linkage** to minimize variance within clusters.
- Final model grouped customers into **4 distinct clusters**.

---

## 📊 Cluster Analysis Results (Agglomerative)

| Cluster | Avg. Income | Avg. Web Purchases | Avg. Store Purchases | Profile Summary |
|:---:|:---:|:---:|:---:|---|
| **0** | $39,680 | 3.15 | (Low) | Lower income, moderate web shoppers |
| **1** | $72,808 | 5.68 | (High) | High income, highly active premium buyers |
| **2** | $36,960 | 2.71 | (Low) | Lowest income, budget-conscious |
| **3** | $70,722 | 5.79 | (High) | High income, frequent web shoppers |

---

## 🛠️ Tech Stack & Workflow
- **Libraries**: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`
- **Preprocessing**: Missing value handling, scaling.
- **Dimensionality Reduction**: `sklearn.decomposition.PCA`
- **Clustering**: `KMeans`, `AgglomerativeClustering`
- **Evaluation**: `silhouette_score`

---

## 🚀 How to Run
```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
jupyter notebook "smartcart.ipynb"
```
