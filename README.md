# Classifier Comparison
This project compares classic classifiers (k-nearest neighbors, logistic regression, decision trees, and linear SVMs) on the UCI Bank Marketing dataset and extends the analysis with imbalance-aware metrics, thresholding, lift, and profitability views.

**Data Sources**
- UCI Bank Marketing dataset: [Bank Marketing (UCI)](https://archive.ics.uci.edu/ml/datasets/bank+marketing)
- CRISP-DM paper (local copy): `CRISP-DM-BANK.pdf`
- CRISP-DM paper (online): [Using Data Mining for Bank Direct Marketing](https://core.ac.uk/display/5566645)

**Notebook**
- Main analysis: `notebooks/classifier-comparison.ipynb`
- Figures saved to: `images/`

**Generated Outputs**
- Decile lift table: `data/decile_lift_table.csv`
- Profit threshold summary: `data/profit_threshold_summary.csv`
- Top call list (ranked by model score): `data/top_call_list.csv`

**Highlights**
- Cross-validated model comparison with PR-AUC, ROC-AUC, balanced accuracy, precision/recall, and F1.
- Threshold trade-offs aligned to business value (profit vs call cost).
- Cumulative gains and lift-by-decile for campaign targeting efficiency.

**Quick Start**
1. Install dependencies: `pip install -r requirements.txt`
2. Run the notebook: `jupyter notebook notebooks/classifier-comparison.ipynb`

**Environment Notes**
- Tested with Python 3.10+.
- If matplotlib cache errors appear, set `MPLCONFIGDIR` to a writable path (example: `/tmp/matplotlib`).
- For faster runs in constrained environments, reduce CV folds and avoid `n_jobs=-1`.
