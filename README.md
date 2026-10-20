# Mercedes-Benz Customer Clustering — Malackathon 2026

Project repository developed by Alberto Gallego Tamayo, Javier Campos Córcoles, Jose Manuel Urbano Olmo and Hugo Enríquez Jiménez for the challenge proposed by **Mercedes-Benz** at **Malackathon 2026** (Hackathon - University of Málaga).

---

## The Challenge: Learning, Designing, and Delivering in 24 Hours

> **Context Note:**  
> This project was developed entirely during an intensive **single-day hackathon**. We arrived at the event without prior knowledge of the specific challenge presented by Mercedes-Benz and **without prior hands-on experience in clustering techniques**.  
> The true challenge was to dive in from scratch, master both the mathematical foundations and business domain, experiment across multiple algorithms, and build an end-to-end, production-grade solution against the clock in **under 24 hours**.

---

## Notebooks Structure

The repository is organized into 7 sequential workflow stages:

* **`01_Exploracion_y_Calidad_Datos.ipynb`**  
  Exploratory Data Analysis (EDA) of over 300,000 records, examining dataset architecture and dimensional footprint. Identifies and justifies missing value handling (uncovering inactive telemetry patterns) and eliminates redundant or multicollinear variables.

* **`02_Feature_Engineering.ipynb`**  
  Design of key business metrics, including true vehicle age, annualized workshop visit frequency, and campaign marketing receptivity. Implements a robust preprocessing pipeline using `RobustScaler` and ordinal encoding without inflating dimensionality.

* **`03_Clustering_KMeans_Baseline.ipynb`**  
  Baseline unsupervised modeling using K-Means across four primary target markets (AT/CH, B2B/B2C). Applies a multi-criteria heuristic to determine the optimal number of clusters (K) by evaluating Silhouette Score, Davies-Bouldin Index, Calinski-Harabasz Index, inertia elbow, and seed stability.

* **`04_Interpretacion_Segmentos.ipynb`**  
  Descriptive profiling of identified customer segments by contrasting vehicle usage behavior against demographic attributes. Translates clusters into actionable business hypotheses and marketing pilot proposals aligned with consented communication channels.

* **`05_Comparativa_Algoritmos.ipynb`**  
  Benchmarking and stability comparison against alternative algorithms, including Gaussian Mixture Models (GMM), Agglomerative Hierarchical Clustering, Sparse K-Means, and DBSCAN. Evaluates audience overlap using Jaccard index and cluster concordance via Adjusted Rand Index (ARI) and Normalized Mutual Information (NMI).

* **`06_PCA_Estructura_Visualizacion.ipynb`**  
  Dimensionality reduction via Principal Component Analysis (PCA) to evaluate explained variance ratios and dominant loadings. Projects clusters into 2D and interactive 3D spaces to assess geometric separability.

* **`07_Jackknife.ipynb`**
  Robustness validation through Jackknife resampling (iterative 15% sub-sampling exclusions) and stress testing against synthetic noise and cluster attrition. Identifies borderline and ambiguous instances to curate a refined candidate pool for commercial pilot campaigns.

---

## 🛠️ Tech Stack

* **Language:** Python 3.10+
* **Data Processing & Modeling:** `pandas`, `numpy`, `scikit-learn`, `scipy`
* **Visualization:** `matplotlib`, `seaborn`

---
