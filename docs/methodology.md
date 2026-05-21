# Methodology

## Overview

This project implemented an integrated transcriptomic and machine learning workflow for breast cancer molecular subtype analysis using the GSE45827 microarray gene expression dataset.

The workflow combined:

- transcriptomic preprocessing
- dimensionality reduction
- clustering analysis
- feature selection
- machine learning classification
- differential expression analysis
- pathway enrichment analysis
- protein interaction network analysis

---

# Dataset Acquisition

The breast cancer gene expression dataset GSE45827 was obtained from the NCBI Gene Expression Omnibus (GEO) database.

Dataset characteristics:

- 151 biological samples
- ~54,000 transcriptomic features
- multiple breast cancer molecular subtypes

Subtypes included:

- HER2-positive
- Basal-like
- Luminal A
- Luminal B
- Normal breast tissue
- Breast cancer cell lines

---

# Orange Data Mining Workflow

The primary transcriptomic analysis workflow was implemented using Orange Data Mining with the Orange3-Bioinformatics add-on.

## Workflow Components

1. File Import
2. Select Columns
3. Preprocess
4. PCA
5. Heatmap
6. Distances
7. Hierarchical Clustering
8. Rank Widget
9. Machine Learning Models
10. Test & Score
11. ROC Analysis
12. Performance Curve

---

# Preprocessing

Preprocessing and normalization were performed using the Preprocess widget to reduce transcriptomic variability and stabilize expression distributions across samples.

Normalization improved downstream:

- PCA visualization
- clustering quality
- machine learning performance

---

# PCA Analysis

Principal Component Analysis (PCA) was used for dimensionality reduction and visualization of subtype-associated transcriptomic variation.

The first two principal components explained approximately 21% of the total variance.

---

# Clustering Analysis

Hierarchical clustering was performed using:

- Euclidean distance
- Ward linkage

Ward linkage produced compact and biologically meaningful subtype clusters.

---

# Feature Selection

The Rank widget was used to identify subtype-associated transcriptomic biomarkers using:

- Information Gain
- Gain Ratio
- ANOVA
- Gini Decrease

Top-ranked genes included:

- PLK1
- TPX2
- CDC20
- BUB1
- ASPM
- KIF14
- TTK

---

# Machine Learning Classification

The following supervised machine learning algorithms were evaluated:

- Support Vector Machine (SVM)
- Random Forest
- Logistic Regression
- k-Nearest Neighbor (kNN)

The top-ranked genes were used as classification features.

SVM demonstrated the highest classification performance.

---

# Differential Expression Analysis

Differential gene expression analysis was performed externally using GEO2R.

Comparison:
- HER2-positive vs Normal breast tissue

Volcano plot visualization was performed using VolcaNoseR.

---

# GO and KEGG Enrichment Analysis

Functional enrichment analysis was performed using Enrichr.

Analyses included:

- GO Biological Process enrichment
- KEGG pathway enrichment

The results demonstrated enrichment of:

- mitotic checkpoint signaling
- chromosome segregation
- cell cycle pathways

---

# STRING Network Analysis

Protein–protein interaction analysis was performed using the STRING database.

The identified biomarkers formed highly interconnected proliferative and mitotic signaling networks.