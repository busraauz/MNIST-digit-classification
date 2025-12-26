MNIST Classification
====================

Overview
--------
This project walks through classic MNIST digit classification in a single
Jupyter notebook. The notebook starts with data loading and visualization,
then builds a binary classifier for detecting the digit 7, evaluates it with
multiple metrics and curves, and expands to multiclass, multilabel, and
multioutput classification.

What the Notebook Covers
------------------------
1) Load MNIST from OpenML, inspect shapes, and visualize a sample digit.
2) Split into train/test sets and shuffle training data.
3) Train a binary classifier (7 vs. not-7) with SGD.
4) Evaluate with:
   - Cross-validation accuracy
   - Confusion matrix (TN/FP/FN/TP)
   - Precision, recall, and F1
   - Precision/recall tradeoff and curves
   - ROC curve and ROC AUC
5) Compare SGD with a Random Forest classifier using ROC AUC.
6) Train multiclass classifiers:
   - One-vs-All (OvA) with SGD (default)
   - One-vs-One (OvO) with OneVsOneClassifier
   - Random Forest multiclass predictions
7) Evaluate multiclass accuracy and show that standard scaling improves it.
8) Perform error analysis with a confusion matrix heatmap and example
   misclassifications.
9) Train a multilabel classifier ("large" digit and "odd" digit labels).
10) Train a multioutput classifier to denoise noisy digits.

Dataset
-------
MNIST is loaded via `sklearn.datasets.fetch_openml`. Each image is 28x28
pixels (784 features). The notebook uses the standard split: 60,000 training
images and 10,000 test images.

Key Notes from the Notebook
---------------------------
- Binary classifier target: digit 7 vs. not-7.
- Confusion matrix breakdown for the 7-detector:
  - TN: 52,893
  - FP: 842
  - FN: 556
  - TP: 5,709
- Multiclass SGD accuracy is about 87% without scaling and about 90% with
  standard scaling.
- ROC AUC comparison shows Random Forest performs better than SGD.

Project Files
-------------
- `notebook.ipynb`: Main analysis and experiments.
- `requirements.txt`: Python dependencies.

Setup
-----
1) Create and activate a virtual environment:

```bash
python -m venv venv
source venv/bin/activate
```

2) Install dependencies:

```bash
pip install -r requirements.txt
```

Run the Notebook
----------------
```bash
jupyter notebook
```

Then open `notebook.ipynb` from the Jupyter UI.

Notes
-----
- All plots and metrics are generated inside the notebook.
- You can extend the notebook with more models or hyperparameter tuning.
