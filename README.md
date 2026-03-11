# Anomaly Detection Project

This project implements anomaly detection on a health metric dataset using machine learning. It identifies unusual data points that deviate significantly from normal patterns.

## Project Structure

- `note_book.ipynb`: Jupyter notebook containing the data analysis, machine learning model, and results.
- `scatter_plot_dataset.csv`: The dataset containing health metrics (`feature_x`, `feature_y`) used for detection.

## Implementation Details

### Anomaly Detection Model
The project uses the **Isolation Forest** algorithm from `scikit-learn`. 
- **Algorithm**: Isolation Forest works by isolating observations by randomly selecting a feature and then randomly selecting a split value between the maximum and minimum values of the selected feature.
- **Labeling**: Results are mapped to:
  - `0`: Normal
  - `1`: Anomaly (Outlier)

### Visualization
The results are visualized using `matplotlib` scatter plots. 
- Normal points are color-coded in blue.
- Anomalies are highlighted in red for easy identification.

## Getting Started

### Prerequisites

You will need Python installed along with the following libraries:
- `pandas`
- `matplotlib`
- `scikit-learn`

You can install these directly within the notebook or via terminal:
```bash
pip install pandas matplotlib scikit-learn
```

### Running the Notebook

1. Open `note_book.ipynb`.
2. Run the cells in order to:
   - Install dependencies.
   - Load the dataset.
   - Train the Isolation Forest model.
   - Visualize the anomalies.

## Fixes Applied
- Resolved `ValueError` in data visualization indexing.
- Fixed `InvalidIndexError` by using `.iloc` for Pandas indexing.
- Switched from deprecated `sklearn` package to `scikit-learn`.
