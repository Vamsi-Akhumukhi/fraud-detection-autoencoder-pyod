# Fraud Detection using PyOD AutoEncoder

This project uses a PyOD AutoEncoder model to detect fraudulent credit card transactions. The dataset is an anonymized credit card fraud dataset from Kaggle.

## Dataset

Dataset source: https://www.kaggle.com/datasets/whenamancodes/fraud-detection

The dataset contains 284,807 transactions and 31 columns. The target column is `Class`, where:

- 0 = Normal transaction
- 1 = Fraudulent transaction

## Method

The AutoEncoder learns to reconstruct normal transaction patterns. Fraudulent or unusual transactions produce higher reconstruction errors and are detected as anomalies.

## Files

- `fraud_detection_autoencoder.py` - Python source code
- `fraud_detection_autoencoder.ipynb` - Colab notebook
- `requirements.txt` - Project dependencies
- `README.md` - Project documentation

## How to Run

Install dependencies:

```bash
pip install -r requirements.txt
