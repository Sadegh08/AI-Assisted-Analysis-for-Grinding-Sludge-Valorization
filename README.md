# AI-Assisted Analysis for Grinding Sludge Valorization

Data analysis, optimization, machine-learning modeling, and visualization for experimental materials research.

This repository brings together Jupyter notebooks and method-specific documentation for four research areas: hydrometallurgy, briquettes, bituminous mastics, and cement mortar. The mortar work includes both mechanical-property prediction and gauge-factor analysis.

## Research areas

| Research area | Analysis focus | Methods |
| --- | --- | --- |
| [Hydrometallurgy](Hydrometallurgy/README.md) | Cr, Ni, and Mn impurities in recovered iron chloride products and reference samples | Impurity classification, weighted quality scoring, and hierarchical clustering |
| [Briquette](Briquette/README.md) | Compression strength and durability of briquette formulations | Standardization, Ward linkage, and comparison with the TEP industrial reference |
| [Bituminous mastic](Bituminous_Mastic/README.md) | Aging Index as a function of filler type, filler-to-bitumen mass ratio, and angular frequency | GA, PSO, ANN, GPR, SVR, and SHAP |
| [Mortar: mechanical properties](Mortar%28Cement%29/README.md#mechanical-properties) | Maximum flexural stress and mean compressive strength | GA, PSO, ANN, GPR, SVR, and SHAP |
| [Mortar: gauge factor](Mortar%28Cement%29/Gauge_Factor/README.md) | Average final gauge factor, GFend | PCHIP and Akima interpolation, ANN, GPR, SVR, and SHAP |

Each section describes its own inputs, validation procedure, and outputs. Refer to those descriptions when interpreting or comparing results.

## Getting started

1. Choose a notebook from the index below and open it in Google Colab.
2. Follow the [execution and reproducibility guide](docs/REPRODUCIBILITY.md) to prepare the runtime and input files.
3. Run the notebook cells in order, then download the generated results.

The notebooks use Colab-style paths, including `/content`. The guide explains where to place the Excel files and how to transfer the trained GPR model needed for the bituminous-mastic SHAP analysis.

## Notebook index

The analysis links open the source notebooks on GitHub; the Colab links open the corresponding execution environment.

| Research area | Notebook | Run |
| --- | --- | --- |
| Hydrometallurgy | [Clustering and quality assessment](Hydrometallurgy/Hydrometallurgy_AI_Analysis.ipynb) | [Open in Colab](https://colab.research.google.com/github/Sadegh08/AI-Assisted-Analysis/blob/main/Hydrometallurgy/Hydrometallurgy_AI_Analysis.ipynb) |
| Briquette | [Mechanical-property clustering](Briquette/Briquette_AI_Analysis.ipynb) | [Open in Colab](https://colab.research.google.com/github/Sadegh08/AI-Assisted-Analysis/blob/main/Briquette/Briquette_AI_Analysis.ipynb) |
| Bituminous mastic | [GA / PSO](Bituminous_Mastic/GA_PSO/GA_and_PSO.ipynb) | [Open in Colab](https://colab.research.google.com/github/Sadegh08/AI-Assisted-Analysis/blob/main/Bituminous_Mastic/GA_PSO/GA_and_PSO.ipynb) |
| Bituminous mastic | [ANN](Bituminous_Mastic/ANN/ANN.ipynb) | [Open in Colab](https://colab.research.google.com/github/Sadegh08/AI-Assisted-Analysis/blob/main/Bituminous_Mastic/ANN/ANN.ipynb) |
| Bituminous mastic | [GPR](Bituminous_Mastic/GPR/GPR.ipynb) | [Open in Colab](https://colab.research.google.com/github/Sadegh08/AI-Assisted-Analysis/blob/main/Bituminous_Mastic/GPR/GPR.ipynb) |
| Bituminous mastic | [SVR](Bituminous_Mastic/SVR/SVR.ipynb) | [Open in Colab](https://colab.research.google.com/github/Sadegh08/AI-Assisted-Analysis/blob/main/Bituminous_Mastic/SVR/SVR.ipynb) |
| Bituminous mastic | [SHAP interpretation](Bituminous_Mastic/SHAP/SHAP.ipynb) | [Open in Colab](https://colab.research.google.com/github/Sadegh08/AI-Assisted-Analysis/blob/main/Bituminous_Mastic/SHAP/SHAP.ipynb) |
| Mortar: mechanical properties | [GA / PSO](Mortar%28Cement%29/Mechanical_Properties/GA_PSO/GA_and_PSO.ipynb) | [Open in Colab](https://colab.research.google.com/github/Sadegh08/AI-Assisted-Analysis/blob/main/Mortar%28Cement%29/Mechanical_Properties/GA_PSO/GA_and_PSO.ipynb) |
| Mortar: mechanical properties | [ANN](Mortar%28Cement%29/Mechanical_Properties/ANN/ANN.ipynb) | [Open in Colab](https://colab.research.google.com/github/Sadegh08/AI-Assisted-Analysis/blob/main/Mortar%28Cement%29/Mechanical_Properties/ANN/ANN.ipynb) |
| Mortar: mechanical properties | [GPR](Mortar%28Cement%29/Mechanical_Properties/GPR/GPR.ipynb) | [Open in Colab](https://colab.research.google.com/github/Sadegh08/AI-Assisted-Analysis/blob/main/Mortar%28Cement%29/Mechanical_Properties/GPR/GPR.ipynb) |
| Mortar: mechanical properties | [SVR](Mortar%28Cement%29/Mechanical_Properties/SVR/SVR.ipynb) | [Open in Colab](https://colab.research.google.com/github/Sadegh08/AI-Assisted-Analysis/blob/main/Mortar%28Cement%29/Mechanical_Properties/SVR/SVR.ipynb) |
| Mortar: mechanical properties | [SHAP interpretation](Mortar%28Cement%29/Mechanical_Properties/SHAP/SHAP_GPR.ipynb) | [Open in Colab](https://colab.research.google.com/github/Sadegh08/AI-Assisted-Analysis/blob/main/Mortar%28Cement%29/Mechanical_Properties/SHAP/SHAP_GPR.ipynb) |
| Mortar: gauge factor | [Interpolation, regression and SHAP](Mortar%28Cement%29/Gauge_Factor/GFend.ipynb) | [Open in Colab](https://colab.research.google.com/github/Sadegh08/AI-Assisted-Analysis/blob/main/Mortar%28Cement%29/Gauge_Factor/GFend.ipynb) |

## Input data

| Analysis | Data source |
| --- | --- |
| Hydrometallurgy | Numerical data are defined in the notebook. |
| Briquette | Numerical data are defined in the notebook. |
| Bituminous mastic | [Aging index.xlsx](Bituminous_Mastic/Aging%20index.xlsx) |
| Mortar: mechanical properties | [Final.xlsx](Mortar%28Cement%29/Mechanical_Properties/Final.xlsx) |
| Mortar: gauge factor | Averaged experimental data are defined in the notebook. |

For the exact runtime locations, model-file dependency, and execution order, see the [input checklist](docs/REPRODUCIBILITY.md#input-files).

## Repository structure

```text
AI-Assisted-Analysis/
├── README.md
├── docs/
│   └── REPRODUCIBILITY.md
├── Hydrometallurgy/
│   ├── README.md
│   └── Hydrometallurgy_AI_Analysis.ipynb
├── Briquette/
│   ├── README.md
│   └── Briquette_AI_Analysis.ipynb
├── Bituminous_Mastic/
│   ├── README.md
│   ├── Aging index.xlsx
│   ├── GA_PSO/
│   ├── ANN/
│   ├── GPR/
│   ├── SVR/
│   └── SHAP/
└── Mortar(Cement)/
    ├── README.md
    ├── Mechanical_Properties/
    │   ├── Final.xlsx
    │   ├── GA_PSO/
    │   ├── ANN/
    │   ├── GPR/
    │   ├── SVR/
    │   └── SHAP/
    └── Gauge_Factor/
        ├── README.md
        └── GFend.ipynb
```

Each method directory contains its notebook and a dedicated README.

## Reproducibility

The notebooks contain the analysis procedures, while the section READMEs explain the modeling and validation choices. The [reproducibility guide](docs/REPRODUCIBILITY.md#record-the-runtime) describes how to record the Python and package versions used for a run.

Package versions are currently unpinned. Keep the runtime information, input data, repository commit, and exported results together when documenting an analysis.
