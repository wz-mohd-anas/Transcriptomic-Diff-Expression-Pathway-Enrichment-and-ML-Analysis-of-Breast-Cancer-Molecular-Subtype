# Integrated Transcriptomic, Differential Expression, Pathway Enrichment, and Machine Learning Analysis of Breast Cancer Molecular Subtypes

## Overview

This project presents a complete transcriptomic and machine learning workflow for breast cancer molecular subtype analysis using microarray gene expression data from the GEO database (GSE45827).

The workflow integrates:

- Gene expression preprocessing
- Principal Component Analysis (PCA)
- Hierarchical clustering
- Feature selection
- Machine learning classification
- Differential gene expression analysis
- Volcano plot visualization
- GO Biological Process enrichment
- KEGG pathway analysis
- STRING protein interaction network analysis

The project was primarily performed using Orange Data Mining along with external bioinformatics platforms including GEO2R, VolcaNoseR, Enrichr, and STRING.

---

# Objectives

The main objectives of this project were:

- To investigate transcriptomic variation among breast cancer molecular subtypes
- To identify subtype-associated biomarkers
- To evaluate machine learning algorithms for subtype classification
- To perform differential expression analysis between HER2-positive and normal samples
- To identify biologically enriched pathways and interaction networks

---

# Dataset Information

Dataset: GSE45827  
Source: NCBI GEO Database

The dataset contains:

- 151 biological samples
- ~54,000 gene expression features

Breast cancer molecular subtypes included:

- HER2-positive
- Basal-like
- Luminal A
- Luminal B
- Normal breast tissue
- Breast cancer cell lines

---

# Tools and Platforms Used

| Tool / Platform | Purpose |
|---|---|
| Orange Data Mining | Preprocessing, PCA, clustering, ML classification |
| GEO2R | Differential gene expression analysis |
| VolcaNoseR | Volcano plot generation |
| Enrichr | GO and KEGG enrichment analysis |
| STRING Database | Protein interaction network analysis |

---

# Workflow

## Orange Data Mining Workflow

1. File Import
2. Select Columns
3. Preprocessing and Normalization
4. PCA Analysis
5. Heatmap Visualization
6. Distance Matrix Calculation
7. Hierarchical Clustering
8. Feature Selection using Rank Widget
9. Machine Learning Classification
10. ROC Analysis
11. Performance Curve Evaluation

## External Bioinformatics Workflow

1. GEO2R Differential Expression Analysis
2. Volcano Plot Visualization
3. GO Biological Process Enrichment
4. KEGG Pathway Analysis
5. STRING Protein Interaction Analysis

---

# Machine Learning Models

The following supervised machine learning algorithms were evaluated:

- Support Vector Machine (SVM)
- Random Forest
- Logistic Regression
- k-Nearest Neighbor (kNN)

Top-ranked transcriptomic biomarkers were used as classification features.

---

# Results

## PCA Analysis

- PCA demonstrated clear subtype-specific clustering patterns.
- Normal tissue samples formed highly distinct clusters.
- Basal-like and HER2-positive tumors exhibited increased molecular heterogeneity.

## Hierarchical Clustering

- Ward linkage produced compact and biologically meaningful clusters.
- Luminal subtypes showed relatively similar transcriptomic signatures.
- Tumor samples clustered separately from normal tissues.

## Top Biomarkers Identified

- PLK1
- CDC20
- TPX2
- BUB1
- ASPM
- TTK
- KIF14
- UBE2C

These genes are primarily associated with:

- Mitotic progression
- Cell cycle regulation
- Chromosome segregation
- Tumor proliferation

---

# Machine Learning Performance

| Model | AUC | Accuracy |
|---|---|---|
| SVM | 0.990 | 92.1% |
| Logistic Regression | 0.988 | 88.1% |
| Random Forest | 0.976 | 85.4% |
| kNN | 0.965 | 74.2% |

SVM demonstrated the best overall classification performance.

---

# Differential Expression Analysis

Differential expression analysis between HER2-positive and normal breast tissue samples identified multiple significantly altered genes.

## Upregulated Genes

- SCD5
- SCARA5
- SH3GL3
- TNXB/TNXA

## Downregulated Genes

- RRM2
- UBE2C
- UBE2T
- NUSAP1

---

# GO Biological Process Enrichment

Major enriched biological processes included:

- Mitotic spindle checkpoint signaling
- Chromosome segregation
- Mitotic nuclear division
- Sister chromatid segregation

---

# KEGG Pathway Analysis

Significantly enriched pathways included:

- Cell cycle
- Oocyte meiosis
- Progesterone-mediated oocyte maturation
- Ubiquitin-mediated proteolysis
- FOXO signaling pathway

---

# STRING Network Analysis

STRING protein interaction analysis demonstrated highly interconnected proliferative and mitotic signaling networks involving:

- PLK1
- CDC20
- TPX2
- BUB1
- ASPM
- TTK
- UBE2C

These genes formed strong interaction hubs associated with tumor proliferation.

---

# Key Findings

- Breast cancer molecular subtypes possess distinct transcriptomic signatures.
- SVM achieved excellent classification performance.
- HER2-positive tumors demonstrated strong mitotic dysregulation.
- Cell cycle and mitotic checkpoint pathways were highly enriched.
- STRING analysis confirmed strong functional connectivity among identified biomarkers.

---

# Project Structure

```text
Main-Folder/
│
├── dataset/
├── docs/
├── orange_workflow/
├── results/
├── report/

© 2026 Anas. Released under the MIT License.
