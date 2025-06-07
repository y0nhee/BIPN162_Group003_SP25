# K-Nearest-Neighbors Induced Topological PCA for Single-Cell RNA-Seq Data Analysis  
**BIPN 162 Final Project - UC San Diego**  
**Authors:** Irene Eu, Dora Deng, Joshua La

## Overview
This project explores a novel dimensionality reduction technique called **K-Nearest-Neighbors Induced Topological PCA (kNN-tPCA)** for analyzing high-dimensional single-cell RNA sequencing (scRNA-seq) data. Based on the work by *Cottrell et al. (2023)*, we replicate and evaluate this method's performance in clustering and structure preservation compared to traditional methods like PCA and sPCA.

## Goals
- **Replicate** kNN-tPCA on a benchmark dataset (GSE82187)
- **Apply** the model to a new scRNA-seq dataset (GSE72056 - melanoma tumors)
- **Evaluate** clustering performance using:
  - Adjusted Rand Index (ARI)
  - Normalized Mutual Information (NMI)
  - Element-Centric Similarity (ECS)
- **Visualize** results using 2D embeddings and heatmaps

## Datasets
- **GSE82187**: Mouse brain dataset used for replication
- **GSE72056**: Human melanoma tumor dataset used for testing generalizability

## Methods
- **Preprocessing**: Log-transform, variance filtering, normalization
- **Dimensionality Reduction**:
  - `kNN-tPCA`: topological regularization using persistent Laplacians
  - `sPCA`: sparse PCA for noise reduction
  - `PCA`: standard linear dimensionality reduction
- **Clustering**: K-means (repeated 30 times)
- **Evaluation**: ARI, NMI, ECS metrics
- **Visualization**: t-SNE, UMAP, bar plots, heatmaps

## Key Findings
- **GSE82187**: Results closely matched the original paper; kNN-tPCA outperformed other models.
- **GSE72056**: Unexpectedly, **sPCA** performed best across all metrics.
- The complex and noisy nature of tumor data may hinder the performance of topological methods like kNN-tPCA.
- **Preprocessing and parameter tuning** are crucial for optimal performance.

## References
Cottrell, S., Hozumi, Y., & Wei, G. W. (2023).
"K-Nearest-Neighbors Induced Topological PCA for Single Cell RNA-Sequence Data Analysis"
arXiv:2310.14521. https://arxiv.org/abs/2310.14521

Jiang, R., Sun, T., Song, D., & Li, J. J. (2022).
"Statistics or biology: the zero-inflation controversy about scRNA-seq data"
Genome Biology, 23(31). https://doi.org/10.1186/s13059-022-02601-5

Jolliffe, I. T. (2002).
"Principal Component Analysis, Second Edition"
Springer. http://cda.psych.uiuc.edu/statistical_learning_course/Jolliffe_PCA_2ed.pdf

Lähnemann, D., et al. (2020).
"Eleven grand challenges in single-cell data science"
Genome Biology, 21(31). https://doi.org/10.1186/s13059-020-1926-6

## Acknowledgments
This project was developed as part of BIPN 162: Neural Data Science at the University of California, San Diego.

We would like to thank Dr. Mikio Aoi for his guidance, feedback, and support throughout the project.
