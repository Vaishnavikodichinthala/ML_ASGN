1. Project Overview

This repository contains all code, figures, and the written tutorial for the assignment “Probability Calibration in Machine Learning Models.”
The project investigates why modern classifiers often produce miscalibrated probability outputs and demonstrates how calibration techniques—Platt scaling (sigmoid) and isotonic regression—improve reliability.

Three models are studied:

Logistic Regression (baseline)

Random Forest (uncalibrated + calibrated)

Gradient Boosting Machine (uncalibrated + calibrated)

The tutorial includes theory, mathematical foundations, experimental setup, results using real plots, and an interpretation of calibration performance using Brier Score, ROC-AUC, PR-AUC, and reliability diagrams.

2. Repository Structure
📂 calibration-tutorial/
│
├── notebooks/
│   └── VAISHNAVI(2).ipynb     # Full reproducible code
│
├── figures/
│   ├── reliability_plot_logreg.png
│   ├── reliability_rf_uncal.png
│
├── README.md                             # (this file)
├── LICENSE                               # MIT License
└── requirements.txt                      # Package list

3. How to Run the Code
Step 1 — Install dependencies
pip install -r requirements.txt


Main libraries used:

scikit-learn

matplotlib

numpy

seaborn

Step 2 — Open the Notebook
jupyter notebook notebooks/calibration_experiments.ipynb


All figures in the tutorial are generated automatically when the notebook is executed.

4. Dataset Description

A synthetic binary classification dataset is generated using sklearn.datasets.make_classification.

1000 samples

20 features (3 informative, 2 redundant)

Class imbalance ratio: 90% negative / 10% positive

Train/Validation/Test split: 60/20/20

This controlled dataset makes miscalibration easier to observe and highlight.

5. Reproducibility

All random seeds are fixed (random_state=42).

All plots are produced directly by the notebook.

Running the notebook end-to-end recreates:

reliability diagrams

calibration histograms

ROC & PR curves

summary tables for all models

6. Accessibility Notes

Figures use color-blind-friendly palettes.

Alt text is provided for all visualizations in the tutorial PDF.

Headings follow a clear hierarchical structure for screen-reader compatibility.

7. License

This project is released under the MIT License, allowing free use, modification, and distribution with attribution.
