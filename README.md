Audio Clustering Project: Unsupervised Sound Pattern Discovery
Overview
This project discovers hidden patterns in unlabeled audio data using machine learning. By combining feature engineering with dimensionality reduction and clustering algorithms, it identifies distinct sound categories without prior labeling.

https://via.placeholder.com/800x400?text=Audio+%E2%86%92+Mel+Features+%E2%86%92+Dimensionality+Reduction+%E2%86%92+Clustering

Key Findings
🎯 4 distinct sound clusters identified using K-Means

🔍 t-SNE visualization revealed clear separations invisible in raw data

⚖️ K-Means outperformed DBSCAN (Silhouette 0.227 vs -0.326)

🧩 Dimensionality reduction was crucial for pattern discovery

🔊 Audio features exhibit spherical cluster tendencies

Methodology
Feature Engineering Pipeline
Audio Processing: Load WAV files using Librosa

Mel Spectrogram: Convert audio to 64-band frequency representation

Feature Extraction: Calculate mean and standard deviation per band

Vector Creation: Combine into 128-dimensional feature vectors

Dimensionality Reduction
Technique	Components	Key Benefit	Limitations
PCA	3	Global variance preservation	Linear relationships only
t-SNE	3	Local neighborhood relationships	Computationally intensive
Clustering Algorithms
Algorithm	Parameters	Best For
K-Means	k=4 (elbow method)	Spherical, equally-sized clusters
DBSCAN	eps=3.5, min_samples=5	Irregular shapes, noise detection
Evaluation Metrics
Silhouette Score (-1 to 1): Measures cluster separation

Davies-Bouldin Index (lower = better): Assesses cluster compactness

Noise Point Analysis: Identifies outliers

Visual Validation: Confirms algorithmic findings

Results
Performance Comparison
Algorithm	Silhouette	DB Index	Noise Points	Clusters
K-Means	0.227	1.524	0	4
DBSCAN	-0.326	1.465	2601	33

