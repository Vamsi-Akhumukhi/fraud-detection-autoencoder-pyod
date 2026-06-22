# Fraud Detection Using PyOD AutoEncoder

## Project Overview

This project implements a fraud detection system using the PyOD AutoEncoder model on an anonymized credit card transaction dataset from Kaggle.

The AutoEncoder is an unsupervised deep learning model that learns normal transaction patterns by reconstructing input data. Transactions that produce high reconstruction errors are considered anomalous and are flagged as potential fraudulent transactions.

---

## Dataset

**Source:**  
https://www.kaggle.com/datasets/whenamancodes/fraud-detection

### Dataset Characteristics

- Total Transactions: 284,807
- Legitimate Transactions: 284,315
- Fraudulent Transactions: 492
- Features: 30 numerical features plus the target variable (`Class`)
- Target Labels:
  - `0` = Legitimate Transaction
  - `1` = Fraudulent Transaction

The dataset is highly imbalanced, making anomaly detection techniques particularly useful for identifying fraudulent behavior.

---

## Methodology

### Data Preprocessing

1. Load the credit card transaction dataset.
2. Separate features and target variable.
3. Standardize numerical features using `StandardScaler`.
4. Calculate fraud contamination rate from the dataset.

### AutoEncoder Model

The PyOD AutoEncoder was trained to learn normal transaction behavior.

Model Parameters:

- Epochs: 30
- Batch Size: 64
- Contamination Rate: Dataset fraud rate (~0.17%)

### Anomaly Detection

After training:

- Reconstruction errors are computed for all transactions.
- Higher reconstruction errors indicate abnormal behavior.
- Transactions exceeding the anomaly threshold are classified as potential fraud.

---

## Technologies Used

- Python
- PyOD
- PyTorch
- Pandas
- NumPy
- Scikit-Learn
- Matplotlib
- Google Colab

---

## Results

The model successfully generated anomaly scores for all transactions and identified abnormal transaction patterns.

Output includes:

- Anomaly Score Visualization
- Threshold-Based Fraud Detection
- Confusion Matrix
- Classification Report
- ROC-AUC Score

Example Output:

- Fraud transactions exhibit significantly higher anomaly scores.
- Transactions above the threshold are flagged as potential anomalies.

---

## Repository Contents

| File | Description |
|--------|-------------|
| fraud_detection_autoencoder.py | Main Python source code |
| requirements.txt | Project dependencies |
| README.md | Project documentation |

---

## Installation

Install required packages:

```bash
pip install -r requirements.txt
```

## Running the Project

```bash
python fraud_detection_autoencoder.py
```

---

## Author

**Vamsi Akhumukhi**

Master of Science in Computer Science

Advanced Artificial Intelligence

Summer 2026

---

## References

- PyOD Documentation: https://pyod.readthedocs.io
- Kaggle Credit Card Fraud Dataset: https://www.kaggle.com/datasets/whenamancodes/fraud-detection
- Deep Learning and XAI Techniques for Anomaly Detection (Packt Publishing)
