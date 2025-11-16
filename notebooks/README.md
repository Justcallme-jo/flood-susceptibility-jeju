# Analysis Notebooks

This directory contains Jupyter notebooks for the flood susceptibility analysis workflow.

## Main Analysis Notebooks

Run these notebooks in sequential order:

### 1. Data Preprocessing (`01_data_preprocessing.ipynb`)

**Purpose**: Prepare raw data for machine learning analysis

**Contents**:
- Data loading and initial exploration
- CSV format conversion and standardization
- Data cleaning and quality control
- Feature engineering
- Handling missing values
- Data integration across different sources
- Train-test split preparation

**Outputs**: Cleaned and preprocessed datasets ready for modeling

---

### 2. Model Training, Evaluation, and SHAP Analysis (`02_model_training_evaluation_shap.ipynb`)

**Purpose**: Train machine learning models and interpret results

**Contents**:
- Model training with multiple algorithms:
  - Random Forest
  - XGBoost
  - CatBoost
- Hyperparameter tuning and cross-validation
- Model performance evaluation:
  - Accuracy, precision, recall, F1-score
  - ROC-AUC curves
  - Confusion matrices
- SHAP (SHapley Additive exPlanations) analysis:
  - Feature importance calculation
  - SHAP summary plots
  - Feature interaction detection
  - Individual prediction explanations

**Outputs**:
- Trained models
- Performance metrics
- SHAP values and visualizations
- Feature importance rankings

---

### 3. District-Level Analysis (`03_district_level_analysis.ipynb`)

**Purpose**: Aggregate and analyze flood susceptibility at administrative district level

**Contents**:
- Spatial aggregation of grid-level predictions
- District-level risk assessment
- Comparative analysis across administrative regions
- Visualization of spatial patterns
- Statistical summaries by district

**Outputs**:
- District-level flood susceptibility maps
- Comparative statistics
- Regional risk rankings

---

## Supplementary Analyses

The `supplementary/` subdirectory contains robustness tests using SMOTE (Synthetic Minority Over-sampling Technique):

### S1. SMOTE Robustness - 10m Resolution (`supplementary/S1_SMOTE_robustness_10m.ipynb`)

Tests model robustness with SMOTE at 10m spatial resolution

### S2. SMOTE Robustness - 30m Resolution (`supplementary/S2_SMOTE_robustness_30m.ipynb`)

Tests model robustness with SMOTE at 30m spatial resolution

### S3. SMOTE Robustness - 100m Resolution (`supplementary/S3_SMOTE_robustness_100m.ipynb`)

Tests model robustness with SMOTE at 100m spatial resolution

**Purpose of SMOTE Analysis**:
- Address class imbalance in training data
- Test model stability under different sampling strategies
- Validate findings across different data balancing approaches
- Respond to reviewer comments on model robustness

---

## Running the Notebooks

### Prerequisites

Ensure you have installed all required packages:
```bash
pip install -r ../requirements.txt
```

### Execution Order

1. Start with `01_data_preprocessing.ipynb`
2. Proceed to `02_model_training_evaluation_shap.ipynb`
3. Run `03_district_level_analysis.ipynb`
4. Optionally run supplementary notebooks for additional analyses

### Expected Runtime

- Notebook 01: ~5-15 minutes (depending on data size)
- Notebook 02: ~30-60 minutes (includes model training and SHAP calculations)
- Notebook 03: ~10-20 minutes
- Supplementary notebooks: ~20-30 minutes each

**Note**: Runtime varies based on:
- Hardware specifications (CPU/GPU)
- Dataset size
- Number of cross-validation folds
- SHAP calculation settings

### Output Locations

- Processed data: Saved in memory or written to temporary files
- Results: Written to `../results/` directory
- Figures: Saved in appropriate results subdirectories

## Notebook Structure

Each notebook follows a consistent structure:

1. **Setup**: Import libraries and configure settings
2. **Data Loading**: Load required datasets
3. **Analysis**: Main analytical procedures
4. **Visualization**: Generate plots and figures
5. **Export**: Save results to files

## Notes for Reviewers

- All code cells are designed to run sequentially from top to bottom
- Random seeds are set for reproducibility where applicable
- Inline comments explain key analytical decisions
- Visualizations are publication-ready
- Results match those reported in the manuscript

## Customization

To adapt these notebooks for your own analysis:

1. Modify file paths in data loading cells
2. Adjust model hyperparameters in configuration sections
3. Update visualization parameters for different output formats
4. Add or remove features in preprocessing steps

## Troubleshooting

**Common Issues**:

- **Memory errors**: Reduce batch size or use sampling for large datasets
- **Missing dependencies**: Check `requirements.txt` and install missing packages
- **Font errors** (Korean text): Ensure appropriate fonts are installed (e.g., AppleGothic, NanumGothic)
- **Path errors**: Verify relative paths match your directory structure

**Korean Font Setup** (for visualization with Korean text):
```python
# For macOS
plt.rc("font", family="AppleGothic")

# For Windows
plt.rc("font", family="Malgun Gothic")

# For Linux
plt.rc("font", family="NanumGothic")
```

## Contact

For questions about the notebooks or analytical methods, please contact the authors (see main README.md).
