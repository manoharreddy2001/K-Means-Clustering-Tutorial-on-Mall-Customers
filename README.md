# K-Means Clustering for Mall Customers Segmentation

This repository demonstrates a complete workflow for customer segmentation using **K-Means Clustering** on the Mall Customers dataset downloaded from Kaggle. It covers data loading from a CSV file, data preprocessing, determining the optimal number of clusters using the Elbow Method and Silhouette Analysis, performing K-Means clustering, and multiple visualization techniques to interpret and communicate the segmentation results, ensuring both clarity and reproducibility.

---

## Table of Contents

1. [Project Overview](#project-overview)  
2. [Features & Visualizations](#features--visualizations)  
3. [Prerequisites & Installation](#prerequisites--installation)  
4. [Usage](#usage)  
5. [Repository Structure](#repository-structure)  
6. [Detailed Explanation](#detailed-explanation)  
7. [Results](#results)  
8. [Accessibility](#accessibility)  
9. [License](#license)  
10. [Clone the Repository](#clone-the-repository)

---

## Project Overview

The **Mall Customers** dataset is a widely used benchmark for customer segmentation. It contains demographic data and spending behavior information for customers visiting a mall. This project applies **K-Means Clustering** to segment customers based on key features: **Age**, **Annual Income (k$)**, and **Spending Score (1-100)**. By following the code and instructions provided, you will learn how to:

- Load and preprocess a real-world dataset.
- Determine the optimal number of clusters using both the Elbow Method and Silhouette Analysis.
- Apply K-Means Clustering to segment customers.
- Visualize the results using both 2D and 3D plots.
- Interpret the clusters to derive actionable business insights.

---

## Features & Visualizations

1. **Data Preprocessing**  
   - Loads the Mall Customers CSV file from Kaggle.
   - Extracts key features and standardizes them using StandardScaler.

2. **Optimal Cluster Determination**  
   - Uses the **Elbow Method** to plot inertia values against different numbers of clusters.
   - Employs **Silhouette Analysis** to evaluate cluster quality and assist in choosing the optimal \(k\).

3. **K-Means Clustering**  
   - Performs clustering on the standardized data with the selected number of clusters.
   - Outputs cluster labels and centroids.

4. **Rich Visualizations**  
   - **Elbow Plot:** Displays the relationship between the number of clusters and inertia.
   - **Silhouette Plot:** Illustrates the silhouette coefficients for each sample to assess cluster quality.
   - **2D PCA Scatter Plot:** Reduces the data to two dimensions and visualizes clusters with centroids.
   - **3D Scatter Plot:** Plots clusters in the original feature space for an intuitive view of segmentation.

---

## Prerequisites & Installation

- **Python 3.7+**
- [NumPy](https://numpy.org/)
- [pandas](https://pandas.pydata.org/)
- [matplotlib](https://matplotlib.org/)
- [seaborn](https://seaborn.pydata.org/)
- [scikit-learn](https://scikit-learn.org/stable/)

## Detailed Explanation

### Data Loading
We load the Mall Customers dataset using `pandas.read_csv()` and extract the relevant features: **Age**, **Annual Income (k$)**, and **Spending Score (1-100)**.

### Preprocessing
- **StandardScaler** normalizes all features to zero mean and unit variance.
- This ensures that differences in feature scales do not bias the clustering algorithm.

### Optimal Cluster Determination

#### Elbow Method
We compute the inertia for a range of cluster values (e.g., 2 to 10) and plot these values to identify the "elbow" where increasing the number of clusters yields diminishing returns.

#### Silhouette Analysis
For a chosen number of clusters, we calculate the silhouette coefficient for each sample and the average silhouette score, which helps assess the quality of clustering. A higher average silhouette score indicates better-defined clusters.

### K-Means Clustering
We perform K-Means clustering on the standardized data with the optimal number of clusters (e.g., 5).
- The algorithm assigns each sample to a cluster and computes the cluster centroids in standardized space.
- These centroids can be inverse-transformed to interpret the typical characteristics of each cluster in the original scale.

### Visualization

#### Elbow Plot
Visualizes the relationship between the number of clusters and inertia, aiding in the selection of \( k \).

#### Silhouette Plot
Shows the distribution of silhouette scores for each sample, highlighting the cohesion and separation of clusters.

#### 2D PCA Scatter Plot
Reduces the high-dimensional standardized data to two principal components and visualizes the clusters along with the centroids.

#### 3D Scatter Plot
Provides a comprehensive view of the clustering in the original feature space (**Age**, **Annual Income (k$)**, **Spending Score (1-100)**).

### Results

#### Cluster Centroids
The centroids reveal the typical characteristics of each customer segment. For example, one cluster might represent younger customers with moderate income and high spending scores.

#### Cluster Quality
The Elbow and Silhouette plots suggest that the chosen number of clusters (e.g., 5) provides a good balance between compactness and separation.

#### Visual Interpretations
- **2D PCA Plot:** Demonstrates clear cluster groupings with visible centroids.
- **3D Scatter Plot:** Offers an intuitive view of the segmentation in the context of **Age**, **Annual Income (k$)**, and **Spending Score (1-100)**.

### Accessibility

#### Color Schemes
We use colorblind-friendly palettes (e.g., Accent, Set2) and large font sizes in our visualizations.

#### Clear Labeling
All plots include descriptive titles, axis labels, and legends for easy interpretation.

#### Screen Reader Compatibility
Textual descriptions and alt-text for figures (if provided) ensure accessibility for users with screen readers.

#### Transcripts/Closed Captions
(Recommended if video or audio content accompanies the tutorial.)

### License
This project is distributed under the **MIT License**. You are free to use, modify, and distribute this code for personal or commercial purposes, provided you include the original license text.

### Clone the Repository

```bash
git clone https://github.com/manoharreddy2001/MallCustomersKMeans.git
