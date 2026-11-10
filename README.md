# Heart Disease Risk Predictor

A small Flask web app that estimates the risk of heart disease from 13 clinical
inputs, using a Logistic Regression model trained on the UCI Cleveland Heart
Disease dataset.

> ⚠️ **Medical disclaimer:** This project is for educational purposes only. It is
> not a medical device and is not a substitute for professional medical advice,
> diagnosis, or treatment.

## Features

- Enter patient details in a web form and get a High/Low risk result with a
  probability percentage
- View all predictions made during the session on a Records page
- Model accuracy on the held-out test set: about 86.67%

## Tech stack

Python 3.11, Flask, scikit-learn, NumPy, pandas

## Getting started

### 1. Clone the repository

```bash
git clone https://github.com/YOUR-USERNAME/YOUR-REPO-NAME.git
cd YOUR-REPO-NAME
```

### 2. Create and activate a virtual environment

**Windows (PowerShell):**
```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

**Mac / Linux:**
```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Run the app

```bash
python app.py
```

Then open http://127.0.0.1:5000 in your browser.

## Notes

- **Model file:** `model.pkl` was created with scikit-learn 1.5.2. Install the
  pinned versions from `requirements.txt` to avoid version warnings. If
  `model.pkl` is deleted, the app retrains automatically (internet connection
  required to download the dataset).
- **Records are temporary:** Predictions are kept in memory only and disappear
  when the server restarts. This app is a demo and should not be deployed
  publicly with real patient data.

## Dataset

[UCI Machine Learning Repository: Heart Disease (Cleveland)](https://archive.ics.uci.edu/dataset/45/heart+disease)

## Author

Shruthe O