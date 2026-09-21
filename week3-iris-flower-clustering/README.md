# Week 3 – Iris Flower Clustering (K-Means)

A beginner-friendly **unsupervised learning** mini project that groups Iris flowers into
3 clusters using **K-Means**, visualizes the clusters, and compares the predicted
clusters against the true species labels.

---

## Project Structure

```
week3-iris-flower-clustering/
├── data/
│   └── iris.csv
├── iris_flower_clustering.ipynb
├── requirements.txt
└── README.md
```

---

## Dataset

**Iris Dataset** (UCI Machine Learning Repository / Kaggle) — stored in `data/iris.csv`.

- 150 rows (flowers), 50 of each species
- 4 numeric features + 1 label column

| Column | Description |
|---|---|
| `sepal_length` | Sepal length in cm |
| `sepal_width` | Sepal width in cm |
| `petal_length` | Petal length in cm |
| `petal_width` | Petal width in cm |
| `species` | True label: `setosa`, `versicolor`, `virginica` |

The `species` column is **not** given to the clustering model. It is kept aside only
to check the results at the end.

---

## Approach

1. **Load the data** from `data/iris.csv` with pandas.
2. **Explore** – shape, data types, missing values, summary statistics, class balance.
3. **Scale the features** with `StandardScaler`, so every measurement contributes
   equally to the distance calculations used by K-Means.
4. **Apply K-Means with `k = 3`** on the scaled features and obtain a cluster label
   (0, 1 or 2) for each flower.
5. **Visualize the clusters** with scatter plots:
   - Petal length vs. petal width, with the cluster centroids marked.
   - Predicted clusters and true species shown side by side.
   - A 2D **PCA** projection so all four features can be seen in one plot.
6. **Compare clusters vs. true labels** using a cross-tabulation, a
   cluster → species mapping (majority vote), and a confusion matrix.
7. **Evaluate** using the Silhouette Score and the Adjusted Rand Index.

---

## Results

**Clusters vs. true species**

| Cluster | setosa | versicolor | virginica |
|---|---|---|---|
| 0 | 0 | 39 | 14 |
| 1 | 50 | 0 | 0 |
| 2 | 0 | 11 | 36 |

**Evaluation scores**

| Metric | Score |
|---|---|
| Correctly grouped flowers | 125 / 150 |
| Match with true labels | 83.33% |
| Silhouette Score | 0.460 |
| Adjusted Rand Index | 0.620 |

**Observations**

- **Setosa** is separated perfectly — cluster 1 contains all 50 setosa flowers and
  nothing else. It is clearly apart from the other two species in every scatter plot.
- **Versicolor** and **Virginica** overlap, so 25 flowers were placed in the wrong
  cluster. This is expected: their petal and sepal measurements are genuinely similar.
- PCA with 2 components retains about **95.8%** of the information in the data,
  which makes the 2D plot a reliable summary of all four features.

**Key takeaway:** even without ever seeing the labels, K-Means recovers most of the
real structure in the Iris measurements.

---

## How to Run

1. Clone the repository and enter the project folder:

   ```bash
   git clone <your-repo-url>
   cd week3-iris-flower-clustering
   ```

2. (Optional but recommended) create a virtual environment:

   ```bash
   python -m venv venv
   source venv/bin/activate      # On Windows: venv\Scripts\activate
   ```

3. Install the dependencies:

   ```bash
   pip install -r requirements.txt
   ```

4. Launch Jupyter and open the notebook:

   ```bash
   jupyter notebook iris_flower_clustering.ipynb
   ```

5. Run all cells (**Kernel → Restart & Run All**).

> Run the notebook from the project root so that the relative path
> `data/iris.csv` resolves correctly.

---

## Requirements

- Python 3.8+
- pandas, numpy, matplotlib, seaborn, scikit-learn, notebook

All listed in `requirements.txt`.
