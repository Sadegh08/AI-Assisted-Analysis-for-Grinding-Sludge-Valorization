# Briquette – AI-Assisted Analysis

[Repository overview](../README.md)

This repository section contains the Python-based analysis developed for the assessment of briquette formulations based on their mechanical properties.

The analysis evaluates similarities among briquette formulations using compression strength and durability and applies hierarchical clustering to identify groups with comparable mechanical behaviour.

## Analysis

The notebook includes:

- Evaluation of compression strength and durability
- Comparison of six briquette samples
- Z-score standardization of mechanical properties
- Hierarchical clustering using Ward linkage and Euclidean distance
- Numerical presentation of Ward linkage results
- Hierarchical clustermap and dendrogram visualization
- Comparison with the TEP industrial reference sample

## Dataset

The analysis includes six briquette samples with the following information:

- Sample ID
- Briquette type
- Additive type
- Filter pressing type
- Compression strength (MPa)
- Durability (%)

The experimental dataset is defined directly in the notebook, so no external Excel file is required to reproduce the analysis.

## Hierarchical Clustering

Hierarchical clustering is performed using two mechanical properties:

- Compression strength (MPa)
- Durability (%)

Before clustering, both variables are standardized using z-scores to prevent differences in measurement scale from dominating the analysis.

Ward linkage with Euclidean distance is then applied to the standardized dataset.

Sample 1 (TEP) is included as the industrial reference.

## Ward Linkage Results

The numerical linkage matrix is presented directly in the notebook.

For each clustering step, the output reports:

- Cluster 1
- Cluster 2
- Ward linkage distance
- Number of samples

This allows the numerical clustering results to be examined alongside the dendrogram.

## Notebook

The complete analysis is available in:

[Briquette_AI_Analysis.ipynb](Briquette_AI_Analysis.ipynb)

[Open in Google Colab](https://colab.research.google.com/github/Sadegh08/AI-Assisted-Analysis/blob/main/Briquette/Briquette_AI_Analysis.ipynb) · [Execution and reproducibility guide](../docs/REPRODUCIBILITY.md)

The notebook was developed for execution in Google Colab and uses:

- pandas
- NumPy
- Matplotlib
- Seaborn
- scikit-learn
- SciPy

## Font

Figures are formatted using Times New Roman when the font is available.

For Google Colab, a legally obtained `TimesNewRoman.ttf` file can be uploaded to:

`/content/TimesNewRoman.ttf`

If the font file is unavailable, the notebook automatically falls back to DejaVu Serif.

## Outputs

The notebook generates:

- Original briquette dataset
- Standardized mechanical-property dataset
- Ward linkage results
- Hierarchical clustering heatmap and dendrogram
- Ward linkage distance axis
- High-resolution PNG, JPG, and TIFF figures suitable for reporting

## Reproducibility

All numerical data required for the clustering analysis are defined directly in the notebook.

This allows the complete analysis and visualization workflow to be reproduced without external data files.
