# Data Samples

This directory contains sample datasets used for flood susceptibility analysis in Jeju Island.

## Files

- `SCI_10grid_flood_risk_data_SAMPLE.csv` - Sample data at 10m spatial resolution
- `SCI_30grid_flood_risk_data_SAMPLE.csv` - Sample data at 30m spatial resolution
- `SCI_100grid_flood_risk_data_SAMPLE.csv` - Sample data at 100m spatial resolution

## Data Description

Each CSV file contains environmental and topographical features for grid cells at different spatial resolutions. The data includes:

- **Target Variable**: Flood occurrence/susceptibility indicator
- **Environmental Features**:
  - Topographical characteristics (elevation, slope, aspect, curvature)
  - Hydrological features (distance to rivers, drainage density, TWI)
  - Land use and land cover information
  - Soil characteristics
  - Rainfall data
  - Other relevant environmental variables

## Data Format

The data is structured with:
- Each row representing a grid cell at the specified resolution
- Columns representing different environmental features
- A binary or continuous target variable indicating flood susceptibility

## Privacy and Usage Notes

**Important**: Due to data privacy and file size constraints, only sample datasets are provided in this repository. These samples are intended to:

1. Demonstrate the data structure and format
2. Allow code execution and testing
3. Facilitate understanding of the analysis workflow

The sample data may be:
- A subset of the full dataset
- Anonymized or aggregated to protect sensitive information
- Representative of the full dataset's structure and characteristics

## Accessing Full Dataset

For access to the complete dataset or questions about data availability, please contact the authors (see main README.md).

## Data Processing

The raw data undergoes several preprocessing steps in `notebooks/01_data_preprocessing.ipynb`, including:
- Data cleaning and quality control
- Feature engineering
- Handling missing values
- Data normalization/standardization
- Train-test splitting

## Citation

If you use this data in your research, please cite the associated publication (see CITATION.cff in the root directory).
