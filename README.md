# K-Means Clustering Implementation

This repository contains an implementation of K-Means clustering in Python, using numpy and matplotlib for computations and visualization. The implementation includes:

- Initialization of centroids
- Assignment of points to the nearest centroid
- Updating centroids based on cluster assignments
- Calculation of the Sum of Squared Errors (SSE)
- Visualization of clustering results

## Features

### Toy Problem
A synthetic dataset with three clusters is generated to test and visualize the functionality of the K-Means clustering algorithm.

- SSE is plotted across iterations to observe the convergence of the algorithm.
- Experiment with the effects of randomness by running the algorithm multiple times.
- Visualize how SSE changes with different numbers of clusters (k).

### Image Problem
Clusters images based on pre-computed HOG features and visualizes the clusters.

## Functions Overview

### Main Clustering Pipeline

1. `kMeansClustering(dataset, k, max_iters=10, min_size=0, visualize=False)`
   - Main function to perform K-Means clustering.
   - Visualizes intermediate steps if `visualize=True`.

### Helper Functions

- **Initialization**:
  - `initalizeCentroids(dataset, k)`
    - Randomly selects `k` points from the dataset as initial centroids.

- **Assignment**:
  - `computeAssignments(dataset, centroids)`
    - Assigns each point to the nearest centroid.

- **Update**:
  - `updateCentroids(dataset, centroids, assignments)`
    - Updates the centroids based on the mean of assigned points.

- **Error Calculation**:
  - `calculateSSE(dataset, centroids, assignments)`
    - Computes the Sum of Squared Errors (SSE) for the current clustering.

- **Visualization**:
  - `plotClustering(centroids, assignments, dataset, title=None)`
    - Creates a scatter plot to visualize clusters and centroids.

### Experimentation Functions

- **Toy Problem**:
  - `toyProblem()`
    - Generates a toy dataset and performs clustering experiments.

- **Image Problem**:
  - `imageProblem()`
    - Clusters images based on HOG features and visualizes cluster contents.

## How to Use

1. Clone the repository:
   ```bash
   git clone <repository-url>
   ```

2. Install dependencies:
   ```bash
   pip install numpy matplotlib
   ```

3. Run the script:
   ```bash
   python <script-name>.py
   ```

Uncomment `toyProblem()` or `imageProblem()` in the `__main__` section to run the desired experiment.

## Example Plots

- **Toy Dataset Clustering**:
  Visualizes clusters and centroids at each iteration.
- **SSE vs. Iterations**:
  Shows the convergence of SSE during clustering.
- **SSE vs. Number of Clusters (k)**:
  Observes how the error decreases as the number of clusters increases.

## Files

- `img.npy`:
  - Array containing the images to be clustered.

- `hog.npy`:
  - Pre-computed HOG features for the images.

## License
This project is licensed under the MIT License. Feel free to use, modify, and distribute this code.
