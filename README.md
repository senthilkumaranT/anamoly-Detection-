# 🏥 Advanced Health Metric Anomaly Detection

This repository contains a high-precision anomaly detection framework designed to monitor health metrics and identify significant deviations using the **Isolation Forest** machine learning algorithm.s 

## 🌟 Project Overview

Monitoring health metrics requires a robust system to differentiate between natural physiological variance and genuine anomalies. This project utilizes an unsupervised learning approach to score and classify data points based on their "degree of isolation" within a multi-dimensional feature space.

### 🧠 Core Technology: Isolation Forest
Unlike traditional anomaly detection methods that model "normal" points and find outliers by distance, **Isolation Forest** explicitly isolates anomalies.
- **How it works**: It builds an ensemble of "Isolation Trees." Since anomalies are few and different, they are partitioned closer to the root of the tree, requiring fewer splits to isolate than normal points.
- **Efficiency**: This approach is highly effective for high-dimensional data and does not require a labeled "normal" dataset for training.

## 📊 Feature Highlights

- **Automated Labeling**: Segregates data into `Normal (0)` and `Anomaly (1)` with adjustable contamination thresholds.
- **Dynamic Visualization**: High-resolution scatter plots that clearly demarcate detected outliers using color-coded semantics.
- **Robust Preprocessing**: Includes automated handling of data indexing and mapping to ensure consistent results across re-runs.

## 🛠️ Getting Started

### Installation
Ensure your environment has the following dependencies:
```bash
pip install pandas matplotlib scikit-learn
```

### Usage
Execute the [note_book.ipynb](file:///Users/spurge/Desktop/anamoly%20Detection%20/note_book.ipynb) sequentially. The pipeline includes:
1. **Data Acquisition**: Loading health metrics from CSV.
2. **Model Training**: Fitting the Isolation Forest to the feature set.
3. **Inference**: Generating anomaly scores and status flags.
4. **Analysis**: Visual examination of the result distribution.

## 🚀 Key Improvements
- **Package Modernization**: Transitioned to `scikit-learn` for long-term stability.
- **Index Optimization**: Implemented `.iloc` based positioning to prevent common Pandas indexing errors.
- **Visual Clarity**: Enhanced plot aesthetics with legends, grids, and semantic color mapping.
