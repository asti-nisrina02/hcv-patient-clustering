# HCV Patient Clustering with K-Means

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/asti-nisrina02/hcv-patient-clustering/blob/main/hcv_patient_clustering_kmeans.ipynb)

Unsupervised machine learning project that groups patients using only routine blood-test values, then checks how well the groups match the real diagnosis categories.

## Project overview

- **Question:** can lab values alone separate patients into meaningful clusters?
- **Data:** [HCV data, UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/571/hcv+data): 615 patients, age, sex, 10 blood-test values and a diagnosis category.
- **Approach:** data cleaning, feature scaling, K-means with K = 2 to 8, model selection with elbow method, silhouette score and cosine-similarity measures, PCA visualisation, cluster profiling, and comparison with the true diagnosis (adjusted Rand index).

## Key findings

> Fill this in after running the notebook. Keep it to 3-4 bullets with real numbers, for example:
> - Selected K = **_** based on ...
> - Cluster 0 is characterised by high ... and low ...
> - Adjusted Rand index vs. diagnosis: **_**, meaning ...

## Methods and tools

Python, pandas, NumPy, scikit-learn (K-means, PCA, silhouette score), SciPy, matplotlib.

## Repository structure

```
hcv-patient-clustering/
├── hcv_patient_clustering_kmeans.ipynb   # full analysis
├── data/
│   └── hcv_dataset.csv                   # download from the UCI link above
├── requirements.txt
└── README.md
```

## How to run

1. Clone the repository and install the requirements:
   ```bash
   pip install -r requirements.txt
   ```
2. Download the dataset from UCI and save it as `data/hcv_dataset.csv`.
3. Open the notebook in Jupyter or click the Colab badge above, and run all cells.

## Limitations

- Small and imbalanced dataset (most patients are healthy blood donors).
- K-means assumes roughly round, similarly sized clusters.
- Exploratory analysis only, not a diagnostic tool.

## Background

Originally built as a university data mining course assignment, then reworked for this portfolio: removed a row-index feature that leaked label information, added model selection across several values of K, visualisations, cluster profiles and a comparison with the real diagnosis categories.
