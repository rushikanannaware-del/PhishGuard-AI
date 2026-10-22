# PhishGuard AI — Phishing URL Classification

**Author:** Mahesh Nannaware  
**Project type:** Cybersecurity / Machine Learning

## Overview
PhishGuard AI is a machine-learning project that classifies examples from the PhiUSIIL Phishing URL Dataset as phishing (`0`) or legitimate (`1`). It uses a Random Forest classifier and visualizes evaluation metrics and feature importance.

## Dataset
- Name: PhiUSIIL Phishing URL Dataset
- Official source: https://archive.ics.uci.edu/dataset/967/phiusiil+phishing+url+dataset
- Download the CSV and upload `PhiUSIIL_Phishing_URL_Dataset.csv` to Google Colab when prompted.

## Technologies
Python, pandas, NumPy, scikit-learn, Matplotlib, Seaborn, joblib, Google Colab.

## Run
1. Open `PhishGuardAI.ipynb` in Google Colab.
2. Upload `PhiUSIIL_Phishing_URL_Dataset.csv` when prompted.
3. Run the notebook cells from top to bottom.
4. The notebook trains/evaluates the model and saves `phishguard_model.pkl` and `phishguard_features.pkl`.

## Label mapping
- `0` = phishing
- `1` = legitimate

## Important limitations
This is a dataset-based research/demo prototype, not a live URL scanner. The trained model uses engineered numeric features, including some that describe webpage content (e.g., number of images and external references). Those features cannot be calculated from a URL string alone. The displayed website URL is an example from the dataset, not a live scan.

Preliminary experiments showed unusually high accuracy (up to 99.98%). This score should not be interpreted as expected real-world performance without further testing for dataset artifacts, leakage, duplicate domains, and generalization on an independent test set.

## Files
- `PhishGuardAI.ipynb` — reproducible notebook
- `requirements.txt` — Python dependencies
- `PhishGuardAI_ProjectReport.docx` — project report
- `README.md` — this overview
