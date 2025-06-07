# BIPN162_Group003_SP25
UC San Diego – BIPN 162 Final Project
Authors: Irene Eu, Dora Deng, Joshua La

Overview
This project investigates a novel dimensionality reduction technique, K-Nearest-Neighbors Induced Topological PCA (kNN-tPCA), for analyzing high-dimensional single-cell RNA sequencing (scRNA-seq) data. Based on the method proposed by Cottrell et al. (2023), we evaluate the model’s performance in capturing complex gene expression structures across diverse cell types, comparing it to traditional approaches like PCA and sPCA.

Goals
Replicate the original paper’s pipeline on a benchmark dataset (GSE82187)

Apply kNN-tPCA to a new dataset (GSE72056 - human melanoma tumor cells)

Evaluate the dimensionality reduction and clustering performance using:

Adjusted Rand Index (ARI)

Normalized Mutual Information (NMI)

Element-Centric Similarity (ECS)

Visualize the results using 2D projections, heatmaps, and cluster comparison plots

Datasets
GSE82187: Mouse brain scRNA-seq dataset used to replicate the original study.

GSE72056: Human melanoma scRNA-seq dataset used to test model generalizability.

Methods
Data preprocessing: normalization, log-transform, gene variance filtering

Dimensionality reduction:

kNN-tPCA (Topological PCA + persistent Laplacians)

Sparse PCA (sPCA)

Principal Component Analysis (PCA)

Clustering: K-means (repeated 30 times for consistency)

Evaluation: ARI, NMI, ECS

Visualization: t-SNE, UMAP, heatmaps, and bar plots

Key Findings
kNN-tPCA successfully reproduced results from the original study on GSE82187.

On the new GSE72056 dataset, sPCA outperformed kNN-tPCA across all metrics.

The biological complexity and heterogeneity in the tumor dataset may challenge topological methods that assume cleaner neighbor structures.

Preprocessing decisions (e.g., parameter tuning, rare cell filtering) heavily impact performance.
