# Results

This directory contains the outputs and results from the flood susceptibility analysis at different spatial resolutions.

## Directory Structure

```
results/
├── 10m_reviewer_response_results/
├── 30m_reviewer_response_results/
└── 100m_reviewer_response_results/
```

## Contents

Each subdirectory corresponds to a specific spatial resolution (10m, 30m, or 100m grid cells) and contains:

### Model Performance Results
- Cross-validation results
- Model evaluation metrics (accuracy, precision, recall, F1-score, AUC-ROC)
- Comparison tables between different algorithms

### SHAP Analysis Outputs
- Feature importance rankings
- SHAP summary plots
- SHAP interaction analysis results
- Feature interaction pairs and their effects

### Visualizations
- Model performance comparison figures
- SHAP visualizations
- Spatial distribution maps
- District-level analysis plots

### Data Tables
- `detailed_cv_results.csv` - Cross-validation performance metrics
- `shap_interaction_pairs.csv` - SHAP interaction analysis results
- `strong_interactions.csv` - Significant feature interactions
- `smote_robustness_comparison.csv` - SMOTE robustness test results
- `Table4_Updated.csv` - Updated results for manuscript tables

### Figures
- `Fig1_SMOTE_Robustness.png` - SMOTE robustness analysis visualization
- Additional figures generated during analysis

## Reviewer Response Results

The subdirectories are specifically organized to address reviewer comments and provide additional analyses:

1. **10m_reviewer_response_results/** - High-resolution (10m) analysis results
2. **30m_reviewer_response_results/** - Medium-resolution (30m) analysis results
3. **100m_reviewer_response_results/** - Lower-resolution (100m) analysis results

These results demonstrate the robustness of the findings across different spatial scales.

## File Formats

- **CSV files**: Tabular results that can be opened in spreadsheet software or loaded into Python/R
- **PNG files**: High-resolution figures suitable for publication
- **JSON files** (if present): Structured data for programmatic access

## Reproducibility

All results in this directory can be reproduced by running the Jupyter notebooks in the `notebooks/` directory in sequential order:

1. `01_data_preprocessing.ipynb`
2. `02_model_training_evaluation_shap.ipynb`
3. `03_district_level_analysis.ipynb`
4. Supplementary notebooks in `notebooks/supplementary/`

## Notes

- Results may vary slightly due to random seed variations in model training
- All analyses use the same preprocessing pipeline and model configurations
- The multi-resolution approach allows for scale-dependent analysis of flood susceptibility

## Usage

These results are referenced in the manuscript and can be used to:
- Verify reported findings
- Compare with alternative approaches
- Extend the analysis with additional methods
- Generate figures for presentations or publications

## Citation

If you use these results in your research, please cite the associated publication (see CITATION.cff in the root directory).
