# Hydrometallurgy – AI-Assisted Analysis

[Repository overview](../README.md)

This repository section contains the Python-based analysis developed for the hydrometallurgical assessment of recovered iron chloride products.

The analysis evaluates impurity levels, product quality classification, quality ranking, and similarities among recovered products and a commercial FeCl3 reference.

## Analysis

The notebook includes:

- Evaluation of Cr, Ni, and Mn impurity concentrations
- Product classification according to EN 888:2023 impurity limits
- Impurity-based quality scoring of recovered products
- Quality ranking and visualization
- Z-score standardization of impurity data
- Hierarchical clustering using Ward linkage
- Comparison with commercial FeCl3 as a reference product

## Quality Classification

Product quality is classified using Cr, Ni, and Mn impurity concentrations.

The final quality class corresponds to the most restrictive classification obtained among the three impurities.

## Quality Score

Recovered products are compared using an impurity-based quality score.

The weighting used in the analysis is:

- Cr: 45%
- Ni: 30%
- Mn: 25%

Lower impurity concentrations result in higher normalized scores.

The ranking is presented both as a table and as a horizontal bar chart.

## Hierarchical Clustering

Hierarchical clustering is performed using Cr, Ni, and Mn concentrations.

Before clustering, the variables are standardized using z-scores to account for differences in scale.

Ward linkage with Euclidean distance is then applied to the standardized data.

The commercial FeCl3 sample is included as a benchmark, while the SKF A2 leachate is excluded from the clustering because it represents a process stream rather than a final recovered product.

## Notebook

The complete analysis is available in:

[Hydrometallurgy_AI_Analysis.ipynb](Hydrometallurgy_AI_Analysis.ipynb)

[Open in Google Colab](https://colab.research.google.com/github/Sadegh08/AI-Assisted-Analysis-for-Grinding-Sludge-Valorization/blob/main/Hydrometallurgy/Hydrometallurgy_AI_Analysis.ipynb) · [Execution and reproducibility guide](../docs/REPRODUCIBILITY.md)

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

- EN 888:2023 quality classification table
- Recovered-product quality ranking
- Quality-ranking bar chart
- Standardized impurity dataset
- Ward hierarchical clustering heatmap and dendrogram
- High-resolution figures suitable for reporting

## Reproducibility

All numerical data used for this analysis are defined directly in the notebook, allowing the analysis and figures to be reproduced without external data files.
