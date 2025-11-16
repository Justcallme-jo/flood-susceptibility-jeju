# Flood Susceptibility Mapping in Jeju Island

This repository contains the code and data for flood susceptibility analysis in Jeju Island, South Korea, using machine learning approaches.

## Overview

This study develops and evaluates machine learning models for flood susceptibility mapping at multiple spatial resolutions (10m, 30m, and 100m grid cells). The analysis includes:

- Data preprocessing and feature engineering
- Model training and evaluation using multiple algorithms (Random Forest, XGBoost, CatBoost)
- SHAP (SHapley Additive exPlanations) analysis for model interpretability
- District-level flood risk assessment
- Robustness testing with SMOTE (Synthetic Minority Over-sampling Technique)

## Repository Structure

```
flood-susceptibility-jeju/
├── notebooks/              # Jupyter notebooks for analysis
│   ├── 01_data_preprocessing.ipynb
│   ├── 02_model_training_evaluation_shap.ipynb
│   ├── 03_district_level_analysis.ipynb
│   └── supplementary/      # Supplementary analyses
│       ├── S1_SMOTE_robustness_10m.ipynb
│       ├── S2_SMOTE_robustness_30m.ipynb
│       └── S3_SMOTE_robustness_100m.ipynb
├── data-samples/           # Sample datasets
│   ├── SCI_10grid_flood_risk_data_SAMPLE.csv
│   ├── SCI_30grid_flood_risk_data_SAMPLE.csv
│   └── SCI_100grid_flood_risk_data_SAMPLE.csv
├── results/                # Analysis results and figures
│   ├── 10m_reviewer_response_results/
│   ├── 30m_reviewer_response_results/
│   └── 100m_reviewer_response_results/
├── requirements.txt        # Python dependencies
└── README.md              # This file
```

## Requirements

- Python 3.8 or higher
- Jupyter Notebook or JupyterLab

See `requirements.txt` for a complete list of Python package dependencies.

## Installation

1. Clone this repository:
```bash
git clone https://github.com/Justcallme-jo/flood-susceptibility-jeju.git
cd flood-susceptibility-jeju
```

2. Create a virtual environment (recommended):
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install required packages:
```bash
pip install -r requirements.txt
```

## Usage

The analysis workflow is organized into sequential Jupyter notebooks:

### 1. Data Preprocessing
```bash
jupyter notebook notebooks/01_data_preprocessing.ipynb
```
This notebook handles:
- Data loading and cleaning
- Feature engineering
- Data integration and preparation for modeling

### 2. Model Training, Evaluation, and SHAP Analysis
```bash
jupyter notebook notebooks/02_model_training_evaluation_shap.ipynb
```
This notebook includes:
- Training multiple machine learning models (Random Forest, XGBoost, CatBoost)
- Model evaluation and performance metrics
- SHAP analysis for feature importance and interaction effects

### 3. District-Level Analysis
```bash
jupyter notebook notebooks/03_district_level_analysis.ipynb
```
This notebook provides:
- Spatial aggregation of flood susceptibility at district level
- Comparative analysis across administrative regions

### Supplementary Analyses

The `notebooks/supplementary/` directory contains robustness tests using SMOTE for each spatial resolution:
- `S1_SMOTE_robustness_10m.ipynb` - 10m resolution analysis
- `S2_SMOTE_robustness_30m.ipynb` - 30m resolution analysis
- `S3_SMOTE_robustness_100m.ipynb` - 100m resolution analysis

## Data

Due to data privacy and size constraints, only sample datasets are included in the `data-samples/` directory. These samples demonstrate the data structure and format used in the analysis.

**Data Format**: Each CSV file contains flood risk data with environmental and topographical features for grid cells at different resolutions.

For access to the complete dataset, please contact the authors.

## Results

The `results/` directory contains analysis outputs organized by spatial resolution:
- Model performance metrics
- SHAP analysis results
- Visualization outputs
- Comparison tables

## Citation

If you use this code or data in your research, please cite:

```
[To be added: Paper citation]
```

## License

[To be added: Appropriate license]

## Contact

For questions or collaboration inquiries, please contact:

- [Author name and email to be added]

## Acknowledgments

This research was conducted as part of [project/institution name to be added].

## Notes for Reviewers

- All notebooks are designed to run sequentially from 01 to 03
- Sample data is provided to demonstrate the workflow
- Complete results are available in the `results/` directory
- Supplementary notebooks provide additional robustness analyses requested during peer review
