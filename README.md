# tcga-cancer-gmm-clustering
Gaussian Mixture Models (GMM) and Hellinger Distance pipeline for clustering and analyzing TCGA cancer genomics (mutation and RNA expression) datasets.
# TCGA Cancer Genomics Analysis with Gaussian Mixture Models & Hellinger Distance

This bioinformatics pipeline is developed for analyzing and clustering high-dimensional cancer genomics data from the TCGA (The Cancer Genome Atlas) dataset, specifically focusing on Lung, Liver, and Prostate cancers.

##  Academic Supervision
This project was conducted under the academic supervision and guidance of [Prof. Dr. Hamza Erol](https://apbs.mersin.edu.tr/profiles_mail/herol), Head of the Computer Engineering Department at Mersin University, Turkey.

##  Features & Pipeline

1. Data Acquisition & Preprocessing: Automatic downloading and parsing of TCGA mutation (MAF) and RNA expression data into efficient sparse matrices.
2. Dimensionality Reduction: Applying `TruncatedSVD` and `PCA` to filter out noise and capture the most variance from genomic data.
3. Probabilistic Clustering: Fitting `Gaussian Mixture Models (GMM)` on the embedding space, with optimal cluster selection via Bayesian Information Criterion (BIC).
4. Statistical Distance Evaluation: Computing pairwise **Hellinger Distance** using Monte Carlo sampling to quantify the similarity between different cancer profile distributions.
5. Visualization: Generating explained variance scree plots, GMM cluster scatter plots, Hellinger distance heatmaps, and hierarchical clustering dendrograms.

##  Tech Stack & Libraries
* Python 3
* Scikit-Learn (TruncatedSVD, PCA, GMM, StandardScaler)
* SciPy (Sparse matrices, Hierarchy, Linkage)
* Pandas & NumPy
* Matplotlib & Seaborn (Data Visualization)

##  Outputs
The scripts automatically generate and save results into structured output directories:
* `gmm_summary.csv` & `hellinger_distance_matrix.csv`
* Hellinger distance heatmaps and dendrograms.
* PCA 2D projections of clustered data.
