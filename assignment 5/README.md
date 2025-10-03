Name: Gagana S
Roll: DA25C008

# Multi-Label Gene Expression Visualization & Manifold Learning

## Overview

This project explores the structure of multi-label gene expression data using advanced dimensionality reduction and visualization techniques. The pipeline includes preprocessing, label simplification, t-SNE & Isomap embeddings, and veracity inspection to understand the challenges of classifying biological functional categories.

Key methods:
- **t-SNE** for local neighborhood preservation.
- **Isomap** for global manifold structure.
- Carefully designed color-coding to visualize the most common and most challenging multi-label categories.

## Project Structure

- **solution.ipynb**: Main code for data loading, preprocessing, label creation, scaling, t-SNE/Isomap computation, and results visualization.
- **requirements.txt**: Minimal, reproducible list of Python package dependencies.
- **README.md**: Assignment summary and instructions.

## Data

- **Dataset:** Yeast or similar gene expression ARFF file (multi-label format).  
  Place your `.arff` file in the working directory and update the filename in the script.

## Setup

1. Clone/download this repository.
2. Install dependencies (Python 3.8+ recommended):

   ```
   pip install -r requirements.txt
   ```

3. Run the notebook or script. All key results and plots will be generated inline.

## How it works

1. **Preprocessing:**  
   Loads ARFF data, separates features/labels, standardizes features, and checks for missing/invalid data.

2. **Label Selection:**  
   Reduces 14 labels to 3–4 major coloring categories for visualization:
   - Two most frequent single-function labels
   - Most common multi-label combination
   - "Other" for all remaining samples

3. **Visualization:**  
   - t-SNE: Plots low-dimensional embeddings at different perplexities to explore local structure.
   - Isomap: Plots embeddings preserving the global manifold.
   - Both use the same color coding for direct comparison.

4. **Veracity Inspection:**  
   - Identifies noisy, ambiguous, outlier, and hard-to-learn samples directly from the plots.
   - Discusses how manifold complexity impedes simple classification.

## Dependencies

```
liac-arff
pandas
numpy
matplotlib
scikit-learn
```
See `requirements.txt` for exact names and installation.

## Results

- Plots showing how biological labels overlap and complicate classification.
- Analysis of data manifold structure and challenges posed for machine learning.



**To reproduce all results, run the notebook from start to finish, ensuring your ARFF file is in the working directory.**
