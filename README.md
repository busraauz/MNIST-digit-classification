MNIST Classification
====================

Overview
--------
This project explores classic MNIST digit classification in a Jupyter
notebook. It covers:
- Binary classification (e.g., 7 vs. not-7) using SGD.
- Evaluation with cross-validation, confusion matrix, precision, recall,
  F1, PR curve, ROC curve, and ROC AUC.
- A comparison with a Random Forest classifier.
- A brief introduction to multiclass classification.

Dataset
-------
The notebook uses the MNIST dataset via `sklearn.datasets.fetch_openml`.
Each image is 28x28 pixels (784 features).

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
- Metrics and plots are computed inside the notebook.
- You can extend the notebook with additional models or tuning.
